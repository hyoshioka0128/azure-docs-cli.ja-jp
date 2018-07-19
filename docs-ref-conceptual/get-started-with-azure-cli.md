---
title: Azure CLI 2.0 を使ってみる
description: コマンドの基本を学習し、Azure CLI 2.0 を使い始めます。
keywords: Azure CLI, CLI ヘルプ, Azure ヘルプ, クエリ, 自動化,
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: f45c3acfdb4edb82cde755472d240ae18d82aba2
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967743"
---
# <a name="get-started-with-azure-cli-20"></a>Azure CLI 2.0 を使ってみる

Azure CLI 2.0 へようこそ。 CLI は、Azure サービスを迅速かつ効率的に使用するためのツールで、オートメーションに重点が置されています。 この記事では、CLI の機能と、生産性の向上に役立つリソースへのリンクを紹介します。

## <a name="install-and-sign-in"></a>インストールとサインイン

[CLI をインストール](install-azure-cli.md)するか、[Azure Cloud Shell](/azure/cloud-shell/overview) を試します (まだこの操作を行っていない場合)。

ローカル インストールで CLI コマンドを使用する前に、[az login](/cli/azure/reference-index#az-login) でサインインする必要があります。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

対話型以外のサインイン方法も用意されています。詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="common-commands"></a>一般的なコマンド

次の表は、CLI で使用される一般的なコマンドをいくつか示しており、それぞれが、リファレンス内の関連ドキュメント ページにリンクされています。
こうしたグループのすべてのサブコマンドおよびそのドキュメントは、オンライン リファレンスまたは `--help` 引数を使用して確認できます。

| リソースの種類 | Azure CLI コマンド グループ |
|---------------|-------------------------|
| [リソース グループ](/azure/azure-resource-manager/resource-group-overview) | [az group](/cli/azure/group) |
| [仮想マシン](/azure/virtual-machines) | [az vm](/cli/azure/vm) |
| [ストレージ アカウント](/azure/storage/common/storage-introduction) | [az storage account](/cli/azure/storage/account) |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [az keyvault](/cli/azure/keyvault) |
| [Web アプリケーション](/azure/app-service) | [az webapp](/cli/azure/webapp) |
| [SQL データベース](/azure/sql-database) | [az sql server](/cli/azure/sql/server) |
| [CosmosDB](/azure/cosmos-db) | [az cosmosdb](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a>コマンドを見つける

CLI のコマンドは、"_グループ_" の "_サブコマンド_" として提供されます。
各グループが、Azure によって提供されるサービスを表しており、サブグループによって、そのサービスのコマンドが論理グループに分かれています。

コマンドを検索するには、[az find](/cli/azure/reference-index#az-find) を使用します。 たとえば、`secret` を含むコマンド名を検索するには、次のコマンドを使用します。

```azurecli-interactive
az find -q secret
```

使用するコマンドのグループがわかっている場合は、`--help` 引数の方が適していることがあります。 これにより、コマンドの詳細情報が表示されます。また、コマンド グループで使用すると、利用可能なすべてのサブコマンドが表示されます。 たとえば、ネットワーク セキュリティ グループ (NSG) で使用すると、利用可能な NSG サブグループとコマンドを確認できます。

```azurecli-interactive
az network nsg --help
```

CLI では Bash シェルにコマンドの完全タブ補完が用意されています。

## <a name="globally-available-arguments"></a>グローバルに使用できる引数

引数の中には、すべてのコマンドで使用できるものがあります。

* `--help` は、コマンドとその引数に関する CLI 参照情報を出力し、利用可能なサブグループとコマンドの一覧を表示します。
* `--output` は出力形式を変更します。 使用可能な出力形式は `json`、`jsonc` (色付けされた JSON)、`tsv` (タブ区切り値)、および `table` (人間が判読できる ASCII テーブル) です。 既定では、CLI は `json` を出力します。 使用可能な出力形式の詳細については、[Azure CLI 2.0 の出力形式](format-output-azure-cli.md)に関するページをご覧ください。
* `--query` は、[JMESPath クエリ言語](http://jmespath.org/)を使用して、Azure サービスから返された出力をフィルター処理します。 クエリの詳細については、[Azure CLI 2.0 でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページ、および「[JMESPath tutorial (JMESPath チュートリアル)](http://jmespath.org/tutorial.html)」を参照してください。
* `--verbose` は、操作中に Azure で作成されたリソースに関する情報と、その他の有用な情報を出力します。
* `--debug` は、デバッグの目的で使用する、CLI 操作に関する詳細情報を出力します。 バグが発生した場合は、バグ レポートを送信するときに、`--debug` フラグをオンにして生成した出力を提供します。

## <a name="interactive-mode"></a>対話モード

CLI には対話モードが用意されています。このモードでは、ヘルプ情報が自動的に表示され、サブコマンドが選択しやすくなっています。 対話モードには [az interactive](/cli/azure/reference-index#az-interactive) コマンドで切り替えます。

```azurecli-interactive
az interactive
```

対話モードの詳細については、[Azure CLI 2.0 対話モード](interactive-azure-cli.md)に関する記事をご覧ください。

また、オートコンプリート、マウス オーバー ドキュメントなど、対話型エクスペリエンスを提供する [Visual Studio Code プラグイン](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)も用意されています。

## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a>クイックスタートとチュートリアルを利用して CLI の基本について学習する

Azure CLI 2.0 の使用を開始するには、詳細なチュートリアルをお試しください。チュートリアルでは、仮想マシンを設定し、CLI の機能を使用して Azure リソースにクエリを実行します。

> [!div class="nextstepaction"]
> [Azure CLI 2.0 での仮想マシンの作成チュートリアル](azure-cli-vm-tutorial.yml)

他のサービスに焦点を当てる必要がある場合、CLI を使用する Azure サービスについては、さまざまなクイックスタートがあります。

* [Azure CLI を使用したストレージ アカウントの作成](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [CLI を使用した Azure Blob Storage との間でのオブジェクトの転送](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [Azure CLI を使用した単一の Azure SQL データベースの作成](/azure/sql-database/sql-database-get-started-cli)
* [Azure CLI を使用した Azure Database for MySQL サーバーの作成](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [Azure CLI を使用した Azure Database for PostgreSQL の作成](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [Azure での Python Web アプリの作成](/azure/app-service/app-service-web-get-started-python)
* [Azure Web Apps for Containers でのカスタム Docker Hub イメージの実行](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a>フィードバックを送る

機能強化とバグ解決に活かすために、CLI に関する皆様のご意見をお待ちしております。 [GitHub で問題を報告](https://github.com/azure/azure-cli/issues)するか、CLI の組み込み機能を使用して、[az feedback](/cli/azure/reference-index#az-feedback) コマンドで一般的なフィードバックをお寄せください。

```azurecli-interactive
az feedback
```
