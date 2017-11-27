---
title: "apt での Azure CLI 2.0 のインストール"
description: "apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure apt, azure debian, azure ubuntu"
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
ms.openlocfilehash: 93d947d91973def1c05e2f5b2e7511bc1c5704a2
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-apt"></a>apt での Azure CLI 2.0 のインストール

Ubuntu、Debian など、`apt` に付属するディストリビューションを実行している場合は、システムにインストールできる Azure CLI 用の利用可能なパッケージがあります。

> [!NOTE]
> CLI を使用するには、Python 2.7.x または Python 3.x が必要です。 ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。

## <a name="install"></a>インストール

1. ソース リストを変更します。
 
   - 32 ビット システム

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64 ビット システム

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. 次の sudo コマンドを実行します。

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

Azure CLI は `az` コマンドで実行できます。

## <a name="update"></a>更新

CLI パッケージを更新するには、`apt-get upgrade` を使用します。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> これにより、依存関係が変更されていない、システム上のすべてのインストール済みパッケージがアップグレードされます。
> CLI のみをアップグレードするには、`apt-get install` を使用します。
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a>アンインストール

Azure CLI が不要であると判断した場合は、アンインストールすることができます。 アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。 Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。 また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。

1. `apt-get remove` を使用してアンインストールします。

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. 不要なパッケージを削除します。

   ```bash
   sudo apt autoremove
   ```
