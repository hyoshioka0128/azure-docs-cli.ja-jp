---
title: Azure CLI 2.0 で Azure サービス プリンシパルを使用する
description: Azure CLI 2.0 でサービス プリンシパルを作成および使用する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azure-cli
ms.service: role-based-access-control
ms.openlocfilehash: d250cb2d35a128c789fccd3aca17c47074121a25
ms.sourcegitcommit: 38549f60d76d4b6b65d180367e83749769fe6e43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2018
ms.locfileid: "34703113"
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="be42b-103">Azure CLI 2.0 で Azure サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="be42b-103">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="be42b-104">アクセス制限を使用して個別のログインを作成するには、サービス プリンシパルを使用します。</span><span class="sxs-lookup"><span data-stu-id="be42b-104">If you want to create a separate login with access restrictions, you can do so through a service principal.</span></span> <span data-ttu-id="be42b-105">サービス プリンシパルは、アカウントに関連付けることができる個別の ID です。</span><span class="sxs-lookup"><span data-stu-id="be42b-105">Service principals are separate identities that can be associated with an account.</span></span> <span data-ttu-id="be42b-106">サービス プリンシパルは、自動化する必要があるアプリケーションとタスクを操作するうえで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="be42b-106">Service principals are useful for working with applications and tasks that must be automated.</span></span> <span data-ttu-id="be42b-107">この記事では、サービス プリンシパルを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="be42b-107">This article runs you through the steps for creating a service principal.</span></span>

## <a name="create-the-service-principal"></a><span data-ttu-id="be42b-108">サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="be42b-108">Create the service principal</span></span>

<span data-ttu-id="be42b-109">サービス プリンシパルを作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="be42b-109">Use the [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) command to create a service principal.</span></span> <span data-ttu-id="be42b-110">サービス プリンシパル名は、既存のアプリケーションまたはユーザー名には関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="be42b-110">The Service Principal's name isn't tied to any existing application or user name.</span></span> <span data-ttu-id="be42b-111">任意の認証の種類を使用して、サービス プリンシパルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="be42b-111">You can create a service principal with your choice of authentication type.</span></span>

* <span data-ttu-id="be42b-112">パスワード ベースの認証には `--password` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-112">`--password` is used for password-based authentication.</span></span> <span data-ttu-id="be42b-113">[Azure Active Directory のパスワードの規則と制約事項](/azure/active-directory/active-directory-passwords-policy)に従って、必ず強力なパスワードを作成してください。</span><span class="sxs-lookup"><span data-stu-id="be42b-113">Make sure that you create a strong password by following the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="be42b-114">自分でパスワードを指定しなかった場合、任意のパスワードが自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-114">If you don't specify a password, one is created for you.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD
  ```

* <span data-ttu-id="be42b-115">既存の証明書に対する証明書ベースの認証には、`--cert` が、PEM または DER パブリック文字列、あるいは `@{file}` として使用され、ファイルが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="be42b-115">`--cert` is used for certificate-based authentication for an existing certificate, either as a PEM or DER public string, or `@{file}` to load a file.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile} 
  ```

  <span data-ttu-id="be42b-116">`--keyvault` 引数を追加すると、証明書が Azure Key Vault に格納されていることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="be42b-116">The `--keyvault` argument can be added to indicate the cert is stored in Azure Key Vault.</span></span> <span data-ttu-id="be42b-117">ここでは、`--cert` 値は Key Vault 内の証明書の名前を表します。</span><span class="sxs-lookup"><span data-stu-id="be42b-117">In this case, the `--cert` value refers to the name of the certificate in Key Vault.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
  ```

* <span data-ttu-id="be42b-118">`--create-cert` は、認証用の "_自己署名_" 証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="be42b-118">`--create-cert` creates a _self-signed_ certificate for authentication.</span></span> <span data-ttu-id="be42b-119">`--cert` 引数が指定されていない場合は、ランダムな証明書名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-119">If the `--cert` argument is not provided, a random certificate name is generated.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

  <span data-ttu-id="be42b-120">`--keyvault` 引数を追加すると、証明書を Azure Key Vault に格納できます。</span><span class="sxs-lookup"><span data-stu-id="be42b-120">The `--keyvault` argument can be added to store the certificate in Azure Key Vault.</span></span> <span data-ttu-id="be42b-121">`--keyvault` を使用する場合は、`--cert` 引数も必要です。</span><span class="sxs-lookup"><span data-stu-id="be42b-121">When using `--keyvault`, the `--cert` argument is also required.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
  ```

<span data-ttu-id="be42b-122">認証の種類を示す引数が含まれていない場合は、`--password` が既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-122">If an argument indicating the authentication type isn't included, `--password` is used by default.</span></span>

<span data-ttu-id="be42b-123">`create-for-rbac` コマンドの出力の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="be42b-123">The output of the `create-for-rbac` command is in the following format:</span></span>

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="be42b-124">認証の値として、`appId`、`tenant`、および `password` が使用されています。</span><span class="sxs-lookup"><span data-stu-id="be42b-124">The `appId`, `tenant`, and `password` values are used for authentication.</span></span> <span data-ttu-id="be42b-125">`displayName` は、既存のサービス プリンシパルを検索するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-125">The `displayName` is used when searching for an existing service principal.</span></span>

> [!NOTE]
> <span data-ttu-id="be42b-126">ご利用のアカウントにサービス プリンシパルを作成するための十分なアクセス許可がない場合は、"この操作を完了するのに十分な特権がありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-126">If your account does not have sufficient permissions to create a service principal, you see an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="be42b-127">サービス プリンシパルを作成するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="be42b-127">Contact your Azure Active Directory admin to create a service principal.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="be42b-128">サービス プリンシパル ロールを管理する</span><span class="sxs-lookup"><span data-stu-id="be42b-128">Manage service principal roles</span></span> 

