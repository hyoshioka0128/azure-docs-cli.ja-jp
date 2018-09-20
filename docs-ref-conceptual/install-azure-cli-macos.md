---
title: macOS での Azure CLI のインストール
description: macOS で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: fd829c6ff9162b660a889d3e08615a76f42aeb97
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388475"
---
# <a name="install-azure-cli-20-on-macos"></a>macOS での Azure CLI 2.0 のインストール

macOS プラットフォームの場合は、[Homebrew パッケージ マネージャー](https://brew.sh)で Azure CLI をインストールできます。 Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。 CLI パッケージは、macOS バージョン 10.9 以降でテストされています。

## <a name="install"></a>Install

CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。 これには、便利なインストール、更新、およびアンインストール手段が用意されています。
システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。

CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。

```bash
brew update && brew install azure-cli
```

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

Homebrew を使用した CLI のインストール時に問題が発生した場合、一般的なエラーを以下に示します。 ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="unable-to-find-python-or-installed-packages"></a>Python またはインストールされているパッケージが見つかりません

Homebrew のインストール中に、マイナー バージョンの不一致またはその他の問題が発生した可能性があります。 CLI では Python 仮想環境を使用しないため、インストールされている Python バージョンを見つけることができる必要があります。 考えられる修正案は、Homebrew から `python3` の依存関係をインストールして再リンクすることです。

```bash
brew update && brew install python3 && brew upgrade python3
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a>CLI バージョン 1.x がインストールされている

古いバージョンがインストールされている場合は、Homebrew の古いキャッシュが原因と考えられます。 [更新](#Update)の手順に従ってください。

## <a name="update"></a>アップデート

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
