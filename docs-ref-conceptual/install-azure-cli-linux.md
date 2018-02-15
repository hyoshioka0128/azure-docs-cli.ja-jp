---
title: "Linux での Azure CLI 2.0 の手動インストール"
description: "Linux で Azure CLI 2.0 を手動インストールする方法"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 4ab1f70308810e045b9a1d923fd809ad9848f6c6
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a>Linux での Azure CLI 2.0 の手動インストール

お使いのディストリビューションで使用できる Azure CLI 用パッケージがない場合は、インストール スクリプトを実行して、いつでも手動で CLI をインストールできます。

> [!NOTE]
> CLI 用パッケージ マネージャーを使用することを強くお勧めします。 パッケージ マネージャーを使用すると、常に最新の更新プログラムを取得できるので、CLI コンポーネントの安定性が保証されます。 手動でインストールする前に、お使いのディストリビューション用のパッケージがあるかどうかを確認してください。

## <a name="prerequisites"></a>前提条件

CLI をインストールするには、システムで次のソフトウェアを使用できる必要があります。

* [Python 2.7 または Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update"></a>インストールまたは更新

CLI をインストールするか更新するかに関わらず、完全インストールを実行する必要があります。 前提条件を準備できたら、`curl` を実行して CLI をインストールできます。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

代わりに、スクリプトをダウンロードしてローカルで実行することもできます。 変更を有効にするために、シェルの再起動が必要になる場合があります。 インストール後、`az` コマンドを使用して CLI を実行します。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、手動インストール中に発生する一般的な問題をいくつか示します。 問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。
### <a name="curl-object-moved-error"></a>curl の "Object Moved" エラー

`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>`az` コマンドが見つからない

インストール後に、`bash` または `zsh` でコマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアします。 実行

```bash
hash -r
```

問題が解決されているかどうかを確認します。

インストール後にシェルを再起動しなかった場合にも、この問題が発生することがあります。 `az` コマンドの場所が `$PATH` にあることを確認してください。 `az` コマンドの場所は次のとおりです。

```bash
<install path>/bin
```

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

CLI をアンインストールするには、インストール時に選択した場所からファイルを直接削除します。 既定のインストール場所は `$HOME` です。

1. インストールされている CLI ファイルを削除します。

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```
2. `$HOME/.bash_profile` ファイルを変更して、次の行を削除します。

  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. `bash` または `zsh` を使用している場合は、シェルのコマンド キャッシュを再読み込みします。

  ```bash
  hash -r
  ```
