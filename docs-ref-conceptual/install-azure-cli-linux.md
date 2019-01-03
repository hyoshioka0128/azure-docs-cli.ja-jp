---
title: Linux での Azure CLI の手動インストール
description: Linux で Azure CLI を手動インストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: b57ddd04d41b09eb145349179e3be48d3fdd5907
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593678"
---
# <a name="install-azure-cli-on-linux-manually"></a>Linux での Azure CLI の手動インストール

お使いのディストリビューションに対応した Azure CLI 用パッケージがない場合は、手動でスクリプトを実行して CLI をインストールします。

> [!NOTE]
> パッケージ マネージャーを使用して CLI をインストールすることを強くお勧めします。 パッケージ マネージャーを使用すると、常に最新の更新プログラムを取得できるので、CLI コンポーネントの安定性が保証されます。 手動でインストールする前に、お使いのディストリビューション用のパッケージがあるかどうかを確認してください。

## <a name="prerequisites"></a>前提条件

CLI には、次のソフトウェアが必要です。

* [Python 2.7 または Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update"></a>インストールまたは更新

CLI をインストールおよび更新するには、いずれの場合もインストール スクリプトを再実行する必要があります。 `curl` を実行して CLI をインストールします。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

スクリプトをダウンロードして、ローカルで実行することもできます。 変更を有効にするために、シェルの再起動が必要になる場合があります。

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、手動インストール中に発生する一般的な問題をいくつか示します。 ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="curl-object-moved-error"></a>curl の "Object Moved" エラー

`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>`az` コマンドが見つからない

インストール後に、`bash` または `zsh` でコマンドを実行できない場合は、シェルのコマンド ハッシュのキャッシュをクリアします。 ラン

```bash
hash -r
```

問題が解決されているかどうかを確認します。

インストール後にシェルを再起動しなかった場合にも、この問題が発生することがあります。 `az` コマンドの場所が `$PATH` にあることを確認してください。 `az` コマンドの場所は次のとおりです。

```bash
<install path>/bin
```

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

CLI をアンインストールするには、インストール時に選択した場所からファイルを直接削除します。 既定のインストール場所は `$HOME` です。

1. インストールされている CLI ファイルを削除します。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. `$HOME/.bash_profile` ファイルを変更して、次の行を削除します。

   ```text
   <install location>/lib/azure-cli/az.completion
   ```

3. `bash` または `zsh` を使用している場合は、シェルのコマンド キャッシュを再読み込みします。

   ```bash
   hash -r
   ```

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
