---
title: apt を使用して Linux に Azure CLI 2.0 をインストールする
description: apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/24/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: abbffb1c474d752130dfffa8e60937b3d632fa14
ms.sourcegitcommit: c6c3058254974b3a1d5d2fa2cd231a900c53d321
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2018
ms.locfileid: "37126584"
---
# <a name="install-azure-cli-20-with-apt"></a>apt での Azure CLI 2.0 のインストール

Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能な 64 ビット パッケージがあります。 このパッケージは、以下でテストされています。

* Ubuntu trusty、xenial、artful、および bionic
* Debian wheezy、jessie、および stretch

## <a name="install"></a>Install

1. <a name="install-step-1"/>お使いのソース リストを変更します。

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

2. <a name="signingKey"></a>Microsoft の署名キーを取得します。

   ```bash
   curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   ```

3. CLI をインストールします。

   ```bash
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > 署名キーは 2018 年 5 月に更新され、置き換えられました。 署名キーのエラーが発生した場合は、[最新の署名キーを取得済み](#signingKey)であることを確認してください。

その後、Azure CLI は `az` コマンドで実行できます。 ログインするには、`az login` コマンドを実行します。

```azurecli
az login
```

さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。 問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="lsbrelease-fails-with-command-not-found"></a>"コマンドが見つかりません" が発生して lsb_release が失敗する

`lsb_release` コマンドの実行時に、次のようなエラーが出力されることがあります。

```output
-bash: lsb_release: command not found
```

このエラーは、lsb_release がインストールされていないことが原因です。 これを解決するには、`lsb-release` パッケージをインストールします。

```bash
sudo apt-get install lsb-release
```

### <a name="lsbrelease-does-not-return-the-base-distribution-version"></a>lsb_release では、ベース ディストリビューション バージョンが返されません

Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。 この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。 ディストリビューションの派生元バージョンの名前がわかっている場合は、[インストール手順 1.](#install-step-1) で `AZ_REPO` 値を手動で設定できます。 それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューション名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。

### <a name="apt-key-fails-with-no-dirmngr"></a>"No dirmngr" で apt-key が失敗する

`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

このエラーは、`apt-key` に必要なコンポーネントがないためです。 これを解決するには、`dirmngr` パッケージをインストールします。

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a>apt-key がハングする

ファイアウォールの内側でポート 11371 への発信接続がブロックされている場合、`apt-key` コマンドが無期限にハングすることがあります。 発信接続用にファイアウォールで HTTP プロキシを使用する必要がある可能性があります。

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

プロキシがあるかどうかがわからない場合は、システム管理者に問い合わせてください。 プロキシでログインを必要としない場合は、ユーザー、パスワード、および `@` トークンを指定しないでください。

## <a name="update"></a>アップデート

CLI パッケージを更新するには、`apt-get upgrade` を使用します。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> 署名キーは 2018 年 5 月に更新され、置き換えられました。 署名キーのエラーが発生した場合は、[最新の署名キーを取得済み](#signingKey)であることを確認してください。
   
> [!NOTE]
> このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。
> CLI だけをアップグレードするには、`apt-get install` を使用します。
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

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
