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
ms.openlocfilehash: 7a2ab41dd6696d658d05ab76e44abf97626761aa
ms.sourcegitcommit: 14aa16beeec59e51890a6cba4906bdc8e19b94d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2018
ms.locfileid: "52892685"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="ebcf3-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-103">Azure CLI release notes</span></span>
## <a name="december-4-2018"></a><span data-ttu-id="ebcf3-104">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-104">December 4, 2018</span></span>

<span data-ttu-id="ebcf3-105">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="ebcf3-105">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="ebcf3-106">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-106">Core</span></span>
* <span data-ttu-id="ebcf3-107">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-107">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="ebcf3-108">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-108">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-109">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-109">Appservice</span></span>
* <span data-ttu-id="ebcf3-110">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-110">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="ebcf3-111">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-111">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-112">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-112">Network</span></span>
* <span data-ttu-id="ebcf3-113">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-113">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-114">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-114">Role</span></span>
* <span data-ttu-id="ebcf3-115">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-115">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="ebcf3-116">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-116">VM</span></span>
* <span data-ttu-id="ebcf3-117">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-117">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="ebcf3-118">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-118">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="ebcf3-119">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-119">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="ebcf3-120">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-120">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="ebcf3-121">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-121">November 20, 2018</span></span>

<span data-ttu-id="ebcf3-122">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="ebcf3-122">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="ebcf3-123">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-123">Core</span></span>
* <span data-ttu-id="ebcf3-124">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-124">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-125">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-125">ACR</span></span>
* <span data-ttu-id="ebcf3-126">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-126">Added context token to task step</span></span>
* <span data-ttu-id="ebcf3-127">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-127">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="ebcf3-128">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-128">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-129">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-129">Appservice</span></span>
* <span data-ttu-id="ebcf3-130">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-130">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="ebcf3-131">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-131">Updated the default `node_version`.</span></span> <span data-ttu-id="ebcf3-132">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-132">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="ebcf3-133">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-133">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="ebcf3-134">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-134">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="ebcf3-135">IotCentral</span><span class="sxs-lookup"><span data-stu-id="ebcf3-135">IotCentral</span></span>
* <span data-ttu-id="ebcf3-136">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-136">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-137">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-137">KeyVault</span></span>
* <span data-ttu-id="ebcf3-138">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-138">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-139">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-139">Network</span></span>
* <span data-ttu-id="ebcf3-140">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-140">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="ebcf3-141">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-141">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="ebcf3-142">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-142">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="ebcf3-143">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-143">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-144">Rdbms</span><span class="sxs-lookup"><span data-stu-id="ebcf3-144">Rdbms</span></span>
* <span data-ttu-id="ebcf3-145">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-145">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="ebcf3-146">Rbac</span><span class="sxs-lookup"><span data-stu-id="ebcf3-146">Rbac</span></span>
* <span data-ttu-id="ebcf3-147">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-147">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="ebcf3-148">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-148">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="ebcf3-149">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-149">Storage</span></span>
* <span data-ttu-id="ebcf3-150">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-150">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="ebcf3-151">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-151">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="ebcf3-152">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-152">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="ebcf3-153">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-153">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-154">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-154">VM</span></span>
* <span data-ttu-id="ebcf3-155">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-155">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="ebcf3-156">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-156">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="ebcf3-157">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-157">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="ebcf3-158">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-158">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="ebcf3-159">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-159">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="ebcf3-160">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-160">Added `snapshot wait` command</span></span>
* <span data-ttu-id="ebcf3-161">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-161">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="ebcf3-162">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-162">November 6, 2018</span></span>

<span data-ttu-id="ebcf3-163">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="ebcf3-163">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-164">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-164">Core</span></span>
* <span data-ttu-id="ebcf3-165">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-165">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-166">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-166">ACR</span></span>
* <span data-ttu-id="ebcf3-167">タスク ソース トリガーのコミットおよびプル要求の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-167">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="ebcf3-168">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-168">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-169">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-169">ACS</span></span>
* <span data-ttu-id="ebcf3-170">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-170">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="ebcf3-171">Advisor</span><span class="sxs-lookup"><span data-stu-id="ebcf3-171">Advisor</span></span>
* <span data-ttu-id="ebcf3-172">GA リリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-172">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="ebcf3-173">AMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-173">AMS</span></span>
* <span data-ttu-id="ebcf3-174">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-174">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="ebcf3-175">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-175">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="ebcf3-176">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-176">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="ebcf3-177">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-177">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="ebcf3-178">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-178">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="ebcf3-179">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-179">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="ebcf3-180">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-180">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="ebcf3-181">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-181">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="ebcf3-182">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-182">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="ebcf3-183">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-183">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="ebcf3-184">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-184">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="ebcf3-185">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-185">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="ebcf3-186">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-186">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="ebcf3-187">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-187">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="ebcf3-188">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-188">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="ebcf3-189">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-189">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="ebcf3-190">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-190">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-191">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-191">AppService</span></span>
* <span data-ttu-id="ebcf3-192">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-192">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="ebcf3-193">構成</span><span class="sxs-lookup"><span data-stu-id="ebcf3-193">Configure</span></span>
* <span data-ttu-id="ebcf3-194">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-194">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-195">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-195">Container</span></span>
* <span data-ttu-id="ebcf3-196">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-196">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="ebcf3-197">EventHub</span><span class="sxs-lookup"><span data-stu-id="ebcf3-197">EventHub</span></span>
* <span data-ttu-id="ebcf3-198">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-198">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-199">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-199">Interactive</span></span>
* <span data-ttu-id="ebcf3-200">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-200">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-201">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-201">Monitor</span></span>
* <span data-ttu-id="ebcf3-202">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-202">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-203">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-203">Network</span></span>
* <span data-ttu-id="ebcf3-204">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-204">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="ebcf3-205">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-205">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="ebcf3-206">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-206">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="ebcf3-207">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-207">Profile</span></span>
* <span data-ttu-id="ebcf3-208">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-208">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-209">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-209">RDBMS</span></span>
* <span data-ttu-id="ebcf3-210">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-210">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-211">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-211">Resource</span></span>
* <span data-ttu-id="ebcf3-212">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-212">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-213">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-213">Role</span></span>
* <span data-ttu-id="ebcf3-214">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-214">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="ebcf3-215">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-215">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="ebcf3-216">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-216">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-217">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-217">Storage</span></span>
* <span data-ttu-id="ebcf3-218">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-218">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-219">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-219">VM</span></span>
* <span data-ttu-id="ebcf3-220">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-220">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="ebcf3-221">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-221">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="ebcf3-222">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-222">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="ebcf3-223">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-223">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="ebcf3-224">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-224">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="ebcf3-225">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-225">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="ebcf3-226">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-226">October 23, 2018</span></span>

<span data-ttu-id="ebcf3-227">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="ebcf3-227">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-228">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-228">Core</span></span>
* <span data-ttu-id="ebcf3-229">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-229">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="ebcf3-230">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-230">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-231">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-231">ACR</span></span>
* <span data-ttu-id="ebcf3-232">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-232">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="ebcf3-233">CDN</span><span class="sxs-lookup"><span data-stu-id="ebcf3-233">CDN</span></span>
* <span data-ttu-id="ebcf3-234">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-234">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="ebcf3-235">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-235">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-236">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-236">Container</span></span>
* <span data-ttu-id="ebcf3-237">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-237">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="ebcf3-238">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-238">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="ebcf3-239">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-239">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="ebcf3-240">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-240">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="ebcf3-241">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-241">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="ebcf3-242">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-242">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="ebcf3-243">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-243">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ebcf3-244">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-244">CosmosDB</span></span>
* <span data-ttu-id="ebcf3-245">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-245">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-246">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-246">Interactive</span></span>
* <span data-ttu-id="ebcf3-247">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-247">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="ebcf3-248">IoT Central</span><span class="sxs-lookup"><span data-stu-id="ebcf3-248">IoT Central</span></span>
* <span data-ttu-id="ebcf3-249">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-249">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="ebcf3-250">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-250">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-251">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-251">Monitor</span></span>
* <span data-ttu-id="ebcf3-252">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="ebcf3-252">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="ebcf3-253">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-253">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="ebcf3-254">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-254">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="ebcf3-255">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-255">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="ebcf3-256">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-256">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="ebcf3-257">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-257">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="ebcf3-258">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="ebcf3-258">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="ebcf3-259">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-259">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="ebcf3-260">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-260">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="ebcf3-261">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-261">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-262">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-262">Network</span></span>
* <span data-ttu-id="ebcf3-263">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-263">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="ebcf3-264">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-264">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="ebcf3-265">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ebcf3-265">ServiceBus</span></span>
* <span data-ttu-id="ebcf3-266">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-266">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-267">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-267">SQL</span></span>
* <span data-ttu-id="ebcf3-268">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-268">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-269">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-269">Storage</span></span>
* <span data-ttu-id="ebcf3-270">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-270">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="ebcf3-271">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-271">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-272">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-272">VM</span></span>
* <span data-ttu-id="ebcf3-273">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-273">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="ebcf3-274">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-274">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="ebcf3-275">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-275">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="ebcf3-276">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-276">October 16, 2018</span></span>

<span data-ttu-id="ebcf3-277">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="ebcf3-277">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-278">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-278">VM</span></span>
* <span data-ttu-id="ebcf3-279">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-279">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="ebcf3-280">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-280">October 9, 2018</span></span>

<span data-ttu-id="ebcf3-281">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="ebcf3-281">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-282">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-282">Core</span></span>
* <span data-ttu-id="ebcf3-283">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-283">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-284">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-284">ACR</span></span>
* <span data-ttu-id="ebcf3-285">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-285">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-286">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-286">ACS</span></span>
* <span data-ttu-id="ebcf3-287">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="ebcf3-287">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="ebcf3-288">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-288">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="ebcf3-289">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-289">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="ebcf3-290">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-290">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-291">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-291">Container</span></span>
* <span data-ttu-id="ebcf3-292">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-292">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="ebcf3-293">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-293">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="ebcf3-294">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-294">Event Hub</span></span>
* <span data-ttu-id="ebcf3-295">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-295">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="ebcf3-296">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-296">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="ebcf3-297">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-297">Extensions</span></span>
* <span data-ttu-id="ebcf3-298">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-298">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="ebcf3-299">HDInsight</span><span class="sxs-lookup"><span data-stu-id="ebcf3-299">HDInsight</span></span>
* <span data-ttu-id="ebcf3-300">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-300">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-301">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-301">IoT</span></span>
* <span data-ttu-id="ebcf3-302">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-302">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-303">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-303">KeyVault</span></span>
* <span data-ttu-id="ebcf3-304">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-304">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-305">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-305">Network</span></span>
* <span data-ttu-id="ebcf3-306">`network dns zone create` を修正しました: ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-306">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="ebcf3-307">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-307">See #6052</span></span>
* <span data-ttu-id="ebcf3-308">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-308">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="ebcf3-309">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-309">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="ebcf3-310">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-310">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="ebcf3-311">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-311">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="ebcf3-312">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-312">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="ebcf3-313">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-313">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-314">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-314">Role</span></span>
* <span data-ttu-id="ebcf3-315">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-315">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="ebcf3-316">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-316">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="ebcf3-317">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-317">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="ebcf3-318">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-318">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="ebcf3-319">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ebcf3-319">Service Bus</span></span>
* <span data-ttu-id="ebcf3-320">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-320">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-321">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-321">VM</span></span>
* <span data-ttu-id="ebcf3-322">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-322">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="ebcf3-323">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-323">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="ebcf3-324">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-324">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="ebcf3-325">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-325">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="ebcf3-326">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-326">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="ebcf3-327">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-327">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="ebcf3-328">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-328">September 21, 2018</span></span>

