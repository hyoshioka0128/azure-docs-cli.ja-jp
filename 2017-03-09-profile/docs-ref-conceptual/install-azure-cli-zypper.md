---
title: "zypper での Azure CLI 2.0 のインストール"
description: "zypper で Azure CLI 2.0 をインストールする方法"
keywords: "azure cli, azure cli のインストール, azure cli zypper, azure cli opensuse, azure cli sle"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c01679ccb77880f1f628f4e48683d8ff030a568b
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-zypper"></a>zypper での Azure CLI 2.0 のインストール

OpenSUSE、SLE など、`zypper` に付属するディストリビューションを実行している場合は、システムにインストールできる Azure CLI 用の利用可能なパッケージがあります。

> [!NOTE]
> CLI を使用するには、Python 2.7.x または Python 3.x が必要です。 ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。

## <a name="install"></a>インストール 

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

## <a name="update"></a>更新

`zypper update` コマンドでパッケージを更新できます。

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a>アンインストール

Azure CLI が不要であると判断した場合は、アンインストールすることができます。 アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。 Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。 また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。

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

