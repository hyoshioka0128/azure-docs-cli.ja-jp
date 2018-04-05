---
title: Azure CLI 2.0 の拡張機能
description: Azure CLI 2.0 での拡張機能の使用
keywords: Azure CLI, 拡張機能
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5695d1df42689b315dd9d8783232ce35205a0a0e
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a>Azure CLI 2.0 での拡張機能の使用

拡張機能は、Azure CLI 自体に付属していない独立したモジュールです。この拡張機能により、新しいコマンドで機能が追加されます。 これは試験段階またはリリース前のサービス、Microsoft の特別なツール、またはご自身で作成したカスタム機能である可能性があります。 拡張機能により、ご自身のニーズに合わせてある程度柔軟に CLI を変更できます。コア機能セットの一部として見なされない多数の追加パッケージを出荷する必要はありません。

この記事は、CLI 用の拡張機能をインストール、更新、および削除する方法を理解するうえで役立ちます。 また、拡張機能の動作に関する一般的な質問にも回答します。

## <a name="find-extensions"></a>拡張機能の検索

使用できる拡張機能を確認するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を使用できます。 このコマンドにより、Microsoft によって提供および管理されている公式の拡張機能が一覧表示されます。

```azurecli
az extension list-available --output table
```

Microsoft では、ドキュメント サイトで [Microsoft 拡張機能の一覧](azure-cli-extensions-list.md)もホストしています。

## <a name="install-extensions"></a>拡張機能のインストール

インストールする拡張機能を見つけたら、[az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-add) を使用して取得します。 その拡張機能が `az extension list-available` に表示される場合は、名前によってインストールすることができます。

```azurecli
az extension add --name <extension-name>
```

拡張機能のソースが外部リソースであるか、その拡張機能への直接リンクがある場合は、ソース URL またはローカル パスを指定できます。 これは、コンパイルされた Python の wheel 形式ファイルである "_必要があります_"。

```azurecli
az extension add --source <URL-or-path>
```

インストールされた拡張機能は、`$AZURE_EXTENSION_DIR` シェル変数の値で確認できます。 この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。

## <a name="update-extensions"></a>拡張機能の更新

拡張機能を名前でインストールした場合、[az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-update) を使用してその拡張機能を更新できます。

```azurecli
az extension update --name <extension-name>
```

それ以外の場合は、「[拡張機能のインストール](#install-extensions)」の説明に従って、ソースから拡張機能を更新できます。

CLI を使用して拡張機能の名前を解決できない場合は、アンインストールしてから再インストールを試みてください。 拡張機能がプレビューから移行し、CLI の組み込みコマンドになった可能性もあります。 「[Azure CLI 2.0 のインストール](install-azure-cli.md)」の説明に従って CLI の更新を試み、拡張機能のコマンドが追加されているかどうかを確認してください。 

## <a name="uninstall-extensions"></a>拡張機能のアンインストール

不要になった拡張機能は、[az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-remove) を使用して削除できます。

```azurecli
az extension remove --name <extension-name>
```

また、手動で削除することもできます。それには、インストールした場所から拡張機能を削除します。 これは、`$AZURE_EXTENSION_DIR` シェル変数の値になります。 この変数が設定されていない場合、既定では、この値は `$HOME/.azure/cliextensions` (Linux と macOS の場合) または `%USERPROFILE%\.azure\cliextensions` (Windows の場合) になります。

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

`az extension remove` を使用してアンインストールすることをお勧めします。

## <a name="faq"></a>FAQ

ここでは、CLI 拡張機能に関するその他の一般的な質問に回答します。

### <a name="what-file-formats-are-allowed-for-installation"></a>インストールでは、どのファイル形式が許可されていますか。

現時点では、Python のコンパイルされた wheel 形式のみを拡張機能としてインストールできます。

### <a name="can-extensions-replace-existing-commands"></a>拡張機能で既存のコマンドを置き換えることはできますか。

はい。 拡張機能で既存のコマンドを置き換えることはできますが、置き換えられたコマンドを実行する前に、CLI によって警告が発せられます。

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a>拡張機能がプレリリースかどうかをどのように確認できますか。

拡張機能がプレリリースかどうかは、それ自体のドキュメントとバージョン管理に示されています。 また、Microsoft では、通常、CLI のプレビュー コマンドを拡張機能としてリリースし、製品がプレビュー段階を脱した時点で、その拡張機能をメインの CLI インターフェイスに移行させる予定です。

### <a name="can-extensions-depend-upon-each-other"></a>拡張機能は相互に依存できますか。

いいえ。 拡張機能は、相互に依存しない独立したパッケージである必要があります。 これは、CLI では拡張機能が読み込まれるタイミングが不明であるため、依存関係が満たされる保証がないからです。 拡張機能をインストールした場合、その拡張機能のみがインストールされます。また、他の拡張機能を削除しても、その拡張機能は動作し続けます。

### <a name="are-extensions-updated-along-with-the-cli"></a>拡張機能は CLI と共に更新されますか。

いいえ。 「[拡張機能の更新](#update-extensions)」で説明したように、拡張機能は個別に更新する必要があります。
