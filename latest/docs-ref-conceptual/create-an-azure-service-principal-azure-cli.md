---
title: "Azure CLI 2.0 で Azure サービス プリンシパルを作成する"
description: "Azure CLI 2.0 でアプリまたはサービスのサービス プリンシパルを作成する方法について説明します。"
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 10/12/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: 5ae8af014b821fe5297ea44056ef33c4570d1d47
ms.sourcegitcommit: 5cfbea569fef193044da712708bc6957d3fb557c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>Azure CLI 2.0 で Azure サービス プリンシパルを作成する

Azure CLI 2.0 を使ってアプリまたはサービスを管理する場合、その実行には、自分の資格情報ではなく、Azure Active Directory (AAD) のサービス プリンシパルを使用する必要があります。
このトピックでは、Azure CLI 2.0 でセキュリティ プリンシパルを作成する手順を紹介します。

> [!NOTE]
> Azure Portal からサービス プリンシパルを作成することもできます。
> 詳細については、「[リソースにアクセスできる Azure Active Directory アプリケーションとサービス プリンシパルをポータルで作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal)」を参照してください。

## <a name="what-is-a-service-principal"></a>"サービス プリンシパル" とは

Azure サービス プリンシパルは、ユーザーによって作成されたアプリ、サービス、およびオートメーション ツールが特定の Azure リソースにアクセスする際に使用するセキュリティ ID です。 特定のロールが割り当てられ、リソースへのアクセス許可が厳しく管理された "ユーザー ID" (ログインとパスワードまたは証明書) と考えてください。 一般的なユーザー ID とは異なり、サービス プリンシパルには求められるのは、限られた目的を遂行する能力だけです。 管理タスクを実行するために必要な最小限のアクセス許可レベルだけを与えるようにすれば、セキュリティは向上します。 

Azure CLI 2.0 では、パスワードベースの認証資格情報と証明書資格情報の作成がサポートされています。 このトピックでは、両方の種類の資格情報について説明します。

## <a name="verify-your-own-permission-level"></a>自分のアクセス許可レベルの確認

まず、Azure Active Directory と Azure サブスクリプションの両方で適切なアクセス許可を持っている必要があります。 具体的には、Active Directory でアプリケーションを作成し、サービス プリンシパルにロールを割り当てることができる必要があります。 

自分のアカウントに適切なアクセス許可があるかどうかを確認する最も簡単な方法は、ポータルを使用することです。 [ポータルでの必要なアクセス許可のチェック](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)に関するページをご覧ください。

## <a name="create-a-service-principal-for-your-application"></a>アプリケーションのサービス プリンシパルを作成する

作成するサービス プリンシパルの対象アプリを識別するために、次のいずれかが必要です。

  * デプロイされているアプリの一意の名前または URI (例の "MyDemoWebApp" など)
  * アプリケーション ID (デプロイされているアプリ、サービス、またはオブジェクトに関連付けられている一意の GUID)

これらの値は、サービス プリンシパルの作成時にアプリケーションを識別します。

### <a name="get-information-about-your-application"></a>アプリケーションに関する情報を取得する

アプリケーションに関する ID 情報は、`az ad app list` で取得します。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

```azurecli-interactive
az ad app list --display-name MyDemoWebApp
```

```json
{
    "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "appPermissions": null,
    "availableToOtherTenants": false,
    "displayName": "MyDemoWebApp",
    "homepage": "http://MyDemoWebApp.azurewebsites.net",
    "identifierUris": [
      "http://MyDemoWebApp"
    ],
    "objectId": "bd07205b-629f-4a2e-945e-1ee5dadf610b9",
    "objectType": "Application",
    "replyUrls": []
  }
```

`--display-name` オプションを使用すると、返されたアプリの一覧がフィルター処理され、`displayName` が MyDemoWebApp で始まるアプリが表示します。

### <a name="create-a-service-principal-with-a-password"></a>パスワードを使用したサービス プリンシパルの作成

パスワードを使用してサービス プリンシパルを作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に加えて `--password` パラメーターを使用します。 ロールまたはスコープを指定しない場合、既定値は、現在のサブスクリプションの**共同作成者**ロールになります。 `--password` または `--cert` パラメーターを使用せずにサービス プリンシパルを作成すると、パスワード認証が使用され、パスワードが生成されます。

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --password "{strong password}" 
``` 

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "name": "http://MyDemoWebApp",
  "password": {strong password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

 > [!WARNING] 
 > 安全でないパスワードを作成しないでください。  [Azure AD のパスワードの規則と制限](/azure/active-directory/active-directory-passwords-policy)に関するガイダンスに従ってください。

### <a name="create-a-service-principal-with-a-self-signed-certificate"></a>自己署名証明書を使用したサービス プリンシパルの作成

自己署名証明書を作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に加えて `--create-cert` パラメーターを使用します。

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --create-cert
```