<span data-ttu-id="ebcf3-329">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="ebcf3-329">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-330">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-330">ACR</span></span>
* <span data-ttu-id="ebcf3-331">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-331">Added ACR Task commands</span></span>
* <span data-ttu-id="ebcf3-332">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-332">Added quick run command</span></span>
* <span data-ttu-id="ebcf3-333">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-333">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="ebcf3-334">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-334">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="ebcf3-335">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-335">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="ebcf3-336">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-336">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-337">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-337">ACS</span></span>
* <span data-ttu-id="ebcf3-338">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-338">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="ebcf3-339">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-339">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-340">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-340">AppService</span></span>

* <span data-ttu-id="ebcf3-341">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-341">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="ebcf3-342">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-342">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="ebcf3-343">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-343">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="ebcf3-344">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-344">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-345">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-345">Batch</span></span>
* <span data-ttu-id="ebcf3-346">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-346">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="ebcf3-347">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-347">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="ebcf3-348">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-348">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="ebcf3-349">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-349">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ebcf3-350">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-350">Batch AI</span></span> 
* <span data-ttu-id="ebcf3-351">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-351">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ebcf3-352">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ebcf3-352">Cognitive Services</span></span>
* <span data-ttu-id="ebcf3-353">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-353">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="ebcf3-354">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-354">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="ebcf3-355">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-355">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="ebcf3-356">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-356">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="ebcf3-357">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-357">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="ebcf3-358">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-358">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-359">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-359">Container</span></span>
* <span data-ttu-id="ebcf3-360">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-360">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="ebcf3-361">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-361">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="ebcf3-362">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-362">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="ebcf3-363">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-363">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="ebcf3-364">DataLake</span><span class="sxs-lookup"><span data-stu-id="ebcf3-364">Datalake</span></span>
* <span data-ttu-id="ebcf3-365">仮想ネットワーク ルール用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-365">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="ebcf3-366">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-366">Interactive Shell</span></span>
* <span data-ttu-id="ebcf3-367">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-367">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="ebcf3-368">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-368">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-369">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-369">IoT</span></span>
* <span data-ttu-id="ebcf3-370">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-370">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="ebcf3-371">Key Vault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-371">Key Vault</span></span>
* <span data-ttu-id="ebcf3-372">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-372">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-373">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-373">Network</span></span>
* <span data-ttu-id="ebcf3-374">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-374">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="ebcf3-375">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-375">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="ebcf3-376">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-376">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="ebcf3-377">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-377">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="ebcf3-378">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-378">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="ebcf3-379">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-379">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="ebcf3-380">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-380">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="ebcf3-381">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-381">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="ebcf3-382">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-382">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="ebcf3-383">`network express-route create/update`: `--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-383">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="ebcf3-384">`network vnet subnet create/update`: `--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-384">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="ebcf3-385">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-385">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="ebcf3-386">`network traffic-manager profile create/update`: 監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、`--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-386">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="ebcf3-387">`network lb frontend-ip create/update`: プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-387">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="ebcf3-388">`dns record-set * create/update`: `--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-388">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="ebcf3-389">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-389">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="ebcf3-390">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-390">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="ebcf3-391">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-391">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-392">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-392">RDBMS</span></span>
* <span data-ttu-id="ebcf3-393">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-393">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="ebcf3-394">予約</span><span class="sxs-lookup"><span data-stu-id="ebcf3-394">Reservation</span></span>
* <span data-ttu-id="ebcf3-395">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-395">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="ebcf3-396">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-396">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="ebcf3-397">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="ebcf3-397">Manage App</span></span>
* <span data-ttu-id="ebcf3-398">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-398">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="ebcf3-399">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-399">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-400">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-400">Role</span></span>
* <span data-ttu-id="ebcf3-401">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-401">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="ebcf3-402">SignalR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-402">SignalR</span></span>
* <span data-ttu-id="ebcf3-403">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-403">First release</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-404">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-404">Storage</span></span>
* <span data-ttu-id="ebcf3-405">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-405">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="ebcf3-406">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-406">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-407">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-407">VM</span></span>
* <span data-ttu-id="ebcf3-408">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-408">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="ebcf3-409">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-409">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="ebcf3-410">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-410">August 28, 2018</span></span>

<span data-ttu-id="ebcf3-411">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="ebcf3-411">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-412">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-412">Core</span></span>

* <span data-ttu-id="ebcf3-413">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-413">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="ebcf3-414">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-414">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-415">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-415">ACR</span></span>

* <span data-ttu-id="ebcf3-416">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-416">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="ebcf3-417">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-417">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-418">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-418">ACS</span></span>

* <span data-ttu-id="ebcf3-419">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-419">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="ebcf3-420">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-420">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-421">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-421">AppService</span></span>

* <span data-ttu-id="ebcf3-422">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-422">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="ebcf3-423">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-423">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="ebcf3-424">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-424">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="ebcf3-425">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-425">Backup</span></span>

* <span data-ttu-id="ebcf3-426">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-426">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="ebcf3-427">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="ebcf3-427">Bot Service</span></span>

* <span data-ttu-id="ebcf3-428">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-428">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ebcf3-429">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ebcf3-429">Cognitive Services</span></span>

* <span data-ttu-id="ebcf3-430">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-430">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-431">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-431">IoT</span></span>

* <span data-ttu-id="ebcf3-432">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-432">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-433">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-433">Monitor</span></span>

* <span data-ttu-id="ebcf3-434">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-434">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="ebcf3-435">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-435">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-436">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-436">Network</span></span>

* <span data-ttu-id="ebcf3-437">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-437">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-438">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-438">Resource</span></span>

* <span data-ttu-id="ebcf3-439">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-439">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-440">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-440">Storage</span></span>

* <span data-ttu-id="ebcf3-441">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-441">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-442">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-442">VM</span></span>

* <span data-ttu-id="ebcf3-443">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-443">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="ebcf3-444">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-444">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="ebcf3-445">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-445">Auguest 14, 2018</span></span>

<span data-ttu-id="ebcf3-446">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="ebcf3-446">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-447">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-447">Core</span></span>

* <span data-ttu-id="ebcf3-448">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-448">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="ebcf3-449">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-449">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="ebcf3-450">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-450">Telemetry</span></span>

* <span data-ttu-id="ebcf3-451">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-451">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-452">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-452">ACR</span></span>

* <span data-ttu-id="ebcf3-453">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-453">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="ebcf3-454">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-454">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-455">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-455">ACS</span></span>

* <span data-ttu-id="ebcf3-456">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-456">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="ebcf3-457">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-457">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="ebcf3-458">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-458">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="ebcf3-459">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-459">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="ebcf3-460">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-460">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="ebcf3-461">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-461">AppService</span></span>

* <span data-ttu-id="ebcf3-462">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-462">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="ebcf3-463">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-463">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="ebcf3-464">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-464">BatchAI</span></span>

* <span data-ttu-id="ebcf3-465">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-465">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="ebcf3-466">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-466">Container</span></span>

* <span data-ttu-id="ebcf3-467">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-467">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="ebcf3-468">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-468">IoT</span></span>

* <span data-ttu-id="ebcf3-469">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-469">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="ebcf3-470">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-470">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="ebcf3-471">Iot Central</span><span class="sxs-lookup"><span data-stu-id="ebcf3-471">Iot Central</span></span>

* <span data-ttu-id="ebcf3-472">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-472">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-473">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-473">KeyVault</span></span>


* <span data-ttu-id="ebcf3-474">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-474">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="ebcf3-475">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-475">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="ebcf3-476">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-476">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="ebcf3-477">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-477">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="ebcf3-478">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-478">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="ebcf3-479">リレー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-479">Relay</span></span>

* <span data-ttu-id="ebcf3-480">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-480">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-481">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-481">Sql</span></span>

* <span data-ttu-id="ebcf3-482">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-482">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-483">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-483">Storage</span></span>

* <span data-ttu-id="ebcf3-484">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-484">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="ebcf3-485">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-485">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="ebcf3-486">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-486">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="ebcf3-487">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-487">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="ebcf3-488">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-488">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-489">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-489">VM</span></span>

* <span data-ttu-id="ebcf3-490">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-490">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="ebcf3-491">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-491">July 31, 2018</span></span>

<span data-ttu-id="ebcf3-492">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="ebcf3-492">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-493">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-493">ACR</span></span>

* <span data-ttu-id="ebcf3-494">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-494">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="ebcf3-495">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-495">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-496">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-496">ACS</span></span>

* <span data-ttu-id="ebcf3-497">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-497">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-498">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-498">Batch</span></span>

* <span data-ttu-id="ebcf3-499">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-499">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-500">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-500">Container</span></span>

* <span data-ttu-id="ebcf3-501">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-501">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-502">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-502">Network</span></span>

* <span data-ttu-id="ebcf3-503">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-503">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="ebcf3-504">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-504">Resource</span></span>

* <span data-ttu-id="ebcf3-505">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-505">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="ebcf3-506">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-506">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-507">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-507">Role</span></span>

* <span data-ttu-id="ebcf3-508">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-508">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="ebcf3-509">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-509">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="ebcf3-510">Search</span><span class="sxs-lookup"><span data-stu-id="ebcf3-510">Search</span></span>

* <span data-ttu-id="ebcf3-511">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-511">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="ebcf3-512">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ebcf3-512">Service Bus</span></span>

* <span data-ttu-id="ebcf3-513">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-513">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="ebcf3-514">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-514">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="ebcf3-515">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-515">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="ebcf3-516">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-516">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-517">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-517">Storage</span></span>

* <span data-ttu-id="ebcf3-518">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-518">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="ebcf3-519">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-519">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-520">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-520">VM</span></span>

* <span data-ttu-id="ebcf3-521">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-521">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="ebcf3-522">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-522">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="ebcf3-523">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-523">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="ebcf3-524">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-524">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="ebcf3-525">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-525">July 18, 2018</span></span>

<span data-ttu-id="ebcf3-526">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="ebcf3-526">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-527">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-527">Core</span></span>

* <span data-ttu-id="ebcf3-528">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-528">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="ebcf3-529">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-529">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="ebcf3-530">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-530">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-531">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-531">ACR</span></span>

* <span data-ttu-id="ebcf3-532">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-532">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="ebcf3-533">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-533">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="ebcf3-534">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-534">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="ebcf3-535">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-535">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-536">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-536">ACS</span></span>

* <span data-ttu-id="ebcf3-537">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-537">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-538">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-538">AppService</span></span>

* <span data-ttu-id="ebcf3-539">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-539">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-540">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-540">Batch</span></span>

* <span data-ttu-id="ebcf3-541">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-541">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="ebcf3-542">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-542">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ebcf3-543">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-543">Batch AI</span></span>

* <span data-ttu-id="ebcf3-544">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-544">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-545">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-545">Container</span></span>

* <span data-ttu-id="ebcf3-546">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-546">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="ebcf3-547">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-547">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-548">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-548">Network</span></span>

* <span data-ttu-id="ebcf3-549">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-549">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="ebcf3-550">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-550">Added `network nic wait`</span></span>
* <span data-ttu-id="ebcf3-551">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-551">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="ebcf3-552">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-552">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="ebcf3-553">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-553">Resource</span></span>

* <span data-ttu-id="ebcf3-554">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-554">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="ebcf3-555">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-555">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="ebcf3-556">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-556">Added `deployment wait` command</span></span>
* <span data-ttu-id="ebcf3-557">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-557">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-558">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-558">SQL</span></span>

* <span data-ttu-id="ebcf3-559">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-559">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="ebcf3-560">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-560">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="ebcf3-561">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-561">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-562">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-562">Storage</span></span>

* <span data-ttu-id="ebcf3-563">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-563">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-564">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-564">VM</span></span>

* <span data-ttu-id="ebcf3-565">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-565">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="ebcf3-566">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-566">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="ebcf3-567">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-567">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="ebcf3-568">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-568">July 3, 2018</span></span>

<span data-ttu-id="ebcf3-569">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="ebcf3-569">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="ebcf3-570">AKS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-570">AKS</span></span>

* <span data-ttu-id="ebcf3-571">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-571">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="ebcf3-572">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-572">July 3, 2018</span></span>

<span data-ttu-id="ebcf3-573">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="ebcf3-573">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-574">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-574">Core</span></span>

* <span data-ttu-id="ebcf3-575">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-575">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-576">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-576">ACR</span></span>

* <span data-ttu-id="ebcf3-577">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-577">Added polling build status</span></span>
* <span data-ttu-id="ebcf3-578">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-578">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="ebcf3-579">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-579">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-580">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-580">ACS</span></span>

* <span data-ttu-id="ebcf3-581">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-581">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="ebcf3-582">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-582">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="ebcf3-583">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-583">Updated options for `aks browse` command.</span></span> <span data-ttu-id="ebcf3-584">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-584">Added `--listen-port` support</span></span>
* <span data-ttu-id="ebcf3-585">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-585">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="ebcf3-586">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-586">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="ebcf3-587">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-587">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-588">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-588">AppService</span></span>

* <span data-ttu-id="ebcf3-589">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-589">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="ebcf3-590">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-590">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="ebcf3-591">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-591">Backup</span></span>

* <span data-ttu-id="ebcf3-592">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-592">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="ebcf3-593">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-593">BatchAI</span></span>

* <span data-ttu-id="ebcf3-594">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-594">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="ebcf3-595">クラウド</span><span class="sxs-lookup"><span data-stu-id="ebcf3-595">Cloud</span></span>

* <span data-ttu-id="ebcf3-596">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-596">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-597">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-597">Container</span></span>

* <span data-ttu-id="ebcf3-598">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-598">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="ebcf3-599">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-599">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="ebcf3-600">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-600">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-601">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-601">Extension</span></span>

* <span data-ttu-id="ebcf3-602">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-602">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-603">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-603">Network</span></span>

* <span data-ttu-id="ebcf3-604">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-604">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-605">Rdbms</span><span class="sxs-lookup"><span data-stu-id="ebcf3-605">Rdbms</span></span>

* <span data-ttu-id="ebcf3-606">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-606">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-607">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-607">Resource</span></span>

* <span data-ttu-id="ebcf3-608">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-608">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-609">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-609">VM</span></span>

* <span data-ttu-id="ebcf3-610">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-610">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="ebcf3-611">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-611">June 25, 2018</span></span>

<span data-ttu-id="ebcf3-612">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="ebcf3-612">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="ebcf3-613">CLI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-613">CLI</span></span>

* <span data-ttu-id="ebcf3-614">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-614">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="ebcf3-615">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-615">June 19, 2018</span></span>

<span data-ttu-id="ebcf3-616">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="ebcf3-616">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-617">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-617">Core</span></span>

* <span data-ttu-id="ebcf3-618">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-618">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-619">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-619">ACR</span></span>

* <span data-ttu-id="ebcf3-620">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-620">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="ebcf3-621">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-621">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-622">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-622">ACS</span></span>

* <span data-ttu-id="ebcf3-623">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-623">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="ebcf3-624">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-624">Added `--update` support</span></span>
* <span data-ttu-id="ebcf3-625">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-625">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="ebcf3-626">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-626">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="ebcf3-627">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-627">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="ebcf3-628">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-628">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="ebcf3-629">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-629">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="ebcf3-630">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-630">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-631">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-631">AppService</span></span>

* <span data-ttu-id="ebcf3-632">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-632">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="ebcf3-633">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-633">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-634">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-634">Batch</span></span>

* <span data-ttu-id="ebcf3-635">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-635">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ebcf3-636">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-636">Batch AI</span></span>

* <span data-ttu-id="ebcf3-637">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-637">Added support for workspaces.</span></span> <span data-ttu-id="ebcf3-638">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-638">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="ebcf3-639">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-639">Added support for experiments.</span></span> <span data-ttu-id="ebcf3-640">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-640">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="ebcf3-641">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-641">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="ebcf3-642">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-642">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="ebcf3-643">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-643">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="ebcf3-644">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-644">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="ebcf3-645">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-645">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="ebcf3-646">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-646">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="ebcf3-647">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-647">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="ebcf3-648">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-648">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="ebcf3-649">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-649">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="ebcf3-650">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-650">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="ebcf3-651">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-651">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="ebcf3-652">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-652">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="ebcf3-653">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-653">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="ebcf3-654">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-654">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="ebcf3-655">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-655">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="ebcf3-656">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-656">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="ebcf3-657">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-657">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="ebcf3-658">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-658">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="ebcf3-659">マップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-659">Maps</span></span>

* <span data-ttu-id="ebcf3-660">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-660">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-661">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-661">Network</span></span>

* <span data-ttu-id="ebcf3-662">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-662">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="ebcf3-663">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-663">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="ebcf3-664">#6502</span><span class="sxs-lookup"><span data-stu-id="ebcf3-664">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="ebcf3-665">Reservations</span><span class="sxs-lookup"><span data-stu-id="ebcf3-665">Reservations</span></span>

* <span data-ttu-id="ebcf3-666">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-666">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="ebcf3-667">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-667">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="ebcf3-668">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-668">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="ebcf3-669">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-669">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="ebcf3-670">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-670">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="ebcf3-671">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-671">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-672">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-672">Role</span></span>

* <span data-ttu-id="ebcf3-673">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-673">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-674">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-674">SQL</span></span>

* <span data-ttu-id="ebcf3-675">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-675">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-676">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-676">Storage</span></span>

* <span data-ttu-id="ebcf3-677">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-677">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-678">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-678">VM</span></span>

* <span data-ttu-id="ebcf3-679">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-679">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="ebcf3-680">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-680">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="ebcf3-681">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-681">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="ebcf3-682">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-682">June 13, 2018</span></span>

<span data-ttu-id="ebcf3-683">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="ebcf3-683">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-684">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-684">Core</span></span>

* <span data-ttu-id="ebcf3-685">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-685">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="ebcf3-686">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-686">June 13, 2018</span></span>

<span data-ttu-id="ebcf3-687">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="ebcf3-687">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="ebcf3-688">AKS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-688">AKS</span></span>

* <span data-ttu-id="ebcf3-689">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-689">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="ebcf3-690">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-690">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="ebcf3-691">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-691">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="ebcf3-692">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-692">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="ebcf3-693">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-693">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-694">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-694">AppService</span></span>

* <span data-ttu-id="ebcf3-695">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-695">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="ebcf3-696">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-696">June 5, 2018</span></span>

<span data-ttu-id="ebcf3-697">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="ebcf3-697">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-698">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-698">Interactive</span></span>

* <span data-ttu-id="ebcf3-699">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-699">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="ebcf3-700">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-700">June 5, 2018</span></span>

<span data-ttu-id="ebcf3-701">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="ebcf3-701">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-702">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-702">Core</span></span>

* <span data-ttu-id="ebcf3-703">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-703">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="ebcf3-704">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-704">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-705">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-705">ACR</span></span>

* <span data-ttu-id="ebcf3-706">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-706">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="ebcf3-707">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-707">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="ebcf3-708">AKS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-708">AKS</span></span>

* <span data-ttu-id="ebcf3-709">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-709">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-710">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-710">Batch</span></span>

* <span data-ttu-id="ebcf3-711">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-711">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-712">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-712">IOT</span></span>

* <span data-ttu-id="ebcf3-713">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-713">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-714">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-714">Network</span></span>

* <span data-ttu-id="ebcf3-715">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-715">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="ebcf3-716">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="ebcf3-716">Policy Insights</span></span>

* <span data-ttu-id="ebcf3-717">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-717">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="ebcf3-718">ARM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-718">ARM</span></span>

* <span data-ttu-id="ebcf3-719">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-719">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-720">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-720">SQL</span></span>

* <span data-ttu-id="ebcf3-721">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-721">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="ebcf3-722">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-722">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="ebcf3-723">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-723">Storage</span></span>

* <span data-ttu-id="ebcf3-724">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-724">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-725">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-725">VM</span></span>

* <span data-ttu-id="ebcf3-726">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-726">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="ebcf3-727">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-727">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="ebcf3-728">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-728">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="ebcf3-729">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-729">May 22, 2018</span></span>

<span data-ttu-id="ebcf3-730">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="ebcf3-730">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-731">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-731">Core</span></span>

* <span data-ttu-id="ebcf3-732">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-732">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-733">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-733">ACS</span></span>

* <span data-ttu-id="ebcf3-734">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-734">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="ebcf3-735">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-735">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-736">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-736">AppService</span></span>

* <span data-ttu-id="ebcf3-737">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-737">Improved generic update commands</span></span>
* <span data-ttu-id="ebcf3-738">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-738">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-739">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-739">Container</span></span>

* <span data-ttu-id="ebcf3-740">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-740">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="ebcf3-741">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-741">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-742">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-742">Extension</span></span>

* <span data-ttu-id="ebcf3-743">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-743">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-744">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-744">Interactive</span></span>

* <span data-ttu-id="ebcf3-745">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-745">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="ebcf3-746">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-746">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-747">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-747">KeyVault</span></span>

* <span data-ttu-id="ebcf3-748">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-748">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-749">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-749">Network</span></span>

* <span data-ttu-id="ebcf3-750">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-750">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="ebcf3-751">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-751">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-752">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-752">SQL</span></span>

* <span data-ttu-id="ebcf3-753">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-753">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="ebcf3-754">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-754">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="ebcf3-755">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-755">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="ebcf3-756">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-756">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="ebcf3-757">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-757">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="ebcf3-758">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-758">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="ebcf3-759">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-759">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="ebcf3-760">`edition`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-760">`edition`.</span></span> <span data-ttu-id="ebcf3-761">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-761">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="ebcf3-762">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-762">`elasticPoolName`.</span></span> <span data-ttu-id="ebcf3-763">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-763">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="ebcf3-764">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-764">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="ebcf3-765">`edition`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-765">`edition`.</span></span> <span data-ttu-id="ebcf3-766">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-766">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="ebcf3-767">`dtu`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-767">`dtu`.</span></span> <span data-ttu-id="ebcf3-768">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-768">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="ebcf3-769">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-769">`databaseDtuMin`.</span></span> <span data-ttu-id="ebcf3-770">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-770">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="ebcf3-771">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-771">`databaseDtuMax`.</span></span> <span data-ttu-id="ebcf3-772">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-772">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="ebcf3-773">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-773">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="ebcf3-774">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-774">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-775">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-775">Storage</span></span>

* <span data-ttu-id="ebcf3-776">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-776">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="ebcf3-777">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-777">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-778">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-778">VM</span></span>

* <span data-ttu-id="ebcf3-779">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-779">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="ebcf3-780">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-780">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="ebcf3-781">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-781">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="ebcf3-782">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-782">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="ebcf3-783">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-783">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="ebcf3-784">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-784">May 7, 2018</span></span>

<span data-ttu-id="ebcf3-785">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="ebcf3-785">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-786">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-786">Core</span></span>

* <span data-ttu-id="ebcf3-787">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-787">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="ebcf3-788">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-788">Added limited support for positional arguments</span></span>
* <span data-ttu-id="ebcf3-789">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-789">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="ebcf3-790">#5591</span><span class="sxs-lookup"><span data-stu-id="ebcf3-790">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="ebcf3-791">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-791">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="ebcf3-792">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-792">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="ebcf3-793">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-793">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="ebcf3-794">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-794">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="ebcf3-795">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-795">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-796">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-796">ACR</span></span>

* <span data-ttu-id="ebcf3-797">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-797">Added ACR Build commands</span></span>
* <span data-ttu-id="ebcf3-798">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-798">Improved resource not found error messages</span></span>
* <span data-ttu-id="ebcf3-799">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-799">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="ebcf3-800">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-800">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="ebcf3-801">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-801">Improved repository commands error messages</span></span>
* <span data-ttu-id="ebcf3-802">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-802">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-803">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-803">ACS</span></span>

* <span data-ttu-id="ebcf3-804">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-804">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="ebcf3-805">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-805">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="ebcf3-806">AMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-806">AMS</span></span>

* <span data-ttu-id="ebcf3-807">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="ebcf3-807">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-808">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-808">Appservice</span></span>

* <span data-ttu-id="ebcf3-809">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-809">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="ebcf3-810">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-810">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="ebcf3-811">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-811">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="ebcf3-812">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-812">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="ebcf3-813">Batch AI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-813">Batch AI</span></span>

* <span data-ttu-id="ebcf3-814">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-814">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ebcf3-815">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ebcf3-815">Cognitive Services</span></span>

* <span data-ttu-id="ebcf3-816">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-816">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="ebcf3-817">消費</span><span class="sxs-lookup"><span data-stu-id="ebcf3-817">Consumption</span></span>

* <span data-ttu-id="ebcf3-818">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-818">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-819">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-819">Container</span></span>

* <span data-ttu-id="ebcf3-820">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-820">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="ebcf3-821">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-821">Cosmos DB</span></span>

* <span data-ttu-id="ebcf3-822">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-822">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="ebcf3-823">DMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-823">DMS</span></span>

* <span data-ttu-id="ebcf3-824">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-824">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-825">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-825">Extension</span></span>

* <span data-ttu-id="ebcf3-826">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-826">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-827">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-827">Interactive</span></span>

* <span data-ttu-id="ebcf3-828">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-828">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="ebcf3-829">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-829">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="ebcf3-830">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-830">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="ebcf3-831">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-831">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="ebcf3-832">ラボ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-832">Lab</span></span>

* <span data-ttu-id="ebcf3-833">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-833">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-834">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-834">Network</span></span>

* <span data-ttu-id="ebcf3-835">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-835">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="ebcf3-836">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-836">Profile</span></span>

* <span data-ttu-id="ebcf3-837">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-837">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="ebcf3-838">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-838">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="ebcf3-839">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-839">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="ebcf3-840">Redis</span><span class="sxs-lookup"><span data-stu-id="ebcf3-840">Redis</span></span>

* <span data-ttu-id="ebcf3-841">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-841">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="ebcf3-842">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-842">Deprecated `redis list-all`.</span></span> <span data-ttu-id="ebcf3-843">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-843">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="ebcf3-844">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-844">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="ebcf3-845">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-845">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-846">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-846">Role</span></span>

* <span data-ttu-id="ebcf3-847">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-847">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-848">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-848">Storage</span></span>

* <span data-ttu-id="ebcf3-849">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-849">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="ebcf3-850">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-850">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="ebcf3-851">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="ebcf3-851">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="ebcf3-852">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-852">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="ebcf3-853">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-853">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-854">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-854">VM</span></span>

* <span data-ttu-id="ebcf3-855">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-855">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="ebcf3-856">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-856">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="ebcf3-857">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-857">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="ebcf3-858">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-858">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="ebcf3-859">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-859">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="ebcf3-860">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-860">Added write accelerator support</span></span>
* <span data-ttu-id="ebcf3-861">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-861">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="ebcf3-862">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-862">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="ebcf3-863">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-863">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="ebcf3-864">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-864">April 10, 2018</span></span>

<span data-ttu-id="ebcf3-865">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="ebcf3-865">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-866">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-866">ACR</span></span>

* <span data-ttu-id="ebcf3-867">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-867">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-868">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-868">ACS</span></span>

* <span data-ttu-id="ebcf3-869">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-869">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-870">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-870">Appservice</span></span>

* [重大な変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="ebcf3-872">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-872">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="ebcf3-873">BatchAI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-873">BatchAI</span></span>

* <span data-ttu-id="ebcf3-874">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-874">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="ebcf3-875">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="ebcf3-875">Job level mounting</span></span>
  - <span data-ttu-id="ebcf3-876">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="ebcf3-876">Environment variables with secret values</span></span>
  - <span data-ttu-id="ebcf3-877">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="ebcf3-877">Performance counters settings</span></span>
  - <span data-ttu-id="ebcf3-878">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-878">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="ebcf3-879">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-879">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="ebcf3-880">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-880">Usage and limits reporting</span></span>
  - <span data-ttu-id="ebcf3-881">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-881">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="ebcf3-882">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-882">Support for custom images</span></span>
  - <span data-ttu-id="ebcf3-883">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-883">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="ebcf3-884">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-884">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="ebcf3-885">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-885">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="ebcf3-886">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="ebcf3-886">National clouds are supported</span></span>
* <span data-ttu-id="ebcf3-887">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-887">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="ebcf3-888">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-888">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="ebcf3-889">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-889">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="ebcf3-890">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-890">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="ebcf3-891">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-891">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="ebcf3-892">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-892">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="ebcf3-893">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-893">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="ebcf3-894">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-894">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="ebcf3-895">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="ebcf3-895">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="ebcf3-896">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-896">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="ebcf3-897">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-897">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="ebcf3-898">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-898">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="ebcf3-899">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-899">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="ebcf3-900">課金</span><span class="sxs-lookup"><span data-stu-id="ebcf3-900">Billing</span></span>

* <span data-ttu-id="ebcf3-901">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-901">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="ebcf3-902">消費</span><span class="sxs-lookup"><span data-stu-id="ebcf3-902">Consumption</span></span>

* <span data-ttu-id="ebcf3-903">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-903">Added `marketplace` commands</span></span>
* <span data-ttu-id="ebcf3-904">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-904">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="ebcf3-905">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-905">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="ebcf3-906">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-906">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="ebcf3-907">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-907">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="ebcf3-908">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-908">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-909">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-909">Container</span></span>

* <span data-ttu-id="ebcf3-910">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-910">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="ebcf3-911">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-911">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-912">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-912">Extension</span></span>

* <span data-ttu-id="ebcf3-913">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-913">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-914">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-914">Interactive</span></span>

* <span data-ttu-id="ebcf3-915">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-915">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="ebcf3-916">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-916">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="ebcf3-917">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-917">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-918">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-918">Network</span></span>

* <span data-ttu-id="ebcf3-919">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-919">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="ebcf3-920">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-920">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="ebcf3-921">#4910</span><span class="sxs-lookup"><span data-stu-id="ebcf3-921">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="ebcf3-922">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-922">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="ebcf3-923">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-923">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="ebcf3-924">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-924">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="ebcf3-925">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-925">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="ebcf3-926">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-926">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-927">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-927">Profile</span></span>

* <span data-ttu-id="ebcf3-928">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-928">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="ebcf3-929">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-929">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-930">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-930">RDBMS</span></span>

* <span data-ttu-id="ebcf3-931">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-931">Added `georestore` command</span></span>
* <span data-ttu-id="ebcf3-932">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-932">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-933">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-933">Resource</span></span>

* <span data-ttu-id="ebcf3-934">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-934">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="ebcf3-935">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-935">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-936">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-936">SQL</span></span>

* <span data-ttu-id="ebcf3-937">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-937">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-938">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-938">Storage</span></span>

* <span data-ttu-id="ebcf3-939">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-939">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-940">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-940">VM</span></span>

* <span data-ttu-id="ebcf3-941">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-941">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="ebcf3-942">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-942">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="ebcf3-944">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-944">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="ebcf3-945">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-945">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="ebcf3-946">#5718</span><span class="sxs-lookup"><span data-stu-id="ebcf3-946">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="ebcf3-947">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-947">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="ebcf3-948">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-948">March 27, 2018</span></span>

<span data-ttu-id="ebcf3-949">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="ebcf3-949">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-950">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-950">Core</span></span>

* <span data-ttu-id="ebcf3-951">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-951">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-952">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-952">ACS</span></span>

* <span data-ttu-id="ebcf3-953">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-953">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-954">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-954">Appservice</span></span>

* <span data-ttu-id="ebcf3-955">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-955">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="ebcf3-956">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-956">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="ebcf3-957">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-957">Backup</span></span>

* <span data-ttu-id="ebcf3-958">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-958">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="ebcf3-959">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-959">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="ebcf3-960">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-960">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="ebcf3-961">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-961">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-962">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-962">Container</span></span>

* <span data-ttu-id="ebcf3-963">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-963">Added `container exec` command.</span></span> <span data-ttu-id="ebcf3-964">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-964">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="ebcf3-965">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-965">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-966">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-966">Extension</span></span>

* <span data-ttu-id="ebcf3-967">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-967">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="ebcf3-968">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-968">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="ebcf3-969">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-969">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-970">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-970">Interactive</span></span>

* <span data-ttu-id="ebcf3-971">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-971">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="ebcf3-972">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-972">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="ebcf3-973">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-973">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="ebcf3-974">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-974">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="ebcf3-975">ラボ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-975">Lab</span></span>

* <span data-ttu-id="ebcf3-976">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-976">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-977">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-977">Monitor</span></span>

* <span data-ttu-id="ebcf3-978">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-978">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="ebcf3-979">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました: `metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-979">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="ebcf3-980">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-980">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-981">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-981">Network</span></span>

