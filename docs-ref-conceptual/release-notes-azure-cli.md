---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/20/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 36b57d52a5851275fd317240e5c2c95171a99e7e
ms.sourcegitcommit: 22b73d56602c1c4e647ed2c5af3d596a2f6a7ed5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2018
ms.locfileid: "52267332"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="39530-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="39530-103">Azure CLI release notes</span></span>
## <a name="november-20-2018"></a><span data-ttu-id="39530-104">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="39530-104">November 20, 2018</span></span>

<span data-ttu-id="39530-105">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="39530-105">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="39530-106">コア</span><span class="sxs-lookup"><span data-stu-id="39530-106">Core</span></span>
* <span data-ttu-id="39530-107">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-107">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="39530-108">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-108">ACR</span></span>
* <span data-ttu-id="39530-109">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-109">Added context token to task step</span></span>
* <span data-ttu-id="39530-110">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-110">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="39530-111">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-111">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-112">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-112">Appservice</span></span>
* <span data-ttu-id="39530-113">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-113">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="39530-114">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="39530-114">Updated the default `node_version`.</span></span> <span data-ttu-id="39530-115">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="39530-115">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="39530-116">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-116">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="39530-117">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-117">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="39530-118">IotCentral</span><span class="sxs-lookup"><span data-stu-id="39530-118">IotCentral</span></span>
* <span data-ttu-id="39530-119">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-119">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-120">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-120">KeyVault</span></span>
* <span data-ttu-id="39530-121">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-121">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="39530-122">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-122">Network</span></span>
* <span data-ttu-id="39530-123">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-123">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="39530-124">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-124">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="39530-125">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-125">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="39530-126">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-126">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-127">Rdbms</span><span class="sxs-lookup"><span data-stu-id="39530-127">Rdbms</span></span>
* <span data-ttu-id="39530-128">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-128">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="39530-129">Rbac</span><span class="sxs-lookup"><span data-stu-id="39530-129">Rbac</span></span>
* <span data-ttu-id="39530-130">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-130">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="39530-131">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-131">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="39530-132">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-132">Storage</span></span>
* <span data-ttu-id="39530-133">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-133">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="39530-134">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-134">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="39530-135">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-135">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="39530-136">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="39530-136">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="39530-137">VM</span><span class="sxs-lookup"><span data-stu-id="39530-137">VM</span></span>
* <span data-ttu-id="39530-138">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-138">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="39530-139">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-139">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="39530-140">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="39530-140">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="39530-141">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-141">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="39530-142">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-142">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="39530-143">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-143">Added `snapshot wait` command</span></span>
* <span data-ttu-id="39530-144">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-144">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="39530-145">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="39530-145">November 6, 2018</span></span>

<span data-ttu-id="39530-146">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="39530-146">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="39530-147">コア</span><span class="sxs-lookup"><span data-stu-id="39530-147">Core</span></span>
* <span data-ttu-id="39530-148">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-148">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="39530-149">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-149">ACR</span></span>
* <span data-ttu-id="39530-150">タスク ソース トリガーのコミットおよびプル要求の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-150">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="39530-151">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-151">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="39530-152">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-152">ACS</span></span>
* <span data-ttu-id="39530-153">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-153">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="39530-154">Advisor</span><span class="sxs-lookup"><span data-stu-id="39530-154">Advisor</span></span>
* <span data-ttu-id="39530-155">GA リリース</span><span class="sxs-lookup"><span data-stu-id="39530-155">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="39530-156">AMS</span><span class="sxs-lookup"><span data-stu-id="39530-156">AMS</span></span>
* <span data-ttu-id="39530-157">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-157">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="39530-158">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-158">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="39530-159">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-159">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="39530-160">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-160">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="39530-161">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-161">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="39530-162">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-162">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="39530-163">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-163">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="39530-164">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="39530-164">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="39530-165">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-165">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="39530-166">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-166">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="39530-167">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="39530-167">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="39530-168">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="39530-168">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="39530-169">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="39530-169">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="39530-170">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="39530-170">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="39530-171">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-171">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="39530-172">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="39530-172">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="39530-173">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="39530-173">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-174">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-174">AppService</span></span>
* <span data-ttu-id="39530-175">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-175">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="39530-176">構成</span><span class="sxs-lookup"><span data-stu-id="39530-176">Configure</span></span>
* <span data-ttu-id="39530-177">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-177">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="39530-178">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-178">Container</span></span>
* <span data-ttu-id="39530-179">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-179">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="39530-180">EventHub</span><span class="sxs-lookup"><span data-stu-id="39530-180">EventHub</span></span>
* <span data-ttu-id="39530-181">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-181">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-182">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-182">Interactive</span></span>
* <span data-ttu-id="39530-183">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="39530-183">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-184">監視</span><span class="sxs-lookup"><span data-stu-id="39530-184">Monitor</span></span>
* <span data-ttu-id="39530-185">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-185">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="39530-186">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-186">Network</span></span>
* <span data-ttu-id="39530-187">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-187">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="39530-188">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-188">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="39530-189">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-189">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="39530-190">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-190">Profile</span></span>
* <span data-ttu-id="39530-191">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-191">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-192">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-192">RDBMS</span></span>
* <span data-ttu-id="39530-193">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-193">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="39530-194">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-194">Resource</span></span>
* <span data-ttu-id="39530-195">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-195">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="39530-196">Role</span><span class="sxs-lookup"><span data-stu-id="39530-196">Role</span></span>
* <span data-ttu-id="39530-197">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-197">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="39530-198">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-198">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="39530-199">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-199">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="39530-200">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-200">Storage</span></span>
* <span data-ttu-id="39530-201">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="39530-201">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="39530-202">VM</span><span class="sxs-lookup"><span data-stu-id="39530-202">VM</span></span>
* <span data-ttu-id="39530-203">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-203">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="39530-204">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-204">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="39530-205">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-205">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="39530-206">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-206">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="39530-207">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="39530-207">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="39530-208">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-208">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="39530-209">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="39530-209">October 23, 2018</span></span>

<span data-ttu-id="39530-210">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="39530-210">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="39530-211">コア</span><span class="sxs-lookup"><span data-stu-id="39530-211">Core</span></span>
* <span data-ttu-id="39530-212">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-212">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="39530-213">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-213">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="39530-214">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-214">ACR</span></span>
* <span data-ttu-id="39530-215">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-215">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="39530-216">CDN</span><span class="sxs-lookup"><span data-stu-id="39530-216">CDN</span></span>
* <span data-ttu-id="39530-217">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="39530-217">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="39530-218">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-218">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="39530-219">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-219">Container</span></span>
* <span data-ttu-id="39530-220">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-220">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="39530-221">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-221">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="39530-222">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-222">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="39530-223">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-223">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="39530-224">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-224">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="39530-225">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-225">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="39530-226">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-226">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39530-227">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-227">CosmosDB</span></span>
* <span data-ttu-id="39530-228">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-228">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-229">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-229">Interactive</span></span>
* <span data-ttu-id="39530-230">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-230">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="39530-231">IoT Central</span><span class="sxs-lookup"><span data-stu-id="39530-231">IoT Central</span></span>
* <span data-ttu-id="39530-232">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-232">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="39530-233">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="39530-233">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-234">監視</span><span class="sxs-lookup"><span data-stu-id="39530-234">Monitor</span></span>
* <span data-ttu-id="39530-235">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="39530-235">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="39530-236">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-236">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="39530-237">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-237">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="39530-238">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-238">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="39530-239">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-239">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="39530-240">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-240">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="39530-241">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="39530-241">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="39530-242">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-242">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="39530-243">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-243">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="39530-244">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-244">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="39530-245">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-245">Network</span></span>
* <span data-ttu-id="39530-246">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-246">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="39530-247">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-247">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="39530-248">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39530-248">ServiceBus</span></span>
* <span data-ttu-id="39530-249">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-249">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="39530-250">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-250">SQL</span></span>
* <span data-ttu-id="39530-251">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-251">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="39530-252">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-252">Storage</span></span>
* <span data-ttu-id="39530-253">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-253">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="39530-254">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-254">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="39530-255">VM</span><span class="sxs-lookup"><span data-stu-id="39530-255">VM</span></span>
* <span data-ttu-id="39530-256">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="39530-256">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="39530-257">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-257">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="39530-258">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-258">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="39530-259">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="39530-259">October 16, 2018</span></span>

<span data-ttu-id="39530-260">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="39530-260">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="39530-261">VM</span><span class="sxs-lookup"><span data-stu-id="39530-261">VM</span></span>
* <span data-ttu-id="39530-262">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-262">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="39530-263">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="39530-263">October 9, 2018</span></span>

<span data-ttu-id="39530-264">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="39530-264">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="39530-265">コア</span><span class="sxs-lookup"><span data-stu-id="39530-265">Core</span></span>
* <span data-ttu-id="39530-266">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-266">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="39530-267">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-267">ACR</span></span>
* <span data-ttu-id="39530-268">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-268">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="39530-269">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-269">ACS</span></span>
* <span data-ttu-id="39530-270">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="39530-270">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="39530-271">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-271">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="39530-272">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-272">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="39530-273">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-273">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="39530-274">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-274">Container</span></span>
* <span data-ttu-id="39530-275">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-275">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="39530-276">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-276">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="39530-277">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="39530-277">Event Hub</span></span>
* <span data-ttu-id="39530-278">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-278">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="39530-279">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-279">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="39530-280">拡張機能</span><span class="sxs-lookup"><span data-stu-id="39530-280">Extensions</span></span>
* <span data-ttu-id="39530-281">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-281">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="39530-282">HDInsight</span><span class="sxs-lookup"><span data-stu-id="39530-282">HDInsight</span></span>
* <span data-ttu-id="39530-283">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-283">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="39530-284">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-284">IoT</span></span>
* <span data-ttu-id="39530-285">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-285">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-286">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-286">KeyVault</span></span>
* <span data-ttu-id="39530-287">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-287">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="39530-288">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-288">Network</span></span>
* <span data-ttu-id="39530-289">`network dns zone create` を修正しました: ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="39530-289">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="39530-290">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="39530-290">See #6052</span></span>
* <span data-ttu-id="39530-291">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-291">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="39530-292">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="39530-292">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="39530-293">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-293">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="39530-294">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-294">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="39530-295">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-295">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="39530-296">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-296">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="39530-297">Role</span><span class="sxs-lookup"><span data-stu-id="39530-297">Role</span></span>
* <span data-ttu-id="39530-298">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-298">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="39530-299">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-299">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="39530-300">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-300">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="39530-301">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-301">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="39530-302">Service Bus</span><span class="sxs-lookup"><span data-stu-id="39530-302">Service Bus</span></span>
* <span data-ttu-id="39530-303">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-303">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="39530-304">VM</span><span class="sxs-lookup"><span data-stu-id="39530-304">VM</span></span>
* <span data-ttu-id="39530-305">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-305">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="39530-306">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-306">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="39530-307">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-307">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="39530-308">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-308">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="39530-309">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-309">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="39530-310">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-310">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="39530-311">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="39530-311">September 21, 2018</span></span>

<span data-ttu-id="39530-312">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="39530-312">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="39530-313">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-313">ACR</span></span>
* <span data-ttu-id="39530-314">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-314">Added ACR Task commands</span></span>
* <span data-ttu-id="39530-315">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-315">Added quick run command</span></span>
* <span data-ttu-id="39530-316">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-316">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="39530-317">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-317">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="39530-318">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-318">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="39530-319">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-319">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="39530-320">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-320">ACS</span></span>
* <span data-ttu-id="39530-321">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-321">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="39530-322">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-322">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-323">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-323">AppService</span></span>