```json
{
  "appId": "c495db57-82e0-4e2e-9369-069dff176858",
  "displayName": "azure-cli-2017-10-12-22-15-38",
  "fileWithCertAndPrivateKey": "<path>/<file-name>.pem",
  "name": "http://MyDemoWebApp",
  "password": null,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

`fileWithCertAndPrivateKey` 応答の値をコピーします。 これは、認証に使用される証明書ファイルです。

証明書を使用する際のその他のオプションについては、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に関するページを参照してください。

### <a name="get-information-about-the-service-principal"></a>サービス プリンシパルに関する情報を取得する

```azurecli-interactive
az ad sp show --id a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "objectId": "0ceae62e-1a1a-446f-aa56-2300d176659bde",
  "objectType": "ServicePrincipal",
  "servicePrincipalNames": [
    "http://MyDemoWebApp",
    "a487e0c1-82af-47d9-9a0b-af184eb87646d"
  ]
}
```

### <a name="sign-in-using-the-service-principal"></a>サービス プリンシパルを使ってサインインする

`az ad sp show` の *appId* と、"*パスワード*" または作成した証明書のパスを使用して、アプリの新しいサービス プリンシパルとしてログインできるようになりました。  *tenant* 値に `az ad sp create-for-rbac` の結果を指定します。

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password-or-path-to-cert} --tenant {tenant}
``` 

サインインに成功すると、次の出力が表示されます。

```json
[
  {
    "cloudName": "AzureCloud",
    "id": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "isDefault": true,
    "state": "Enabled",
    "tenantId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "user": {
      "name": "https://MyDemoWebApp",
      "type": "servicePrincipal"
    }
  }
]
```

アプリを実行するための資格情報として、`id`、`password`、`tenant` の値を使用します。 

## <a name="managing-roles"></a>ロールを管理する 

> [!NOTE]
> Azure のロールベースのアクセス制御 (RBAC) は、ユーザー プリンシパルとサービス プリンシパルのロールを定義して管理するためのモデルです。
> ロールに関連付けられる一連のアクセス許可によって、プリンシパルが各種の操作 (読み取り、アクセス、書き込み、または管理) を実行できるリソースが決まります。
> RBAC とロールの詳細については、[RBAC の組み込みロール](/azure/active-directory/role-based-access-built-in-roles)に関するページを参照してください。

Azure CLI 2.0 には、ロールの割り当てを管理するために、次のコマンドが用意されています。

* [az role assignment list](/cli/azure/role/assignment#list)
* [az role assignment create](/cli/azure/role/assignment#create)
* [az role assignment delete](/cli/azure/role/assignment#delete)

サービス プリンシパルの既定のロールは、**Contributor** です。 このロールは、広範なアクセス許可が与えられているため、アプリと Azure サービスとの対話用には最適でない場合があります。 **Reader** ロールは、より制限が厳しく、読み取り専用のアクセスに適しています。 Azure Portal では、ロールごとのアクセス許可に関する詳しい情報を確認したり、カスタム ロールを作成したりすることができます。

次の例では、先ほどの例に **Reader** ロールを追加し、**Contributor** ロールを削除しています。

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

変更を確認するには、現在割り当てられているロールを一覧表示します。

```azurecli-interactive
az role assignment list --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
    "id": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleAssignments/c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "name": "c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "properties": {
      "principalId": "790525226-46f9-4051-b439-7079e41dfa31",
      "principalName": "http://MyDemoWebApp",
      "roleDefinitionId": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7",
      "roleDefinitionName": "Reader",
      "scope": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac"
    },
    "type": "Microsoft.Authorization/roleAssignments"
}
```

> [!NOTE] 
> ロールを割り当てることのできるアクセス許可がアカウントに設定されていない場合は、エラー メッセージが表示されます。
> このメッセージは、アカウントで、スコープ "/subscriptions/{guid} に対するアクション Microsoft.Authorization/roleAssignments/write の実行が承認されていない" ことを示しています。
   
## <a name="change-the-credentials-of-a-security-principal"></a>セキュリティ プリンシパルの資格情報を変更する

セキュリティ上、アクセス許可の確認とパスワードの更新を定期的に行うことが大切です。 アプリの変更に合わせて、セキュリティ資格情報を管理したり変更したりする場合もあります。

### <a name="reset-a-service-principal-password"></a>サービス プリンシパルのパスワードをリセットする

サービス プリンシパルの現在のパスワードをリセットするには、`az ad sp reset-credentials` を使用します。

```azurecli-interactive
az ad sp reset-credentials --name 20bce7de-3cd7-49f4-ab64-bb5b443838c3 --password {new-password}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "name": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "password": {new-password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

`--password` オプションを指定しなかった場合は、CLI によって安全なパスワードが生成されます。