* <span data-ttu-id="ebcf3-982">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-982">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-983">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-983">Profile</span></span>

* <span data-ttu-id="ebcf3-984">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-984">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-985">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-985">RDBMS</span></span>

* <span data-ttu-id="ebcf3-986">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-986">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-987">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-987">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="ebcf3-989">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-989">Role</span></span>

* <span data-ttu-id="ebcf3-990">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-990">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="ebcf3-991">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-991">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="ebcf3-992">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-992">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="ebcf3-993">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-993">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="ebcf3-994">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-994">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-995">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-995">Storage</span></span>

* <span data-ttu-id="ebcf3-996">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-996">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="ebcf3-997">[#4049](https://github.com/Azure/azure-cli/issues/4049) (追加 BLOB のアップロードで条件のパラメーターが無視される問題) を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-997">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-998">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-998">VM</span></span>

* <span data-ttu-id="ebcf3-999">インスタンス数が 100 を超えるセットに対する今後の重大な変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-999">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="ebcf3-1000">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1000">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="ebcf3-1001">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1001">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="ebcf3-1002">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1002">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="ebcf3-1003">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1003">March 13, 2018</span></span>

<span data-ttu-id="ebcf3-1004">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1004">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-1005">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1005">ACR</span></span>

* <span data-ttu-id="ebcf3-1006">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1006">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="ebcf3-1007">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1007">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="ebcf3-1008">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1008">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1009">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1009">ACS</span></span>

