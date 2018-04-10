---
title: Azure CLI 2.0 のエイリアス拡張機能
description: Azure CLI 2.0 のエイリアス拡張機能を使用する方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/14/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e457d78b1009fe573554df36db18f525516e0b4a
ms.sourcegitcommit: 335c11e6c34f7907e61a43507745ba84ed4e7469
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/05/2018
---
# <a name="the-azure-cli-20-alias-extension"></a>Azure CLI 2.0 のエイリアス拡張機能

エイリアス拡張機能を使用すると、既存のコマンドを使用して、Azure CLI のカスタム コマンドを定義することができます。 エイリアスを使用すると、ショートカットが許可され、位置引数を使用する機能が提供されるため、ワークフローを簡潔でシンプルに保つことができます。 エイリアスには Jinja2 テンプレート エンジンが使用されているため、高度な引数の処理にも対応できます。

> [!NOTE]
> エイリアス拡張機能はパブリック プレビュー段階にあります。 機能と構成ファイルの形式は変更される可能性があります。

## <a name="install-the-alias-extension"></a>エイリアス拡張機能のインストール

エイリアス拡張機能を使用するために最低限必要な Azure CLI バージョンは **2.0.28** です。 CLI のバージョンを確認するには、`az --version` を実行してください。 インストールを更新する必要がある場合は、「[Azure CLI 2.0 のインストール](./install-azure-cli.md)」の説明に従ってください。

[az extension add](/cli/azure/extension#az-extension-add) コマンドを使用して拡張機能をインストールします。

```azurecli
az extension add --name alias
```

[az extension list](/cli/azure/extension#az-extension-list) を使用して拡張機能のインストールを確認します。 エイリアス拡張機能が正しくインストールされていれば、コマンドの出力に表示されます。

```azurecli
az extension list --output table
```

```output
ExtensionType    Name                       Version
---------------  -------------------------  ---------
whl              alias                      0.2.0
```

## <a name="keep-the-extension-up-to-date"></a>拡張機能を最新の状態に保つ

エイリアス拡張機能は活発に開発が行われており、新しいバージョンが定期的にリリースされます。 CLI を更新したときに、新しいバージョンが自動的にインストールされるわけではありません。 [az extension update](/cli/azure/extension#az-extension-update) を使用して拡張機能の更新プログラムをインストールします。

```azurecli
az extension update --name alias
```

## <a name="alias-commands-file-format"></a>エイリアス コマンド ファイルの形式

エイリアス コマンド定義は、`$AZURE_USER_CONFIG/alias` にある構成ファイルに書き込まれます。 `AZURE_USER_CONFIG` の既定値は、macOS と Linux の場合は `$HOME/.azure`、Windows の場合は `%USERPROFILE%\.azure` です。 エイリアス構成ファイルは、INI 構成ファイル形式で記述されます。 エイリアス コマンドの一般的な形式は次のとおりです。

```
[command_name]
command = invoked_commands
```

コマンドの一部として `az` を含めないでください。

## <a name="create-simple-alias-commands"></a>単純なエイリアス コマンドを作成する

エイリアスの用途の 1 つは、既存のコマンド グループやコマンド名の短縮です。 たとえば、`group` コマンド グループを `rg` に、`list` コマンドを `ls` に短縮できます。

```
[rg]
command = group

[ls]
command = list
```

新しく定義したこれらのエイリアスは、定義が存在する任意の場所で使用できるようになります。

```azurecli
az rg list
az rg ls
az vm ls
```

エイリアスは、完全なコマンドのショートカットにすることもできます。 次の例では、使用可能なリソース グループとその位置がテーブル出力で表示されています。

```
[ls-groups]
command = group list --query '[].{Name:name, Location:location}' --output table
```

これで `ls-groups` を他の CLI コマンドのように実行できます。

```azurecli
az ls-groups
```

## <a name="create-an-alias-command-with-arguments"></a>引数付きのエイリアス コマンドを作成する

エイリアス名に `{{ arg_name }}` として含めることで、位置引数をエイリアス コマンドに追加することもできます。 中かっこ内には空白が必要です。

```
[alias_name {{ arg1 }} {{ arg2 }} ...]
command = invoke_including_args
```

次の例のエイリアスは、位置引数を使用して VM のパブリック IP アドレスを取得する方法を示しています。

```
[get-vm-ip {{ resourceGroup }} {{ vmName }}]
command = vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }} --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress
```

このコマンドを実行するときに、位置引数に値を指定します。

```azurecli
az get-vm-ip MyResourceGroup MyVM
```

エイリアスによって呼び出したコマンドで環境変数を使用することもできます。この環境変数は実行時に評価されます。 次の例では、`create-rg` エイリアスを追加します。これにより、`eastus` 内にリソース グループが作成され、`owner` タグが追加されます。 このタグには、ローカル環境変数 `USER` の値が割り当てられます。

```
[create-rg {{ groupName }}]
command = group create --name {{ groupName }} --location eastus --tags owner=$USER
```

## <a name="process-arguments-using-jinja2-templates"></a>Jinja2 テンプレートを使用した引数の処理

エイリアス拡張機能での引数の置換は、[Jinja2](http://jinja.pocoo.org/docs/2.10/) によって実行されるため、ユーザーは Jinja2 テンプレート エンジンの機能にフル アクセスできるようになります。 テンプレートを使用すると、文字列上のデータの抽出や置換などのアクションを実行できます。

Jinja2 テンプレートにより、基になるコマンドとは異なるさまざまな種類の引数を受け入れるエイリアスを作成できます。 たとえば、ストレージ URL を受け入れるエイリアスを作成できます。 この URL が解析され、アカウント名とコンテナー名がストレージ コマンドに渡されます。

```
[storage-ls {{ url }}]
command = storage blob list --account-name {{ url.replace('https://', '').split('.')[0] }} --container-name {{ url.replace('https://', '').split('/')[1] }}
```

Jinja2 テンプレート エンジンについては、[Jinja2 のドキュメント](http://jinja.pocoo.org/docs/2.10/templates/)を参照してください。

## <a name="uninstall-the-alias-extension"></a>エイリアス拡張機能のアンインストール

拡張機能をアンインストールするには、[az extension remove](/cli/azure/extension#az-extension-remove) コマンドを使用します。

```azurecli
az extension remove --name alias
```

拡張機能に関するバグなどの問題が原因でアンインストールした場合は、Microsoft が修正プログラムを提供できるように、[GitHub に問題を提出](https://github.com/Azure/azure-cli-extensions/issues)してください。