* <span data-ttu-id="39530-324">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-324">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="39530-325">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-325">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="39530-326">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-326">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="39530-327">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-327">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="39530-328">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-328">Batch</span></span>
* <span data-ttu-id="39530-329">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-329">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="39530-330">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-330">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="39530-331">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-331">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="39530-332">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-332">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="39530-333">Batch AI</span><span class="sxs-lookup"><span data-stu-id="39530-333">Batch AI</span></span> 
* <span data-ttu-id="39530-334">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-334">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="39530-335">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="39530-335">Cognitive Services</span></span>
* <span data-ttu-id="39530-336">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-336">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="39530-337">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-337">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="39530-338">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-338">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="39530-339">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-339">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="39530-340">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-340">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="39530-341">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-341">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="39530-342">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-342">Container</span></span>
* <span data-ttu-id="39530-343">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-343">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="39530-344">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-344">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="39530-345">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-345">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="39530-346">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-346">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="39530-347">DataLake</span><span class="sxs-lookup"><span data-stu-id="39530-347">Datalake</span></span>
* <span data-ttu-id="39530-348">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-348">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="39530-349">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="39530-349">Interactive Shell</span></span>
* <span data-ttu-id="39530-350">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-350">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="39530-351">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-351">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="39530-352">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-352">IoT</span></span>
* <span data-ttu-id="39530-353">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-353">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="39530-354">Key Vault</span><span class="sxs-lookup"><span data-stu-id="39530-354">Key Vault</span></span>
* <span data-ttu-id="39530-355">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-355">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="39530-356">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-356">Network</span></span>
* <span data-ttu-id="39530-357">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-357">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="39530-358">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-358">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="39530-359">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-359">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="39530-360">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-360">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="39530-361">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-361">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="39530-362">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-362">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="39530-363">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="39530-363">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="39530-364">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-364">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="39530-365">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-365">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="39530-366">`network express-route create/update`: `--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-366">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="39530-367">`network vnet subnet create/update`: `--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-367">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="39530-368">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-368">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="39530-369">`network traffic-manager profile create/update`: 監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、`--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-369">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="39530-370">`network lb frontend-ip create/update`: プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="39530-370">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="39530-371">`dns record-set * create/update`: `--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-371">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="39530-372">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-372">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="39530-373">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-373">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="39530-374">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-374">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-375">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-375">RDBMS</span></span>
* <span data-ttu-id="39530-376">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-376">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="39530-377">予約</span><span class="sxs-lookup"><span data-stu-id="39530-377">Reservation</span></span>
* <span data-ttu-id="39530-378">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-378">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="39530-379">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-379">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="39530-380">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="39530-380">Manage App</span></span>
* <span data-ttu-id="39530-381">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-381">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="39530-382">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-382">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="39530-383">Role</span><span class="sxs-lookup"><span data-stu-id="39530-383">Role</span></span>
* <span data-ttu-id="39530-384">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-384">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="39530-385">SignalR</span><span class="sxs-lookup"><span data-stu-id="39530-385">SignalR</span></span>
* <span data-ttu-id="39530-386">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-386">First release</span></span>

### <a name="storage"></a><span data-ttu-id="39530-387">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-387">Storage</span></span>
* <span data-ttu-id="39530-388">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-388">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="39530-389">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-389">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="39530-390">VM</span><span class="sxs-lookup"><span data-stu-id="39530-390">VM</span></span>
* <span data-ttu-id="39530-391">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="39530-391">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="39530-392">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-392">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="39530-393">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="39530-393">August 28, 2018</span></span>

<span data-ttu-id="39530-394">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="39530-394">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="39530-395">コア</span><span class="sxs-lookup"><span data-stu-id="39530-395">Core</span></span>

* <span data-ttu-id="39530-396">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-396">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="39530-397">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-397">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="39530-398">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-398">ACR</span></span>

* <span data-ttu-id="39530-399">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-399">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="39530-400">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-400">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="39530-401">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-401">ACS</span></span>

* <span data-ttu-id="39530-402">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-402">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="39530-403">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-403">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-404">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-404">AppService</span></span>

* <span data-ttu-id="39530-405">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-405">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="39530-406">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-406">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="39530-407">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-407">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="39530-408">バックアップ</span><span class="sxs-lookup"><span data-stu-id="39530-408">Backup</span></span>

* <span data-ttu-id="39530-409">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-409">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="39530-410">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="39530-410">Bot Service</span></span>

* <span data-ttu-id="39530-411">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="39530-411">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="39530-412">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="39530-412">Cognitive Services</span></span>

* <span data-ttu-id="39530-413">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-413">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="39530-414">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-414">IoT</span></span>

* <span data-ttu-id="39530-415">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-415">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-416">監視</span><span class="sxs-lookup"><span data-stu-id="39530-416">Monitor</span></span>

* <span data-ttu-id="39530-417">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-417">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="39530-418">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-418">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="39530-419">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-419">Network</span></span>

* <span data-ttu-id="39530-420">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-420">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="39530-421">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-421">Resource</span></span>

* <span data-ttu-id="39530-422">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-422">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="39530-423">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-423">Storage</span></span>

* <span data-ttu-id="39530-424">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-424">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="39530-425">VM</span><span class="sxs-lookup"><span data-stu-id="39530-425">VM</span></span>

* <span data-ttu-id="39530-426">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-426">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="39530-427">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-427">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="39530-428">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="39530-428">Auguest 14, 2018</span></span>

<span data-ttu-id="39530-429">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="39530-429">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="39530-430">コア</span><span class="sxs-lookup"><span data-stu-id="39530-430">Core</span></span>

* <span data-ttu-id="39530-431">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-431">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="39530-432">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-432">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="39530-433">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="39530-433">Telemetry</span></span>

* <span data-ttu-id="39530-434">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-434">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="39530-435">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-435">ACR</span></span>

* <span data-ttu-id="39530-436">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-436">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="39530-437">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-437">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="39530-438">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-438">ACS</span></span>

* <span data-ttu-id="39530-439">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-439">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="39530-440">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-440">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="39530-441">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-441">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="39530-442">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-442">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="39530-443">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-443">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="39530-444">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-444">AppService</span></span>

* <span data-ttu-id="39530-445">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-445">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="39530-446">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-446">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="39530-447">BatchAI</span><span class="sxs-lookup"><span data-stu-id="39530-447">BatchAI</span></span>

* <span data-ttu-id="39530-448">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-448">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="39530-449">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-449">Container</span></span>

* <span data-ttu-id="39530-450">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-450">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="39530-451">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-451">IoT</span></span>

* <span data-ttu-id="39530-452">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-452">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="39530-453">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-453">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="39530-454">Iot Central</span><span class="sxs-lookup"><span data-stu-id="39530-454">Iot Central</span></span>

* <span data-ttu-id="39530-455">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-455">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-456">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-456">KeyVault</span></span>


* <span data-ttu-id="39530-457">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-457">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="39530-458">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-458">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="39530-459">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-459">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="39530-460">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-460">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="39530-461">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-461">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="39530-462">リレー</span><span class="sxs-lookup"><span data-stu-id="39530-462">Relay</span></span>

* <span data-ttu-id="39530-463">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-463">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="39530-464">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-464">Sql</span></span>

* <span data-ttu-id="39530-465">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-465">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="39530-466">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-466">Storage</span></span>

* <span data-ttu-id="39530-467">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="39530-467">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="39530-468">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-468">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="39530-469">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="39530-469">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="39530-470">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-470">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="39530-471">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-471">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="39530-472">VM</span><span class="sxs-lookup"><span data-stu-id="39530-472">VM</span></span>

* <span data-ttu-id="39530-473">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-473">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="39530-474">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="39530-474">July 31, 2018</span></span>

<span data-ttu-id="39530-475">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="39530-475">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="39530-476">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-476">ACR</span></span>

* <span data-ttu-id="39530-477">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-477">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="39530-478">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-478">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="39530-479">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-479">ACS</span></span>

* <span data-ttu-id="39530-480">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-480">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="39530-481">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-481">Batch</span></span>

* <span data-ttu-id="39530-482">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-482">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="39530-483">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-483">Container</span></span>

* <span data-ttu-id="39530-484">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-484">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="39530-485">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-485">Network</span></span>

* <span data-ttu-id="39530-486">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-486">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="39530-487">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-487">Resource</span></span>

* <span data-ttu-id="39530-488">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-488">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="39530-489">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-489">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="39530-490">Role</span><span class="sxs-lookup"><span data-stu-id="39530-490">Role</span></span>

* <span data-ttu-id="39530-491">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-491">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="39530-492">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-492">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="39530-493">Search</span><span class="sxs-lookup"><span data-stu-id="39530-493">Search</span></span>

* <span data-ttu-id="39530-494">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-494">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="39530-495">Service Bus</span><span class="sxs-lookup"><span data-stu-id="39530-495">Service Bus</span></span>

* <span data-ttu-id="39530-496">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-496">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="39530-497">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-497">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="39530-498">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="39530-498">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="39530-499">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="39530-499">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-500">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-500">Storage</span></span>

* <span data-ttu-id="39530-501">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-501">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="39530-502">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="39530-502">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="39530-503">VM</span><span class="sxs-lookup"><span data-stu-id="39530-503">VM</span></span>

* <span data-ttu-id="39530-504">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-504">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="39530-505">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-505">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="39530-506">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-506">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="39530-507">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-507">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="39530-508">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="39530-508">July 18, 2018</span></span>

<span data-ttu-id="39530-509">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="39530-509">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="39530-510">コア</span><span class="sxs-lookup"><span data-stu-id="39530-510">Core</span></span>

* <span data-ttu-id="39530-511">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-511">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="39530-512">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-512">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="39530-513">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-513">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="39530-514">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-514">ACR</span></span>

* <span data-ttu-id="39530-515">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-515">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="39530-516">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-516">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="39530-517">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-517">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="39530-518">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-518">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="39530-519">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-519">ACS</span></span>

* <span data-ttu-id="39530-520">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-520">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-521">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-521">AppService</span></span>

* <span data-ttu-id="39530-522">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-522">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="39530-523">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-523">Batch</span></span>

* <span data-ttu-id="39530-524">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-524">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="39530-525">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-525">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="39530-526">Batch AI</span><span class="sxs-lookup"><span data-stu-id="39530-526">Batch AI</span></span>

* <span data-ttu-id="39530-527">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-527">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="39530-528">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-528">Container</span></span>

* <span data-ttu-id="39530-529">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-529">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="39530-530">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-530">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="39530-531">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-531">Network</span></span>

* <span data-ttu-id="39530-532">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-532">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="39530-533">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-533">Added `network nic wait`</span></span>
* <span data-ttu-id="39530-534">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-534">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="39530-535">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-535">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="39530-536">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-536">Resource</span></span>

* <span data-ttu-id="39530-537">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-537">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="39530-538">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-538">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="39530-539">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-539">Added `deployment wait` command</span></span>
* <span data-ttu-id="39530-540">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-540">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="39530-541">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-541">SQL</span></span>

* <span data-ttu-id="39530-542">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-542">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="39530-543">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-543">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="39530-544">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="39530-544">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="39530-545">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-545">Storage</span></span>

* <span data-ttu-id="39530-546">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-546">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="39530-547">VM</span><span class="sxs-lookup"><span data-stu-id="39530-547">VM</span></span>

* <span data-ttu-id="39530-548">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-548">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="39530-549">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-549">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="39530-550">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-550">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="39530-551">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="39530-551">July 3, 2018</span></span>

<span data-ttu-id="39530-552">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="39530-552">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="39530-553">AKS</span><span class="sxs-lookup"><span data-stu-id="39530-553">AKS</span></span>

* <span data-ttu-id="39530-554">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-554">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="39530-555">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="39530-555">July 3, 2018</span></span>