* <span data-ttu-id="ebcf3-1010">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1010">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="ebcf3-1011">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1011">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="ebcf3-1012">Advisor</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1012">Advisor</span></span>

* <span data-ttu-id="ebcf3-1013">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1013">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="ebcf3-1014">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1014">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="ebcf3-1015">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1015">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="ebcf3-1016">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1016">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="ebcf3-1017">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1017">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1018">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1018">Appservice</span></span>

* <span data-ttu-id="ebcf3-1019">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1019">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="ebcf3-1020">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1020">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="ebcf3-1021">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1021">Eventhubs</span></span>

* <span data-ttu-id="ebcf3-1022">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1022">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-1023">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1023">Extension</span></span>

* <span data-ttu-id="ebcf3-1024">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1024">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-1025">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1025">Interactive</span></span>

* <span data-ttu-id="ebcf3-1026">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました: 異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1026">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="ebcf3-1027">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました: スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1027">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="ebcf3-1028">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました: コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1028">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="ebcf3-1029">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1029">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1030">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1030">Monitor</span></span>

* <span data-ttu-id="ebcf3-1031">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1031">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="ebcf3-1032">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1032">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="ebcf3-1033">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1033">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="ebcf3-1034">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1034">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1035">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1035">Network</span></span>

