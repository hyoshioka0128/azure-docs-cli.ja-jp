---
title: macOS での Azure CLI のインストール
description: macOS で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/05/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 61be6c31e7251c8b374bf09072a9ecba9b914342
ms.sourcegitcommit: 1987a39809f9865034b27130e56f30b2bd1eb72c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "56422053"
---
# <a name="install-azure-cli-on-macos"></a>macOS での Azure CLI のインストール

macOS プラットフォームの場合は、[Homebrew パッケージ マネージャー](https://brew.sh)で Azure CLI をインストールできます。 Homebrew を使用すると、CLI のインストールを最新の状態に保つことが容易になります。 CLI パッケージは、macOS バージョン 10.9 以降でテストされています。

[!INCLUDE [current-version](includes/current-version.md)]

## <a name="install"></a>Install

CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。 これには、便利なインストール、更新、およびアンインストール手段が用意されています。
システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。

CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。

```bash
brew update && brew install azure-cli
```

> [!IMPORTANT]
>
> Azure CLI は Homebrew 内の `python3` パッケージに依存しているため、Python 2 が使用できる場合でも、お使いのシステムにインストールされます。 Azure CLI は、Homebrew で公開される `python3` の最新バージョンと互換性があることが保証されています。

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

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

## <a name="other-installation-methods"></a>その他のインストール方法

Homebrew を使用して環境に Azure CLI をインストールできない場合は、Linux の手動手順を使用できます。 正式には、このプロセスは macOS との互換性が維持されていないことに注意してください。 Homebrew などのパッケージ マネージャーを使用することを常にお勧めします。 他の選択肢を利用できない場合のみ、手動によるインストール方法を使用します。

手動インストールの手順については、「[Linux での Azure CLI の手動インストール](install-azure-cli-linux.md)」参照してください。

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