<span data-ttu-id="39530-556">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="39530-556">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="39530-557">コア</span><span class="sxs-lookup"><span data-stu-id="39530-557">Core</span></span>

* <span data-ttu-id="39530-558">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-558">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="39530-559">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-559">ACR</span></span>

* <span data-ttu-id="39530-560">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-560">Added polling build status</span></span>
* <span data-ttu-id="39530-561">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-561">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="39530-562">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-562">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="39530-563">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-563">ACS</span></span>

* <span data-ttu-id="39530-564">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-564">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="39530-565">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-565">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="39530-566">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="39530-566">Updated options for `aks browse` command.</span></span> <span data-ttu-id="39530-567">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-567">Added `--listen-port` support</span></span>
* <span data-ttu-id="39530-568">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="39530-568">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="39530-569">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="39530-569">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="39530-570">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-570">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-571">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-571">AppService</span></span>

* <span data-ttu-id="39530-572">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-572">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="39530-573">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-573">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="39530-574">バックアップ</span><span class="sxs-lookup"><span data-stu-id="39530-574">Backup</span></span>

* <span data-ttu-id="39530-575">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-575">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="39530-576">BatchAI</span><span class="sxs-lookup"><span data-stu-id="39530-576">BatchAI</span></span>

* <span data-ttu-id="39530-577">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-577">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="39530-578">クラウド</span><span class="sxs-lookup"><span data-stu-id="39530-578">Cloud</span></span>

* <span data-ttu-id="39530-579">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-579">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="39530-580">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-580">Container</span></span>

* <span data-ttu-id="39530-581">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-581">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="39530-582">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-582">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="39530-583">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-583">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="39530-584">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-584">Extension</span></span>

* <span data-ttu-id="39530-585">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-585">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="39530-586">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-586">Network</span></span>

* <span data-ttu-id="39530-587">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-587">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-588">Rdbms</span><span class="sxs-lookup"><span data-stu-id="39530-588">Rdbms</span></span>

* <span data-ttu-id="39530-589">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-589">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="39530-590">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-590">Resource</span></span>

* <span data-ttu-id="39530-591">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-591">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="39530-592">VM</span><span class="sxs-lookup"><span data-stu-id="39530-592">VM</span></span>

* <span data-ttu-id="39530-593">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-593">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="39530-594">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="39530-594">June 25, 2018</span></span>

<span data-ttu-id="39530-595">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="39530-595">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="39530-596">CLI</span><span class="sxs-lookup"><span data-stu-id="39530-596">CLI</span></span>

* <span data-ttu-id="39530-597">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-597">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="39530-598">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="39530-598">June 19, 2018</span></span>

<span data-ttu-id="39530-599">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="39530-599">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="39530-600">コア</span><span class="sxs-lookup"><span data-stu-id="39530-600">Core</span></span>

* <span data-ttu-id="39530-601">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-601">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="39530-602">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-602">ACR</span></span>

* <span data-ttu-id="39530-603">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-603">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="39530-604">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-604">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="39530-605">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-605">ACS</span></span>

* <span data-ttu-id="39530-606">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="39530-606">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="39530-607">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-607">Added `--update` support</span></span>
* <span data-ttu-id="39530-608">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-608">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="39530-609">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-609">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="39530-610">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-610">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="39530-611">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="39530-611">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="39530-612">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-612">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="39530-613">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-613">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-614">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-614">AppService</span></span>

* <span data-ttu-id="39530-615">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-615">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="39530-616">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-616">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="39530-617">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-617">Batch</span></span>

* <span data-ttu-id="39530-618">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-618">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="39530-619">Batch AI</span><span class="sxs-lookup"><span data-stu-id="39530-619">Batch AI</span></span>

* <span data-ttu-id="39530-620">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-620">Added support for workspaces.</span></span> <span data-ttu-id="39530-621">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="39530-621">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="39530-622">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-622">Added support for experiments.</span></span> <span data-ttu-id="39530-623">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="39530-623">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="39530-624">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-624">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="39530-625">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-625">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="39530-626">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="39530-626">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="39530-627">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-627">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="39530-628">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="39530-628">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="39530-629">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="39530-629">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="39530-630">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-630">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="39530-631">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="39530-631">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="39530-632">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-632">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="39530-633">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="39530-633">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="39530-634">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-634">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="39530-635">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="39530-635">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="39530-636">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-636">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="39530-637">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-637">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="39530-638">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-638">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="39530-639">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-639">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="39530-640">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-640">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="39530-641">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-641">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="39530-642">マップ</span><span class="sxs-lookup"><span data-stu-id="39530-642">Maps</span></span>

* <span data-ttu-id="39530-643">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-643">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="39530-644">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-644">Network</span></span>

* <span data-ttu-id="39530-645">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="39530-645">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="39530-646">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-646">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="39530-647">#6502</span><span class="sxs-lookup"><span data-stu-id="39530-647">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="39530-648">Reservations</span><span class="sxs-lookup"><span data-stu-id="39530-648">Reservations</span></span>

* <span data-ttu-id="39530-649">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-649">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="39530-650">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-650">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="39530-651">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-651">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="39530-652">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-652">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="39530-653">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-653">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="39530-654">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-654">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="39530-655">Role</span><span class="sxs-lookup"><span data-stu-id="39530-655">Role</span></span>

* <span data-ttu-id="39530-656">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-656">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="39530-657">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-657">SQL</span></span>

* <span data-ttu-id="39530-658">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-658">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="39530-659">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-659">Storage</span></span>

* <span data-ttu-id="39530-660">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="39530-660">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="39530-661">VM</span><span class="sxs-lookup"><span data-stu-id="39530-661">VM</span></span>

* <span data-ttu-id="39530-662">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-662">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="39530-663">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-663">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="39530-664">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-664">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="39530-665">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="39530-665">June 13, 2018</span></span>

<span data-ttu-id="39530-666">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="39530-666">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="39530-667">コア</span><span class="sxs-lookup"><span data-stu-id="39530-667">Core</span></span>

* <span data-ttu-id="39530-668">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-668">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="39530-669">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="39530-669">June 13, 2018</span></span>

<span data-ttu-id="39530-670">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="39530-670">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="39530-671">AKS</span><span class="sxs-lookup"><span data-stu-id="39530-671">AKS</span></span>

* <span data-ttu-id="39530-672">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-672">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="39530-673">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-673">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="39530-674">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-674">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="39530-675">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-675">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="39530-676">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-676">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-677">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-677">AppService</span></span>

* <span data-ttu-id="39530-678">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-678">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="39530-679">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="39530-679">June 5, 2018</span></span>

<span data-ttu-id="39530-680">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="39530-680">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-681">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-681">Interactive</span></span>

* <span data-ttu-id="39530-682">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-682">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="39530-683">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="39530-683">June 5, 2018</span></span>

<span data-ttu-id="39530-684">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="39530-684">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="39530-685">コア</span><span class="sxs-lookup"><span data-stu-id="39530-685">Core</span></span>

* <span data-ttu-id="39530-686">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-686">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="39530-687">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-687">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="39530-688">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-688">ACR</span></span>

* <span data-ttu-id="39530-689">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-689">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="39530-690">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-690">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="39530-691">AKS</span><span class="sxs-lookup"><span data-stu-id="39530-691">AKS</span></span>

* <span data-ttu-id="39530-692">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-692">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="39530-693">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-693">Batch</span></span>

* <span data-ttu-id="39530-694">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-694">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="39530-695">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-695">IOT</span></span>

* <span data-ttu-id="39530-696">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-696">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="39530-697">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-697">Network</span></span>

* <span data-ttu-id="39530-698">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-698">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="39530-699">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="39530-699">Policy Insights</span></span>

* <span data-ttu-id="39530-700">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-700">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="39530-701">ARM</span><span class="sxs-lookup"><span data-stu-id="39530-701">ARM</span></span>

* <span data-ttu-id="39530-702">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-702">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="39530-703">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-703">SQL</span></span>

* <span data-ttu-id="39530-704">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-704">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="39530-705">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-705">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="39530-706">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-706">Storage</span></span>

* <span data-ttu-id="39530-707">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-707">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="39530-708">VM</span><span class="sxs-lookup"><span data-stu-id="39530-708">VM</span></span>

* <span data-ttu-id="39530-709">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-709">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="39530-710">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-710">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="39530-711">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-711">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="39530-712">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="39530-712">May 22, 2018</span></span>

<span data-ttu-id="39530-713">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="39530-713">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="39530-714">コア</span><span class="sxs-lookup"><span data-stu-id="39530-714">Core</span></span>

* <span data-ttu-id="39530-715">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-715">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="39530-716">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-716">ACS</span></span>

* <span data-ttu-id="39530-717">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-717">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="39530-718">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-718">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-719">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-719">AppService</span></span>

* <span data-ttu-id="39530-720">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-720">Improved generic update commands</span></span>
* <span data-ttu-id="39530-721">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-721">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="39530-722">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-722">Container</span></span>

* <span data-ttu-id="39530-723">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-723">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="39530-724">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-724">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="39530-725">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-725">Extension</span></span>

* <span data-ttu-id="39530-726">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-726">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-727">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-727">Interactive</span></span>

* <span data-ttu-id="39530-728">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-728">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="39530-729">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-729">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-730">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-730">KeyVault</span></span>

* <span data-ttu-id="39530-731">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-731">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="39530-732">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-732">Network</span></span>

* <span data-ttu-id="39530-733">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-733">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="39530-734">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-734">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="39530-735">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-735">SQL</span></span>

* <span data-ttu-id="39530-736">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-736">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="39530-737">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-737">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="39530-738">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-738">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="39530-739">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-739">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="39530-740">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-740">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="39530-741">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="39530-741">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="39530-742">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="39530-742">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="39530-743">`edition`</span><span class="sxs-lookup"><span data-stu-id="39530-743">`edition`.</span></span> <span data-ttu-id="39530-744">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="39530-744">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="39530-745">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="39530-745">`elasticPoolName`.</span></span> <span data-ttu-id="39530-746">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="39530-746">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="39530-747">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-747">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="39530-748">`edition`</span><span class="sxs-lookup"><span data-stu-id="39530-748">`edition`.</span></span> <span data-ttu-id="39530-749">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="39530-749">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="39530-750">`dtu`</span><span class="sxs-lookup"><span data-stu-id="39530-750">`dtu`.</span></span> <span data-ttu-id="39530-751">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="39530-751">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="39530-752">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="39530-752">`databaseDtuMin`.</span></span> <span data-ttu-id="39530-753">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="39530-753">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="39530-754">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="39530-754">`databaseDtuMax`.</span></span> <span data-ttu-id="39530-755">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="39530-755">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="39530-756">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-756">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="39530-757">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-757">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="39530-758">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-758">Storage</span></span>

* <span data-ttu-id="39530-759">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-759">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="39530-760">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-760">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="39530-761">VM</span><span class="sxs-lookup"><span data-stu-id="39530-761">VM</span></span>

* <span data-ttu-id="39530-762">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-762">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="39530-763">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="39530-763">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="39530-764">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-764">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="39530-765">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-765">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="39530-766">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-766">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="39530-767">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="39530-767">May 7, 2018</span></span>

<span data-ttu-id="39530-768">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="39530-768">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="39530-769">コア</span><span class="sxs-lookup"><span data-stu-id="39530-769">Core</span></span>

* <span data-ttu-id="39530-770">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-770">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="39530-771">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-771">Added limited support for positional arguments</span></span>
* <span data-ttu-id="39530-772">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-772">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="39530-773">#5591</span><span class="sxs-lookup"><span data-stu-id="39530-773">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="39530-774">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="39530-774">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="39530-775">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="39530-775">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="39530-776">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-776">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="39530-777">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-777">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="39530-778">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-778">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="39530-779">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-779">ACR</span></span>