* <span data-ttu-id="ebcf3-1036">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1036">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="ebcf3-1037">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1037">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="ebcf3-1038">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1038">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="ebcf3-1039">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1039">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1040">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1040">Profile</span></span>

* <span data-ttu-id="ebcf3-1041">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1041">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="ebcf3-1042">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1042">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-1043">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1043">RDBMS</span></span>

* <span data-ttu-id="ebcf3-1044">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1044">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="ebcf3-1045">Service Bus</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1045">Service Bus</span></span>

* <span data-ttu-id="ebcf3-1046">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1046">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1047">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1047">Storage</span></span>

* <span data-ttu-id="ebcf3-1048">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1048">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="ebcf3-1049">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました: Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1049">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1050">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1050">VM</span></span>

* <span data-ttu-id="ebcf3-1051">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1051">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="ebcf3-1052">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1052">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="ebcf3-1053">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1053">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="ebcf3-1054">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1054">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="ebcf3-1055">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1055">February 27, 2018</span></span>

<span data-ttu-id="ebcf3-1056">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1056">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1057">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1057">Core</span></span>

* <span data-ttu-id="ebcf3-1058">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正: Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1058">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="ebcf3-1059">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1059">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="ebcf3-1060">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1060">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1061">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1061">ACS</span></span>

* <span data-ttu-id="ebcf3-1062">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1062">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="ebcf3-1063">修正された問題: ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1063">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="ebcf3-1064">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1064">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="ebcf3-1065">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1065">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1066">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1066">Appservice</span></span>

* <span data-ttu-id="ebcf3-1067">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1067">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="ebcf3-1068">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1068">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="ebcf3-1069">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1069">Cognitive Services</span></span>

* <span data-ttu-id="ebcf3-1070">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1070">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="ebcf3-1071">消費</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1071">Consumption</span></span>

* <span data-ttu-id="ebcf3-1072">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1072">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="ebcf3-1073">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1073">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1074">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1074">Container</span></span>

* <span data-ttu-id="ebcf3-1075">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1075">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1076">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1076">Network</span></span>

