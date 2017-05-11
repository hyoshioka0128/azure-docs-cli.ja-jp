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
ms.openlocfilehash: 664535701ad814f8ff85fefe8ecc45772777d0ba
ms.sourcegitcommit: ec22ff07aedb5c47e5f636f2a9a341c3edbe7ca1
ms.translationtype: HT
ms.contentlocale: ja-JP
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

Azure CLI 2.0 では Bash のコマンド構文をサポートしているため、Bash on Ubuntu on Windows は CLI を使用する優れた方法です。
Bash を使用しない場合は、Windows コマンド ラインで CLI をインストールして使用することができます。

### <a name="bash-on-ubuntu-on-windows"></a>Bash on Ubuntu on Windows

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

### <a name="windows-command-line"></a>Windows コマンド ライン 

1. Python サイトにアクセスし、Windows 向けの [Python をダウンロード](https://www.python.org/downloads/)します。
   Python をインストールする場合は、必ず Pip コンポーネントをインストールしてください。
   インストールが完了したら、PATH 環境変数に Python を追加します (インストーラーによって追加するよう求められます)。

2. コマンド プロンプトから Python のインストールを確認します。

   ```bash
   python --version
   ```

3. `pip` を使用して Azure CLI 2.0 をインストールします。

   ```bash
   pip install --user azure-cli
   ```

4. az.bat が含まれているフォルダーをパスに追加します。
   CLI の `az.bat` は、通常、`%USERPROFILE%\AppData\Roaming\Python\Scripts` または `%USERPROFILE%\AppData\Roaming\Python\PythonXY\Scripts` にインストールされています。`XY` は Python のバージョンです (例: `%USERPROFILE%\AppData\Roaming\Python\Python27\Scripts`)。
   `az.bat` が含まれているフォルダーをパスに追加します。
   
4. コマンド プロンプトから `az` コマンドを使用して、Azure CLI 2.0 を実行します。

> [!NOTE]
> Azure CLI 2.0 が既にインストールされており、最新バージョンがインストールされているかどうかを確認するには、`az --version` を使用して、バージョンを確認します。
> そのバージョンを、[https://pypi.python.org/pypi/azure-cli](https://pypi.python.org/pypi/azure-cli) から入手できる最新バージョンと比較します。
> 
> 最新の CLI に更新するには、`az component update` を実行します。
> 
> CLI をアンインストールするには、`pip uninstall azure-cli` を実行します。

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
-------------------------------

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


### <a name="errors-on-install-with-cffi-or-cryptography"></a>`cffi` または暗号化を使用してインストールした場合のエラー

OS X でインストール時にエラーが発生した場合は、`pip` をアップグレードします。

```bash
pip install --upgrade --force-reinstall pip
```

**Debian** または **Ubuntu** でインストール時にエラーが発生した場合は、`libssl-dev` と `libffi-dev` をインストールしてください。

```bash
sudo apt-get update
sudo apt-get install -y libssl-dev libffi-dev
```

また、使用している Python のバージョンに対応した Python Dev をインストールします。

Python 2:

```bash
sudo apt-get install -y python-dev
```

Python 3:

```bash
sudo apt-get install -y python3-dev
```

Ubuntu 15 では `build-essential` も必要な場合があります。

```bash
sudo apt-get install -y build-essential
```

### <a name="example-errors"></a>エラーの例

```
Downloading cffi-1.5.2.tar.gz (388kB)
    100% |################################| 389kB 3.9MB/s
    Complete output from command python setup.py egg_info:

        No working compiler found, or bogus compiler options
        passed to the compiler from Python's distutils module.
        See the error messages above.
        (If they are about -mno-fused-madd and you are on OS/X 10.8,
        see http://stackoverflow.com/questions/22313407/ .)

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-77i2fido/cffi/
```

```
#include <openssl/e_os2.h>
                            ^
compilation terminated.
error: command 'x86_64-linux-gnu-gcc' failed with exit status 1

Failed building wheel for cryptography
```

Stack Overflow の質問 (「[Failed to install Python Cryptography package with PIP and setup.py (PIP と setup.py で Python 暗号化パッケージをインストールできない)](http://stackoverflow.com/questions/22073516/failed-to-install-python-cryptography-package-with-pip-and-setup-py)」) を参照してください。

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

pip、apt-get、または Docker を使用して CLI をインストールした場合は、同じツールを使用してアンインストールします。

## <a name="reporting-issues-and-feedback"></a>問題とフィードバックの報告

ツールにバグを発見した場合は、GitHub リポジトリの [[Issues (問題)]](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。
コマンド ラインからフィードバックを送るには、`az feedback` コマンドを試してください。
