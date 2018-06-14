---
title: zypper を使用して Linux に Azure CLI 2.0 をインストールする
description: zypper で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: a862cca17adb1bfa0201af250819158081c29813
ms.sourcegitcommit: 5c80e96e96f9608c92a94fa4a9c4afb25099f3fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2018
ms.locfileid: "35512973"
---
# <a name="install-azure-cli-20-with-zypper"></a>zypper での Azure CLI 2.0 のインストール

openSUSE や SLES など、`zypper` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。 このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>Install

1. `curl` をインストールします。

   ```bash
   sudo zypper install -y curl
   ```

2. Microsoft リポジトリ キーをインポートします。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. ローカル `azure-cli` リポジトリ情報を作成します。

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. `zypper` パッケージのインデックスを更新し、インストールを行います。

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

その後、Azure CLI は `az` コマンドで実行できます。 ログインするには、`az login` コマンドを実行します。

```azurecli
az login
```

さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。

## <a name="update"></a>アップデート

`zypper update` コマンドでパッケージを更新できます。

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. システムからパッケージを削除します。

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。

  ```bash
  sudo zypper removerepo azure-cli
  ```

3. リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

