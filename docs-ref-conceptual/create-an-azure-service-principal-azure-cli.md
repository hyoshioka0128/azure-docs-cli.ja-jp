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
# <a name="create-an-azure-service-principal-with-azure-cli"></a><span data-ttu-id="546a9-103">Azure CLI で Azure サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="546a9-103">Create an Azure service principal with Azure CLI</span></span>

<span data-ttu-id="546a9-104">アクセス制限を使用して個別のサインインを作成する場合は、サービス プリンシパルを使用してこれを行います。</span><span class="sxs-lookup"><span data-stu-id="546a9-104">If you want to create a separate sign-in with access restrictions, you can do so through a service principal.</span></span> <span data-ttu-id="546a9-105">サービス プリンシパルは、アカウントに関連付けることができる個別の ID です。</span><span class="sxs-lookup"><span data-stu-id="546a9-105">Service principals are separate identities that can be associated with an account.</span></span> <span data-ttu-id="546a9-106">サービス プリンシパルは、自動化する必要があるアプリケーションとタスクを操作するうえで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="546a9-106">Service principals are useful for working with applications and tasks that must be automated.</span></span> <span data-ttu-id="546a9-107">この記事では、サービス プリンシパルを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="546a9-107">This article runs you through the steps for creating a service principal.</span></span>

## <a name="create-the-service-principal"></a><span data-ttu-id="546a9-108">サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="546a9-108">Create the service principal</span></span>

<span data-ttu-id="546a9-109">サービス プリンシパルを作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="546a9-109">Use the [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) command to create a service principal.</span></span> <span data-ttu-id="546a9-110">サービス プリンシパル名は、既存のアプリケーションまたはユーザー名には関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="546a9-110">The Service Principal's name isn't tied to any existing application or user name.</span></span> <span data-ttu-id="546a9-111">任意の認証の種類を使用して、サービス プリンシパルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="546a9-111">You can create a service principal with your choice of authentication type.</span></span>

* <span data-ttu-id="546a9-112">パスワード ベースの認証には `--password` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-112">`--password` is used for password-based authentication.</span></span> <span data-ttu-id="546a9-113">認証の種類を示す引数が含まれていない場合は、--password が既定で使用され、パスワードが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-113">If an argument indicating the authentication type isn't included, --password is used by default, and one is created for you.</span></span> <span data-ttu-id="546a9-114">パスワード ベースの認証を使用する場合は、このコマンドを使用することをお勧めします。そうすれば、パスワードが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-114">If you want to use password-based authentication, we recommend using this command, so the password is created for you.</span></span>  

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName 
  ```
  <span data-ttu-id="546a9-115">パスワードを自動的に作成するのではなく、選択する場合は (セキュリティ上の理由から推奨されません)、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="546a9-115">If you want to choose the password, instead of it being created for you (which is not recommended, for security reasons), you can use this command.</span></span> <span data-ttu-id="546a9-116">[Azure Active Directory のパスワードの規則と制約事項](/azure/active-directory/active-directory-passwords-policy)に従って、必ず強力なパスワードを作成してください。</span><span class="sxs-lookup"><span data-stu-id="546a9-116">Make sure that you create a strong password by following the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="546a9-117">パスワードを選択するオプションでは、脆弱なパスワードが選択されたり、パスワードが再利用されたりする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="546a9-117">The option to choose password leaves the chance of a weak password being chosen or password being re-used.</span></span> <span data-ttu-id="546a9-118">このオプションは、Azure CLI の今後バージョンで非推奨になる予定です。</span><span class="sxs-lookup"><span data-stu-id="546a9-118">This option is planned to be deprecated in a future version of Azure CLI.</span></span> 

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --password <Choose a strong password>
  ```

