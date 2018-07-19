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
ms.openlocfilehash: e614f0d108cef0702525e033d166e0498a94729f
ms.sourcegitcommit: fb3fed8701aff6c46af856e8fdc3e56ff9a678bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38228977"
---
# <a name="install-azure-cli-20-on-windows"></a>Windows での Azure CLI 2.0 のインストール

Windows では、MSI を使用して Azure CLI バイナリがインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。
Windows Subsystem for Linux (WSL) を実行している場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。 サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。

## <a name="install-or-update"></a>インストールまたは更新

再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。

> [!div class="nextstepaction"]
> [MSI インストーラーのダウンロード](https://aka.ms/installazurecliwindows)

インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。

これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。 PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。

> [!div class="nextstepaction"]
> [MSI インストーラーのダウンロード](https://aka.ms/installazurecliwindows)