* <span data-ttu-id="39530-780">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-780">Added ACR Build commands</span></span>
* <span data-ttu-id="39530-781">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-781">Improved resource not found error messages</span></span>
* <span data-ttu-id="39530-782">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-782">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="39530-783">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-783">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="39530-784">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-784">Improved repository commands error messages</span></span>
* <span data-ttu-id="39530-785">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-785">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="39530-786">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-786">ACS</span></span>

* <span data-ttu-id="39530-787">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-787">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="39530-788">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-788">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="39530-789">AMS</span><span class="sxs-lookup"><span data-stu-id="39530-789">AMS</span></span>

* <span data-ttu-id="39530-790">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="39530-790">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-791">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-791">Appservice</span></span>

* <span data-ttu-id="39530-792">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-792">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="39530-793">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-793">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="39530-794">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-794">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="39530-795">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-795">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="39530-796">Batch AI</span><span class="sxs-lookup"><span data-stu-id="39530-796">Batch AI</span></span>

* <span data-ttu-id="39530-797">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-797">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="39530-798">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="39530-798">Cognitive Services</span></span>

* <span data-ttu-id="39530-799">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-799">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="39530-800">消費</span><span class="sxs-lookup"><span data-stu-id="39530-800">Consumption</span></span>

* <span data-ttu-id="39530-801">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-801">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="39530-802">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-802">Container</span></span>

* <span data-ttu-id="39530-803">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-803">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="39530-804">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-804">Cosmos DB</span></span>

* <span data-ttu-id="39530-805">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="39530-805">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="39530-806">DMS</span><span class="sxs-lookup"><span data-stu-id="39530-806">DMS</span></span>

* <span data-ttu-id="39530-807">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-807">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="39530-808">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-808">Extension</span></span>

* <span data-ttu-id="39530-809">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-809">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-810">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-810">Interactive</span></span>

* <span data-ttu-id="39530-811">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-811">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="39530-812">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="39530-812">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="39530-813">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-813">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="39530-814">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-814">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="39530-815">ラボ</span><span class="sxs-lookup"><span data-stu-id="39530-815">Lab</span></span>

* <span data-ttu-id="39530-816">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-816">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="39530-817">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-817">Network</span></span>

* <span data-ttu-id="39530-818">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-818">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="39530-819">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-819">Profile</span></span>

* <span data-ttu-id="39530-820">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-820">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="39530-821">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-821">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="39530-822">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-822">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="39530-823">Redis</span><span class="sxs-lookup"><span data-stu-id="39530-823">Redis</span></span>

* <span data-ttu-id="39530-824">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-824">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="39530-825">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="39530-825">Deprecated `redis list-all`.</span></span> <span data-ttu-id="39530-826">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="39530-826">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="39530-827">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-827">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="39530-828">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-828">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="39530-829">Role</span><span class="sxs-lookup"><span data-stu-id="39530-829">Role</span></span>

* <span data-ttu-id="39530-830">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-830">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-831">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-831">Storage</span></span>

* <span data-ttu-id="39530-832">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="39530-832">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="39530-833">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-833">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="39530-834">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="39530-834">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="39530-835">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="39530-835">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="39530-836">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-836">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="39530-837">VM</span><span class="sxs-lookup"><span data-stu-id="39530-837">VM</span></span>

* <span data-ttu-id="39530-838">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-838">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="39530-839">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-839">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="39530-840">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="39530-840">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="39530-841">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-841">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="39530-842">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-842">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="39530-843">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-843">Added write accelerator support</span></span>
* <span data-ttu-id="39530-844">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-844">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="39530-845">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-845">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="39530-846">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-846">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="39530-847">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="39530-847">April 10, 2018</span></span>

<span data-ttu-id="39530-848">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="39530-848">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="39530-849">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-849">ACR</span></span>

* <span data-ttu-id="39530-850">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-850">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="39530-851">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-851">ACS</span></span>

* <span data-ttu-id="39530-852">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-852">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-853">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-853">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="39530-855">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-855">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="39530-856">BatchAI</span><span class="sxs-lookup"><span data-stu-id="39530-856">BatchAI</span></span>

* <span data-ttu-id="39530-857">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-857">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="39530-858">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="39530-858">Job level mounting</span></span>
  - <span data-ttu-id="39530-859">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="39530-859">Environment variables with secret values</span></span>
  - <span data-ttu-id="39530-860">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="39530-860">Performance counters settings</span></span>
  - <span data-ttu-id="39530-861">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="39530-861">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="39530-862">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="39530-862">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="39530-863">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="39530-863">Usage and limits reporting</span></span>
  - <span data-ttu-id="39530-864">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="39530-864">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="39530-865">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="39530-865">Support for custom images</span></span>
  - <span data-ttu-id="39530-866">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-866">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="39530-867">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="39530-867">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="39530-868">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="39530-868">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="39530-869">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="39530-869">National clouds are supported</span></span>
* <span data-ttu-id="39530-870">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-870">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="39530-871">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-871">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="39530-872">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-872">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="39530-873">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="39530-873">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="39530-874">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="39530-874">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="39530-875">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="39530-875">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="39530-876">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-876">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="39530-877">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-877">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="39530-878">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="39530-878">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="39530-879">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-879">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="39530-880">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="39530-880">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="39530-881">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="39530-881">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="39530-882">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-882">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="39530-883">課金</span><span class="sxs-lookup"><span data-stu-id="39530-883">Billing</span></span>

* <span data-ttu-id="39530-884">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-884">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="39530-885">消費</span><span class="sxs-lookup"><span data-stu-id="39530-885">Consumption</span></span>

* <span data-ttu-id="39530-886">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-886">Added `marketplace` commands</span></span>
* <span data-ttu-id="39530-887">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-887">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="39530-888">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-888">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="39530-889">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-889">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="39530-890">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-890">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="39530-891">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-891">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="39530-892">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-892">Container</span></span>

* <span data-ttu-id="39530-893">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-893">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="39530-894">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-894">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="39530-895">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-895">Extension</span></span>

* <span data-ttu-id="39530-896">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-896">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-897">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-897">Interactive</span></span>

* <span data-ttu-id="39530-898">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-898">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="39530-899">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-899">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="39530-900">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-900">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="39530-901">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-901">Network</span></span>

* <span data-ttu-id="39530-902">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-902">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="39530-903">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-903">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="39530-904">#4910</span><span class="sxs-lookup"><span data-stu-id="39530-904">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="39530-905">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-905">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="39530-906">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="39530-906">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="39530-907">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-907">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="39530-908">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-908">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="39530-909">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-909">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="39530-910">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-910">Profile</span></span>

* <span data-ttu-id="39530-911">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-911">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="39530-912">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-912">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-913">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-913">RDBMS</span></span>

* <span data-ttu-id="39530-914">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-914">Added `georestore` command</span></span>
* <span data-ttu-id="39530-915">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-915">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="39530-916">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-916">Resource</span></span>

* <span data-ttu-id="39530-917">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-917">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="39530-918">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-918">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="39530-919">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-919">SQL</span></span>

* <span data-ttu-id="39530-920">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-920">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-921">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-921">Storage</span></span>

* <span data-ttu-id="39530-922">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-922">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="39530-923">VM</span><span class="sxs-lookup"><span data-stu-id="39530-923">VM</span></span>

* <span data-ttu-id="39530-924">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-924">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="39530-925">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-925">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="39530-927">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-927">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="39530-928">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-928">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="39530-929">#5718</span><span class="sxs-lookup"><span data-stu-id="39530-929">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="39530-930">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-930">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="39530-931">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="39530-931">March 27, 2018</span></span>

<span data-ttu-id="39530-932">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="39530-932">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="39530-933">コア</span><span class="sxs-lookup"><span data-stu-id="39530-933">Core</span></span>

* <span data-ttu-id="39530-934">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="39530-934">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="39530-935">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-935">ACS</span></span>

* <span data-ttu-id="39530-936">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-936">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-937">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-937">Appservice</span></span>

* <span data-ttu-id="39530-938">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-938">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="39530-939">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-939">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="39530-940">バックアップ</span><span class="sxs-lookup"><span data-stu-id="39530-940">Backup</span></span>

* <span data-ttu-id="39530-941">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-941">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="39530-942">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="39530-942">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="39530-943">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-943">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="39530-944">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-944">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="39530-945">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-945">Container</span></span>

* <span data-ttu-id="39530-946">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-946">Added `container exec` command.</span></span> <span data-ttu-id="39530-947">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="39530-947">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="39530-948">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="39530-948">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="39530-949">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-949">Extension</span></span>

* <span data-ttu-id="39530-950">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-950">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="39530-951">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-951">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="39530-952">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-952">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-953">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-953">Interactive</span></span>

* <span data-ttu-id="39530-954">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-954">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="39530-955">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-955">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="39530-956">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="39530-956">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="39530-957">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-957">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="39530-958">ラボ</span><span class="sxs-lookup"><span data-stu-id="39530-958">Lab</span></span>

* <span data-ttu-id="39530-959">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-959">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-960">監視</span><span class="sxs-lookup"><span data-stu-id="39530-960">Monitor</span></span>

* <span data-ttu-id="39530-961">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="39530-961">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="39530-962">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="39530-962">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="39530-963">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="39530-963">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="39530-964">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-964">Network</span></span>

* <span data-ttu-id="39530-965">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-965">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="39530-966">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-966">Profile</span></span>

* <span data-ttu-id="39530-967">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-967">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-968">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-968">RDBMS</span></span>

* <span data-ttu-id="39530-969">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-969">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="39530-970">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-970">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="39530-972">Role</span><span class="sxs-lookup"><span data-stu-id="39530-972">Role</span></span>

* <span data-ttu-id="39530-973">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-973">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="39530-974">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-974">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="39530-975">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-975">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="39530-976">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-976">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="39530-977">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-977">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-978">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-978">Storage</span></span>

* <span data-ttu-id="39530-979">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-979">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="39530-980">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-980">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="39530-981">VM</span><span class="sxs-lookup"><span data-stu-id="39530-981">VM</span></span>

* <span data-ttu-id="39530-982">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-982">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="39530-983">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-983">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="39530-984">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-984">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="39530-985">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-985">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="39530-986">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="39530-986">March 13, 2018</span></span>

<span data-ttu-id="39530-987">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="39530-987">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="39530-988">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-988">ACR</span></span>

* <span data-ttu-id="39530-989">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-989">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="39530-990">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-990">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="39530-991">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-991">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="39530-992">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-992">ACS</span></span>

* <span data-ttu-id="39530-993">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-993">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="39530-994">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-994">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="39530-995">Advisor</span><span class="sxs-lookup"><span data-stu-id="39530-995">Advisor</span></span>

* <span data-ttu-id="39530-996">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-996">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="39530-997">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-997">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="39530-998">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-998">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="39530-999">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-999">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="39530-1000">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1000">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1001">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1001">Appservice</span></span>

* <span data-ttu-id="39530-1002">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1002">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="39530-1003">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1003">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="39530-1004">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="39530-1004">Eventhubs</span></span>

* <span data-ttu-id="39530-1005">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1005">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="39530-1006">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-1006">Extension</span></span>

* <span data-ttu-id="39530-1007">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1007">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-1008">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-1008">Interactive</span></span>

* <span data-ttu-id="39530-1009">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="39530-1009">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="39530-1010">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="39530-1010">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="39530-1011">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="39530-1011">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="39530-1012">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1012">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1013">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1013">Monitor</span></span>

* <span data-ttu-id="39530-1014">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1014">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="39530-1015">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1015">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="39530-1016">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1016">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="39530-1017">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1017">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="39530-1018">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1018">Network</span></span>

