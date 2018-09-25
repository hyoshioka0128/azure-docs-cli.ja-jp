---
title: yum を使用して Linux に Azure CLI 2.0 をインストールする
description: yum で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 25eb473aa56d3ddd34f8e1808b84ebb5f6324f2b
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46470016"
---
# <a name="install-azure-cli-20-with-yum"></a>yum での Azure CLI 2.0 のインストール

RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。 このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

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

さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

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
