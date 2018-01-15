---
title: "macOS での Azure CLI のインストール"
description: "macOS で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure macos, azure インストール macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e615d2b3ab3b1307e982cb1d4d456633440afdf6
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-macos"></a>macOS での Azure CLI 2.0 のインストール

macOS プラットフォームについては、[Homebrew パッケージ マネージャー](http://brew.sh)または手動のいずれかで、Azure CLI をインストールできます。 Homebrew を使用したインストール方法をお勧めします。こちらの方がインストール、更新プログラムの取得、およびアンインストール (必要な場合) が容易です。

## <a name="use-homebrew-to-install"></a>Homebrew を使用したインストール

CLI インストールを管理する方法としては、Homebrew を使用するのが最も簡単です。 これには、便利なインストール、更新、およびアンインストール手段が用意されています。 これは、`apt` や`yum` などの他のパッケージ マネージャーと似ています。
システムで使用できる Homebrew がない場合は、[Homebrew をインストール](https://docs.brew.sh/Installation.html)してから操作を続行します。

### <a name="install-with-homebrew"></a>Homebrew でのインストール

CLI をインストールするには、brew リポジトリ情報を更新し、`install` コマンドを実行します。

```bash
brew update && brew install azure-cli
```

その後、Azure CLI は `az` コマンドで実行できます。

### <a name="update-with-homebrew"></a>Homebrew での更新

CLI は、バグの修正、機能強化、新機能、およびプレビュー機能で定期的に更新されています。 新しいリリースは約 2 週間ごとに入手できます。 ローカル リポジトリ情報を更新してから、CLI パッケージを更新する必要があります。

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a>トラブルシューティング

Homebrew での CLI のインストールまたは更新時に問題が発生しましたか。 ここでは、発生する可能性のある一般的なエラーをいくつか取り上げ、そのエラーを診断および解決する方法を示します。

#### <a name="unable-to-find-python-or-installed-packages"></a>Python またはインストールされているパッケージが見つかりません

インストール時に Python またはインストールされているパッケージが見つからない場合、マイナー バージョンの不一致があるか、Homebrew のインストール中に別の問題が発生した可能性があります。 CLI は Virtualenv を使用しないため、Homebrew によってインストールされた正しいバージョンの Python を検索できる必要があります。 この問題を修正するには、Python インストールを再リンクします。

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a>CLI バージョンが古すぎます

インストールされている CLI バージョンが古くなっていると思われる場合は、`brew update` コマンドを実行し、その後に `brew upgrade azure-cli` を実行します。 これで CLI が更新されない場合は、Homebrew パッケージのロールアウトが、一般公開リリースよりも時間がかかっている可能性があります。 最新の CLI インストールが必要な場合は、[手動でインストール](#manage-the-cli-manually)してください。

### <a name="uninstall-with-homebrew"></a>Homebrew でのアンインストール

Azure CLI が不要であると判断した場合は、アンインストールすることができます。 アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。 Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。 また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。

Homebrew でインストールした場合は、アンインストールにも、それを使用する必要があります。

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a>CLI の手動インストール

CLI インストールの管理に Homebrew を使用できない、または使用したくない場合は、手動でインストールできます。

[手動による Linux インストール手順](install-azure-cli-linux.md)に従って、macOS に手動でインストールしてください。 macOS 10.9 バージョン以降には、必要な依存関係がすべて含まれています。