* <span data-ttu-id="39530-1019">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1019">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="39530-1020">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1020">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="39530-1021">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1021">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="39530-1022">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1022">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1023">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1023">Profile</span></span>

* <span data-ttu-id="39530-1024">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1024">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="39530-1025">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1025">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-1026">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-1026">RDBMS</span></span>

* <span data-ttu-id="39530-1027">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1027">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="39530-1028">Service Bus</span><span class="sxs-lookup"><span data-stu-id="39530-1028">Service Bus</span></span>

* <span data-ttu-id="39530-1029">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1029">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1030">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1030">Storage</span></span>

* <span data-ttu-id="39530-1031">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1031">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="39530-1032">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1032">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1033">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1033">VM</span></span>

* <span data-ttu-id="39530-1034">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1034">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="39530-1035">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1035">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="39530-1036">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1036">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="39530-1037">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1037">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="39530-1038">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="39530-1038">February 27, 2018</span></span>

<span data-ttu-id="39530-1039">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="39530-1039">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="39530-1040">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1040">Core</span></span>

* <span data-ttu-id="39530-1041">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="39530-1041">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="39530-1042">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1042">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="39530-1043">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1043">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1044">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1044">ACS</span></span>

* <span data-ttu-id="39530-1045">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1045">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="39530-1046">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="39530-1046">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="39530-1047">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1047">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="39530-1048">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1048">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1049">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1049">Appservice</span></span>

* <span data-ttu-id="39530-1050">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="39530-1050">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="39530-1051">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="39530-1051">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="39530-1052">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="39530-1052">Cognitive Services</span></span>

* <span data-ttu-id="39530-1053">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1053">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="39530-1054">消費</span><span class="sxs-lookup"><span data-stu-id="39530-1054">Consumption</span></span>

* <span data-ttu-id="39530-1055">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1055">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="39530-1056">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1056">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="39530-1057">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1057">Container</span></span>

* <span data-ttu-id="39530-1058">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1058">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="39530-1059">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1059">Network</span></span>

* <span data-ttu-id="39530-1060">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="39530-1060">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1061">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1061">Resource</span></span>

* <span data-ttu-id="39530-1062">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1062">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="39530-1063">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1063">Role</span></span>

* <span data-ttu-id="39530-1064">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1064">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1065">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1065">SQL</span></span>

* <span data-ttu-id="39530-1066">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1066">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1067">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1067">Storage</span></span>

* <span data-ttu-id="39530-1068">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1068">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1069">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1069">VM</span></span>

* <span data-ttu-id="39530-1070">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1070">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="39530-1071">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="39530-1071">February 13, 2018</span></span>

<span data-ttu-id="39530-1072">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="39530-1072">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="39530-1073">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1073">Core</span></span>

* <span data-ttu-id="39530-1074">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1074">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1075">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1075">ACS</span></span>

* <span data-ttu-id="39530-1076">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1076">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="39530-1077">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1077">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="39530-1078">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1078">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="39530-1079">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1079">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="39530-1080">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1080">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="39530-1081">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="39530-1081">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="39530-1082">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1082">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="39530-1083">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="39530-1083">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1084">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1084">Appservice</span></span>

* <span data-ttu-id="39530-1085">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1085">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="39530-1086">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1086">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="39530-1087">CDN</span><span class="sxs-lookup"><span data-stu-id="39530-1087">CDN</span></span>

* <span data-ttu-id="39530-1088">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1088">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="39530-1089">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1089">Container</span></span>

* <span data-ttu-id="39530-1090">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1090">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="39530-1091">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1091">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39530-1092">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-1092">CosmosDB</span></span>

* <span data-ttu-id="39530-1093">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1093">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="39530-1094">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-1094">Extension</span></span>

* <span data-ttu-id="39530-1095">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1095">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="39530-1096">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1096">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="39530-1097">フィードバック</span><span class="sxs-lookup"><span data-stu-id="39530-1097">Feedback</span></span>

* <span data-ttu-id="39530-1098">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1098">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-1099">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-1099">Interactive</span></span>

* <span data-ttu-id="39530-1100">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1100">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="39530-1101">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1101">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="39530-1102">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-1102">IoT</span></span>

* <span data-ttu-id="39530-1103">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1103">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="39530-1104">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1104">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="39530-1105">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1105">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="39530-1106">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1106">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1107">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1107">Monitor</span></span>

* <span data-ttu-id="39530-1108">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1108">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="39530-1109">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1109">Network</span></span>

* <span data-ttu-id="39530-1110">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1110">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="39530-1111">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1111">Profile</span></span>

* <span data-ttu-id="39530-1112">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1112">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1113">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1113">Resource</span></span>

* <span data-ttu-id="39530-1114">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1114">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="39530-1115">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1115">Role</span></span>

* <span data-ttu-id="39530-1116">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1116">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1117">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1117">SQL</span></span>

* <span data-ttu-id="39530-1118">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1118">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="39530-1119">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1119">Added `sql db rename`</span></span>
* <span data-ttu-id="39530-1120">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1120">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1121">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1121">Storage</span></span>

* <span data-ttu-id="39530-1122">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1122">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1123">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1123">VM</span></span>

* <span data-ttu-id="39530-1124">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1124">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="39530-1125">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1125">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="39530-1126">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="39530-1126">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="39530-1127">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="39530-1127">January 31, 2018</span></span>

<span data-ttu-id="39530-1128">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="39530-1128">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="39530-1129">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1129">Core</span></span>

* <span data-ttu-id="39530-1130">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1130">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="39530-1131">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1131">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="39530-1132">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1132">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="39530-1133">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="39530-1133">Use `--verbose` to see</span></span>
* <span data-ttu-id="39530-1134">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="39530-1134">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1135">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1135">ACS</span></span>

* <span data-ttu-id="39530-1136">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="39530-1136">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="39530-1137">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-1137">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1138">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1138">Appservice</span></span>

* <span data-ttu-id="39530-1139">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="39530-1139">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="39530-1140">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1140">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="39530-1141">CDN</span><span class="sxs-lookup"><span data-stu-id="39530-1141">CDN</span></span>

* <span data-ttu-id="39530-1142">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1142">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39530-1143">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-1143">CosmosDB</span></span>

* <span data-ttu-id="39530-1144">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1144">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-1145">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-1145">Interactive</span></span>

* <span data-ttu-id="39530-1146">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1146">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="39530-1147">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1147">Network</span></span>

* <span data-ttu-id="39530-1148">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1148">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="39530-1149">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1149">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="39530-1150">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1150">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="39530-1151">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1151">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="39530-1152">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1152">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="39530-1153">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1153">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="39530-1154">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1154">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="39530-1155">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1155">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="39530-1156">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1156">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="39530-1157">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="39530-1157">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1158">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1158">Profile</span></span>

* <span data-ttu-id="39530-1159">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1159">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1160">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1160">Resource</span></span>

* <span data-ttu-id="39530-1161">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1161">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1162">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1162">Storage</span></span>

* <span data-ttu-id="39530-1163">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1163">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="39530-1164">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1164">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="39530-1165">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1165">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="39530-1166">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1166">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="39530-1167">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1167">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1168">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1168">VM</span></span>

* <span data-ttu-id="39530-1169">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1169">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="39530-1170">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1170">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="39530-1171">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1171">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="39530-1172">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1172">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="39530-1173">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="39530-1173">January 17, 2018</span></span>

<span data-ttu-id="39530-1174">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="39530-1174">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="39530-1175">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-1175">ACR</span></span>

* <span data-ttu-id="39530-1176">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1176">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="39530-1177">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1177">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1178">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1178">ACS</span></span>

* <span data-ttu-id="39530-1179">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1179">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="39530-1180">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1180">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1181">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1181">Appservice</span></span>

* <span data-ttu-id="39530-1182">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1182">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="39530-1183">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1183">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="39530-1184">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1184">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="39530-1185">バックアップ</span><span class="sxs-lookup"><span data-stu-id="39530-1185">Backup</span></span>

* <span data-ttu-id="39530-1186">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1186">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="39530-1187">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1187">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="39530-1188">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1188">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="39530-1189">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1189">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="39530-1190">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1190">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="39530-1191">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-1191">Batch</span></span>

* <span data-ttu-id="39530-1192">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1192">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="39530-1193">クラウド</span><span class="sxs-lookup"><span data-stu-id="39530-1193">Cloud</span></span>

* <span data-ttu-id="39530-1194">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1194">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="39530-1195">消費</span><span class="sxs-lookup"><span data-stu-id="39530-1195">Consumption</span></span>

* <span data-ttu-id="39530-1196">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1196">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="39530-1197">Event Grid</span><span class="sxs-lookup"><span data-stu-id="39530-1197">Event Grid</span></span>

* <span data-ttu-id="39530-1198">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="39530-1198">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="39530-1199">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="39530-1199">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="39530-1200">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1200">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="39530-1201">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="39530-1201">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="39530-1202">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1202">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="39530-1203">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1203">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="39530-1204">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1204">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="39530-1205">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1205">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-1206">Interactive</span><span class="sxs-lookup"><span data-stu-id="39530-1206">Interactive</span></span>

* <span data-ttu-id="39530-1207">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="39530-1207">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="39530-1208">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1208">Fixed errors on startup</span></span>
* <span data-ttu-id="39530-1209">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1209">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="39530-1210">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-1210">IoT</span></span>

* <span data-ttu-id="39530-1211">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1211">Added support for device provisioning service</span></span>
* <span data-ttu-id="39530-1212">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1212">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="39530-1213">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1213">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1214">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1214">Monitor</span></span>

* <span data-ttu-id="39530-1215">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1215">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="39530-1216">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="39530-1216">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="39530-1217">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1217">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="39530-1218">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1218">Network</span></span>

* <span data-ttu-id="39530-1219">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1219">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="39530-1220">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1220">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1221">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1221">Profile</span></span>

* <span data-ttu-id="39530-1222">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1222">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="39530-1223">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1223">Role</span></span>

* <span data-ttu-id="39530-1224">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1224">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="39530-1225">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39530-1225">Service Fabric</span></span>

* <span data-ttu-id="39530-1226">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1226">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="39530-1227">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1227">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1228">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1228">VM</span></span>

* <span data-ttu-id="39530-1229">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="39530-1229">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="39530-1230">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1230">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="39530-1231">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1231">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="39530-1232">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1232">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="39530-1233">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1233">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="39530-1234">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1234">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="39530-1235">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1235">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="39530-1236">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1236">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="39530-1237">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="39530-1237">December 19, 2017</span></span>

<span data-ttu-id="39530-1238">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="39530-1238">Version 2.0.23</span></span>

* <span data-ttu-id="39530-1239">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1239">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="39530-1240">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1240">Container</span></span>

* <span data-ttu-id="39530-1241">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1241">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="39530-1242">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1242">Network</span></span>

* <span data-ttu-id="39530-1243">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1243">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="39530-1244">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1244">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1245">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1245">Storage</span></span>

* <span data-ttu-id="39530-1246">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1246">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1247">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1247">VM</span></span>

* <span data-ttu-id="39530-1248">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1248">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="39530-1249">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="39530-1249">December 5, 2017</span></span>

<span data-ttu-id="39530-1250">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="39530-1250">Version 2.0.22</span></span>

* <span data-ttu-id="39530-1251">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1251">Removed `az component` commands.</span></span> <span data-ttu-id="39530-1252">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="39530-1252">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="39530-1253">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1253">Core</span></span>
* <span data-ttu-id="39530-1254">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1254">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="39530-1255">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1255">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1256">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1256">ACS</span></span>