* <span data-ttu-id="546a9-119">既存の証明書に対する証明書ベースの認証には、`--cert` が、PEM または DER パブリック文字列、あるいは `@{file}` として使用され、ファイルが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="546a9-119">`--cert` is used for certificate-based authentication for an existing certificate, either as a PEM or DER public string, or `@{file}` to load a file.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile}
  ```

  <span data-ttu-id="546a9-120">`--keyvault` 引数を追加すると、証明書が Azure Key Vault に格納されていることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="546a9-120">The `--keyvault` argument can be added to indicate the cert is stored in Azure Key Vault.</span></span> <span data-ttu-id="546a9-121">ここでは、`--cert` 値は Key Vault 内の証明書の名前を表します。</span><span class="sxs-lookup"><span data-stu-id="546a9-121">In this case, the `--cert` value refers to the name of the certificate in Key Vault.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
  ```

* <span data-ttu-id="546a9-122">`--create-cert` は、認証用の "_自己署名_" 証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="546a9-122">`--create-cert` creates a _self-signed_ certificate for authentication.</span></span> <span data-ttu-id="546a9-123">`--cert` 引数が指定されていない場合は、ランダムな証明書名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-123">If the `--cert` argument isn't provided, a random certificate name is generated.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

  <span data-ttu-id="546a9-124">`--keyvault` 引数を追加すると、証明書を Azure Key Vault に格納できます。</span><span class="sxs-lookup"><span data-stu-id="546a9-124">The `--keyvault` argument can be added to store the certificate in Azure Key Vault.</span></span> <span data-ttu-id="546a9-125">`--keyvault` を使用する場合は、`--cert` 引数も必要です。</span><span class="sxs-lookup"><span data-stu-id="546a9-125">When using `--keyvault`, the `--cert` argument is also required.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
  ```

<span data-ttu-id="546a9-126">認証の種類を示す引数が含まれていない場合は、`--password` が既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-126">If an argument indicating the authentication type isn't included, `--password` is used by default.</span></span>

<span data-ttu-id="546a9-127">`create-for-rbac` コマンドの JSON 出力の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="546a9-127">The JSON output of the `create-for-rbac` command is in the following format:</span></span>

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="546a9-128">認証の値として、`appId`、`tenant`、および `password` が使用されています。</span><span class="sxs-lookup"><span data-stu-id="546a9-128">The `appId`, `tenant`, and `password` values are used for authentication.</span></span> <span data-ttu-id="546a9-129">`displayName` は、既存のサービス プリンシパルを検索するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-129">The `displayName` is used when searching for an existing service principal.</span></span>

> [!NOTE]
> <span data-ttu-id="546a9-130">ご利用のアカウントにサービス プリンシパルを作成するための十分なアクセス許可がない場合は、"この操作を完了するのに十分な特権がありません" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-130">If your account does not have sufficient permissions to create a service principal, you see an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="546a9-131">サービス プリンシパルを作成するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="546a9-131">Contact your Azure Active Directory admin to create a service principal.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="546a9-132">サービス プリンシパル ロールを管理する</span><span class="sxs-lookup"><span data-stu-id="546a9-132">Manage service principal roles</span></span>

<span data-ttu-id="546a9-133">Azure CLI には、ロールの割り当てを管理するために、次のコマンドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="546a9-133">The Azure CLI provides the following commands to manage role assignments.</span></span>

* [<span data-ttu-id="546a9-134">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="546a9-134">az role assignment list</span></span>](/cli/azure/role/assignment#az-role-assignment-list)
* [<span data-ttu-id="546a9-135">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="546a9-135">az role assignment create</span></span>](/cli/azure/role/assignment#az-role-assignment-create)
* [<span data-ttu-id="546a9-136">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="546a9-136">az role assignment delete</span></span>](/cli/azure/role/assignment#az-role-assignment-delete)

<span data-ttu-id="546a9-137">サービス プリンシパルの既定のロールは**共同作成者**です。</span><span class="sxs-lookup"><span data-stu-id="546a9-137">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="546a9-138">このロールは、Azure アカウントの読み取りと書き込みを行うための完全なアクセス許可が付与されるため、アプリケーションには適していません。</span><span class="sxs-lookup"><span data-stu-id="546a9-138">This role has full permissions to read and write to an Azure account, and is not appropriate for applications.</span></span> <span data-ttu-id="546a9-139">**閲覧者**ロールは制限が厳しく、読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="546a9-139">The **Reader** role is more restrictive, providing read-only access.</span></span>  <span data-ttu-id="546a9-140">ロールベースのアクセス制御 (RBAC) とロールの詳細については、[RBAC の組み込みのロール](/azure/active-directory/role-based-access-built-in-roles)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="546a9-140">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="546a9-141">この例では、**閲覧者**ロールを追加し、**共同作成者**ロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="546a9-141">This example adds the **Reader** role and deletes the **Contributor** one.</span></span>

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

<span data-ttu-id="546a9-142">ロールを追加しても、以前に割り当てられたアクセス許可は変更され "_ません_"。</span><span class="sxs-lookup"><span data-stu-id="546a9-142">Adding a role does _not_ change any previously assigned permissions.</span></span> <span data-ttu-id="546a9-143">サービス プリンシパルのアクセス許可を制限するときは、__共同作成者__ロールを必ず削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="546a9-143">When restricting a service principal's permissions, the __Contributor__ role should always be removed.</span></span>

<span data-ttu-id="546a9-144">変更を確認するには、割り当てられているロールの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="546a9-144">The changes can be verified by listing the assigned roles.</span></span>

```azurecli-interactive
az role assignment list --assignee APP_ID
```

> [!NOTE]
> <span data-ttu-id="546a9-145">ロールを割り当てるためのアクセス許可がアカウントにない場合は、アカウントに "'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}' のアクションを実行するためのアクセス権限がありません" というエラー メッセージが表示されます。ロールを管理するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="546a9-145">If your account doesn't have the permissions to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'." Contact your Azure Active Directory admin to manage roles.</span></span>

## <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="546a9-146">サービス プリンシパルを使ってサインインする</span><span class="sxs-lookup"><span data-stu-id="546a9-146">Sign in using the service principal</span></span>

<span data-ttu-id="546a9-147">新しいサービス プリンシパルの資格情報とアクセス許可をテストするには、Azure CLI 内でそのサービス プリンシパルとしてサインインします。</span><span class="sxs-lookup"><span data-stu-id="546a9-147">You can test the new service principal's credentials and permissions by signing in under it within the Azure CLI.</span></span> <span data-ttu-id="546a9-148">新しいサービス プリンシパルには、`appId`、`tenant`、および資格情報の値を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="546a9-148">Sign in as the new service principal using the `appId`, `tenant`, and credentials values.</span></span> <span data-ttu-id="546a9-149">サービス プリンシパルの作成に使用した認証の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="546a9-149">Use the authentication type that the service principal was created with.</span></span>

<span data-ttu-id="546a9-150">パスワードでサインインするには、そのパスワードを引数パラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="546a9-150">To sign in with a password, provide it as an argument parameter.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

<span data-ttu-id="546a9-151">証明書でサインインする場合、その証明書は、PEM または DER ファイルとしてローカルで使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="546a9-151">To sign in with a certificate, it must be available locally as a PEM or DER file.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```

## <a name="reset-credentials"></a><span data-ttu-id="546a9-152">資格情報をリセットする</span><span class="sxs-lookup"><span data-stu-id="546a9-152">Reset credentials</span></span>

<span data-ttu-id="546a9-153">サービス プリンシパルの資格情報を忘れた場合、その情報は、[az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) コマンドでリセットできます。</span><span class="sxs-lookup"><span data-stu-id="546a9-153">In the event that you forget the credentials for a service principal, they can be reset with the [az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) command.</span></span> <span data-ttu-id="546a9-154">新しいサービス プリンシパルを作成するときの制限事項とオプションと同じものが、ここでも適用されます。</span><span class="sxs-lookup"><span data-stu-id="546a9-154">The same restrictions and options for creating a new service principal also apply here.</span></span>

```azurecli-interactive
az ad sp credential reset --name APP_ID 
```