* <span data-ttu-id="ebcf3-1077">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正: `network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1077">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1078">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1078">Resource</span></span>

* <span data-ttu-id="ebcf3-1079">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1079">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1080">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1080">Role</span></span>

* <span data-ttu-id="ebcf3-1081">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1081">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1082">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1082">SQL</span></span>

* <span data-ttu-id="ebcf3-1083">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1083">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1084">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1084">Storage</span></span>

* <span data-ttu-id="ebcf3-1085">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1085">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1086">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1086">VM</span></span>

* <span data-ttu-id="ebcf3-1087">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1087">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="ebcf3-1088">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1088">February 13, 2018</span></span>

<span data-ttu-id="ebcf3-1089">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1089">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1090">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1090">Core</span></span>

* <span data-ttu-id="ebcf3-1091">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1091">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1092">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1092">ACS</span></span>

* <span data-ttu-id="ebcf3-1093">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1093">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="ebcf3-1094">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1094">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="ebcf3-1095">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1095">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="ebcf3-1096">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1096">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="ebcf3-1097">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1097">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="ebcf3-1098">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1098">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="ebcf3-1099">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1099">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="ebcf3-1100">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1100">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1101">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1101">Appservice</span></span>

* <span data-ttu-id="ebcf3-1102">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1102">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="ebcf3-1103">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1103">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="ebcf3-1104">CDN</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1104">CDN</span></span>

* <span data-ttu-id="ebcf3-1105">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1105">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1106">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1106">Container</span></span>

* <span data-ttu-id="ebcf3-1107">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1107">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="ebcf3-1108">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1108">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ebcf3-1109">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1109">CosmosDB</span></span>

* <span data-ttu-id="ebcf3-1110">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1110">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-1111">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1111">Extension</span></span>

* <span data-ttu-id="ebcf3-1112">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1112">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="ebcf3-1113">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1113">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="ebcf3-1114">フィードバック</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1114">Feedback</span></span>

* <span data-ttu-id="ebcf3-1115">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1115">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-1116">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1116">Interactive</span></span>

* <span data-ttu-id="ebcf3-1117">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1117">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="ebcf3-1118">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1118">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-1119">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1119">IoT</span></span>

* <span data-ttu-id="ebcf3-1120">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1120">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="ebcf3-1121">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1121">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="ebcf3-1122">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1122">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1123">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1123">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1124">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1124">Monitor</span></span>

* <span data-ttu-id="ebcf3-1125">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1125">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1126">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1126">Network</span></span>

* <span data-ttu-id="ebcf3-1127">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1127">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="ebcf3-1128">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1128">Profile</span></span>

* <span data-ttu-id="ebcf3-1129">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1129">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1130">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1130">Resource</span></span>

* <span data-ttu-id="ebcf3-1131">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1131">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1132">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1132">Role</span></span>

* <span data-ttu-id="ebcf3-1133">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1133">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1134">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1134">SQL</span></span>

* <span data-ttu-id="ebcf3-1135">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1135">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="ebcf3-1136">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1136">Added `sql db rename`</span></span>
* <span data-ttu-id="ebcf3-1137">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1137">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1138">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1138">Storage</span></span>

* <span data-ttu-id="ebcf3-1139">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1139">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1140">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1140">VM</span></span>

* <span data-ttu-id="ebcf3-1141">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1141">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="ebcf3-1142">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1142">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="ebcf3-1143">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1143">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="ebcf3-1144">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1144">January 31, 2018</span></span>

<span data-ttu-id="ebcf3-1145">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1145">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1146">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1146">Core</span></span>

* <span data-ttu-id="ebcf3-1147">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1147">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="ebcf3-1148">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1148">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="ebcf3-1149">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1149">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="ebcf3-1150">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1150">Use `--verbose` to see</span></span>
* <span data-ttu-id="ebcf3-1151">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1151">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1152">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1152">ACS</span></span>

* <span data-ttu-id="ebcf3-1153">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1153">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="ebcf3-1154">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1154">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1155">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1155">Appservice</span></span>

* <span data-ttu-id="ebcf3-1156">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1156">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="ebcf3-1157">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1157">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="ebcf3-1158">CDN</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1158">CDN</span></span>

* <span data-ttu-id="ebcf3-1159">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1159">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ebcf3-1160">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1160">CosmosDB</span></span>

* <span data-ttu-id="ebcf3-1161">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1161">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-1162">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1162">Interactive</span></span>

* <span data-ttu-id="ebcf3-1163">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1163">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1164">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1164">Network</span></span>

* <span data-ttu-id="ebcf3-1165">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1165">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="ebcf3-1166">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1166">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="ebcf3-1167">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1167">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="ebcf3-1168">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1168">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="ebcf3-1169">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1169">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="ebcf3-1170">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1170">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="ebcf3-1171">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1171">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="ebcf3-1172">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1172">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="ebcf3-1173">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1173">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="ebcf3-1174">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1174">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1175">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1175">Profile</span></span>

* <span data-ttu-id="ebcf3-1176">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1176">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1177">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1177">Resource</span></span>

* <span data-ttu-id="ebcf3-1178">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1178">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1179">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1179">Storage</span></span>

* <span data-ttu-id="ebcf3-1180">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1180">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="ebcf3-1181">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1181">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="ebcf3-1182">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1182">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="ebcf3-1183">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1183">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="ebcf3-1184">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1184">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1185">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1185">VM</span></span>

* <span data-ttu-id="ebcf3-1186">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1186">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="ebcf3-1187">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1187">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="ebcf3-1188">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1188">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="ebcf3-1189">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1189">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="ebcf3-1190">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1190">January 17, 2018</span></span>

<span data-ttu-id="ebcf3-1191">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1191">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-1192">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1192">ACR</span></span>

* <span data-ttu-id="ebcf3-1193">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1193">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="ebcf3-1194">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1194">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1195">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1195">ACS</span></span>

* <span data-ttu-id="ebcf3-1196">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1196">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="ebcf3-1197">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1197">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1198">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1198">Appservice</span></span>

* <span data-ttu-id="ebcf3-1199">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1199">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="ebcf3-1200">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1200">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="ebcf3-1201">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1201">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="ebcf3-1202">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1202">Backup</span></span>

* <span data-ttu-id="ebcf3-1203">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1203">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="ebcf3-1204">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1204">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="ebcf3-1205">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1205">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="ebcf3-1206">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1206">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="ebcf3-1207">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1207">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-1208">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1208">Batch</span></span>

* <span data-ttu-id="ebcf3-1209">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1209">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="ebcf3-1210">クラウド</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1210">Cloud</span></span>

* <span data-ttu-id="ebcf3-1211">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1211">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="ebcf3-1212">消費</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1212">Consumption</span></span>

* <span data-ttu-id="ebcf3-1213">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1213">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="ebcf3-1214">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1214">Event Grid</span></span>

* <span data-ttu-id="ebcf3-1215">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1215">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ebcf3-1216">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1216">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="ebcf3-1217">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1217">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="ebcf3-1218">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1218">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="ebcf3-1219">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1219">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="ebcf3-1220">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1220">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="ebcf3-1221">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1221">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="ebcf3-1222">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1222">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-1223">Interactive</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1223">Interactive</span></span>

* <span data-ttu-id="ebcf3-1224">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1224">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="ebcf3-1225">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1225">Fixed errors on startup</span></span>
* <span data-ttu-id="ebcf3-1226">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1226">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-1227">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1227">IoT</span></span>

* <span data-ttu-id="ebcf3-1228">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1228">Added support for device provisioning service</span></span>
* <span data-ttu-id="ebcf3-1229">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1229">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="ebcf3-1230">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1230">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1231">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1231">Monitor</span></span>

* <span data-ttu-id="ebcf3-1232">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1232">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="ebcf3-1233">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1233">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="ebcf3-1234">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1234">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1235">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1235">Network</span></span>

* <span data-ttu-id="ebcf3-1236">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1236">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="ebcf3-1237">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1237">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1238">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1238">Profile</span></span>

* <span data-ttu-id="ebcf3-1239">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1239">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1240">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1240">Role</span></span>

* <span data-ttu-id="ebcf3-1241">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1241">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ebcf3-1242">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1242">Service Fabric</span></span>

* <span data-ttu-id="ebcf3-1243">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1243">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="ebcf3-1244">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1244">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1245">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1245">VM</span></span>

* <span data-ttu-id="ebcf3-1246">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1246">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="ebcf3-1247">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1247">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="ebcf3-1248">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1248">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="ebcf3-1249">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1249">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="ebcf3-1250">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1250">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="ebcf3-1251">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1251">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="ebcf3-1252">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1252">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="ebcf3-1253">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1253">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="ebcf3-1254">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1254">December 19, 2017</span></span>

<span data-ttu-id="ebcf3-1255">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1255">Version 2.0.23</span></span>

* <span data-ttu-id="ebcf3-1256">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1256">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1257">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1257">Container</span></span>

* <span data-ttu-id="ebcf3-1258">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1258">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1259">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1259">Network</span></span>

* <span data-ttu-id="ebcf3-1260">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1260">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1261">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1261">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1262">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1262">Storage</span></span>

* <span data-ttu-id="ebcf3-1263">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1263">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1264">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1264">VM</span></span>

* <span data-ttu-id="ebcf3-1265">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1265">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="ebcf3-1266">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1266">December 5, 2017</span></span>

<span data-ttu-id="ebcf3-1267">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1267">Version 2.0.22</span></span>

* <span data-ttu-id="ebcf3-1268">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1268">Removed `az component` commands.</span></span> <span data-ttu-id="ebcf3-1269">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1269">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1270">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1270">Core</span></span>
* <span data-ttu-id="ebcf3-1271">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1271">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="ebcf3-1272">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1272">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1273">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1273">ACS</span></span>

* <span data-ttu-id="ebcf3-1274">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1274">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="ebcf3-1275">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1275">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="ebcf3-1276">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1276">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="ebcf3-1277">Advisor</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1277">Advisor</span></span>

* <span data-ttu-id="ebcf3-1278">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1278">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1279">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1279">Appservice</span></span>

* <span data-ttu-id="ebcf3-1280">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1280">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="ebcf3-1281">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1281">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="ebcf3-1282">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1282">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="ebcf3-1283">消費</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1283">Consumption</span></span>

* <span data-ttu-id="ebcf3-1284">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1284">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1285">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1285">Container</span></span>

* <span data-ttu-id="ebcf3-1286">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1286">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1287">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1287">Monitor</span></span>

* <span data-ttu-id="ebcf3-1288">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1288">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1289">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1289">Resource</span></span>

* <span data-ttu-id="ebcf3-1290">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1290">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1291">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1291">Role</span></span>

* <span data-ttu-id="ebcf3-1292">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1292">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="ebcf3-1293">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1293">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="ebcf3-1294">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1294">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1295">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1295">SQL</span></span>

* <span data-ttu-id="ebcf3-1296">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1296">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="ebcf3-1297">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1297">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1298">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1298">VM</span></span>

* <span data-ttu-id="ebcf3-1299">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1299">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="ebcf3-1300">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1300">November 14, 2017</span></span>

<span data-ttu-id="ebcf3-1301">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1301">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-1302">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1302">ACR</span></span>

* <span data-ttu-id="ebcf3-1303">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1303">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="ebcf3-1304">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1304">ACS</span></span>

* <span data-ttu-id="ebcf3-1305">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1305">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="ebcf3-1306">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1306">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="ebcf3-1307">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1307">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="ebcf3-1308">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1308">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="ebcf3-1309">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1309">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1310">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1310">Appservice</span></span>

* <span data-ttu-id="ebcf3-1311">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1311">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="ebcf3-1312">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1312">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="ebcf3-1313">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1313">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="ebcf3-1314">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1314">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="ebcf3-1315">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1315">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="ebcf3-1316">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1316">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-1317">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1317">Batch</span></span>

* <span data-ttu-id="ebcf3-1318">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1318">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="ebcf3-1319">Batchai</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1319">Batchai</span></span>

* <span data-ttu-id="ebcf3-1320">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1320">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="ebcf3-1321">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1321">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="ebcf3-1322">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1322">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="ebcf3-1323">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1323">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="ebcf3-1324">クラウド</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1324">Cloud</span></span>

* <span data-ttu-id="ebcf3-1325">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1325">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1326">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1326">Container</span></span>

* <span data-ttu-id="ebcf3-1327">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1327">Added support to open multiple ports</span></span>
* <span data-ttu-id="ebcf3-1328">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1328">Added container group restart policy</span></span>
* <span data-ttu-id="ebcf3-1329">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1329">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="ebcf3-1330">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1330">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ebcf3-1331">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1331">Data Lake Analytics</span></span>

* <span data-ttu-id="ebcf3-1332">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1332">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ebcf3-1333">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1333">Data Lake Store</span></span>

* <span data-ttu-id="ebcf3-1334">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1334">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-1335">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1335">Extension</span></span>

* <span data-ttu-id="ebcf3-1336">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1336">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="ebcf3-1337">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1337">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-1338">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1338">IoT</span></span>

* <span data-ttu-id="ebcf3-1339">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1339">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1340">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1340">Monitor</span></span>

* <span data-ttu-id="ebcf3-1341">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1341">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1342">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1342">Network</span></span>

* <span data-ttu-id="ebcf3-1343">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1343">Added support for CAA DNS records</span></span>
* <span data-ttu-id="ebcf3-1344">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1344">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="ebcf3-1345">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1345">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="ebcf3-1346">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1346">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="ebcf3-1347">Reservations</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1347">Reservations</span></span>

* <span data-ttu-id="ebcf3-1348">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1348">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1349">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1349">Resource</span></span>

* <span data-ttu-id="ebcf3-1350">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1350">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1351">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1351">SQL</span></span>

* <span data-ttu-id="ebcf3-1352">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1352">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1353">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1353">Storage</span></span>

* <span data-ttu-id="ebcf3-1354">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1354">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="ebcf3-1355">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1355">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="ebcf3-1356">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1356">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="ebcf3-1357">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1357">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="ebcf3-1358">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1358">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="ebcf3-1359">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1359">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="ebcf3-1360">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1360">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1361">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1361">VM</span></span>

* <span data-ttu-id="ebcf3-1362">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1362">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="ebcf3-1363">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1363">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="ebcf3-1364">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1364">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="ebcf3-1365">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1365">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="ebcf3-1366">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1366">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="ebcf3-1367">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1367">October 24, 2017</span></span>

<span data-ttu-id="ebcf3-1368">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1368">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1369">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1369">Core</span></span>

* <span data-ttu-id="ebcf3-1370">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1370">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-1371">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1371">ACR</span></span>

* <span data-ttu-id="ebcf3-1372">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1372">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="ebcf3-1373">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1373">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="ebcf3-1374">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1374">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1375">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1375">ACS</span></span>

* <span data-ttu-id="ebcf3-1376">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1376">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="ebcf3-1377">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1377">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1378">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1378">Appservice</span></span>

* <span data-ttu-id="ebcf3-1379">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1379">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="ebcf3-1380">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1380">Component</span></span>

* <span data-ttu-id="ebcf3-1381">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1381">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1382">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1382">Monitor</span></span>

* <span data-ttu-id="ebcf3-1383">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1383">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1384">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1384">Resource</span></span>

* <span data-ttu-id="ebcf3-1385">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1385">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="ebcf3-1386">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1386">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1387">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1387">VM</span></span>

* <span data-ttu-id="ebcf3-1388">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1388">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="ebcf3-1389">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1389">October 9, 2017</span></span>

<span data-ttu-id="ebcf3-1390">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1390">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1391">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1391">Core</span></span>

* <span data-ttu-id="ebcf3-1392">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1392">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1393">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1393">Appservice</span></span>

* <span data-ttu-id="ebcf3-1394">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1394">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-1395">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1395">Batch</span></span>

* <span data-ttu-id="ebcf3-1396">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1396">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="ebcf3-1397">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1397">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="ebcf3-1398">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1398">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="ebcf3-1399">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1399">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="ebcf3-1400">Batchai</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1400">Batchai</span></span>

* <span data-ttu-id="ebcf3-1401">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1401">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-1402">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1402">Keyvault</span></span>

* <span data-ttu-id="ebcf3-1403">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1403">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="ebcf3-1404">(#4448)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1404">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="ebcf3-1405">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1405">Network</span></span>

* <span data-ttu-id="ebcf3-1406">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1406">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="ebcf3-1407">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1407">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1408">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1408">Resource</span></span>

* <span data-ttu-id="ebcf3-1409">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1409">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="ebcf3-1410">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1410">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="ebcf3-1411">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1411">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="ebcf3-1412">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1412">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1413">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1413">Sql</span></span>

* <span data-ttu-id="ebcf3-1414">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1414">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="ebcf3-1415">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1415">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="ebcf3-1416">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1416">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1417">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1417">Storage</span></span>

* <span data-ttu-id="ebcf3-1418">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1418">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1419">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1419">Vm</span></span>

* <span data-ttu-id="ebcf3-1420">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1420">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="ebcf3-1421">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1421">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="ebcf3-1422">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1422">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="ebcf3-1423">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1423">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="ebcf3-1424">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1424">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="ebcf3-1425">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1425">September 22, 2017</span></span>

<span data-ttu-id="ebcf3-1426">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1426">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1427">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1427">Resource</span></span>

* <span data-ttu-id="ebcf3-1428">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1428">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="ebcf3-1429">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1429">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="ebcf3-1430">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1430">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="ebcf3-1431">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1431">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1432">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1432">Network</span></span>

* <span data-ttu-id="ebcf3-1433">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1433">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="ebcf3-1434">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1434">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="ebcf3-1435">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1435">Added `asg` application security group commands</span></span>
* <span data-ttu-id="ebcf3-1436">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1436">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="ebcf3-1437">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1437">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1438">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1438">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1439">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1439">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1440">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1440">Storage</span></span>

* <span data-ttu-id="ebcf3-1441">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1441">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="ebcf3-1442">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1442">Eventgrid</span></span>

* <span data-ttu-id="ebcf3-1443">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1443">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1444">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1444">SQL</span></span>

* <span data-ttu-id="ebcf3-1445">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1445">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="ebcf3-1446">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1446">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="ebcf3-1447">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1447">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-1448">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1448">Keyvault</span></span>

* <span data-ttu-id="ebcf3-1449">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1449">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1450">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1450">VM</span></span>

* <span data-ttu-id="ebcf3-1451">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1451">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="ebcf3-1452">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1452">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="ebcf3-1453">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1453">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="ebcf3-1454">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1454">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="ebcf3-1455">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1455">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="ebcf3-1456">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1456">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1457">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1457">ACS</span></span>

* <span data-ttu-id="ebcf3-1458">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1458">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1459">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1459">Appservice</span></span>

* <span data-ttu-id="ebcf3-1460">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1460">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="ebcf3-1461">バックアップ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1461">Backup</span></span>

* <span data-ttu-id="ebcf3-1462">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1462">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="ebcf3-1463">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1463">September 11, 2017</span></span>

<span data-ttu-id="ebcf3-1464">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1464">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="ebcf3-1465">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1465">Core</span></span>

* <span data-ttu-id="ebcf3-1466">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1466">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="ebcf3-1467">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1467">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1468">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1468">Acs</span></span>

* <span data-ttu-id="ebcf3-1469">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1469">Added `acs list-locations` command</span></span>
* <span data-ttu-id="ebcf3-1470">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1470">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1471">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1471">Appservice</span></span>

* <span data-ttu-id="ebcf3-1472">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1472">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="ebcf3-1473">CDN</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1473">CDN</span></span>

* <span data-ttu-id="ebcf3-1474">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1474">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="ebcf3-1475">拡張機能</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1475">Extension</span></span>

* <span data-ttu-id="ebcf3-1476">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1476">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-1477">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1477">Keyvault</span></span>

* <span data-ttu-id="ebcf3-1478">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1478">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1479">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1479">Network</span></span>

* <span data-ttu-id="ebcf3-1480">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1480">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ebcf3-1481">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1481">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="ebcf3-1482">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1482">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="ebcf3-1483">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1483">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ebcf3-1484">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1484">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1485">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1485">Resource</span></span>

* <span data-ttu-id="ebcf3-1486">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1486">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="ebcf3-1487">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1487">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="ebcf3-1488">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1488">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="ebcf3-1489">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1489">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1490">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1490">SQL</span></span>

* <span data-ttu-id="ebcf3-1491">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1491">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1492">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1492">VM</span></span>

* <span data-ttu-id="ebcf3-1493">修正済み: `--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1493">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="ebcf3-1494">修正済み: ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1494">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="ebcf3-1495">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1495">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="ebcf3-1496">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1496">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="ebcf3-1497">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1497">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="ebcf3-1498">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1498">August 31, 2017</span></span>

<span data-ttu-id="ebcf3-1499">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1499">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-1500">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1500">Keyvault</span></span>