* <span data-ttu-id="39530-1257">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1257">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="39530-1258">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1258">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="39530-1259">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1259">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="39530-1260">Advisor</span><span class="sxs-lookup"><span data-stu-id="39530-1260">Advisor</span></span>

* <span data-ttu-id="39530-1261">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1261">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1262">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1262">Appservice</span></span>

* <span data-ttu-id="39530-1263">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1263">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="39530-1264">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1264">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="39530-1265">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1265">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="39530-1266">消費</span><span class="sxs-lookup"><span data-stu-id="39530-1266">Consumption</span></span>

* <span data-ttu-id="39530-1267">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1267">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="39530-1268">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1268">Container</span></span>

* <span data-ttu-id="39530-1269">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1269">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1270">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1270">Monitor</span></span>

* <span data-ttu-id="39530-1271">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1271">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1272">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1272">Resource</span></span>

* <span data-ttu-id="39530-1273">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1273">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="39530-1274">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1274">Role</span></span>

* <span data-ttu-id="39530-1275">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1275">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="39530-1276">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="39530-1276">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="39530-1277">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1277">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1278">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1278">SQL</span></span>

* <span data-ttu-id="39530-1279">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1279">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="39530-1280">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1280">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1281">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1281">VM</span></span>

* <span data-ttu-id="39530-1282">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1282">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="39530-1283">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="39530-1283">November 14, 2017</span></span>

<span data-ttu-id="39530-1284">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="39530-1284">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="39530-1285">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-1285">ACR</span></span>

* <span data-ttu-id="39530-1286">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1286">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="39530-1287">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1287">ACS</span></span>

* <span data-ttu-id="39530-1288">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1288">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="39530-1289">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1289">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="39530-1290">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1290">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="39530-1291">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1291">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="39530-1292">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1292">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1293">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1293">Appservice</span></span>

* <span data-ttu-id="39530-1294">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1294">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="39530-1295">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1295">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="39530-1296">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1296">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="39530-1297">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1297">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="39530-1298">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1298">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="39530-1299">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="39530-1299">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="39530-1300">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-1300">Batch</span></span>

* <span data-ttu-id="39530-1301">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1301">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="39530-1302">Batchai</span><span class="sxs-lookup"><span data-stu-id="39530-1302">Batchai</span></span>

* <span data-ttu-id="39530-1303">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1303">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="39530-1304">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1304">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="39530-1305">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1305">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="39530-1306">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1306">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="39530-1307">クラウド</span><span class="sxs-lookup"><span data-stu-id="39530-1307">Cloud</span></span>

* <span data-ttu-id="39530-1308">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1308">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="39530-1309">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1309">Container</span></span>

* <span data-ttu-id="39530-1310">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1310">Added support to open multiple ports</span></span>
* <span data-ttu-id="39530-1311">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1311">Added container group restart policy</span></span>
* <span data-ttu-id="39530-1312">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1312">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="39530-1313">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1313">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39530-1314">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39530-1314">Data Lake Analytics</span></span>

* <span data-ttu-id="39530-1315">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1315">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39530-1316">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39530-1316">Data Lake Store</span></span>

* <span data-ttu-id="39530-1317">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1317">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="39530-1318">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-1318">Extension</span></span>

* <span data-ttu-id="39530-1319">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1319">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="39530-1320">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1320">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="39530-1321">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-1321">IoT</span></span>

* <span data-ttu-id="39530-1322">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1322">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1323">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1323">Monitor</span></span>

* <span data-ttu-id="39530-1324">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1324">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="39530-1325">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1325">Network</span></span>

* <span data-ttu-id="39530-1326">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1326">Added support for CAA DNS records</span></span>
* <span data-ttu-id="39530-1327">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1327">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="39530-1328">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1328">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="39530-1329">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1329">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="39530-1330">Reservations</span><span class="sxs-lookup"><span data-stu-id="39530-1330">Reservations</span></span>

* <span data-ttu-id="39530-1331">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39530-1331">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1332">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1332">Resource</span></span>

* <span data-ttu-id="39530-1333">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1333">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1334">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1334">SQL</span></span>

* <span data-ttu-id="39530-1335">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1335">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1336">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1336">Storage</span></span>

* <span data-ttu-id="39530-1337">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1337">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="39530-1338">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1338">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="39530-1339">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1339">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="39530-1340">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1340">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="39530-1341">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1341">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="39530-1342">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1342">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="39530-1343">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1343">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1344">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1344">VM</span></span>

* <span data-ttu-id="39530-1345">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1345">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="39530-1346">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1346">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="39530-1347">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1347">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="39530-1348">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1348">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="39530-1349">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1349">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="39530-1350">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="39530-1350">October 24, 2017</span></span>

<span data-ttu-id="39530-1351">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="39530-1351">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="39530-1352">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1352">Core</span></span>

* <span data-ttu-id="39530-1353">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1353">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="39530-1354">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-1354">ACR</span></span>

* <span data-ttu-id="39530-1355">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1355">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="39530-1356">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1356">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="39530-1357">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1357">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1358">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1358">ACS</span></span>

* <span data-ttu-id="39530-1359">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1359">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="39530-1360">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1360">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1361">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1361">Appservice</span></span>

* <span data-ttu-id="39530-1362">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1362">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="39530-1363">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="39530-1363">Component</span></span>

* <span data-ttu-id="39530-1364">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1364">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1365">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1365">Monitor</span></span>

* <span data-ttu-id="39530-1366">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1366">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1367">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1367">Resource</span></span>

* <span data-ttu-id="39530-1368">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1368">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="39530-1369">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1369">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1370">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1370">VM</span></span>

* <span data-ttu-id="39530-1371">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1371">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="39530-1372">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="39530-1372">October 9, 2017</span></span>

<span data-ttu-id="39530-1373">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="39530-1373">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="39530-1374">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1374">Core</span></span>

* <span data-ttu-id="39530-1375">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1375">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1376">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1376">Appservice</span></span>

* <span data-ttu-id="39530-1377">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1377">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="39530-1378">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-1378">Batch</span></span>

* <span data-ttu-id="39530-1379">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1379">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="39530-1380">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1380">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="39530-1381">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1381">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="39530-1382">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1382">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="39530-1383">Batchai</span><span class="sxs-lookup"><span data-stu-id="39530-1383">Batchai</span></span>

* <span data-ttu-id="39530-1384">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1384">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-1385">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-1385">Keyvault</span></span>

* <span data-ttu-id="39530-1386">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1386">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="39530-1387">(#4448)</span><span class="sxs-lookup"><span data-stu-id="39530-1387">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="39530-1388">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1388">Network</span></span>

* <span data-ttu-id="39530-1389">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1389">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="39530-1390">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1390">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1391">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1391">Resource</span></span>

* <span data-ttu-id="39530-1392">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1392">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="39530-1393">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1393">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="39530-1394">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1394">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="39530-1395">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1395">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1396">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1396">Sql</span></span>

* <span data-ttu-id="39530-1397">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1397">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="39530-1398">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="39530-1398">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="39530-1399">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="39530-1399">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1400">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1400">Storage</span></span>

* <span data-ttu-id="39530-1401">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1401">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1402">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1402">Vm</span></span>

* <span data-ttu-id="39530-1403">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1403">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="39530-1404">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1404">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="39530-1405">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1405">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="39530-1406">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1406">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="39530-1407">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1407">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="39530-1408">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="39530-1408">September 22, 2017</span></span>

<span data-ttu-id="39530-1409">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="39530-1409">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1410">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1410">Resource</span></span>

* <span data-ttu-id="39530-1411">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1411">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="39530-1412">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1412">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="39530-1413">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1413">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="39530-1414">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1414">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="39530-1415">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1415">Network</span></span>

* <span data-ttu-id="39530-1416">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1416">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="39530-1417">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1417">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="39530-1418">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1418">Added `asg` application security group commands</span></span>
* <span data-ttu-id="39530-1419">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1419">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="39530-1420">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1420">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="39530-1421">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1421">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="39530-1422">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1422">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1423">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1423">Storage</span></span>

* <span data-ttu-id="39530-1424">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1424">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="39530-1425">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="39530-1425">Eventgrid</span></span>

* <span data-ttu-id="39530-1426">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1426">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1427">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1427">SQL</span></span>

* <span data-ttu-id="39530-1428">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1428">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="39530-1429">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="39530-1429">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="39530-1430">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1430">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-1431">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-1431">Keyvault</span></span>

* <span data-ttu-id="39530-1432">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1432">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1433">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1433">VM</span></span>

* <span data-ttu-id="39530-1434">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1434">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="39530-1435">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1435">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="39530-1436">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1436">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="39530-1437">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1437">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="39530-1438">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1438">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="39530-1439">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1439">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1440">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1440">ACS</span></span>

* <span data-ttu-id="39530-1441">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1441">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1442">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1442">Appservice</span></span>

* <span data-ttu-id="39530-1443">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1443">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="39530-1444">バックアップ</span><span class="sxs-lookup"><span data-stu-id="39530-1444">Backup</span></span>

* <span data-ttu-id="39530-1445">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39530-1445">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="39530-1446">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="39530-1446">September 11, 2017</span></span>

<span data-ttu-id="39530-1447">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="39530-1447">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="39530-1448">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1448">Core</span></span>

* <span data-ttu-id="39530-1449">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1449">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="39530-1450">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1450">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1451">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1451">Acs</span></span>

* <span data-ttu-id="39530-1452">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1452">Added `acs list-locations` command</span></span>
* <span data-ttu-id="39530-1453">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="39530-1453">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1454">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1454">Appservice</span></span>

* <span data-ttu-id="39530-1455">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1455">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="39530-1456">CDN</span><span class="sxs-lookup"><span data-stu-id="39530-1456">CDN</span></span>

* <span data-ttu-id="39530-1457">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1457">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="39530-1458">内線番号</span><span class="sxs-lookup"><span data-stu-id="39530-1458">Extension</span></span>

* <span data-ttu-id="39530-1459">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1459">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-1460">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-1460">Keyvault</span></span>

* <span data-ttu-id="39530-1461">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1461">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="39530-1462">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1462">Network</span></span>

* <span data-ttu-id="39530-1463">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1463">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="39530-1464">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1464">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="39530-1465">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1465">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="39530-1466">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1466">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="39530-1467">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1467">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1468">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1468">Resource</span></span>

* <span data-ttu-id="39530-1469">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39530-1469">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="39530-1470">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39530-1470">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="39530-1471">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="39530-1471">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="39530-1472">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="39530-1472">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1473">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1473">SQL</span></span>

* <span data-ttu-id="39530-1474">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1474">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1475">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1475">VM</span></span>

* <span data-ttu-id="39530-1476">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="39530-1476">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="39530-1477">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="39530-1477">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="39530-1478">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1478">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="39530-1479">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="39530-1479">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="39530-1480">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="39530-1480">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="39530-1481">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="39530-1481">August 31, 2017</span></span>

<span data-ttu-id="39530-1482">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="39530-1482">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-1483">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-1483">Keyvault</span></span>

* <span data-ttu-id="39530-1484">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1484">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="39530-1485">SF</span><span class="sxs-lookup"><span data-stu-id="39530-1485">Sf</span></span>

* <span data-ttu-id="39530-1486">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="39530-1486">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1487">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1487">Storage</span></span>

* <span data-ttu-id="39530-1488">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1488">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="39530-1489">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="39530-1489">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="39530-1490">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="39530-1490">August 28, 2017</span></span>

<span data-ttu-id="39530-1491">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="39530-1491">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="39530-1492">CLI</span><span class="sxs-lookup"><span data-stu-id="39530-1492">CLI</span></span>

* <span data-ttu-id="39530-1493">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1493">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1494">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1494">ACS</span></span>

