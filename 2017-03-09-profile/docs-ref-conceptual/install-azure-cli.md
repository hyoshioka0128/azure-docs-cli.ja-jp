---
title: "Azure CLI 2.0 のインストール"
description: "Azure CLI 2.0 のインストールに関するリファレンス ドキュメント"
keywords: "Azure CLI, Azure CLI のインストール, Azure Python CLI, Azure CLI のリファレンス"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 2b56382355cad5313a604ed1f493a2bcbebf3e27
ms.sourcegitcommit: e9b4c6dd9093980b69ca47f93f44ac54d0e5b68a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2017
---
# <a name="install-azure-cli-20"></a>Azure CLI 2.0 のインストール

今すぐ Azure CLI の新しいバージョンをインストールしてください。
Azure のリソース管理を目的とした優れたネイティブ コマンド ライン エクスペリエンスを実現するために強化して更新しました。
macOS、Linux、および Windows で使用できます。
最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。

> [!NOTE]
> Azure CLI の以前のバージョンが必要な場合は、[Azure CLI 1.0 をインストールする](/azure/cli-install-nodejs)方法に関するページを参照してください。

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>macOS へのインストール

macOS では、[Homebrew](https://brew.sh/) または手動でインストールを行えます。

### <a name="install-with-homebrew"></a>Homebrew でインストールする

1. まだお持ちでない場合は、[Homebrew のインストール手順](https://docs.brew.sh/Installation.html)に従って Homebrew をインストールします。

2. 以前に手動で CLI をインストール済みの場合は、[手動によるアンインストール](#UninstallManually)の手順に従います。

3. ローカルの Homebrew リポジトリを更新します。

   ```bash
   brew update
   ```

4. `azure-cli` パッケージをインストールします。

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> 以前 Homebrew で Azure CLI 1.0 をインストールしている場合、パッケージをインストールをするのではなく、通常の Homebrew アップグレード プロセスで CLI 2.0 を取得できます。
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a>手動でインストールする

1. `curl` で Azure CLI 2.0 をインストールします。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 場合によっては、変更を有効にするために、シェルを再起動する必要があります。

   ```bash
   exec -l $SHELL
   ```
   
3. コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="install-on-windows"></a>Windows へのインストール

### <a name="install-with-msi-for-the-windows-command-line"></a>Windows コマンド ライン用に MSI でインストールを行う 

Windows に CLI をインストールして、Windows コマンド ラインで使用するには、[Azure CLI インストーラー (MSI)](https://aka.ms/InstallAzureCliWindows) をダウンロードして実行します。

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a>Bash on Ubuntu on Windows 用に apt-get でインストールを行う

1. Bash on Windows をインストールしていない場合は、[インストールします](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. Bash シェルを開きます。

3. ソース リストを変更します。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. 次の sudo コマンドを実行します。

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="install-with-apt-package-manager"></a>apt パッケージ マネージャーでのインストール 

Ubuntu、Debian など、`apt` パッケージ マネージャーを使用するディストリビューションでは、`apt-get` を使用して Azure CLI 2.0 をインストールできます。

> [!NOTE]
> CLI を使用するには、Python 2.7.x または Python 3.x が必要です。 ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。

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

3.  コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="install-with-yum-package-manager"></a>yum パッケージ マネージャーでのインストール

Red Hat Enterprise Linux (RHEL)、Fedora、CentOS など、`yum` パッケージ マネージャーを使用するディストリビューションでは、`yum` を使用して Azure CLI 2.0 をインストールできます。

> [!NOTE]
> CLI を使用するには、Python 2.7.x または Python 3.x が必要です。 ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。

1. Microsoft リポジトリ キーをインポートします。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. ローカル `azure-cli` リポジトリ情報を作成します。

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. `yum` パッケージのインデックスを更新し、インストールを行います。

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="install-with-zypper-package-manager"></a>zypper パッケージ マネージャーでのインストール

OpenSUSE、SLE など、`zypper` パッケージ マネージャーを使用するディストリビューションでは、`zypper` を使用して Azure CLI 2.0 をインストールできます。

> [!NOTE]
> CLI を使用するには、Python 2.7.x または Python 3.x が必要です。 ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。

1. Microsoft リポジトリ キーをインポートします。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. ローカル `azure-cli` リポジトリ情報を作成します。

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. `zypper` パッケージのインデックスを更新し、インストールを行います。

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="install-with-docker"></a>Docker によるインストール

Microsoft では、Azure CLI 2.0 が事前構成されている Docker イメージを保持しています。

`docker run` を使用して、CLI をインストールしてください。

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。

CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。

> [!NOTE]
> ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><a name="Linux"/>パッケージ マネージャーなしでの Linux へのインストール

可能であれば、CLI はパッケージ マネージャーを使ってインストールすることをお勧めします。 Microsoft のリポジトリを追加しない場合、または指定されたパッケージがないディストリビューションで操作している場合は、手動で CLI をインストールできます。

1. Linux ディストリビューションに応じて、前提条件をインストールします。

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

ディストリビューションが上の一覧に記載されていない場合は、[Python 2.7 以降](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/)、[OpenSSL](https://www.openssl.org/source/) をインストールする必要があります。

2. `curl` で CLI をインストールしてください。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 場合によっては、変更を有効にするために、シェルを再起動する必要があります。

   ```bash
   exec -l $SHELL
   ```

4. コマンド プロンプトで `az` コマンドを使用して、CLI を実行します。

## <a name="troubleshooting"></a>トラブルシューティング

CLI のインストール中に問題が発生した場合は、このセクションを見て、該当するケースの説明があるかどうかを確認してください。 問題がここで説明されていない場合は、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)してください。

### <a name="curl-object-moved-error"></a>curl の "Object Moved" エラー

`curl` で `-L` パラメーターに関連するエラーが発生した場合や、"Object Moved" というテキストが含まれているエラー メッセージが表示された場合は、次のように、`aka.ms` リダイレクトの代わりに完全な URL を使用してみてください。

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>`az` コマンドが見つからない

シェルのコマンド ハッシュのキャッシュをクリアすることが必要になる場合があります。 実行

```bash
hash -r
```

問題が解決されているかどうかを確認してください。 コマンドが、`$PATH` にない可能性もあります。 `<install path>/bin` が `$PATH` に 表示されることを確認し、必要に応じてシェルを再起動してください。

## <a name="uninstall-cli-1x-versions"></a>CLI 1.x バージョンのアンインストール

システム上で以前の CLI 1.x バージョンが使用可能な場合は、使用されたインストールの種類に基づいてアンインストールすることができます。

### <a name="uninstall-with-npm"></a>npm でのアンインストール

古い CLI を `npm uninstall` で削除します。

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a>再頒布可能パッケージでのアンインストール

[Azure CLI インストーラー (MSI)](http://aka.ms/webpi-azure-cli) または [macOS パッケージ](http://aka.ms/mac-azure-cli)を通じてインストールした場合は、同じツールを使用してインストールを削除してください。

### <a name="uninstall-with-docker"></a>Docker でのアンインストール

以前の CLI バージョンを使用するために Docker イメージをインストールした場合は、そのイメージと、関連するすべてのコンテナーを削除します。 その後、インストール手順の説明に従って新しい Docker イメージをインストールしてから、コンテナーを再作成できます。

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>CLI の更新

Azure CLI を更新するには、それをインストールしたのと同じ方法を使用します。

### <a name="update-with-homebrew"></a>Homebrew での更新

1. 以前に手動でインストール済みの場合は、「[Homebrew でインストールする](#macOS)」の手順に従います。

2. ローカルの Homebrew リポジトリ情報を更新します。

   ```bash
   brew update
   ```

3. インストール済みパッケージをアップグレードします。

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a>MSI での更新

もう一度 [Azure CLI インストーラー (MSI)](https://aka.ms/InstallAzureCliWindows) を実行します。

### <a name="update-with-apt"></a>apt での更新

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

### <a name="update-with-yum"></a>yum での更新

`yum update` コマンドで Azure CLI を更新します。

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a>zypper での更新

`zypper update` コマンドでパッケージを更新できます。

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

### <a name="update-with-docker"></a>Docker での更新

1. `docker pull` でローカル イメージを更新します。

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. 現時点で CLI イメージを使用しているコンテナーを取得します。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。

3. コンテナーを停止し、もう一度作成します。

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a>手動での更新

更新するには、[macOS](#macOS) または [Linux](#Linux) の手動でのインストール手順に従ってください。

## <a name="uninstall"></a>アンインストール

CLI が不要であると判断した場合は、アンインストールすることができます。 CLI をインストールしたときと同じ方法を使用して、アンインストールする必要があります。

### <a name="uninstall-with-homebrew"></a>Homebrew でのアンインストール

`azure-cli` パッケージをアンインストールします。

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a>MSI でのアンインストール

[MSI](https://aka.ms/InstallAzureCliWindows) をもう一度実行して、アンインストールを選択します。

### <a name="uninstall-with-apt"></a>apt でのアンインストール

次のように、`apt-get remove` を通じてアンインストールします。

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a>yum でのアンインストール

1. システムからパッケージを削除します。

   ```bash
   sudo yum remove azure-cli
   ```

2. CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a>zypper でのアンインストール

1. システムからパッケージを削除します。

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-docker"></a>Docker でのアンインストール

Docker イメージをインストールした場合は、それを実行しているすべてのコンテナーを削除してから、ローカル イメージを削除する必要があります。

1. azure-cli イメージを実行しているコンテナーを取得します。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. CLI イメージがあるすべてのコンテナーを削除します。

   ```bash
   docker rm 34a868beb2ab
   ```

3. ローカルにインストールされた CLI イメージを削除します。

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><a name="UninstallManually"/>手動でのアンインストール

https://aka.ms/InstallAzureCli のスクリプトを使用して CLI をインストールした場合は、次の手順でアンインストールできます。

1. インストールされたファイルを削除します。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. `<install location>/.bash_profile` から `<install location>/lib/azure-cli/az.completion` という行を削除します。

3. シェルでコマンド キャッシュを使用する場合は、それを再度読み込んでください。

   ```bash
   hash -r
   ```

> [!Note]
> 既定のインストール場所は `/Users/<username>` です。

## <a name="report-cli-issues-and-feedback"></a>CLI の問題とフィードバックの報告

ツールにバグを発見した場合は、GitHub リポジトリの [[Issues]\(問題\)](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。
コマンド ラインからフィードバックを送るには、`az feedback` コマンドを使用します。
