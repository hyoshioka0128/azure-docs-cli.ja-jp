---
title: Azure CLI 2.0 で複数のクラウドを管理する
description: Azure CLI 2.0 で複数のクラウドの作成、ログイン、管理を行います。
author: sptramer
manager: routlaw
ms.author: sttramer
ms.date: 10/20/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: c17506cc81adc859ff5778b109c1832c857764e6
ms.sourcegitcommit: c9da729f4a42a839f13106f7589deaa0ca19cc4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2018
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>Azure CLI 2.0 で複数のクラウドを管理する

異なるリージョンにわたって作業したり、[Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/) を使用したりする場合、複数のクラウドの使用が必要になることがあります。 Microsoft はお客様が使用可能な、リージョンの法規に従ったクラウドを提供します。 この記事では、お客様のアカウントで使用可能なクラウドに関する情報の取得、現行クラウドの変更、Azure Stack で使用する新規クラウドの登録または登録解除の方法について説明します。

## <a name="listing-clouds"></a>クラウドの一覧表示

使用可能なクラウドを [az cloud list](/cli/azure/cloud#az-cloud-list) コマンドで一覧表示することができます。 これにより、現在アクティブなクラウド、その現在のプロファイル、およびリージョン サフィックスとホスト名に関する情報が得られます。

アクティブなクラウドと、すべての使用可能クラウドの一覧を取得するには、次のように入力します。

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

現在アクティブなクラウドには `IsActive` 列に `True` と表示されます。 一度にアクティブにできるクラウドは 1 つのみです。 Azure サービスに使用するエンドポイントなど、クラウドに関するより詳細な情報を得るには、`cloud show` コマンドを使用します。

```azurecli
az cloud show --name AzureChinaCloud --output json
```

```output
{
  "endpoints": {
    "activeDirectory": "https://login.chinacloudapi.cn",
    "activeDirectoryDataLakeResourceId": null,
    "activeDirectoryGraphResourceId": "https://graph.chinacloudapi.cn/",
    "activeDirectoryResourceId": "https://management.core.chinacloudapi.cn/",
    "batchResourceId": "https://batch.chinacloudapi.cn/",
    "gallery": "https://gallery.chinacloudapi.cn/",
    "management": "https://management.core.chinacloudapi.cn/",
    "resourceManager": "https://management.chinacloudapi.cn",
    "sqlManagement": "https://management.core.chinacloudapi.cn:8443/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json"
  },
  "isActive": false,
  "name": "AzureChinaCloud",
  "profile": "latest",
  "suffixes": {
    "azureDatalakeAnalyticsCatalogAndJobEndpoint": null,
    "azureDatalakeStoreFileSystemEndpoint": null,
    "keyvaultDns": ".vault.azure.cn",
    "sqlServerHostname": ".database.chinacloudapi.cn",
    "storageEndpoint": "core.chinacloudapi.cn"
  }
}
```

## <a name="switching-the-active-cloud"></a>アクティブなクラウドの切り替え

現在アクティブなクラウドを切り替えるには、[az cloud set](/cli/azure/cloud#az-cloud-set) コマンドを実行します。 このコマンドは、1 つの必須の引数として、クラウドの名前を受け取ります。

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> アクティブ化されたクラウドの認証が期限切れになった場合は、他の CLI タスクを実行する前に、再認証を行う必要があります。 新しいクラウドに初めて切り替える場合は、アクティブなサブスクリプションの設定も行う必要があります。
> 認証の手順については、「[Log in with Azure CLI 2.0 (Azure CLI 2.0 を使用してログインする)](authenticate-azure-cli.md)」を参照してください。 サブスクリプションの管理については、[Azure CLI 2.0 での Azure サブスクリプションの管理](manage-azure-subscriptions-azure-cli.md)に関するページをご覧ください。

## <a name="register-a-cloud"></a>クラウドを登録する

Azure Stack 用の独自のエンドポイントがある場合は、新しいクラウドを登録します。 [az cloud register](/cli/azure/cloud#az-cloud-register) コマンドを実行すると、クラウドが作成されます。 このコマンドは、名前と、関連するエンドポイントを持つ機能のセットを必要とします。 Azure Stack で使用するクラウドの登録方法については、[Azure Stack で使用する CLI のインストールと構成](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack)に関するページをご覧ください。

中国、米国政府、またはドイツのリージョンについては、独自のクラウドを登録する必要はありません。 これらは Microsoft が管理しているため、既定値で使用可能です。  使用可能なエンドポイント設定に関する詳細については、[`az cloud register` のドキュメント](/cli/azure/cloud#az-cloud-register)を参照してください。

クラウドを登録しても、自動的にそのクラウドに切り替わるわけではありません。 前述のように、`az cloud set` コマンドを使用して、新規作成したクラウドを選択してください。

## <a name="update-an-existing-cloud"></a>既存のクラウドを更新する

権限がある場合は、既存のクラウドを更新することもできます。 この更新は、別の Azure プロファイルへの切り替え、エンドポイントの追加、またはエンドポイントの変更が必要な場合に行いますい。
これは [az cloud update](/cli/azure/cloud#az-cloud-update) コマンドを使用して実行します。このコマンドでは `az cloud register` と同じ引数を使用します。

## <a name="unregister-a-cloud"></a>クラウドを登録解除する

登録済みのクラウドが不要になった場合は、次のように、[az cloud unregister](/cli/azure/cloud#az-cloud-unregister) コマンドを使用して登録解除できます。

```azurecli
az cloud unregister --name MyCloud
```
