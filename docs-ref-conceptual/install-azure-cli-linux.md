---
title: "Linux での Azure CLI 2.0 の手動インストール"
description: "Linux で Azure CLI 2.0 を手動インストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure linux, azure インストール linux"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf1405cae70762146f63bc6629edc0dd1d949fff
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a>Linux での Azure CLI 2.0 の手動インストール

ディストリビューションで使用できる Azure CLI 用パッケージがない場合は、インストール スクリプトを実行して、いつでも手動で CLI をインストールできます。 使用できるパッケージがある場合は、それを使用してインストールすることをお勧めします。

## <a name="prerequisites"></a>前提条件

CLI をインストールするには、システムで次のソフトウェアを使用できる必要があります。

* [Python 2.7 または Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a>手動でのインストールまたは更新

CLI をインストールするか更新するかにかかわらず、完全インストールを実行する必要があります。 前提条件を準備できたら、`curl` を実行して CLI をインストールできます。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

必要がある場合、または `curl` がシステムにない場合は、代わりにスクリプトをダウンロードして、ローカルで実行できます。 変更を有効にするために、シェルの再起動が必要になる場合があります。 インストール後、`az` コマンドを使用して CLI を実行します。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="curl-object-moved-error"></a>curl の "Object Moved" エラー

`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>`az` コマンドが見つからない

インストール後に、コマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアしなければならない可能性があります。 実行

```bash
hash -r
```

問題が解決されているかどうかを確認してください。

これは、インストール後、シェルを再起動していない場合にも発生することがあります。 `az` コマンドの場所が `$PATH` にあることを確認してください。

インストール スクリプトを実行した場合、これは次のようになります。

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a>手動でのアンインストール

Azure CLI が不要であると判断した場合は、アンインストールすることができます。 アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。 Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。 また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。

CLI をアンインストールするには、インストール場所からファイルを直接削除します。 `https://aka.ms/InstallAzureCLI` スクリプト経由でインストールした場合、インストール時に選択した場所にインストールされています。 既定のインストール場所は `$HOME` です。

最初に、インストールされた CLI ファイルを削除します。

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

次に、`$HOME/.bash_profile` ファイルを変更して、行を削除します。

```
<install location>/lib/azure-cli/az.completion
```

最後に、シェルのコマンド キャッシュを再度読み込みます (使用している場合)。 `bash` および `zsh` ユーザーは、次の手順を実行する必要があります。

```bash
hash -r
```
