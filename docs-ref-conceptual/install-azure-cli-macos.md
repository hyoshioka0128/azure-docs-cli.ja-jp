---
title: "macOS での Azure CLI のインストール"
description: "macOS で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure macos, azure インストール macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 36fd2604677db0b7f820ee11884bf790fb1d75cb
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-macos"></a>macOS での Azure CLI 2.0 のインストール

macOS プラットフォームの場合、[Homebrew パッケージ マネージャー](http://brew.sh)を使用して Azure CLI をインストールできます。 Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。 CLI パッケージは、macOS バージョン 10.9 以降でテストされています。

## <a name="install"></a>[インストール]

CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。 これには、便利なインストール、更新、およびアンインストール手段が用意されています。 システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。

CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。

```bash
brew update && brew install azure-cli
```

その後、Azure CLI は `az` コマンドで実行できます。

## <a name="troubleshooting"></a>トラブルシューティング

Homebrew を使用した CLI のインストール時に問題が発生した場合、一般的なエラーを以下に示します。 問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="unable-to-find-python-or-installed-packages"></a>Python またはインストールされているパッケージが見つかりません

インストール時に Python またはインストールされているパッケージが見つからない場合、マイナー バージョンの不一致があるか、Homebrew のインストール中に別の問題が発生した可能性があります。 CLI では Python 仮想環境を使用しないため、適切な Python バージョンを見つけることができる必要があります。 Python インストールを再リンクすることで、これらの問題を解決できる場合があります。

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a>CLI バージョン 1.x がインストールされている

古いバージョンがインストールされている場合は、Homebrew の古いキャッシュが原因と考えられます。 [更新](#Update)の手順に従ってください。

## <a name="update"></a>プライマリの

CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。 新しいリリースは約 2 週間ごとに入手できます。 ローカル リポジトリ情報を更新してから、`azure-cli` パッケージをアップグレードします。

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

Homebrew を使用して、`azure-cli` パッケージをアンインストールします。

```bash
brew uninstall azure-cli
```