* <span data-ttu-id="ebcf3-1501">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1501">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="ebcf3-1502">SF</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1502">Sf</span></span>

* <span data-ttu-id="ebcf3-1503">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1503">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1504">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1504">Storage</span></span>

* <span data-ttu-id="ebcf3-1505">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1505">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="ebcf3-1506">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1506">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="ebcf3-1507">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1507">August 28, 2017</span></span>

<span data-ttu-id="ebcf3-1508">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1508">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="ebcf3-1509">CLI</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1509">CLI</span></span>

* <span data-ttu-id="ebcf3-1510">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1510">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1511">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1511">ACS</span></span>

* <span data-ttu-id="ebcf3-1512">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1512">Corrected preview regions</span></span>
* <span data-ttu-id="ebcf3-1513">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1513">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="ebcf3-1514">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1514">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1515">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1515">Appservice</span></span>

* <span data-ttu-id="ebcf3-1516">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1516">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="ebcf3-1517">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1517">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="ebcf3-1518">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1518">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="ebcf3-1519">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1519">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="ebcf3-1520">修正済み: スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1520">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-1521">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1521">IoT</span></span>

* <span data-ttu-id="ebcf3-1522">修正済み #3934: ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1522">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1523">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1523">Network</span></span>

* <span data-ttu-id="ebcf3-1524">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1524">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="ebcf3-1525">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1525">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1526">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1526">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="ebcf3-1527">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1527">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="ebcf3-1528">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1528">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1529">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1529">Profile</span></span>

* <span data-ttu-id="ebcf3-1530">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1530">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ebcf3-1531">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1531">Service Fabric</span></span>

* <span data-ttu-id="ebcf3-1532">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1532">Preview release</span></span>
* <span data-ttu-id="ebcf3-1533">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1533">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="ebcf3-1534">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1534">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="ebcf3-1535">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1535">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1536">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1536">Storage</span></span>

* <span data-ttu-id="ebcf3-1537">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1537">Enabled setting blob tier</span></span>
* <span data-ttu-id="ebcf3-1538">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1538">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="ebcf3-1539">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1539">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="ebcf3-1540">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1540">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="ebcf3-1541">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1541">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="ebcf3-1542">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1542">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1543">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1543">VM</span></span>

* <span data-ttu-id="ebcf3-1544">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1544">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="ebcf3-1545">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1545">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="ebcf3-1546">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1546">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="ebcf3-1547">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1547">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="ebcf3-1548">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1548">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="ebcf3-1549">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1549">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="ebcf3-1550">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1550">August 15, 2017</span></span>

<span data-ttu-id="ebcf3-1551">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1551">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1552">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1552">ACS</span></span>

* <span data-ttu-id="ebcf3-1553">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1553">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1554">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1554">Appservice</span></span>

* <span data-ttu-id="ebcf3-1555">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1555">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="ebcf3-1556">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1556">Event Grid</span></span>

* <span data-ttu-id="ebcf3-1557">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1557">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="ebcf3-1558">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1558">August 11, 2017</span></span>

<span data-ttu-id="ebcf3-1559">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1559">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1560">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1560">ACS</span></span>

* <span data-ttu-id="ebcf3-1561">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1561">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-1562">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1562">Batch</span></span>

* <span data-ttu-id="ebcf3-1563">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1563">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="ebcf3-1564">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1564">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="ebcf3-1565">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1565">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="ebcf3-1566">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1566">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="ebcf3-1567">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1567">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="ebcf3-1568">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1568">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="ebcf3-1569">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1569">Component</span></span>

* <span data-ttu-id="ebcf3-1570">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1570">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="ebcf3-1571">コンテナー</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1571">Container</span></span>

* <span data-ttu-id="ebcf3-1572">`create`: 環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1572">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="ebcf3-1573">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1573">Data Lake Store</span></span>

* <span data-ttu-id="ebcf3-1574">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1574">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="ebcf3-1575">Event Grid</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1575">Event Grid</span></span>

* <span data-ttu-id="ebcf3-1576">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1576">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1577">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1577">Network</span></span>

* <span data-ttu-id="ebcf3-1578">`lb`: 特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1578">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="ebcf3-1579">`application-gateway {subresource} delete`: `--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1579">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="ebcf3-1580">`application-gateway http-settings update`: `--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1580">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="ebcf3-1581">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1581">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1582">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1582">Profile</span></span>

* <span data-ttu-id="ebcf3-1583">`account list`: サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1583">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1584">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1584">Storage</span></span>

* <span data-ttu-id="ebcf3-1585">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1585">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1586">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1586">VM</span></span>

* <span data-ttu-id="ebcf3-1587">`availability-set`: 変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1587">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="ebcf3-1588">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1588">Exposed `list-skus` command</span></span>
* <span data-ttu-id="ebcf3-1589">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1589">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="ebcf3-1590">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1590">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="ebcf3-1591">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1591">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="ebcf3-1592">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1592">July 28, 2017</span></span>

<span data-ttu-id="ebcf3-1593">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1593">Version 2.0.12</span></span>

* <span data-ttu-id="ebcf3-1594">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1594">Added container commands</span></span>
* <span data-ttu-id="ebcf3-1595">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1595">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="ebcf3-1596">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1596">Core</span></span>

* <span data-ttu-id="ebcf3-1597">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1597">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="ebcf3-1598">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1598">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="ebcf3-1599">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1599">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="ebcf3-1600">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1600">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="ebcf3-1601">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1601">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="ebcf3-1602">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1602">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="ebcf3-1603">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1603">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ebcf3-1604">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1604">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="ebcf3-1605">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1605">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="ebcf3-1606">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1606">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="ebcf3-1607">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1607">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="ebcf3-1608">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1608">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="ebcf3-1609">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1609">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="ebcf3-1610">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1610">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="ebcf3-1611">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1611">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="ebcf3-1612">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1612">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="ebcf3-1613">ACR</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1613">ACR</span></span>

* <span data-ttu-id="ebcf3-1614">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1614">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="ebcf3-1615">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1615">Support SKU update for managed registries</span></span>
* <span data-ttu-id="ebcf3-1616">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1616">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="ebcf3-1617">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1617">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="ebcf3-1618">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1618">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="ebcf3-1619">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1619">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1620">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1620">ACS</span></span>

* <span data-ttu-id="ebcf3-1621">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1621">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1622">Appservice</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1622">Appservice</span></span>

* <span data-ttu-id="ebcf3-1623">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1623">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="ebcf3-1624">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1624">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="ebcf3-1625">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1625">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="ebcf3-1626">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1626">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="ebcf3-1627">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1627">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="ebcf3-1628">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1628">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="ebcf3-1629">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1629">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="ebcf3-1630">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1630">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="ebcf3-1631">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1631">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="ebcf3-1632">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1632">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="ebcf3-1633">Batch</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1633">Batch</span></span>

* <span data-ttu-id="ebcf3-1634">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1634">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="ebcf3-1635">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1635">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="ebcf3-1636">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1636">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="ebcf3-1637">CDN</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1637">CDN</span></span>

* <span data-ttu-id="ebcf3-1638">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1638">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="ebcf3-1639">クラウド</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1639">Cloud</span></span>

* <span data-ttu-id="ebcf3-1640">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1640">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="ebcf3-1641">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1641">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="ebcf3-1642">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1642">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="ebcf3-1643">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1643">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="ebcf3-1644">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1644">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ebcf3-1645">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1645">CosmosDB</span></span>

* <span data-ttu-id="ebcf3-1646">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1646">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="ebcf3-1647">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1647">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ebcf3-1648">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1648">Data Lake Analytics</span></span>

* <span data-ttu-id="ebcf3-1649">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1649">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="ebcf3-1650">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1650">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="ebcf3-1651">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1651">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ebcf3-1652">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1652">Data Lake Store</span></span>

* <span data-ttu-id="ebcf3-1653">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1653">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="ebcf3-1654">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1654">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="ebcf3-1655">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1655">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="ebcf3-1656">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1656">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="ebcf3-1657">対話</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1657">Interactive</span></span>

* <span data-ttu-id="ebcf3-1658">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1658">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="ebcf3-1659">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1659">Increased test coverage</span></span>
* <span data-ttu-id="ebcf3-1660">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1660">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="ebcf3-1661">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1661">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="ebcf3-1662">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1662">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="ebcf3-1663">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1663">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="ebcf3-1664">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1664">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="ebcf3-1665">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1665">Added `--progress` flag</span></span>
* <span data-ttu-id="ebcf3-1666">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1666">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="ebcf3-1667">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1667">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="ebcf3-1668">IoT</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1668">IoT</span></span>

* <span data-ttu-id="ebcf3-1669">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1669">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="ebcf3-1670">(#3934)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1670">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="ebcf3-1671">Key Vault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1671">Key vault</span></span>

* <span data-ttu-id="ebcf3-1672">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1672">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="ebcf3-1673">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1673">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="ebcf3-1674">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1674">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ebcf3-1675">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1675">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="ebcf3-1676">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1676">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="ebcf3-1677">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1677">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="ebcf3-1678">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1678">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="ebcf3-1679">(#3307)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1679">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="ebcf3-1680">ラボ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1680">Lab</span></span>

* <span data-ttu-id="ebcf3-1681">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1681">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="ebcf3-1682">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1682">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1683">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1683">Monitor</span></span>

* <span data-ttu-id="ebcf3-1684">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1684">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="ebcf3-1685">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1685">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="ebcf3-1686">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1686">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="ebcf3-1687">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1687">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="ebcf3-1688">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1688">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="ebcf3-1689">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1689">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="ebcf3-1690">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1690">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="ebcf3-1691">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1691">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="ebcf3-1692">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1692">`location` no longer required</span></span>
  * <span data-ttu-id="ebcf3-1693">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1693">Add name and ID support for target</span></span>
  * <span data-ttu-id="ebcf3-1694">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1694">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="ebcf3-1695">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1695">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="ebcf3-1696">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1696">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="ebcf3-1697">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1697">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="ebcf3-1698">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1698">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="ebcf3-1699">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1699">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1700">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1700">Network</span></span>

* <span data-ttu-id="ebcf3-1701">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1701">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="ebcf3-1702">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1702">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="ebcf3-1703">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1703">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="ebcf3-1704">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1704">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="ebcf3-1705">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1705">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="ebcf3-1706">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1706">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="ebcf3-1707">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1707">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="ebcf3-1708">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1708">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="ebcf3-1709">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1709">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="ebcf3-1710">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1710">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="ebcf3-1711">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1711">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="ebcf3-1712">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1712">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="ebcf3-1713">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1713">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="ebcf3-1714">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1714">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="ebcf3-1715">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1715">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="ebcf3-1716">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1716">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="ebcf3-1717">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました: --dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1717">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="ebcf3-1718">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1718">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="ebcf3-1719">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1719">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="ebcf3-1720">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1720">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="ebcf3-1721">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1721">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="ebcf3-1722">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1722">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="ebcf3-1723">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1723">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="ebcf3-1724">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1724">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="ebcf3-1725">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1725">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="ebcf3-1726">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1726">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="ebcf3-1727">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1727">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1728">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1728">Profile</span></span>

* <span data-ttu-id="ebcf3-1729">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1729">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="ebcf3-1730">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1730">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="ebcf3-1731">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1731">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="ebcf3-1732">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1732">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="ebcf3-1733">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1733">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="ebcf3-1734">RDBMS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1734">RDBMS</span></span>

* <span data-ttu-id="ebcf3-1735">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1735">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="ebcf3-1736">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1736">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="ebcf3-1737">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1737">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="ebcf3-1738">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1738">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1739">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1739">Resource</span></span>

* <span data-ttu-id="ebcf3-1740">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1740">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="ebcf3-1741">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1741">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="ebcf3-1742">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1742">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="ebcf3-1743">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1743">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="ebcf3-1744">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1744">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="ebcf3-1745">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1745">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="ebcf3-1746">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1746">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="ebcf3-1747">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1747">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1748">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1748">Role</span></span>

* <span data-ttu-id="ebcf3-1749">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1749">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="ebcf3-1750">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1750">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="ebcf3-1751">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1751">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="ebcf3-1752">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1752">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="ebcf3-1753">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1753">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="ebcf3-1754">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1754">Service Fabric</span></span>
* <span data-ttu-id="ebcf3-1755">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1755">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="ebcf3-1756">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1756">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="ebcf3-1757">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1757">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1758">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1758">SQL</span></span>

* <span data-ttu-id="ebcf3-1759">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1759">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="ebcf3-1760">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1760">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="ebcf3-1761">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1761">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1762">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1762">Storage</span></span>

* <span data-ttu-id="ebcf3-1763">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1763">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="ebcf3-1764">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1764">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="ebcf3-1765">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1765">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="ebcf3-1766">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1766">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="ebcf3-1767">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1767">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="ebcf3-1768">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1768">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1769">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1769">VM</span></span>

* <span data-ttu-id="ebcf3-1770">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1770">Support configuring nsg</span></span>
* <span data-ttu-id="ebcf3-1771">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1771">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="ebcf3-1772">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1772">Support managed service identities</span></span>
* <span data-ttu-id="ebcf3-1773">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1773">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="ebcf3-1774">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1774">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="ebcf3-1775">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1775">May 10, 2017</span></span>

<span data-ttu-id="ebcf3-1776">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1776">Version 2.0.6</span></span>

* <span data-ttu-id="ebcf3-1777">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1777">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="ebcf3-1778">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1778">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="ebcf3-1779">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1779">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="ebcf3-1780">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1780">Include Cognitive Services module</span></span>
* <span data-ttu-id="ebcf3-1781">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1781">Include Service Fabric module</span></span>
* <span data-ttu-id="ebcf3-1782">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1782">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="ebcf3-1783">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1783">Add support for CDN commands</span></span>
* <span data-ttu-id="ebcf3-1784">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1784">Remove Container module</span></span>
* <span data-ttu-id="ebcf3-1785">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1785">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="ebcf3-1786">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1786">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="ebcf3-1787">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1787">Core</span></span>

* <span data-ttu-id="ebcf3-1788">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1788">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="ebcf3-1789">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1789">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="ebcf3-1790">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1790">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="ebcf3-1791">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1791">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="ebcf3-1792">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1792">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="ebcf3-1793">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1793">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="ebcf3-1794">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1794">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="ebcf3-1795">コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1795">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="ebcf3-1796">コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1796">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="ebcf3-1797">コア: パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1797">core: Improved performance</span></span>
* <span data-ttu-id="ebcf3-1798">コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1798">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="ebcf3-1799">コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1799">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1800">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1800">ACS</span></span>

* <span data-ttu-id="ebcf3-1801">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1801">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="ebcf3-1802">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1802">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="ebcf3-1803">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1803">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="ebcf3-1804">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1804">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1805">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1805">AppService</span></span>

* <span data-ttu-id="ebcf3-1806">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1806">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="ebcf3-1807">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1807">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="ebcf3-1808">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1808">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="ebcf3-1809">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1809">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="ebcf3-1810">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1810">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="ebcf3-1811">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1811">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="ebcf3-1812">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1812">support slot swap with preview</span></span>
* <span data-ttu-id="ebcf3-1813">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1813">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="ebcf3-1814">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1814">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="ebcf3-1815">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1815">CosmosDB</span></span>

* <span data-ttu-id="ebcf3-1816">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1816">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="ebcf3-1817">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1817">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="ebcf3-1818">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1818">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="ebcf3-1819">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1819">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="ebcf3-1820">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1820">Data Lake Analytics</span></span>

* <span data-ttu-id="ebcf3-1821">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1821">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="ebcf3-1822">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1822">Add support for new catalog item type: package.</span></span> <span data-ttu-id="ebcf3-1823">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1823">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="ebcf3-1824">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1824">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="ebcf3-1825">テーブル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1825">Table</span></span>
  * <span data-ttu-id="ebcf3-1826">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1826">Table valued function</span></span>
  * <span data-ttu-id="ebcf3-1827">表示</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1827">View</span></span>
  * <span data-ttu-id="ebcf3-1828">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1828">Table Statistics.</span></span> <span data-ttu-id="ebcf3-1829">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1829">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="ebcf3-1830">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1830">Data Lake Store</span></span>

* <span data-ttu-id="ebcf3-1831">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1831">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="ebcf3-1832">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1832">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="ebcf3-1833">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1833">missed help for access show.</span></span> <span data-ttu-id="ebcf3-1834">追加しました </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1834">adding it.</span></span> <span data-ttu-id="ebcf3-1835">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1835">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="ebcf3-1836">検索</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1836">Find</span></span>

* <span data-ttu-id="ebcf3-1837">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1837">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="ebcf3-1838">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1838">KeyVault</span></span>

* <span data-ttu-id="ebcf3-1839">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1839">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="ebcf3-1840">BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1840">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="ebcf3-1841">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1841">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="ebcf3-1842">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1842">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="ebcf3-1843">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1843">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="ebcf3-1844">ラボ</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1844">Lab</span></span>

* <span data-ttu-id="ebcf3-1845">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1845">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="ebcf3-1846">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1846">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="ebcf3-1847">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1847">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="ebcf3-1848">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1848">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="ebcf3-1849">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1849">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="ebcf3-1850">監視</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1850">Monitor</span></span>

* <span data-ttu-id="ebcf3-1851">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1851">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="ebcf3-1852">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1852">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="ebcf3-1853">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1853">Network</span></span>

* <span data-ttu-id="ebcf3-1854">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1854">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="ebcf3-1855">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1855">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="ebcf3-1856">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1856">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="ebcf3-1857">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1857">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="ebcf3-1858">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1858">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="ebcf3-1859">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1859">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="ebcf3-1860">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1860">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="ebcf3-1861">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1861">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="ebcf3-1862">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1862">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="ebcf3-1863">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1863">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="ebcf3-1864">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1864">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="ebcf3-1865">BC: `vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1865">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="ebcf3-1866">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1866">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="ebcf3-1867">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1867">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="ebcf3-1868">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1868">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="ebcf3-1869">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1869">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="ebcf3-1870">プロファイル</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1870">Profile</span></span>