* <span data-ttu-id="39530-1495">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1495">Corrected preview regions</span></span>
* <span data-ttu-id="39530-1496">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1496">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="39530-1497">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="39530-1497">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1498">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1498">Appservice</span></span>

* <span data-ttu-id="39530-1499">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1499">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="39530-1500">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1500">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="39530-1501">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1501">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="39530-1502">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1502">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="39530-1503">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="39530-1503">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="39530-1504">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-1504">IoT</span></span>

* <span data-ttu-id="39530-1505">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1505">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="39530-1506">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1506">Network</span></span>

* <span data-ttu-id="39530-1507">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1507">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="39530-1508">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1508">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="39530-1509">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1509">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="39530-1510">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1510">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="39530-1511">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1511">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1512">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1512">Profile</span></span>

* <span data-ttu-id="39530-1513">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1513">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="39530-1514">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39530-1514">Service Fabric</span></span>

* <span data-ttu-id="39530-1515">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="39530-1515">Preview release</span></span>
* <span data-ttu-id="39530-1516">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="39530-1516">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="39530-1517">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1517">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="39530-1518">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1518">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1519">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1519">Storage</span></span>

* <span data-ttu-id="39530-1520">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1520">Enabled setting blob tier</span></span>
* <span data-ttu-id="39530-1521">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1521">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="39530-1522">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1522">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="39530-1523">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1523">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="39530-1524">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1524">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="39530-1525">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="39530-1525">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1526">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1526">VM</span></span>

* <span data-ttu-id="39530-1527">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1527">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="39530-1528">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1528">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="39530-1529">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1529">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="39530-1530">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1530">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="39530-1531">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1531">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="39530-1532">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1532">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="39530-1533">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="39530-1533">August 15, 2017</span></span>

<span data-ttu-id="39530-1534">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="39530-1534">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1535">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1535">ACS</span></span>

* <span data-ttu-id="39530-1536">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1536">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1537">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1537">Appservice</span></span>

* <span data-ttu-id="39530-1538">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1538">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="39530-1539">Event Grid</span><span class="sxs-lookup"><span data-stu-id="39530-1539">Event Grid</span></span>

* <span data-ttu-id="39530-1540">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1540">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="39530-1541">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="39530-1541">August 11, 2017</span></span>

<span data-ttu-id="39530-1542">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="39530-1542">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1543">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1543">ACS</span></span>

* <span data-ttu-id="39530-1544">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1544">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="39530-1545">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-1545">Batch</span></span>

* <span data-ttu-id="39530-1546">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="39530-1546">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="39530-1547">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1547">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="39530-1548">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1548">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="39530-1549">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1549">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="39530-1550">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1550">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="39530-1551">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1551">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="39530-1552">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="39530-1552">Component</span></span>

* <span data-ttu-id="39530-1553">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1553">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="39530-1554">コンテナー</span><span class="sxs-lookup"><span data-stu-id="39530-1554">Container</span></span>

* <span data-ttu-id="39530-1555">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1555">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="39530-1556">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39530-1556">Data Lake Store</span></span>

* <span data-ttu-id="39530-1557">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1557">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="39530-1558">Event Grid</span><span class="sxs-lookup"><span data-stu-id="39530-1558">Event Grid</span></span>

* <span data-ttu-id="39530-1559">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1559">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="39530-1560">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1560">Network</span></span>

* <span data-ttu-id="39530-1561">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1561">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="39530-1562">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1562">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="39530-1563">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1563">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="39530-1564">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1564">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1565">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1565">Profile</span></span>

* <span data-ttu-id="39530-1566">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1566">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1567">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1567">Storage</span></span>

* <span data-ttu-id="39530-1568">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="39530-1568">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1569">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1569">VM</span></span>

* <span data-ttu-id="39530-1570">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1570">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="39530-1571">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1571">Exposed `list-skus` command</span></span>
* <span data-ttu-id="39530-1572">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1572">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="39530-1573">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="39530-1573">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="39530-1574">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1574">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="39530-1575">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="39530-1575">July 28, 2017</span></span>

<span data-ttu-id="39530-1576">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="39530-1576">Version 2.0.12</span></span>

* <span data-ttu-id="39530-1577">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1577">Added container commands</span></span>
* <span data-ttu-id="39530-1578">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1578">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="39530-1579">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1579">Core</span></span>

* <span data-ttu-id="39530-1580">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="39530-1580">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="39530-1581">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1581">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="39530-1582">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="39530-1582">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="39530-1583">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="39530-1583">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="39530-1584">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="39530-1584">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="39530-1585">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="39530-1585">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="39530-1586">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="39530-1586">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="39530-1587">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="39530-1587">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="39530-1588">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="39530-1588">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="39530-1589">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="39530-1589">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="39530-1590">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="39530-1590">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="39530-1591">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="39530-1591">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="39530-1592">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1592">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="39530-1593">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1593">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="39530-1594">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1594">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="39530-1595">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="39530-1595">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="39530-1596">ACR</span><span class="sxs-lookup"><span data-stu-id="39530-1596">ACR</span></span>

* <span data-ttu-id="39530-1597">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1597">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="39530-1598">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1598">Support SKU update for managed registries</span></span>
* <span data-ttu-id="39530-1599">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1599">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="39530-1600">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1600">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="39530-1601">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1601">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="39530-1602">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1602">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1603">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1603">ACS</span></span>

* <span data-ttu-id="39530-1604">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1604">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1605">Appservice</span><span class="sxs-lookup"><span data-stu-id="39530-1605">Appservice</span></span>

* <span data-ttu-id="39530-1606">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1606">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="39530-1607">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1607">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="39530-1608">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="39530-1608">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="39530-1609">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="39530-1609">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="39530-1610">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="39530-1610">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="39530-1611">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="39530-1611">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="39530-1612">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="39530-1612">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="39530-1613">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="39530-1613">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="39530-1614">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1614">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="39530-1615">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="39530-1615">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="39530-1616">Batch</span><span class="sxs-lookup"><span data-stu-id="39530-1616">Batch</span></span>

* <span data-ttu-id="39530-1617">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="39530-1617">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="39530-1618">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1618">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="39530-1619">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1619">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="39530-1620">CDN</span><span class="sxs-lookup"><span data-stu-id="39530-1620">CDN</span></span>

* <span data-ttu-id="39530-1621">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1621">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="39530-1622">クラウド</span><span class="sxs-lookup"><span data-stu-id="39530-1622">Cloud</span></span>

* <span data-ttu-id="39530-1623">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1623">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="39530-1624">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="39530-1624">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="39530-1625">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1625">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="39530-1626">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="39530-1626">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="39530-1627">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="39530-1627">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39530-1628">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-1628">CosmosDB</span></span>

* <span data-ttu-id="39530-1629">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1629">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="39530-1630">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1630">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39530-1631">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39530-1631">Data Lake Analytics</span></span>

* <span data-ttu-id="39530-1632">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1632">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="39530-1633">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1633">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="39530-1634">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1634">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39530-1635">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39530-1635">Data Lake Store</span></span>

* <span data-ttu-id="39530-1636">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1636">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="39530-1637">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="39530-1637">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="39530-1638">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1638">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="39530-1639">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="39530-1639">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="39530-1640">対話</span><span class="sxs-lookup"><span data-stu-id="39530-1640">Interactive</span></span>

* <span data-ttu-id="39530-1641">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="39530-1641">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="39530-1642">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="39530-1642">Increased test coverage</span></span>
* <span data-ttu-id="39530-1643">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="39530-1643">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="39530-1644">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="39530-1644">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="39530-1645">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="39530-1645">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="39530-1646">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="39530-1646">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="39530-1647">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="39530-1647">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="39530-1648">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1648">Added `--progress` flag</span></span>
* <span data-ttu-id="39530-1649">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1649">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="39530-1650">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="39530-1650">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="39530-1651">IoT</span><span class="sxs-lookup"><span data-stu-id="39530-1651">IoT</span></span>

* <span data-ttu-id="39530-1652">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1652">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="39530-1653">(#3934)</span><span class="sxs-lookup"><span data-stu-id="39530-1653">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="39530-1654">Key Vault</span><span class="sxs-lookup"><span data-stu-id="39530-1654">Key vault</span></span>

* <span data-ttu-id="39530-1655">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1655">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="39530-1656">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39530-1656">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="39530-1657">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39530-1657">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="39530-1658">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39530-1658">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="39530-1659">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="39530-1659">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="39530-1660">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="39530-1660">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="39530-1661">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1661">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="39530-1662">(#3307)</span><span class="sxs-lookup"><span data-stu-id="39530-1662">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="39530-1663">ラボ</span><span class="sxs-lookup"><span data-stu-id="39530-1663">Lab</span></span>

* <span data-ttu-id="39530-1664">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1664">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="39530-1665">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1665">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1666">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1666">Monitor</span></span>

* <span data-ttu-id="39530-1667">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="39530-1667">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="39530-1668">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1668">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="39530-1669">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1669">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="39530-1670">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1670">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="39530-1671">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="39530-1671">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="39530-1672">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="39530-1672">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="39530-1673">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1673">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="39530-1674">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="39530-1674">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="39530-1675">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="39530-1675">`location` no longer required</span></span>
  * <span data-ttu-id="39530-1676">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="39530-1676">Add name and ID support for target</span></span>
  * <span data-ttu-id="39530-1677">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="39530-1677">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="39530-1678">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1678">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="39530-1679">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1679">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="39530-1680">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="39530-1680">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="39530-1681">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1681">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="39530-1682">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1682">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="39530-1683">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1683">Network</span></span>

* <span data-ttu-id="39530-1684">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1684">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="39530-1685">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1685">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="39530-1686">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1686">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="39530-1687">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1687">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="39530-1688">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1688">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="39530-1689">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1689">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="39530-1690">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1690">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="39530-1691">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1691">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="39530-1692">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1692">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="39530-1693">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1693">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="39530-1694">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1694">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="39530-1695">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1695">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="39530-1696">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1696">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="39530-1697">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1697">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="39530-1698">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1698">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="39530-1699">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1699">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="39530-1700">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1700">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="39530-1701">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1701">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="39530-1702">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1702">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="39530-1703">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1703">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="39530-1704">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1704">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="39530-1705">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1705">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="39530-1706">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1706">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="39530-1707">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39530-1707">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="39530-1708">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39530-1708">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="39530-1709">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39530-1709">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="39530-1710">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="39530-1710">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1711">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1711">Profile</span></span>

* <span data-ttu-id="39530-1712">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1712">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="39530-1713">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1713">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="39530-1714">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="39530-1714">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="39530-1715">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1715">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="39530-1716">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1716">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="39530-1717">RDBMS</span><span class="sxs-lookup"><span data-stu-id="39530-1717">RDBMS</span></span>

* <span data-ttu-id="39530-1718">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="39530-1718">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="39530-1719">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="39530-1719">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="39530-1720">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="39530-1720">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="39530-1721">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="39530-1721">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1722">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1722">Resource</span></span>

* <span data-ttu-id="39530-1723">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1723">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="39530-1724">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="39530-1724">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="39530-1725">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1725">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="39530-1726">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1726">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="39530-1727">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="39530-1727">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="39530-1728">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1728">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="39530-1729">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="39530-1729">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="39530-1730">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1730">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="39530-1731">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1731">Role</span></span>

* <span data-ttu-id="39530-1732">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1732">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="39530-1733">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="39530-1733">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="39530-1734">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="39530-1734">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="39530-1735">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="39530-1735">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="39530-1736">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1736">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="39530-1737">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39530-1737">Service Fabric</span></span>
* <span data-ttu-id="39530-1738">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="39530-1738">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="39530-1739">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="39530-1739">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="39530-1740">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="39530-1740">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1741">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1741">SQL</span></span>

