---
title: Azure CLI リリース ノート
description: Azure CLI の最新情報について説明します
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/04/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 3061d4b5519cfafbde92df68ecdee4d88d0bddff
ms.sourcegitcommit: b854f9b6acfdb814ba1d6ba87aac03e2d547d998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2019
ms.locfileid: "73536781"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="8cc5e-103">Azure CLI リリース ノート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-103">Azure CLI release notes</span></span>

## <a name="november-4-2019"></a><span data-ttu-id="8cc5e-104">2019 年 11 月 4 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-104">November 4, 2019</span></span>

<span data-ttu-id="8cc5e-105">バージョン 2.0.76</span><span class="sxs-lookup"><span data-stu-id="8cc5e-105">Version 2.0.76</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-106">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-106">ACR</span></span>

* <span data-ttu-id="8cc5e-107">コマンド `az acr pack build` にプレビュー パラメーター `--pack-image-tag` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-107">Added a preview parameter `--pack-image-tag` to command `az acr pack build`.</span></span>
* <span data-ttu-id="8cc5e-108">レジストリの作成時の監査の有効化をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-108">Supported enabling auditing on creating a registry</span></span>
* <span data-ttu-id="8cc5e-109">レジストリ スコープを持つ RBAC をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-109">Supported Repository-scoped RBAC</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-110">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-110">AKS</span></span>

* <span data-ttu-id="8cc5e-111">`az aks create` コマンドに `--enable-cluster-autoscaler`、`--min-count`、および `--max-count` を追加しました。これにより、ノード プールのクラスター オートスケーラーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-111">Added `--enable-cluster-autoscaler`, `--min-count` and `--max-count` to the `az aks create` command, which enables cluster autoscaler for the node pool.</span></span>
* <span data-ttu-id="8cc5e-112">上記のフラグに加えて、`--update-cluster-autoscaler` および `--disable-cluster-autoscaler` を `az aks update` コマンドに追加し、クラスター オートスケーラーを更新できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-112">Added the above flags as well as `--update-cluster-autoscaler` and `--disable-cluster-autoscaler` to the `az aks update` command, allowing updates to cluster autoscaler.</span></span>

### <a name="appconfig"></a><span data-ttu-id="8cc5e-113">AppConfig</span><span class="sxs-lookup"><span data-stu-id="8cc5e-113">AppConfig</span></span>

* <span data-ttu-id="8cc5e-114">App Configuration に格納される機能フラグを管理するために、appconfig feature コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-114">Added appconfig feature command group to manage feature flags stored in an App Configuration.</span></span>
* <span data-ttu-id="8cc5e-115">ファイルに対する appconfig kv export コマンドの軽微なバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-115">Fixed minor bug for appconfig kv export to file command.</span></span> <span data-ttu-id="8cc5e-116">エクスポート中に宛先ファイルの内容を読み取らないようにしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-116">Stop reading dest file contents during export.</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-117">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-117">AppService</span></span>

* <span data-ttu-id="8cc5e-118">`az appservice plan create`:appservice plan create に "persitescaling" を設定するためのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-118">`az appservice plan create`: Added support to set 'persitescaling' on appservice plan create.</span></span>
* <span data-ttu-id="8cc5e-119">webapp config ssl bind 操作がリソースから既存のタグを削除する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-119">Fixed an issue where webapp config ssl bind operation was removing existing tags from the resource</span></span>
* <span data-ttu-id="8cc5e-120">関数アプリのデプロイ時にリモート ビルド アクションをサポートするために、`az functionapp deployment source config-zip` に `--build-remote` フラグを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-120">Added `--build-remote` flag for `az functionapp deployment source config-zip` to support remote build action during function app deployment.</span></span>
* <span data-ttu-id="8cc5e-121">Windows 向けの関数アプリの既定のノードバージョンを 10 に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-121">Changed default node version on function apps to ~10 for Windows</span></span>
* <span data-ttu-id="8cc5e-122">`az functionapp create` に `--runtime-version` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-122">Added `--runtime-version` property to `az functionapp create`</span></span>

### <a name="arm"></a><span data-ttu-id="8cc5e-123">ARM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-123">ARM</span></span>

* <span data-ttu-id="8cc5e-124">`az deployment/group deployment validate`:デプロイ時に、json テンプレートで複数行とコメントをサポートするために `--handle-extended-json-format` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-124">`az deployment/group deployment validate`: Added `--handle-extended-json-format` parameter to support multiline and comments in json template when deployment.</span></span>
* <span data-ttu-id="8cc5e-125">azure-mgmt-resource を 2019-07-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-125">Bumped azure-mgmt-resource to 2019-07-01</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-126">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-126">Backup</span></span>

* <span data-ttu-id="8cc5e-127">AzureFiles のバックアップ サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-127">Added AzureFiles backup support</span></span>

### <a name="compute"></a><span data-ttu-id="8cc5e-128">Compute</span><span class="sxs-lookup"><span data-stu-id="8cc5e-128">Compute</span></span>

* <span data-ttu-id="8cc5e-129">`az vm create`:高速ネットワークと既存の NIC を一緒に指定した場合の警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-129">`az vm create`: Added warning when specifying accelerated networking and an existing NIC together.</span></span>
* <span data-ttu-id="8cc5e-130">`az vm create`:仮想マシンを割り当てる必要がある既存の仮想マシン スケール セットを指定するための `--vmss` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-130">`az vm create`: Added `--vmss` to specify an existing virtual machine scale set that the virtual machine should be assigned to.</span></span>
* <span data-ttu-id="8cc5e-131">`az vm/vmss create`:イメージ エイリアス ファイルのローカル コピーを追加し、制限付きネットワーク環境でそれにアクセスできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-131">`az vm/vmss create`: Added a local copy of image alias file so that it can be accessed in a restricted network environment.</span></span>
* <span data-ttu-id="8cc5e-132">`az vmss create`:スケール セットによる仮想マシンの管理方法を指定するための `--orchestration-mode` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-132">`az vmss create`: Added `--orchestration-mode` to specify how virtual machines are managed by the scale set.</span></span>
* <span data-ttu-id="8cc5e-133">`az vm/vmss update`:Ultra SSD 設定を更新できるように `--ultra-ssd-enabled` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-133">`az vm/vmss update`: Added `--ultra-ssd-enabled` to allow updating ultra SSD setting.</span></span>
* <span data-ttu-id="8cc5e-134">[破壊的変更] `az vm extension set`:ユーザーが `--ids` を使用して、VM に拡張機能を設定できないバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-134">[BREAKING CHANGE] `az vm extension set`: Fixed bug where users could not set an extension on a VM with `--ids`.</span></span>
* <span data-ttu-id="8cc5e-135">Azure Marketplace イメージの使用条件を管理するための新しいコマンド `az vm image terms accept/cancel/show` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-135">Added new commands `az vm image terms accept/cancel/show` to manage Azure Marketplace image terms.</span></span>
* <span data-ttu-id="8cc5e-136">VMAccessForLinux をバージョン 1.5 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-136">Updated VMAccessForLinux to version 1.5</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-137">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-137">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-138">[破壊的変更] `az sql container create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-138">[BREAKING CHANGE] `az sql container create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="8cc5e-139">[破壊的変更] `az gremlin graph create`:`--partition-key-path` を必須パラメーターに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-139">[BREAKING CHANGE] `az gremlin graph create`: Changed `--partition-key-path` to required parameter</span></span>
* <span data-ttu-id="8cc5e-140">`az sql container create`:`--unique-key-policy` および `--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-140">`az sql container create`: Added `--unique-key-policy` and `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="8cc5e-141">`az sql container create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-141">`az sql container create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="8cc5e-142">`gremlin graph create`:`--conflict-resolution-policy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-142">`gremlin graph create`: Added `--conflict-resolution-policy`</span></span>
* <span data-ttu-id="8cc5e-143">`gremlin graph create/update`:既定のスキーマ `--idx` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-143">`gremlin graph create/update`: Updated the `--idx` default schema</span></span>
* <span data-ttu-id="8cc5e-144">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-144">Fixed typo in help message</span></span>
* <span data-ttu-id="8cc5e-145">データベース:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-145">database: Added deprecation infomation</span></span>
* <span data-ttu-id="8cc5e-146">コレクション:非推奨の情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-146">collection: Added deprecation infomation</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-147">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-147">IoT</span></span>

* <span data-ttu-id="8cc5e-148">新しいルーティング ソースの種類を追加しました: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8cc5e-148">Added new routing source type: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8cc5e-149">`az iot hub create` の不十分な機能を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-149">Fixed missing features in `az iot hub create`</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-150">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-150">Key Vault</span></span>

* <span data-ttu-id="8cc5e-151">証明書ファイルが存在しない場合の予期しないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-151">Fixed an unexpected error when certificate file does not exist</span></span>
* <span data-ttu-id="8cc5e-152">`az keyvault recover/purge` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-152">Fixed `az keyvault recover/purge` not working</span></span>

### <a name="netappfiles"></a><span data-ttu-id="8cc5e-153">NetAppFiles</span><span class="sxs-lookup"><span data-stu-id="8cc5e-153">NetAppFiles</span></span>

* <span data-ttu-id="8cc5e-154">API バージョン 2019-07-01 を使用するために azure-mgmt-netapp を 0.6.0 にアップグレードしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-154">Upgraded azure-mgmt-netapp to 0.6.0 to use API version 2019-07-01.</span></span> <span data-ttu-id="8cc5e-155">この新しい API バージョンには以下の変更内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-155">This new API version includes:</span></span>

    - <span data-ttu-id="8cc5e-156">ボリューム作成の `--protocol-types` が "NFSv4" ではなく "NFSv 4.1" を受け入れるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-156">Volume creation `--protocol-types` accepts now "NFSv4.1" not "NFSv4"</span></span>
    - <span data-ttu-id="8cc5e-157">ボリューム エクスポート ポリシー プロパティの名前が "nfsv4" ではなく "nfsv41" に変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-157">Volume export policy property now named 'nfsv41' not 'nfsv4'</span></span>
    - <span data-ttu-id="8cc5e-158">ボリュームの `--creation-token` の名前が `--file-path` に変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-158">Volume `--creation-token` renamed to `--file-path`</span></span>
    - <span data-ttu-id="8cc5e-159">スナップショット作成日の名前が単に "created" に変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-159">Snapshot creation date now named just 'created'</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-160">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-160">Network</span></span>

* <span data-ttu-id="8cc5e-161">`az network private-dns link vnet create/update`:テナント間の仮想ネットワーク リンクがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-161">`az network private-dns link vnet create/update`: Support cross-tenant virtual network linking.</span></span>
* <span data-ttu-id="8cc5e-162">[破壊的変更] `az network vnet subnet list`:`--resource-group` と `--vnet-name` を必須に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-162">[BREAKING CHANGE] `az network vnet subnet list`: Changed `--resource-group` and `--vnet-name` to be required now.</span></span>
* <span data-ttu-id="8cc5e-163">`az network public-ip prefix create`:作成時の IP アドレス バージョン (IPv4、IPv6) の指定をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-163">`az network public-ip prefix create`: Supported to specify IP address version (IPv4, IPv6) when creation</span></span>
* <span data-ttu-id="8cc5e-164">azure-mgmt-network を 7.0.0 に、api-version を 2019-09-01 に引き上げました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-164">Bumped azure-mgmt-network to 7.0.0 and api-version to 2019-09-01</span></span>
* <span data-ttu-id="8cc5e-165">`az network vrouter`:新しいサービスの仮想ルーターと仮想ルーター ピアリングをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-165">`az network vrouter`: Supported new service virtual router and virtual router peering</span></span>
* <span data-ttu-id="8cc5e-166">`az network express-route gateway connection`:`--internet-security` をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-166">`az network express-route gateway connection`: Supported `--internet-security`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-167">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-167">Profile</span></span>

* <span data-ttu-id="8cc5e-168">`az account get-access-token --resource-type ms-graph` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-168">Fixed `az account get-access-token --resource-type ms-graph` not working</span></span>
* <span data-ttu-id="8cc5e-169">`az login` からの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-169">Removed warning from `az login`</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-170">RBAC</span><span class="sxs-lookup"><span data-stu-id="8cc5e-170">RBAC</span></span>

* <span data-ttu-id="8cc5e-171">`az ad app update --id {} --display-name {}` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-171">Fixed `az ad app update --id {} --display-name {}` doesn't work</span></span>

### <a name="servicefabric"></a><span data-ttu-id="8cc5e-172">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-172">ServiceFabric</span></span>

* <span data-ttu-id="8cc5e-173">`az sf cluster create`:Service Fabric の Linux と Windows の template.json コンピューティング vmss を標準からマネージド ディスクに変更することによって問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-173">`az sf cluster create`: Fixed an issue by modifying service fabric linux and windows template.json compute vmss from standard to managed disks</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-174">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-174">SQL</span></span>

* <span data-ttu-id="8cc5e-175">新しい SQL Database オファリングであるサーバーレス コンピューティング モデルの CRUD 操作をサポートするために、`--compute-model`、`--auto-pause-delay`、および `--min-capacity` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-175">Added `--compute-model`, `--auto-pause-delay`, and `--min-capacity` parameters to support CRUD operations for new SQL Database offering: Serverless compute model.</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-176">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-176">Storage</span></span>

* <span data-ttu-id="8cc5e-177">`az storage account create/update`:Azure Files Active Directory Domain Services 認証をサポートするために、--enable-files-adds パラメーターと Azure Active Directory プロパティ引数グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-177">`az storage account create/update`: Added --enable-files-adds parameter and Azure Active Directory Properties Argument group to support Azure Files Active Directory Domain Service Authentication</span></span>
* <span data-ttu-id="8cc5e-178">ストレージ アカウントの Kerberos キーの一覧表示または再生成をサポートするために、`az storage account keys list/renew` を拡張しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-178">Expanded `az storage account keys list/renew` to support listing or regenerating Kerberos keys of storage account.</span></span>

## <a name="october-15-2019"></a><span data-ttu-id="8cc5e-179">2019 年 10 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-179">October 15, 2019</span></span>

<span data-ttu-id="8cc5e-180">バージョン 2.0.75</span><span class="sxs-lookup"><span data-stu-id="8cc5e-180">Version 2.0.75</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-181">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-181">AKS</span></span>

* <span data-ttu-id="8cc5e-182">Kubernetes のバージョンでサポートされている場合、`--load-balancer-sku` の既定値を `standard` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-182">Changed `--load-balancer-sku` default value to `standard` if supported by the kubernetes version</span></span>
* <span data-ttu-id="8cc5e-183">Kubernetes のバージョンでサポートされている場合、`--vm-set-type` の既定値を `virtualmachinescalesets` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-183">Changed `--vm-set-type` default value to `virtualmachinescalesets` if supported by the kubernetes version</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-184">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-184">AMS</span></span>

* <span data-ttu-id="8cc5e-185">[重大な変更] `job start` の名前を `job create` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-185">[BREAKING CHANGE] Changed the name of `job start` to `job create`</span></span>
* <span data-ttu-id="8cc5e-186">[重大な変更] `content-key-policy create` の `--ask` パラメーターが UTF8 ではなく 32 文字の 16 進文字列を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-186">[BREAKING CHANGE] Changed the `--ask` parameter of `content-key-policy create` to use a 32-character hex string instead of UTF8</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-187">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-187">AppService</span></span>

* <span data-ttu-id="8cc5e-188">コマンド `webapp config access-restriction show|set|add|remove` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-188">Added commands `webapp config access-restriction show|set|add|remove`</span></span>
* <span data-ttu-id="8cc5e-189">より優れたエラー処理を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-189">Added better error handling to `webapp up`</span></span>
* <span data-ttu-id="8cc5e-190">`Isolated` SKU のサポートを `appservice plan update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-190">Added support for `Isolated` SKU to `appservice plan update`</span></span>

### <a name="arm"></a><span data-ttu-id="8cc5e-191">ARM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-191">ARM</span></span>

* <span data-ttu-id="8cc5e-192">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `deployment create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-192">Added `--handle-extended-json-format` parameter `deployment create` to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="8cc5e-193">Compute</span><span class="sxs-lookup"><span data-stu-id="8cc5e-193">Compute</span></span>

* <span data-ttu-id="8cc5e-194">`--enable-agent` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-194">Added `--enable-agent` parameter to `vm create`</span></span>
* <span data-ttu-id="8cc5e-195">ゾーンを使用するときに標準のパブリック IP SKU を自動的に使用するように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-195">Changed `vm create` to use standard public IP SKU automatically when using zones</span></span>
* <span data-ttu-id="8cc5e-196">VM の有効なコンピューター名が指定されていない場合に自動的に作成されるように `vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-196">Changed `vm create` to automatically create a valid computer name for a VM if none is provided</span></span>
* <span data-ttu-id="8cc5e-197">VMSS 内の仮想マシンのカスタム コンピューター名プレフィックスをサポートするために `--computer-name-prefix` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-197">Added `--computer-name-prefix` parameter to `vmss create` to support custom computer name prefix of virtual machines in the VMSS</span></span>
* <span data-ttu-id="8cc5e-198">ログ分析ワークスペースを自動的に有効にする `--workspace` パラメーターを `vm create` に追加します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-198">Add `--workspace` parameter to `vm create` to enable log analytics workspace automatically</span></span>
* <span data-ttu-id="8cc5e-199">ギャラリーの API バージョンが 2019-07-01 に更新されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-199">Updated galleries API version to 2019-07-01</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-200">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-200">Core</span></span>

* <span data-ttu-id="8cc5e-201">汎用の update コマンドで `--set` パラメーターの構文チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-201">Added syntax check for `--set` parameter in generic update command</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-202">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-202">IoT</span></span>

* <span data-ttu-id="8cc5e-203">`iot hub show` で "リソースが見つかりません" のエラーが誤って発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-203">Fixed an issue where `iot hub show` would incorrectly error with "resource not found"</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-204">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-204">Monitor</span></span>

* <span data-ttu-id="8cc5e-205">CRUD のサポートを `monitor log-analytics workspace` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-205">Added support for CRUD to `monitor log-analytics workspace`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-206">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-206">Network</span></span>

* <span data-ttu-id="8cc5e-207">クロステナントの仮想リンクのサポートを `network private-dns link vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-207">Added support for cross-tenant virtual linking to `network private-dns link vnet [create|update]`</span></span>
* <span data-ttu-id="8cc5e-208">[重大な変更] `network vnet subnet list` で `--resource-group` および `--vnet-name` パラメーターが必須に変更になりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-208">[BREAKING CHANGE] Changed `network vnet subnet list` to require `--resource-group` and `--vnet-name` parameters</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-209">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-209">SQL</span></span>

* <span data-ttu-id="8cc5e-210">マネージ インスタンスの AAD 管理者の設定をサポートするコマンドを `sql mi ad-admin` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-210">Added commands to `sql mi ad-admin` that support setting an AAD administrator on managed instances</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-211">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-211">Storage</span></span>

* <span data-ttu-id="8cc5e-212">サービス間のコピー中にアクセス層を保持する `--preserve-s2s-access-tier` パラメーターを `storage copy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-212">Added `--preserve-s2s-access-tier` parameter `storage copy` to preserve access tier during service to service copy</span></span>
* <span data-ttu-id="8cc5e-213">ストレージ アカウントで大容量ファイルの共有をサポートするために `--enable-large-file-share` パラメーターを `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-213">Added `--enable-large-file-share` parameter to `storage account [create|update]` to support large file shares for storage account</span></span>

## <a name="september-24-2019"></a><span data-ttu-id="8cc5e-214">2019 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-214">September 24, 2019</span></span>

<span data-ttu-id="8cc5e-215">バージョン 2.0.74</span><span class="sxs-lookup"><span data-stu-id="8cc5e-215">Version 2.0.74</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-216">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-216">ACR</span></span>

* <span data-ttu-id="8cc5e-217">必須の `--type` パラメーターを `acr config retention update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-217">Added a required `--type` parameter to `acr config retention update`</span></span>
* <span data-ttu-id="8cc5e-218">[破壊的変更] `acr config` コマンド グループでパラメーター `--name -n` の名前が `--registry -r ` に変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-218">[BREAKING CHNAGE] Renamed parameter `--name -n` changed to `--registry -r ` for `acr config` command group</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-219">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-219">AKS</span></span>

* <span data-ttu-id="8cc5e-220">`--load-balancer-sku` パラメーターを `aks create` コマンドに追加しました。これにより、SLB を使用する AKS クラスターを作成できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-220">Added `--load-balancer-sku` parameter to `aks create` command, which allows for creating AKS cluster with SLB</span></span>
* <span data-ttu-id="8cc5e-221">`--load-balancer-managed-outbound-ip-count`、`--load-balancer-outbound-ips`、`--load-balancer-outbound-ip-prefixes` パラメーターを `aks [create|update]` コマンドに追加しました。これにより、SLB を使用する AKS クラスターのロード バランサー プロファイルを更新できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-221">Added `--load-balancer-managed-outbound-ip-count`, `--load-balancer-outbound-ips` and `--load-balancer-outbound-ip-prefixes` parameters to `aks [create|update]` commands, which allow for updating load balancer profile of an AKS cluster with SLB</span></span>
* <span data-ttu-id="8cc5e-222">`--vm-set-type` パラメーターを `aks create` コマンドに追加しました。これにより、AKS クラスターの VM の種類 (vmas または vmss) を指定できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-222">Added `--vm-set-type` parameter to `aks create` command, which allows to specify vm types of an AKS Cluster (vmas or vmss)</span></span>

### <a name="arm"></a><span data-ttu-id="8cc5e-223">ARM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-223">ARM</span></span>

* <span data-ttu-id="8cc5e-224">JSON テンプレートで複数行とコメントをサポートするための `--handle-extended-json-format` パラメーターを `group deployment create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-224">Added `--handle-extended-json-format` parameter to `group deployment create` command to support multiline and comments in json template</span></span>

### <a name="compute"></a><span data-ttu-id="8cc5e-225">Compute</span><span class="sxs-lookup"><span data-stu-id="8cc5e-225">Compute</span></span>

* <span data-ttu-id="8cc5e-226">終了のスケジュール化されたイベントを構成しやすくするために `--terminate-notification-time` パラメーターを `vmss [create|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-226">Added `--terminate-notification-time` parameter to `vmss [create|update]` commands to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="8cc5e-227">終了のスケジュール化されたイベントを構成しやすくするために `--enable-terminate-notification` パラメーターを `vmss update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-227">Added `--enable-terminate-notification` parameter to `vmss update` command to support terminate scheduled event configurability</span></span>
* <span data-ttu-id="8cc5e-228">`--priority,` `--eviction-policy,` `--max-billing` パラメーターを `[vm|vmss] create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-228">Added `--priority,` `--eviction-policy,` `--max-billing` parameters to `[vm|vmss] create` commands</span></span>
* <span data-ttu-id="8cc5e-229">`disk create` を変更し、ディスク アップロードの正確なサイズを指定できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-229">Changed `disk create` to allow specifying the exact size of the disk upload</span></span>
* <span data-ttu-id="8cc5e-230">マネージド ディスクの増分スナップショットのサポートを `snapshot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-230">Added support for incremental snapshots for managed disks to `snapshot create`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="8cc5e-231">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-231">Cosmos DB</span></span>

* <span data-ttu-id="8cc5e-232">キー、読み取り専用キー、または接続文字列を表示する `--type <key-type>` パラメーターを `cosmosdb keys list` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-232">Added `--type <key-type>` parameter to `cosmosdb keys list` command to show key, read only keys or connection strings</span></span>
* <span data-ttu-id="8cc5e-233">`cosmosdb keys regenerate` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-233">Added `cosmosdb keys regenerate` command</span></span>
* <span data-ttu-id="8cc5e-234">[非推奨] `cosmosdb list-connection-strings`、`cosmosdb regenerate-key`、`cosmosdb list-read-only-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-234">[DEPRECATED] Deprecated `cosmosdb list-connection-strings`, `cosmosdb regenerate-key` and `cosmosdb list-read-only-keys` commands</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8cc5e-235">EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-235">EventGrid</span></span>

* <span data-ttu-id="8cc5e-236">正しいパラメーターを参照するようにエンドポイントのヘルプ テキストを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-236">Fixed the endpoint help text to refer to the right parameter</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-237">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-237">Key Vault</span></span>

* <span data-ttu-id="8cc5e-238">テナントを使用してログインすると (`login -t`)、`keyvault create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-238">Fixed issue where logging in with a tenant (`login -t`) could cause `keyvault create` to fail</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-239">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-239">Monitor</span></span>

* <span data-ttu-id="8cc5e-240">`monitor metrics alert create` の `--condition` 引数で `:` 文字を使用できないという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-240">Fixed issue where `:` character was not allowed in `--condition` argument to `monitor metrics alert create`</span></span>

### <a name="policy"></a><span data-ttu-id="8cc5e-241">ポリシー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-241">Policy</span></span>

* <span data-ttu-id="8cc5e-242">Policy API バージョン 2019-06-01 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-242">Added support for Policy API version 2019-06-01</span></span>
* <span data-ttu-id="8cc5e-243">`policy assignment create` コマンドに `--enforcement-mode` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-243">Added `--enforcement-mode` parameter to `policy assignment create` command</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-244">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-244">Storage</span></span>

* <span data-ttu-id="8cc5e-245">`az storage copy` コマンドに `--blob-type` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-245">Added `--blob-type` parameter to `az storage copy` command</span></span>

## <a name="september-10-2019"></a><span data-ttu-id="8cc5e-246">2019 年 9 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-246">September 10, 2019</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-247">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-247">ACR</span></span>

* <span data-ttu-id="8cc5e-248">アイテム保持ポリシーを構成するためのコマンド グループ `acr config retention` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-248">Added command group `acr config retention` to configure retention policy</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-249">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-249">AKS</span></span>

* <span data-ttu-id="8cc5e-250">次のコマンドを使用した ACR 統合のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-250">Added support for ACR integration with the following commands:</span></span>
  * <span data-ttu-id="8cc5e-251">AKS クラスターに ACR をアタッチするための `--attach-acr` パラメーターを `aks [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-251">Added `--attach-acr` parameter to `aks [create|update]` to attach an ACR to an AKS cluster</span></span>
  * <span data-ttu-id="8cc5e-252">AKS クラスターから ACR をデタッチするための `--detach-acr` パラメーターを `aks update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-252">Added `--detach-acr` parameter to `aks update` to detach the ACR from an AKS cluster</span></span>

### <a name="arm"></a><span data-ttu-id="8cc5e-253">ARM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-253">ARM</span></span>

* <span data-ttu-id="8cc5e-254">API バージョン 2019-05-10 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-254">Updated to use API version 2019-05-10</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-255">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-255">Batch</span></span>

* <span data-ttu-id="8cc5e-256">`batch pool create` の `--json-file` に新しい JSON 構成設定を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-256">Added new JSON configuration settings to `--json-file` for `batch pool create`:</span></span>
  * <span data-ttu-id="8cc5e-257">ファイル システム マウント用の `MountConfigurations` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-257">Added `MountConfigurations` for file system mounts (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
  * <span data-ttu-id="8cc5e-258">プール上のパブリック IP 用に、`NetworkConfiguration` にオプションのプロパティ `publicIPs` を追加しました (詳細については https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body を参照してください)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-258">Added optional property `publicIPs` on `NetworkConfiguration` for public IPs on pools (see https://docs.microsoft.com/en-us/rest/api/batchservice/pool/add#request-body for details)</span></span>
* <span data-ttu-id="8cc5e-259">共有イメージ ギャラリーのサポートを `--image` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-259">Added support for shared image galleries to `--image`</span></span>
* <span data-ttu-id="8cc5e-260">[重大な変更] `batch pool create` の `--start-task-wait-for-success` の既定値を `true` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-260">[BREAKING CHANGE] Changed default value of `--start-task-wait-for-success` on `batch pool create` to be `true`</span></span>
* <span data-ttu-id="8cc5e-261">[重大な変更] `AutoUserSpecification` の `Scope` の既定値が常に Pool になるように変更しました (以前は Windows ノードでは `Task`、Linux ノードでは `Pool` でした)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-261">[BREAKING CHANGE] Changed default value for `Scope` on `AutoUserSpecification` to always be Pool (was `Task` on Windows nodes, `Pool` on Linux nodes)</span></span>
  * <span data-ttu-id="8cc5e-262">この引数は、`--json-file` を使用して JSON 構成からのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-262">This argument can only be set from a JSON configuration with `--json-file`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-263">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-263">HDInsight</span></span>

* <span data-ttu-id="8cc5e-264">GA リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-264">GA release</span></span>
* <span data-ttu-id="8cc5e-265">[重大な変更] `az hdinsight resize` のパラメーター `--workernode-count/-c` が必須に変更されました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-265">[BREAKING CHANGE] Changed parameter `--workernode-count/-c` of `az hdinsight resize` to be required.</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-266">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-266">Key Vault</span></span>

* <span data-ttu-id="8cc5e-267">ネットワーク ルールからサブネットを削除できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-267">Fixed issue where subnets couldn't be deleted from network rules</span></span>
* <span data-ttu-id="8cc5e-268">重複したサブネットと IP アドレスをネットワーク ルールに追加できる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-268">Fixed issue where duplicated subnets and IP addresses could be added to network rules</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-269">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-269">Network</span></span>

* <span data-ttu-id="8cc5e-270">トラフィック分析間隔の値を設定する `--interval` パラメーターを `network watcher flow-log` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-270">Added `--interval` parameter to `network watcher flow-log` to set traffic analysis interval value</span></span>
* <span data-ttu-id="8cc5e-271">ゲートウェイ ID を管理するための `network application-gateway identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-271">Added `network application-gateway identity` to manage gateway identity</span></span>
* <span data-ttu-id="8cc5e-272">Key Vault ID を設定するためのサポートを `network application-gateway ssl-cert` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-272">Added support for setting Key Vault ID to `network application-gateway ssl-cert`</span></span>
* <span data-ttu-id="8cc5e-273">`network express-route peering peer-connection [show|list]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-273">Added `network express-route peering peer-connection [show|list]`</span></span>

### <a name="policy"></a><span data-ttu-id="8cc5e-274">ポリシー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-274">Policy</span></span>

* <span data-ttu-id="8cc5e-275">API バージョン 2019-01-01 を使用するように更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-275">Updated to use API version 2019-01-01</span></span>

## <a name="august-27-2019"></a><span data-ttu-id="8cc5e-276">2019 年 8 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-276">August 27, 2019</span></span>

<span data-ttu-id="8cc5e-277">バージョン 2.0.72</span><span class="sxs-lookup"><span data-stu-id="8cc5e-277">Version 2.0.72</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-278">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-278">ACR</span></span>

* <span data-ttu-id="8cc5e-279">[重大な変更] `classic` SKU のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-279">[BREAKING CHANGE] Removed support for the `classic` SKU</span></span>

### <a name="api-management"></a><span data-ttu-id="8cc5e-280">API Management</span><span class="sxs-lookup"><span data-stu-id="8cc5e-280">API Management</span></span>

* <span data-ttu-id="8cc5e-281">[プレビュー] `apim` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-281">[PREVIEW] Added `apim` command group</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-282">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-282">AppService</span></span>

* <span data-ttu-id="8cc5e-283">スロットを指定したときの `webapp webjob continuous start` コマンドに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-283">Fixed issue with `webapp webjob continuous start` command when specifying a slot</span></span>
* <span data-ttu-id="8cc5e-284">`env` フォルダーを検出してデプロイに使用されているファイルから削除するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-284">Changed `webapp up` to detect `env` folder and remove it from the file used for deployment</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-285">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-285">Keyvault</span></span>

* <span data-ttu-id="8cc5e-286">`--expires` 引数を無視する `keyvault secret set` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-286">Fixed a bug in `keyvault secret set` that igored the `--expires` argument</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-287">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-287">Network</span></span>

* <span data-ttu-id="8cc5e-288">`--private-ip-address-version` 引数に IPv6 アドレスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-288">Added support for IPv6 addresses to `--private-ip-address-version` arguments</span></span>
* <span data-ttu-id="8cc5e-289">プライベート エンドポイントの管理用に新しいコマンド `network private-endpoint [create|update|list-types]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-289">Added new commands `network private-endpoint [create|update|list-types]` for private endpoint management</span></span>
* <span data-ttu-id="8cc5e-290">コマンド グループ `network private-link-service` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-290">Added command group `network private-link-service`</span></span>
* <span data-ttu-id="8cc5e-291">`--private-endpoint-network-policies` 引数と `--private-link-service-network-policies` 引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-291">Added `--private-endpoint-network-policies` and `--private-link-service-network-policies` arguments to `network vnet subnet update`</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-292">RBAC</span><span class="sxs-lookup"><span data-stu-id="8cc5e-292">RBAC</span></span>

* <span data-ttu-id="8cc5e-293">ホームページが更新されない `ad app update --homepage` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-293">Fixed issue with `ad app update --homepage` where homepage would not be updated</span></span>

### <a name="servicefabric"></a><span data-ttu-id="8cc5e-294">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-294">ServiceFabric</span></span>

* <span data-ttu-id="8cc5e-295">キー コンテナーの大文字と小文字が混在する名前のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-295">Added support for mixed-case Key Vault names</span></span>
* <span data-ttu-id="8cc5e-296">Key Vault で証明書を使用したときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-296">Fixed issue when using certificates in Key Vault</span></span>
* <span data-ttu-id="8cc5e-297">PFX 証明書ファイルの使用に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-297">Fixed issue with using PFX certificate files</span></span>
* <span data-ttu-id="8cc5e-298">Key Vault リソースグループが指定されていなかったときの `sf cluster certificate add` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-298">Fixed issue with `sf cluster certificate add` when Key Vault resource group wasn't specified</span></span>
* <span data-ttu-id="8cc5e-299">`sf cluster set` が動作しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-299">Fixed issue with `sf cluster set` not working</span></span>

### <a name="signalr"></a><span data-ttu-id="8cc5e-300">SignalR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-300">SignalR</span></span>

* <span data-ttu-id="8cc5e-301">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-301">Added new commands:</span></span>
  * <span data-ttu-id="8cc5e-302">`signalr cors`:SignalR CORS の管理</span><span class="sxs-lookup"><span data-stu-id="8cc5e-302">`signalr cors`: Manage SignalR CORS</span></span>
  * <span data-ttu-id="8cc5e-303">`signalr restart`:SignalR Service の再起動</span><span class="sxs-lookup"><span data-stu-id="8cc5e-303">`signalr restart`: Restart a SignalR service</span></span>
  * <span data-ttu-id="8cc5e-304">`signalr update`:SignalR Service の更新</span><span class="sxs-lookup"><span data-stu-id="8cc5e-304">`signalr update`: Update a SignalR service</span></span>
* <span data-ttu-id="8cc5e-305">`--service-mode` 引数を `signalr create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-305">Added `--service-mode` argument to `signalr create`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-306">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-306">Storage</span></span>

* <span data-ttu-id="8cc5e-307">`storage account revoke-delegation-keys` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-307">Added `storage account revoke-delegation-keys` command</span></span>

## <a name="august-13-2019"></a><span data-ttu-id="8cc5e-308">2019 年 8 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-308">August 13, 2019</span></span>

<span data-ttu-id="8cc5e-309">バージョン 2.0.71</span><span class="sxs-lookup"><span data-stu-id="8cc5e-309">Version 2.0.71</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-310">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-310">AppService</span></span>

* <span data-ttu-id="8cc5e-311">`webapp webjob continuous` コマンドがスロットで失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-311">Fixed issue where `webapp webjob continuous` commands were failing for slots</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-312">BotService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-312">BotService</span></span>

* <span data-ttu-id="8cc5e-313">[重大な変更] v3 SDK ボットの作成のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-313">[BREAKING CHANGE] Removed support for creating v3 SDK bots</span></span>

### <a name="cognitiveservices"></a><span data-ttu-id="8cc5e-314">CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8cc5e-314">CognitiveServices</span></span>

* <span data-ttu-id="8cc5e-315">`cognitiveservices account network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-315">Added `cognitiveservices account network-rule` commands</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="8cc5e-316">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-316">Cosmos DB</span></span>

* <span data-ttu-id="8cc5e-317">複数の書き込み場所を更新するときの警告を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-317">Removed warning when updating multiple write locations</span></span>
* <span data-ttu-id="8cc5e-318">CosmosDB SQL、MongoDB、Cassandra、Gremlin、およびテーブル リソースとリソースのスループットのための CRUD コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-318">Added CRUD commands for CosmosDB SQL, MongoDB, Cassandra, Gremlin and Table resources and resource's throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-319">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-319">HDInsight</span></span>

<span data-ttu-id="8cc5e-320">このリリースには、多数の破壊的変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-320">This release contains a large number of breaking changes.</span></span>

* <span data-ttu-id="8cc5e-321">[重大な変更] `hdinsight create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-321">[BREAKING CHANGE] Renamed parameters for `hdinsight create`:</span></span>
  * <span data-ttu-id="8cc5e-322">`--storage-default-container` の名前を `--storage-container` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-322">Renamed `--storage-default-container` to `--storage-container`</span></span>
  * <span data-ttu-id="8cc5e-323">`--storage-default-filesystem` の名前を `--storage-filesystem` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-323">Renamed `--storage-default-filesystem` to `--storage-filesystem`</span></span>
* <span data-ttu-id="8cc5e-324">[重大な変更] `application create` の `--name` 引数が、クラスター名の代わりにアプリケーション名を表すように変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-324">[BREAKING CHANGE] Changed the `--name` argument of `application create` to represent the application name instead of the cluster name</span></span>
* <span data-ttu-id="8cc5e-325">`--cluster-name` 引数が `application create` に追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-325">Added `--cluster-name` argument to `application create` to replace old `--name` functionality</span></span>
* <span data-ttu-id="8cc5e-326">[重大な変更] `application create` のパラメーターの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-326">[BREAKING CHANGE] Renamed parameters for `application create`:</span></span>
  * <span data-ttu-id="8cc5e-327">`--application-type` の名前を `--type` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-327">Renamed `--application-type` to `--type`</span></span>
  * <span data-ttu-id="8cc5e-328">`--marketplace-identifier` の名前を `--marketplace-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-328">Renamed `--marketplace-identifier` to `--marketplace-id`</span></span>
  * <span data-ttu-id="8cc5e-329">`--https-endpoint-access-mode` の名前を `--access-mode` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-329">Renamed `--https-endpoint-access-mode` to `--access-mode`</span></span>
  * <span data-ttu-id="8cc5e-330">`--https-endpoint-destination-port` の名前を `--destination-port` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-330">Renamed  `--https-endpoint-destination-port` to `--destination-port`</span></span>
* <span data-ttu-id="8cc5e-331">[重大な変更] `application create` のパラメーターを削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-331">[BREAKING CHANGE] Removed parameters for `application create`:</span></span>
  * `--https-endpoint-location`
  * `--https-endpoint-public-port`
  * `--ssh-endpoint-destination-port`
  * `--ssh-endpoint-location`
  * `--ssh-endpoint-public-port`
* <span data-ttu-id="8cc5e-332">[破壊的変更] `hdinsight resize`の `--target-instance-count` の名前を `--workernode-count` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-332">[BREAKING CHNAGE] Renamed `--target-instance-count` to `--workernode-count` for `hdinsight resize`</span></span>
* <span data-ttu-id="8cc5e-333">[重大な変更] `hdinsight script-action` グループのすべてのコマンドが、スクリプト アクションの名前として `--name` パラメーターを使用するように変更されました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-333">[BREAKING CHANGE] Changed all commands in the `hdinsight script-action` group to use the `--name` parameter as the name of the script action.</span></span>
* <span data-ttu-id="8cc5e-334">`--cluster-name` 引数がすべての `hdinsight script-action` コマンドに追加され、以前の `--name` の機能に置き換わりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-334">Added `--cluster-name` argument to all `hdinsight script-action` commands to replace old `--name` functionality</span></span>
* <span data-ttu-id="8cc5e-335">[重大な変更] すべての `hdinsight script-action` コマンドで `--script-execution-id` の名前を `--execution-id` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-335">[BREAKING CHANGE] Renamed `--script-execution-id` to `--execution-id` for all `hdinsight script-action` commands</span></span>
* <span data-ttu-id="8cc5e-336">[重大な変更] 名前を `hdinsight script-action show` から `hdinsight script-action show-execution-details` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-336">[BREAKING CHANGE] Renamed `hdinsight script-action show` to `hdinsight script-action show-execution-details`</span></span>
* <span data-ttu-id="8cc5e-337">[破壊的変更] `hdinsight script-action execute --roles` に対するパラメーターを、コンマ区切りではなくスペース区切りにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-337">[BREAKING CHNAGE] Changed parameters to `hdinsight script-action execute --roles` to be space-separated instead of comma-separated</span></span>
* <span data-ttu-id="8cc5e-338">[重大な変更] `hdinsight script-action list`の `--persisted` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-338">[BREAKING CHANGE] Removed the `--persisted` parameter of `hdinsight script-action list`</span></span>
* <span data-ttu-id="8cc5e-339">ローカル JSON ファイルへのパスまたは JSON 文字列を受け入れるように `hdinsight create --cluster-configurations` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-339">Changed the `hdinsight create --cluster-configurations` parameter to accept a path to a local JSON file or a JSON string</span></span>
* <span data-ttu-id="8cc5e-340">`hdinsight script-action list-execution-history` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-340">Added command `hdinsight script-action list-execution-history`</span></span>
* <span data-ttu-id="8cc5e-341">Log Analytics ワークスペース ID またはワークスペース名を受け入れるように `hdinsight monitor enable --workspace` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-341">Changed `hdinsight monitor enable --workspace` to accept a Log Analytics workspace ID or workspace name</span></span>
* <span data-ttu-id="8cc5e-342">`hdinsight monitor enable --primary-key` 引数を追加しました。これは、ワークスペース ID がパラメーターとして指定されている場合に必要です</span><span class="sxs-lookup"><span data-stu-id="8cc5e-342">Added the `hdinsight monitor enable --primary-key` argument, which is needed if a workspace ID is provided as the parameter</span></span>
* <span data-ttu-id="8cc5e-343">例をさらに追加し、ヘルプ メッセージの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-343">Added more examples and updated descriptions for help messages</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-344">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-344">Interactive</span></span>

* <span data-ttu-id="8cc5e-345">読み込みエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-345">Fixed a loading error</span></span>

### <a name="kubernetes"></a><span data-ttu-id="8cc5e-346">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="8cc5e-346">Kubernetes</span></span>

* <span data-ttu-id="8cc5e-347">ダッシュボードのコンテナー ポートで `https` が使用されている場合に `https` を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-347">Changed to use `https` if dashboard container port is using `https`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-348">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-348">Network</span></span>

* <span data-ttu-id="8cc5e-349">`--yes` 引数を `network dns record-set cname delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-349">Added `--yes` argument `network dns record-set cname delete`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-350">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-350">Profile</span></span>

* <span data-ttu-id="8cc5e-351">リソースのアクセス トークンを取得するための `account get-access-token` に `--resource-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-351">Added `--resource-type` argument to `account get-access-token` to get resource access tokens</span></span>

### <a name="servicefabric"></a><span data-ttu-id="8cc5e-352">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-352">ServiceFabric</span></span>

* <span data-ttu-id="8cc5e-353">sf cluster create でサポートされているすべての OS バージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-353">Added all supported os version for sf cluster create</span></span>
* <span data-ttu-id="8cc5e-354">プライマリ証明書の検証のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-354">Fixed primary certificate validation bug</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-355">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-355">Storage</span></span>

* <span data-ttu-id="8cc5e-356">`storage copy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-356">Added command `storage copy`</span></span>

## <a name="july-30-2019"></a><span data-ttu-id="8cc5e-357">2019 年 7 月 30 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-357">July 30, 2019</span></span>

<span data-ttu-id="8cc5e-358">バージョン 2.0.70</span><span class="sxs-lookup"><span data-stu-id="8cc5e-358">Version 2.0.70</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-359">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-359">ACR</span></span>

* <span data-ttu-id="8cc5e-360">問題 #9952 (`acr pack build` コマンドでの回帰) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-360">Fixed issue #9952 (a regression in the `acr pack build` command)</span></span>
* <span data-ttu-id="8cc5e-361">`acr pack build` の既定のビルダー イメージ名を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-361">Removed the default builder image name in `acr pack build`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-362">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-362">Appservice</span></span>

* <span data-ttu-id="8cc5e-363">リソースが見つからない場合にメッセージ表示するように `webapp config ssl` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-363">Changed `webapp config ssl` to show a message if a resource is not found</span></span>
* <span data-ttu-id="8cc5e-364">`functionapp create` がストレージ アカウントの種類 `Standard_RAGRS` を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-364">Fixed issue where `functionapp create` does not accept `Standard_RAGRS` storage account type</span></span>
* <span data-ttu-id="8cc5e-365">古いバージョンの python を使用して `webapp up` を実行すると失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-365">Fixed an issue where `webapp up` would fail if run using older versions of python</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-366">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-366">Network</span></span>

* <span data-ttu-id="8cc5e-367">`network nic ip-config add` から無効なパラメーター `--ids` を削除しました (#9861 の修正)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-367">Removed invalid parameter `--ids` from `network nic ip-config add` (fixes #9861)</span></span>
* <span data-ttu-id="8cc5e-368">#9604 を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-368">Fixes #9604.</span></span> <span data-ttu-id="8cc5e-369">信頼されたルート証明書へのユーザーの関連付けをサポートするために、`network application-gateway http-settings [create|update]` に `--root-certs` パラメーターを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-369">Added `--root-certs` parameter to `network application-gateway http-settings [create|update]` to support user associate trusted root certificates.</span></span>
* <span data-ttu-id="8cc5e-370">`network dns record-set ns create` の引数 `--subscription` を修正しました (#9965)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-370">Fixed arguent `--subscription` for `network dns record-set ns create` (#9965)</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-371">RBAC</span><span class="sxs-lookup"><span data-stu-id="8cc5e-371">RBAC</span></span>

* <span data-ttu-id="8cc5e-372">`user update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-372">Added `user update` command</span></span>
* <span data-ttu-id="8cc5e-373">[非推奨] ユーザー関連コマンドで `--upn-or-object-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-373">[DEPRECATED] Deprecated `--upn-or-object-id` from user-related commands</span></span>
    * <span data-ttu-id="8cc5e-374">代替引数の `--id` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-374">Use replacement argument `--id`</span></span>
* <span data-ttu-id="8cc5e-375">ユーザー関連コマンドに `--id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-375">Added `--id` argument to user-related commands</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-376">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-376">SQL</span></span>

* <span data-ttu-id="8cc5e-377">マネージド インスタンス キーおよび TDE 保護機能の管理コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-377">Added management commands for managed instance keys and TDE protector</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-378">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-378">Storage</span></span>

* <span data-ttu-id="8cc5e-379">`storage remove` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-379">Added `storage remove` command</span></span>
* <span data-ttu-id="8cc5e-380">`storage blob update` での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-380">Fixed an issue with `storage blob update`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-381">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-381">VM</span></span>

* <span data-ttu-id="8cc5e-382">ゾーンの詳細を出力するための新しい API バージョンを使用するように `list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-382">Changed `list-skus` to use newer api-version to output zone details</span></span>
* <span data-ttu-id="8cc5e-383">`vmss create` の `--single-placement-group` の既定値を`false` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-383">Changed default of `--single-placement-group` to `false` for `vmss create`</span></span>
* <span data-ttu-id="8cc5e-384">`[snapshot|disk] create` において ZRS ストレージ SKU を選択する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-384">Added ability to select ZRS storage SKUs for `[snapshot|disk] create`</span></span>
* <span data-ttu-id="8cc5e-385">専用ホストをサポートするために、新しいコマンド グループ `vm host` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-385">Added new command group `vm host` to support dedicated hosts</span></span>
* <span data-ttu-id="8cc5e-386">VM 専用ホストを設定するためのパラメーター `--host` と `--host-group` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-386">Added parameters `--host` and `--host-group` on `vm create` to set VM dedicated host</span></span>

## <a name="july-16-2019"></a><span data-ttu-id="8cc5e-387">2019 年 7 月 16 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-387">July 16, 2019</span></span>

<span data-ttu-id="8cc5e-388">バージョン 2.0.69</span><span class="sxs-lookup"><span data-stu-id="8cc5e-388">Version 2.0.69</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-389">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-389">Appservice</span></span>

* <span data-ttu-id="8cc5e-390">ResourceGroupName または App の名前が無効な場合に適切なエラー メッセージを返すように `webapp identity` コマンドが変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-390">Changed `webapp identity` commands to return a proper error message if ResourceGroupName or App name are invalid</span></span>
* <span data-ttu-id="8cc5e-391">ResourceGroup が指定されなかった場合に numberOfSites の正しい値を返すように `webapp list` が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-391">Fixed `webapp list` to return the correct value for numberOfSites if no ResourceGroup was provided</span></span>
* <span data-ttu-id="8cc5e-392">`appservice plan create` と `webapp create` の副作用が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-392">Fixed side-effects of `appservice plan create` and `webapp create`</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-393">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-393">Core</span></span>

* <span data-ttu-id="8cc5e-394">`--subscription` が適用不可にもかかわらず表示される問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-394">Fixed issue where `--subscription` would appear despite being not applicable</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-395">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-395">Batch</span></span>

* <span data-ttu-id="8cc5e-396">[重大な変更] `batch pool node-agent-skus list` が `batch pool supported-images list` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-396">[BREAKING CHANGE] Replaced `batch pool node-agent-skus list` with `batch pool supported-images list`</span></span>
* <span data-ttu-id="8cc5e-397">`batch pool create network` の `--json-file` オプションを使用するときに、トラフィックのソース ポートに基づいてプールへのネットワーク アクセスをブロックするセキュリティ規則のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-397">Added support for security rules blocking network access to a pool based on the source port of the traffic when using the `--json-file` option of `batch pool create network`</span></span>
* <span data-ttu-id="8cc5e-398">`batch task create`の `--json-file` オプションを使用するときに、コンテナーの作業ディレクトリまたは Batch タスクの作業ディレクトリでタスクを実行するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-398">Added support for executing the task in the container working directory or in the Batch task working directory when using the `--json-file` option of `batch task create`</span></span>
* <span data-ttu-id="8cc5e-399">`batch pool create`の `--application-package-references` オプションが、既定値でのみ動作するというエラーが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-399">Fixed error in `--application-package-references` option of `batch pool create` where it would only work with defaults</span></span>

### <a name="eventhubs"></a><span data-ttu-id="8cc5e-400">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-400">Eventhubs</span></span>

* <span data-ttu-id="8cc5e-401">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-401">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-402">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-402">RDBMS</span></span>

* <span data-ttu-id="8cc5e-403">レプリカ作成コマンドでレプリカ SKU を指定するためのオプション パラメーターが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-403">Added optional parameter to specify replica SKU for create replica command</span></span>
* <span data-ttu-id="8cc5e-404">MySQL レプリカの作成で CI テストが失敗する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-404">Fixed the issue with CI test failure with creating MySQL replica</span></span>

### <a name="relay"></a><span data-ttu-id="8cc5e-405">リレー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-405">Relay</span></span>

* <span data-ttu-id="8cc5e-406">クライアント承認が無効になっているときのハイブリッド接続の問題が修正されました ([#8775](https://github.com/azure/azure-cli/issues/8775))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-406">Fixed issue with hybrid connection when client authroization disabled [#8775](https://github.com/azure/azure-cli/issues/8775)</span></span>
* <span data-ttu-id="8cc5e-407">パラメーター `--requires-transport-security` を `relay wcfrelay create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-407">Added parameter `--requires-transport-security` to `relay wcfrelay create`</span></span>

### <a name="servicebus"></a><span data-ttu-id="8cc5e-408">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-408">Servicebus</span></span>

* <span data-ttu-id="8cc5e-409">`authorizationrule`コマンドのパラメーター `--rights` の検証が追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-409">Added validation for parameter `--rights` of `authorizationrule` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-410">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-410">Storage</span></span>

* <span data-ttu-id="8cc5e-411">ストレージ アカウントの更新で Files AADDS を有効にします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-411">Enable Files AADDS for storage account update</span></span>
* <span data-ttu-id="8cc5e-412">修正された問題 `storage blob service-properties update --set`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-412">Fixed issue `storage blob service-properties update --set`</span></span>

## <a name="july-2-2019"></a><span data-ttu-id="8cc5e-413">2019 年 7 月 2 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-413">July 2, 2019</span></span>

<span data-ttu-id="8cc5e-414">バージョン 2.0.68</span><span class="sxs-lookup"><span data-stu-id="8cc5e-414">Version 2.0.68</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-415">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-415">Core</span></span>

* <span data-ttu-id="8cc5e-416">コマンド モジュールが再頒布可能な 1 つの Python コードに統合されました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-416">Command modules are now consolidated into a single Python distributable.</span></span> <span data-ttu-id="8cc5e-417">これにより、PyPI での多くの `azure-cli-` パッケージの直接使用が廃止されます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-417">This deprecates direct use of many `azure-cli-` packages on PyPI.</span></span>
  <span data-ttu-id="8cc5e-418">またこれにより、インストール サイズが削減され、`pip` 経由で直接インストールしたユーザーにのみ影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-418">This should reduce install size and only affect users who have directly installed via `pip`.</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-419">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-419">ACR</span></span>

* <span data-ttu-id="8cc5e-420">タスクへのタイマー トリガーのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-420">Added support for Timer Triggers to Task</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-421">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-421">Appservice</span></span>

* <span data-ttu-id="8cc5e-422">既定でアプリケーション インサイトを有効にするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-422">Changed `functionapp create` to enable application insights by default</span></span>
* <span data-ttu-id="8cc5e-423">[重大な変更] 非推奨の `functionapp devops-build` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-423">[BREAKING CHANGE] Removed deprecated `functionapp devops-build` command.</span></span>
  *  <span data-ttu-id="8cc5e-424">代わりに新しいコマンド `az functionapp devops-pipeline` を使用</span><span class="sxs-lookup"><span data-stu-id="8cc5e-424">Use the new command `az functionapp devops-pipeline` instead</span></span>
* <span data-ttu-id="8cc5e-425">Linux 従量課金プランの関数アプリのプラン サポートを `functionapp deployment config-zip` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-425">Added Linux Consumption function app plan support to `functionapp deployment config-zip`</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="8cc5e-426">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-426">Cosmos DB</span></span>

* <span data-ttu-id="8cc5e-427">ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-427">Added support for disabling TTL</span></span>

### <a name="dls"></a><span data-ttu-id="8cc5e-428">DLS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-428">DLS</span></span>

* <span data-ttu-id="8cc5e-429">ADLS バージョンを更新しました (0.0.45)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-429">Updated ADLS version (0.0.45)</span></span>

### <a name="feedback"></a><span data-ttu-id="8cc5e-430">フィードバック</span><span class="sxs-lookup"><span data-stu-id="8cc5e-430">Feedback</span></span>

* <span data-ttu-id="8cc5e-431">失敗した拡張機能コマンドを報告するときに、`az feedback` はインデックスからの拡張機能のプロジェクト/リポジトリの url にブラウザーを開こうとするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-431">When reporting a failed extension command, `az feedback` now attempts to open the browser to the project/repo url of the extension from the index</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-432">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-432">HDInsight</span></span>

* <span data-ttu-id="8cc5e-433">[重大な変更] `oms` コマンド グループ名を `monitor` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-433">[BREAKING CHANGE] Changed `oms` command group name to `monitor`</span></span>
* <span data-ttu-id="8cc5e-434">[重大な変更] `--http-password/-p` が必須パラメーターになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-434">[BREAKING CHANGE] Made `--http-password/-p` a required parameter</span></span> 
* <span data-ttu-id="8cc5e-435">`--cluster-admin-account` および `cluster-users-group-dns` パラメーター入力候補の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-435">Added completers for `--cluster-admin-account` and `cluster-users-group-dns` parameters completer</span></span> 
* <span data-ttu-id="8cc5e-436">`cluster-users-group-dns` パラメーターを `—esp` が存在するときに必要となるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-436">Changed `cluster-users-group-dns` parameter to be required when `—esp` is present</span></span>
* <span data-ttu-id="8cc5e-437">既存の引数自動オートコンプリートすべてにタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-437">Added a timeout for all existing argument auto-completers</span></span>
* <span data-ttu-id="8cc5e-438">リソース名をリソース id に変換する際のタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-438">Added a timeout for transforming resource name to resource id</span></span>
* <span data-ttu-id="8cc5e-439">任意のリソース グループからリソースを選択するようにオートコンプリートを変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-439">Changed Auto-completers to select resources from any resource group.</span></span> <span data-ttu-id="8cc5e-440">`-g` で指定されるリソース グループとは別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-440">It can be a different resource group than the one specified with `-g`</span></span>
* <span data-ttu-id="8cc5e-441">`hdinsight application create` コマンドで `--sub-domain-suffix` および `--disable_gateway_auth` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-441">Added support for `--sub-domain-suffix` and `--disable_gateway_auth` parameters in the `hdinsight application create` command</span></span>

### <a name="managed-services"></a><span data-ttu-id="8cc5e-442">マネージド サービス</span><span class="sxs-lookup"><span data-stu-id="8cc5e-442">Managed Services</span></span>

* <span data-ttu-id="8cc5e-443">プレビューにマネージド サービス コマンド モジュールを導入</span><span class="sxs-lookup"><span data-stu-id="8cc5e-443">Introducing managed service command module in preview</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-444">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-444">Profile</span></span>
* <span data-ttu-id="8cc5e-445">ログアウト コマンドの `--subscription` 引数を抑制</span><span class="sxs-lookup"><span data-stu-id="8cc5e-445">Suppress `--subscription` argument for logout command</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-446">RBAC</span><span class="sxs-lookup"><span data-stu-id="8cc5e-446">RBAC</span></span>

* <span data-ttu-id="8cc5e-447">[重大な変更] `create-for-rbac` の `--password` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-447">[BREAKING CHANGE] Removed `--password` argument for `create-for-rbac`</span></span>
* <span data-ttu-id="8cc5e-448">AAD グラフ サーバー レプリケーションの待機時間によって発生する断続的なエラーを回避するために `--assignee-principal-type` パラメーターを `create` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-448">Added `--assignee-principal-type` parameter to `create` command to avoid intermittent failures caused by AAD graph server replication latency</span></span>
* <span data-ttu-id="8cc5e-449">所有オブジェクトの一覧表示時の `ad signed-in-user` のクラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-449">Fixed a crash in `ad signed-in-user` when listing owned objects</span></span>
* <span data-ttu-id="8cc5e-450">`ad sp` によってサービス プリンシパルから適切なアプリケーションが検出されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-450">Fixed issue where `ad sp` would not find the right application from a service principal</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-451">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-451">RDBMS</span></span>

* <span data-ttu-id="8cc5e-452">MariaDB のレプリケーション サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-452">Added support for replication for MariaDB</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-453">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-453">SQL</span></span>

* <span data-ttu-id="8cc5e-454">`sql db create --sample-name` に使用できる値を文書化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-454">Documented allowed values for `sql db create --sample-name`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-455">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-455">Storage</span></span>

* <span data-ttu-id="8cc5e-456">`--as-user` を使用した `storage blob generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-456">Added user delegation SAS token support with `--as-user` to `storage blob generate-sas`</span></span> 
* <span data-ttu-id="8cc5e-457">`--as-user` を使用した `storage container generate-sas` に対するユーザーの委任 SAS トークンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-457">Added user delegation SAS token support with `--as-user` to `storage container generate-sas`</span></span> 

### <a name="vm"></a><span data-ttu-id="8cc5e-458">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-458">VM</span></span>

* <span data-ttu-id="8cc5e-459">`--no-wait` による実行時に `vmss create` によってエラー メッセージが返されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-459">Fixed bug where `vmss create` returns an error message when run with `--no-wait`</span></span>
* <span data-ttu-id="8cc5e-460">`vmss create --single-placement-group` のクライアント側の検証を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-460">Removed client-side validation for `vmss create --single-placement-group`.</span></span> <span data-ttu-id="8cc5e-461">`--single-placement-group` が `true` に設定され、`--instance-count` が 100 より大きいか、可用性ゾーンが指定されていても失敗にはならず、この検証はコンピューティング サービスに任されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-461">Does not fail if `--single-placement-group` is set to `true` and`--instance-count` is greater than 100 or availability zones are specified, but leaves this validation to the compute service</span></span>
* <span data-ttu-id="8cc5e-462">`--latest` と共に使用したときに `[vm|vmss] extension image list` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-462">Fixed bug where `[vm|vmss] extension image list` fails when used with `--latest`</span></span>


## <a name="june-18-2019"></a><span data-ttu-id="8cc5e-463">2019 年 6 月 18 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-463">June 18, 2019</span></span>

<span data-ttu-id="8cc5e-464">バージョン 2.0.67</span><span class="sxs-lookup"><span data-stu-id="8cc5e-464">Version 2.0.67</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-465">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-465">Core</span></span>

<span data-ttu-id="8cc5e-466">このリリースでは、新しい [プレビュー] タグが導入され、コマンド グループ、コマンド、または引数がプレビュー状態である場合に、お客様により明確に通知できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-466">This release introduces a new [Preview] tag to more clearly communicate to customers when a command group, command or argument is in preview status.</span></span> <span data-ttu-id="8cc5e-467">以前は、これはヘルプ テキストで通知されていたか、コマンド モジュールのバージョン番号によって暗黙的に通知されていました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-467">This was previously called out in help text or communicated implicitly by the command module version number.</span></span>
<span data-ttu-id="8cc5e-468">CLI では、将来、個々のパッケージのバージョン番号が削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-468">The CLI will be removing version numbers for individual packages in the future.</span></span> <span data-ttu-id="8cc5e-469">コマンドがプレビュー状態の場合は、そのすべての引数もプレビュー状態です。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-469">If a command is in preview, all of its arguments are as well.</span></span> <span data-ttu-id="8cc5e-470">コマンド グループにプレビュー状態のラベルが付いている場合、すべてのコマンドと引数もプレビュー状態と見なされます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-470">If a command group is labeled as being in preview, then all commands and arguments are considered to be in preview as well.</span></span>

<span data-ttu-id="8cc5e-471">この変更の結果、このリリースでは、一部のコマンド グループが "突然" プレビュー状態になったように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-471">As a result of this change, several command groups may seem to "suddenly" appear to be in a preview status with this release.</span></span> <span data-ttu-id="8cc5e-472">ほとんどのパッケージがプレビュー状態にあったのですが、このリリースでは一般提供と見なされていることがその真相です</span><span class="sxs-lookup"><span data-stu-id="8cc5e-472">What actually happened is that most packages were in a preview status, but are being deemed GA with this release</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-473">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-473">ACR</span></span>
* <span data-ttu-id="8cc5e-474">'acr check-health' コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-474">Added 'acr check-health' command</span></span>
* <span data-ttu-id="8cc5e-475">AAD トークンおよび外部コマンドの取得に関するエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-475">Improved error handling for AAD tokens and for retrieving external commands</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-476">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-476">ACS</span></span>
* <span data-ttu-id="8cc5e-477">非推奨の ACS コマンドがヘルプ ビューで非表示になりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-477">Deprecated ACS commands are now hidden from help view</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-478">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-478">AMS</span></span>
* <span data-ttu-id="8cc5e-479">[重大な変更] archive-window-length および key-frame-interval-duration の ISO 8601 時間文字列を返すように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-479">[BREAKING CHANGE] Changed to return ISO 8601 time strings for archive-window-length and key-frame-interval-duration</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-480">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-480">AppService</span></span>
* <span data-ttu-id="8cc5e-481">`webapp deleted list` および `webapp deleted restore` に対してロケーション ベースのルーティングを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-481">Added location based routing for `webapp deleted list` and `webapp deleted restore`</span></span>
* <span data-ttu-id="8cc5e-482">Azure Cloud Shell で Web アプリのログに記録されたターゲット URL ("You can launch the app at...") がクリックできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-482">Fixed issue where webapp up logged target URL ("You can launch the app at...") was not clickable in Azure Cloud Shell</span></span>
* <span data-ttu-id="8cc5e-483">一部の SKU でのアプリ作成が AlwaysOn エラーで失敗するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-483">Fixed an issue where creating apps with the some SKUs was failing with an AlwaysOn error</span></span>
* <span data-ttu-id="8cc5e-484">`[appservice|webapp] create` に事前検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-484">Added pre-validation to `[appservice|webapp] create`</span></span>
* <span data-ttu-id="8cc5e-485">正しい actionHostName を使用するように `[webapp|functionapp] traffic-routing` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-485">Fixed `[webapp|functionapp] traffic-routing` to use the correct actionHostName</span></span>
* <span data-ttu-id="8cc5e-486">`functionapp` コマンドにスロット サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-486">Added slot support to `functionapp` commands</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-487">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-487">Batch</span></span>
* <span data-ttu-id="8cc5e-488">共有キー認証の過度のエラー報告による AAD 認証の回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-488">Fixed AAD auth regression caused by over-aggressive error reporting for Shared Key Auth</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-489">BatchAI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-489">BatchAI</span></span>
* <span data-ttu-id="8cc5e-490">BatchAI コマンドが非推奨となり、非表示になりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-490">BatchAI commands are now deprecated and hidden</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-491">BotService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-491">BotService</span></span>
* <span data-ttu-id="8cc5e-492">v3 SDK をサポートするコマンドに "廃止されたサポート"/"保守モード" 警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-492">Added "discontinued support"/"maintenance mode" warning messages for commands that support the v3 SDK</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-493">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-493">CosmosDB</span></span>
* <span data-ttu-id="8cc5e-494">[非推奨] `cosmosdb list-keys` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-494">[DEPRECATED] Deprecated the `cosmosdb list-keys` command</span></span>
* <span data-ttu-id="8cc5e-495">`cosmosdb keys list` コマンドを追加しました。`cosmosdb list-keys` に置き換わるものです</span><span class="sxs-lookup"><span data-stu-id="8cc5e-495">Added the `cosmosdb keys list` command - replaces `cosmosdb list-keys`</span></span>
* <span data-ttu-id="8cc5e-496">`cosmsodb create/update`:"isZoneRedundant" プロパティを設定できるように --location の新しいフォーマットを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-496">`cosmsodb create/update`: Added new format for --location to allow setting "isZoneRedundant" property.</span></span> <span data-ttu-id="8cc5e-497">古いフォーマットを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-497">Deprecated old format</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8cc5e-498">EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-498">EventGrid</span></span>
* <span data-ttu-id="8cc5e-499">ドメイン CRUD 操作のための `eventgrid domain` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-499">Added `eventgrid domain` commands for domain CRUD operations</span></span>
* <span data-ttu-id="8cc5e-500">ドメイン トピック CRUD 操作のための `eventgrid domain topic` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-500">Added `eventgrid domain topic` commands for domain topics CRUD operations</span></span>
* <span data-ttu-id="8cc5e-501">OData 構文を使用して結果をフィルタリングするための `--odata-query` 引数を `eventgrid [topic|event-subscription] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-501">Added `--odata-query` argument to `eventgrid [topic|event-subscription] list` for filtering results using OData syntax</span></span>
* <span data-ttu-id="8cc5e-502">`event-subscription create/update`:`--endpoint-type` パラメーターの新しい値として servicebusqueue を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-502">`event-subscription create/update`: Added servicebusqueue as new values for the `--endpoint-type` parameter</span></span>
* <span data-ttu-id="8cc5e-503">[重大な変更] `eventgrid event-subscription [create|update]` での `--included-event-types All` のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-503">[BREAKING CHANGE] Removed support for `--included-event-types All` with `eventgrid event-subscription [create|update]`</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-504">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-504">HDInsight</span></span>
* <span data-ttu-id="8cc5e-505">`hdinsight create` コマンドでの `--ssh-public-key` パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-505">Added support for `--ssh-public-key` parameter in `hdinsight create` command</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-506">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-506">IoT</span></span>
* <span data-ttu-id="8cc5e-507">承認ポリシー キーの再生成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-507">Added support to regenerate authorization policy keys</span></span>
* <span data-ttu-id="8cc5e-508">DigitalTwin リポジトリ プロビジョニング サービスの SDK およびサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-508">Added SDK and support for DigitalTwin Repository Provisioning Service</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-509">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-509">Network</span></span>
* <span data-ttu-id="8cc5e-510">Nat Gateway に対するゾーン サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-510">Added Zone support for Nat Gateway</span></span>
* <span data-ttu-id="8cc5e-511">`network list-service-tags` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-511">Added command `network list-service-tags`</span></span>
* <span data-ttu-id="8cc5e-512">ユーザーがワイルドカード A レコードをインポートできない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-512">Fixed issue with `dns zone import` where users could not import wildcard A records</span></span>
* <span data-ttu-id="8cc5e-513">特定のリージョンでフロー ロギングを有効にできない `watcher flow-log configure` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-513">Fixed issue with `watcher flow-log configure` where flow logging could not be enabled in certain regions</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-514">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-514">Resource</span></span>
* <span data-ttu-id="8cc5e-515">REST 呼び出しを行うための `az rest` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-515">Added `az rest` command for making REST calls</span></span>
* <span data-ttu-id="8cc5e-516">リソース グループまたはサブスクリプション レベル`--scope` で `policy assignment list` を使用する場合のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-516">Fixed error when using `policy assignment list` with a resource group or subscription level `--scope`</span></span>

### <a name="servicebus"></a><span data-ttu-id="8cc5e-517">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-517">ServiceBus</span></span>
* <span data-ttu-id="8cc5e-518">`servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319) での問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-518">Fixed issue with `servicebus topic create --max-size` [#9319](https://github.com/azure/azure-cli/issues/9319)</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-519">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-519">SQL</span></span>
* <span data-ttu-id="8cc5e-520">`--location` を `sql [server|mi] create` のオプションに変更しました - 指定されていない場合、リソース グループの場所を使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-520">Changed `--location` to be optional for `sql [server|mi] create` - uses resource group location if not specified</span></span>
* <span data-ttu-id="8cc5e-521">`sql db list-editions --available` の "'NoneType' object is not iterable" エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-521">Fixed "'NoneType' object is not iterable" error for `sql db list-editions --available`</span></span>

### <a name="sqlvm"></a><span data-ttu-id="8cc5e-522">SQLVm</span><span class="sxs-lookup"><span data-stu-id="8cc5e-522">SQLVm</span></span>
* <span data-ttu-id="8cc5e-523">[破壊的変更] `--license-type` パラメーターを必要とするように `sql vm create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-523">[BREAKING CHNAGE] Changed `sql vm create` to require `--license-type` parameter</span></span>
* <span data-ttu-id="8cc5e-524">sql vm の作成または更新時に SQL イメージ SKU を設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-524">Changed to allow setting SQL image SKU when creating or updating a sql vm</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-525">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-525">Storage</span></span>
* <span data-ttu-id="8cc5e-526">`storage container generate-sas` のアカウント キーが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-526">Fixed issue with missing account key for `storage container generate-sas`</span></span>
* <span data-ttu-id="8cc5e-527">Linux での `storage blob sync` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-527">Fixed issue with `storage blob sync` on Linux</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-528">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-528">VM</span></span>
* <span data-ttu-id="8cc5e-529">[プレビュー] VM イメージを構築するための `vm image template` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-529">[PREVIEW] Added `vm image template` commands to build VM images</span></span>

## <a name="june-4-2019"></a><span data-ttu-id="8cc5e-530">2019 年 6 月 4 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-530">June 4, 2019</span></span>

<span data-ttu-id="8cc5e-531">バージョン 2.0.66</span><span class="sxs-lookup"><span data-stu-id="8cc5e-531">Version 2.0.66</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-532">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-532">Core</span></span>
* <span data-ttu-id="8cc5e-533">`--output yaml` が `--query` と共に使用された場合、コマンドが正常に実行されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-533">Fixed bug where commands fail if `--output yaml` is used with `--query`</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-534">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-534">ACR</span></span>
* <span data-ttu-id="8cc5e-535">Buildpack を使用して簡単なビルド タスクを作成するための 'acr pack' コマンド グループを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-535">Added 'acr pack' command group for creating quick build Tasks using Buildpacks.</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-536">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-536">ACS</span></span>
* <span data-ttu-id="8cc5e-537">AKS kube-dashboard アドオンを有効化/無効化できるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-537">Allow enabling/disabling AKS kube-dashboard addon</span></span>
* <span data-ttu-id="8cc5e-538">サブスクリプションが Azure Red Hat OpenShift を使用するようにホワイトリストに登録されていない場合、わかりやすいメッセージが出力されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-538">Print a friendly message when the subscription is not whitelisted to use Azure Red Hat OpenShift</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-539">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-539">Batch</span></span>
* <span data-ttu-id="8cc5e-540">アカウント \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\] にログインしていないときのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-540">Improved error handling when not logged in to an account \[[#9165](https://github.com/Azure/azure-cli/issues/9165)\]\[[#8978](https://github.com/Azure/azure-cli/issues/8978)\]</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-541">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-541">IoT</span></span>
* <span data-ttu-id="8cc5e-542">手動フェールオーバーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-542">Added support for manual failover</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-543">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-543">Network</span></span>
* <span data-ttu-id="8cc5e-544">カスタム WAF 規則をサポートするように `network application-gateway waf-policy` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-544">Added `network application-gateway waf-policy` commands to support custom WAF rules.</span></span>
* <span data-ttu-id="8cc5e-545">`--waf-policy` 引数と `--max-capacity` 引数を `network application-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-545">Added `--waf-policy` and `--max-capacity` arguments to `network application-gateway [create|update]`</span></span> 

### <a name="resource"></a><span data-ttu-id="8cc5e-546">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-546">Resource</span></span>
* <span data-ttu-id="8cc5e-547">使用できる TTY がない場合の `deployment create` からのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-547">Improved error message from `deployment create` when there is no TTY available</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-548">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-548">Role</span></span>
* <span data-ttu-id="8cc5e-549">ヘルプ テキストを更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-549">Updated help text.</span></span>

### <a name="compute"></a><span data-ttu-id="8cc5e-550">Compute</span><span class="sxs-lookup"><span data-stu-id="8cc5e-550">Compute</span></span>
* <span data-ttu-id="8cc5e-551">データディスク LUN が 0 から始まらないまたは番号をスキップするマネージド イメージの VM 用の `vm create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-551">Added support to `vm create` for VMs from a managed image with data-disk luns that do not start from 0 or that skip numbers</span></span>

## <a name="may-21-2019"></a><span data-ttu-id="8cc5e-552">2019 年 5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-552">May 21, 2019</span></span>

<span data-ttu-id="8cc5e-553">バージョン 2.0.65</span><span class="sxs-lookup"><span data-stu-id="8cc5e-553">Version 2.0.65</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-554">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-554">Core</span></span>
* <span data-ttu-id="8cc5e-555">認証エラーのより有意義なフィードバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-555">Added better feedback for authentication errors</span></span>
* <span data-ttu-id="8cc5e-556">CLI でそのコア バージョンと互換性がない拡張機能が読み込まれる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-556">Fixed issue where the CLI would load extensions that were not compatible with its core version</span></span>
* <span data-ttu-id="8cc5e-557">`clouds.config` が破損したときの起動時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-557">Fixed issue with launching when `clouds.config` is corrupted</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-558">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-558">ACR</span></span>
* <span data-ttu-id="8cc5e-559">タスクに対するマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-559">Added support for Managed Identities to Tasks</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-560">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-560">ACS</span></span>
* <span data-ttu-id="8cc5e-561">お客様の AAD クライアントでの使用時の `openshift create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-561">Fixed `openshift create` command when used with customer AAD client</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-562">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-562">AppService</span></span>
* <span data-ttu-id="8cc5e-563">[非推奨] `functionapp devops-build` コマンドを非推奨にしました - 次のリリースから削除されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-563">[DEPRECATED] Deprecated `functionapp devops-build` command - will be removed in next release</span></span>
* <span data-ttu-id="8cc5e-564">詳細モードで Azure DevOps からビルド ログをフェッチするように `functionapp devops-pipeline` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-564">Changed `functionapp devops-pipeline` to fetch build log from Azure DevOps in verbose mode</span></span>
* <span data-ttu-id="8cc5e-565">[重大な変更] `--use_local_settings` フラグを `functionapp devops-pipeline` コマンドから削除しました (操作なし)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-565">[BREAKING CHANGE] Removed `--use_local_settings` flag from `functionapp devops-pipeline` command - was a no-op</span></span>
* <span data-ttu-id="8cc5e-566">`--logs` が使用されていないときに、JSON 出力を返すように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-566">Changed `webapp up` to return JSON output if `--logs` is not used</span></span>
* <span data-ttu-id="8cc5e-567">`webapp up` 用のローカル構成に既定のリソースを書き込むためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-567">Added support for writing default resources to local config for `webapp up`</span></span>
* <span data-ttu-id="8cc5e-568">`--location` 引数を使用しないでアプリを再デプロイするために `webapp up` にサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-568">Added support to `webapp up` for redeploying an app without using the `--location` argument</span></span>
* <span data-ttu-id="8cc5e-569">SKU 値が機能しないため Linux Free SKU ASP 作成が無料で使用される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-569">Fixed an issue where for Linux Free SKU ASP creation use Free as SKU value was not working</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-570">BotService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-570">BotService</span></span>
* <span data-ttu-id="8cc5e-571">コマンドの `--lang` パラメーターに大文字小文字のすべてが許可されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-571">Changed to allow all casing for `--lang` parameters for commands</span></span>
* <span data-ttu-id="8cc5e-572">コマンド モジュールの説明を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-572">Updated description for command module</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-573">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-573">Consumption</span></span>
* <span data-ttu-id="8cc5e-574">`consumption usage list --billing-period-name` の実行時に存在しない必須パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-574">Added missing required parameter when running `consumption usage list --billing-period-name`</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-575">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-575">IoT</span></span>
* <span data-ttu-id="8cc5e-576">すべてのキーを一覧表示するようサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-576">Added support to list all keys</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-577">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-577">Network</span></span>
* [重大な変更]: Removed `network interface-endpoints` command group - use `network private-endpoints`
[BREAKING CHANGE]: Removed `network interface-endpoints` command group - use `network private-endpoints` 
* <span data-ttu-id="8cc5e-579">NAT ゲートウェイへのアタッチ用に `--nat-gateway` 引数を `network vnet subnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-579">Added `--nat-gateway` argument to `network vnet subnet [create|update]` for attaching to a NAT gateway</span></span>
* <span data-ttu-id="8cc5e-580">レコード名がレコードの種類と一致しない `dns zone import` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-580">Fixed issue with `dns zone import` where record names could not match a record type</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-581">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-581">RDBMS</span></span>
* <span data-ttu-id="8cc5e-582">geo レプリケーション用の postgres と mysql のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-582">Added postgres and mysql support for geo replication</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-583">RBAC</span><span class="sxs-lookup"><span data-stu-id="8cc5e-583">RBAC</span></span>
* <span data-ttu-id="8cc5e-584">管理グループ スコープのサポートを `role assignment` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-584">Added support for management group scope to `role assignment`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-585">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-585">Storage</span></span>
* <span data-ttu-id="8cc5e-586">`storage blob sync`: ストレージ BLOB 用の同期コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="8cc5e-586">`storage blob sync`: add sync command for storage blob</span></span>

### <a name="compute"></a><span data-ttu-id="8cc5e-587">Compute</span><span class="sxs-lookup"><span data-stu-id="8cc5e-587">Compute</span></span>
* <span data-ttu-id="8cc5e-588">VM のコンピューター名設定用に `--computer-name` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-588">Added `--computer-name` to `vm create` for setting a VM's computer name</span></span>
* <span data-ttu-id="8cc5e-589">`[vm|vmss] create` について `--ssh-key-value` を `--ssh-key-values` に変更しました。複数の ssh 公開キーの値またはパスが受け入れられるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-589">Renamed `--ssh-key-value` renamed to `--ssh-key-values` for `[vm|vmss] create` - can now accept multiple ssh public key values or paths</span></span>
  * <span data-ttu-id="8cc5e-590">__メモ__:これは、破壊的変更 "**ではありません**" - `--ssh-key-values` にのみ一致するため `--ssh-key-value` は 適切に解析されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-590">__Note__: This is **not** a breaking change - `--ssh-key-value` will be parsed correctly as it matches only `--ssh-key-values`</span></span>
* <span data-ttu-id="8cc5e-591">`ppg create` の `--type` 引数をオプションに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-591">Changed the `--type` argument of `ppg create` to be optional</span></span>

## <a name="may-6-2019"></a><span data-ttu-id="8cc5e-592">2019 年 5 月 6 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-592">May 6, 2019</span></span>

<span data-ttu-id="8cc5e-593">バージョン 2.0.64</span><span class="sxs-lookup"><span data-stu-id="8cc5e-593">Version 2.0.64</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-594">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-594">ACS</span></span>
* <span data-ttu-id="8cc5e-595">[重大な変更] `--fqdn` フラグを `openshift` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-595">[BREAKING CHANGE] Removed `--fqdn` flag on `openshift` commands</span></span>
* <span data-ttu-id="8cc5e-596">Azure Red Hat Openshift GA API Version を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-596">Changed to use Azure Red Hat Openshift GA API Version</span></span>
* <span data-ttu-id="8cc5e-597">`customer-admin-group-id` フラグを `openshift create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-597">Added `customer-admin-group-id` flag to `openshift create`</span></span>
* <span data-ttu-id="8cc5e-598">[GA] `aks create` オプション `--network-policy` から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-598">[GA] Removed `(PREVIEW)` from `aks create` option `--network-policy`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-599">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-599">Appservice</span></span>
* <span data-ttu-id="8cc5e-600">[非推奨] `functionapp devops-build` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-600">[DEPRECATED] Deprecated `functionapp devops-build` command</span></span>
  * <span data-ttu-id="8cc5e-601">名前を `functionapp devops-pipeline` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-601">Renamed to `functionapp devops-pipeline`</span></span>
* <span data-ttu-id="8cc5e-602">`webapp up` が失敗する原因となっていた問題を修正し、CloudShell の正しいユーザー名が取得されるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-602">Fixed getting the correct username for cloudshell which was causing `webapp up` to fail</span></span>
* <span data-ttu-id="8cc5e-603">サポートされる appserviceplans を反映するために `appservice plan --sku` のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-603">Updated `appservice plan --sku` documentation updated to reflect the supported appserviceplans</span></span>
* <span data-ttu-id="8cc5e-604">リソース グループとプランの省略可能な引数を `webapp up` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-604">Added optional arguments for resource group and plan to `webapp up`</span></span>
* <span data-ttu-id="8cc5e-605">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を尊重するために、`webapp ssh` に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-605">Added support to `webapp ssh` to respect `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>
* <span data-ttu-id="8cc5e-606">Linux の無料 SKU に `appserviceplan create` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-606">Added `appserviceplan create` support for Linux Free SKU</span></span>
* <span data-ttu-id="8cc5e-607">kudu コールド スタートを処理するように `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting を設定した後に、`webapp up` が 30 秒間スリープ状態になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-607">Changed `webapp up` to have a 30s sleep after setting `SCM_DO_BUILD_DURING_DEPLOYMENT=true` appsetting to handle kudu cold start</span></span>
* <span data-ttu-id="8cc5e-608">Windows 上で `functionapp create` を実行するために `powershell` ランタイムに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-608">Added support for `powershell` runtime to `functionapp create` on Windows</span></span>
* <span data-ttu-id="8cc5e-609">`create-remote-connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-609">Added `create-remote-connection` command</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-610">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-610">Batch</span></span>
* <span data-ttu-id="8cc5e-611">`--application-package-references` オプションの検証コントロールのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-611">Fixed bug in validator for `--application-package-references` options</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-612">Botservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-612">Botservice</span></span>
* <span data-ttu-id="8cc5e-613">[重大な変更] 空の Web アプリ ボットを既定で作成するように `bot create -v v4 -k webapp` を変更しました (つまり、アプリ サービスにデプロイされるボットはありません)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-613">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to create an empty Web App Bot by default (i.e. no bot is deployed to the App Service)</span></span>
* <span data-ttu-id="8cc5e-614">`-v v4` により以前の動作を使用するように `--echo` フラグを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-614">Added `--echo` flag to `bot create` to use the old behavior with `-v v4`</span></span>
* <span data-ttu-id="8cc5e-615">[重大な変更] `--version` の既定値を `v4` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-615">[BREAKING CHANGE] Changed the default value of  `--version` to `v4`</span></span>
  * <span data-ttu-id="8cc5e-616">__注:__ `bot prepare-publish` ではその以前の既定値を引き続き使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-616">__NOTE:__ `bot prepare-publish` still uses the its old default</span></span>
* <span data-ttu-id="8cc5e-617">[重大な変更] 既定値が `Csharp` にならないように `--lang` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-617">[BREAKING CHANGE] Changed `--lang` to no longer default to `Csharp`.</span></span> <span data-ttu-id="8cc5e-618">コマンドで `--lang` が必要で、これが指定されないと、コマンドでエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-618">If the command requires `--lang` and it is not provided, the command will now error out</span></span>
* <span data-ttu-id="8cc5e-619">[重大な変更] `bot create` が必要になるように、および `ad app create` を通じて作成されるように `--appid` と `--password` 引数を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-619">[BREAKING CHANGE] Changed the `--appid` and `--password` args for `bot create` to be required and can now be created via `ad app create`</span></span>
* <span data-ttu-id="8cc5e-620">`--appid` および `--password` 検証を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-620">Added `--appid` and `--password` validation</span></span>
* <span data-ttu-id="8cc5e-621">[重大な変更] ストレージ アカウントまたは Application Insights を作成または使用しないように `bot create -v v4` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-621">[BREAKING CHANGE] Changed `bot create -v v4` to not create or use a Storage Account or Application Insights</span></span>
* <span data-ttu-id="8cc5e-622">[重大な変更] Application Insights を使用できるリージョンを必要とするように `bot create -v v3` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-622">[BREAKING CHANGE] Changed `bot create -v v3` to require a region where Application Insights is available</span></span>
* <span data-ttu-id="8cc5e-623">[重大な変更] ボットの特定のプロパティのみに影響するように `bot update` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-623">[BREAKING CHANGE] Changed `bot update` to now affect only specific properties of a bot</span></span>
* <span data-ttu-id="8cc5e-624">[重大な変更] `Node` の代わりに `Javascript` を受け入れるように `--lang` フラグを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-624">[BREAKING CHANGE] Changed `--lang` flags to accept `Javascript` instead of `Node`</span></span>
* <span data-ttu-id="8cc5e-625">[重大な変更] 許可された `--lang` 値としての `Node` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-625">[BREAKING CHANGE] Removed `Node` as an allowed `--lang` value</span></span>
* <span data-ttu-id="8cc5e-626">[重大な変更] `SCM_DO_BUILD_DURING_DEPLOYMENT` が true に設定されないように `bot create -v v4 -k webapp` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-626">[BREAKING CHANGE] Changed `bot create -v v4 -k webapp` to no longer set `SCM_DO_BUILD_DURING_DEPLOYMENT` to true.</span></span> <span data-ttu-id="8cc5e-627">Kudu を通じたすべてのデプロイがその既定の動作に従って動作します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-627">All deployments through Kudu will act according to their default behavior</span></span>
* <span data-ttu-id="8cc5e-628">`.bot` ファイルのないボットで言語固有の構成ファイルが、ボット用のアプリケーション設定からの値により作成されるように `bot download` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-628">Changed `bot download` for bots without `.bot` files to create the language-specific configuration file with values from the Application Settings for the bot</span></span>
* <span data-ttu-id="8cc5e-629">`bot prepare-deploy` に `Typescript` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-629">Added `Typescript` support to `bot prepare-deploy`</span></span>
* <span data-ttu-id="8cc5e-630">`--code-dir` に `package.json` が含まれない場合に備えて `Javascript` および `Typescript` ボット用に `bot prepare-deploy` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-630">Added warning message to `bot prepare-deploy` for `Javascript` and `Typescript` bots for when `--code-dir` does not contain `package.json`</span></span>
* <span data-ttu-id="8cc5e-631">成功した場合に `true` を返すように `bot prepare-deploy` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-631">Changed `bot prepare-deploy` to return `true` if successful</span></span>
* <span data-ttu-id="8cc5e-632">詳細ログ記録を `bot prepare-deploy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-632">Added verbose logging to `bot prepare-deploy`</span></span>
* <span data-ttu-id="8cc5e-633">さらに多くの使用可能な Application Insights リージョンを `az bot create -v v3` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-633">Added more available Application Insights regions to `az bot create -v v3`</span></span>

### <a name="configure"></a><span data-ttu-id="8cc5e-634">構成</span><span class="sxs-lookup"><span data-stu-id="8cc5e-634">Configure</span></span>
* <span data-ttu-id="8cc5e-635">フォルダー ベースの引数の既定値の構成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-635">Added support for folder based argument default value configurations</span></span>

### <a name="eventhubs"></a><span data-ttu-id="8cc5e-636">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-636">Eventhubs</span></span>
* <span data-ttu-id="8cc5e-637">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-637">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="8cc5e-638">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-638">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-639">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-639">Network</span></span>
* <span data-ttu-id="8cc5e-640">[重大な変更] `vnet [create|update]` 用に `--cache` 引数を `--defer` に置き換えました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-640">[BREAKING CHANGE] Replaced `--cache` arugment with `--defer` for `vnet [create|update]`</span></span> 

### <a name="policy-insights"></a><span data-ttu-id="8cc5e-641">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="8cc5e-641">Policy Insights</span></span>
* <span data-ttu-id="8cc5e-642">リソースに関するポリシー評価の詳細にクエリを実行するために `--expand PolicyEvaluationDetails` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-642">Added support for `--expand PolicyEvaluationDetails` to query policy evaluation details on the resource</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-643">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-643">Role</span></span>
* <span data-ttu-id="8cc5e-644">[非推奨] `create-for-rbac` '--password' 引数を非表示にするように変更しました。サポートは 2019 年 5 月に削除されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-644">[DEPRECATED] Changed `create-for-rbac` hide '--password' argument - support will be removed in May 2019</span></span>

### <a name="service-bus"></a><span data-ttu-id="8cc5e-645">Service Bus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-645">Service Bus</span></span>
* <span data-ttu-id="8cc5e-646">`namespace network-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-646">Added `namespace network-rule` commands</span></span>
* <span data-ttu-id="8cc5e-647">ネットワーク ルールの `--default-action` 引数を `namespace [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-647">Added `--default-action` argument for network rules to `namespace [create|update]`</span></span>
* <span data-ttu-id="8cc5e-648">Premium SKU で値 10、20、40、および 80 GB の `--max-size` サポートを許可するように `topic [create|update]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-648">Fixed `topic [create|update]` to allow `--max-size` support for 10, 20, 40 and 80GB values with premium SKU</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-649">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-649">SQL</span></span>
* <span data-ttu-id="8cc5e-650">`sql virtual-cluster [list|show|delete]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-650">Added `sql virtual-cluster [list|show|delete]` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-651">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-651">VM</span></span>
* <span data-ttu-id="8cc5e-652">VMSS VM インスタンスの保護ポリシーへの更新を有効にするように `--protect-from-scale-in` および `--protect-from-scale-set-actions` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-652">Added `--protect-from-scale-in` and `--protect-from-scale-set-actions` to `vmss update` to enable updates to the protection policy of VMSS VM instances</span></span>
* <span data-ttu-id="8cc5e-653">VMSS VM インスタンスの汎用的な更新を有効にするように `--instance-id` を `vmss update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-653">Added `--instance-id` to `vmss update` to enable generic update of VMSS VM instances</span></span>
* <span data-ttu-id="8cc5e-654">`--instance-id` を `vmss wait` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-654">Added `--instance-id` to `vmss wait`</span></span>
* <span data-ttu-id="8cc5e-655">近接通信配置グループの管理用に新しい `ppg` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-655">Added new `ppg` command group for managing Proximity Placement Groups</span></span>
* <span data-ttu-id="8cc5e-656">PPG の管理用に `--ppg` を `[vm|vmss] create` および `vm availability-set create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-656">Added `--ppg` to `[vm|vmss] create` and `vm availability-set create` for managing PPGs</span></span>
* <span data-ttu-id="8cc5e-657">`--hyper-v-generation` パラメーターを `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-657">Added `--hyper-v-generation` parameter to `image create`</span></span>

## <a name="april-23-2019"></a><span data-ttu-id="8cc5e-658">2019 年 4 月 23 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-658">April 23, 2019</span></span>

<span data-ttu-id="8cc5e-659">バージョン 2.0.63</span><span class="sxs-lookup"><span data-stu-id="8cc5e-659">Version 2.0.63</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-660">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-660">ACS</span></span>
* <span data-ttu-id="8cc5e-661">重複する値の上書きを求めるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-661">Changed `aks get-credentials` to prompt to overwrite duplicated values</span></span>
* <span data-ttu-id="8cc5e-662">Dev Spaces コマンド "aks use-dev-spaces" および "aks remove-dev-spaces" から `(PREVIEW)` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-662">Removed `(PREVIEW)` from Dev Spaces commands "aks use-dev-spaces" and "aks remove-dev-spaces"</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-663">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-663">AMS</span></span>
* <span data-ttu-id="8cc5e-664">資産およびアカウント フィルターの更新プログラムによりバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-664">Fixed bug with asset and account filters update</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-665">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-665">AppService</span></span>
* <span data-ttu-id="8cc5e-666">ASE のサポートと `webapp ssh` へのタイムアウトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-666">Added support for ASE and timeout to `webapp ssh`</span></span>
* <span data-ttu-id="8cc5e-667">Github リポジトリから関数アプリへ CI CD を確立するためのサポートを Azure DevOps パイプラインに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-667">Added support for establishing CI CD to an Azure DevOps pipeline from a Github repository to Function apps</span></span>
* <span data-ttu-id="8cc5e-668">Github 個人用アクセス トークンを受け入れるために、`functionapp devops-build create` に `--github-pat` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-668">Added `--github-pat` argument to `functionapp devops-build create` to accept Github personal access token</span></span>
* <span data-ttu-id="8cc5e-669">functionapp ソース コード を含む Github リポジトリを受け入れるために、`functionapp devops-build create` に `--github-repository` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-669">Added `--github-repository` argument to `functionapp devops-build create` to accept Github repository that contains a functionapp source code</span></span>
* <span data-ttu-id="8cc5e-670">`az webapp up --logs` がエラーで失敗し、既定の .NETCORE バージョンを 2.1 に更新する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-670">Fixed issue where `az webapp up --logs` was failing with a error and updating default .NETCORE version to 2.1</span></span>
* <span data-ttu-id="8cc5e-671">従量課金プランでの関数アプリ作成時の不要な functionapp 設定を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-671">Removed unnecessary functionapp settings when creating a function app with consumption plan</span></span>
* <span data-ttu-id="8cc5e-672">SKU オプションに基づいて新しい ASP を作成するために、既定の ASP 文字列の末尾に数字を追加するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-672">Changed `webapp up` so the default asp string now appends number at the end to create a new ASP based on SKU options</span></span>
* <span data-ttu-id="8cc5e-673">ブラウザーでアプリを起動するためのオプションとして、`webapp up` に `-b` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-673">Added `-b` as an option to `webapp up` to launch the app in the browser</span></span>
* <span data-ttu-id="8cc5e-674">`AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` 環境変数を処理するように `webapp deployment source config zip` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-674">Changed `webapp deployment source config zip` to handle `AZURE_CLI_DISABLE_CONNECTION_VERIFICATION` environment variable</span></span>

### <a name="deployment-manager"></a><span data-ttu-id="8cc5e-675">Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="8cc5e-675">Deployment Manager</span></span>
* <span data-ttu-id="8cc5e-676">[プレビュー] 展開をサポートする成果物を作成して管理します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-676">[PREVIEW] Create and manage artifacts that support rollouts</span></span>

### <a name="lab"></a><span data-ttu-id="8cc5e-677">ラボ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-677">Lab</span></span>
* <span data-ttu-id="8cc5e-678">早期終了の原因となっていたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-678">Fixed bug which would cause an early exit</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-679">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-679">Network</span></span>
* <span data-ttu-id="8cc5e-680">子ゾーン作成時のネーム サーバーの自動委任を親の `dns zone create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-680">Added auto name server delegation to `dns zone create` in parent during child zone creation</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-681">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-681">Resource</span></span>
* <span data-ttu-id="8cc5e-682">[非推奨] `resource link` の引数 `--link-id`、`--target-id`、`--filter-string` を廃止しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-682">[DEPRECATED] Deprecated `--link-id`, `--target-id` and `--filter-string` arguments of `resource link`</span></span>
  * <span data-ttu-id="8cc5e-683">代わりに、引数 `--link`、`--target`、および `--filter` を使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-683">Use the arguments `--link`, `--target`, and `--filter` instead</span></span>
* <span data-ttu-id="8cc5e-684">`resource link [create|update]` コマンドが機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-684">Fixed issue where `resource link [create|update]` commands would not work</span></span>
* <span data-ttu-id="8cc5e-685">リソース ID を使用した削除がエラーでクラッシュする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-685">Fixed an issue where deleting using a resource ID could crash on error</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-686">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-686">SQL</span></span>
* <span data-ttu-id="8cc5e-687">マネージド インスタンスでのカスタム タイム ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-687">Added support for custom time zone on managed instances</span></span>
* <span data-ttu-id="8cc5e-688">`sql db update` でのエラスティック プール名の使用を許可するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-688">Changed to allow elastic pool name to be used with `sql db update`</span></span>
* <span data-ttu-id="8cc5e-689">`sql server [create|update]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-689">Added `--no-wait` support to `sql server [create|update]`</span></span>
* <span data-ttu-id="8cc5e-690">`sql server wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-690">Added command `sql server wait`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-691">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-691">Storage</span></span>
* <span data-ttu-id="8cc5e-692">`storage blob generate-sas` での二重エンコードされた SAS トークンの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-692">Fixed issue with double-encoded SAS tokens in `storage blob generate-sas`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-693">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-693">VM</span></span>
* <span data-ttu-id="8cc5e-694">シャットダウンせずに VM の電源をオフにするために、`--skip-shutdown`フラグを `vm|vmss stop` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-694">Added `--skip-shutdown` flag to `vm|vmss stop` to power-off VMs without shutdown</span></span>
* <span data-ttu-id="8cc5e-695">発行プロファイルのアカウントの種類を設定するために、`sig image-version create` に `--storage-account-type` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-695">Added `--storage-account-type` argument to `sig image-version create` to set the publishing profile's account type</span></span>
* <span data-ttu-id="8cc5e-696">リージョン固有のストレージ アカウントの種類を設定できるようにするために、`sig image-version create` に `--target-regions` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-696">Added `--target-regions` argument to `sig image-version create` to allow setting region-specific storage account types</span></span>

## <a name="april-9-2019"></a><span data-ttu-id="8cc5e-697">2019 年 4 月 9 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-697">April 9, 2019</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-698">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-698">Core</span></span>
* <span data-ttu-id="8cc5e-699">一部の拡張機能のバージョンが `Unknown` と表示され、更新できなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-699">Fixed issue where some extensions showed a version of `Unknown` and could not be updated</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-700">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-700">ACR</span></span>
* <span data-ttu-id="8cc5e-701">コンテキストと無関係なイメージ実行のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-701">Added support running an image contextlessly</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-702">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-702">AMS</span></span>
* [非推奨]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
[DEPRECATED]: Deprecated the `--bitrate` parameter of `account-filter` and `asset-filter`
* [破壊的変更]: Renamed the `--bitrate` parameter to `--first-quality`
[BREAKING CHANGE]: Renamed the `--bitrate` parameter to `--first-quality`
* <span data-ttu-id="8cc5e-705">`ams streaming-policy create` に新しい暗号化パラメーターのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-705">Added new encryption parameters support in `ams streaming-policy create`</span></span>
* <span data-ttu-id="8cc5e-706">`ams streaming-locator create` に新しいパラメーター `--filters` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-706">Added new paramter `--filters` to `ams streaming-locator create`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-707">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-707">AppService</span></span>
* <span data-ttu-id="8cc5e-708">`webapp up` に `--logs` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-708">Added `--logs` support to `webapp up`</span></span>
* <span data-ttu-id="8cc5e-709">`functionapp devops-build create` コマンドでの `azure-pipelines.yml` の生成に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-709">Fixed `functionapp devops-build create` command `azure-pipelines.yml` generation issues</span></span>
* <span data-ttu-id="8cc5e-710">`unctionapp devops-build create` のエラー処理とインジケーターを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-710">Improved `unctionapp devops-build create` error handling and indicators</span></span>
* <span data-ttu-id="8cc5e-711">[重大な変更] `devops-build` コマンドの `--local-git` フラグが削除され、Azure DevOps パイプラインを作成する際のローカル Git の検出と処理は強制となりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-711">[BREAKING CHANGE] Removed the `--local-git` flag for `devops-build` command, local git detection and handling are compulsory for creating Azure DevOps pipelines</span></span>
* <span data-ttu-id="8cc5e-712">Linux 関数プラン作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-712">Added support for Linux functions plan creation</span></span>
* <span data-ttu-id="8cc5e-713">`functionapp update --plan` を使用して、関数アプリの基盤になっているプランを切り替える機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-713">Added ability to switch a plan underneath a function app using `functionapp update --plan`</span></span>
* <span data-ttu-id="8cc5e-714">Azure Functions Premium プランのスケールアウト設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-714">Added support for Azure Functions premium plan scale out settings</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-715">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-715">CDN</span></span>
* <span data-ttu-id="8cc5e-716">`Microsoft_Standard` と `Standard_ChinaCdn` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-716">Added support for `Microsoft_Standard` and `Standard_ChinaCdn`</span></span>

### <a name="feedback"></a><span data-ttu-id="8cc5e-717">フィードバック</span><span class="sxs-lookup"><span data-stu-id="8cc5e-717">Feedback</span></span>
* <span data-ttu-id="8cc5e-718">最近実行されたコマンドのメタデータを表示するように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-718">Changed `feedback` to show metadata on recently run commands</span></span>
* <span data-ttu-id="8cc5e-719">ブラウザーを開き、問題テンプレートを使用して、問題作成プロセスの支援をユーザーに促すよう `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-719">Changed `feedback` to prompt user to assist in issue creation process by opening a brower and using an issue template</span></span>
* <span data-ttu-id="8cc5e-720">"--verbose" を指定して実行すると、問題の本文が出力されるように `feedback` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-720">Changed `feedback` to print out issue body when run with '--verbose'</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-721">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-721">Monitor</span></span>
* <span data-ttu-id="8cc5e-722">`metrics alert [create|update]` で "Count" が許容値ではなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-722">Fixed issue where "count" was not a permitted value with `metrics alert [create|update]`</span></span> 

### <a name="network"></a><span data-ttu-id="8cc5e-723">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-723">Network</span></span>
* <span data-ttu-id="8cc5e-724">`vnet-gateway list-bgp-peer-status` で表形式が表示されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-724">Fixed table format not displaying with `vnet-gateway list-bgp-peer-status`</span></span>
* <span data-ttu-id="8cc5e-725">`application-gateway rewrite-rule` に `list-request-headers` コマンドと `list-response-headers` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-725">Added `list-request-headers` and `list-response-headers` commands to `application-gateway rewrite-rule`</span></span>
* <span data-ttu-id="8cc5e-726">`application-gateway rewrite-rule condition` に `list-server-variables` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-726">Added `list-server-variables` command to `application-gateway rewrite-rule condition`</span></span>
* <span data-ttu-id="8cc5e-727">ExpressRoute Port のリンク状態を更新すると、属性不明例外 `express-route port update` がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-727">Fixed an issue where updating link state on an express-route port would throw an unknown attribute exception `express-route port update`</span></span>

### <a name="privatedns"></a><span data-ttu-id="8cc5e-728">プライベート DNS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-728">PrivateDNS</span></span>
* <span data-ttu-id="8cc5e-729">プライベート DNS ゾーンに `network private-dns` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-729">Added `network private-dns` for Private DNS zones</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-730">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-730">Resource</span></span>
* <span data-ttu-id="8cc5e-731">問題を修正しました空のパラメーター セットが含まれるパラメーター ファイルが機能しない、`deployment create` と `group deployment create` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-731">Fixed issue with `deployment create` and `group deployment create` where a parameters file with an empty set of parameters would not work</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-732">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-732">Role</span></span>
* <span data-ttu-id="8cc5e-733">`create-for-rbac` で `--years` が正しく処理されるように修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-733">Fixed `create-for-rbac` to handle `--years` correctly</span></span>
* <span data-ttu-id="8cc5e-734">[重大な変更] サブスクリプションのすべての割り当てを無条件に削除する場合、プロンプトを表示するように `role assignment delete` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-734">[BREAKING CHANGE] Changed `role assignment delete` to prompt when deleting all assignments under the subscription unconditionally</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-735">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-735">SQL</span></span>
* <span data-ttu-id="8cc5e-736">`sql mi [create|update]` を proxyOverride プロパティと publicDataEndpointEnabled プロパティで更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-736">Updated `sql mi [create|update]` with the properties proxyOverride and publicDataEndpointEnabled</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-737">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-737">Storage</span></span>
* <span data-ttu-id="8cc5e-738">[重大な変更] `storage blob delete` の結果を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-738">[BREAKING CHANGE] Removed result of `storage blob delete`</span></span>
* <span data-ttu-id="8cc5e-739">SAS を使用して BLOB の完全な URI を作成できるように `storage blob generate-sas` に `--full-uri` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-739">Added `--full-uri` to `storage blob generate-sas` to create the full uri for the blob with sas</span></span>
* <span data-ttu-id="8cc5e-740">スナップショットからファイルをコピーできるように `storage file copy start` に `--file-snapshot` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-740">Added `--file-snapshot` to `storage file copy start` to copy file from snapshot</span></span>
* <span data-ttu-id="8cc5e-741">NoPendingCopyOperation の例外ではなくエラーのみを表示するように `storage blob copy cancel` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-741">Changed `storage blob copy cancel` to only show the error instead of exception for NoPendingCopyOperation</span></span>

## <a name="march-26-2019"></a><span data-ttu-id="8cc5e-742">2019 年 3 月 26 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-742">March 26, 2019</span></span>


### <a name="core"></a><span data-ttu-id="8cc5e-743">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-743">Core</span></span>
* <span data-ttu-id="8cc5e-744">dev 拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-744">Fixed issues with dev extension incompatibility</span></span>
* <span data-ttu-id="8cc5e-745">エラー処理でお客様が問題のページに誘導されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-745">Error handling now points customers to issues page</span></span>

### <a name="cloud"></a><span data-ttu-id="8cc5e-746">クラウド</span><span class="sxs-lookup"><span data-stu-id="8cc5e-746">Cloud</span></span>
* <span data-ttu-id="8cc5e-747">`cloud set` の 'サブスクリプションが見つかりません' エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-747">Fixed a 'subscription not found' error in `cloud set`</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-748">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-748">ACR</span></span>
* <span data-ttu-id="8cc5e-749">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-749">Fixed redundant sources in image import</span></span>
* <span data-ttu-id="8cc5e-750">`--auth-mode` を `acr build`、`acr run`、`acr task create`、および `acr task update` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-750">Added `--auth-mode` to `acr build`, `acr run`, `acr task create`, and `acr task update` commands</span></span>
* <span data-ttu-id="8cc5e-751">タスク用の資格情報を管理するための 'acr task credential' コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-751">Added 'acr task credential' command group for managing credentials for a Task</span></span>
* <span data-ttu-id="8cc5e-752">'--no-wait' を `acr build` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-752">Added '--no-wait' to `acr build` command</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-753">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-753">AppService</span></span>
* <span data-ttu-id="8cc5e-754">`webapp up` が空のディレクトリから、または不明なコード シナリオでの実行を正しく処理しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-754">Fixed bug where `webapp up` was not handling running from empty directory or unknown code scenario correctly</span></span>
* <span data-ttu-id="8cc5e-755">スロットが `[webapp|functionapp] config ssl bind` に機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-755">Fixed bug where slots didn't work for `[webapp|functionapp] config ssl bind`</span></span>

### <a name="bot-service"></a><span data-ttu-id="8cc5e-756">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="8cc5e-756">BOT Service</span></span>
* <span data-ttu-id="8cc5e-757">`webapp` を介したボットのデプロイに備えるため `bot prepare-deploy` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-757">Added `bot prepare-deploy` to prepare for deploying bots via `webapp`</span></span>
* <span data-ttu-id="8cc5e-758">パスワードが指定されていないときにパスワードを表示するように `bot create --kind registration` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-758">Changed `bot create --kind registration` to show password if the password is not provided</span></span>
* <span data-ttu-id="8cc5e-759">[重大な変更] 要求されるのではなく、既定で空の文字列になるように `bot create --kind registration` で `--endpoint` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-759">[BREAKING CHANGE] Changed `--endpoint` in `bot create --kind registration` to default to an empty string instead of being required</span></span>
* <span data-ttu-id="8cc5e-760">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-760">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-761">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-761">CDN</span></span>
* <span data-ttu-id="8cc5e-762">`--no-wait` のサポートを `cdn endpoint [create|update|start|stop|delete|load|purge]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-762">Added support for `--no-wait` to `cdn endpoint [create|update|start|stop|delete|load|purge]`</span></span>  
* [重大な変更]:`cdn endpoint create` のクエリ文字列の既定のキャッシュ動作を変更しました
[BREAKING CHANGE]: Changed `cdn endpoint create` default query string caching behaviour. <span data-ttu-id="8cc5e-764">"IgnoreQueryString" は既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-764">No longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="8cc5e-765">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-765">It is now set by the service</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-766">Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="8cc5e-766">Cosmosdb</span></span>
* <span data-ttu-id="8cc5e-767">アカウントの更新で `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-767">Added support for `--enable-multiple-write-locations` on account update</span></span>
* <span data-ttu-id="8cc5e-768">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-768">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-769">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-769">Interactive</span></span>
* <span data-ttu-id="8cc5e-770">azdev を通じてインストールされたインタラクティブ拡張機能の非互換性の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-770">Fixed incompatibility with Interactive extension installed through azdev</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-771">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-771">Monitor</span></span>
* <span data-ttu-id="8cc5e-772">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-772">Changed to allow dimension value `*` for `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-773">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-773">Network</span></span>
* <span data-ttu-id="8cc5e-774">`rewrite-rule` コマンド グループを `application-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-774">Added `rewrite-rule` command group to `application-gateway`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-775">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-775">Profile</span></span>
* <span data-ttu-id="8cc5e-776">マネージド サービス ID に対応するテナント レベル アカウントのサポートを `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-776">Added tenant level account support for managed service identity to `login`</span></span>

### <a name="postgres"></a><span data-ttu-id="8cc5e-777">Postgres</span><span class="sxs-lookup"><span data-stu-id="8cc5e-777">Postgres</span></span> 
* <span data-ttu-id="8cc5e-778">postgresql`replica` コマンドと `restart server` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-778">Added postgresql `replica` commands and `restart server` command</span></span>
* <span data-ttu-id="8cc5e-779">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための変更を行いました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-779">Changed to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-780">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-780">Resource</span></span>
* <span data-ttu-id="8cc5e-781">`deployment [create|list|show]` のテーブル出力を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-781">Improved table output for `deployment [create|list|show]`</span></span>
* <span data-ttu-id="8cc5e-782">型 secureObject が認識されない `deployment [create|validate]` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-782">Fixed issue with `deployment [create|validate]` where type secureObject was not recognized</span></span>

### <a name="graph"></a><span data-ttu-id="8cc5e-783">Graph</span><span class="sxs-lookup"><span data-stu-id="8cc5e-783">Graph</span></span>
* <span data-ttu-id="8cc5e-784">`--end-date` のサポートを `ad [app|sp] credential reset` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-784">Added support for `--end-date` to `ad [app|sp] credential reset`</span></span>
* <span data-ttu-id="8cc5e-785">`ad app permission add` にアクセス許可の追加サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-785">Added support to add permissions with `ad app permission add`</span></span>
* <span data-ttu-id="8cc5e-786">アクセス許可がない `ad app permission list` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-786">Fixed a bug with `ad app permission list` when there were no permissions</span></span>
* <span data-ttu-id="8cc5e-787">現在のアカウントにサブスクリプションがない場合にロール割り当ての削除をスキップするように `ad sp delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-787">Changed `ad sp delete` to skip role assignment delete if the current account has no subscription</span></span>
* <span data-ttu-id="8cc5e-788">指定されていない場合、`--identifier-uris` が既定で空のリストを指定するように `ad app create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-788">Changed `ad app create` to have `--identifier-uris` default to empty list if not provided</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-789">storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-789">storage</span></span>
* <span data-ttu-id="8cc5e-790">共有スナップショットからダウンロードするように `--snapshot` を `storage file download-batch` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-790">Added `--snapshot` to `storage file download-batch` to download from a share snapshot</span></span>
* <span data-ttu-id="8cc5e-791">より簡潔に、現在の BLOB を示すように `storage blob [download-batch|upload-batch]` 進行状況バーを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-791">Changed `storage blob [download-batch|upload-batch]` progress bar to be less verbose and indicate current blob</span></span>
* <span data-ttu-id="8cc5e-792">暗号化パラメーターの更新時の `storage account update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-792">Fixed issue with `storage account update` when updating encryption parameters</span></span>
* <span data-ttu-id="8cc5e-793">OAuth (`--auth-mode=login`) の使用時に `storage blob show` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-793">Fixed issue where `storage blob show` would fail when using oauth (`--auth-mode=login`)</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-794">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-794">VM</span></span>
* <span data-ttu-id="8cc5e-795">`image update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-795">Added `image update` command</span></span>

## <a name="march-12-2019"></a><span data-ttu-id="8cc5e-796">2019 年 3 月 12 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-796">March 12, 2019</span></span>

<span data-ttu-id="8cc5e-797">バージョン 2.0.60</span><span class="sxs-lookup"><span data-stu-id="8cc5e-797">Version 2.0.60</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-798">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-798">Core</span></span>

* <span data-ttu-id="8cc5e-799">サブスクリプションが見つからないという `cloud set` の正しくないエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-799">Fixed an incorrect error in `cloud set` about subscription not found</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-800">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-800">ACR</span></span>

* <span data-ttu-id="8cc5e-801">イメージ インポートの冗長なソースを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-801">Fixed redundant sources in image import</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-802">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-802">ACS</span></span>

* <span data-ttu-id="8cc5e-803">kubectl でサポートされていない場合、`aks browse` の `--listen-address`パラメーターを無視するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-803">Changed to ignore the `--listen-address` parameter for `aks browse` if it is not supported by kubectl</span></span> 

### <a name="appservice"></a><span data-ttu-id="8cc5e-804">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-804">AppService</span></span>

* <span data-ttu-id="8cc5e-805">Kudu の公開 URL とその資格情報を取得するための `[webapp|functionapp] deployment list-publishing-credentials` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-805">Added `[webapp|functionapp] deployment list-publishing-credentials` to get the Kudu publishing url and its credentials</span></span>
* <span data-ttu-id="8cc5e-806">`webapp auth update` の誤った print ステートメントを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-806">Removed erroneous print statement for `webapp auth update`</span></span>
* <span data-ttu-id="8cc5e-807">Linux App Service プランのランタイム用に正しいイメージを設定するように `functionapp` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-807">Fixed `functionapp` to set the correct image for runtime in Linux App Service plans</span></span>
* <span data-ttu-id="8cc5e-808">`webapp up` のプレビュー タグを削除し、コマンドを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-808">Removed preview tag for `webapp up` and added improvements to the command</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-809">Botservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-809">Botservice</span></span>

* <span data-ttu-id="8cc5e-810">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `SCM_DO_BUILD_DURING_DEPLOYMENT` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-810">Added `SCM_DO_BUILD_DURING_DEPLOYMENT` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="8cc5e-811">v4 Web アプリ ボット用の ARM テンプレートのアプリケーション設定に `Microsoft-BotFramework-AppId` と `Microsoft-BotFramework-AppPassword` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-811">Added `Microsoft-BotFramework-AppId` and `Microsoft-BotFramework-AppPassword` to ARM template's Application Settings for v4 Web App Bots</span></span>
* <span data-ttu-id="8cc5e-812">`bot create` の最後で `bot publish` コマンドの出力から一重引用符を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-812">Removed single quotes from `bot publish` command output at end of `bot create`</span></span>
* <span data-ttu-id="8cc5e-813">`bot publish` を非同期に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-813">Changed `bot publish` to be asynchronous</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-814">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-814">Container</span></span>

* <span data-ttu-id="8cc5e-815">`--no-wait` 引数を `container [start|restart]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-815">Added `--no-wait` argument to `container [start|restart]`</span></span>

### <a name="eventhub"></a><span data-ttu-id="8cc5e-816">EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc5e-816">EventHub</span></span>

* <span data-ttu-id="8cc5e-817">キャプチャで空のアーカイブをサポートするために、`--skip-empty-archives` フラグを `eventhub create|update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-817">Added `--skip-empty-archives` flag to `eventhub create|update` to support empty archives in capture</span></span>

### <a name="find"></a><span data-ttu-id="8cc5e-818">Find</span><span class="sxs-lookup"><span data-stu-id="8cc5e-818">Find</span></span>

* <span data-ttu-id="8cc5e-819">主要な機能更新</span><span class="sxs-lookup"><span data-stu-id="8cc5e-819">Major functionality update</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-820">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-820">HDInsight</span></span>

* <span data-ttu-id="8cc5e-821">ADLS Gen2 MSI をサポートするために、`--storage-account-managed-identity` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-821">Added the `--storage-account-managed-identity` parameter to `hdinsight create` to support ADLS Gen2 MSI</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-822">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-822">Network</span></span>

* <span data-ttu-id="8cc5e-823">異なるサブスクリプションのゲートウェイ間の VPN 接続を更新できない `vpn-connection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-823">Fixed issue with `vpn-connection update` where updating a VPN connection between gateways in different subscriptions would fail</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-824">Rdbms</span><span class="sxs-lookup"><span data-stu-id="8cc5e-824">Rdbms</span></span>

* <span data-ttu-id="8cc5e-825">サーバーの作成用に提供されていない場合にリソース グループから規定の場所を取得し、リテンション期間の日数の検証を追加するための軽微な修正を行いました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-825">Minor fixes to get default location from resource group when not provided for creating servers and add validation for retention days</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-826">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-826">Role</span></span>

* <span data-ttu-id="8cc5e-827">定義を正しく解決するために ID を使用するように `role definition update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-827">Fixed `role definition update` to use ID to resolve definition correctly</span></span>
* <span data-ttu-id="8cc5e-828">アプリのサービス プリンシパルが常に存在するという前提を除去するように `ad app credential reset` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-828">Changed `ad app credential reset` to remove the assumption that app's service principal always exists</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8cc5e-829">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-829">Service Fabric</span></span>

* <span data-ttu-id="8cc5e-830">`sf cluster list` が反復可能ではないことに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-830">Fixed issue with `sf cluster list` was not iterable</span></span>

## <a name="february-26-2019"></a><span data-ttu-id="8cc5e-831">2019 年 2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-831">February 26, 2019</span></span>

<span data-ttu-id="8cc5e-832">バージョン 2.0.59</span><span class="sxs-lookup"><span data-stu-id="8cc5e-832">Version 2.0.59</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-833">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-833">Core</span></span>

* <span data-ttu-id="8cc5e-834">一部のインスタンスで `--subscription NAME` を使用すると例外がスローされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-834">Fixed issue where in some instances using `--subscription NAME` would throw an exception</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-835">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-835">ACR</span></span>

* <span data-ttu-id="8cc5e-836">`acr build`、`acr task create`、`acr task update` コマンドに `--target` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-836">Added `--target` parameter for `acr build`, `acr task create` and `acr task update` commands</span></span>
* <span data-ttu-id="8cc5e-837">Azure にログインしていない場合の、ランタイム コマンドのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-837">Improved error handling for runtime commands when not logged into Azure</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-838">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-838">ACS</span></span>

* <span data-ttu-id="8cc5e-839">`--listen-address` オプションを `aks port-forward` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-839">Added `--listen-address` option to `aks port-forward`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-840">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-840">AppService</span></span>

* <span data-ttu-id="8cc5e-841">`functionapp devops-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-841">Added `functionapp devops-build` command</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-842">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-842">Batch</span></span>
* <span data-ttu-id="8cc5e-843">[重大な変更] `batch pool upgrade os` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-843">[BREAKING CHANGE] Removed the `batch pool upgrade os` command</span></span>
* <span data-ttu-id="8cc5e-844">[重大な変更] `Application` の応答から `Pacakges` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-844">[BREAKING CHANGE] Removed the `Pacakges` property from `Application` responses</span></span>
* <span data-ttu-id="8cc5e-845">アプリケーションのパッケージを一覧表示する `batch application package list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-845">Added the `batch application package list` command to list packages of an application</span></span>
* <span data-ttu-id="8cc5e-846">[重大な変更] すべての `batch application` コマンドで `--application-id` を `--application-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-846">[BREAKING CHANGE] Changed `--application-id` to `--application-name` in all `batch application` commands,</span></span> 
* <span data-ttu-id="8cc5e-847">生の API 応答を要求するためのコマンドに `--json-file` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-847">Added the `--json-file` argument to commands for requesting the raw API response</span></span>
* <span data-ttu-id="8cc5e-848">すべてのエンドポイントに自動的に `https://` を含めるように検証を更新しました (抜けている場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-848">Updated validation to automatically include `https://` in all endpoints if missing</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-849">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-849">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-850">Cosmos DB アカウントの VNET ルールを管理するために、`add`、`remove`、および `list` コマンドに `network-rule` サブグループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-850">Added `network-rule` subgroup with commands `add`, `remove`, and `list` for managing VNET rules of a Cosmos DB account</span></span>

### <a name="kusto"></a><span data-ttu-id="8cc5e-851">Kusto</span><span class="sxs-lookup"><span data-stu-id="8cc5e-851">Kusto</span></span>

* <span data-ttu-id="8cc5e-852">[重大な変更] データベースの `hot_cache_period` および `soft_delete_period` 型を ISO8601 の期間形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-852">[BREAKING CHANGE] Changed `hot_cache_period` and `soft_delete_period` types for database to ISO8601 duration format</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-853">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-853">Network</span></span>

* <span data-ttu-id="8cc5e-854">`--express-route-gateway-bypass` 引数を `vpn-connection [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-854">Added `--express-route-gateway-bypass` argument to `vpn-connection [create|update]`</span></span>
* <span data-ttu-id="8cc5e-855">`express-route` 拡張機能のコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-855">Added command groups from `express-route` extensions</span></span>
* <span data-ttu-id="8cc5e-856">`express-route gateway` および `express-route port` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-856">Added `express-route gateway` and `express-route port` command groups</span></span>
* <span data-ttu-id="8cc5e-857">`--legacy-mode` 引数を `express-route peering [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-857">Added argument `--legacy-mode` to `express-route peering [create|update]`</span></span> 
* <span data-ttu-id="8cc5e-858">`--allow-classic-operations` 引数を `--express-route-port` および `express-route [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-858">Added arguments `--allow-classic-operations` and `--express-route-port` to `express-route [create|update]`</span></span>
* <span data-ttu-id="8cc5e-859">`--gateway-default-site` 引数を `vnet-gateway [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-859">Added `--gateway-default-site` argument to `vnet-gateway [create|update]`</span></span>
* <span data-ttu-id="8cc5e-860">`ipsec-policy` コマンドを `vnet-gateway` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-860">Added `ipsec-policy` commands to `vnet-gateway`</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-861">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-861">Resource</span></span>

* <span data-ttu-id="8cc5e-862">型フィールドで大文字と小文字が区別されていた `deployment create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-862">Fixed issue with `deployment create` where type field was case-sensitive</span></span>
* <span data-ttu-id="8cc5e-863">`policy assignment create` に URI ベースのパラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-863">Added support for URI-based parameters file to `policy assignment create`</span></span>
* <span data-ttu-id="8cc5e-864">`policy set-definition update` に URI ベースのパラメーターおよび定義のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-864">Added support for URI-based parameters and definitions to `policy set-definition update`</span></span>
* <span data-ttu-id="8cc5e-865">`policy definition update` のパラメーターと規則の処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-865">Fixed handling of parameters and rules for `policy definition update`</span></span>
* <span data-ttu-id="8cc5e-866">クロス サブスクリプション ID でサブスクリプション ID が正しく優先されなかった `resource show/update/delete/tag/invoke-action` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-866">Fixed issue with `resource show/update/delete/tag/invoke-action` where cross-subscription IDs did not properly honor the subscription ID</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-867">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-867">Role</span></span>

* <span data-ttu-id="8cc5e-868">アプリ ロールのサポートを `ad app [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-868">Added support for app roles to `ad app [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-869">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-869">VM</span></span>

* <span data-ttu-id="8cc5e-870">Ubuntu 18.0 で --accelerated-networking が既定で有効になっていなかった `vm create where ` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-870">Fixed issue with `vm create where `--accelerated-networking\` was not enabled by default for Ubuntu 18.0</span></span>

## <a name="february-12-2019"></a><span data-ttu-id="8cc5e-871">2019 年 2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-871">February 12, 2019</span></span>

<span data-ttu-id="8cc5e-872">バージョン 2.0.58</span><span class="sxs-lookup"><span data-stu-id="8cc5e-872">Version 2.0.58</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-873">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-873">Core</span></span>

* <span data-ttu-id="8cc5e-874">更新可能なパッケージがある場合、`az --version` で通知が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-874">`az --version` now displays a notification if you have packages that can be updated</span></span>
* <span data-ttu-id="8cc5e-875">JSON 出力で `--ids` を使用できなくなる回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-875">Fixed regression where `--ids` could no longer be used with JSON output</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-876">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-876">ACR</span></span>
* <span data-ttu-id="8cc5e-877">[重大な変更] `acr build-task` コマンド グループを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-877">[BREAKING CHANGE] Removed `acr build-task` command group</span></span>
* <span data-ttu-id="8cc5e-878">[重大な変更] `acr repository delete` から `--tag` オプションおよび `--manifest` オプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-878">[BREAKING CHANGE] Removed `--tag` and `--manifest` options from from `acr repository delete`</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-879">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-879">ACS</span></span>
* <span data-ttu-id="8cc5e-880">`aks [enable-addons|disable-addons]` に、大文字と小文字を区別しない名前のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-880">Added support for case-insensitive names to `aks [enable-addons|disable-addons]`</span></span>
* <span data-ttu-id="8cc5e-881">`aks update-credentials --reset-aad` を使用した Azure Active Directory 更新操作のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-881">Added support for Azure Active Directory updating operation using `aks update-credentials --reset-aad`</span></span>
* <span data-ttu-id="8cc5e-882">`aks get-credentials` のために `--output` が無視されることの説明を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-882">Added clarification that `--output` is ignored for `aks get-credentials`</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-883">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-883">AMS</span></span>
* <span data-ttu-id="8cc5e-884">`ams streaming-endpoint [start | stop | create | update] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-884">Added `ams streaming-endpoint [start | stop | create | update] wait` commands</span></span>
* <span data-ttu-id="8cc5e-885">`ams live-event [create | start | stop | reset] wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-885">Added `ams live-event [create | start | stop | reset] wait` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-886">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-886">Appservice</span></span>
* <span data-ttu-id="8cc5e-887">ACR のコンテナーを使用して関数を作成および構成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-887">Added ability to create and configure functions using ACR containers</span></span>
* <span data-ttu-id="8cc5e-888">JSON 経由で Web アプリの構成を更新するためのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-888">Added support for updating webapp configurations through json</span></span>
* <span data-ttu-id="8cc5e-889">`appservice-plan-update` のヘルプを強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-889">Improved help for `appservice-plan-update`</span></span>
* <span data-ttu-id="8cc5e-890">functionapp create に対する App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-890">Added support for app insights on functionapp create</span></span>
* <span data-ttu-id="8cc5e-891">Web アプリの SSH の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-891">Fixed issues with webapp SSH</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-892">Botservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-892">Botservice</span></span>
* <span data-ttu-id="8cc5e-893">`bot publish` の UX を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-893">Improved UX for `bot publish`</span></span>
* <span data-ttu-id="8cc5e-894">`az bot publish` の間に `npm install` を実行した場合のタイムアウトの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-894">Added warning for timeouts when running `npm install` during `az bot publish`</span></span>
* <span data-ttu-id="8cc5e-895">`az bot create` の `--name` から無効な文字 `.` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-895">Removed invalid char `.` from `--name`  in `az bot create`</span></span>
* <span data-ttu-id="8cc5e-896">Azure Storage、App Service プラン、関数または Web アプリ、Application Insights を作成するときに、リソース名のランダム化を停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-896">Changed to stop randomizing resource names when creating Azure Storage, App Service Plan, Function/Web App and Application Insights</span></span>
* <span data-ttu-id="8cc5e-897">[非推奨] `--proj-file-path`を優先して、`--proj-name` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-897">[DEPRECATED] Deprecated `--proj-name` argument in favor of `--proj-file-path`</span></span>
* <span data-ttu-id="8cc5e-898">存在しなかった場合にフェッチされた IIS Node.js デプロイ ファイルを削除するように、`az bot publish` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-898">Changed `az bot publish` to remove fetched IIS Node.js deployment files if they did not already exist</span></span>
* <span data-ttu-id="8cc5e-899">App Service で `node_modules` フォルダーを削除しないように、`az bot publish` に `--keep-node-modules` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-899">Added `--keep-node-modules` argument to `az bot publish` to not delete `node_modules` folder on App Service</span></span>
* <span data-ttu-id="8cc5e-900">Azure Functions ボットまたは Web アプリ ボットの作成時の、`az bot create` からの出力に `"publishCommand"` キーと値のペアを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-900">Added `"publishCommand"` key-value pair to output from `az bot create` when creating an Azure Function or Web App bot</span></span>
  * <span data-ttu-id="8cc5e-901">`"publishCommand"` の値は、新しく作成したボットを発行するために必要なパラメーターが入力された `az bot publish` コマンドです</span><span class="sxs-lookup"><span data-stu-id="8cc5e-901">The value of `"publishCommand"` is an `az bot publish` command prepopulated with the required parameters to publish the newly created bot</span></span>
* <span data-ttu-id="8cc5e-902">8\.9.4 ではなく 10.14.1 を使用するように、v4 SDK ボット用の ARM テンプレートで `"WEBSITE_NODE_DEFAULT_VERSION"` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-902">Updated `"WEBSITE_NODE_DEFAULT_VERSION"` in ARM template for v4 SDK bots to use 10.14.1 instead of 8.9.4</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-903">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-903">Key Vault</span></span>
* <span data-ttu-id="8cc5e-904">`--id` の使用時に一部のユーザーに `unexpected_keyword` エラーが発生する `keyvault secret backup` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-904">Fixed issue with `keyvault secret backup` where some users received an `unexpected_keyword` error when using `--id`</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-905">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-905">Monitor</span></span>
* <span data-ttu-id="8cc5e-906">ディメンション値 `*` を許可するように `monitor metrics alert [create|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-906">Changed `monitor metrics alert [create|update]` to allow dimension value `*`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-907">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-907">Network</span></span>
* <span data-ttu-id="8cc5e-908">エクスポートされた CNAME が必ず FQDN になるように `dns zone export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-908">Changed `dns zone export` to ensure exported CNAMEs are FQDNs</span></span>
* <span data-ttu-id="8cc5e-909">アプリケーション ゲートウェイのバックエンド アドレス プールをサポートするように、`--gateway-name` パラメーターを `nic ip-config address-pool [add|remove]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-909">Added `--gateway-name` parameter to `nic ip-config address-pool [add|remove]` to support application gateway backend address pools</span></span>
* <span data-ttu-id="8cc5e-910">Log Analytics ワークスペースによるトラフィック分析をサポートするために、`--traffic-analytics` 引数と `--workspace` 引数を `network watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-910">Added `--traffic-analytics` and `--workspace` arguments to `network watcher flow-log configure` to support traffic analytics through a Log Analytics workspace</span></span>
* <span data-ttu-id="8cc5e-911">`--idle-timeout` と `--floating-ip` を `lb inbound-nat-pool [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-911">Added `--idle-timeout` and `--floating-ip` to `lb inbound-nat-pool [create|update]`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="8cc5e-912">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="8cc5e-912">Policy Insights</span></span>
* <span data-ttu-id="8cc5e-913">リソース ポリシーの修復機能をサポートするために、`policy remediation` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-913">Added `policy remediation` commands to support resource policy remediation features</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-914">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-914">RDBMS</span></span>
* <span data-ttu-id="8cc5e-915">ヘルプ メッセージとコマンド パラメーターを強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-915">Improved help message and command parameters</span></span>

### <a name="redis"></a><span data-ttu-id="8cc5e-916">Redis</span><span class="sxs-lookup"><span data-stu-id="8cc5e-916">Redis</span></span>
* <span data-ttu-id="8cc5e-917">ファイアウォール規則を管理 (作成、更新、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-917">Added commands for managing firewall-rules (create, update, delete, show, list)</span></span>
* <span data-ttu-id="8cc5e-918">サーバーのリンクを管理 (作成、削除、表示、一覧表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-918">Added commands for managing server-link (create, delete, show, list)</span></span>
* <span data-ttu-id="8cc5e-919">パッチ スケジュールを管理 (作成、更新、削除、表示) するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-919">Added commands for managing patch-schedule (create, update, delete, show)</span></span>
* <span data-ttu-id="8cc5e-920">redis create に、Availability Zones と TLS 最小バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-920">Added support for Availability Zones and Minimum TLS Version to \`redis create</span></span>
* <span data-ttu-id="8cc5e-921">[重大な変更] `redis update-settings` コマンドおよび `redis list-all` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-921">[BREAKING CHANGE] Removed `redis update-settings` and `redis list-all` commands</span></span>
* <span data-ttu-id="8cc5e-922">[重大な変更] `redis create` のパラメーター 'tenant settings' は、key[=value] 形式では使用できなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-922">[BREAKING CHANGE] Parameter for `redis create`: 'tenant settings' is not accepted in key[=value] format</span></span>
* <span data-ttu-id="8cc5e-923">[非推奨] `redis import-method` コマンドが非推奨であることを示す警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-923">[DEPRECATED] Added warning message for deprecating `redis import-method` command</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-924">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-924">Role</span></span>
* <span data-ttu-id="8cc5e-925">[重大な変更] `az identity` コマンドを `vm` のコマンドからここに移動しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-925">[BREAKING CHANGE] Moved `az identity` command here from `vm` commands</span></span>

### <a name="sql-vm"></a><span data-ttu-id="8cc5e-926">SQL VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-926">SQL VM</span></span>
* <span data-ttu-id="8cc5e-927">[非推奨] 誤りがあったため、`--boostrap-acc-pwd` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-927">[DEPRECATED] Deprecated `--boostrap-acc-pwd` argument due to typo</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-928">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-928">VM</span></span>
* <span data-ttu-id="8cc5e-929">`--all true` の代わりに `--all` を使用できるように `vm list-skus` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-929">Changed `vm list-skus` to allow use of `--all` in place of `--all true`</span></span>
* <span data-ttu-id="8cc5e-930">`vmss run-command [invoke | list | show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-930">Added `vmss run-command [invoke | list | show]`</span></span>
* <span data-ttu-id="8cc5e-931">以前に実行していた場合に `vmss encryption enable` が失敗するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-931">Fixed bug where `vmss encryption enable` would fail if run previously</span></span>
* <span data-ttu-id="8cc5e-932">[重大な変更] `az identity` コマンドを `role` のコマンドに移動しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-932">[BREAKING CHANGE] Moved `az identity` command to `role` commands</span></span>

## <a name="january-31-2019"></a><span data-ttu-id="8cc5e-933">2019 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-933">January 31, 2019</span></span>

<span data-ttu-id="8cc5e-934">バージョン 2.0.57</span><span class="sxs-lookup"><span data-stu-id="8cc5e-934">Version 2.0.57</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-935">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-935">Core</span></span>

* <span data-ttu-id="8cc5e-936">[問題 8399](https://github.com/Azure/azure-cli/issues/8399) 用のホット フィックス。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-936">Hot Fix for [issue 8399](https://github.com/Azure/azure-cli/issues/8399).</span></span>

## <a name="january-28-2019"></a><span data-ttu-id="8cc5e-937">2019 年 1 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-937">January 28, 2019</span></span>

<span data-ttu-id="8cc5e-938">バージョン 2.0.56</span><span class="sxs-lookup"><span data-stu-id="8cc5e-938">Version 2.0.56</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-939">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-939">ACR</span></span>
* <span data-ttu-id="8cc5e-940">VNet ルールまたは IP 規則のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-940">Added support for VNet/IP rules</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-941">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-941">ACS</span></span>
* <span data-ttu-id="8cc5e-942">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-942">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="8cc5e-943">マネージド OpenShift コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-943">Added Managed OpenShift commands</span></span>
* <span data-ttu-id="8cc5e-944">`aks update-credentials -reset-service-principal` を使用したサービス プリンシパル更新操作に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-944">Added support for service principal updates operation with `aks update-credentials -reset-service-principal`</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-945">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-945">AMS</span></span>
* <span data-ttu-id="8cc5e-946">[重大な変更] 名前を `ams asset get-streaming-locators` から `ams asset list-streaming-locators` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-946">[BREAKING CHANGE] Renamed `ams asset get-streaming-locators` to `ams asset list-streaming-locators`</span></span>
* <span data-ttu-id="8cc5e-947">[重大な変更] 名前を `ams streaming-locator get-content-keys` から `ams streaming-locator list-content-keys` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-947">[BREAKING CHANGE] Renamed `ams streaming-locator get-content-keys` to `ams streaming-locator list-content-keys`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-948">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-948">Appservice</span></span>
* <span data-ttu-id="8cc5e-949">`functionapp create` での App Insights のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-949">Added support for app insights on `functionapp create`</span></span>
* <span data-ttu-id="8cc5e-950">Function App に、App Service プラン作成 (エラスティック Premium を含む) のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-950">Added support for app service plan creation (including Elastic Premium) to Function Apps</span></span>
* <span data-ttu-id="8cc5e-951">エラスティック Premium プランのアプリ設定に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-951">Fixed app setting issues with Elastic Premium plans</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-952">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-952">Container</span></span>
* <span data-ttu-id="8cc5e-953">`container start` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-953">Added `container start` command</span></span>
* <span data-ttu-id="8cc5e-954">コンテナーの作成時に CPU に 10 進数値を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-954">Changed to allow using decimal values for CPU during container creation</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8cc5e-955">EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-955">EventGrid</span></span>
* <span data-ttu-id="8cc5e-956">`--deadletter-endpoint` パラメーターを `event-subscription [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-956">Added `--deadletter-endpoint` parameter to `event-subscription [create|update]`</span></span>
* <span data-ttu-id="8cc5e-957">"event-subscription [create|update] --endpoint-type" の新しい値として、storagequeue と hybridconnection を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-957">Added storagequeue and hybridconnection as new values for 'event-subscription [create|update] --endpoint-type\`</span></span>
* <span data-ttu-id="8cc5e-958">イベントの再試行ポリシーを指定するために、`--max-delivery-attempts` パラメーターと `--event-ttl` パラメーターを `event-subscription create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-958">Added `--max-delivery-attempts` and `--event-ttl` parameters to `event-subscription create` to specify the retry policy for events</span></span>
* <span data-ttu-id="8cc5e-959">イベント サブスクリプションの保存先として Webhook が使用されている場合、`event-subscription [create|update]` に警告メッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-959">Added a warning message to `event-subscription [create|update]` when webhook as destination is used for an event subscription</span></span>
* <span data-ttu-id="8cc5e-960">すべてのイベント サブスクリプションに関連するコマンドに source-resource-id パラメーターを追加し、その他のすべてのソース リソース関連パラメーターを非推奨としてマークしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-960">Added source-resource-id parameter for all event subscription related commands and mark all other source resource related parameters as deprecated</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-961">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-961">HDInsight</span></span>
* <span data-ttu-id="8cc5e-962">[重大な変更] `hdinsight [application] create` から `--virtual-network` パラメーターと `--subnet-name` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-962">[BREAKING CHANGE] Removed the `--virtual-network` and `--subnet-name` parameters from `hdinsight [application] create`</span></span>
* <span data-ttu-id="8cc5e-963">[重大な変更] BLOB エンドポイントではなく、ストレージ アカウントの名前または ID を受け入れるように、`hdinsight create --storage-account` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-963">[BREAKING CHANGE] Changed `hdinsight create --storage-account` to accept name or id of storage account instead of blob endpoints</span></span>
* <span data-ttu-id="8cc5e-964">`--vnet-name` および `--subnet-name` パラメーターを `hdinsight create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-964">Added `--vnet-name` and `--subnet-name` parameters to `hdinsight create`</span></span>
* <span data-ttu-id="8cc5e-965">Enterprise セキュリティ パッケージとディスク暗号化のサポートが `hdinsight create` に追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-965">Added support for Enterprise Security Package and disk encryption to `hdinsight create`</span></span> 
* <span data-ttu-id="8cc5e-966">`hdinsight rotate-disk-encryption-key` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-966">Added `hdinsight rotate-disk-encryption-key` command</span></span>
* <span data-ttu-id="8cc5e-967">`hdinsight update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-967">Added `hdinsight update` command</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-968">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-968">IoT</span></span>
* <span data-ttu-id="8cc5e-969">routing-endpoint コマンドにエンコード形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-969">Added encoding format to routing-endpoint command</span></span>

### <a name="kusto"></a><span data-ttu-id="8cc5e-970">Kusto</span><span class="sxs-lookup"><span data-stu-id="8cc5e-970">Kusto</span></span>
* <span data-ttu-id="8cc5e-971">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-971">Preview release</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-972">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-972">Monitor</span></span>
* <span data-ttu-id="8cc5e-973">大文字と小文字が区別されないように、ID 比較を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-973">Changed ID comparison to be case insensitive</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-974">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-974">Profile</span></span>
* <span data-ttu-id="8cc5e-975">`login` でマネージド サービス ID に対応するテナント レベル アカウントを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-975">Enable tenant level account for managed service identity for `login`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-976">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-976">Network</span></span>
* <span data-ttu-id="8cc5e-977">`--bandwidth` 引数が無視される `express-route update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-977">Fixed issue with `express-route update`: where `--bandwidth` argument was ignored</span></span>
* <span data-ttu-id="8cc5e-978">set comprehension によってスタック トレースが引き起こされる `ddos-protection update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-978">Fixed issue with `ddos-protection update` where set comprehension caused stack trace</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-979">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-979">Resource</span></span>
* <span data-ttu-id="8cc5e-980">`group deployment create` に URI パラメーター ファイルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-980">Added support for URI parameters file to `group deployment create`</span></span>
* <span data-ttu-id="8cc5e-981">`policy assignment [create|list|show]` にマネージド ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-981">Added support for managed identity to `policy assignment [create|list|show]`</span></span>

### <a name="sql-virtual-machine"></a><span data-ttu-id="8cc5e-982">SQL 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="8cc5e-982">SQL Virtual Machine</span></span>
* <span data-ttu-id="8cc5e-983">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-983">Preview release</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-984">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-984">Storage</span></span>
* <span data-ttu-id="8cc5e-985">同じオブジェクトで変更されるプロパティのみを更新するように修正プログラムを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-985">Changed fix to update only properties that are changed on the same object</span></span>
* <span data-ttu-id="8cc5e-986">#8021 を修正しました。バイナリ データが返されるとき、base 64 でエンコードされます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-986">Fixed #8021, binary data is encoded in base 64 when returned</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-987">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-987">VM</span></span>
* <span data-ttu-id="8cc5e-988">ディスク暗号化 keyvault と、キー暗号化 keyvault が存在することを検証するように `vm encryption enable` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-988">Changed `vm encryption enable` to validate disk encryption keyvault and that key encryption keyvault exists</span></span>
* <span data-ttu-id="8cc5e-989">`--force` フラグを `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-989">Added `--force` flag to `vm encryption enable`</span></span>

## <a name="january-15-2019"></a><span data-ttu-id="8cc5e-990">2019 年 1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-990">January 15, 2019</span></span>

<span data-ttu-id="8cc5e-991">バージョン 2.0.55</span><span class="sxs-lookup"><span data-stu-id="8cc5e-991">Version 2.0.55</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-992">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-992">ACR</span></span>
* <span data-ttu-id="8cc5e-993">存在しない Helm チャートを強制プッシュできるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-993">Changed to allow force push a helm chart that doesn't exist</span></span>
* <span data-ttu-id="8cc5e-994">ARM 要求なしでランタイム操作できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-994">changed to allow runtime operations without ARM requests</span></span>
* <span data-ttu-id="8cc5e-995">[非推奨] 次のコマンドの `--resource-group` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-995">[DEPRECATED] Deprecated `--resource-group` parameter in the commands:</span></span>
  * `acr login`
  * `acr repository`
  * `acr helm`

### <a name="acs"></a><span data-ttu-id="8cc5e-996">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-996">ACS</span></span>
* <span data-ttu-id="8cc5e-997">新しい ACI リージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-997">Added support for new ACI regions</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-998">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-998">Appservice</span></span>
* <span data-ttu-id="8cc5e-999">ASE RG とアプリ RG の異なる ASE でホストされているアプリの証明書のアップロードに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-999">Fixed issue with uploading certificates for apps that are hosted on an ASE, where the ASE RG & App RG are different</span></span>
* <span data-ttu-id="8cc5e-1000">Linux 用の既定値として SKU P1V1 を使用するように `webapp up` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1000">Changed `webapp up` to use SKU P1V1 as default for Linux</span></span>
* <span data-ttu-id="8cc5e-1001">デプロイが失敗したときに、適切なエラー メッセージが表示されるように `[webapp|functionapp] deployment source config-zip` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1001">Fixed `[webapp|functionapp] deployment source config-zip` to show the right error message when a deployment fails</span></span> 
* <span data-ttu-id="8cc5e-1002">`webapp ssh` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1002">Added `webapp ssh` command</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-1003">Botservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1003">Botservice</span></span>
* <span data-ttu-id="8cc5e-1004">デプロイ状態の更新プログラムを `bot create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1004">Added deployment status updates to `bot create`</span></span>

### <a name="configure"></a><span data-ttu-id="8cc5e-1005">構成</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1005">Configure</span></span>
* <span data-ttu-id="8cc5e-1006">構成可能な出力形式として `none` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1006">Added `none` as a configurable output format</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-1007">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1007">CosmosDB</span></span>
* <span data-ttu-id="8cc5e-1008">共有スループットを使用したデータベース作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1008">Added support for creating database with shared throughput</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-1009">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1009">HDInsight</span></span>
* <span data-ttu-id="8cc5e-1010">アプリケーションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1010">Added commands for managing applications</span></span>
* <span data-ttu-id="8cc5e-1011">スクリプト アクションを管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1011">Added commands for managing script actions</span></span>
* <span data-ttu-id="8cc5e-1012">Operations Management Suite (OMS) を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1012">Added commands for managing Operations Management Suite (OMS)</span></span>
* <span data-ttu-id="8cc5e-1013">リージョンの使用状況を一覧表するためのサポートを `hdinsight list-usage` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1013">Added support to list regional usage to `hdinsight list-usage`</span></span>
* <span data-ttu-id="8cc5e-1014">[重大な変更] 既定のクラスターの種類を `hdinsight create` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1014">[BREAKING CHANGE] Removed default cluster type from `hdinsight create`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1015">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1015">Network</span></span>
* <span data-ttu-id="8cc5e-1016">`--custom-headers` 引数と `--status-code-ranges` 引数を `traffic-manager profile [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1016">Added `--custom-headers` and `--status-code-ranges` arguments to `traffic-manager profile [create|update]`</span></span>
* <span data-ttu-id="8cc5e-1017">新しいルーティングの種類として、サブネットと複数値を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1017">Added new routing types: Subnet and Multivalue</span></span>
* <span data-ttu-id="8cc5e-1018">`--custom-headers` 引数と `--subnets` 引数を `traffic-manager endpoint [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1018">Added `--custom-headers` and `--subnets` arguments to `traffic-manager endpoint [create|update]`</span></span>  
* <span data-ttu-id="8cc5e-1019">`ddos-protection update` に `--vnets ""` を指定するとエラーが発生する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1019">Fixed issue where supplying `--vnets ""` to `ddos-protection update` caused an error</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1020">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1020">Role</span></span>
* <span data-ttu-id="8cc5e-1021">[非推奨] `create-for-rbac` の `--password` 引数を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1021">[DEPRECATED] Deprecated `--password` argument for `create-for-rbac`.</span></span> <span data-ttu-id="8cc5e-1022">代わりに、CLI によって生成された安全なパスワードを使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1022">Use secure passwords generated by the CLI instead</span></span>

### <a name="security"></a><span data-ttu-id="8cc5e-1023">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1023">Security</span></span>
* <span data-ttu-id="8cc5e-1024">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1024">Initial Release</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1025">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1025">Storage</span></span>
* <span data-ttu-id="8cc5e-1026">[重大な変更] 既定の結果数が 5,000 になるように `storage [blob|file|container|share] list` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1026">[BREAKING CHANGE] Changed `storage [blob|file|container|share] list` default number of results to be 5,000.</span></span> <span data-ttu-id="8cc5e-1027">すべての結果を返す元の動作が必要な場合は `--num-results *` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1027">Use `--num-results *` for original behavior of returning all results</span></span>
* <span data-ttu-id="8cc5e-1028">`--marker` パラメーターを `storage [blob|file|container|share] list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1028">Added `--marker` parameter to `storage [blob|file|container|share] list`</span></span>
* <span data-ttu-id="8cc5e-1029">次のページを表すログ マーカーを `storage [blob|file|container|share] list` の STDERR に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1029">Added log marker for next page to STDERR for `storage [blob|file|container|share] list`</span></span> 
* <span data-ttu-id="8cc5e-1030">静的 Web サイトをサポートする `storage blob service-properties update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1030">Added `storage blob service-properties update` command with support for static websites</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1031">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1031">VM</span></span>
* <span data-ttu-id="8cc5e-1032">より一貫性のあるパラメーターが指定されるように `vm [disk|unmanaged-disk]` と `vmss disk` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1032">Changed `vm [disk|unmanaged-disk]` and `vmss disk` to have more consistent parameters</span></span>
* <span data-ttu-id="8cc5e-1033">テナント イメージ相互参照のサポートを `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1033">Added support for cross tenant image referencing to `[vm|vmss] create`</span></span>
* <span data-ttu-id="8cc5e-1034">`vm diagnostics get-default-config --windows-os` の既定の構成に関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1034">Fixed bug with default configuration in `vm diagnostics get-default-config --windows-os`</span></span>
* <span data-ttu-id="8cc5e-1035">拡張機能を設定する前に拡張機能をプロビジョニングしておく必要があるかを定義するために、`--provision-after-extensions` 引数を `vmss extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1035">Added argument `--provision-after-extensions` to `vmss extension set` to define what extensions must be provisioned before the extension being set</span></span>
* <span data-ttu-id="8cc5e-1036">既定のレプリケーション数を設定できるように、`--replica-count` 引数を `sig image-version update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1036">Added argument `--replica-count` to `sig image-version update` for setting the default replication count</span></span>
* <span data-ttu-id="8cc5e-1037">完全なリソース ID を指定しているにもかかわらず、ソース OS ディスクが同じ名前の VM と取り違えられる `image create --source` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1037">Fixed bug with `image create --source` where source os disk is mistaken for a VM with the same name, even if the full resource ID is provided</span></span>

## <a name="december-20-2018"></a><span data-ttu-id="8cc5e-1038">2018 年 12 月 20 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1038">December 20, 2018</span></span>

<span data-ttu-id="8cc5e-1039">バージョン 2.0.54</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1039">Version 2.0.54</span></span>
### <a name="appservice"></a><span data-ttu-id="8cc5e-1040">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1040">Appservice</span></span>
* <span data-ttu-id="8cc5e-1041">`webapp up` で再デプロイが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1041">Fixed issue where `webapp up` would fail to redeploy</span></span>
* <span data-ttu-id="8cc5e-1042">Web アプリのスナップショットの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1042">Added support for listing and restoring webapp snapshots</span></span>
* <span data-ttu-id="8cc5e-1043">`--runtime` フラグのサポートを Windows 関数アプリに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1043">Added support for `--runtime` flag to Windows function apps</span></span>

### <a name="iotcentral"></a><span data-ttu-id="8cc5e-1044">IoTCentral</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1044">IoTCentral</span></span>
* <span data-ttu-id="8cc5e-1045">更新コマンドの API 呼び出しを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1045">Fixed update command API call</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1046">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1046">Role</span></span>
* <span data-ttu-id="8cc5e-1047">[重大な変更] 既定では最初の 100 個のオブジェクトのみを一覧表示するように、`ad [app|sp] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1047">[BREAKING CHANGE] Changed `ad [app|sp] list` to only list the first 100 objects by default</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1048">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1048">SQL</span></span>
* <span data-ttu-id="8cc5e-1049">マネージド インスタンスでカスタム照合順序のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1049">Added support for custom collation on managed instances</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1050">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1050">VM</span></span>
* <span data-ttu-id="8cc5e-1051">`---os-type` パラメーターを `disk create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1051">Added `---os-type` parameter to `disk create`</span></span>

## <a name="december-18-2018"></a><span data-ttu-id="8cc5e-1052">2018 年 12 月 18 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1052">December 18, 2018</span></span>

<span data-ttu-id="8cc5e-1053">バージョン 2.0.53</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1053">Version 2.0.53</span></span>
### <a name="acr"></a><span data-ttu-id="8cc5e-1054">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1054">ACR</span></span>
* <span data-ttu-id="8cc5e-1055">外部のコンテナー レジストリからのイメージのインポートのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1055">Added support for image import from external Container Registries</span></span>
* <span data-ttu-id="8cc5e-1056">タスク一覧のテーブルのレイアウトを縮小しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1056">Condensed the table layout for task list</span></span>
* <span data-ttu-id="8cc5e-1057">Azure DevOps の URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1057">Added support for Azure DevOps URLs</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1058">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1058">ACS</span></span>
* <span data-ttu-id="8cc5e-1059">仮想ノードのプレビューを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1059">Added Virtual Nodes Preview</span></span>
* <span data-ttu-id="8cc5e-1060">`aks create` の AAD 引数から "(プレビュー)" を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1060">Removed "(PREVIEW)" from AAD arguments to `aks create`</span></span>
* <span data-ttu-id="8cc5e-1061">[非推奨] `az acs` コマンドを非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1061">[DEPRECATED] Deprecated `az acs` commands.</span></span> <span data-ttu-id="8cc5e-1062">ACS サービスは 2020 年 1 月 31 日に廃止予定</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1062">The ACS service will retire on January 31, 2020</span></span>
* <span data-ttu-id="8cc5e-1063">新しい AKS クラスターの作成時のネットワーク ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1063">Added support of Network Policy when creating new AKS clusters</span></span>
* <span data-ttu-id="8cc5e-1064">nodepool が 1 つのみの場合に `aks scale` に求められる `--nodepool-name` 引数の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1064">Removed requirement of `--nodepool-name` argument for `aks scale` if there's only one nodepool</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1065">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1065">Appservice</span></span>
* <span data-ttu-id="8cc5e-1066">`webapp config container` で `--slot` パラメーターが許可されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1066">Fixed issue where `webapp config container` did not honor `--slot` parameter</span></span>

### <a name="botservice"></a><span data-ttu-id="8cc5e-1067">Botservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1067">Botservice</span></span>
* <span data-ttu-id="8cc5e-1068">`bot show` の呼び出し時に `.bot` ファイルの解析のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1068">Added support for `.bot` file parsing when calling `bot show`</span></span>
* <span data-ttu-id="8cc5e-1069">AppInsights のプロビジョニングのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1069">Fixed AppInsights provisioning bug</span></span>
* <span data-ttu-id="8cc5e-1070">ファイル パスを処理するときの空白文字のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1070">Fixed whitespace bug when dealing with file paths</span></span>
* <span data-ttu-id="8cc5e-1071">Kudu ネットワーク呼び出しを削減しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1071">Reduced Kudu network calls</span></span>
* <span data-ttu-id="8cc5e-1072">一般的なコマンド UX を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1072">General command UX improvements</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-1073">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1073">Consumption</span></span>
* <span data-ttu-id="8cc5e-1074">予算 API での通知の表示のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1074">Fixed bugs for budget API to show notifications</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-1075">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1075">CosmosDB</span></span>
* <span data-ttu-id="8cc5e-1076">マルチマスターからシングルマスターへのアカウントの更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1076">Added support for updating account from multi-master to single-master</span></span>

### <a name="maps"></a><span data-ttu-id="8cc5e-1077">マップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1077">Maps</span></span>
* <span data-ttu-id="8cc5e-1078">S1 SKU のサポートを `maps account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1078">Added support for the S1 SKU to `maps account [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1079">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1079">Network</span></span>
* <span data-ttu-id="8cc5e-1080">`--format` と `--log-version` のサポートを `watcher flow-log configure` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1080">Added support for `--format` and `--log-version` to `watcher flow-log configure`</span></span>
* <span data-ttu-id="8cc5e-1081">解決仮想ネットワークと登録仮想ネットワークをクリアするために "" を使用しても機能しないときの `dns zone update` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1081">Fixed issue with `dns zone update` where using "" to clear resolution and registration VNets didn't work</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1082">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1082">Resource</span></span>
* <span data-ttu-id="8cc5e-1083">`policy assignment [create|list|delete|show|update]` の管理グループのスコープ パラメーターの処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1083">Fixed handling of scope parameter for management groups in `policy assignment [create|list|delete|show|update]`</span></span> 
* <span data-ttu-id="8cc5e-1084">新しいコマンド `resource wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1084">Added new command `resource wait`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1085">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1085">Storage</span></span>
*  <span data-ttu-id="8cc5e-1086">`storage logging update` でストレージ サービスのログ スキーマのバージョンを更新する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1086">Added ability to update log schema version for storage services in `storage logging update`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1087">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1087">VM</span></span>
* <span data-ttu-id="8cc5e-1088">指定された VM に割り当てられているマネージド サービス ID がない場合の `vm identity remove` でのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1088">Fixed crash in `vm identity remove` when the specified vm has no assigned managed service identities</span></span>

## <a name="december-4-2018"></a><span data-ttu-id="8cc5e-1089">2018 年 12 月 4 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1089">December 4, 2018</span></span>

<span data-ttu-id="8cc5e-1090">バージョン 2.0.52</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1090">Version 2.0.52</span></span>
### <a name="core"></a><span data-ttu-id="8cc5e-1091">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1091">Core</span></span>
* <span data-ttu-id="8cc5e-1092">マルチテナント サービス プリンシパルのクロス テナント リソース プロビジョニングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1092">Added support for cross tenant resource provisioning for multi-tenant service principal</span></span>
* <span data-ttu-id="8cc5e-1093">tsv 出力するコマンドからパイプ処理された ID が適切に解析されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1093">Fixed bug where ids piped from a command with tsv output was improperly parsed</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1094">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1094">Appservice</span></span>
* <span data-ttu-id="8cc5e-1095">[プレビュー] コンテンツを作成してアプリに展開する際に役立つ `webapp up` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1095">[PREVIEW] Added `webapp up` command that helps in creating & deploying contents to app</span></span>
* <span data-ttu-id="8cc5e-1096">バックエンドの変更に起因するコンテナー ベースの Windows アプリのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1096">Fixed a bug on container based windows app due to backend change</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1097">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1097">Network</span></span>
* <span data-ttu-id="8cc5e-1098">WAF 除外をサポートするために、`application-gateway waf-config set` に `--exclusion` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1098">Added `--exclusion` argument to `application-gateway waf-config set` to support WAF exclusions</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1099">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1099">Role</span></span>
* <span data-ttu-id="8cc5e-1100">パスワード資格情報のカスタム識別子のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1100">Added support for custom identifiers for password credential</span></span> 

### <a name="vm"></a><span data-ttu-id="8cc5e-1101">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1101">VM</span></span>
* <span data-ttu-id="8cc5e-1102">[非推奨] `vm extension [show|wait] --expand` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1102">[DEPRECATED] Deprecated `vm extension [show|wait] --expand` parameter</span></span>
* <span data-ttu-id="8cc5e-1103">応答しない VM を再デプロイするために、`vm restart` に `--force` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1103">Added `--force` parameter to `vm restart` to redeploy unresponsive VMs</span></span>
* <span data-ttu-id="8cc5e-1104">パスワードと SSH 認証の両方を使用して VM を作成するために、"all" を受け入れるように `[vm|vmss] create --authentication-type` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1104">Changed `[vm|vmss] create --authentication-type` to accept "all" to create a VM with both password and ssh authentication</span></span>
* <span data-ttu-id="8cc5e-1105">イメージの OS ディスク キャッシュを設定するための `image create --os-disk-caching` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1105">Added `image create --os-disk-caching` parameter to set os disk caching for an image</span></span>

## <a name="november-20-2018"></a><span data-ttu-id="8cc5e-1106">2018 年 11 月 20 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1106">November 20, 2018</span></span>

<span data-ttu-id="8cc5e-1107">バージョン 2.0.51</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1107">Version 2.0.51</span></span>
### <a name="core"></a><span data-ttu-id="8cc5e-1108">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1108">Core</span></span>
* <span data-ttu-id="8cc5e-1109">ID のサブスクリプション名を再利用しないように MSI ログインを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1109">Changed MSI login to not reuse subscription name in identity</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1110">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1110">ACR</span></span>
* <span data-ttu-id="8cc5e-1111">タスク ステップにコンテキスト トークンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1111">Added context token to task step</span></span>
* <span data-ttu-id="8cc5e-1112">ACR タスクをミラーリングするために、ACR 実行でシークレットを設定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1112">Added support for setting secrets in acr run to mirror acr task</span></span>
* <span data-ttu-id="8cc5e-1113">`show-tags` および `show-manifests` コマンドの `--top` と `--orderby` のサポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1113">Improved support for `--top` and `--orderby` for `show-tags` and `show-manifests` commands</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1114">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1114">Appservice</span></span>
* <span data-ttu-id="8cc5e-1115">ZIP デプロイの既定のタイムアウトを変更し、状態のポーリングを 5 分に増やしました。また、この値をカスタマイズするためのタイムアウト プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1115">Changed zip deployment default timeout to poll for the status increased to 5 mins, also adding a timeout property to customize this value</span></span>
* <span data-ttu-id="8cc5e-1116">既定の `node_version` を更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1116">Updated the default `node_version`.</span></span> <span data-ttu-id="8cc5e-1117">2 フェーズのスワップ時にスロット スワップ アクションをリセットしても、appsettings と接続文字列はすべて保持されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1117">Resetting slot swap action, during a two phase swap preserves all the appsettings & connection strings</span></span>
* <span data-ttu-id="8cc5e-1118">Linux App Service プラン作成時のクライアント側の SKU チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1118">Removed client-side SKU check for Linux app service plan create</span></span>
* <span data-ttu-id="8cc5e-1119">zipdeploy の状態を取得しようとしたときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1119">Fixed error when trying to get zipdeploy status</span></span>

### <a name="iotcentral"></a><span data-ttu-id="8cc5e-1120">IotCentral</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1120">IotCentral</span></span>
* <span data-ttu-id="8cc5e-1121">IoT Central アプリケーションの作成時にサブドメインの可用性チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1121">Added subdomain availability check when creating an IoT Central application</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-1122">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1122">KeyVault</span></span>
* <span data-ttu-id="8cc5e-1123">エラーが無視される場合があるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1123">Fixed bug where errors may have been ignored</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1124">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1124">Network</span></span>
* <span data-ttu-id="8cc5e-1125">信頼されたルート証明書を処理するために、`application-gateway` に `root-cert` サブコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1125">Added `root-cert` subcommands to `application-gateway` to handle trusted root certifcates</span></span>
* <span data-ttu-id="8cc5e-1126">`application-gateway [create|update]` に、`--min-capacity` および `--custom-error-pages` オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1126">Added `--min-capacity` and `--custom-error-pages` options to `application-gateway [create|update]`:</span></span>
* <span data-ttu-id="8cc5e-1127">`application-gateway create` に、可用性ゾーンをサポートするための `--zones` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1127">Added `--zones` for availability zone support to `application-gateway create`</span></span> 
* <span data-ttu-id="8cc5e-1128">`application-gateway waf-config set` に、引数 `--file-upload-limit`、`--max-request-body-size`、`--request-body-check` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1128">Added arguments `--file-upload-limit`, `--max-request-body-size` and `--request-body-check` to `application-gateway waf-config set`</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1129">Rdbms</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1129">Rdbms</span></span>
* <span data-ttu-id="8cc5e-1130">mariadb vnet コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1130">Added mariadb vnet commands</span></span>

### <a name="rbac"></a><span data-ttu-id="8cc5e-1131">Rbac</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1131">Rbac</span></span>
* <span data-ttu-id="8cc5e-1132">`ad app update` で変更できない資格情報を更新しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1132">Fixed an issue with attempting to update immutable credentials in `ad app update`</span></span>
* <span data-ttu-id="8cc5e-1133">近い将来の `ad [app|sp] list` の破壊的変更を伝えるための出力に関する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1133">Added output warnings to communicate breaking changes in the near future for `ad [app|sp] list`</span></span> 

### <a name="storage"></a><span data-ttu-id="8cc5e-1134">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1134">Storage</span></span>
* <span data-ttu-id="8cc5e-1135">ストレージ コピー コマンドのまれに発生するケースの処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1135">Improved handling of corner cases for storage copy commands</span></span>
* <span data-ttu-id="8cc5e-1136">コピー先アカウントとコピー元アカウントが同じである場合にログイン資格情報を使用しない、`storage blob copy start-batch` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1136">Fixed issue with `storage blob copy start-batch` not using login credentials when the destination and source accounts are the same</span></span>
* <span data-ttu-id="8cc5e-1137">`sas_token` が URL に組み込まれない `storage [blob|file] url` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1137">Fixed bug with`storage [blob|file] url` where `sas_token` wasn't incorporated into URL</span></span>
* <span data-ttu-id="8cc5e-1138">`[blob|container] list` に破壊的変更に関する警告を追加しました。既定で最初の 5000 個の結果のみがすぐに出力されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1138">Added breaking change warning to `[blob|container] list`: will soon output only first 5000 results by default</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1139">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1139">VM</span></span>
* <span data-ttu-id="8cc5e-1140">`[vm|vmss] create --storage-sku` に、マネージド OS ディスクとデータ ディスクのストレージ アカウント SKU を個別に指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1140">Added support to `[vm|vmss] create --storage-sku` to specify the storage account SKU for managed OS and data disks separately</span></span>
* <span data-ttu-id="8cc5e-1141">`sig image-version` のバージョン名パラメーターを `--image-version -e` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1141">Changed version name parameters to `sig image-version` to be `--image-version -e`</span></span>
* <span data-ttu-id="8cc5e-1142">`sig image-version` の引数 `--image-version-name` が非推奨になり、`--image-version` に置き換えられました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1142">Deprecated `sig image-version` argument `--image-version-name`, replaced by `--image-version`</span></span>
* <span data-ttu-id="8cc5e-1143">`[vm|vmss] create --ephemeral-os-disk` に、ローカル OS ディスクを使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1143">Added support to use local OS disk to `[vm|vmss] create --ephemeral-os-disk`</span></span>
* <span data-ttu-id="8cc5e-1144">`--no-wait` のサポートを `snapshot create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1144">Added support for `--no-wait` to `snapshot create/update`</span></span>
* <span data-ttu-id="8cc5e-1145">`snapshot wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1145">Added `snapshot wait` command</span></span>
* <span data-ttu-id="8cc5e-1146">`[vm|vmss] extension set --extension-instance-name` でインスタンス名を使用するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1146">Added support for using instance name with `[vm|vmss] extension set --extension-instance-name`</span></span>

## <a name="november-6-2018"></a><span data-ttu-id="8cc5e-1147">2018 年 11 月 6 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1147">November 6, 2018</span></span>

<span data-ttu-id="8cc5e-1148">バージョン 2.0.50</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1148">Version 2.0.50</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1149">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1149">Core</span></span>
* <span data-ttu-id="8cc5e-1150">サービス プリンシパル インスタンスと発行者による認証に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1150">Added support for service principal sn+issuer auth</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1151">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1151">ACR</span></span>
* <span data-ttu-id="8cc5e-1152">タスク ソース トリガーのコミットおよび pull request の Git イベントに対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1152">Added support for commit and pull request git events for Task source trigger</span></span>
* <span data-ttu-id="8cc5e-1153">ビルド コマンドで指定されていない場合、既定の Dockerfile を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1153">Changed to use default Dockerfile if it's not specified in build command</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1154">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1154">ACS</span></span>
* <span data-ttu-id="8cc5e-1155">[重大な変更] 既定で 'az aks browse' が有効になるように、`enable_cloud_console_aks_browse` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1155">[BREAKING CHANGE] Removed `enable_cloud_console_aks_browse` to enable 'az aks browse' by default</span></span>

### <a name="advisor"></a><span data-ttu-id="8cc5e-1156">Advisor</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1156">Advisor</span></span>
* <span data-ttu-id="8cc5e-1157">GA リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1157">GA release</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-1158">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1158">AMS</span></span>
* <span data-ttu-id="8cc5e-1159">次の新しいコマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1159">Added new command groups:</span></span>
  *  `ams account-filter`
  *  `ams asset-filter`
  *  `ams content-key-policy`
  *  `ams live-event`
  *  `ams live-output`
  *  `ams streaming-endpoint`
  *  `ams mru`
* <span data-ttu-id="8cc5e-1160">次の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1160">Added new commands:</span></span>
  * `ams account check-name`
  * `ams job update`
  * `ams asset get-encryption-key`
  * `ams asset get-streaming-locators`
  * `ams streaming-locator get-content-keys`
* <span data-ttu-id="8cc5e-1161">暗号化パラメーターのサポートを `ams streaming-policy create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1161">Added encryption parameters support to `ams streaming-policy create`</span></span>
* <span data-ttu-id="8cc5e-1162">`ams transform output remove` にサポートを追加しました。削除する出力インデックスを渡すことで実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1162">Added support to `ams transform output remove` now can be performed by passing the output index to remove</span></span>
* <span data-ttu-id="8cc5e-1163">`--correlation-data` と `--label` の各引数を `ams job` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1163">Added `--correlation-data` and `--label` arguments to `ams job` command group</span></span>
* <span data-ttu-id="8cc5e-1164">`--storage-account` と `--container` の各引数を `ams asset` コマンド グループに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1164">Added `--storage-account` and `--container` arguments to `ams asset` command group</span></span>
* <span data-ttu-id="8cc5e-1165">`ams asset get-sas-url` コマンドに有効期限 (現在 + 23 時間) とアクセス許可 (読み取り) の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1165">Added default values for expiry time (Now+23h) and permissions (Read) in `ams asset get-sas-url` command</span></span> 
* <span data-ttu-id="8cc5e-1166">[重大な変更] `ams streaming locator` コマンドを `ams streaming-locator` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1166">[BREAKING CHANGE] Replaced `ams streaming locator` command with `ams streaming-locator`</span></span>
* <span data-ttu-id="8cc5e-1167">[重大な変更] `ams streaming locator` の `--content-keys` 引数を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1167">[BREAKING CHANGE] Updated `--content-keys` argument of `ams streaming locator`</span></span>
* <span data-ttu-id="8cc5e-1168">[重大な変更] `ams streaming locator` コマンドの `--content-policy-name` の名前を `--content-key-policy-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1168">[BREAKING CHANGE] Renamed `--content-policy-name` to `--content-key-policy-name` in `ams streaming locator` command</span></span>
* <span data-ttu-id="8cc5e-1169">[重大な変更] `ams streaming policy` コマンドを `ams streaming-policy` で置き換えました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1169">[BREAKING CHANGE] Replaced `ams streaming policy` command with `ams streaming-policy`</span></span>
* <span data-ttu-id="8cc5e-1170">[重大な変更] `ams transform` コマンド グループの `--preset-names` 引数を `--preset` で置き換えました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1170">[BREAKING CHANGE] Replaced `--preset-names` argument with `--preset` in `ams transform` command group.</span></span> <span data-ttu-id="8cc5e-1171">現在同時に設定できるのは、1 つの出力/プリセットのみです (さらに追加するには `ams transform output add` を実行する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1171">Now you can only set 1 output/preset at a time (to add more you have to run `ams transform output add`).</span></span> <span data-ttu-id="8cc5e-1172">また、カスタムの JSON にパスを渡すことで、カスタム StandardEncoderPreset を設定することもできます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1172">Also, you can set custom StandardEncoderPreset by passing the path to your custom JSON</span></span>
* <span data-ttu-id="8cc5e-1173">[重大な変更] `ams job start` コマンドの `--output-asset-names ` の名前を `--output-assets` に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1173">[BREAKING CHANGE] Renamed `--output-asset-names ` to `--output-assets` in `ams job start` command.</span></span> <span data-ttu-id="8cc5e-1174">"assetName=label" 形式の、スペース区切りのアセットのリストを受け入れるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1174">Now it accepts a space-separated list of assets in 'assetName=label' format.</span></span> <span data-ttu-id="8cc5e-1175">"assetName=" のようなラベルのないアセットを送信できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1175">An asset without label can be sent like this: 'assetName='</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1176">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1176">AppService</span></span>
* <span data-ttu-id="8cc5e-1177">バックアップ スケジュールがまだ設定されていない場合はバックアップ スケジュールを設定できないという `az webapp config backup update` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1177">Fixed a bug in `az webapp config backup update` that prevents setting a backup schedule if one is not already set</span></span>

### <a name="configure"></a><span data-ttu-id="8cc5e-1178">構成</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1178">Configure</span></span>
* <span data-ttu-id="8cc5e-1179">YAML を出力形式のオプションに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1179">Added YAML to output format options</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1180">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1180">Container</span></span>
* <span data-ttu-id="8cc5e-1181">YAML にコンテナー グループをエクスポートするときに、ID を表示するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1181">Changed to show identity when exporting a container group to yaml</span></span>

### <a name="eventhub"></a><span data-ttu-id="8cc5e-1182">EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1182">EventHub</span></span>
* <span data-ttu-id="8cc5e-1183">`eventhub namespace [create|update]` で、Kafka をサポートするように `--enable-kafka` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1183">Added `--enable-kafka` flag to support Kafka in `eventhub namespace [create|update]`</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1184">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1184">Interactive</span></span>
* <span data-ttu-id="8cc5e-1185">対話型で `interactive` 拡張機能をインストールするようになりました。これにより、迅速な更新とサポートが可能になります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1185">Interactive now installs the `interactive` extension, which will allow for faster updates and support</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-1186">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1186">Monitor</span></span>
* <span data-ttu-id="8cc5e-1187">`monitor metrics alert [create|update]` の `--condition` で、フォワードスラッシュ (/) とピリオド (.) の文字を含むメトリック名がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1187">Added support for metric names  which include characters forward-slash (/) and period (.) to `--condition` in `monitor metrics alert [create|update]`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1188">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1188">Network</span></span>
* <span data-ttu-id="8cc5e-1189">`network private-endpoint` を優先して、`network interface-endpoint` コマンド名を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1189">Deprecated `network interface-endpoint` command names in favor of `network private-endpoint`</span></span>
* <span data-ttu-id="8cc5e-1190">`express-route peering connection create` の `--peer-circuit` 引数が ID を受け入れない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1190">Fixed issue with where `--peer-circuit` argument in `express-route peering connection create`would not accept an ID</span></span>
* <span data-ttu-id="8cc5e-1191">`public-ip create` で `--ip-tags` が正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1191">Fixed issue where `--ip-tags` did not work correctly with `public-ip create`</span></span> 

### <a name="profile"></a><span data-ttu-id="8cc5e-1192">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1192">Profile</span></span>
* <span data-ttu-id="8cc5e-1193">証明書の自動ロールでサービス プリンシパルのログインが可能になるように `--use-cert-sn-issuer` を `az login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1193">Added `--use-cert-sn-issuer` to `az login` for service principal login with cert auto-rolls</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1194">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1194">RDBMS</span></span>
* <span data-ttu-id="8cc5e-1195">mysql replica コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1195">Added mysql replica commands</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1196">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1196">Resource</span></span>
* <span data-ttu-id="8cc5e-1197">管理グループとサブスクリプションのサポートを `policy definition|set-definition` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1197">Added support for management groups and subscriptions to `policy definition|set-definition` commands</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1198">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1198">Role</span></span>
* <span data-ttu-id="8cc5e-1199">API アクセス許可の管理、サインインしているユーザー、およびアプリケーションのパスワードと証明書の資格情報管理のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1199">Added support for API permission management, signed-in-user, and application password & certificate credential management</span></span>
* <span data-ttu-id="8cc5e-1200">displayName とサービス プリンシパル名を取り違えないように、`ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1200">Changed `ad sp create-for-rbac` to clarify the confusion between displayName and service principal name</span></span>
* <span data-ttu-id="8cc5e-1201">AAD アプリにアクセス許可を付与するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1201">Added support to grant permissions to AAD apps</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1202">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1202">Storage</span></span>
* <span data-ttu-id="8cc5e-1203">アカウント名またはキーなしで、SAS とエンドポイントのみを使用してストレージ サービスに接続するサポートを追加しました (`Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>` を参照してください)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1203">Added support to connect to storage services only with SAS and endpoints (without an account name or a key) as described in `Configure Azure Storage connection strings <https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string>`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1204">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1204">VM</span></span>
* <span data-ttu-id="8cc5e-1205">イメージの既定のストレージ アカウントの種類を設定できるように、`storage-sku` 引数を `image create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1205">Added `storage-sku` argument to `image create` for setting the image's default storage account type</span></span>
* <span data-ttu-id="8cc5e-1206">`--no-wait` オプションでコマンドがクラッシュする `vm resize` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1206">Fixed bug with `vm resize` where `--no-wait` option causes command to crash</span></span>
* <span data-ttu-id="8cc5e-1207">状態が表示されるように `vm encryption show` のテーブル出力形式を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1207">Changed `vm encryption show` table output format to show status</span></span>
* <span data-ttu-id="8cc5e-1208">json/jsonc 出力を要求するように `vm secret format` を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1208">Changed `vm secret format` to require json/jsonc output.</span></span> <span data-ttu-id="8cc5e-1209">望ましくない出力形式が選択された場合、ユーザーに警告し、既定値が json 出力になります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1209">Warns user and defaults to json output if an undesired output format is selected</span></span>
* <span data-ttu-id="8cc5e-1210">`vm create --image` の引数検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1210">Improved argument validation for `vm create --image`</span></span>

## <a name="october-23-2018"></a><span data-ttu-id="8cc5e-1211">2018 年 10 月 23 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1211">October 23, 2018</span></span>

<span data-ttu-id="8cc5e-1212">バージョン 2.0.49</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1212">Version 2.0.49</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1213">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1213">Core</span></span>
* <span data-ttu-id="8cc5e-1214">`--subscription` が `--ids` のサブスクリプションよりも優先される場合の `--ids` に関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1214">Fixed issue with `--ids` where `--subscription` would take precedence over the subscription in `--ids`</span></span>
* <span data-ttu-id="8cc5e-1215">`--ids` を使用してパラメーターを無視するときの明示的な警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1215">Added explicit warnings when parameters would be ignored by use of `--ids`</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1216">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1216">ACR</span></span>
* <span data-ttu-id="8cc5e-1217">Python2 の ACR ビルドのエンコードの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1217">Fixed an ACR Build encoding issue in Python2</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-1218">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1218">CDN</span></span>
* <span data-ttu-id="8cc5e-1219">[重大な変更] `cdn endpoint create` のクエリ文字列の既定のキャッシュ動作が変更され、"IgnoreQueryString" が既定値ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1219">[BREAKING CHANGE] Changed `cdn endpoint create`'s default query string caching behaviour to no longer defaults to "IgnoreQueryString".</span></span> <span data-ttu-id="8cc5e-1220">これはサービスによって設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1220">It is now set by the service</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1221">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1221">Container</span></span>
* <span data-ttu-id="8cc5e-1222">"--ip-address" に渡す有効な型として、`Private` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1222">Added `Private` as a valid type to pass to '--ip-address'</span></span>
* <span data-ttu-id="8cc5e-1223">サブネット ID のみを使用して、コンテナー グループの仮想ネットワークを設定できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1223">Changed to allow using only subnet ID to setup a virtual network for the container group</span></span>
* <span data-ttu-id="8cc5e-1224">VNet 名またはリソース ID を使用して、さまざまなリソース グループの VNet を使用できるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1224">Changed to allow using vnet name or resource id to enable using vnets from different resource groups</span></span>
* <span data-ttu-id="8cc5e-1225">コンテナー グループに MSI ID を追加するための `--assign-identity` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1225">Added `--assign-identity` for adding a MSI identity to a container group</span></span>
* <span data-ttu-id="8cc5e-1226">システム割り当て MSI ID のロールの割り当てを作成するために、`--scope` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1226">Added `--scope` to create a role assignment for the system assigned MSI identity</span></span>
* <span data-ttu-id="8cc5e-1227">イメージを使用して、長時間実行プロセスなしでコンテナー グループを作成するときの警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1227">Added a warning when creating a container group with an image without a long running process</span></span>
* <span data-ttu-id="8cc5e-1228">`list` コマンドと `show` コマンドのテーブル出力の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1228">Fixed table output issues for `list` and `show` commands</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-1229">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1229">CosmosDB</span></span>
* <span data-ttu-id="8cc5e-1230">`cosmosdb create` に `--enable-multiple-write-locations` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1230">Added `--enable-multiple-write-locations` support to `cosmosdb create`</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1231">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1231">Interactive</span></span>
* <span data-ttu-id="8cc5e-1232">パラメーターにグローバル サブスクリプション パラメーターが確実に表示されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1232">Changed to ensure global subscription parameter appears in parameters</span></span>

### <a name="iot-central"></a><span data-ttu-id="8cc5e-1233">IoT Central</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1233">IoT Central</span></span>
* <span data-ttu-id="8cc5e-1234">IoT Central アプリケーションを作成するためのテンプレートと表示名のオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1234">Added template and display name options for IoT Central Application creation</span></span>
* <span data-ttu-id="8cc5e-1235">[重大な変更] F1 SKU のサポートを削除しました。代わりに S1 SKU を使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1235">[BREAKING CHANGE] Removed support for the F1 SKU; Use S1 SKU instead</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-1236">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1236">Monitor</span></span>
* <span data-ttu-id="8cc5e-1237">`monitor activity-log list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1237">Changes to `monitor activity-log list`:</span></span>
  * <span data-ttu-id="8cc5e-1238">すべてのイベントをサブスクリプション レベルで一覧表示するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1238">Added support for listing all events at the subscription level</span></span>
  * <span data-ttu-id="8cc5e-1239">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1239">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="8cc5e-1240">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1240">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
  * <span data-ttu-id="8cc5e-1241">非推奨の `--resource-provider` オプションのエイリアスとして、`--namespace` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1241">Added `--namespace` as alias for deprecated option `--resource-provider`</span></span>
  * <span data-ttu-id="8cc5e-1242">厳密に型指定されたオプションを使用する値以外はサービスでサポートされていないため、`--filters` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1242">Deprecated `--filters` because no values other than those with strongly-typed options are supported by the service</span></span>
* <span data-ttu-id="8cc5e-1243">`monitor metrics list` の変更点:</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1243">Changes to `monitor metrics list`:</span></span>
  * <span data-ttu-id="8cc5e-1244">時間クエリをより簡単に作成できるように、`--offset` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1244">Added `--offset` parameter to more easily create time queries</span></span>
  * <span data-ttu-id="8cc5e-1245">幅広い ISO8601 形式とユーザー フレンドリな datetime 形式を使用するために、`--start-time` と `--end-time` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1245">Improved validation for `--start-time` and `--end-time` to use wider range of ISO8601 formats and more user-friendly datetime formats</span></span>
* <span data-ttu-id="8cc5e-1246">`monitor diagnostic-settings create` の引数 `--event-hub` と `--event-hub-rule` の検証を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1246">Improved validation for `--event-hub` and `--event-hub-rule` arguments to `monitor diagnostic-settings create`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1247">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1247">Network</span></span>
* <span data-ttu-id="8cc5e-1248">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic create` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1248">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic create`, to support adding application gateway backend address pools to a NIC</span></span>
* <span data-ttu-id="8cc5e-1249">NIC へのアプリケーション ゲートウェイ バックエンド アドレス プールの追加をサポートするために、`nic ip-config create/update` に引数 `--app-gateway-address-pools` と `--gateway-name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1249">Added `--app-gateway-address-pools` and `--gateway-name` arguments to `nic ip-config create/update`, to support adding application gateway backend address pools to a NIC</span></span>

### <a name="servicebus"></a><span data-ttu-id="8cc5e-1250">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1250">ServiceBus</span></span>
* <span data-ttu-id="8cc5e-1251">Service Bus Standard から Premium 名前空間への移行の現在の状態を表示するために、MigrationConfigProperties に読み取り専用の `migration_state` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1251">Added Read-Only `migration_state` to MigrationConfigProperties to show current Service Bus Standard to Premium namespace migration state</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1252">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1252">SQL</span></span>
* <span data-ttu-id="8cc5e-1253">手動フェールオーバー ポリシーで機能するように、`sql failover-group create` と `sql failover-group update` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1253">Fixed `sql failover-group create` and `sql failover-group update` to work with Manual failover policy</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1254">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1254">Storage</span></span>
* <span data-ttu-id="8cc5e-1255">すべての項目に正しい "サービス" キーが表示されるように、`az storage cors list` の出力書式設定を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1255">Fixed `az storage cors list` output formatting, all items show correct "Service" key</span></span>
* <span data-ttu-id="8cc5e-1256">不変ポリシーによってブロックされたコンテナーの削除を可能にする `--bypass-immutability-policy` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1256">Added `--bypass-immutability-policy` parameter for immutability-policy blocked container deletion</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1257">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1257">VM</span></span>
* <span data-ttu-id="8cc5e-1258">`[vm|vmss] create` で、Lv/Lv2 シリーズのマシンに対して、ディスク キャッシュ モードが強制的に `None` に設定されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1258">Enforce disk caching mode be `None` for Lv/Lv2 series of machines in `[vm|vmss] create`</span></span>
* <span data-ttu-id="8cc5e-1259">`vm create` でネットワーク アクセラレータをサポートすることにより、サポートされているサイズのリストを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1259">Updated supported size list supporting networking accelerator for `vm create`</span></span>
* <span data-ttu-id="8cc5e-1260">`disk create` の ultrassd iops と mbps configs に、厳密に型指定された引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1260">Added strong typed arguments for ultrassd iops and mbps configs for `disk create`</span></span>

## <a name="october-16-2018"></a><span data-ttu-id="8cc5e-1261">2018 年 10 月 16 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1261">October 16, 2018</span></span>

<span data-ttu-id="8cc5e-1262">バージョン 2.0.48</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1262">Version 2.0.48</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1263">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1263">VM</span></span>
* <span data-ttu-id="8cc5e-1264">Homebrew のインストールが失敗する原因となっていた SDK の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1264">Fixed SDK issue that caused Homebrew instllation to fail</span></span>

## <a name="october-9-2018"></a><span data-ttu-id="8cc5e-1265">2018 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1265">October 9, 2018</span></span>

<span data-ttu-id="8cc5e-1266">バージョン 2.0.47</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1266">Version 2.0.47</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1267">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1267">Core</span></span>
* <span data-ttu-id="8cc5e-1268">"無効な要求" エラーのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1268">Improved error handling for "Bad Request" errors</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1269">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1269">ACR</span></span>
* <span data-ttu-id="8cc5e-1270">Helm クライアントと似たテーブル形式のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1270">Added support for similar table format as helm client</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1271">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1271">ACS</span></span>
* <span data-ttu-id="8cc5e-1272">nodepool 名を構成するために `aks [create|scale] --nodepool-name` を追加しました。12 文字に切り詰められており、既定値は nodepool1 です</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1272">Added `aks [create|scale] --nodepool-name` to configure nodepool name, truncated to 12 characters, default - nodepool1</span></span> 
* <span data-ttu-id="8cc5e-1273">Parimiko が失敗したときに "scp" にフォールバックするように修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1273">Fixed to fall back to 'scp' when Parimiko fails</span></span>
* <span data-ttu-id="8cc5e-1274">`--aad-tenant-id` が省略可能になるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1274">Changed `aks create` to no longer require `--aad-tenant-id`</span></span>
* <span data-ttu-id="8cc5e-1275">重複するエントリが存在するときの Kubernetes 資格情報のマージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1275">Improved merging of Kubernetes credentials when duplicate entries are present</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1276">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1276">Container</span></span>
* <span data-ttu-id="8cc5e-1277">特定のランタイムでの Linux 従量課金プランの種類の作成をサポートするように `functionapp create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1277">Changed `functionapp create` to support creating a Linux consumption plan type with a specific runtime</span></span>
* <span data-ttu-id="8cc5e-1278">[プレビュー] Windows コンテナーでの Web アプリのホストのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1278">[PREVIEW] Added support for hosting webapps on Windows containers</span></span>

### <a name="event-hub"></a><span data-ttu-id="8cc5e-1279">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1279">Event Hub</span></span>
* <span data-ttu-id="8cc5e-1280">`eventhub update` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1280">Fixed `eventhub update` command</span></span>
* <span data-ttu-id="8cc5e-1281">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1281">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="extensions"></a><span data-ttu-id="8cc5e-1282">Extensions</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1282">Extensions</span></span>
* <span data-ttu-id="8cc5e-1283">既にインストールされている拡張機能を追加しようとする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1283">Fixed issue with attempting to add an extension that is already installed</span></span>

### <a name="hdinsight"></a><span data-ttu-id="8cc5e-1284">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1284">HDInsight</span></span>
* <span data-ttu-id="8cc5e-1285">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1285">Initial release</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-1286">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1286">IoT</span></span>
* <span data-ttu-id="8cc5e-1287">拡張機能のインストール コマンドを初回実行時のバナーに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1287">Added extension installation comand to first-run banner</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-1288">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1288">KeyVault</span></span>
* <span data-ttu-id="8cc5e-1289">keyvault storage コマンドが最新の API プロファイルに制限されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1289">Changed to restrict keyvault storage commmands to the latest API profile</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1290">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1290">Network</span></span>
* <span data-ttu-id="8cc5e-1291">`network dns zone create` を修正しました:ユーザーが既定の場所を構成している場合でも、コマンドは成功します。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1291">Fixed `network dns zone create`: Command succeeds even if the user has configured a default location.</span></span> <span data-ttu-id="8cc5e-1292">#6052 を参照してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1292">See #6052</span></span>
* <span data-ttu-id="8cc5e-1293">`network vnet peering create` を使用できるため `--remote-vnet-id` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1293">Deprecated `--remote-vnet-id` for `network vnet peering create`</span></span>
* <span data-ttu-id="8cc5e-1294">`--remote-vnet` を `network vnet peering create` に追加しました。これは名前または ID を指定できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1294">Added `--remote-vnet` to `network vnet peering create` which accepts a name or ID</span></span>
* <span data-ttu-id="8cc5e-1295">`--subnet-prefixes` で `network vnet create` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1295">Added support for multiple subnet prefixes to `network vnet create` with `--subnet-prefixes`</span></span>
* <span data-ttu-id="8cc5e-1296">`--address-prefixes` で `network vnet subnet [create|update]` への複数のサブネット プレフィックスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1296">Added support for multiple subnet prefixes to `network vnet subnet [create|update]` with `--address-prefixes`</span></span>
* <span data-ttu-id="8cc5e-1297">`WAF_v2` または `Standard_v2` SKU でのゲートウェイの作成を妨げていた `network application-gateway create` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1297">Fixed issue with `network application-gateway create` that prevented creating gateways with `WAF_v2` or `Standard_v2` SKU</span></span>
* <span data-ttu-id="8cc5e-1298">`--service-endpoint-policy` の利便性の引数を `network vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1298">Added `--service-endpoint-policy` convenience argument to `network vnet subnet update`</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1299">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1299">Role</span></span>
* <span data-ttu-id="8cc5e-1300">Azure AD アプリ所有者を一覧表示するためのサポートを `ad app owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1300">Added support for listing Azure AD app owners to `ad app owner`</span></span>
* <span data-ttu-id="8cc5e-1301">Azure AD サービス プリンシパル所有者を一覧表示するためのサポートを `ad sp owner` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1301">Added support for listing Azure AD service principal owners to `ad sp owner`</span></span>
* <span data-ttu-id="8cc5e-1302">ロール定義の作成および更新コマンドが複数のアクセス許可構成を確実に受け入れるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1302">Changed to ensure role definition create & update commands accept multiple permission configurations</span></span>
* <span data-ttu-id="8cc5e-1303">ホーム ページの URI が確実かつ常に "https" になるように `ad sp create-for-rbac` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1303">Changed `ad sp create-for-rbac` to ensure home page URI is always "https"</span></span>

### <a name="service-bus"></a><span data-ttu-id="8cc5e-1304">Service Bus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1304">Service Bus</span></span>
* <span data-ttu-id="8cc5e-1305">[重大な変更] 空のリストを表示するのではなく、一般的な方法でリソースのエラー NotFound(404) を処理するように `list` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1305">[BREAKING CHANGE] Changed `list` commands to handle errors for resource(s) NotFound(404) in the typical way instead of showing empty list</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1306">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1306">VM</span></span>
* <span data-ttu-id="8cc5e-1307">`disk grant-access` の空の `accessSas` フィールドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1307">Fixed empty `accessSas` field in `disk grant-access`</span></span>
* <span data-ttu-id="8cc5e-1308">オーバープロビジョニングを処理するのに十分なフロントエンド ポート範囲が予約されるように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1308">Changed `vmss create` to reserve large enough frontend port range to handle overprovisioning</span></span>
* <span data-ttu-id="8cc5e-1309">`sig` の更新コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1309">Fixed update commands for `sig`</span></span>
* <span data-ttu-id="8cc5e-1310">`sig` のイメージ バージョンを管理するための `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1310">Added `--no-wait` support for managing image versions in `sig`</span></span>
* <span data-ttu-id="8cc5e-1311">パブリック IP アドレスの可用性ゾーンが表示されるように `vm list-ip-addresses` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1311">Changed `vm list-ip-addresses` to show availability zone of public IP addresses</span></span>
* <span data-ttu-id="8cc5e-1312">ディスクの既定の LUN が最初の使用可能なスポットに設定されるように `[vm|vmss] disk attach` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1312">Changed `[vm|vmss] disk attach` to set disk's default lun to the first available spot</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="8cc5e-1313">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1313">September 21, 2018</span></span>

<span data-ttu-id="8cc5e-1314">バージョン 2.0.46</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1314">Version 2.0.46</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1315">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1315">ACR</span></span>
* <span data-ttu-id="8cc5e-1316">ACR タスクのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1316">Added ACR Task commands</span></span>
* <span data-ttu-id="8cc5e-1317">クイック実行コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1317">Added quick run command</span></span>
* <span data-ttu-id="8cc5e-1318">`build-task` コマンド グループを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1318">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="8cc5e-1319">ACR での Helm チャートの管理をサポートするように `helm` コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1319">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="8cc5e-1320">マネージド レジストリについて、べき等作成のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1320">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="8cc5e-1321">ビルド ログを表示するために形式のないフラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1321">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1322">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1322">ACS</span></span>
* <span data-ttu-id="8cc5e-1323">AKS マスター FQDN を設定するように `install-connector` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1323">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="8cc5e-1324">サービス プリンシパルと skip-role-assignemnt を指定しない場合の vnet-subnet-id に対するロールの割り当て作成を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1324">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1325">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1325">AppService</span></span>

* <span data-ttu-id="8cc5e-1326">Web ジョブの (継続的およびトリガーされた) 運用管理のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1326">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="8cc5e-1327">az webapp config set で --fts-state プロパティがサポートされました。また、az functionapp config set および az functionapp config show のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1327">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="8cc5e-1328">Web アプリについて Bring Your Own Storage のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1328">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="8cc5e-1329">削除された Web アプリの一覧表示および復元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1329">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-1330">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1330">Batch</span></span>
* <span data-ttu-id="8cc5e-1331">AddTaskCollectionParameter 構文をサポートするように `--json-file` を使用したタスク追加を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1331">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="8cc5e-1332">承認済み `--json-file` 形式のドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1332">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="8cc5e-1333">`--max-tasks-per-node-option` を `batch pool create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1333">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="8cc5e-1334">オプションが指定されていない場合に、現在ログインしているアカウントを表示するように `batch account` の動作を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1334">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="8cc5e-1335">Batch AI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1335">Batch AI</span></span> 
* <span data-ttu-id="8cc5e-1336">`batchai cluster create` コマンドの自動ストレージ アカウント作成エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1336">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="8cc5e-1337">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1337">Cognitive Services</span></span>
* <span data-ttu-id="8cc5e-1338">`--sku`、`--kind`、`--location` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1338">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="8cc5e-1339">`cognitiveservices account list-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1339">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="8cc5e-1340">`cognitiveservices account list-kinds` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1340">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="8cc5e-1341">`cognitiveservices account list` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1341">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="8cc5e-1342">`cognitiveservices list` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1342">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="8cc5e-1343">`cognitiveservices account list-skus` について `--name` を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1343">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1344">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1344">Container</span></span>
* <span data-ttu-id="8cc5e-1345">実行中のコンテナー グループを再起動および停止する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1345">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="8cc5e-1346">ネットワーク プロファイルに渡すための `--network-profile` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1346">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="8cc5e-1347">VNet でのコンテナー グループの作成できるように `--subnet`、`--vnet_name` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1347">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="8cc5e-1348">コンテナー グループの状態を表示するようにテーブル出力を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1348">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="8cc5e-1349">DataLake</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1349">Datalake</span></span>
* <span data-ttu-id="8cc5e-1350">仮想ネットワーク規則用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1350">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="8cc5e-1351">対話型シェル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1351">Interactive Shell</span></span>
* <span data-ttu-id="8cc5e-1352">Windows でコマンドが正常に実行されないというエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1352">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="8cc5e-1353">非推奨のオブジェクトによって発生した、対話形式でのコマンド読み込みの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1353">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-1354">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1354">IoT</span></span>
* <span data-ttu-id="8cc5e-1355">IoT ハブのルーティングのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1355">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-1356">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1356">Key Vault</span></span>
* <span data-ttu-id="8cc5e-1357">RSA キーの Key Vault のキー インポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1357">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1358">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1358">Network</span></span>
* <span data-ttu-id="8cc5e-1359">パブリック IP プレフィックス機能をサポートするように `network public-ip prefix` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1359">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="8cc5e-1360">サービス エンドポイント ポリシー機能をサポートするように `network service-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1360">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="8cc5e-1361">Standard Load Balancer 送信規則の作成をサポートするように `network lb outbound-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1361">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="8cc5e-1362">パブリック IP プレフィックスを使用したフロントエンド IP 構成をサポートするように `--public-ip-prefix` を `network lb frontend-ip create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1362">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="8cc5e-1363">`--enable-tcp-reset` を `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1363">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="8cc5e-1364">`--disable-outbound-snat` を `network lb rule create/update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1364">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="8cc5e-1365">`network watcher flow-log show/configure` をクラシック NSG で使用できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1365">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="8cc5e-1366">`network watcher run-configuration-diagnostic` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1366">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="8cc5e-1367">`network watcher test-connectivity` コマンドを修正し、`--method`、`--valid-status-codes`、および `--headers` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1367">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="8cc5e-1368">`network express-route create/update`:`--allow-global-reach` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1368">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="8cc5e-1369">`network vnet subnet create/update`:`--delegation` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1369">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="8cc5e-1370">`network vnet subnet list-available-delegations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1370">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="8cc5e-1371">`network traffic-manager profile create/update`:監視の構成について `--interval`、`--timeout`、および `--max-failures` のサポートを追加しました。オプション `--path`、`--port`、`--protocol` を優先し、`--monitor-path`、`--monitor-port`、および `--monitor-protocol` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1371">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="8cc5e-1372">`network lb frontend-ip create/update`:プライベート IP 割り当て方法の設定ロジックを修正しました。プライベート IP アドレスが指定されている場合、割り当ては静的になります。プライベート IP アドレスが指定されていない場合、またはプライベート IP アドレスに対して空の文字列が指定されている場合、割り当ては動的です。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1372">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="8cc5e-1373">`dns record-set * create/update`:`--target-resource` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1373">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="8cc5e-1374">インターフェイス エンドポイント オブジェクトにクエリを実行する `network interface-endpoint` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1374">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="8cc5e-1375">ネットワーク プロファイルの部分的な管理用に `network profile show/list/delete` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1375">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="8cc5e-1376">ExpressRoute 間のピアリング接続を管理する `network express-route peering connection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1376">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1377">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1377">RDBMS</span></span>
* <span data-ttu-id="8cc5e-1378">MariaDB サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1378">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="8cc5e-1379">予約</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1379">Reservation</span></span>
* <span data-ttu-id="8cc5e-1380">予約されたリソース列挙型に CosmosDB を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1380">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="8cc5e-1381">Patch モデルに name プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1381">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="8cc5e-1382">アプリの管理</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1382">Manage App</span></span>
* <span data-ttu-id="8cc5e-1383">Marketplace マネージド アプリのインスタンス作成がクラッシュする原因となっている `managedapp create --kind MarketPlace` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1383">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="8cc5e-1384">サポートされているプロファイルに制限されるように `feature` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1384">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1385">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1385">Role</span></span>
* <span data-ttu-id="8cc5e-1386">ユーザーのグループ メンバーシップ表示のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1386">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="8cc5e-1387">SignalR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1387">SignalR</span></span>
* <span data-ttu-id="8cc5e-1388">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1388">First release</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1389">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1389">Storage</span></span>
* <span data-ttu-id="8cc5e-1390">BLOB およびキュー承認用のユーザー ログイン資格情報に使用する `--auth-mode login` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1390">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="8cc5e-1391">不変ストレージを管理するための `storage container immutability-policy/legal-hold` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1391">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1392">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1392">VM</span></span>
* <span data-ttu-id="8cc5e-1393">公開キー ファイルが見つからない場合に `vm create --generate-ssh-keys` によって秘密キー ファイルが上書きされる問題を修正しました (#4725、#6780)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1393">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="8cc5e-1394">`az sig` によって共有イメージ ギャラリーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1394">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="8cc5e-1395">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1395">August 28, 2018</span></span>

<span data-ttu-id="8cc5e-1396">バージョン 2.0.45</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1396">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1397">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1397">Core</span></span>

* <span data-ttu-id="8cc5e-1398">空の構成ファイルの読み込みに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1398">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="8cc5e-1399">Azure Stack におけるプロファイル `2018-03-01-hybrid` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1399">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1400">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1400">ACR</span></span>

* <span data-ttu-id="8cc5e-1401">ARM 要求がないランタイム操作に対する回避策を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1401">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="8cc5e-1402">`build` コマンドで、アップロードされた tar からバージョン コントロール ファイル (git、gitignore など) が既定で除外されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1402">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1403">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1403">ACS</span></span>

* <span data-ttu-id="8cc5e-1404">`Standard_DS2_v2` VM が既定で設定されるように `aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1404">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="8cc5e-1405">新しい API を呼び出して、クラスター資格情報を取得するように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1405">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1406">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1406">AppService</span></span>

* <span data-ttu-id="8cc5e-1407">関数アプリおよび Web アプリで CORS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1407">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="8cc5e-1408">作成コマンドに ARM タグのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1408">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="8cc5e-1409">リソースが見つからないときにコード 3 で終了するように `[webapp|functionapp] identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1409">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-1410">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1410">Backup</span></span>

* <span data-ttu-id="8cc5e-1411">リソースが見つからないときにコード 3 で終了するように `backup vault backup-properties show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1411">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="8cc5e-1412">ボット サービス</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1412">Bot Service</span></span>

* <span data-ttu-id="8cc5e-1413">初期ボット サービス CLI リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1413">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="8cc5e-1414">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1414">Cognitive Services</span></span>

* <span data-ttu-id="8cc5e-1415">一部のサービスの作成に必要な新しいパラメーター `--api-properties,` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1415">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-1416">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1416">IoT</span></span>

* <span data-ttu-id="8cc5e-1417">リンクされたハブの関連付けに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1417">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-1418">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1418">Monitor</span></span>

* <span data-ttu-id="8cc5e-1419">ほぼリアルタイムのメトリック アラートのための `monitor metrics alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1419">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="8cc5e-1420">`monitor alert` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1420">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1421">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1421">Network</span></span>

* <span data-ttu-id="8cc5e-1422">リソースが見つからないときにコード 3 で終了するように `network application-gateway ssl-policy predefined show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1422">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1423">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1423">Resource</span></span>

* <span data-ttu-id="8cc5e-1424">リソースが見つからないときにコード 3 で終了するように `provider operation show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1424">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1425">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1425">Storage</span></span>

* <span data-ttu-id="8cc5e-1426">リソースが見つからないときにコード 3 で終了するように `storage share policy show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1426">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1427">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1427">VM</span></span>

* <span data-ttu-id="8cc5e-1428">リソースが見つからないときにコード 3 で終了するように `vm/vmss identity show` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1428">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="8cc5e-1429">`vm create` を使用できるため `--storage-caching` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1429">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="8cc5e-1430">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1430">Auguest 14, 2018</span></span>

<span data-ttu-id="8cc5e-1431">バージョン 2.0.44</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1431">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1432">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1432">Core</span></span>

* <span data-ttu-id="8cc5e-1433">`table` 出力の数値表示を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1433">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="8cc5e-1434">YAML 出力形式を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1434">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="8cc5e-1435">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1435">Telemetry</span></span>

* <span data-ttu-id="8cc5e-1436">テレメトリ レポートを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1436">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1437">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1437">ACR</span></span>

* <span data-ttu-id="8cc5e-1438">`content-trust policy` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1438">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="8cc5e-1439">`.dockerignore` が適切に処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1439">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1440">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1440">ACS</span></span>

* <span data-ttu-id="8cc5e-1441">Windows で `%USERPROFILE%\.azure-kubectl` にインストールされるように `az acs/aks install-cli` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1441">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="8cc5e-1442">クラスターに RBAC が含まれるかどうかを検出し、ACI コネクタを適切に構成するように `az aks install-connector` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1442">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="8cc5e-1443">サブネットが指定されている場合、そのサブネットにロールが割り当てられるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1443">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="8cc5e-1444">サブネットが指定されている場合、そのサブネットについて "ロールの割り当てをスキップ" する新しいオプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1444">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="8cc5e-1445">サブネットへのロールの割り当てが既に存在する場合、その割り当てをスキップするように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1445">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="8cc5e-1446">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1446">AppService</span></span>

* <span data-ttu-id="8cc5e-1447">外部のリソース グループのストレージ アカウントを使用した関数アプリの作成を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1447">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="8cc5e-1448">zip デプロイ上のクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1448">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-1449">BatchAI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1449">BatchAI</span></span>

* <span data-ttu-id="8cc5e-1450">"resource *group*" が指定されるように、自動ストレージ アカウント作成のロガー出力を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1450">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="8cc5e-1451">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1451">Container</span></span>

* <span data-ttu-id="8cc5e-1452">セキュリティで保護された環境変数をコンテナーに渡すための `--secure-environment-variables` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1452">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="8cc5e-1453">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1453">IoT</span></span>

* <span data-ttu-id="8cc5e-1454">[重大な変更] iot 拡張機能に移動された非推奨のコマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1454">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="8cc5e-1455">`azure-devices.net` ドメインを想定しないように要素を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1455">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="8cc5e-1456">Iot Central</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1456">Iot Central</span></span>

* <span data-ttu-id="8cc5e-1457">IoT Central モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1457">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-1458">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1458">KeyVault</span></span>


* <span data-ttu-id="8cc5e-1459">ストレージ アカウントと SAS 定義を管理するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1459">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="8cc5e-1460">network-rules 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1460">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="8cc5e-1461">`--id` パラメーターをシークレット、キー、および証明書の操作に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1461">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="8cc5e-1462">KV 管理マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1462">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="8cc5e-1463">KV データ プレーン マルチ API バージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1463">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="8cc5e-1464">リレー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1464">Relay</span></span>

* <span data-ttu-id="8cc5e-1465">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1465">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1466">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1466">Sql</span></span>

* <span data-ttu-id="8cc5e-1467">`sql failover-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1467">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1468">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1468">Storage</span></span>

* <span data-ttu-id="8cc5e-1469">[重大な変更] `--location` パラメーターを必要とするように `storage account show-usage` を変更しました。リージョンごとに表示されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1469">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="8cc5e-1470">`storage account` コマンドで省略できるように `--resource-group` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1470">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="8cc5e-1471">バッチ コマンドの個々のエラーを表す "前提条件が満たされていない" という警告を削除し、1 つのメッセージに集約しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1471">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="8cc5e-1472">null の配列が出力されないように `[blob|file] delete-batch` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1472">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="8cc5e-1473">コンテナー URL から SAS トークンが読み取られるように `blob [download|upload|delete-batch]` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1473">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1474">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1474">VM</span></span>

* <span data-ttu-id="8cc5e-1475">使いやすくするために、共通フィルターを `vm list-skus` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1475">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="8cc5e-1476">2018 年 7 月 31日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1476">July 31, 2018</span></span>

<span data-ttu-id="8cc5e-1477">バージョン 2.0.43</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1477">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1478">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1478">ACR</span></span>

* <span data-ttu-id="8cc5e-1479">`--with-secure-properties` フラグを `acr build-task show` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1479">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="8cc5e-1480">`acr build-task update-build` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1480">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1481">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1481">ACS</span></span>

* <span data-ttu-id="8cc5e-1482">Ctrl + C キーを押して `az aks browse` を終了すると、戻り値 0 (成功) が返されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1482">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-1483">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1483">Batch</span></span>

* <span data-ttu-id="8cc5e-1484">CloudShell で AAD トークンを表示する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1484">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1485">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1485">Container</span></span>

* <span data-ttu-id="8cc5e-1486">サブスクリプションの設定時に、名または ID が求められる `--log-analytics-workspace-key` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1486">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1487">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1487">Network</span></span>

* <span data-ttu-id="8cc5e-1488">Azure Stack の 2017-03-09-profile に DNS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1488">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="8cc5e-1489">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1489">Resource</span></span>

* <span data-ttu-id="8cc5e-1490">エラー時に既知の正常なデプロイが実行されるように、`group deployment create` に `--rollback-on-error` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1490">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="8cc5e-1491">`group deployment create` を指定した `--parameters {}` がエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1491">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1492">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1492">Role</span></span>

* <span data-ttu-id="8cc5e-1493">Stack プロファイル 2017-03-09-profile のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1493">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="8cc5e-1494">`app update` に対する汎用更新パラメーターが正しく機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1494">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="8cc5e-1495">Search</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1495">Search</span></span>

* <span data-ttu-id="8cc5e-1496">Azure Search サービスのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1496">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="8cc5e-1497">Service Bus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1497">Service Bus</span></span>

* <span data-ttu-id="8cc5e-1498">Service Bus Standard から Premium に名前空間を移行する移行コマンド グループを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1498">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="8cc5e-1499">Service Bus キューおよびサブスクリプションに、新しい省略可能なプロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1499">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="8cc5e-1500">`queue` の `--enable-batched-operations` および `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1500">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="8cc5e-1501">`subscriptions` の `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1501">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1502">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1502">Storage</span></span>

* <span data-ttu-id="8cc5e-1503">1 つの接続を使用した大きなファイルのダウンロードがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1503">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="8cc5e-1504">リソースが見つからないときに終了コード 3 で失敗しそこなっていた `show` コマンドを変換しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1504">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1505">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1505">VM</span></span>

* <span data-ttu-id="8cc5e-1506">サブスクリプションごとに可用性セットを一覧表示できるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1506">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="8cc5e-1507">`StandardSSD_LRS` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1507">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="8cc5e-1508">VM スケール セットの作成でアプリケーション セキュリティ グループのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1508">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="8cc5e-1509">[重大な変更] ディクショナリ形式でユーザー割り当て ID を出力するように、`[vm|vmss] create`、`[vm|vmss] identity assign`、および `[vm|vmss] identity remove` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1509">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="8cc5e-1510">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1510">July 18, 2018</span></span>

<span data-ttu-id="8cc5e-1511">バージョン 2.0.42</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1511">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1512">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1512">Core</span></span>

* <span data-ttu-id="8cc5e-1513">WSL bash ウィンドウでのブラウザー ベースのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1513">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="8cc5e-1514">すべての汎用更新コマンドに `--force-string` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1514">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="8cc5e-1515">[重大な変更] リソースが見つからないときに、エラー メッセージを記録し、終了コード 3 で失敗するように "show" コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1515">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1516">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1516">ACR</span></span>

* <span data-ttu-id="8cc5e-1517">[重大な変更] "acr build" コマンドの "--no-push" を純粋なフラグに更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1517">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="8cc5e-1518">`acr repository` グループに、`show` コマンドと `update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1518">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="8cc5e-1519">`show-manifests` および `show-tags` に、詳細情報を表示する `--detail` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1519">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="8cc5e-1520">ビルドの詳細またはログのイメージによる取得をサポートするために、`--image` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1520">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1521">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1521">ACS</span></span>

* <span data-ttu-id="8cc5e-1522">`--max-pods` が 5 未満の場合にエラーが出力されるように `az aks create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1522">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1523">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1523">AppService</span></span>

* <span data-ttu-id="8cc5e-1524">PremiumV2 SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1524">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-1525">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1525">Batch</span></span>

* <span data-ttu-id="8cc5e-1526">Cloud Shell モードでトークン資格情報を使用する際のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1526">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="8cc5e-1527">大文字と小文字が区別されないように JSON 入力を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1527">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="8cc5e-1528">Batch AI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1528">Batch AI</span></span>

* <span data-ttu-id="8cc5e-1529">`az batchai job exec` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1529">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1530">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1530">Container</span></span>

* <span data-ttu-id="8cc5e-1531">DockerHub 以外のレジストリのユーザー名とパスワードの要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1531">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="8cc5e-1532">yaml ファイルからコンテナー グループを作成するときのエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1532">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1533">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1533">Network</span></span>

* <span data-ttu-id="8cc5e-1534">`network nic [create|update|delete]` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1534">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="8cc5e-1535">`network nic wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1535">Added `network nic wait`</span></span>
* <span data-ttu-id="8cc5e-1536">`network vnet [subnet|peering] list` の `--ids` 引数を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1536">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="8cc5e-1537">`network nsg rule list` の出力に既定のセキュリティ規則を含める `--include-default` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1537">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="8cc5e-1538">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1538">Resource</span></span>

* <span data-ttu-id="8cc5e-1539">`group deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1539">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="8cc5e-1540">`deployment delete` に `--no-wait` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1540">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="8cc5e-1541">`deployment wait` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1541">Added `deployment wait` command</span></span>
* <span data-ttu-id="8cc5e-1542">2017-03-09-profile プロファイルにサブスクリプション レベルの `az deployment` コマンドが誤って表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1542">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1543">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1543">SQL</span></span>

* <span data-ttu-id="8cc5e-1544">`sql db copy` コマンドおよび `sql db replica create` コマンドにエラスティック プール名を指定したときの、"The provided resource group name ... did not match the name in the Url"\(指定されたリソース グループ名 ... が URL 内の名前と一致しませんでした\) というエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1544">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="8cc5e-1545">`az configure --defaults sql-server=<name>` を実行して、既定の SQL Server を構成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1545">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="8cc5e-1546">`sql server`、`sql server firewall-rule`、`sql list-usages`、`sql show-usage` の各コマンドのテーブル フォーマッタを実装しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1546">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1547">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1547">Storage</span></span>

* <span data-ttu-id="8cc5e-1548">`storage blob show` の出力に、ページ BLOB 用に設定される `pageRanges` プロパティを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1548">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1549">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1549">VM</span></span>

* <span data-ttu-id="8cc5e-1550">[重大な変更] 既定のインスタンス サイズとして `Standard_DS1_v2` を使用するように `vmss create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1550">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="8cc5e-1551">`--no-wait` のサポートを `vm extension [set|delete]` および `vmss extension [set|delete]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1551">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="8cc5e-1552">`vm extension wait` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1552">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="8cc5e-1553">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1553">July 3, 2018</span></span>

<span data-ttu-id="8cc5e-1554">バージョン 2.0.41</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1554">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-1555">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1555">AKS</span></span>

* <span data-ttu-id="8cc5e-1556">サブスクリプション ID を使用するように監視を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1556">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="8cc5e-1557">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1557">July 3, 2018</span></span>

<span data-ttu-id="8cc5e-1558">バージョン 2.0.40</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1558">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1559">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1559">Core</span></span>

* <span data-ttu-id="8cc5e-1560">対話型ログインの新しい承認コード フローを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1560">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1561">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1561">ACR</span></span>

* <span data-ttu-id="8cc5e-1562">ビルド状態のポーリングを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1562">Added polling build status</span></span>
* <span data-ttu-id="8cc5e-1563">大文字と小文字が区別されない列挙型の値のサポ―トを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1563">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="8cc5e-1564">`show-manifests` の `--top` および `--orderby` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1564">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1565">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1565">ACS</span></span>

* <span data-ttu-id="8cc5e-1566">[重大な変更] Kubernetes のロールベースのアクセス制御を既定で有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1566">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="8cc5e-1567">`--disable-rbac` 引数を追加しました。また、`--enable-rbac` は現在の既定値なので非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1567">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="8cc5e-1568">`aks browse` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1568">Updated options for `aks browse` command.</span></span> <span data-ttu-id="8cc5e-1569">`--listen-port` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1569">Added `--listen-port` support</span></span>
* <span data-ttu-id="8cc5e-1570">`aks install-connector` コマンドの既定の Helm チャート パッケージを更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1570">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="8cc5e-1571">virtual-kubelet-for-aks-latest.tgz を使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1571">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="8cc5e-1572">既存のクラスターを更新するための `aks enable-addons` コマンドと `aks disable-addons` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1572">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1573">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1573">AppService</span></span>

* <span data-ttu-id="8cc5e-1574">`webapp identity remove` による ID の無効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1574">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="8cc5e-1575">ID 機能の `preview` タグを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1575">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-1576">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1576">Backup</span></span>

* <span data-ttu-id="8cc5e-1577">モジュール定義を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1577">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-1578">BatchAI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1578">BatchAI</span></span>

* <span data-ttu-id="8cc5e-1579">`batchai cluster node list` コマンドと `batchai job node list` コマンドのテーブル出力を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1579">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="8cc5e-1580">クラウド</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1580">Cloud</span></span>

* <span data-ttu-id="8cc5e-1581">`acr login` サーバー サフィックスをクラウド構成に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1581">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1582">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1582">Container</span></span>

* <span data-ttu-id="8cc5e-1583">`container create` の既定値が実行時間の長い操作に設定されるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1583">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="8cc5e-1584">Log Analytics の `--log-analytics-workspace` パラメーターと `--log-analytics-workspace-key` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1584">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="8cc5e-1585">使用するネットワーク プロトコルを指定する `--protocol` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1585">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-1586">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1586">Extension</span></span>

* <span data-ttu-id="8cc5e-1587">CLI バージョンと互換性のある拡張機能のみが表示されるように `extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1587">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1588">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1588">Network</span></span>

* <span data-ttu-id="8cc5e-1589">レコードの種類で大文字と小文字が区別される問題 ([#6602](https://github.com/Azure/azure-cli/issues/6602)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1589">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1590">Rdbms</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1590">Rdbms</span></span>

* <span data-ttu-id="8cc5e-1591">`[postgres|myql] server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1591">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1592">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1592">Resource</span></span>

* <span data-ttu-id="8cc5e-1593">新しい操作グループ `deployment` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1593">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1594">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1594">VM</span></span>

* <span data-ttu-id="8cc5e-1595">システム割り当て ID の削除に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1595">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="8cc5e-1596">2018 年 6 月 25 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1596">June 25, 2018</span></span>

<span data-ttu-id="8cc5e-1597">バージョン 2.0.39</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1597">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="8cc5e-1598">CLI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1598">CLI</span></span>

* <span data-ttu-id="8cc5e-1599">拡張機能のインストールの問題を解決するために MSI インストーラーのファイルのトリミングを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1599">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="8cc5e-1600">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1600">June 19, 2018</span></span>

<span data-ttu-id="8cc5e-1601">バージョン 2.0.38</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1601">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1602">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1602">Core</span></span>

* <span data-ttu-id="8cc5e-1603">`--subscription` のグローバル サポートをほとんどのコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1603">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1604">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1604">ACR</span></span>

* <span data-ttu-id="8cc5e-1605">`azure-storage-blob` を依存関係として追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1605">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="8cc5e-1606">2 コアが使用されるように `acr build-task create` での既定の CPU 構成を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1606">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1607">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1607">ACS</span></span>

* <span data-ttu-id="8cc5e-1608">`aks use-dev-spaces` コマンドのオプションを更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1608">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="8cc5e-1609">`--update` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1609">Added `--update` support</span></span>
* <span data-ttu-id="8cc5e-1610">`$HOME/.kube/config` のユーザー コンテキストが置き換えられないように `aks get-credentials --admin` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1610">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="8cc5e-1611">マネージド クラスターで読み取り専用の `nodeResourceGroup` プロパティを公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1611">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="8cc5e-1612">`acs browse` コマンド エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1612">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="8cc5e-1613">`aks install-connector`、`aks upgrade-connector`、および `aks remove-connector` について、`--connector-name` を省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1613">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="8cc5e-1614">`aks install-connector` の新しい Azure コンテナー インスタンス リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1614">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="8cc5e-1615">Helm のリリース名とノード名への正規化された場所を `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1615">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1616">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1616">AppService</span></span>

* <span data-ttu-id="8cc5e-1617">urllib の新しいバージョンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1617">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="8cc5e-1618">外部リソース グループから appservice プランが使用されるようにサポートを `functionapp create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1618">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-1619">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1619">Batch</span></span>

* <span data-ttu-id="8cc5e-1620">`azure-batch-extensions` 依存関係を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1620">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="8cc5e-1621">Batch AI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1621">Batch AI</span></span>

* <span data-ttu-id="8cc5e-1622">ワークスペースのサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1622">Added support for workspaces.</span></span> <span data-ttu-id="8cc5e-1623">ワークスペースを使用すると、クラスター、ファイル サーバー、および実験をグループ化できるため、作成できるリソースの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1623">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="8cc5e-1624">実験のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1624">Added support for experiments.</span></span> <span data-ttu-id="8cc5e-1625">実験を使用すると、ジョブをグループ化できるため、作成されたジョブの数に対する制限がなくなります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1625">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="8cc5e-1626">Docker コンテナーで実行されているジョブに対して `/dev/shm` を構成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1626">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="8cc5e-1627">`batchai cluster node exec` コマンドと `batchai job node exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1627">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="8cc5e-1628">これらのコマンドを使用すると、すべてのコマンドをノードで直接実行して、ポート フォワーディングの機能を提供できます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1628">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="8cc5e-1629">`--ids` のサポートを `batchai` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1629">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="8cc5e-1630">[重大な変更] すべてのクラスターおよびファイルサーバーをワークスペースに作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1630">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="8cc5e-1631">[重大な変更] ジョブを実験に作成する必要があります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1631">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="8cc5e-1632">[重大な変更] `--nfs-resource-group` を `cluster create` コマンドおよび `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1632">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="8cc5e-1633">別のワークスペース/リソース グループに属している NFS をマウントするには、`--nfs` オプションによってファイル サーバーの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1633">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="8cc5e-1634">[重大な変更] `--cluster-resource-group` を `job create` コマンドから削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1634">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="8cc5e-1635">別のワークスペース/リソース グループに属しているクラスターでジョブを送信するには、`--cluster` オプションによってクラスターの ARM ID を指定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1635">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="8cc5e-1636">[重大な変更] `location` 属性をジョブ、クラスター、およびファイル サーバーから削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1636">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="8cc5e-1637">現在の場所はワークスペースの属性です。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1637">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="8cc5e-1638">[重大な変更] `--location` を `job create` コマンド、`cluster create` コマンド、および `file-server create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1638">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="8cc5e-1639">[重大な変更] インターフェイスの一貫性を向上させるために短いオプションの名前を変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1639">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
  - <span data-ttu-id="8cc5e-1640">[`--config`, `-c`] の名前を [`--config-file`, `-f`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1640">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
  - <span data-ttu-id="8cc5e-1641">[`--cluster`, `-r`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1641">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="8cc5e-1642">[`--cluster`, `-n`] の名前を [`--cluster`, `-c`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1642">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
  - <span data-ttu-id="8cc5e-1643">[`--job`, `-n`] の名前を [`--job`, `-j`] に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1643">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="8cc5e-1644">マップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1644">Maps</span></span>

* <span data-ttu-id="8cc5e-1645">[重大な変更] 対話形式のプロンプトまたは `--accept-tos` フラグによるサービス利用規約への同意を必要とするように `maps account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1645">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1646">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1646">Network</span></span>

* <span data-ttu-id="8cc5e-1647">`https` のサポートを `network lb probe create` に追加しました [#6571](https://github.com/Azure/azure-cli/issues/6571)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1647">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="8cc5e-1648">`--endpoint-status` で大文字と小文字が区別されていた問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1648">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="8cc5e-1649">#6502</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1649">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="8cc5e-1650">Reservations</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1650">Reservations</span></span>

* <span data-ttu-id="8cc5e-1651">[重大な変更] 必要なパラメーター `ReservedResourceType` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1651">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="8cc5e-1652">パラメーター `Location` を `reservations catalog show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1652">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="8cc5e-1653">[重大な変更] `kind` を `ReservationProperties` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1653">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="8cc5e-1654">[重大な変更] `Catalog` で `capabilities` の名前を `sku_properties` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1654">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="8cc5e-1655">[重大な変更] `Catalog` から `size` プロパティおよび `tier` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1655">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="8cc5e-1656">パラメーター `InstanceFlexibility` を `reservations reservation update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1656">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1657">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1657">Role</span></span>

* <span data-ttu-id="8cc5e-1658">エラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1658">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1659">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1659">SQL</span></span>

* <span data-ttu-id="8cc5e-1660">ご自身のサブスクリプションで利用できない場所で `az sql db list-editions` 実行しているときに発生するわかりにくいエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1660">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1661">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1661">Storage</span></span>

* <span data-ttu-id="8cc5e-1662">`storage blob download` のテーブル出力を読みやすくしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1662">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1663">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1663">VM</span></span>

* <span data-ttu-id="8cc5e-1664">`vm create` で高速化されたネットワークをサポートするために、VM サイズの絞り込みチェックを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1664">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="8cc5e-1665">既定の VM サイズが `Standard_D1_v2` から `Standard_DS1_v2` に切り替わるこという `vmss create` に対する警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1665">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="8cc5e-1666">構成が変更されていない場合でも拡張機能が更新されるように `--force-update` を `[vm|vmss] extension set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1666">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="8cc5e-1667">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1667">June 13, 2018</span></span>

<span data-ttu-id="8cc5e-1668">バージョン 2.0.37</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1668">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1669">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1669">Core</span></span>

* <span data-ttu-id="8cc5e-1670">対話形式の利用統計情報を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1670">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="8cc5e-1671">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1671">June 13, 2018</span></span>

<span data-ttu-id="8cc5e-1672">バージョン 2.0.36</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1672">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-1673">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1673">AKS</span></span>

* <span data-ttu-id="8cc5e-1674">高度なネットワーク オプションを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1674">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="8cc5e-1675">引数を `aks create` に追加して、監視と HTTP ルーティングを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1675">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="8cc5e-1676">`--no-ssh-key` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1676">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="8cc5e-1677">`--enable-rbac` 引数を `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1677">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="8cc5e-1678">[プレビュー] Azure Active Directory 認証のサポートを `aks create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1678">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1679">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1679">AppService</span></span>

* <span data-ttu-id="8cc5e-1680">互換性のない urllib バージョンに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1680">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="8cc5e-1681">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1681">June 5, 2018</span></span>

<span data-ttu-id="8cc5e-1682">バージョン 2.0.35</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1682">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1683">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1683">Interactive</span></span>

* <span data-ttu-id="8cc5e-1684">対話モードの依存関係に対する制限を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1684">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="8cc5e-1685">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1685">June 5, 2018</span></span>

<span data-ttu-id="8cc5e-1686">バージョン 2.0.34</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1686">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1687">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1687">Core</span></span>

* <span data-ttu-id="8cc5e-1688">テナント リソース相互参照のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1688">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="8cc5e-1689">製品利用統計情報のアップロードの信頼性を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1689">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1690">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1690">ACR</span></span>

* <span data-ttu-id="8cc5e-1691">リモート ソースの場所として VSTS のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1691">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="8cc5e-1692">`acr import` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1692">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="8cc5e-1693">AKS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1693">AKS</span></span>

* <span data-ttu-id="8cc5e-1694">より安全なファイルシステム アクセス許可を使用して kube 構成ファイルが作成されるように `aks get-credentials` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1694">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-1695">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1695">Batch</span></span>

* <span data-ttu-id="8cc5e-1696">プール リスト テーブルのフォーマットのバグ [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)] を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1696">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-1697">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1697">IOT</span></span>

* <span data-ttu-id="8cc5e-1698">Basic レベルの IoT ハブを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1698">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1699">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1699">Network</span></span>

* <span data-ttu-id="8cc5e-1700">`network vnet peering` を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1700">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="8cc5e-1701">ポリシーの分析情報</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1701">Policy Insights</span></span>

* <span data-ttu-id="8cc5e-1702">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1702">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="8cc5e-1703">ARM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1703">ARM</span></span>

* <span data-ttu-id="8cc5e-1704">`account management-group` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1704">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1705">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1705">SQL</span></span>

* <span data-ttu-id="8cc5e-1706">新しいマネージド インスタンス コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1706">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="8cc5e-1707">新しいマネージド データベース コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1707">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="8cc5e-1708">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1708">Storage</span></span>

* <span data-ttu-id="8cc5e-1709">ファイル名拡張子から JSON および JavaScript が推論されるように、mimetype を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1709">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1710">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1710">VM</span></span>

* <span data-ttu-id="8cc5e-1711">固定列が使用されるように `vm list-skus` を変更し、`Tier` と `Size` が削除されることを知らせる警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1711">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="8cc5e-1712">`--accelerated-networking` オプションを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1712">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="8cc5e-1713">`--tags` を `identity create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1713">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="8cc5e-1714">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1714">May 22, 2018</span></span>

<span data-ttu-id="8cc5e-1715">バージョン 2.0.33</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1715">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1716">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1716">Core</span></span>

* <span data-ttu-id="8cc5e-1717">ファイル名で `@` を展開するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1717">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1718">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1718">ACS</span></span>

* <span data-ttu-id="8cc5e-1719">新しい Dev Space コマンド `aks use-dev-spaces` と `aks remove-dev-spaces` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1719">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="8cc5e-1720">ヘルプ メッセージの誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1720">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1721">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1721">AppService</span></span>

* <span data-ttu-id="8cc5e-1722">汎用的な更新コマンドを強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1722">Improved generic update commands</span></span>
* <span data-ttu-id="8cc5e-1723">`webapp deployment source config-zip` の非同期サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1723">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1724">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1724">Container</span></span>

* <span data-ttu-id="8cc5e-1725">YAML 形式のコンテナー グループをエクスポートするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1725">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="8cc5e-1726">YAML ファイルを使用してコンテナー グループを作成/更新するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1726">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-1727">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1727">Extension</span></span>

* <span data-ttu-id="8cc5e-1728">拡張機能の削除機能を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1728">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1729">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1729">Interactive</span></span>

* <span data-ttu-id="8cc5e-1730">ミュート パーサーへの完了のログ記録を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1730">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="8cc5e-1731">正しくないヘルプ キャッシュの処理を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1731">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-1732">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1732">KeyVault</span></span>

* <span data-ttu-id="8cc5e-1733">ID を持つ VM またはクラウド シェルで動作するように KeyVault コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1733">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1734">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1734">Network</span></span>

* <span data-ttu-id="8cc5e-1735">`network watcher show-topology` が VNet またはサブネット名で動作しない問題 ([#6326](https://github.com/Azure/azure-cli/issues/6326)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1735">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="8cc5e-1736">実際は有効になっているリージョンについて Network Watcher が、一部の `network watcher` コマンドによって、有効になっていないと通知される問題 ([#6264](https://github.com/Azure/azure-cli/issues/6264)) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1736">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1737">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1737">SQL</span></span>

* <span data-ttu-id="8cc5e-1738">[重大な変更] `db` コマンドおよび `dw` コマンドから返される応答オブジェクトを変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1738">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="8cc5e-1739">`serviceLevelObjective` プロパティの名前を `currentServiceObjectiveName` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1739">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="8cc5e-1740">`currentServiceObjectiveId` プロパティと `requestedServiceObjectiveId` プロパティを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1740">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="8cc5e-1741">`maxSizeBytes` プロパティを、文字列ではなく整数値に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1741">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="8cc5e-1742">[重大な変更] 次の `db` プロパティと `dw` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1742">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="8cc5e-1743">`requestedServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1743">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="8cc5e-1744">更新するには、`--service-objective` パラメーターを使用するか、`sku.name` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1744">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="8cc5e-1745">`edition`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1745">`edition`.</span></span> <span data-ttu-id="8cc5e-1746">更新するには、`--edition` パラメーターを使用するか、`sku.tier` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1746">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="8cc5e-1747">`elasticPoolName`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1747">`elasticPoolName`.</span></span> <span data-ttu-id="8cc5e-1748">更新するには、`--elastic-pool` パラメーターを使用するか、`elasticPoolId` プロパティを設定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1748">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="8cc5e-1749">[重大な変更] 次の `elastic-pool` プロパティを読み取り専用に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1749">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="8cc5e-1750">`edition`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1750">`edition`.</span></span> <span data-ttu-id="8cc5e-1751">更新するには、`--edition` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1751">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="8cc5e-1752">`dtu`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1752">`dtu`.</span></span> <span data-ttu-id="8cc5e-1753">更新するには、`--capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1753">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="8cc5e-1754">`databaseDtuMin`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1754">`databaseDtuMin`.</span></span> <span data-ttu-id="8cc5e-1755">更新するには、`--db-min-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1755">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="8cc5e-1756">`databaseDtuMax`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1756">`databaseDtuMax`.</span></span> <span data-ttu-id="8cc5e-1757">更新するには、`--db-max-capacity` パラメーターを使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1757">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="8cc5e-1758">`--family` パラメーターと `--capacity` パラメーターを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1758">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="8cc5e-1759">テーブル フォーマッタを、`db`、`dw`、`elastic-pool` の各コマンドに追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1759">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1760">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1760">Storage</span></span>

* <span data-ttu-id="8cc5e-1761">`--account-name` 引数の入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1761">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="8cc5e-1762">`storage entity query` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1762">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1763">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1763">VM</span></span>

* <span data-ttu-id="8cc5e-1764">[重大な変更] `--write-accelerator` を `vm create` から削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1764">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="8cc5e-1765">同じサポートに、`vm update` または `vm disk attach` を使用してアクセスできます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1765">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="8cc5e-1766">`[vm|vmss] extension` で一致する拡張機能イメージを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1766">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="8cc5e-1767">ブート ログがキャプチャされるように `--boot-diagnostics-storage` を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1767">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="8cc5e-1768">`--license-type` を `[vm|vmss] update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1768">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="8cc5e-1769">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1769">May 7, 2018</span></span>

<span data-ttu-id="8cc5e-1770">バージョン 2.0.32</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1770">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1771">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1771">Core</span></span>

* <span data-ttu-id="8cc5e-1772">証明書を使用してサービス プリンシパル アカウントからシークレットを取得する際のハンドルされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1772">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="8cc5e-1773">位置引数の制限付きサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1773">Added limited support for positional arguments</span></span>
* <span data-ttu-id="8cc5e-1774">`--ids` で `--query` を使用できない問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1774">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="8cc5e-1775">#5591</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1775">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="8cc5e-1776">`--ids` を使用するときのコマンドのパイプ処理シナリオを改善しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1776">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="8cc5e-1777">`-o tsv` (クエリが指定されている場合) と `-o json` (クエリが指定されていない場合) がサポートされます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1777">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="8cc5e-1778">ユーザーが入力したコマンドに誤りがある場合のエラーにコマンドの候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1778">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="8cc5e-1779">ユーザーが「`az ''`」と入力したときのエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1779">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="8cc5e-1780">コマンド モジュールとコマンド拡張機能でのカスタム リソースの種類のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1780">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1781">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1781">ACR</span></span>

* <span data-ttu-id="8cc5e-1782">ACR ビルドのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1782">Added ACR Build commands</span></span>
* <span data-ttu-id="8cc5e-1783">リソースが見つからないというエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1783">Improved resource not found error messages</span></span>
* <span data-ttu-id="8cc5e-1784">リソース作成のパフォーマンスとエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1784">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="8cc5e-1785">非標準コンソールと WSL での ACR ログインを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1785">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="8cc5e-1786">リポジトリ コマンドのエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1786">Improved repository commands error messages</span></span>
* <span data-ttu-id="8cc5e-1787">テーブルの列と順序付けを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1787">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1788">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1788">ACS</span></span>

* <span data-ttu-id="8cc5e-1789">`az aks` がプレビュー サービスであることを示す警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1789">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="8cc5e-1790">`--aci-resource-group` が指定されていないときの `aks install-connector` でのアクセス許可の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1790">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="8cc5e-1791">AMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1791">AMS</span></span>

* <span data-ttu-id="8cc5e-1792">最初のリリース - Azure Media Services リソースの管理</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1792">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1793">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1793">Appservice</span></span>

* <span data-ttu-id="8cc5e-1794">`--slot` を指定したときの `webapp delete` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1794">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="8cc5e-1795">`webapp auth update` から `--runtime-version` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1795">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="8cc5e-1796">min\_tls\_version と https2.0 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1796">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="8cc5e-1797">複数コンテナーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1797">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="8cc5e-1798">Batch AI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1798">Batch AI</span></span>

* <span data-ttu-id="8cc5e-1799">クラスターの構成ファイルで構成されている VM 優先度を優先するように `batchai create cluster` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1799">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="8cc5e-1800">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1800">Cognitive Services</span></span>

* <span data-ttu-id="8cc5e-1801">`cognitiveservices account create` の例 ([#5603](https://github.com/Azure/azure-cli/issues/5603)) の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1801">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-1802">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1802">Consumption</span></span>

* <span data-ttu-id="8cc5e-1803">budget API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1803">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1804">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1804">Container</span></span>

* <span data-ttu-id="8cc5e-1805">イメージ名にレジストリ サーバーが含まれている場合の `container create` での `--registry-server` の要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1805">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="8cc5e-1806">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1806">Cosmos DB</span></span>

* <span data-ttu-id="8cc5e-1807">Azure CLI (Cosmos DB) での VNET サポートを導入しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1807">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="8cc5e-1808">DMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1808">DMS</span></span>

* <span data-ttu-id="8cc5e-1809">最初のリリース - SQL から Azure SQL への移行シナリオのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1809">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-1810">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1810">Extension</span></span>

* <span data-ttu-id="8cc5e-1811">拡張機能メタデータが表示されなくなるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1811">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1812">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1812">Interactive</span></span>

* <span data-ttu-id="8cc5e-1813">対話型の入力候補が位置引数で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1813">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="8cc5e-1814">ユーザーが「\'」と入力したときの出力をわかりやすくしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1814">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="8cc5e-1815">ヘルプのないパラメーターの入力候補を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1815">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="8cc5e-1816">コマンド グループの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1816">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="8cc5e-1817">ラボ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1817">Lab</span></span>

* <span data-ttu-id="8cc5e-1818">knack 変換からの回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1818">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1819">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1819">Network</span></span>

* <span data-ttu-id="8cc5e-1820">[重大な変更] 次の要素の `--ids` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1820">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="8cc5e-1821">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1821">Profile</span></span>

* <span data-ttu-id="8cc5e-1822">`disk create` のソース検出を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1822">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="8cc5e-1823">[重大な変更] `--msi-port` と `--identity-port` は使用されなくなったため削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1823">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="8cc5e-1824">`account get-access-token` の概要の誤りを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1824">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="8cc5e-1825">Redis</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1825">Redis</span></span>

* <span data-ttu-id="8cc5e-1826">`redis patch-schedule show` を優先して、`redis patch-schedule patch-schedule show` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1826">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="8cc5e-1827">`redis list-all` を非推奨にしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1827">Deprecated `redis list-all`.</span></span> <span data-ttu-id="8cc5e-1828">この機能は `redis list` に組み込まれました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1828">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="8cc5e-1829">`redis import` を優先して、`redis import-method` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1829">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="8cc5e-1830">さまざまなコマンドに `--ids` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1830">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-1831">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1831">Role</span></span>

* <span data-ttu-id="8cc5e-1832">[重大な変更] 非推奨の `ad sp reset-credentials` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1832">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1833">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1833">Storage</span></span>

* <span data-ttu-id="8cc5e-1834">ソース SAS とアカウント キーが指定されていない場合、コピー先の SAS トークンを BLOB コピーのソースに適用できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1834">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="8cc5e-1835">BLOB のアップロードとダウンロードのための --socket-timeout を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1835">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="8cc5e-1836">パスの区切り記号で始まる BLOB 名は相対パスとして扱います</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1836">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="8cc5e-1837">先頭の文字が "?" のクエリで `storage blob copy --source-sas` を使用できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1837">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="8cc5e-1838">key=values のリストを受け入れるように `storage entity query --marker` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1838">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1839">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1839">VM</span></span>

* <span data-ttu-id="8cc5e-1840">非管理対象の BLOB URI の無効な検出ロジックを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1840">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="8cc5e-1841">ユーザーが指定したサービス プリンシパルを使用しないディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1841">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="8cc5e-1842">[重大な変更] MSI をサポートするために VM の "ManagedIdentityExtension" を使用しないでください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1842">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="8cc5e-1843">`vmss` に削除ポリシーのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1843">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="8cc5e-1844">[重大な変更] 次の要素から `--ids` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1844">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="8cc5e-1845">書き込みアクセラレータのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1845">Added write accelerator support</span></span>
* <span data-ttu-id="8cc5e-1846">`vmss perform-maintenance` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1846">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="8cc5e-1847">VM の OS の種類が確実に検出されるように `vm diagnostics set` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1847">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="8cc5e-1848">要求されたサイズが現在設定されているサイズと異なるかどうかをチェックし、変更時にのみ更新するように `vm resize` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1848">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="8cc5e-1849">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1849">April 10, 2018</span></span>

<span data-ttu-id="8cc5e-1850">バージョン 2.0.31</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1850">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1851">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1851">ACR</span></span>

* <span data-ttu-id="8cc5e-1852">wincred フォールバックのエラー処理を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1852">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1853">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1853">ACS</span></span>

* <span data-ttu-id="8cc5e-1854">AKS で作成した SPN を変更して 5 年間有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1854">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1855">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1855">Appservice</span></span>

* [破壊的変更]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="8cc5e-1857">存在しない webapp プランのキャッチされない例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1857">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-1858">BatchAI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1858">BatchAI</span></span>

* <span data-ttu-id="8cc5e-1859">2018-03-01 API のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1859">Added support for 2018-03-01 API</span></span>

  - <span data-ttu-id="8cc5e-1860">ジョブ レベルのマウント</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1860">Job level mounting</span></span>
  - <span data-ttu-id="8cc5e-1861">シークレット値を含む環境変数</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1861">Environment variables with secret values</span></span>
  - <span data-ttu-id="8cc5e-1862">パフォーマンス カウンターの設定</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1862">Performance counters settings</span></span>
  - <span data-ttu-id="8cc5e-1863">ジョブ固有のパス セグメントのレポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1863">Reporting of job specific path segment</span></span>
  - <span data-ttu-id="8cc5e-1864">ファイルを一覧表示する API のサブフォルダーのサポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1864">Support for subfolders in list files api</span></span>
  - <span data-ttu-id="8cc5e-1865">使用状況と制限のレポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1865">Usage and limits reporting</span></span>
  - <span data-ttu-id="8cc5e-1866">NFS サーバーのキャッシュの種類が指定可能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1866">Allow to specify caching type for NFS servers</span></span>
  - <span data-ttu-id="8cc5e-1867">カスタム イメージのサポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1867">Support for custom images</span></span>
  - <span data-ttu-id="8cc5e-1868">pyTorch ツールキットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1868">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="8cc5e-1869">`job wait` コマンドを追加しました。このコマンドは、ジョブ完了を待機できるようにして、ジョブ終了コードをレポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1869">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="8cc5e-1870">`usage show` コマンドを追加しました。このコマンドは、さまざまなリージョンにおける現在の Batch AI リソースの使用状況と制限を一覧表示します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1870">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="8cc5e-1871">National Clouds がサポートされています</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1871">National clouds are supported</span></span>
* <span data-ttu-id="8cc5e-1872">構成ファイルに加え、ジョブ レベルでファイルシステムをマウントするジョブ コマンド ライン引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1872">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="8cc5e-1873">VM 優先順位、サブネット、自動スケール クラスターの初期ノード数、カスタム イメージの指定など、クラスターのカスタマイズ オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1873">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="8cc5e-1874">Batch AI マネージド NFS のキャッシュの種類を指定するコマンド ライン オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1874">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="8cc5e-1875">構成ファイルでのファイルシステム マウントの指定を簡素化しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1875">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="8cc5e-1876">Azure ファイル共有および Azure BLOB コンテナーの資格情報を省略できます。不足している資格情報は、CLI によって、コマンド ライン パラメーターを介して提供された、または環境変数によって指定されたストレージ アカウント キーを使用して設定されるか、Azure Storage からキーが照会されます (ストレージ アカウントが現在のサブスクリプションに属している場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1876">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="8cc5e-1877">ジョブ ファイル ストリーム コマンドがオートコンプリートされるようになりました (成功、失敗、終了、または削除)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1877">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="8cc5e-1878">`show` 操作の `table` 出力を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1878">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="8cc5e-1879">クラスター作成の `--use-auto-storage` オプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1879">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="8cc5e-1880">このオプションによって、ストレージ アカウントの管理と、クラスターへの Azure ファイル共有および Azure BLOB コンテナーのマウントがシンプルになります</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1880">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="8cc5e-1881">`--generate-ssh-keys` オプションを `cluster create` と `file-server create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1881">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="8cc5e-1882">コマンド ラインでノードのセットアップ タスクを提供できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1882">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="8cc5e-1883">[重大な変更] `job file` グループで `job stream-file` および `job list-files` コマンドを移行しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1883">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="8cc5e-1884">[重大な変更] `cluster create` コマンドに合わせて、`file-server create` コマンドの `--admin-user-name` の名前を `--user-name` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1884">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="8cc5e-1885">課金</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1885">Billing</span></span>

* <span data-ttu-id="8cc5e-1886">登録アカウント コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1886">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-1887">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1887">Consumption</span></span>

* <span data-ttu-id="8cc5e-1888">`marketplace` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1888">Added `marketplace` commands</span></span>
* <span data-ttu-id="8cc5e-1889">[重大な変更] 名前を `reservations summaries` から `reservation summary` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1889">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="8cc5e-1890">[重大な変更] 名前を `reservations details` から `reservation detail` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1890">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="8cc5e-1891">[重大な変更] `reservation` コマンドの `--reservation-order-id` および `--reservation-id` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1891">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="8cc5e-1892">[重大な変更] `reservation summary` コマンドの `--grain` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1892">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="8cc5e-1893">[重大な変更] `pricesheet` コマンドの `--include-meter-details` の短いオプションを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1893">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1894">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1894">Container</span></span>

* <span data-ttu-id="8cc5e-1895">Git リポジトリのボリューム マウント パラメーター `--gitrepo-url`、`--gitrepo-dir`、`--gitrepo-revision`、および `--gitrepo-mount-path` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1895">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="8cc5e-1896">[#5926](https://github.com/Azure/azure-cli/issues/5926) (--container-name が指定されたときに `az container exec` が失敗する) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1896">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-1897">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1897">Extension</span></span>

* <span data-ttu-id="8cc5e-1898">ディストリビューション チェック メッセージをデバッグ レベルに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1898">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1899">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1899">Interactive</span></span>

* <span data-ttu-id="8cc5e-1900">認識できないコマンドが入力されたときに入力候補が停止するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1900">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="8cc5e-1901">コマンド サブツリーの作成前および作成後にイベント フックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1901">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="8cc5e-1902">`--ids` パラメーターの入力候補を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1902">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1903">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1903">Network</span></span>

* <span data-ttu-id="8cc5e-1904">[#5936](https://github.com/Azure/azure-cli/issues/5936) (`application-gateway create` タグを設定できない) を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1904">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="8cc5e-1905">`application-gateway http-settings [create|update]` の認証証明書をアタッチする引数 `--auth-certs` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1905">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="8cc5e-1906">#4910</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1906">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="8cc5e-1907">DDoS 保護プランを作成する `ddos-protection` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1907">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="8cc5e-1908">`--ddos-protection-plan` のサポートを `vnet [create|update]` に追加して、VNet を DDoS 保護プランに関連付けました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1908">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="8cc5e-1909">`network route-table [create|update]` の `--disable-bgp-route-propagation` フラグに関する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1909">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="8cc5e-1910">`network lb [create|update]` のダミー引数 `--public-ip-address-type` および `--subnet-type` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1910">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="8cc5e-1911">RFC 1035 エスケープ シーケンスを含む TXT レコードのサポートを `network dns zone [import|export]` および `network dns record-set txt add-record` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1911">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-1912">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1912">Profile</span></span>

* <span data-ttu-id="8cc5e-1913">`account list` に Azure クラシック アカウントのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1913">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="8cc5e-1914">[重大な変更] `--msi` & `--msi-port` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1914">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1915">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1915">RDBMS</span></span>

* <span data-ttu-id="8cc5e-1916">`georestore` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1916">Added `georestore` command</span></span>
* <span data-ttu-id="8cc5e-1917">ストレージ サイズの制限を `create` コマンドから削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1917">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1918">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1918">Resource</span></span>

* <span data-ttu-id="8cc5e-1919">`--metadata` のサポートを `policy definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1919">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="8cc5e-1920">`--metadata`、`--set`、`--add`、`--remove` のサポートを `policy definition update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1920">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-1921">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1921">SQL</span></span>

* <span data-ttu-id="8cc5e-1922">`sql elastic-pool op list` および `sql elastic-pool op cancel` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1922">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1923">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1923">Storage</span></span>

* <span data-ttu-id="8cc5e-1924">無効な形式の接続文字列のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1924">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1925">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1925">VM</span></span>

* <span data-ttu-id="8cc5e-1926">プラットフォーム障害ドメイン数の構成サポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1926">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="8cc5e-1927">ゾーンベースの大規模な、または single-placement-group が無効なスケールセットについて、`vmss create` の既定値が Standard LB になるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1927">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [破壊的変更]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="8cc5e-1929">Public-IP SKU のサポートを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1929">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="8cc5e-1930">コマンドでコンテナー ID を解決できないシナリオをサポートするように、`--keyvault` 引数と `--resource-group` 引数を `vm secret format` に追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1930">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="8cc5e-1931">#5718</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1931">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="8cc5e-1932">リソース グループの場所でゾーンがサポートされていない場合の、`[vm|vmss create]` のエラーを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1932">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="8cc5e-1933">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1933">March 27, 2018</span></span>

<span data-ttu-id="8cc5e-1934">バージョン 2.0.30</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1934">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-1935">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1935">Core</span></span>

* <span data-ttu-id="8cc5e-1936">ヘルプでプレビュー版としてマークされている拡張機能に関するメッセージを表示します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1936">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1937">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1937">ACS</span></span>

* <span data-ttu-id="8cc5e-1938">Cloud Shell の `aks install-cli` での SSL 証明書の検証エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1938">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-1939">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1939">Appservice</span></span>

* <span data-ttu-id="8cc5e-1940">`webapp update` に HTTPS 専用サポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1940">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="8cc5e-1941">`az webapp identity [assign|show]` と `az functionapp identity [assign|show]` にスロットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1941">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-1942">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1942">Backup</span></span>

* <span data-ttu-id="8cc5e-1943">新しいコマンド `az backup protection isenabled-for-vm` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1943">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="8cc5e-1944">このコマンドは、VM がサブスクリプション内の任意のコンテナーによってバックアップされるかどうかを確認するときに使用できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1944">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="8cc5e-1945">次のコマンドの `--resource-group` パラメーターと `--vault-name` パラメーターに対して Azure のオブジェクト ID を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1945">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="8cc5e-1946">`backup ... show` コマンドからの出力形式を受け入れるように、`--name` パラメーターを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1946">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-1947">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1947">Container</span></span>

* <span data-ttu-id="8cc5e-1948">`container exec` コマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1948">Added `container exec` command.</span></span> <span data-ttu-id="8cc5e-1949">実行中のコンテナー グループのコンテナーでコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1949">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="8cc5e-1950">コンテナー グループの作成および更新のために、テーブル出力が許可されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1950">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-1951">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1951">Extension</span></span>

* <span data-ttu-id="8cc5e-1952">拡張機能がプレビュー段階である場合に、`extension add` のメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1952">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="8cc5e-1953">`--show-details` を使用して完全な拡張機能データを表示できるように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1953">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="8cc5e-1954">[重大な変更] 簡略化された拡張機能データを既定で表示するように、`extension list-available` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1954">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-1955">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1955">Interactive</span></span>

* <span data-ttu-id="8cc5e-1956">コマンド テーブルの読み込みが完了するとすぐに入力候補がアクティブになるように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1956">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="8cc5e-1957">`--style` パラメーター使用時のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1957">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="8cc5e-1958">存在しない場合、コマンド テーブルのダンプ後に対話型レクサーがインスタンス化されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1958">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="8cc5e-1959">入力候補のサポートを強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1959">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="8cc5e-1960">ラボ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1960">Lab</span></span>

* <span data-ttu-id="8cc5e-1961">`create environment` コマンドに関するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1961">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-1962">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1962">Monitor</span></span>

* <span data-ttu-id="8cc5e-1963">`--top`、`--orderby`、`--namespace` のサポートを `metrics list`に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1963">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="8cc5e-1964">[#4529](https://github.com/Azure/azure-cli/issues/5785) を修正しました:`metrics list` は、取得するメトリックのスペース区切りリストを受け入れます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1964">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="8cc5e-1965">`--namespace` のサポートを `metrics list-definitions` に追加しました [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1965">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-1966">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1966">Network</span></span>

* <span data-ttu-id="8cc5e-1967">プライベート DNS ゾーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1967">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-1968">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1968">Profile</span></span>

* <span data-ttu-id="8cc5e-1969">`--identity-port` と `--msi-port` の警告を `login` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1969">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-1970">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1970">RDBMS</span></span>

* <span data-ttu-id="8cc5e-1971">ビジネス モデル GA API バージョン 2017-12-01 を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1971">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-1972">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1972">Resource</span></span>

* [破壊的変更]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="8cc5e-1974">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1974">Role</span></span>

* <span data-ttu-id="8cc5e-1975">必要なアクセス権の構成とネイティブ クライアントのサポートを `az ad app create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1975">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="8cc5e-1976">オブジェクトの解決時に 1000 未満の ID を返すように、`rbac` コマンドを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1976">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="8cc5e-1977">資格情報管理コマンド `ad sp credential [reset|list|delete]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1977">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="8cc5e-1978">[重大な変更] `az role assignment [list|show]` の出力から 'properties' を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1978">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="8cc5e-1979">`dataActions` アクセス許可と `notDataActions` アクセス許可のサポートを `role definition` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1979">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-1980">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1980">Storage</span></span>

* <span data-ttu-id="8cc5e-1981">サイズが 195 ～ 200 GB のファイルをアップロードするときの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1981">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="8cc5e-1982">[#4049](https://github.com/Azure/azure-cli/issues/4049) を修正しました:追加 BLOB のアップロードで条件のパラメーターが無視される問題</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1982">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-1983">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1983">VM</span></span>

* <span data-ttu-id="8cc5e-1984">インスタンス数が 100 を超えるセットに対する今後の破壊的変更に向けて、`vmss create` に警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1984">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="8cc5e-1985">ゾーン回復性のサポートを `vm [snapshot|image]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1985">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="8cc5e-1986">より適切に暗号化状態がレポートされるように、ディスクのインスタンス ビューを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1986">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="8cc5e-1987">[重大な変更] 出力を返さないように `vm extension delete` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1987">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="8cc5e-1988">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1988">March 13, 2018</span></span>

<span data-ttu-id="8cc5e-1989">バージョン 2.0.29</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1989">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-1990">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1990">ACR</span></span>

* <span data-ttu-id="8cc5e-1991">`--image` パラメーターのサポートを `repository delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1991">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="8cc5e-1992">`repository delete` コマンドの `--manifest` および `--tag` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1992">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="8cc5e-1993">データを削除せずに、タグを削除する `repository untag` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1993">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-1994">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1994">ACS</span></span>

* <span data-ttu-id="8cc5e-1995">既存のコネクタをアップグレードする `aks upgrade-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1995">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="8cc5e-1996">より読み取りやすいブロック スタイルの YAML を使用するように `kubectl` 構成ファイルを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1996">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="8cc5e-1997">Advisor</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1997">Advisor</span></span>

* <span data-ttu-id="8cc5e-1998">[重大な変更] 名前を `advisor configuration get` から `advisor configuration list` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1998">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="8cc5e-1999">[重大な変更] 名前を `advisor configuration set` から `advisor configuration update` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-1999">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="8cc5e-2000">[重大な変更] `advisor recommendation generate` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2000">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="8cc5e-2001">`--refresh` パラメーターを `advisor recommendation list` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2001">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="8cc5e-2002">`advisor recommendation show` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2002">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2003">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2003">Appservice</span></span>

* <span data-ttu-id="8cc5e-2004">`[webapp|functionapp] assign-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2004">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="8cc5e-2005">管理対象 ID コマンド `webapp identity [assign|show]` および `functionapp identity [assign|show]` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2005">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="8cc5e-2006">イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2006">Eventhubs</span></span>

* <span data-ttu-id="8cc5e-2007">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2007">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-2008">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2008">Extension</span></span>

* <span data-ttu-id="8cc5e-2009">使用しているディストリビューションがパッケージ ソース ファイルに格納されているものと異なる場合は、エラーが発生する可能性があるため、ユーザーに警告するチェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2009">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-2010">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2010">Interactive</span></span>

* <span data-ttu-id="8cc5e-2011">[#5625](https://github.com/Azure/azure-cli/issues/5625) を修正しました:異なるセッション間で履歴が保持されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2011">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="8cc5e-2012">[#3016](https://github.com/Azure/azure-cli/issues/3016) を修正しました:スコープ内にある間は履歴が記録されませんでした</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2012">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="8cc5e-2013">[#5688](https://github.com/Azure/azure-cli/issues/5688) を修正しました:コマンド テーブルの読み込み中に例外が発生した場合、入力候補が表示されませんでした</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2013">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="8cc5e-2014">実行時間の長い操作の進行状況インジケーターを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2014">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2015">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2015">Monitor</span></span>

* <span data-ttu-id="8cc5e-2016">`monitor autoscale-settings` コマンドを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2016">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="8cc5e-2017">`monitor autoscale` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2017">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="8cc5e-2018">`monitor autoscale profile` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2018">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="8cc5e-2019">`monitor autoscale rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2019">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2020">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2020">Network</span></span>

* <span data-ttu-id="8cc5e-2021">[重大な変更] `route-filter rule create` から `--tags` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2021">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="8cc5e-2022">次のコマンドの不適切な既定値を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2022">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="8cc5e-2023">`network watcher connection-monitor` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2023">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="8cc5e-2024">`--vnet` および `--subnet` パラメーターを `network watcher show-topology` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2024">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2025">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2025">Profile</span></span>

* <span data-ttu-id="8cc5e-2026">`az login` の `--msi` パラメーターを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2026">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="8cc5e-2027">`az login` の `--msi` パラメーターの代わりに `--identity` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2027">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-2028">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2028">RDBMS</span></span>

* <span data-ttu-id="8cc5e-2029">[プレビュー] API 2017-12-01-preview を使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2029">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="8cc5e-2030">Service Bus</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2030">Service Bus</span></span>

* <span data-ttu-id="8cc5e-2031">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2031">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2032">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2032">Storage</span></span>

* <span data-ttu-id="8cc5e-2033">[#4971](https://github.com/Azure/azure-cli/issues/4971) を修正しました: `storage blob copy` では他の Azure クラウドをサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2033">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="8cc5e-2034">[#5286](https://github.com/Azure/azure-cli/issues/5286) を修正しました:Batch コマンド `storage blob [delete-batch|download-batch|upload-batch]` の前提条件が満たされていなくても、エラーがスローされなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2034">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2035">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2035">VM</span></span>

* <span data-ttu-id="8cc5e-2036">被管理対象データ ディスクを接続し、キャッシュを構成できるように `[vm|vmss] create` へのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2036">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="8cc5e-2037">`[vm|vmss] assign-identity` および `[vm|vmss] remove-identity` を非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2037">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="8cc5e-2038">非推奨のコマンドの代わりに `vm identity [assign|remove|show]` および `vmss identity [assign|remove|show]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2038">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="8cc5e-2039">`vmss create` での既定の優先順位を None に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2039">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="8cc5e-2040">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2040">February 27, 2018</span></span>

<span data-ttu-id="8cc5e-2041">バージョン 2.0.28</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2041">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2042">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2042">Core</span></span>

* <span data-ttu-id="8cc5e-2043">[#5184](https://github.com/Azure/azure-cli/issues/5184) を修正しました:Homebrew のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2043">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="8cc5e-2044">カスタム キーを使用した拡張機能のテレメトリのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2044">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="8cc5e-2045">HTTP ログを `--debug` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2045">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2046">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2046">ACS</span></span>

* <span data-ttu-id="8cc5e-2047">既定で `aks install-connector` の `virtual-kubelet-for-aks` Helm チャートを使用するように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2047">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="8cc5e-2048">修正された問題:ACI コンテナー グループを作成するためのアクセス許可がサービス プリンシパルに不足している問題</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2048">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="8cc5e-2049">`--aci-container-group`、`--location`、および `--image-tag` の各パラメーターを `aks install-connector` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2049">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="8cc5e-2050">非推奨に関する通知を `aks get-versions` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2050">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2051">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2051">Appservice</span></span>

* <span data-ttu-id="8cc5e-2052">新しい SDK バージョン (azure-mgmt-web 0.35.0) の更新</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2052">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="8cc5e-2053">[#5538](https://github.com/Azure/azure-cli/issues/5538) を修正: 無効な SKU として報告された `Free`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2053">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="8cc5e-2054">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2054">Cognitive Services</span></span>

* <span data-ttu-id="8cc5e-2055">新しい Cognitive Services アカウントを作成するときの "通知" を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2055">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-2056">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2056">Consumption</span></span>

* <span data-ttu-id="8cc5e-2057">pricesheet API の新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2057">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="8cc5e-2058">既存の使用方法の詳細と予約の詳細の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2058">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2059">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2059">Container</span></span>

* <span data-ttu-id="8cc5e-2060">ACI でシークレットを使用するために `--secrets` と `--secrets-mount-path` の各引数を `container create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2060">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2061">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2061">Network</span></span>

* <span data-ttu-id="8cc5e-2062">[#5559](https://github.com/Azure/azure-cli/issues/5559) を修正:`network vnet-gateway vpn-client generate` でクライアントが見つからない</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2062">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2063">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2063">Resource</span></span>

* <span data-ttu-id="8cc5e-2064">エラー発生時にテンプレートとエラーの一部が表示されるように `group deployment export` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2064">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2065">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2065">Role</span></span>

* <span data-ttu-id="8cc5e-2066">サービス プリンシパル ロールの監査を許可するために `role assignment list-changelogs` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2066">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2067">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2067">SQL</span></span>

* <span data-ttu-id="8cc5e-2068">作成および更新時のデータベースとエラスティック プールのゾーン冗長性に対するサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2068">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2069">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2069">Storage</span></span>

* <span data-ttu-id="8cc5e-2070">`storage blob [upload-batch|download-batch]` のターゲット パス/プレフィックスの指定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2070">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2071">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2071">VM</span></span>

* <span data-ttu-id="8cc5e-2072">1 つの VMSS インスタンス上でのディスクの接続/デタッチのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2072">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="8cc5e-2073">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2073">February 13, 2018</span></span>

<span data-ttu-id="8cc5e-2074">バージョン 2.0.27</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2074">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2075">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2075">Core</span></span>

* <span data-ttu-id="8cc5e-2076">MSI ログインのサブスクリプション ID と名前の両方で認証をキーに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2076">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2077">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2077">ACS</span></span>

* <span data-ttu-id="8cc5e-2078">[重大な変更] 精度のために名前を `aks get-versions` から `aks get-upgrades` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2078">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="8cc5e-2079">`aks create` で使用可能な Kubernetes バージョンが表示されるように `aks get-versions` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2079">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="8cc5e-2080">サーバーで Kubernetes のバージョンを選択できるように `aks create` 既定値を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2080">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="8cc5e-2081">AKS によって生成されたサービス プリンシパルを参照するヘルプ メッセージを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2081">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="8cc5e-2082">`aks create` の既定のノード サイズを "Standard\_D1\_v2" から "Standard\_DS1\_v2" に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2082">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="8cc5e-2083">`az aks browse` のダッシュボード ポッドを特定するときの信頼性が向上しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2083">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="8cc5e-2084">Kubernetes 構成ファイルを読み込むときの Unicode エラーを処理するように `aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2084">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="8cc5e-2085">メッセージを `az aks install-cli` に追加しました。これは `$PATH` での `kubectl` の取得に役立ちます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2085">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2086">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2086">Appservice</span></span>

* <span data-ttu-id="8cc5e-2087">null 参照のために `webapp [backup|restore]` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2087">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="8cc5e-2088">`az configure --defaults appserviceplan=my-asp` による既定のアプリ サービス プランのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2088">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-2089">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2089">CDN</span></span>

* <span data-ttu-id="8cc5e-2090">`cdn custom-domain [enable-https|disable-https]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2090">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2091">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2091">Container</span></span>

* <span data-ttu-id="8cc5e-2092">ログ ストリーミングのために `--follow` オプションを `az container logs` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2092">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="8cc5e-2093">ローカル標準出力とエラー ストリームをコンテナー グループのコンテナーにアタッチする `container attach` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2093">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-2094">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2094">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-2095">機能の設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2095">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-2096">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2096">Extension</span></span>

* <span data-ttu-id="8cc5e-2097">`--pip-proxy` パラメーターのサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2097">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="8cc5e-2098">`--pip-extra-index-urls` 引数のサポートを `az extension [add|update]` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2098">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="8cc5e-2099">フィードバック</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2099">Feedback</span></span>

* <span data-ttu-id="8cc5e-2100">拡張機能の情報を利用統計情報に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2100">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-2101">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2101">Interactive</span></span>

* <span data-ttu-id="8cc5e-2102">Cloud Shell で対話モードを使用するときにユーザーのログインが求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2102">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="8cc5e-2103">パラメーター不足での完了による回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2103">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-2104">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2104">IoT</span></span>

* <span data-ttu-id="8cc5e-2105">成功時に `iot dps access policy [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2105">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="8cc5e-2106">成功時に `iot dps linked-hub [create|update]` が "検出不可" エラーを返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2106">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="8cc5e-2107">`--no-wait` のサポートを `iot dps access policy [create|update]` および `iot dps linked-hub [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2107">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2108">パーティション数の指定を許可するように `iot hub create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2108">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2109">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2109">Monitor</span></span>

* <span data-ttu-id="8cc5e-2110">`az monitor log-profiles create` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2110">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2111">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2111">Network</span></span>

* <span data-ttu-id="8cc5e-2112">次のコマンドの `--tags` オプションを修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2112">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="8cc5e-2113">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2113">Profile</span></span>

* <span data-ttu-id="8cc5e-2114">対話モードで `az login` を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2114">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2115">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2115">Resource</span></span>

* <span data-ttu-id="8cc5e-2116">`feature show` を再び追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2116">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2117">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2117">Role</span></span>

* <span data-ttu-id="8cc5e-2118">`--available-to-other-tenants` 引数を `ad app update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2118">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2119">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2119">SQL</span></span>

* <span data-ttu-id="8cc5e-2120">`sql server dns-alias` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2120">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="8cc5e-2121">`sql db rename` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2121">Added `sql db rename`</span></span>
* <span data-ttu-id="8cc5e-2122">`--ids` 引数のサポートをすべての SQL コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2122">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2123">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2123">Storage</span></span>

* <span data-ttu-id="8cc5e-2124">論理的な削除を有効にする `storage blob service-properties delete-policy` コマンドと `storage blob undelete` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2124">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2125">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2125">VM</span></span>

* <span data-ttu-id="8cc5e-2126">VM 暗号化の一部を初期化できないときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2126">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="8cc5e-2127">MSI を有効にするときのプリンシパル ID 出力を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2127">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="8cc5e-2128">`vm boot-diagnostics get-boot-log` (固定)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2128">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="8cc5e-2129">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2129">January 31, 2018</span></span>

<span data-ttu-id="8cc5e-2130">バージョン 2.0.26</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2130">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2131">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2131">Core</span></span>

* <span data-ttu-id="8cc5e-2132">MSI コンテキストでの未処理トークン取得のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2132">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="8cc5e-2133">Windows cmd.exe での LRO 終了後のインジケーター文字列ポーリングを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2133">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="8cc5e-2134">構成された既定値の使用が情報レベル エントリに変更されたときに表示される警告を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2134">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="8cc5e-2135">確認するには `--verbose` を使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2135">Use `--verbose` to see</span></span>
* <span data-ttu-id="8cc5e-2136">待機コマンドの進行状況のインジケーターを追加します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2136">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2137">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2137">ACS</span></span>

* <span data-ttu-id="8cc5e-2138">`--disable-browser` 引数を明確化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2138">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="8cc5e-2139">`--vm-size` 引数のタブ補完を強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2139">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2140">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2140">Appservice</span></span>

* <span data-ttu-id="8cc5e-2141">`webapp log [tail|download]` (固定)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2141">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="8cc5e-2142">WebApps と機能で `kind` チェックを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2142">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-2143">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2143">CDN</span></span>

* <span data-ttu-id="8cc5e-2144">`cdn custom-domain create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2144">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-2145">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2145">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-2146">フェールオーバー ポリシーのパラメーターの説明を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2146">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-2147">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2147">Interactive</span></span>

* <span data-ttu-id="8cc5e-2148">コマンド オプションの完了が表示されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2148">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2149">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2149">Network</span></span>

* <span data-ttu-id="8cc5e-2150">`--cert-password` の保護を `application-gateway create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2150">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="8cc5e-2151">`--sku` が誤って既定値を適用する `application-gateway update` の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2151">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="8cc5e-2152">`--shared-key` の保護を `--authorization-key` および `vpn-connection create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2152">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="8cc5e-2153">`asg create` のクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2153">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="8cc5e-2154">エクスポートされた名前の `--file-name / -f` パラメーターを `dns zone export` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2154">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="8cc5e-2155">`dns zone export` の次の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2155">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="8cc5e-2156">長い TXT レコードが誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2156">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="8cc5e-2157">引用符で囲まれた TXT レコードが、エスケープされた引用符なしで誤ってエクスポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2157">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="8cc5e-2158">特定のレコードが `dns zone import` で 2 回インポートされる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2158">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="8cc5e-2159">`vnet-gateway root-cert` コマンドと `vnet-gateway revoked-cert` コマンドを復元しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2159">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2160">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2160">Profile</span></span>

* <span data-ttu-id="8cc5e-2161">ID を使用して VM 内で動作するように `get-access-token` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2161">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2162">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2162">Resource</span></span>

* <span data-ttu-id="8cc5e-2163">テンプレートの "type" フィールドに大文字の値が含まれているときに警告が誤って表示される `deployment [create|validate]` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2163">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2164">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2164">Storage</span></span>

* <span data-ttu-id="8cc5e-2165">ストレージ V1 からストレージ V2 へのアカウント移行の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2165">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="8cc5e-2166">すべてのアップロード/ダウンロード コマンドについて、進行状況レポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2166">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="8cc5e-2167">`storage account check-name` で "-n" 引数オプションが妨げられるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2167">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="8cc5e-2168">"snapshot" 列を `blob [list|show]` のテーブル出力に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2168">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="8cc5e-2169">整数として解析する必要があるさまざまなパラメーターのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2169">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2170">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2170">VM</span></span>

* <span data-ttu-id="8cc5e-2171">追加料金でイメージからの VM 作成を許可する `vm image accept-terms` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2171">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="8cc5e-2172">署名されていない証明書を使用して、コマンドをプロキシで確実に実行できるように `[vm|vmss create]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2172">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="8cc5e-2173">[プレビュー] "低" 優先度のサポートを VMSS に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2173">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="8cc5e-2174">`--admin-password` の保護を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2174">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="8cc5e-2175">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2175">January 17, 2018</span></span>

<span data-ttu-id="8cc5e-2176">バージョン 2.0.25</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2176">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-2177">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2177">ACR</span></span>

* <span data-ttu-id="8cc5e-2178">Windows 資格情報エラーの acr ログイン フォールバックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2178">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="8cc5e-2179">レジストリ ログを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2179">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2180">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2180">ACS</span></span>

* <span data-ttu-id="8cc5e-2181">`get-credentials` コマンドを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2181">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="8cc5e-2182">SPN のロール要件を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2182">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2183">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2183">Appservice</span></span>

* <span data-ttu-id="8cc5e-2184">`hosting_environment_profile` が null になる `config ssl upload` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2184">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="8cc5e-2185">`browse` にカスタム URL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2185">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="8cc5e-2186">`log tail` のスロットのサポートを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2186">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-2187">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2187">Backup</span></span>

* <span data-ttu-id="8cc5e-2188">`backup item list` の `--container-name` オプションを省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2188">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="8cc5e-2189">`backup restore restore-disks` にストレージ アカウント オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2189">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="8cc5e-2190">`backup protection enable-for-vm` での場所のチェックを、大文字と小文字が区別されないように修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2190">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="8cc5e-2191">無効なコンテナー名でコマンドが失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2191">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="8cc5e-2192">既定で "正常性状態" が含まれるように `backup item list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2192">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-2193">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2193">Batch</span></span>

* <span data-ttu-id="8cc5e-2194">認証の詳細を返すように `batch login` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2194">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="8cc5e-2195">クラウド</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2195">Cloud</span></span>

* <span data-ttu-id="8cc5e-2196">クラウドで `--profile` を設定するときに、エンドポイントを不要にするように変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2196">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-2197">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2197">Consumption</span></span>

* <span data-ttu-id="8cc5e-2198">予約の新しいコマンドとして、`consumption reservations summaries` と `consumption reservations details` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2198">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="8cc5e-2199">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2199">Event Grid</span></span>

* <span data-ttu-id="8cc5e-2200">[重大な変更] `az eventgrid topic event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2200">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8cc5e-2201">[重大な変更] `az eventgrid resource event-subscription` コマンドを `eventgrid event-subscription` に移行しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2201">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="8cc5e-2202">[重大な変更] `eventgrid event-subscription show-endpoint-url` コマンドを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2202">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="8cc5e-2203">代わりに `eventgrid event-subscription show --include-full-endpoint-url` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2203">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="8cc5e-2204">`eventgrid topic update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2204">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="8cc5e-2205">`eventgrid event-subscription update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2205">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="8cc5e-2206">`eventgrid topic` コマンドの `--ids` パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2206">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="8cc5e-2207">トピック名のタブ補完のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2207">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-2208">Interactive</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2208">Interactive</span></span>

* <span data-ttu-id="8cc5e-2209">Python 2.x で対話モードが機能しない問題を解決しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2209">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="8cc5e-2210">起動時のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2210">Fixed errors on startup</span></span>
* <span data-ttu-id="8cc5e-2211">対話モードで実行されない一部のコマンドの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2211">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-2212">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2212">IoT</span></span>

* <span data-ttu-id="8cc5e-2213">デバイス プロビジョニング サービスのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2213">Added support for device provisioning service</span></span>
* <span data-ttu-id="8cc5e-2214">コマンドとコマンドのヘルプに非推奨を示すメッセージを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2214">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="8cc5e-2215">ユーザーに IoT 拡張機能を通知する IoT チェックを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2215">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2216">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2216">Monitor</span></span>

* <span data-ttu-id="8cc5e-2217">複数診断設定のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2217">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="8cc5e-2218">`az monitor diagnostic-settings create` で `--name` パラメーターが必須になりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2218">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="8cc5e-2219">診断設定カテゴリを取得する `monitor diagnostic-settings categories` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2219">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2220">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2220">Network</span></span>

* <span data-ttu-id="8cc5e-2221">`vnet-gateway update` でのアクティブ/スタンバイ モードの切り替え時の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2221">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="8cc5e-2222">`application-gateway [create|update]` に HTTP2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2222">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2223">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2223">Profile</span></span>

* <span data-ttu-id="8cc5e-2224">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2224">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2225">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2225">Role</span></span>

* <span data-ttu-id="8cc5e-2226">グラフ クエリをバイパスするために、`role assignment create` に `--assignee-object-id` 引数を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2226">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8cc5e-2227">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2227">Service Fabric</span></span>

* <span data-ttu-id="8cc5e-2228">クラスターの作成時の検証応答に詳細なエラーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2228">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="8cc5e-2229">一部のコマンドでのクライアントが見つからない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2229">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2230">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2230">VM</span></span>

* <span data-ttu-id="8cc5e-2231">[プレビュー] `vmss` のクロス ゾーンのサポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2231">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="8cc5e-2232">[重大な変更] 単一ゾーン `vmss` の既定値を "Standard" ロード バランサーに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2232">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="8cc5e-2233">[重大な変更] EMSI の `externalIdentities` を `userAssignedIdentities` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2233">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="8cc5e-2234">[プレビュー] OS ディスク スワップのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2234">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="8cc5e-2235">他のサブスクリプションの VM イメージの使用のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2235">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="8cc5e-2236">`--plan-name`、`--plan-product`、`--plan-promotion-code`、`--plan-publisher` の各引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2236">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="8cc5e-2237">`[vm|vmss] create` でのエラーの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2237">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="8cc5e-2238">`vm image list --all` に起因するリソースの過剰使用を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2238">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="8cc5e-2239">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2239">December 19, 2017</span></span>

<span data-ttu-id="8cc5e-2240">バージョン 2.0.23</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2240">Version 2.0.23</span></span>

* <span data-ttu-id="8cc5e-2241">ユーザーが割り当てた ID でのログインのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2241">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2242">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2242">Container</span></span>

* <span data-ttu-id="8cc5e-2243">コンテナー ログのパラメーターのパラメーターの不適切な順序を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2243">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2244">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2244">Network</span></span>

* <span data-ttu-id="8cc5e-2245">`--disable-bgp-route-propagation` 引数を `route-table [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2245">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2246">`--ip-tags` 引数を `public-ip [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2246">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2247">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2247">Storage</span></span>

* <span data-ttu-id="8cc5e-2248">ストレージ V2 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2248">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2249">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2249">VM</span></span>

* <span data-ttu-id="8cc5e-2250">[プレビュー] VM と VMSS のユーザーが割り当てた ID のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2250">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="8cc5e-2251">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2251">December 5, 2017</span></span>

<span data-ttu-id="8cc5e-2252">バージョン 2.0.22</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2252">Version 2.0.22</span></span>

* <span data-ttu-id="8cc5e-2253">`az component` コマンドを削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2253">Removed `az component` commands.</span></span> <span data-ttu-id="8cc5e-2254">代わりに `az extension` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2254">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2255">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2255">Core</span></span>
* <span data-ttu-id="8cc5e-2256">`AZURE_US_GOV_CLOUD` AAD 機関エンドポイントを、login.microsoftonline.com から login.microsoftonline.us に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2256">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="8cc5e-2257">テレメトリが連続的に再送信される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2257">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2258">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2258">ACS</span></span>

* <span data-ttu-id="8cc5e-2259">`aks install-connector` コマンドと `aks remove-connector` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2259">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="8cc5e-2260">`acs create` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2260">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="8cc5e-2261">完全修飾パスなしでの `aks get-credentials -f` の使用方法を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2261">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="8cc5e-2262">Advisor</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2262">Advisor</span></span>

* <span data-ttu-id="8cc5e-2263">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2263">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2264">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2264">Appservice</span></span>

* <span data-ttu-id="8cc5e-2265">`webapp config ssl upload` による証明書名の生成を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2265">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="8cc5e-2266">正しいアプリを表示するように、`webapp [list|show]` と `functionapp [list|show]` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2266">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="8cc5e-2267">`WEBSITE_NODE_DEFAULT_VERSION` の既定値を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2267">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="8cc5e-2268">消費</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2268">Consumption</span></span>

* <span data-ttu-id="8cc5e-2269">API バージョン 2017-11-30 のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2269">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2270">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2270">Container</span></span>

* <span data-ttu-id="8cc5e-2271">既定のポート回帰を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2271">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2272">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2272">Monitor</span></span>

* <span data-ttu-id="8cc5e-2273">メトリック コマンドに多次元のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2273">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2274">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2274">Resource</span></span>

* <span data-ttu-id="8cc5e-2275">`--include-response-body` 引数を `resource show` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2275">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2276">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2276">Role</span></span>

* <span data-ttu-id="8cc5e-2277">`role assignment list` に、"従来の" 管理者の既定の割り当ての表示を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2277">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="8cc5e-2278">`ad sp reset-credentials` で、上書きではなく、資格情報を追加できるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2278">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="8cc5e-2279">`ad sp create-for-rbac` のエラー報告を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2279">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2280">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2280">SQL</span></span>

* <span data-ttu-id="8cc5e-2281">`sql db list-usages` コマンドと `sql db show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2281">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="8cc5e-2282">`sql server conn-policy show` コマンドと `sql server conn-policy update` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2282">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2283">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2283">VM</span></span>

* <span data-ttu-id="8cc5e-2284">`az vm list-skus` にゾーン情報を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2284">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="8cc5e-2285">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2285">November 14, 2017</span></span>

<span data-ttu-id="8cc5e-2286">バージョン 2.0.21</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2286">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-2287">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2287">ACR</span></span>

* <span data-ttu-id="8cc5e-2288">レプリケーション リージョンで webhook を作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2288">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="8cc5e-2289">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2289">ACS</span></span>

* <span data-ttu-id="8cc5e-2290">AKS の "エージェント" という用語をすべて "ノード" に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2290">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="8cc5e-2291">`acs create` の `--orchestrator-release` オプションを非推奨にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2291">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="8cc5e-2292">`Standard_D1_v2` に対する AKS の既定 VM サイズを変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2292">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="8cc5e-2293">Windows での `az aks browse` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2293">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="8cc5e-2294">Windows での `az aks get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2294">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2295">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2295">Appservice</span></span>

* <span data-ttu-id="8cc5e-2296">Web アプリおよび関数アプリ用のデプロイ ソース `config-zip` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2296">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="8cc5e-2297">`--docker-container-logging` オプションを `az webapp log config` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2297">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="8cc5e-2298">`storage` オプションを `az webapp log config` のパラメーター `--web-server-logging` から削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2298">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="8cc5e-2299">`deployment user set` のエラー メッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2299">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="8cc5e-2300">Linux 関数アプリを作成するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2300">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="8cc5e-2301">`list-locations` (固定)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2301">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-2302">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2302">Batch</span></span>

* <span data-ttu-id="8cc5e-2303">`--image` を指定してリソース ID を使用した場合のプール作成コマンドのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2303">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-2304">Batchai</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2304">Batchai</span></span>

* <span data-ttu-id="8cc5e-2305">`file-server create` コマンドで VM サイズを指定する場合の `--vm-size` の短いオプション `-s` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2305">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="8cc5e-2306">ストレージ アカウント名とキー引数を `cluster create` パラメーターに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2306">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="8cc5e-2307">`job list-files` および `job stream-file` のドキュメントを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2307">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="8cc5e-2308">`job create` コマンドでクラスター名を指定する場合の `--cluster-name` の短いオプション `-r` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2308">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="8cc5e-2309">クラウド</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2309">Cloud</span></span>

* <span data-ttu-id="8cc5e-2310">必要なエンドポイントのないクラウドの登録を防ぐために `cloud [register|update]` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2310">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2311">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2311">Container</span></span>

* <span data-ttu-id="8cc5e-2312">複数のポートを開くためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2312">Added support to open multiple ports</span></span>
* <span data-ttu-id="8cc5e-2313">コンテナー グループ再起動ポリシーを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2313">Added container group restart policy</span></span>
* <span data-ttu-id="8cc5e-2314">Azure ファイル共有をボリュームとしてマウントするためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2314">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="8cc5e-2315">ヘルパー ドキュメントを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2315">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8cc5e-2316">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2316">Data Lake Analytics</span></span>

* <span data-ttu-id="8cc5e-2317">より簡潔な情報を返すように `[job|account] list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2317">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8cc5e-2318">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2318">Data Lake Store</span></span>

* <span data-ttu-id="8cc5e-2319">より簡潔な情報を返すように `account list` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2319">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-2320">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2320">Extension</span></span>

* <span data-ttu-id="8cc5e-2321">公式の Microsoft 拡張機能を一覧表示できるようにするための `extension list-available` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2321">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="8cc5e-2322">拡張機能を名前別にインストールできるように、`--name` を `extension [add|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2322">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-2323">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2323">IoT</span></span>

* <span data-ttu-id="8cc5e-2324">証明機関 (CA) および証明書チェーンのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2324">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2325">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2325">Monitor</span></span>

* <span data-ttu-id="8cc5e-2326">`activity-log alert` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2326">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2327">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2327">Network</span></span>

* <span data-ttu-id="8cc5e-2328">CAA DNS レコードのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2328">Added support for CAA DNS records</span></span>
* <span data-ttu-id="8cc5e-2329">エンドポイントを `traffic-manager profile update` で更新できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2329">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="8cc5e-2330">VNET の作成方法によっては `vnet update --dns-servers` が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2330">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="8cc5e-2331">相対 DNS 名が `dns zone import` によって正しくインポートされない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2331">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="8cc5e-2332">Reservations</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2332">Reservations</span></span>

* <span data-ttu-id="8cc5e-2333">初期プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2333">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2334">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2334">Resource</span></span>

* <span data-ttu-id="8cc5e-2335">リソース ID のサポートを `--resource` パラメーターとリソースレベル ロックに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2335">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2336">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2336">SQL</span></span>

* <span data-ttu-id="8cc5e-2337">`--ignore-missing-vnet-service-endpoint` パラメーターを `sql server vnet-rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2337">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2338">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2338">Storage</span></span>

* <span data-ttu-id="8cc5e-2339">SKU `Standard_RAGRS` を既定値として使用するように `storage account create` を変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2339">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="8cc5e-2340">非 ASCII 文字を含むファイル/BLOB 名を処理する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2340">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="8cc5e-2341">`storage [blob|file] copy start-batch` での `--source-uri` の使用を妨げるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2341">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="8cc5e-2342">`storage [blob|file] delete-batch` で複数のオブジェクトを glob および削除するコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2342">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="8cc5e-2343">`storage metrics update` でメトリックを有効にする場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2343">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="8cc5e-2344">`storage blob upload-batch` の使用時に 200 GB を超えるファイルにおける問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2344">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="8cc5e-2345">`--bypass` と `--default-action` が `storage account [create|update]` によって無視される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2345">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2346">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2346">VM</span></span>

* <span data-ttu-id="8cc5e-2347">`Basic` サイズ レベルの使用を妨げていり `vmss create` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2347">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="8cc5e-2348">課金情報を含むカスタム イメージ用に `--plan` 引数を `[vm|vmss] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2348">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="8cc5e-2349">`vm secret `[add|remove|list]\` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2349">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="8cc5e-2350">`vm format-secret` の名前を `vm secret format` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2350">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="8cc5e-2351">`--encrypt format` 引数を `vm encryption enable` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2351">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="8cc5e-2352">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2352">October 24, 2017</span></span>

<span data-ttu-id="8cc5e-2353">バージョン 2.0.20</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2353">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2354">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2354">Core</span></span>

* <span data-ttu-id="8cc5e-2355">`MGMT_STORAGE` API バージョン `2016-01-01` を使用するように `2017-03-09-profile` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2355">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-2356">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2356">ACR</span></span>

* <span data-ttu-id="8cc5e-2357">`2017-10-01` API バージョンを指すようにリソース管理を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2357">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="8cc5e-2358">"Bring Your Own Storage" SKU をクラシックに変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2358">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="8cc5e-2359">レジストリの SKU の名前を Basic、Standard、Premium に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2359">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2360">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2360">ACS</span></span>

* <span data-ttu-id="8cc5e-2361">[プレビュー] `az aks` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2361">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="8cc5e-2362">Kubernetes の `get-credentials` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2362">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2363">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2363">Appservice</span></span>

* <span data-ttu-id="8cc5e-2364">ダウンロードした `webapp` ログが無効である可能性のある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2364">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="8cc5e-2365">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2365">Component</span></span>

* <span data-ttu-id="8cc5e-2366">すべてのインストーラー向けのより明確な非推奨メッセージと、確認プロンプトを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2366">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2367">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2367">Monitor</span></span>

* <span data-ttu-id="8cc5e-2368">`action-group` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2368">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2369">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2369">Resource</span></span>

* <span data-ttu-id="8cc5e-2370">`group export` における msrest の依存関係の最新バージョンとの非互換性を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2370">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="8cc5e-2371">組み込みのポリシー定義とポリシーセットの定義を使用するように `policy assignment create` を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2371">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2372">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2372">VM</span></span>

* <span data-ttu-id="8cc5e-2373">`--accelerated-networking` 引数を `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2373">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="8cc5e-2374">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2374">October 9, 2017</span></span>

<span data-ttu-id="8cc5e-2375">バージョン 2.0.19</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2375">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2376">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2376">Core</span></span>

* <span data-ttu-id="8cc5e-2377">末尾にスラッシュが付いている ADFS 権限 URL の処理を Azure Stack に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2377">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2378">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2378">Appservice</span></span>

* <span data-ttu-id="8cc5e-2379">新しいコマンド `webapp update` による全体的な更新を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2379">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-2380">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2380">Batch</span></span>

* <span data-ttu-id="8cc5e-2381">Batch SDK 4.0.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2381">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="8cc5e-2382">publish:offer:sku:version に加えて ARM イメージ参照をサポートするように VirtualMachineConfiguration の `--image` オプションを更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2382">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="8cc5e-2383">Batch 拡張機能のコマンドの新しい CLI 拡張モデルのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2383">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="8cc5e-2384">コンポーネント モデルから Batch のサポートを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2384">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="8cc5e-2385">Batchai</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2385">Batchai</span></span>

* <span data-ttu-id="8cc5e-2386">Batch AI モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2386">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-2387">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2387">Keyvault</span></span>

* <span data-ttu-id="8cc5e-2388">Azure Stack で ADFS を使用したときの Key Vault の認証の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2388">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="8cc5e-2389">(#4448)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2389">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="8cc5e-2390">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2390">Network</span></span>

* <span data-ttu-id="8cc5e-2391">アドレス プールを空にできるように `application-gateway address-pool create` の `--server` 引数を省略可能に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2391">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="8cc5e-2392">最新機能をサポートするように `traffic-manager` を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2392">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2393">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2393">Resource</span></span>

* <span data-ttu-id="8cc5e-2394">リソース グループ名に関する `--resource-group/-g` オプションのサポートを `group` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2394">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="8cc5e-2395">サブスクリプション レベルのロックを処理するための `account lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2395">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="8cc5e-2396">グループ レベルのロックを処理するための `group lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2396">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="8cc5e-2397">リソース レベルのロックを処理するための `resource lock` 用のコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2397">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2398">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2398">Sql</span></span>

* <span data-ttu-id="8cc5e-2399">SQL Transparent Data Encryption (TDE) および Bring Your Own Key による TDE のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2399">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="8cc5e-2400">`db list-deleted` コマンドと `db restore --deleted-time` パラメーターを追加し、削除したデータベースを検索して復元できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2400">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="8cc5e-2401">`db op list` と `db op cancel` を追加し、データベースに対して実行中の操作を一覧表示およびキャンセルできるようにしました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2401">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2402">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2402">Storage</span></span>

* <span data-ttu-id="8cc5e-2403">ファイル共有スナップショットのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2403">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2404">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2404">Vm</span></span>

* <span data-ttu-id="8cc5e-2405">`-d` を使用すると存在しないプライベート IP アドレスでクラッシュする `vm show` のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2405">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="8cc5e-2406">[プレビュー] ローリング アップグレードのサポートを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2406">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="8cc5e-2407">`vm encryption enable` による暗号化設定の更新のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2407">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="8cc5e-2408">`--os-disk-size-gb` パラメーターを `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2408">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="8cc5e-2409">Windows 用の `--license-type` パラメーターを `vmss create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2409">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="8cc5e-2410">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2410">September 22, 2017</span></span>

<span data-ttu-id="8cc5e-2411">バージョン 2.0.18</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2411">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2412">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2412">Resource</span></span>

* <span data-ttu-id="8cc5e-2413">組み込みのポリシー定義を表示するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2413">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="8cc5e-2414">ポリシー定義を作成するためのサポート モード パラメーターを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2414">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="8cc5e-2415">UI の定義とテンプレートのサポートを `managedapp definition create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2415">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="8cc5e-2416">[重大な変更] `managedapp` のリソースの種類を `appliances` から `applications`、`applianceDefinitions` から `applicationDefinitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2416">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2417">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2417">Network</span></span>

* <span data-ttu-id="8cc5e-2418">可用性ゾーンのサポートを `network lb` および `network public-ip` サブコマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2418">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="8cc5e-2419">IPv6 Microsoft ピアリングのサポートを `express-route` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2419">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="8cc5e-2420">`asg` アプリケーション セキュリティ グループのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2420">Added `asg` application security group commands</span></span>
* <span data-ttu-id="8cc5e-2421">`--application-security-groups` 引数を `nic [create|ip-config create|ip-config update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2421">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="8cc5e-2422">`--source-asgs` 引数と `--destination-asgs` 引数を `nsg rule [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2422">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2423">`--ddos-protection` 引数と `--vm-protection` 引数を `vnet [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2423">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2424">`network [vnet-gateway|vpn-client|show-url]` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2424">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2425">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2425">Storage</span></span>

* <span data-ttu-id="8cc5e-2426">SDK の更新後に `storage account network-rule` コマンドが失敗する可能性がある問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2426">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="8cc5e-2427">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2427">Eventgrid</span></span>

* <span data-ttu-id="8cc5e-2428">新しい API バージョン "2017-09-15-preview" を使用するように Azure Event Grid Python SDK を更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2428">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2429">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2429">SQL</span></span>

* <span data-ttu-id="8cc5e-2430">`sql server list` の引数 `--resource-group` を省略可能に変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2430">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="8cc5e-2431">指定しなかった場合は、サブスクリプション内のすべての SQL Server が返されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2431">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="8cc5e-2432">`--no-wait` パラメーターを `db [create|copy|restore|update|replica create|create|update]` と `dw [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2432">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-2433">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2433">Keyvault</span></span>

* <span data-ttu-id="8cc5e-2434">プロキシの内側からの KeyVault コマンドのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2434">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2435">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2435">VM</span></span>

* <span data-ttu-id="8cc5e-2436">可用性ゾーンに対するサポートを `[vm|vmss|disk] create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2436">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="8cc5e-2437">`vmss create` で `--app-gateway ID` を使用するとエラーになる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2437">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="8cc5e-2438">`--asgs` 引数を `vm create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2438">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="8cc5e-2439">`vm run-command` を使用して VM でコマンドを実行するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2439">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="8cc5e-2440">[プレビュー] `vmss encryption` による VMSS ディスク暗号化のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2440">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="8cc5e-2441">`vm perform-maintenance` を使用して VM のメンテナンスを行うためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2441">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2442">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2442">ACS</span></span>

* <span data-ttu-id="8cc5e-2443">ACS プレビューのリージョン用に `--orchestrator-release` 引数を `acs create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2443">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2444">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2444">Appservice</span></span>

* <span data-ttu-id="8cc5e-2445">`webapp auth [update|show]` で認証設定を更新および表示する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2445">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="8cc5e-2446">バックアップ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2446">Backup</span></span>

* <span data-ttu-id="8cc5e-2447">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2447">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="8cc5e-2448">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2448">September 11, 2017</span></span>

<span data-ttu-id="8cc5e-2449">バージョン 2.0.17</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2449">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="8cc5e-2450">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2450">Core</span></span>

* <span data-ttu-id="8cc5e-2451">テレメトリで独自の関連付け ID を設定するコマンド モジュールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2451">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="8cc5e-2452">テレメトリが診断モードに設定された際に発生する JSON ダンプの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2452">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2453">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2453">Acs</span></span>

* <span data-ttu-id="8cc5e-2454">`acs list-locations` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2454">Added `acs list-locations` command</span></span>
* <span data-ttu-id="8cc5e-2455">`ssh-key-file` を予想される既定値と共に使用されるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2455">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2456">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2456">Appservice</span></span>

* <span data-ttu-id="8cc5e-2457">アクティブなサービス プラン以外のリソース グループで Web アプリを作成する機能を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2457">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-2458">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2458">CDN</span></span>

* <span data-ttu-id="8cc5e-2459">`cdn custom-domain create` の "CustomDomain is not interable" バグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2459">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="8cc5e-2460">拡張機能</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2460">Extension</span></span>

* <span data-ttu-id="8cc5e-2461">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2461">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-2462">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2462">Keyvault</span></span>

* <span data-ttu-id="8cc5e-2463">`keyvault set-policy` について、アクセス許可の大文字と小文字が区別される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2463">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2464">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2464">Network</span></span>

* <span data-ttu-id="8cc5e-2465">`vnet list-private-access-services` の名前を `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2465">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8cc5e-2466">`vnet subnet create/update` の `--private-access-services` 引数の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2466">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="8cc5e-2467">`nsg rule create/update` に対する複数の IP 範囲およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2467">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="8cc5e-2468">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2468">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8cc5e-2469">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2469">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2470">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2470">Resource</span></span>

* <span data-ttu-id="8cc5e-2471">`policy definition create` と `policy definition update` でリソース ポリシーのパラメーター定義を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2471">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="8cc5e-2472">`policy assignment create` でパラメーター値を渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2472">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="8cc5e-2473">すべてのパラメーターについて JSON またはファイルを渡せるようにします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2473">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="8cc5e-2474">API バージョンを増やしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2474">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2475">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2475">SQL</span></span>

* <span data-ttu-id="8cc5e-2476">`sql server vnet-rule` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2476">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2477">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2477">VM</span></span>

* <span data-ttu-id="8cc5e-2478">修正済み:`--scope` が指定されないとアクセス権が割り当てられない</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2478">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="8cc5e-2479">修正済み:ポータルと同じ拡張機能の名前付けが行われる</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2479">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="8cc5e-2480">`[vm|vmss] create` 出力から `subscription` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2480">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="8cc5e-2481">修正済み: `[vm|vmss] create` ストレージ SKU がイメージ付きのデータ ディスクに適用されない</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2481">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="8cc5e-2482">修正済み: `vm format-secret --secrets` で、改行によって分かれた ID を使用できない</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2482">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="8cc5e-2483">2017 年 8 月 31 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2483">August 31, 2017</span></span>

<span data-ttu-id="8cc5e-2484">バージョン 2.0.16</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2484">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-2485">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2485">Keyvault</span></span>

* <span data-ttu-id="8cc5e-2486">`secret download` でシークレット エンコードを自動的に解決しようとする際に発生するバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2486">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="8cc5e-2487">SF</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2487">Sf</span></span>

* <span data-ttu-id="8cc5e-2488">すべてのコマンドが非推奨とされ、Service Fabric CLI (sfctl) が優先されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2488">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2489">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2489">Storage</span></span>

* <span data-ttu-id="8cc5e-2490">ネットワーク ACL 機能がサポートされていないリージョンでストレージ アカウントを作成できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2490">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="8cc5e-2491">コンテンツの種類とエンコードがどちらも指定されていない場合、BLOB とファイルのアップロード中にコンテンツの種類とエンコードを決定します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2491">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="8cc5e-2492">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2492">August 28, 2017</span></span>

<span data-ttu-id="8cc5e-2493">バージョン 2.0.15</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2493">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="8cc5e-2494">CLI</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2494">CLI</span></span>

* <span data-ttu-id="8cc5e-2495">`--version` に法的事項を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2495">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2496">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2496">ACS</span></span>

* <span data-ttu-id="8cc5e-2497">プレビュー リージョンを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2497">Corrected preview regions</span></span>
* <span data-ttu-id="8cc5e-2498">既定の `dns_name_prefix` を正しい形式にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2498">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="8cc5e-2499">ACS コマンド出力を最適化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2499">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2500">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2500">Appservice</span></span>

* <span data-ttu-id="8cc5e-2501">[重大な変更] `az webapp config appsettings [delete|set]` の出力の不整合を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2501">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="8cc5e-2502">`az webapp config container set --docker-custom-image-name` の `-i` の新しいエイリアスを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2502">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="8cc5e-2503">`az webapp log show` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2503">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="8cc5e-2504">App Service プラン、メトリック、または DNS 登録を保持するために、`az webapp delete` の新しい引数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2504">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="8cc5e-2505">修正済み:スロット設定の正常な検出</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2505">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-2506">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2506">IoT</span></span>

* <span data-ttu-id="8cc5e-2507">#3934 を修正しました:ポリシーの作成で既存のポリシーが消去されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2507">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2508">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2508">Network</span></span>

* <span data-ttu-id="8cc5e-2509">[重大な変更] 名前を `vnet list-private-access-services` から `vnet list-endpoint-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2509">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="8cc5e-2510">[重大な変更] `vnet subnet [create|update]` のオプション `--private-access-services` の名前を `--service-endpoints` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2510">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2511">`nsg rule [create|update]` に対する複数 IP およびポート範囲のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2511">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="8cc5e-2512">`lb create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2512">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="8cc5e-2513">`public-ip create` に対する SKU のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2513">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2514">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2514">Profile</span></span>

* <span data-ttu-id="8cc5e-2515">仮想マシンの ID を使用してログインするために、`--msi` と `--msi-port` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2515">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8cc5e-2516">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2516">Service Fabric</span></span>

* <span data-ttu-id="8cc5e-2517">プレビュー リリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2517">Preview release</span></span>
* <span data-ttu-id="8cc5e-2518">コマンドに対するレジストリのユーザー/パスワード規則を簡略化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2518">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="8cc5e-2519">パラメーターを渡した後でもユーザーにパスワードの入力が求められる問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2519">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="8cc5e-2520">空の `registry_cred` のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2520">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2521">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2521">Storage</span></span>

* <span data-ttu-id="8cc5e-2522">BLOB 層の設定を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2522">Enabled setting blob tier</span></span>
* <span data-ttu-id="8cc5e-2523">サービス トンネリングをサポートするために、`--bypass` 引数と `--default-action` 引数を `storage account [create|update]` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2523">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="8cc5e-2524">VNET ルールと IP ベースのルールを `storage account network-rule` に追加するためのコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2524">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="8cc5e-2525">顧客管理キーによるサービスの暗号化を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2525">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="8cc5e-2526">[重大な変更] `az storage account create and az storage account update` コマンドの `--encryption` オプションの名前を `--encryption-services` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2526">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="8cc5e-2527">修正済み #4220: `az storage account update encryption` - 構文の不一致</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2527">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2528">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2528">VM</span></span>

* <span data-ttu-id="8cc5e-2529">`vmss get-instance-view` で `--instance-id *` を使用した場合に、余分な間違えた情報が表示される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2529">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="8cc5e-2530">`vmss create` に `--lb-sku` のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2530">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="8cc5e-2531">`[vm|vmss] create` の管理者名ブラックリストから人物名を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2531">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="8cc5e-2532">イメージからプラン情報を抽出できない場合に `[vm|vmss] create` がエラーをスローする問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2532">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="8cc5e-2533">内部 LB で vmms scaleset を作成するときのクラッシュを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2533">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="8cc5e-2534">`vm availability-set create` で `--no-wait` 引数が機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2534">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="8cc5e-2535">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2535">August 15, 2017</span></span>

<span data-ttu-id="8cc5e-2536">バージョン 2.0.14</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2536">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2537">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2537">ACS</span></span>

* <span data-ttu-id="8cc5e-2538">kubernetes の sshMaster0 ポート番号を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2538">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2539">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2539">Appservice</span></span>

* <span data-ttu-id="8cc5e-2540">新しい Git ベースの Linux Web アプリを作成するときの例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2540">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="8cc5e-2541">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2541">Event Grid</span></span>

* <span data-ttu-id="8cc5e-2542">SDK 依存関係を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2542">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="8cc5e-2543">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2543">August 11, 2017</span></span>

<span data-ttu-id="8cc5e-2544">バージョン 2.0.13</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2544">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2545">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2545">ACS</span></span>

* <span data-ttu-id="8cc5e-2546">プレビュー リージョンを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2546">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-2547">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2547">Batch</span></span>

* <span data-ttu-id="8cc5e-2548">Batch SDK 3.1.0 と Batch Management SDK 4.1.0 に更新しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2548">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="8cc5e-2549">ジョブのタスク数を表示する新しいコマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2549">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="8cc5e-2550">リソース ファイルの SAS URL 処理のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2550">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="8cc5e-2551">Batch アカウントのエンドポイントで、オプションの "https://" プレフィックスがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2551">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="8cc5e-2552">ジョブに対する 100 を超えるタスクのリストの追加をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2552">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="8cc5e-2553">拡張機能コマンド モジュールの読み込みのデバッグ ログを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2553">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="8cc5e-2554">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2554">Component</span></span>

* <span data-ttu-id="8cc5e-2555">"az component" コマンドに非推奨警告を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2555">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="8cc5e-2556">コンテナー</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2556">Container</span></span>

* <span data-ttu-id="8cc5e-2557">`create`:環境変数内で等号を使用できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2557">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="8cc5e-2558">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2558">Data Lake Store</span></span>

* <span data-ttu-id="8cc5e-2559">プログレス コントロールを有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2559">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="8cc5e-2560">Event Grid</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2560">Event Grid</span></span>

* <span data-ttu-id="8cc5e-2561">最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2561">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2562">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2562">Network</span></span>

* <span data-ttu-id="8cc5e-2563">`lb`:特定の子リソース名が省略された場合に正しく解決されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2563">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="8cc5e-2564">`application-gateway {subresource} delete`:`--no-wait` が受け入れられない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2564">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="8cc5e-2565">`application-gateway http-settings update`:`--connection-draining-timeout` を無効にできない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2565">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="8cc5e-2566">`az network vpn-connection ipsec-policy add` での予期しないキーワード引数 `sa_data_size_kilobyes` のエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2566">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2567">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2567">Profile</span></span>

* <span data-ttu-id="8cc5e-2568">`account list`:サーバーの最新のサブスクリプションを同期する `--refresh` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2568">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2569">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2569">Storage</span></span>

* <span data-ttu-id="8cc5e-2570">システムによって割り当てられた ID によるストレージ アカウントの更新を有効にします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2570">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2571">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2571">VM</span></span>

* <span data-ttu-id="8cc5e-2572">`availability-set`:変換時の障害ドメイン数を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2572">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="8cc5e-2573">`list-skus` コマンドを公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2573">Exposed `list-skus` command</span></span>
* <span data-ttu-id="8cc5e-2574">ロールの割り当てを作成しない ID の割り当てをサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2574">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="8cc5e-2575">データ ディスクのアタッチ時にストレージ SKU を適用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2575">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="8cc5e-2576">管理ディスクを使用する場合の既定の os-disk 名とストレージ SKU を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2576">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="8cc5e-2577">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2577">July 28, 2017</span></span>

<span data-ttu-id="8cc5e-2578">バージョン 2.0.12</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2578">Version 2.0.12</span></span>

* <span data-ttu-id="8cc5e-2579">コンテナー コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2579">Added container commands</span></span>
* <span data-ttu-id="8cc5e-2580">請求および使用量モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2580">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="8cc5e-2581">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2581">Core</span></span>

* <span data-ttu-id="8cc5e-2582">サービス プリンシパルの SDK 認証情報と証明書を出力します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2582">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="8cc5e-2583">デプロイの進行状況の例外を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2583">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="8cc5e-2584">サブスクリプション クライアントを作成するために、現在のクラウドの ARM エンドポイントを使用します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2584">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="8cc5e-2585">clouds.config ファイルの同時処理機能が向上しました (#3636)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2585">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="8cc5e-2586">コマンド実行のたびにクライアント要求 ID を更新します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2586">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="8cc5e-2587">正しい SDK プロファイルでサブスクリプション クライアントを作成します (#3635)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2587">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="8cc5e-2588">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2588">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8cc5e-2589">jmespath クエリを通じてテーブル出力フィールドを選択するサポートを追加しました (#3581)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2589">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="8cc5e-2590">解析引数のミュートを改善し、ジェスチャによる履歴を追加しました (#3434)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2590">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="8cc5e-2591">正しい SDK プロファイルでサブスクリプション クライアントを作成します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2591">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="8cc5e-2592">すべての既存のレコーディング ファイルを最新のフォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2592">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="8cc5e-2593">VM/VMSS 作成のべき等を修正しました (#3586)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2593">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="8cc5e-2594">コマンド パスで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2594">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="8cc5e-2595">特定のブール型パラメーターで大文字と小文字が区別されなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2595">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="8cc5e-2596">Azure Stack のような ADFS オンプレミス サーバーへのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2596">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="8cc5e-2597">clouds.config への同時書き込みを修正しました (#3255)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2597">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="8cc5e-2598">ACR</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2598">ACR</span></span>

* <span data-ttu-id="8cc5e-2599">管理対象レジストリ用の `show-usage` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2599">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="8cc5e-2600">管理対象レジストリの SKU 更新をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2600">Support SKU update for managed registries</span></span>
* <span data-ttu-id="8cc5e-2601">管理対象レジストリと管理 SKU を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2601">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="8cc5e-2602">管理対象レジストリの webhook と acr webhook コマンド モジュールを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2602">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="8cc5e-2603">AAD 認証と acr login コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2603">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="8cc5e-2604">Docker リポジトリ、マニフェスト、タグ用の delete コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2604">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2605">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2605">ACS</span></span>

* <span data-ttu-id="8cc5e-2606">API バージョン 2017-07-01 をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2606">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2607">Appservice</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2607">Appservice</span></span>

* <span data-ttu-id="8cc5e-2608">Linux Web アプリの一覧表示で何も返されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2608">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="8cc5e-2609">acr からの資格情報の取得をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2609">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="8cc5e-2610">`appservice web` のすべてのコマンドを削除します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2610">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="8cc5e-2611">コマンド出力で Docker レジストリのパスワードをマスクします (#3656)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2611">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="8cc5e-2612">macOS でエラーにならずに既定のブラウザーが使用されます (#3623)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2612">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="8cc5e-2613">`webapp log tail` と `webapp log download` のヘルプを改善します (#3624)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2613">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="8cc5e-2614">静的ルーティングを構成するための `traffic-routing` コマンドを公開しました (#3566)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2614">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="8cc5e-2615">ソース管理の構成で信頼性のための修正が追加されました (#3245)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2615">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="8cc5e-2616">Windows Web アプリ用の `webapp config update` から、サポートされていない `--node-version` 引数を削除しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2616">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="8cc5e-2617">代わりに `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...` を使用してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2617">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="8cc5e-2618">Batch</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2618">Batch</span></span>

* <span data-ttu-id="8cc5e-2619">Batch SDK 3.0.0 に更新して、プール内の優先度が低い VM がサポートされるようにしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2619">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="8cc5e-2620">`pool create` のオプション `--target-dedicated` の名前を `--target-dedicated-nodes` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2620">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="8cc5e-2621">`pool create` のオプションの `--target-low-priority-nodes` と `--application-licenses` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2621">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="8cc5e-2622">CDN</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2622">CDN</span></span>

* <span data-ttu-id="8cc5e-2623">`--profile-name` によって指定されたプロファイルが存在しない場合に表示される `cdn endpoint list` のエラー メッセージを、より適切な内容に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2623">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="8cc5e-2624">クラウド</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2624">Cloud</span></span>

* <span data-ttu-id="8cc5e-2625">クラウド メタデータ エンドポイントの API バージョンを YYYY-MM-DD 形式に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2625">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="8cc5e-2626">ギャラリー エンドポイントは必須ではありません</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2626">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="8cc5e-2627">ARM リソース マネージャー エンドポイントだけでのクラウドの登録をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2627">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="8cc5e-2628">`cloud set` で現在のクラウドを選択するときにプロファイルを選択できるオプションを提供しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2628">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="8cc5e-2629">`endpoint_vm_image_alias_doc` を公開しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2629">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-2630">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2630">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-2631">カスタム パーティション キーでコレクションを作成できるように修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2631">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="8cc5e-2632">既定のコレクション TTL のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2632">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8cc5e-2633">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2633">Data Lake Analytics</span></span>

* <span data-ttu-id="8cc5e-2634">コンピューティング ポリシー管理用のコマンドを `dla account compute-policy` 見出しの下に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2634">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="8cc5e-2635">`dla job pipeline show` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2635">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="8cc5e-2636">`dla job recurrence list` を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2636">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8cc5e-2637">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2637">Data Lake Store</span></span>

* <span data-ttu-id="8cc5e-2638">ユーザー管理のキー コンテナーのキー ローテーションのサポートを `dls account update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2638">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="8cc5e-2639">基になる Data Lake Store ファイル システム SDK のバージョンを更新して、パフォーマンスの問題に対応しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2639">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="8cc5e-2640">コマンド `dls enable-key-vault` を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2640">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="8cc5e-2641">このコマンドでは、Data Lake Store アカウント内でデータの暗号化を使用するために、ユーザー指定のキー コンテナーの有効化が試行されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2641">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="8cc5e-2642">対話</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2642">Interactive</span></span>

* <span data-ttu-id="8cc5e-2643">キャッシュされたコマンドを使用することで、起動時間が向上しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2643">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="8cc5e-2644">テスト カバレッジが増えました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2644">Increased test coverage</span></span>
* <span data-ttu-id="8cc5e-2645">"?" ジェスチャが次のコマンドにも挿入されるよう強化しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2645">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="8cc5e-2646">プロファイル 2017-03-09-profile-preview との対話エラーを修正しました (#3587)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2646">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="8cc5e-2647">`--version` を対話モードのパラメーターとして使用できるようにしました (#3645)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2647">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="8cc5e-2648">対話モードで検証の完了時にエラーがスローされないようにします (#3570)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2648">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="8cc5e-2649">テンプレート デプロイの進行状況レポート (#3510)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2649">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="8cc5e-2650">`--progress` フラグを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2650">Added `--progress` flag</span></span>
* <span data-ttu-id="8cc5e-2651">入力候補から `--debug` と `--verbose` を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2651">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="8cc5e-2652">入力候補から `interactive` を削除しました (#3324)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2652">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="8cc5e-2653">IoT</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2653">IoT</span></span>

* <span data-ttu-id="8cc5e-2654">ポリシーの作成で既存のポリシーが消去されないように修正しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2654">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="8cc5e-2655">(#3934)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2655">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="8cc5e-2656">Key Vault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2656">Key vault</span></span>

* <span data-ttu-id="8cc5e-2657">キー コンテナーの回復機能のために、以下のコマンドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2657">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="8cc5e-2658">`keyvault` サブコマンドの `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2658">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="8cc5e-2659">`keyvault secret` サブコマンドの `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2659">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8cc5e-2660">`keyvault certificate` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2660">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="8cc5e-2661">`keyvault key` サブコマンドの `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2661">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="8cc5e-2662">サービス プリンシパルのキー コンテナーの統合を追加しました (#3133)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2662">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="8cc5e-2663">キー コンテナー データプレーンを 0.3.2 に更新しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2663">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="8cc5e-2664">(#3307)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2664">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="8cc5e-2665">ラボ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2665">Lab</span></span>

* <span data-ttu-id="8cc5e-2666">`az lab vm claim` を通じてラボ内の任意の VM を要求するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2666">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="8cc5e-2667">`az lab vm list` と `az lab vm show` のテーブル出力フォーマッタを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2667">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2668">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2668">Monitor</span></span>

* <span data-ttu-id="8cc5e-2669">`monitor autoscale-settings get-parameters-template` コマンドのテンプレート ファイルを修正しました (#3349)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2669">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="8cc5e-2670">`monitor alert-rule-incidents list` の名前を `monitor alert list-incidents` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2670">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="8cc5e-2671">`monitor alert-rule-incidents show` の名前を `monitor alert show-incident` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2671">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="8cc5e-2672">`monitor metric-defintions list` の名前を `monitor metrics list-definitions` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2672">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="8cc5e-2673">`monitor alert-rules` の名前を `monitor alert` に変更しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2673">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="8cc5e-2674">`monitor alert create` を次のように変更しました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2674">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="8cc5e-2675">`condition` および `action` サブコマンドが JSON を受け入れなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2675">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="8cc5e-2676">ルール作成プロセスを簡略化するために多数のパラメーターを追加します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2676">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="8cc5e-2677">`location` が必須ではなくなりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2677">`location` no longer required</span></span>
  * <span data-ttu-id="8cc5e-2678">ターゲットの名前と ID のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2678">Add name and ID support for target</span></span>
  * <span data-ttu-id="8cc5e-2679">`--alert-rule-resource-name` を削除します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2679">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="8cc5e-2680">`is-enabled` の名前を `enabled` に変更し、省略可能にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2680">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="8cc5e-2681">`description` の既定値が、指定された条件に基づいて設定されるようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2681">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="8cc5e-2682">新しい形式をわかりやすく示すための例を追加します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2682">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="8cc5e-2683">`monitor metric` コマンドの名前または ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2683">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="8cc5e-2684">`monitor alert rule update` に便利な引数と例を追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2684">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2685">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2685">Network</span></span>

* <span data-ttu-id="8cc5e-2686">`list-private-access-services` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2686">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="8cc5e-2687">`--private-access-services` 引数を `vnet subnet create` と `vnet subnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2687">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="8cc5e-2688">`application-gateway redirect-config create` が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2688">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="8cc5e-2689">`application-gateway redirect-config update` で `--no-wait` を指定しても機能しない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2689">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="8cc5e-2690">`application-gateway address-pool create` と `application-gateway address-pool update` で `--servers` 引数を使用する場合のバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2690">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="8cc5e-2691">`application-gateway redirect-config` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2691">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="8cc5e-2692">`list-options`、`predefined list`、`predefined show` の各コマンドを `application-gateway ssl-policy` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2692">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="8cc5e-2693">`--name`、`--cipher-suites`、`--min-protocol-version` の各引数を `application-gateway ssl-policy set` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2693">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="8cc5e-2694">`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path` の各引数を `application-gateway http-settings create` と `application-gateway http-settings update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2694">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="8cc5e-2695">`--default-redirect-config` 引数と `--redirect-config` 引数を `application-gateway url-path-map create` と `application-gateway url-path-map update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2695">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="8cc5e-2696">`--redirect-config` 引数を `application-gateway url-path-map rule create` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2696">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="8cc5e-2697">`--no-wait` のサポートを `application-gateway url-path-map rule delete` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2697">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="8cc5e-2698">`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes` の各引数を `application-gateway probe create` と `application-gateway probe update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2698">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="8cc5e-2699">`--redirect-config` 引数を `application-gateway rule create` と `application-gateway rule update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2699">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="8cc5e-2700">`--accelerated-networking` のサポートを `nic create` と `nic update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2700">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="8cc5e-2701">`nic create` から `--internal-dns-name-suffix` 引数を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2701">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="8cc5e-2702">`--dns-servers` のサポートを `nic update` と `nic create` に追加しました:--dns-servers のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2702">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="8cc5e-2703">`local-gateway create` で `--local-address-prefixes` が無視されるバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2703">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="8cc5e-2704">`--dns-servers` のサポートを `vnet update` に追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2704">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="8cc5e-2705">`express-route peering create` でルート フィルター処理をせずにピアリングを作成するときのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2705">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="8cc5e-2706">`express-route update` で `--provider` および `--bandwidth` 引数が機能しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2706">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="8cc5e-2707">`network watcher show-topology` の既定値設定ロジックのバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2707">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="8cc5e-2708">`network list-usages` の出力書式設定を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2708">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="8cc5e-2709">`application-gateway http-listener create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2709">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="8cc5e-2710">`application-gateway rule create` に既定のアドレス プール、HTTP 設定、および HTTP リスナーを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2710">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="8cc5e-2711">`lb rule create` に既定のフロントエンド IP およびバックエンド プールを使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2711">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="8cc5e-2712">`lb inbound-nat-rule create` に既定のフロントエンド IP を使用します (1 つしかない場合)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2712">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2713">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2713">Profile</span></span>

* <span data-ttu-id="8cc5e-2714">管理対象 ID での VM 内のログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2714">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="8cc5e-2715">`account show` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2715">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="8cc5e-2716">"--expanded-view" を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2716">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="8cc5e-2717">生の AAD トークンを提供するための `get-access-token` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2717">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="8cc5e-2718">サブスクリプションが関連付けられていないユーザー アカウントでのログインをサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2718">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="8cc5e-2719">RDBMS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2719">RDBMS</span></span>

* <span data-ttu-id="8cc5e-2720">サブスクリプション全体のサーバーの一覧表示をサポートします (#3417)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2720">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="8cc5e-2721">`% server_type` が見つからないために `%s` が処理されない問題を修正しました (#3393)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2721">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="8cc5e-2722">ドキュメント ソース マップを修正し、検証するための CI タスクを追加しました (#3361)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2722">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="8cc5e-2723">MySQL および PostgreSQL のヘルプを修正しました (#3369)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2723">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2724">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2724">Resource</span></span>

* <span data-ttu-id="8cc5e-2725">`group deployment create` の不足しているパラメーターの指定を求めるメッセージを改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2725">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="8cc5e-2726">`--parameters KEY=VALUE` 構文の解析を改善しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2726">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="8cc5e-2727">`group deployment create` のパラメーター ファイルが `@<file>` 構文で認識されなくなった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2727">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="8cc5e-2728">`resource` および `managedapp` コマンドで `--ids` 引数をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2728">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="8cc5e-2729">いくつかの解析およびエラー メッセージを修正しました (#3584)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2729">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="8cc5e-2730">`<resource-namespace>` と `<resource-type>` を受け入れるよう、`lock` コマンドの `--resource-type` の解析を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2730">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="8cc5e-2731">テンプレート リンク テンプレートのパラメーター チェックを追加しました (#3629)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2731">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="8cc5e-2732">`KEY=VALUE` 構文でデプロイ パラメーターを指定するためのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2732">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2733">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2733">Role</span></span>

* <span data-ttu-id="8cc5e-2734">`create-for-rbac` で SDK 認証ファイル形式での出力をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2734">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="8cc5e-2735">サービス プリンシパルを削除するときに、ロールの割り当てと、関連する AAD アプリケーションがクリーンアップされるようになりました (#3610)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2735">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="8cc5e-2736">`app create` の引数 `--start-date` および `--end-date` の説明に時刻形式を含めます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2736">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="8cc5e-2737">`--expanded-view` を使用した場合に非推奨警告を表示します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2737">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="8cc5e-2738">キー コンテナーの統合を `create-for-rbac` および `reset-credentials` コマンドに追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2738">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="8cc5e-2739">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2739">Service Fabric</span></span>
* <span data-ttu-id="8cc5e-2740">アプリケーション内の大きなファイルがアップロード時に切り詰められる問題を修正しました (#3666)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2740">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="8cc5e-2741">Service Fabric コマンドのテストを追加しました (#3424)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2741">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="8cc5e-2742">多数の Service Fabric コマンドを修正しました (#3234)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2742">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2743">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2743">SQL</span></span>

* <span data-ttu-id="8cc5e-2744">壊れた `sql server create` `--identity` パラメーターを削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2744">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="8cc5e-2745">`sql server create` および `sql server update` コマンドの出力からパスワード値を削除しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2745">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="8cc5e-2746">`sql db list-editions` および `sql elastic-pool list-editions` コマンドを追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2746">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2747">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2747">Storage</span></span>

* <span data-ttu-id="8cc5e-2748">`storage blob list`、`storage container list`、`storage share list` の各コマンドから `--marker` オプションを削除しました (#3745)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2748">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="8cc5e-2749">https 専用ストレージ アカウントの作成を有効にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2749">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="8cc5e-2750">storage metrics、logging、cors の各コマンドを更新しました (#3495)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2750">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="8cc5e-2751">CORS add からの例外メッセージを言い換えました (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2751">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="8cc5e-2752">ジェネレーターをドライ ラン モードのダウンロード バッチ コマンド内の一覧に変換しました (#3592)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2752">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="8cc5e-2753">BLOB ダウンロード バッチのドライ ランの問題を修正しました (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2753">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2754">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2754">VM</span></span>

* <span data-ttu-id="8cc5e-2755">nsg の構成をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2755">Support configuring nsg</span></span>
* <span data-ttu-id="8cc5e-2756">DNS サーバーが正しく構成されないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2756">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="8cc5e-2757">管理対象のサービス ID をサポートします</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2757">Support managed service identities</span></span>
* <span data-ttu-id="8cc5e-2758">既存のロード バランサーを使用する `cmss create` で `--backend-pool-name` が必要だった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2758">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="8cc5e-2759">`vm image create` で作成された datadisks の lun を 0 から開始します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2759">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="8cc5e-2760">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2760">May 10, 2017</span></span>

<span data-ttu-id="8cc5e-2761">バージョン 2.0.6</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2761">Version 2.0.6</span></span>

* <span data-ttu-id="8cc5e-2762">documentdb から cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2762">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="8cc5e-2763">rdbms (mysql、postgres) が追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2763">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="8cc5e-2764">Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2764">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="8cc5e-2765">Cognitive Services モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2765">Include Cognitive Services module</span></span>
* <span data-ttu-id="8cc5e-2766">Service Fabric モジュールが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2766">Include Service Fabric module</span></span>
* <span data-ttu-id="8cc5e-2767">対話型モジュールが追加されました (az-shell の名前変更)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2767">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="8cc5e-2768">CDN コマンドに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2768">Add support for CDN commands</span></span>
* <span data-ttu-id="8cc5e-2769">コンテナー モジュールが削除されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2769">Remove Container module</span></span>
* <span data-ttu-id="8cc5e-2770">"az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2770">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="8cc5e-2771">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2771">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="8cc5e-2772">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2772">Core</span></span>

* <span data-ttu-id="8cc5e-2773">コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2773">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="8cc5e-2774">パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2774">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="8cc5e-2775">16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2775">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="8cc5e-2776">Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2776">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="8cc5e-2777">Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2777">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="8cc5e-2778">ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2778">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="8cc5e-2779">コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2779">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="8cc5e-2780">コア:accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2780">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="8cc5e-2781">コア:構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2781">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="8cc5e-2782">コア:パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2782">core: Improved performance</span></span>
* <span data-ttu-id="8cc5e-2783">コア:カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2783">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="8cc5e-2784">コア:クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2784">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2785">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2785">ACS</span></span>

* <span data-ttu-id="8cc5e-2786">マスター数とエージェント数が文字列から整数に修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2786">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="8cc5e-2787">非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2787">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="8cc5e-2788">ドライラン検証用に "az acs create --validate" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2788">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="8cc5e-2789">スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2789">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2790">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2790">AppService</span></span>

* <span data-ttu-id="8cc5e-2791">関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2791">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="8cc5e-2792">Team Services (VSTS) が継続的デリバリー オプションとして "appservice web source-control config" に追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2792">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="8cc5e-2793">"az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2793">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="8cc5e-2794">WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2794">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="8cc5e-2795">"webapp list-runtimes" が公開されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2795">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="8cc5e-2796">接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2796">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="8cc5e-2797">プレビューでのスロット スワップがサポートされています</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2797">support slot swap with preview</span></span>
* <span data-ttu-id="8cc5e-2798">appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2798">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="8cc5e-2799">証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2799">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="8cc5e-2800">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2800">CosmosDB</span></span>

* <span data-ttu-id="8cc5e-2801">documentdb モジュールから cosmosdb に名前が変更されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2801">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="8cc5e-2802">DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2802">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="8cc5e-2803">データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2803">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="8cc5e-2804">新しい一貫性ポリシー ConsistentPrefix に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2804">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="8cc5e-2805">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2805">Data Lake Analytics</span></span>

* <span data-ttu-id="8cc5e-2806">ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2806">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="8cc5e-2807">新しいカタログ項目の種類: パッケージに対応するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2807">Add support for new catalog item type: package.</span></span> <span data-ttu-id="8cc5e-2808">`az dla catalog package` を介してアクセスされます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2808">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="8cc5e-2809">次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2809">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="8cc5e-2810">テーブル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2810">Table</span></span>
  * <span data-ttu-id="8cc5e-2811">テーブル値関数</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2811">Table valued function</span></span>
  * <span data-ttu-id="8cc5e-2812">表示</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2812">View</span></span>
  * <span data-ttu-id="8cc5e-2813">テーブルの統計。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2813">Table Statistics.</span></span> <span data-ttu-id="8cc5e-2814">スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2814">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="8cc5e-2815">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2815">Data Lake Store</span></span>

* <span data-ttu-id="8cc5e-2816">基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2816">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="8cc5e-2817">パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2817">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="8cc5e-2818">access show のヘルプがなかったため、</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2818">missed help for access show.</span></span> <span data-ttu-id="8cc5e-2819">追加しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2819">adding it.</span></span> <span data-ttu-id="8cc5e-2820">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2820">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="8cc5e-2821">検索</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2821">Find</span></span>

* <span data-ttu-id="8cc5e-2822">検索結果を改善し、検索インデックスのバージョン管理を可能にしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2822">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="8cc5e-2823">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2823">KeyVault</span></span>

* <span data-ttu-id="8cc5e-2824">BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2824">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="8cc5e-2825">BC:--expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2825">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="8cc5e-2826">--validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的にオーバーライドされます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2826">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="8cc5e-2827">"expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2827">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="8cc5e-2828">KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2828">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="8cc5e-2829">ラボ</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2829">Lab</span></span>

* <span data-ttu-id="8cc5e-2830">ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2830">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="8cc5e-2831">ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2831">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="8cc5e-2832">ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2832">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="8cc5e-2833">ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2833">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="8cc5e-2834">ラボ内でシークレットを管理するためのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2834">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="8cc5e-2835">監視</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2835">Monitor</span></span>

* <span data-ttu-id="8cc5e-2836">バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2836">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="8cc5e-2837">バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2837">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="8cc5e-2838">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2838">Network</span></span>

* <span data-ttu-id="8cc5e-2839">`network watcher test-connectivity` コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2839">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="8cc5e-2840">`network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2840">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="8cc5e-2841">Application Gateway 接続のドレインに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2841">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="8cc5e-2842">Application Gateway WAF 規則セットの構成に対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2842">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="8cc5e-2843">ExpressRoute ルート フィルターとルールに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2843">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="8cc5e-2844">TrafficManager の地理的なルーティングに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2844">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="8cc5e-2845">VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2845">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="8cc5e-2846">VPN 接続 IPSec ポリシーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2846">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="8cc5e-2847">`--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2847">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="8cc5e-2848">アクティブ/アクティブ VNet ゲートウェイに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2848">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="8cc5e-2849">`network vpn-connection list/show` コマンドの出力から null 値が削除されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2849">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="8cc5e-2850">BC:`vpn-connection create` の出力のバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2850">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="8cc5e-2851">"vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2851">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="8cc5e-2852">`dns zone import` でレコードが適切にインポートされないバグが修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2852">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="8cc5e-2853">`traffic-manager endpoint update` が動作しないバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2853">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="8cc5e-2854">"Network Watcher" プレビューのコマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2854">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="8cc5e-2855">プロファイル</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2855">Profile</span></span>

* <span data-ttu-id="8cc5e-2856">サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2856">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="8cc5e-2857">az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2857">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="8cc5e-2858">Redis</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2858">Redis</span></span>

* <span data-ttu-id="8cc5e-2859">Redis Cache のスケール機能も追加する更新コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2859">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="8cc5e-2860">"update-settings" コマンドが廃止されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2860">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="8cc5e-2861">リソース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2861">Resource</span></span>

* <span data-ttu-id="8cc5e-2862">managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2862">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="8cc5e-2863">"provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2863">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="8cc5e-2864">汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2864">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="8cc5e-2865">リソース解析および API バージョンの検索が修正されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2865">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="8cc5e-2866">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2866">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="8cc5e-2867">az lock update のドキュメントが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2867">Add docs for az lock update.</span></span> <span data-ttu-id="8cc5e-2868">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2868">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="8cc5e-2869">存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2869">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="8cc5e-2870">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2870">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="8cc5e-2871">[コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2871">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="8cc5e-2872">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2872">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="8cc5e-2873">parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2873">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="8cc5e-2874">Role</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2874">Role</span></span>

* <span data-ttu-id="8cc5e-2875">create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2875">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="8cc5e-2876">RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2876">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="8cc5e-2877">ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2877">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="8cc5e-2878">create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2878">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="8cc5e-2879">SQL</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2879">SQL</span></span>

* <span data-ttu-id="8cc5e-2880">az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2880">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="8cc5e-2881">SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2881">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="8cc5e-2882">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2882">Storage</span></span>

* <span data-ttu-id="8cc5e-2883">`storage account create` のリソース グループの場所に対する既定の場所</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2883">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="8cc5e-2884">増分 BLOB コピーに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2884">Add support for incremental blob copy</span></span>
* <span data-ttu-id="8cc5e-2885">大きなブロック BLOB アップロードに対応するようになりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2885">Add support for large block blob upload</span></span>
* <span data-ttu-id="8cc5e-2886">アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2886">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2887">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2887">VM</span></span>

* <span data-ttu-id="8cc5e-2888">avail-set: UD&FD ドメイン数が省略可能になりました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2888">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="8cc5e-2889">注:独立したクラウドの VM コマンド。次のマネージド ディスク関連機能は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2889">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="8cc5e-2890">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2890">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="8cc5e-2891">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2891">az vm/vmss disk</span></span>
  3. <span data-ttu-id="8cc5e-2892">"az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2892">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="8cc5e-2893">vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2893">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="8cc5e-2894">vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2894">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="8cc5e-2895">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2895">April 3, 2017</span></span>

<span data-ttu-id="8cc5e-2896">バージョン 2.0.2</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2896">Version 2.0.2</span></span>

<span data-ttu-id="8cc5e-2897">このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2897">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="8cc5e-2898">コア</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2898">Core</span></span>

* <span data-ttu-id="8cc5e-2899">既定の一覧に acr、lab、monitor、find モジュールを追加</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2899">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="8cc5e-2900">ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2900">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="8cc5e-2901">ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2901">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="8cc5e-2902">wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2902">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8cc5e-2903">コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2903">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="8cc5e-2904">不足しているテンプレート パラメーターの指定を求めるメッセージを追加</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2904">Add prompting for missing template parameters.</span></span> <span data-ttu-id="8cc5e-2905">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2905">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="8cc5e-2906">既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2906">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="8cc5e-2907">特定のテナントへのログインをサポート</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2907">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="8cc5e-2908">ACS</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2908">ACS</span></span>

* <span data-ttu-id="8cc5e-2909">[ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2909">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="8cc5e-2910">ssh キー パスワードの入力要求のサポートを追加</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2910">Add support for ssh key password prompting.</span></span> <span data-ttu-id="8cc5e-2911">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2911">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="8cc5e-2912">Windows クラスターのためのサポートを追加</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2912">Add support for windows clusters.</span></span> <span data-ttu-id="8cc5e-2913">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2913">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="8cc5e-2914">所有者から共同作成者へのロールの切り替え</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2914">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="8cc5e-2915">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2915">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="8cc5e-2916">AppService</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2916">AppService</span></span>

* <span data-ttu-id="8cc5e-2917">appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2917">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="8cc5e-2918">appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2918">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="8cc5e-2919">appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2919">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="8cc5e-2920">AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2920">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="8cc5e-2921">DataLake</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2921">DataLake</span></span>

* <span data-ttu-id="8cc5e-2922">Data Lake Analytics モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2922">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="8cc5e-2923">Data Lake Store モジュールの最初のリリース</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2923">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="8cc5e-2924">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2924">DocuemntDB</span></span>

* <span data-ttu-id="8cc5e-2925">DocumentDB:接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2925">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="8cc5e-2926">VM</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2926">VM</span></span>

* <span data-ttu-id="8cc5e-2927">[コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2927">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="8cc5e-2928">[VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2928">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="8cc5e-2929">VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2929">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="8cc5e-2930">wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2930">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="8cc5e-2931">仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート \* ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2931">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="8cc5e-2932">VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](<https://github.com/Azure/azure-cli/pull/2212>))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2932">Add --secrets for VM and virtual machine scale set ([#2212}(<https://github.com/Azure/azure-cli/pull/2212>))</span></span>
* <span data-ttu-id="8cc5e-2933">特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2933">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="8cc5e-2934">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2934">February 27, 2017</span></span>

<span data-ttu-id="8cc5e-2935">バージョン 2.0.0</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2935">Version 2.0.0</span></span>

<span data-ttu-id="8cc5e-2936">Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。一般公開に該当するのは、以下のコマンド モジュールです。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2936">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="8cc5e-2937">コンテナー サービス (acs)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2937">Container Service (acs)</span></span>
- <span data-ttu-id="8cc5e-2938">コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2938">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="8cc5e-2939">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2939">Networking</span></span>
- <span data-ttu-id="8cc5e-2940">Storage</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2940">Storage</span></span>

<span data-ttu-id="8cc5e-2941">これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。問題は、Microsoft サポートで直接開くことも、[GitHub の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2941">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="8cc5e-2942">これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2942">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="8cc5e-2943">CLI のバージョンを確認するには、`az --version` を使用します。出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2943">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="8cc5e-2944">コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2944">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="8cc5e-2945">CLI のナイトリー プレビュー ビルドもあります。詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2945">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="8cc5e-2946">ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2946">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="8cc5e-2947">[github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2947">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="8cc5e-2948">製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2948">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="8cc5e-2949">`az feedback` コマンドを使用してコマンド ラインからフィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="8cc5e-2949">Provide feedback from the command line with the `az feedback` command</span></span>

