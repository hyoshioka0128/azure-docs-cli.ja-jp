---
title: zypper を使用して Linux に Azure CLI をインストールする
description: zypper で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: f8a3bec4fffb731c6521fa7b8a2a90798ef191e6
ms.sourcegitcommit: 08043c47d3ccf23522b91e6bba3932e312c04c7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66516232"
---
# <a name="install-azure-cli-with-zypper"></a>zypper での Azure CLI のインストール

openSUSE や SLES など、`zypper` が付属するディストリビューションには、Azure CLI 用に利用できるパッケージが用意されています。 このパッケージは、openSUSE 42.2 以降と SLES 12 SP 2 以降でテストされています。

[!INCLUDE [current-version](includes/current-version.md)]

[!INCLUDE [rpm-warning](includes/rpm-warning.md)]

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

その後、Azure CLI は `az` コマンドで実行できます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

ここでは、`zypper` でのインストール時に発生する一般的な問題をいくつか示します。 ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。

### <a name="proxy-blocks-connection"></a>プロキシによる接続のブロック

[!INCLUDE[configure-proxy](includes/configure-proxy.md)]

常にこのプロキシを使用するように `zypper` (`yast2` 経由) を明示的に構成することが必要な場合もあります。 このためには、`yast2 proxy` コマンドをスーパーユーザーとして実行し、フォームに提示された情報を入力します。 システムでウィンドウ マネージャーを使用できる場合、`YaST Control Center` で `Network Services > Proxy` ウィンドウを使用することもできます。

詳細な構成やその他の情報については、[OpenSUSE プロキシの構成に関するドキュメント](https://www.suse.com/documentation/slms1/book_slms/data/sec_wy_config_updates_proxy.html)をご覧ください。

Microsoft 署名キーを取得し、リポジトリからパッケージを取得するには、お使いのプロキシで次のアドレスへの HTTPS 接続を許可する必要があります。

* `https://packages.microsoft.com`
* `https://download.opensuse.org`

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

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

## <a name="next-steps"></a>次の手順

これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。

> [!div class="nextstepaction"]
> [Azure CLI の概要](get-started-with-azure-cli.md)