* <span data-ttu-id="39530-1742">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1742">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="39530-1743">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="39530-1743">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="39530-1744">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="39530-1744">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1745">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1745">Storage</span></span>

* <span data-ttu-id="39530-1746">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="39530-1746">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="39530-1747">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1747">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="39530-1748">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="39530-1748">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="39530-1749">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="39530-1749">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="39530-1750">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="39530-1750">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="39530-1751">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="39530-1751">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1752">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1752">VM</span></span>

* <span data-ttu-id="39530-1753">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1753">Support configuring nsg</span></span>
* <span data-ttu-id="39530-1754">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1754">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="39530-1755">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="39530-1755">Support managed service identities</span></span>
* <span data-ttu-id="39530-1756">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1756">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="39530-1757">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="39530-1757">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="39530-1758">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="39530-1758">May 10, 2017</span></span>

<span data-ttu-id="39530-1759">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="39530-1759">Version 2.0.6</span></span>

* <span data-ttu-id="39530-1760">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="39530-1760">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="39530-1761">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1761">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="39530-1762">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1762">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="39530-1763">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1763">Include Cognitive Services module</span></span>
* <span data-ttu-id="39530-1764">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1764">Include Service Fabric module</span></span>
* <span data-ttu-id="39530-1765">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="39530-1765">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="39530-1766">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1766">Add support for CDN commands</span></span>
* <span data-ttu-id="39530-1767">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="39530-1767">Remove Container module</span></span>
* <span data-ttu-id="39530-1768">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="39530-1768">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="39530-1769">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="39530-1769">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="39530-1770">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1770">Core</span></span>

* <span data-ttu-id="39530-1771">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="39530-1771">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="39530-1772">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="39530-1772">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="39530-1773">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="39530-1773">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="39530-1774">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="39530-1774">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="39530-1775">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="39530-1775">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="39530-1776">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="39530-1776">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="39530-1777">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="39530-1777">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="39530-1778">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="39530-1778">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="39530-1779">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="39530-1779">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="39530-1780">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="39530-1780">core: Improved performance</span></span>
* <span data-ttu-id="39530-1781">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="39530-1781">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="39530-1782">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="39530-1782">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1783">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1783">ACS</span></span>

* <span data-ttu-id="39530-1784">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1784">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="39530-1785">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39530-1785">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="39530-1786">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39530-1786">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="39530-1787">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="39530-1787">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1788">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-1788">AppService</span></span>

* <span data-ttu-id="39530-1789">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1789">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="39530-1790">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1790">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="39530-1791">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="39530-1791">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="39530-1792">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="39530-1792">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="39530-1793">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="39530-1793">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="39530-1794">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="39530-1794">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="39530-1795">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="39530-1795">support slot swap with preview</span></span>
* <span data-ttu-id="39530-1796">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="39530-1796">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="39530-1797">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="39530-1797">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="39530-1798">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="39530-1798">CosmosDB</span></span>

* <span data-ttu-id="39530-1799">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="39530-1799">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="39530-1800">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1800">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="39530-1801">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1801">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="39530-1802">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1802">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="39530-1803">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="39530-1803">Data Lake Analytics</span></span>

* <span data-ttu-id="39530-1804">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1804">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="39530-1805">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="39530-1805">Add support for new catalog item type: package.</span></span> <span data-ttu-id="39530-1806">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="39530-1806">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="39530-1807">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="39530-1807">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="39530-1808">テーブル</span><span class="sxs-lookup"><span data-stu-id="39530-1808">Table</span></span>
  * <span data-ttu-id="39530-1809">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="39530-1809">Table valued function</span></span>
  * <span data-ttu-id="39530-1810">表示</span><span class="sxs-lookup"><span data-stu-id="39530-1810">View</span></span>
  * <span data-ttu-id="39530-1811">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="39530-1811">Table Statistics.</span></span> <span data-ttu-id="39530-1812">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="39530-1812">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="39530-1813">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="39530-1813">Data Lake Store</span></span>

* <span data-ttu-id="39530-1814">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="39530-1814">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="39530-1815">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="39530-1815">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="39530-1816">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="39530-1816">missed help for access show.</span></span> <span data-ttu-id="39530-1817">追加しました </span><span class="sxs-lookup"><span data-stu-id="39530-1817">adding it.</span></span> <span data-ttu-id="39530-1818">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="39530-1818">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="39530-1819">検索</span><span class="sxs-lookup"><span data-stu-id="39530-1819">Find</span></span>

* <span data-ttu-id="39530-1820">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="39530-1820">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="39530-1821">KeyVault</span><span class="sxs-lookup"><span data-stu-id="39530-1821">KeyVault</span></span>

* <span data-ttu-id="39530-1822">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="39530-1822">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="39530-1823">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="39530-1823">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="39530-1824">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="39530-1824">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="39530-1825">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1825">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="39530-1826">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="39530-1826">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="39530-1827">ラボ</span><span class="sxs-lookup"><span data-stu-id="39530-1827">Lab</span></span>

* <span data-ttu-id="39530-1828">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1828">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="39530-1829">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1829">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="39530-1830">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1830">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="39530-1831">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1831">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="39530-1832">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1832">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="39530-1833">監視</span><span class="sxs-lookup"><span data-stu-id="39530-1833">Monitor</span></span>

* <span data-ttu-id="39530-1834">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="39530-1834">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="39530-1835">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="39530-1835">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="39530-1836">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1836">Network</span></span>

* <span data-ttu-id="39530-1837">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1837">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="39530-1838">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1838">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="39530-1839">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1839">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="39530-1840">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1840">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="39530-1841">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1841">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="39530-1842">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1842">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="39530-1843">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1843">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="39530-1844">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1844">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="39530-1845">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1845">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="39530-1846">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1846">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="39530-1847">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="39530-1847">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="39530-1848">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1848">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="39530-1849">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1849">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="39530-1850">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="39530-1850">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="39530-1851">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="39530-1851">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="39530-1852">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1852">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="39530-1853">プロファイル</span><span class="sxs-lookup"><span data-stu-id="39530-1853">Profile</span></span>

* <span data-ttu-id="39530-1854">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="39530-1854">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="39530-1855">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="39530-1855">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="39530-1856">Redis</span><span class="sxs-lookup"><span data-stu-id="39530-1856">Redis</span></span>

* <span data-ttu-id="39530-1857">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1857">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="39530-1858">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="39530-1858">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="39530-1859">リソース</span><span class="sxs-lookup"><span data-stu-id="39530-1859">Resource</span></span>

* <span data-ttu-id="39530-1860">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="39530-1860">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="39530-1861">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="39530-1861">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="39530-1862">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="39530-1862">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="39530-1863">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="39530-1863">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="39530-1864">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="39530-1864">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="39530-1865">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="39530-1865">Add docs for az lock update.</span></span> <span data-ttu-id="39530-1866">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="39530-1866">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="39530-1867">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="39530-1867">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="39530-1868">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="39530-1868">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="39530-1869">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="39530-1869">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="39530-1870">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="39530-1870">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="39530-1871">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="39530-1871">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="39530-1872">Role</span><span class="sxs-lookup"><span data-stu-id="39530-1872">Role</span></span>

* <span data-ttu-id="39530-1873">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="39530-1873">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="39530-1874">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="39530-1874">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="39530-1875">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="39530-1875">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="39530-1876">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="39530-1876">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="39530-1877">SQL</span><span class="sxs-lookup"><span data-stu-id="39530-1877">SQL</span></span>

* <span data-ttu-id="39530-1878">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="39530-1878">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="39530-1879">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="39530-1879">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="39530-1880">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1880">Storage</span></span>

* <span data-ttu-id="39530-1881">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="39530-1881">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="39530-1882">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1882">Add support for incremental blob copy</span></span>
* <span data-ttu-id="39530-1883">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="39530-1883">Add support for large block blob upload</span></span>
* <span data-ttu-id="39530-1884">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="39530-1884">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1885">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1885">VM</span></span>

* <span data-ttu-id="39530-1886">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="39530-1886">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="39530-1887">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="39530-1887">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="39530-1888">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="39530-1888">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="39530-1889">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="39530-1889">az vm/vmss disk</span></span>
  3. <span data-ttu-id="39530-1890">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="39530-1890">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="39530-1891">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="39530-1891">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="39530-1892">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="39530-1892">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="39530-1893">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="39530-1893">April 3, 2017</span></span>

<span data-ttu-id="39530-1894">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="39530-1894">Version 2.0.2</span></span>

<span data-ttu-id="39530-1895">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="39530-1895">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="39530-1896">コア</span><span class="sxs-lookup"><span data-stu-id="39530-1896">Core</span></span>

* <span data-ttu-id="39530-1897">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="39530-1897">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="39530-1898">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="39530-1898">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="39530-1899">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="39530-1899">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="39530-1900">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="39530-1900">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="39530-1901">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="39530-1901">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="39530-1902">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="39530-1902">Add prompting for missing template parameters.</span></span> <span data-ttu-id="39530-1903">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="39530-1903">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="39530-1904">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="39530-1904">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="39530-1905">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="39530-1905">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="39530-1906">ACS</span><span class="sxs-lookup"><span data-stu-id="39530-1906">ACS</span></span>

* <span data-ttu-id="39530-1907">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="39530-1907">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="39530-1908">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="39530-1908">Add support for ssh key password prompting.</span></span> <span data-ttu-id="39530-1909">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="39530-1909">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="39530-1910">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="39530-1910">Add support for windows clusters.</span></span> <span data-ttu-id="39530-1911">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="39530-1911">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="39530-1912">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="39530-1912">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="39530-1913">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="39530-1913">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="39530-1914">AppService</span><span class="sxs-lookup"><span data-stu-id="39530-1914">AppService</span></span>

* <span data-ttu-id="39530-1915">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="39530-1915">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="39530-1916">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="39530-1916">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="39530-1917">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="39530-1917">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="39530-1918">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="39530-1918">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="39530-1919">DataLake</span><span class="sxs-lookup"><span data-stu-id="39530-1919">DataLake</span></span>

* <span data-ttu-id="39530-1920">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1920">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="39530-1921">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="39530-1921">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="39530-1922">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="39530-1922">DocuemntDB</span></span>

* <span data-ttu-id="39530-1923">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="39530-1923">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="39530-1924">VM</span><span class="sxs-lookup"><span data-stu-id="39530-1924">VM</span></span>

* <span data-ttu-id="39530-1925">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="39530-1925">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="39530-1926">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="39530-1926">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="39530-1927">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="39530-1927">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="39530-1928">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="39530-1928">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="39530-1929">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="39530-1929">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="39530-1930">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="39530-1930">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="39530-1931">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="39530-1931">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="39530-1932">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="39530-1932">February 27, 2017</span></span>

<span data-ttu-id="39530-1933">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="39530-1933">Version 2.0.0</span></span>

<span data-ttu-id="39530-1934">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="39530-1934">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="39530-1935">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="39530-1935">Container Service (acs)</span></span>
- <span data-ttu-id="39530-1936">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="39530-1936">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="39530-1937">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="39530-1937">Networking</span></span>
- <span data-ttu-id="39530-1938">Storage</span><span class="sxs-lookup"><span data-stu-id="39530-1938">Storage</span></span>

<span data-ttu-id="39530-1939">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="39530-1939">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="39530-1940">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="39530-1940">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="39530-1941">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="39530-1941">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="39530-1942">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="39530-1942">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="39530-1943">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="39530-1943">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="39530-1944">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="39530-1944">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="39530-1945">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="39530-1945">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="39530-1946">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="39530-1946">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="39530-1947">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="39530-1947">Provide feedback from the command line with the `az feedback` command</span></span>

