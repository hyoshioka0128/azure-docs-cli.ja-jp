---
title: apt を使用して Linux に Azure CLI をインストールする
description: apt パッケージ マネージャーで Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/27/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 1973c933cbffa494cbe9c0749346450251feefcb
ms.sourcegitcommit: 9bd90875a324908ec7195fc4c4f63ebf124760f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982588"
---
# <a name="install-azure-cli-with-apt"></a>apt での Azure CLI のインストール

Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用に 64 ビット パッケージを使用できます。 このパッケージは、以下でテストされています。

* Ubuntu trusty、xenial、artful、および bionic
* Debian wheezy、jessie、および stretch

## <a name="install"></a>Install

1. 前提条件となるパッケージをインストールします。

    ```bash
    sudo apt-get install apt-transport-https lsb-release software-properties-common dirmngr -y
    ```

2. <div id="set-release"/>ソース リストを変更します。

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

3. <div id="signingKey"/>Microsoft の署名キーを取得します。

   ```bash
   sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
        --keyserver packages.microsoft.com \
        --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
   ```

4. CLI をインストールします。

   ```bash
   sudo apt-get update
   sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > 署名キーは 2018 年 5 月に更新され、置き換えられました。 署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。 ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="lsbrelease-does-not-return-the-correct-base-distribution-version"></a>lsb_release がベース ディストリビューション バージョンを返さない

Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。 この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。 ディストリビューションの派生元バージョンの名前がわかっている場合は、[インストール手順 2.](#set-release) で `AZ_REPO` 値を手動で設定できます。 それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューション名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。

### <a name="no-package-for-your-distribution"></a>ご使用のディストリビューションのパッケージがない

Ubuntu ディストリビューションがリリースされてから、そのディストリビューション用の Azure CLI パッケージが利用可能になるまではしばらくかかることがあります。 Azure CLI は、以降のバージョンの依存関係に関して弾力性を持つように、また可能な限り以降のバージョンに依存しないように設計されています。 ベース ディストリビューションに使用できるパッケージがない場合は、以前のディストリビューション用のパッケージをお試しください。

これを行うには、[インストール手順 1.](#install-step-1) で、`AZ_REPO` の値を手動で設定します。 Ubuntu ディストリビューションには `bionic` リポジトリーを使用し、Debian ディストリビューションには `stretch` を使用します。 Ubuntu Trusty および Debian Wheezy より前にリリースされたディストリビューションはサポートされていません。

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

Windows Subsystem for Linux (WSL) の場合は、このエラーは Windows 10 1809 よりも前のバージョンの Windows にも表示されます。 問題を解決するには、Windows のバージョンを更新します。

### <a name="apt-key-hangs"></a>apt-key がハングする

ファイアウォールの内側でポート 11371 への発信接続がブロックされている場合、`apt-key` コマンドが無期限にハングすることがあります。
ご使用のファイアウォールでは、発信接続用に HTTP プロキシが必要になる場合があります。

```bash
sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
    --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ \
    --keyserver packages.microsoft.com \
    --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
```

プロキシがあるかどうかを確認するには、システム管理者に問い合わせてください。 プロキシでログインが不要な場合は、ユーザーとパスワードの情報を指定しないでください。

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a>アップデート

CLI パッケージを更新するには、`apt-get upgrade` を使用します。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> 署名キーは 2018 年 5 月に更新され、置き換えられました。 署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。
>
> [!NOTE]
> このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。
> CLI だけをアップグレードするには、`apt-get install` を使用します。
> 
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

3. 署名キーを削除します。

    ```bash
    sudo rm /etc/apt/trusted.gpg.d/Microsoft.gpg
    ```

4. 不要なパッケージを削除します。

   ```bash
   sudo apt autoremove
   ```

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
