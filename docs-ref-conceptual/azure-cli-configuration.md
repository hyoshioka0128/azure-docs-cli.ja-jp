---
title: Azure CLI 構成オプション
description: Azure CLI 2.0 を構成する方法
keywords: Azure CLI, 構成, 設定, Azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: b0d26beac83a7ce3bba44d5e64d129a211c82836
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2018
ms.locfileid: "34305878"
---
# <a name="azure-cli-20-configuration"></a>Azure CLI 2.0 の構成

Azure CLI 2.0 を使用すると、ユーザー構成によってログ記録、データ収集などの内部設定を上書きして、一部の必須パラメーターに対して既定のオプションを指定できます。 CLI は、こういった値のいくつかを管理するための便利なコマンド `az configure` を提供します。他の値については、構成ファイルまたは環境変数で設定できます。

CLI で使用される構成値は、次の優先順位で上から順番に評価されます。

1. コマンドライン パラメーター
2. 環境変数
3. 構成ファイルの値または `az configure` で設定された値

## <a name="cli-configuration-with-az-configure"></a>az configure での CLI 構成

CLI の既定値を [az configure](/cli/azure/reference-index#az-configure) コマンドで設定します。
このコマンドは 1 つの引数 `--defaults` を取ります。この引数は、スペースで区切られた `key=value` ペアのリストです。 指定した値は、必須の引数の代わりに、CLI によって使用されます。

使用できるキーの一覧を次に示します。

| Name | [説明] |
|------|-------------|
| group | すべてのコマンドに使用する既定のリソース グループ。 |
| location | すべてのコマンドに使用する既定の場所。 |
| web | `az webapp` コマンドに使用する既定のアプリ名。 |
| vm | `az vm` コマンドに使用する既定の VM 名。 |
| vmss | `az vmss` コマンドに使用する既定の VMSS 名。 |
| acr | `az acr` コマンドに使用する既定のコンテナー レジストリ名。 |
| acs | `az acs` コマンドに使用する既定のコンテナー サービス名。 |

例として、すべてのコマンドの既定のリソース グループと場所を設定する方法を次に示します。

```azurecli-interactive
az configure --defaults location=westus2 group=MyResourceGroup
```

## <a name="cli-configuration-file"></a>CLI 構成ファイル

CLI 構成ファイルには、CLI の動作の管理に使用されるその他の設定が含まれています。 構成ファイル自体は `$AZURE_CONFIG_DIR/config` にあります。 `AZURE_CONFIG_DIR` の既定値は、Linux と macOS の場合は `$HOME/.azure`、Windows の場合は `%USERPROFILE%\.azure` です。

構成ファイルは、INI ファイル形式で記述されます。 こうしたファイルは、`[section-name]` ヘッダーで始まり、その後に `key=value` エントリのリストが続くセクションで構成されます。 セクション名は大文字と小文字が区別され、キー名は区別されません。
`#` または `;` で始まる行はすべてコメントです。 インライン コメントは許可されていません。 ブール値は、大文字と小文字が区別されず、次の値によって表されます。

* __True__: 1、yes、true、on
* __False__: 0、no、false、off

次の例は、確認のプロンプトを無効にして、`/var/log/azure` ディレクトリへのログ記録を設定する CLI 構成ファイルです。

```ini
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

使用できる構成値とその意味の詳細については、次のセクションを参照してください。 INI ファイル形式の詳細については、[INI に関する Python のドキュメント](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure)を参照してください。

## <a name="cli-configuration-values-and-environment-variables"></a>CLI 構成値と環境変数

次の表は、構成ファイルで指定できるすべてのセクションとオプションの名前を示しています。 対応する環境変数は、`AZURE_{section}_{name}` としてすべて大文字で設定できます。 たとえば、`batchai` セクションの `storage_account` の既定値は、`AZURE_BATCHAI_STORAGE_ACCOUNT` 変数で設定します。

既定値を使用できる値は、必須の場合でも、コマンド ライン引数に存在する必要はありません。

| セクション | Name      | type | [説明]|
|---------|-----------|------|------------|
| __core__ | output | 文字列 | 既定の出力形式。 `json`、`jsonc`、`tsv`、`table` のいずれかを指定できます。 |
| | disable\_confirm\_prompt | ブール値 | 確認のプロンプトをオン/オフにします。 |
| | collect\_telemetry | ブール値 | Microsoft による、CLI の使用に関する匿名データの収集を許可します。 プライバシー情報については、[Azure CLI 2.0 の使用条件](http://aka.ms/AzureCliLegal)を参照してください。 |
| __logging__ | enable\_log\_file | ブール値 | ログ記録をオン/オフにします。 |
| | log\_dir | 文字列 | ログを書き込むディレクトリ。 既定では `${AZURE_CONFIG_DIR}/logs` です。 |
| __storage__ | connection\_string | 文字列 | `az storage` コマンドに使用する既定の接続文字列。 |
| | アカウント | 文字列 | `az storage` コマンドに使用する既定のアカウント名。 |
| | key | 文字列 | `az storage` コマンドに使用する既定のアカウント キー。 |
| | sas\_token | 文字列 | `az storage` コマンドに使用する既定の SAS トークン。 |
| __batchai__ | storage\_account | 文字列 | `az batchai` コマンドに使用する既定のストレージ アカウント。 |
| | storage\_key | 文字列 | `az batchai` コマンドに使用する既定のストレージ キー。 |
| __batch__ | アカウント | 文字列 | `az batch` コマンドに使用する既定の Azure Batch アカウント名。 |
| | access\_key | 文字列 | `az batch` コマンドに使用する既定のアクセス キー。 `aad` 承認でのみ使用されます。 |
| | endpoint | 文字列 | `az batch` コマンドに対する既定の接続先エンドポイント。 |
| | auth\_mode | 文字列 | `az batch` コマンドに使用する承認モード。 `shared_key` または `aad` を指定できます。 |

> [!NOTE]
> 構成ファイルに他の値が含まれる場合もありますが、その値は、`az configure` などの CLI コマンドで直接管理されます。 上記の表は、自身で変更する必要がある値のみを示しています。