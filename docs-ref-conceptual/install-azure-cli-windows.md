---
title: Windows での Azure CLI のインストール
description: Windows で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: c3ed3585b601ee55b267ea6cfc43ce41c54f084a
ms.sourcegitcommit: 15d6dfaee2075d0abceb2aa2423f0b6ef7b2ac9b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2018
---
# <a name="install-azure-cli-20-on-windows"></a>Windows での Azure CLI 2.0 のインストール

Windows では、MSI を使用して Azure CLI バイナリがインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。
Windows Subsystem for Linux (WSL) を実行している場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。 サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。

## <a name="install-or-update"></a>インストールまたは更新

再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。

> [!div class="nextstepaction"]
> [MSI インストーラーのダウンロード](https://aka.ms/installazurecliwindows)

インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。

これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。 PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。 ログインするには、`az login` コマンドを実行します。

```azurecli
az login
```

さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。

> [!div class="nextstepaction"]
> [MSI インストーラーのダウンロード](https://aka.ms/installazurecliwindows)
