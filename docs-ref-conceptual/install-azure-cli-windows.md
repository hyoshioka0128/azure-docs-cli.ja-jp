---
title: Windows での Azure CLI のインストール
description: Windows で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/01/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: c5c499800e49dcdc536337e7655ec1ee280d48f2
ms.sourcegitcommit: 65bf8561a6e047e4eab52186e066a2e8c21f1d40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "65240547"
---
# <a name="install-azure-cli-on-windows"></a>Windows での Azure CLI のインストール

Windows では、MSI を使用して Azure CLI がインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。
Windows Subsystem for Linux (WSL) 用にインストールする場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。 サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。

[!INCLUDE [current-version](includes/current-version.md)]

## <a name="install-or-update"></a>インストールまたは更新

再頒布可能 MSI は、Windows での Azure CLI のインストールまたは更新に使用されます。 MSI インストーラーの使用前に現在のバージョンをアンインストールする必要はありません。

> [!div class="nextstepaction"]
> [MSI インストーラーのダウンロード](https://aka.ms/installazurecliwindows)

インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。

これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。 PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

Windows の "アプリと機能" の一覧から Azure CLI をアンインストールします。 アンインストールするには、次のようにします。

| プラットフォーム | Instructions |
|---|---|
| Windows 10 | [スタート] > [設定] > [アプリ] |
| Windows 8<br/>Windows 7 | [スタート] > [コントロール パネル] > [プログラム] > [プログラムのアンインストール] |

この画面に移動したら、プログラムの検索バーに "__Azure CLI__" と入力します。 アンインストールするプログラムが "__Microsoft CLI 2.0 for Azure__" として一覧に表示されます。 このアプリケーションを選択し、`Uninstall` ボタンをクリックします。

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
