---
title: Azure CLI で Azure サービス プリンシパルを使用する
description: Azure CLI でサービス プリンシパルを作成および使用する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 6cce8fb47dd2b57180487441055333343fff8330
ms.sourcegitcommit: 614811ea63ceb0e71bd99323846dc1b754e15255
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2018
ms.locfileid: "53805875"
---
# <a name="create-an-azure-service-principal-with-azure-cli"></a>Azure CLI で Azure サービス プリンシパルを作成する

アクセス制限を使用して個別のサインインを作成する場合は、サービス プリンシパルを使用してこれを行います。 サービス プリンシパルは、アカウントに関連付けることができる個別の ID です。 サービス プリンシパルは、自動化する必要があるアプリケーションとタスクを操作するうえで役に立ちます。 この記事では、サービス プリンシパルを作成する手順について説明します。

## <a name="create-the-service-principal"></a>サービス プリンシパルを作成する

サービス プリンシパルを作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) コマンドを使用します。 サービス プリンシパル名は、既存のアプリケーションまたはユーザー名には関連付けられていません。 任意の認証の種類を使用して、サービス プリンシパルを作成できます。

* パスワード ベースの認証には `--password` が使用されます。 認証の種類を示す引数が含まれていない場合は、--password が既定で使用され、パスワードが自動的に作成されます。 パスワード ベースの認証を使用する場合は、このコマンドを使用することをお勧めします。そうすれば、パスワードが自動的に作成されます。  

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName 
  ```
  パスワードを自動的に作成するのではなく、選択する場合は (セキュリティ上の理由から推奨されません)、次のコマンドを使用します。 [Azure Active Directory のパスワードの規則と制約事項](/azure/active-directory/active-directory-passwords-policy)に従って、必ず強力なパスワードを作成してください。 パスワードを選択するオプションでは、脆弱なパスワードが選択されたり、パスワードが再利用されたりする可能性があります。 このオプションは、Azure CLI の今後バージョンで非推奨になる予定です。 

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --password <Choose a strong password>
  ```

* 既存の証明書に対する証明書ベースの認証には、`--cert` が、PEM または DER パブリック文字列、あるいは `@{file}` として使用され、ファイルが読み込まれます。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile}
  ```

  `--keyvault` 引数を追加すると、証明書が Azure Key Vault に格納されていることを指定できます。 ここでは、`--cert` 値は Key Vault 内の証明書の名前を表します。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
  ```

* `--create-cert` は、認証用の "_自己署名_" 証明書を作成します。 `--cert` 引数が指定されていない場合は、ランダムな証明書名が生成されます。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

  `--keyvault` 引数を追加すると、証明書を Azure Key Vault に格納できます。 `--keyvault` を使用する場合は、`--cert` 引数も必要です。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
  ```

認証の種類を示す引数が含まれていない場合は、`--password` が既定で使用されます。

`create-for-rbac` コマンドの JSON 出力の形式は次のとおりです。

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

認証の値として、`appId`、`tenant`、および `password` が使用されています。 `displayName` は、既存のサービス プリンシパルを検索するときに使用されます。

> [!NOTE]
> ご利用のアカウントにサービス プリンシパルを作成するための十分なアクセス許可がない場合は、"この操作を完了するのに十分な特権がありません" というエラー メッセージが表示されます。 サービス プリンシパルを作成するには、Azure Active Directory 管理者にお問い合わせください。

## <a name="manage-service-principal-roles"></a>サービス プリンシパル ロールを管理する

Azure CLI には、ロールの割り当てを管理するために、次のコマンドが用意されています。

* [az role assignment list](/cli/azure/role/assignment#az-role-assignment-list)
* [az role assignment create](/cli/azure/role/assignment#az-role-assignment-create)
* [az role assignment delete](/cli/azure/role/assignment#az-role-assignment-delete)

サービス プリンシパルの既定のロールは**共同作成者**です。 このロールは、Azure アカウントの読み取りと書き込みを行うための完全なアクセス許可が付与されるため、アプリケーションには適していません。 **閲覧者**ロールは制限が厳しく、読み取り専用アクセスを提供します。  ロールベースのアクセス制御 (RBAC) とロールの詳細については、[RBAC の組み込みのロール](/azure/active-directory/role-based-access-built-in-roles)に関するページをご覧ください。

この例では、**閲覧者**ロールを追加し、**共同作成者**ロールを削除します。

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

ロールを追加しても、以前に割り当てられたアクセス許可は変更され "_ません_"。 サービス プリンシパルのアクセス許可を制限するときは、__共同作成者__ロールを必ず削除する必要があります。

変更を確認するには、割り当てられているロールの一覧を表示します。

```azurecli-interactive
az role assignment list --assignee APP_ID
```

> [!NOTE]
> ロールを割り当てるためのアクセス許可がアカウントにない場合は、アカウントに "'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}' のアクションを実行するためのアクセス権限がありません" というエラー メッセージが表示されます。ロールを管理するには、Azure Active Directory 管理者にお問い合わせください。

## <a name="sign-in-using-the-service-principal"></a>サービス プリンシパルを使ってサインインする

新しいサービス プリンシパルの資格情報とアクセス許可をテストするには、Azure CLI 内でそのサービス プリンシパルとしてサインインします。 新しいサービス プリンシパルには、`appId`、`tenant`、および資格情報の値を使用してサインインします。 サービス プリンシパルの作成に使用した認証の種類を使用します。

パスワードでサインインするには、そのパスワードを引数パラメーターとして指定します。

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

証明書でサインインする場合、その証明書は、PEM または DER ファイルとしてローカルで使用できる必要があります。

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```

## <a name="reset-credentials"></a>資格情報をリセットする

サービス プリンシパルの資格情報を忘れた場合、その情報は、[az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) コマンドでリセットできます。 新しいサービス プリンシパルを作成するときの制限事項とオプションと同じものが、ここでも適用されます。

```azurecli-interactive
az ad sp credential reset --name APP_ID 
```
