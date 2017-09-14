---
title: "Azure CLI 2.0 で複数のクラウドを管理する"
description: "Azure CLI 2.0 でさまざまなクラウドの作成、ログイン、管理を行います。"
keywords: "Azure CLI 2.0, Azure, クラウド, データセンター, 政府機関, リージョン, 中国, ドイツ"
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>Azure CLI 2.0 で複数のクラウドを管理する

Azure に複数のサブスクリプションが関連付けられている場合は、複数のクラウドを使用できます。 各クラウドには独自の関連エンドポイントと機能があり、多くの場合、さまざまなデータ保護標準や要件がある特定のリージョンに関連付けられています。

複数のクラウドを効果的に使用するには、アクティブなクラウドを切り替えることができ、新しいクラウドを作成できる必要があります。

## <a name="listing-clouds"></a>クラウドの一覧表示

[cloud list](/cli/azure/cloud#list) コマンドを使って、使用できるクラウドを一覧表示することができます。 これで、どのクラウドが現在アクティブであり、どれが現在のプロファイルであるかがわかります。また、リージョン サフィックスとホスト名に関する情報も示されます。

使用できるクラウドと現在アクティブなクラウドの一覧を取得するには、次のようにします。

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

## <a name="switching-the-active-cloud"></a>アクティブなクラウドの切り替え

現在アクティブなクラウドを切り替えるには、[cloud set](/cli/azure/cloud#set) コマンドを実行します。 このコマンドは、1 つの必須の引数として、クラウドの名前を受け取ります。

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> アクティブ クラウドでまだ認証を行っていない場合は、他の CLI 操作を実行する前に、認証を行う必要があります。 認証の手順については、「[Log in with Azure CLI 2.0 (Azure CLI 2.0 を使用してログインする)](/cli/azure/authenticate-azure-cli)」を参照してください。

## <a name="register-or-unregister-a-cloud"></a>クラウドの登録または登録解除

独自のエンドポイントがあるか、別のプロファイルが必要な場合は、新しいクラウドを登録します。 [cloud register](/cli/azure/cloud#register) コマンドを実行すると、クラウドが作成されます。 このコマンドには、名前を指定する必要があります。また、オプションで、機能とエンドポイントのセットも指定できます。

リソース マネージャー用の特別なエンドポイントと特定のプロファイルを備えたクラウドを作成するには、次のようにします。

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

これでクラウドが作成されますが、自動的には選択され "_ません_"。

作成したクラウドが不要になった場合は、次のように、[cloud unregister](/cli/azure/cloud#unregister) コマンドで登録解除することができます。

```azurecli
az cloud unregister --name MyCloud
```