* <span data-ttu-id="ebcf3-1871">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1871">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="ebcf3-1872">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1872">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="ebcf3-1873">Redis</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1873">Redis</span></span>

* <span data-ttu-id="ebcf3-1874">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1874">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="ebcf3-1875">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1875">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="ebcf3-1876">リソース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1876">Resource</span></span>

* <span data-ttu-id="ebcf3-1877">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1877">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="ebcf3-1878">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1878">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="ebcf3-1879">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1879">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="ebcf3-1880">リソース解析および API バージョンの検索が修正されました </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1880">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="ebcf3-1881">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1881">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="ebcf3-1882">az lock update のドキュメントが追加されました </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1882">Add docs for az lock update.</span></span> <span data-ttu-id="ebcf3-1883">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1883">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="ebcf3-1884">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1884">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="ebcf3-1885">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1885">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="ebcf3-1886">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1886">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="ebcf3-1887">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1887">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="ebcf3-1888">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1888">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="ebcf3-1889">Role</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1889">Role</span></span>

* <span data-ttu-id="ebcf3-1890">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1890">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="ebcf3-1891">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1891">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="ebcf3-1892">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1892">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="ebcf3-1893">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1893">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="ebcf3-1894">SQL</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1894">SQL</span></span>

* <span data-ttu-id="ebcf3-1895">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1895">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="ebcf3-1896">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1896">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="ebcf3-1897">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1897">Storage</span></span>

* <span data-ttu-id="ebcf3-1898">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1898">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="ebcf3-1899">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1899">Add support for incremental blob copy</span></span>
* <span data-ttu-id="ebcf3-1900">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1900">Add support for large block blob upload</span></span>
* <span data-ttu-id="ebcf3-1901">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1901">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1902">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1902">VM</span></span>

* <span data-ttu-id="ebcf3-1903">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1903">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="ebcf3-1904">注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1904">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="ebcf3-1905">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1905">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="ebcf3-1906">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1906">az vm/vmss disk</span></span>
  3. <span data-ttu-id="ebcf3-1907">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1907">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="ebcf3-1908">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1908">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="ebcf3-1909">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1909">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="ebcf3-1910">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1910">April 3, 2017</span></span>

<span data-ttu-id="ebcf3-1911">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1911">Version 2.0.2</span></span>

<span data-ttu-id="ebcf3-1912">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1912">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="ebcf3-1913">コア</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1913">Core</span></span>

* <span data-ttu-id="ebcf3-1914">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1914">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="ebcf3-1915">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1915">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="ebcf3-1916">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1916">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="ebcf3-1917">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1917">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ebcf3-1918">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1918">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="ebcf3-1919">不足しているテンプレート パラメーターの指定を求めるメッセージを追加 </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1919">Add prompting for missing template parameters.</span></span> <span data-ttu-id="ebcf3-1920">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1920">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="ebcf3-1921">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1921">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="ebcf3-1922">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1922">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="ebcf3-1923">ACS</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1923">ACS</span></span>

* <span data-ttu-id="ebcf3-1924">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1924">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="ebcf3-1925">ssh キー パスワードの入力要求のサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1925">Add support for ssh key password prompting.</span></span> <span data-ttu-id="ebcf3-1926">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1926">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="ebcf3-1927">Windows クラスターのためのサポートを追加 </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1927">Add support for windows clusters.</span></span> <span data-ttu-id="ebcf3-1928">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1928">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="ebcf3-1929">所有者から共同作成者へのロールの切り替え </span><span class="sxs-lookup"><span data-stu-id="ebcf3-1929">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="ebcf3-1930">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1930">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="ebcf3-1931">AppService</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1931">AppService</span></span>

* <span data-ttu-id="ebcf3-1932">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1932">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="ebcf3-1933">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1933">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="ebcf3-1934">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1934">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="ebcf3-1935">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1935">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="ebcf3-1936">DataLake</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1936">DataLake</span></span>

* <span data-ttu-id="ebcf3-1937">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1937">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="ebcf3-1938">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1938">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="ebcf3-1939">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1939">DocuemntDB</span></span>

* <span data-ttu-id="ebcf3-1940">DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1940">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="ebcf3-1941">VM</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1941">VM</span></span>

* <span data-ttu-id="ebcf3-1942">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1942">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="ebcf3-1943">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1943">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="ebcf3-1944">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1944">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="ebcf3-1945">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1945">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="ebcf3-1946">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1946">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="ebcf3-1947">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1947">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="ebcf3-1948">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1948">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="ebcf3-1949">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1949">February 27, 2017</span></span>

<span data-ttu-id="ebcf3-1950">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1950">Version 2.0.0</span></span>

<span data-ttu-id="ebcf3-1951">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1951">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="ebcf3-1952">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1952">Container Service (acs)</span></span>
- <span data-ttu-id="ebcf3-1953">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1953">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="ebcf3-1954">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1954">Networking</span></span>
- <span data-ttu-id="ebcf3-1955">Storage</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1955">Storage</span></span>

<span data-ttu-id="ebcf3-1956">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1956">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="ebcf3-1957">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1957">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="ebcf3-1958">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1958">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="ebcf3-1959">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1959">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="ebcf3-1960">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1960">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="ebcf3-1961">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1961">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="ebcf3-1962">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1962">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="ebcf3-1963">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1963">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="ebcf3-1964">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="ebcf3-1964">Provide feedback from the command line with the `az feedback` command</span></span>