<span data-ttu-id="be42b-129">Azure CLI 2.0 には、ロールの割り当てを管理するために、次のコマンドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="be42b-129">The Azure CLI 2.0 provides the following commands to manage role assignments.</span></span>

* [<span data-ttu-id="be42b-130">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="be42b-130">az role assignment list</span></span>](/cli/azure/role/assignment#az-role-assignment-list)
* [<span data-ttu-id="be42b-131">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="be42b-131">az role assignment create</span></span>](/cli/azure/role/assignment#az-role-assignment-create)
* [<span data-ttu-id="be42b-132">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="be42b-132">az role assignment delete</span></span>](/cli/azure/role/assignment#az-role-assignment-delete)

<span data-ttu-id="be42b-133">サービス プリンシパルの既定のロールは**共同作成者**です。</span><span class="sxs-lookup"><span data-stu-id="be42b-133">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="be42b-134">このロールは、Azure アカウントの読み取りと書き込みを行うための完全なアクセス許可が付与され、通常、アプリケーションには適していません。</span><span class="sxs-lookup"><span data-stu-id="be42b-134">This role has full permissions to read and write to an Azure account, and is usually not appropriate for applications.</span></span> <span data-ttu-id="be42b-135">**閲覧者**ロールは制限が厳しく、読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="be42b-135">The **Reader** role is more restrictive, providing read-only access.</span></span>  <span data-ttu-id="be42b-136">ロールベースのアクセス制御 (RBAC) とロールの詳細については、[RBAC: 組み込みロール](/azure/active-directory/role-based-access-built-in-roles)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="be42b-136">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="be42b-137">この例では、**閲覧者**ロールを追加し、**共同作成者**ロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="be42b-137">This example adds the **Reader** role and deletes the **Contributor** one.</span></span>

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

<span data-ttu-id="be42b-138">ロールを追加しても、以前に割り当てられたアクセス許可は変更され "_ません_"。</span><span class="sxs-lookup"><span data-stu-id="be42b-138">Adding a role does _not_ change any previously assigned permissions.</span></span> <span data-ttu-id="be42b-139">サービス プリンシパルのアクセス許可を制限するときは、__共同作成者__ロールを必ず削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be42b-139">When restricting a service principal's permissions, the __Contributor__ role should always be removed.</span></span>

<span data-ttu-id="be42b-140">変更を確認するには、割り当てられているロールの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="be42b-140">The changes can be verified by listing the assigned roles.</span></span>

```azurecli-interactive
az role assignment list --assignee APP_ID
```

> [!NOTE] 
> <span data-ttu-id="be42b-141">ロールを割り当てるためのアクセス許可がアカウントにない場合は、アカウントに "'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}' のアクションを実行するためのアクセス権限がありません" というエラー メッセージが表示されます。ロールを管理するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="be42b-141">If your account doesn't have the permissions to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'." Contact your Azure Active Directory admin to manage roles.</span></span>

## <a name="log-in-using-the-service-principal"></a><span data-ttu-id="be42b-142">サービス プリンシパルを使ってログインする</span><span class="sxs-lookup"><span data-stu-id="be42b-142">Log in using the service principal</span></span>

<span data-ttu-id="be42b-143">新しいサービス プリンシパルのログインとアクセス許可をテストするには、Azure CLI 内でそのサービス プリンシパルとしてログインします。</span><span class="sxs-lookup"><span data-stu-id="be42b-143">You can test the new service principal's login and permissions by logging in under it within the Azure CLI.</span></span> <span data-ttu-id="be42b-144">新しいサービス プリンシパルには、`appId`、`tenant`、および資格情報の値を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="be42b-144">Log in as the new service principal using the `appId`, `tenant`, and credentials values.</span></span> <span data-ttu-id="be42b-145">指定する認証情報は、サービス プリンシパルの作成にパスワードまたは証明書のどちらを使用したかに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="be42b-145">The authentication information you provide changes based on whether you chose to create the service principal with a password, or a certificate.</span></span>

<span data-ttu-id="be42b-146">パスワードでログインをするには、そのパスワードを引数パラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="be42b-146">To log in with a password, provide it as an argument parameter.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

<span data-ttu-id="be42b-147">証明書でログインする場合、その証明書は、PEM または DER ファイルとしてローカルで使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="be42b-147">To log in with a certificate, it must be available locally as a PEM or DER file.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```

## <a name="reset-credentials"></a><span data-ttu-id="be42b-148">資格情報をリセットする</span><span class="sxs-lookup"><span data-stu-id="be42b-148">Reset credentials</span></span>

<span data-ttu-id="be42b-149">サービス プリンシパルの資格情報を忘れた場合、その情報は、[az ad sp reset-credentials](https://docs.microsoft.com/en-us/cli/azure/ad/sp#az-ad-sp-reset-credentials) コマンドでリセットできます。</span><span class="sxs-lookup"><span data-stu-id="be42b-149">In the event that you forget the credentials for a service principal, they can be reset with the [az ad sp reset-credentials](https://docs.microsoft.com/en-us/cli/azure/ad/sp#az-ad-sp-reset-credentials) command.</span></span> <span data-ttu-id="be42b-150">新しいサービス プリンシパルを作成するときの制限事項とオプションと同じものが、ここでも適用されます。</span><span class="sxs-lookup"><span data-stu-id="be42b-150">The same restrictions and options for creating a new service principal also apply here.</span></span>

```azurecli-interactive
az ad sp reset-credentials --name APP_ID --password NEW_PASSWORD
```
