---
title: "Azure CLI 2.0 のインストール"
description: "Azure CLI 2.0 のリファレンス ドキュメント"
keywords: "Azure CLI 2.0, Azure CLI 2.0 のリファレンス, Azure CLI 2.0 のインストール, Azure Python CLI, Azure CLI 2.0 のアンインストール"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 7065ed5270ef9bfc70beea81d0bc442a7b4df38c
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a>Azure CLI 2.0 のインストール

今すぐ Azure CLI の新しいバージョンをインストールしてください。
Azure のリソース管理を目的とした優れたネイティブ コマンド ライン エクスペリエンスを実現するために強化して更新しました。
macOS、Linux、および Windows で使用できます。
最新リリースについては、[リリース ノート](release-notes-azure-cli.md)を参照してください。

> [!NOTE]
> Azure CLI の以前のバージョンが必要な場合は、[Azure 1.0 をインストールする](/azure/cli-install-nodejs)方法を参照してください。

## <a name="macos"></a>macOS

1. 1 つの `curl` コマンドで Azure CLI 2.0 をインストールします。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 場合によっては、変更を有効にするために、コマンド シェルを再起動する必要があります。

   ```bash
   exec -l $SHELL
   ```
   
3. コマンド プロンプトから `az` コマンドを使用して、Azure CLI 2.0 を実行します。

> [!Note]
> InstallAzureCli を使用してインストールした場合、`az component update` はサポートされません。
> 最新の CLI に更新するには、`curl -L https://aka.ms/InstallAzureCli | bash` をもう一度実行します。
> 
> アンインストールするには、[手動のアンインストール手順](#uninstall)を参照してください。

## <a name="windows"></a>Windows

MSI を使用して CLI をインストールし、Windows コマンド ラインで使用するか、Bash on Ubuntu on Windows で apt-get を使用して、CLI をインストールできます。

### <a name="msi-for-the-windows-command-line"></a>Windows コマンド ライン用の MSI 

Windows に CLI をインストールして、Windows コマンド ラインで使用するには、[msi](https://aka.ms/InstallAzureCliWindows) をダウンロードして実行します。

> [!NOTE]
> msi を使用してインストールする場合、`az component` はサポートされません。
> 最新の CLI に更新するには、[msi](https://aka.ms/InstallAzureCliWindows) をもう一度実行します。
> 
> CLI をアンインストールするには、[msi](https://aka.ms/InstallAzureCliWindows) をもう一度実行して、アンインストールを選択します。

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a>Bash on Ubuntu on Windows 用の apt-get

1. Bash on Windows をインストールしていない場合は、[インストールします](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. Bash シェルを開きます。

3. ソース リストを変更します。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. 次の sudo コマンドを実行します。

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> apt-get を使用してインストールした場合、`az component` はサポートされません。
> CLI を更新するには、`sudo apt-get update && sudo apt-get install azure-cli` をもう一度実行します。
> 
> アンインストールするには、`sudo apt-get remove azure-cli` を実行します。

## <a name="linux"></a>Linux

1. Linux では、固有の[前提条件](#linux-prerequisites)をインストールすることが必要な場合があります。

2. 1 つの `curl` コマンドで Azure CLI 2.0 をインストールします。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 場合によっては、変更を有効にするために、コマンド シェルを再起動する必要があります。

   ```bash
   exec -l $SHELL
   ```

4. コマンド プロンプトから `az` コマンドを使用して、Azure CLI 2.0 を実行します。

> [!Note]
> InstallAzureCli を使用してインストールした場合、`az component update` はサポートされません。
> 最新の CLI に更新するには、`curl -L https://aka.ms/InstallAzureCli | bash` をもう一度実行します。
> 
> アンインストールするには、[手動のアンインストール手順](#uninstall)を参照してください。

## <a name="docker"></a>Docker

Microsoft では、Azure CLI が事前構成されている Docker イメージを保持しています。

`docker run` を使用して Azure CLI をインストールします。

```bash
docker run azuresdk/azure-cli-python:<version>
```

利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。

> [!NOTE]
> ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> Docker イメージでは、[`component` 機能](/cli/azure/component)がサポートされていません。
> Azure CLI 2.0 を更新するには、`docker run` を使用して、最新のイメージまたは必要とする特定のイメージをインストールします。

## <a name="apt-get"></a>apt-get

Debian/Ubuntu ベースのシステムでは、`apt-get` を使用して Azure CLI 2.0 をインストールできます。

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
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> apt-get を使用してインストールした場合、`az component` はサポートされません。
> CLI を更新するには、`sudo apt-get update && sudo apt-get install azure-cli` をもう一度実行します。
> 
> アンインストールするには、`sudo apt-get remove azure-cli` を実行します。

## <a name="linux-prerequisites"></a>Linux の前提条件

1. [Python](https://www.python.org/downloads) をインストールしていない場合は、インストールします。

2. お使いの Linux ディストリビューションに応じて、前提条件をインストールします。

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="errors-with-curl-redirection"></a>curl リダイレクトでのエラー

`curl` コマンドで `-L` パラメーターに関連するエラーが発生した場合や、"Object moved" というエラーが発生した場合は、aka.ms URL の代わりに完全な URL を使用してみてください。

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a>アンインストール

https://aka.ms/InstallAzureCli のスクリプトを使用して CLI をインストールした場合は、次の手順でアンインストールできます。

1. インストールされたファイルを削除します。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. `<install location>/.bash_profile` から `<install location>/lib/azure-cli/az.completion` という行を削除します。

> [!Note]
> 既定のインストール場所は `/Users/<username>` です。

apt-get、Docker、または msi を使用して CLI をインストールした場合は、同じツールを使用してアンインストールします。

## <a name="reporting-issues-and-feedback"></a>問題とフィードバックの報告

ツールにバグを発見した場合は、GitHub リポジトリの [[Issues (問題)]](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。
コマンド ラインからフィードバックを送るには、`az feedback` コマンドを試してください。
