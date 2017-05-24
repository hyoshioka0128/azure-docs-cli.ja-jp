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
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 リリース ノート

## <a name="may-10-2017"></a>2017 年 5 月 10 日

バージョン 2.0.6

* documentdb から cosmosdb に名前が変更されました
* rdbms (mysql、postgres) が追加されました
* Data Lake Analytics モジュールと Data Lake Store モジュールが追加されました。
* Cognitive Services モジュールが追加されました。
* Service Fabric モジュールが追加されました。
* 対話型モジュールが追加されました (az-shell の名前変更)。
* CDN コマンドに対応するようになりました。
* コンテナー モジュールが削除されました。
* "az --version" のショートカットとして "az -v" が追加されました ([#2926](https://github.com/Azure/azure-cli/issues/2926))
* パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))

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

### <a name="core"></a>コア

* コア: 登録されていないプロバイダーによる例外がキャプチャされ、自動登録されます   
* パフォーマンス: プロセスが終了するまで ADAL トークン キャッシュがメモリに保持されます ([#2603](https://github.com/Azure/azure-cli/issues/2603))
* 16 進フィンガープリント -o tsv から返されるバイトが修正されました ([#3053](https://github.com/Azure/azure-cli/issues/3053))
* Key Vault 証明書ダウンロードの強化と AAD SP 統合 ([#3003](https://github.com/Azure/azure-cli/issues/3003))
* Python の場所が "az —version" に追加されました ([#2986](https://github.com/Azure/azure-cli/issues/2986))
* ログイン: サブスクリプションがないときのログインに対応するようになりました ([#2929](https://github.com/Azure/azure-cli/issues/2929))
* コア: サービス プリンシパルを 2 回使用してログインするときのエラーが修正されました ([#2800](https://github.com/Azure/azure-cli/issues/2800))
* コア: accessTokens.json のファイル パスを環境変数で構成できます ([#2605](https://github.com/Azure/azure-cli/issues/2605))
* コア: 構成済み既定値を省略可能な引数に適用できます ([#2703](https://github.com/Azure/azure-cli/issues/2703))
* コア: パフォーマンスの向上
* コア: カスタム CA 証明書 - REQUESTS_CA_BUNDLE 環境変数の設定を利用できます
* コア: クラウド構成 - "管理" エンドポイントが設定されていない場合に、"リソース マネージャー" エンドポイントが使用されます

### <a name="acs"></a>ACS

* マスター数とエージェント数が文字列から整数に修正されました
* 非同期作成用に "az acs create --no-wait" と "az acs wait" が公開されました
* ドライラン検証用に "az acs create --validate" が公開されました
* スケール コマンドの PUT 呼び出しの前の Windows プロファイルが削除されます ([#2755](https://github.com/Azure/azure-cli/issues/2755))

### <a name="appservice"></a>AppService

* 関数アプリ: 作成、表示、リスト、削除、ホスト名、SSL など、関数アプリに完全に対応するようになりました
* Team Services (VSTS) が継続的な配信オプションとして "appservice web source-control config" に追加されました
* "az webapp" が作成され "az app service web" が置き換えられています (下位互換性のために "az app service web" は 2 リリースだけ保持されます)
* WebApp 作成時にデプロイと "ランタイム スタック" を構成するための引数が公開されました
* "webapp list-runtimes" が公開されました
* 接続文字列の構成がサポートされています ([#2647](https://github.com/Azure/azure-cli/issues/2647))
* プレビューでのスロット スワップがサポートされています
* appservice コマンドからのポーランド語のエラー ([#2948](https://github.com/Azure/azure-cli/issues/2948))
* 証明書の操作に App Service プランのリソース グループが使用されます ([#2750](https://github.com/Azure/azure-cli/issues/2750))

### <a name="cosmosdb"></a>CosmosDB

* documentdb モジュールから cosmosdb に名前が変更されました。
* DocumentDB データプレーン API: データベースとコレクション管理に対応するようになりました
* データベース アカウントにおける自動フェールオーバーの有効化に対応するようになりました
* 新しい一貫性ポリシー ConsistentPrefix に対応するようになりました

### <a name="data-lake-analytics"></a>Data Lake Analytics

* ジョブ リストの結果と状態に対するフィルター処理でエラーがスローされるバグが修正されました。
* 新しいカタログ項目の種類: パッケージに対応するようになりました。 `az dla catalog package` を介してアクセスされます
* 次のカタログ項目の一覧をデータベース内から表示できます (スキーマ仕様は不要です)。

  * テーブル
  * テーブル値関数
  * 表示
  * テーブルの統計。 スキーマと一緒に表示することもできますが、テーブル名を指定する必要はありません。

### <a name="data-lake-store"></a>Data Lake Store

* 基になるファイルシステム SDK のバージョンが更新され、サーバー側スロットル処理への対応が強化されました。
* パッケージ読み込みとコマンド実行のパフォーマンスが向上しています ([#2819](https://github.com/Azure/azure-cli/issues/2819))
* access show のヘルプがなかったため、 追加しました  ([#2743](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>検索

* 検索結果を改善し、検索インデックスのバージョン管理を可能にしました

### <a name="keyvault"></a>KeyVault

* BC: `az keyvault certificate download` によって -e が文字列またはバイナリから PEM または DER に変更され、オプションの表現が向上しました
* BC: --expires パラメーターと --not-before パラメーターはサービスでサポートされていないため、`keyvault certificate create` から削除されました。
* --validity パラメーターが `keyvault certificate create` に追加され、--policy の値が選択的に上書きされます
* "expires" と "not_before" が公開され、"validity_in_months" が公開されなかった場合に `keyvault certificate get-default-policy` で発生する問題が修正されました。
* KeyVault における pem と pfx のインポートが修正されました ([#2754](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>ラボ

* ラボ環境用の作成、表示、削除、およびリスト コマンドが追加されました。
* ラボで ARM テンプレートを表示するための表示およびリスト コマンドが追加されました。
* ラボ環境で VM をフィルター処理するための --environment フラグが `az lab vm list` に追加されました。
* ラボの数式内でアーティファクト スキャフォールディングをエクスポートするための便利なコマンド `az lab formula export-artifacts` が追加されました。
* ラボ内でシークレットを管理するためのコマンドが追加されました。

### <a name="monitor"></a>監視

* バグの修正: JSON 文字列を使用するため `az alert-rules create` の `--actions` がモデル化されています ([#3009](https://github.com/Azure/azure-cli/issues/3009))
* バグの修正: diagnostic settings create が、表示コマンドからのログ/メトリックを受け付けません ([#2913](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>ネットワーク

* `network watcher test-connectivity` コマンドが追加されました。
* `network watcher packet-capture create` の `--filters` パラメーターに対応するようになりました。
* Application Gateway 接続のドレインに対応するようになりました。
* Application Gateway WAF 規則セットの構成に対応するようになりました。
* ExpressRoute ルート フィルターとルールに対応するようになりました。
* TrafficManager の地理的なルーティングに対応するようになりました。
* VPN 接続ポリシー ベースのトラフィック セレクターに対応するようになりました。
* VPN 接続 IPSec ポリシーに対応するようになりました。
* `--no-wait` パラメーターまたは `--validate` パラメーターを使用するときの `vpn-connection create` のバグが修正されました。
* アクティブ/アクティブ VNet ゲートウェイに対応するようになりました
* `network vpn-connection list/show` コマンドの出力から null 値が削除されました。
* BC: `vpn-connection create` の出力のバグが修正されました 
* "vpn-connection create" の "--key-length" 引数が適切に解析されないバグが修正されました。
* `dns zone import` でレコードが適切にインポートされないバグが修正されました。
* `traffic-manager endpoint update` が動作しないバグを修正しました。
* "Network Watcher" プレビューのコマンドが追加されました。

### <a name="profile"></a>プロファイル

* サブスクリプションが見つからないときのログインに対応するようになりました ([#2560](https://github.com/Azure/azure-cli/issues/2560))
* az account set --subscription で短いパラメーター名に対応するようになりました ([#2980](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* Redis Cache のスケール機能も追加する更新コマンドが追加されました
* "update-settings" コマンドが廃止されました。

### <a name="resource"></a>リソース

* managedapp と managedapp の定義コマンドが追加されました ([#2985](https://github.com/Azure/azure-cli/issues/2985))
* "provider operation" コマンドに対応するようになりました ([#2908](https://github.com/Azure/azure-cli/issues/2908))
* 汎用リソースの作成に対応するようになりました ([#2606](https://github.com/Azure/azure-cli/issues/2606))
* リソース解析および API バージョンの検索が修正されました  ([#2781](https://github.com/Azure/azure-cli/issues/2781))
* az lock update のドキュメントが追加されました  ([#2702](https://github.com/Azure/azure-cli/issues/2702))
* 存在しないグループのリソースの一覧を表示しようとするとエラーが出力されます  ([#2769](https://github.com/Azure/azure-cli/issues/2769))
* [コンピューティング] VMSS と VM の可用性セットの更新に関する問題が修正されました。 ([#2773](https://github.com/Azure/azure-cli/issues/2773))
* parent-resource-path が None の場合のロックの作成と削除が修正されました ([#2742](https://github.com/Azure/azure-cli/issues/2742))

### <a name="role"></a>役割

* create-for-rbac: SP の終了日が、確実に証明書の有効期限の前に設定されます ([#2989](https://github.com/Azure/azure-cli/issues/2989))
* RBAC: "ad group" が完全にサポートされるようになりました ([#2016](https://github.com/Azure/azure-cli/issues/2016))
* ロール: ロール定義の更新に関する問題が修正されました ([#2745](https://github.com/Azure/azure-cli/issues/2745))
* create-for-rbac: ユーザーによって指定されたパスワードが確実に取得されます

### <a name="sql"></a>SQL

* az sql server list-usages コマンドと az sql db list-usages コマンドが追加されました。
* SQL - リソース プロバイダーに直接接続できます ([#2832](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>Storage

* `storage account create` のリソース グループの場所に対する既定の場所。
* 増分 BLOB コピーに対応するようになりました
* 大きなブロック BLOB アップロードに対応するようになりました
* アップロードするファイルが 200 GB を超える場合にブロック サイズが 100 MB に変更されます

### <a name="vm"></a>VM

* avail-set: UD&FD ドメイン数が省略可能になりました

  注: 独立したクラウドの VM コマンド。次の管理対象ディスク関連機能は避けるようにしてください。
  1. az disk/snapshot/image
  2. az vm/vmss disk
  3. "az vm/vmss create" 内では、"—use-unmanaged-disk" を使用して管理対象ディスクを回避します。他のコマンドは機能します
* vm/vmss: SSH キー ペアを生成するときの警告テキストが向上します
* vm/vmss: プラン情報を必要とするマーケットプレイス イメージからの作成をサポートします ([#1209](https://github.com/Azure/azure-cli/issues/1209))


## <a name="april-3-2017"></a>2017 年 4 月 3 日

バージョン 2.0.2

このリリースでは、ACR、Batch、KeyVault、SQL コンポーネントをリリースしました。

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

### <a name="core"></a>コア

* 既定の一覧に acr、lab、monitor、find モジュールを追加。
* ログイン: 誤ったテナントをスキップ ([#2634](https://github.com/Azure/azure-cli/pull/2634))
* ログイン: 既定のサブスクリプションを "Enabled" の状態のサブスクリプションに設定 ([#2575](https://github.com/Azure/azure-cli/pull/2575))
* wait コマンドと --no-wait のサポートをより多くのコマンドに追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* コア: 証明書を持つサービス プリンシパルを使用したログインをサポート ([#2457](https://github.com/Azure/azure-cli/pull/2457))
* 不足しているテンプレート パラメーターの指定を求めるメッセージを追加  ([#2364](https://github.com/Azure/azure-cli/pull/2364))
* 既定のリソース グループ、既定の Web、既定の VM など、一般的な引数の既定値の設定をサポート
* 特定のテナントへのログインをサポート
 
### <a name="acs"></a>ACS

* [ACS] 既定の ACS クラスターを構成するためのサポートを追加 ([#2554](https://github.com/Azure/azure-cli/pull/2554))
* ssh キー パスワードの入力要求のサポートを追加  ([#2044](https://github.com/Azure/azure-cli/pull/2044))
* Windows クラスターのためのサポートを追加  ([#2211](https://github.com/Azure/azure-cli/pull/2211))
* 所有者から共同作成者へのロールの切り替え  ([#2321](https://github.com/Azure/azure-cli/pull/2321))
 
### <a name="appservice"></a>AppService

* appservice: DNS A レコードで使用される外部 IP アドレスの取得をサポート ([#2627](https://github.com/Azure/azure-cli/pull/2627))
* appservice: ワイルドカード証明書のバインドをサポート ([#2625](https://github.com/Azure/azure-cli/pull/2625))
* appservice: 発行プロファイルの一覧表示をサポート ([#2504](https://github.com/Azure/azure-cli/pull/2504))
* AppService - 構成後にソース管理の同期をトリガー ([#2326](https://github.com/Azure/azure-cli/pull/2326))
 
### <a name="datalake"></a>DataLake

* Data Lake Analytics モジュールの最初のリリース。
* Data Lake Store モジュールの最初のリリース。
 
### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB: 接続文字列を一覧表示するためのサポートを追加 ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>VM

* [コンピューティング] 仮想マシン スケール セットを作成するための AppGateway サポートを追加 ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] ディスク キャッシュのサポートを改善しました ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS: ポータルで使用される資格情報検証ロジックを組み込む ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* wait コマンドと --no-wait のサポートを追加 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* 仮想マシン スケール セット: VM 間にわたるインスタンス ビューの一覧表示をサポート * ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* VM と仮想マシン スケール セット用の --secrets を追加 ([#2212](https://github.com/Azure/azure-cli/pull/2212))
* 特殊化した VHD による VM 作成を許可 ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>2017 年 2 月 27 日

バージョン 2.0.0

Azure CLI 2.0 のこのリリースは、最初の "一般公開" リリースです。
一般公開に該当するのは、以下のコマンド モジュールです。
- コンテナー サービス (acs)
- コンピューティング (Resource Manager、VM、仮想マシン スケール セット、Managed Disks など)
- ネットワーク
- Storage

これらのコマンド モジュールは、運用環境で使用することができ、標準の Microsoft SLA でサポートされています。
問題は、Microsoft サポートで直接開くことも、[github の問題一覧](https://github.com/azure/azure-cli/issues/)で開くこともできます。
[azure-cli タグを使用して StackOverflow](http://stackoverflow.com/questions/tagged/azure-cli) で質問したり、製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせたりすることもできます。
`az feedback` コマンドを使用すると、コマンド ラインからフィードバックを送ることができます。

これらのモジュールのコマンドは安定しており、Azure CLI のこのバージョンの今後のリリースで構文が変更されることは想定されていません。

CLI のバージョンを確認するには、`az --version` を使用します。
出力では、CLI 自体のバージョン (このリリースでは 2.0.0)、個々のコマンド モジュール、および使用している Python と GCC のバージョンが示されます。

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
> コマンド モジュールには、"b*n*" または "rc*n*" という接尾辞が付いているものがあります。
> これらのコマンド モジュールはまだプレビュー段階であり、今後一般公開される予定です。

CLI のナイトリー プレビュー ビルドもあります。
詳細については、[ナイトリー ビルドの入手](https://github.com/Azure/azure-cli#nightly-builds)に関する手順と、[開発者向けセットアップおよび共同作成コード](https://github.com/Azure/azure-cli#developer-setup)に関する手順を参照してください。

ナイトリー プレビュー ビルドの問題は、次の方法で報告することができます。
- [github の問題一覧](https://github.com/azure/azure-cli/issues/)で問題を報告する。
- 製品チーム ([azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)) に問い合わせる。
- `az feedback` コマンドを使用してコマンド ラインからフィードバックを送る。

