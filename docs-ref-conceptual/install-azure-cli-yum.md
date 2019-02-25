---
title: yum を使用して Linux に Azure CLI をインストールする
description: yum で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: e0b2406ee8b235fc96fb9f2990ad1646d8cb8494
ms.sourcegitcommit: 1987a39809f9865034b27130e56f30b2bd1eb72c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "56421872"
---
# <a name="install-azure-cli-with-yum"></a>yum での Azure CLI のインストール

RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。 このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

## <a name="install"></a>Install

1. Microsoft リポジトリ キーをインポートします。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. ローカル `azure-cli` リポジトリ情報を作成します。

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. `yum install` コマンドを使用してインストールします。

   ```bash
   sudo yum install azure-cli
   ```

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。 ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a>アップデート

`yum update` コマンドで Azure CLI を更新します。

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a>アンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

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
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
