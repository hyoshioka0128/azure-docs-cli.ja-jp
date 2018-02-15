---
title: "zypper を使用して Linux に Azure CLI 2.0 をインストールする"
description: "zypper で Azure CLI 2.0 をインストールする方法"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 6ee3aff74f43fab0c80c58c7fe57c9fa74a6ef2f
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-with-zypper"></a>zypper での Azure CLI 2.0 のインストール

openSUSE や SLES など、`zypper` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。 このパッケージは、openSUSE 42.2 と SLES 12 SP 2 でテストされています。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>Install

1. `curl` をインストールします。

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. Microsoft リポジトリ キーをインポートします。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. ローカル `azure-cli` リポジトリ情報を作成します。

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. `zypper` パッケージのインデックスを更新し、インストールを行います。

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

CLI は `az` コマンドで実行できます。

## <a name="update"></a>プライマリの

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
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

