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
ms.openlocfilehash: bc3ae41ea04ae8d7f62242b2bfe415c8a3bfea33
ms.sourcegitcommit: 08043c47d3ccf23522b91e6bba3932e312c04c7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66516294"
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

### <a name="proxy-blocks-connection"></a>プロキシによる接続のブロック

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

常にこのプロキシを使用するように `yum` を明示的に構成することが必要な場合もあります。 次の行が `/etc/yum.conf` の `[main]` セクションの下に表示されていることを確認してください。

```yum.conf
[main]
# ...
proxy=http://[proxy]:[port] # If your proxy requires https, change http->https
proxy_username=[username] # Only required for basic auth
proxy_password=[password] # Only required for basic auth
```

Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。

* `https://packages.microsoft.com`

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
