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
ms.openlocfilehash: a6ad5611f3e507b65e160122c87e22ec44546588
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="4b3ae-104">Azure CLI 2.0 で Azure サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-104">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="4b3ae-105">Azure CLI 2.0 を使ってアプリまたはサービスを管理する場合、その実行には、自分の資格情報ではなく、Azure Active Directory (AAD) のサービス プリンシパルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-105">If you plan to manage your app or service with Azure CLI 2.0, you should run it under an Azure Active Directory (AAD) service principal rather than your own credentials.</span></span>
<span data-ttu-id="4b3ae-106">このトピックでは、Azure CLI 2.0 でセキュリティ プリンシパルを作成する手順を紹介します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-106">This topic steps you through creating a security principal with Azure CLI 2.0.</span></span>

> [!NOTE]
> <span data-ttu-id="4b3ae-107">Azure Portal からサービス プリンシパルを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-107">You can also create a service principal through the Azure portal.</span></span>
> <span data-ttu-id="4b3ae-108">詳細については、「[リソースにアクセスできる Azure Active Directory アプリケーションとサービス プリンシパルをポータルで作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="4b3ae-109">"サービス プリンシパル" とは</span><span class="sxs-lookup"><span data-stu-id="4b3ae-109">What is a 'service principal'?</span></span>

<span data-ttu-id="4b3ae-110">Azure サービス プリンシパルは、ユーザーによって作成されたアプリ、サービス、およびオートメーション ツールが特定の Azure リソースにアクセスする際に使用するセキュリティ ID です。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="4b3ae-111">特定のロールが割り当てられ、リソースへのアクセス許可が厳しく管理された "ユーザー ID" (ログインとパスワードまたは証明書) と考えてください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-111">Think of it as a 'user identity' (login and password or certificate) with a specific role, and tightly controlled permissions to access your resources.</span></span> <span data-ttu-id="4b3ae-112">一般的なユーザー ID とは異なり、サービス プリンシパルには求められるのは、限られた目的を遂行する能力だけです。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="4b3ae-113">管理タスクを実行するために必要な最小限のアクセス許可レベルだけを与えるようにすれば、セキュリティは向上します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span> 

<span data-ttu-id="4b3ae-114">Azure CLI 2.0 では、パスワードベースの認証資格情報と証明書資格情報の作成がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-114">Azure CLI 2.0 supports the creation of password-based authentication credentials and certificate credentials.</span></span> <span data-ttu-id="4b3ae-115">このトピックでは、両方の種類の資格情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-115">In this topic, we cover both types of credentials.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="4b3ae-116">自分のアクセス許可レベルの確認</span><span class="sxs-lookup"><span data-stu-id="4b3ae-116">Verify your own permission level</span></span>

<span data-ttu-id="4b3ae-117">まず、Azure Active Directory と Azure サブスクリプションの両方で適切なアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-117">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="4b3ae-118">具体的には、Active Directory でアプリケーションを作成し、サービス プリンシパルにロールを割り当てることができる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-118">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span> 

<span data-ttu-id="4b3ae-119">自分のアカウントに適切なアクセス許可があるかどうかを確認する最も簡単な方法は、ポータルを使用することです。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-119">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="4b3ae-120">[ポータルでの必要なアクセス許可のチェック](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-120">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="4b3ae-121">アプリケーションのサービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-121">Create a service principal for your application</span></span>

<span data-ttu-id="4b3ae-122">作成するサービス プリンシパルの対象アプリを識別するために、次のいずれかが必要です。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-122">You must have one of the following to identify the app you want to create a service principal for:</span></span>

  * <span data-ttu-id="4b3ae-123">デプロイされているアプリの一意の名前または URI (例の "MyDemoWebApp" など)</span><span class="sxs-lookup"><span data-stu-id="4b3ae-123">The unique name or URI of your deployed app (such as "MyDemoWebApp" in the examples), or</span></span>
  * <span data-ttu-id="4b3ae-124">アプリケーション ID (デプロイされているアプリ、サービス、またはオブジェクトに関連付けられている一意の GUID)</span><span class="sxs-lookup"><span data-stu-id="4b3ae-124">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

<span data-ttu-id="4b3ae-125">これらの値は、サービス プリンシパルの作成時にアプリケーションを識別します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-125">These values identify your application when creating a service principal.</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="4b3ae-126">アプリケーションに関する情報を取得する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-126">Get information about your application</span></span>

<span data-ttu-id="4b3ae-127">アプリケーションに関する ID 情報は、`az ad app list` で取得します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-127">Get identity information about your application with the `az ad app list`.</span></span>

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

<span data-ttu-id="4b3ae-128">`--display-name` オプションを使用すると、返されたアプリの一覧がフィルター処理され、`displayName` が MyDemoWebApp で始まるアプリが表示します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-128">The `--display-name` option filters the returned list of apps to show those with `displayName` starting with MyDemoWebApp.</span></span>

### <a name="create-a-service-principal-with-a-password"></a><span data-ttu-id="4b3ae-129">パスワードを使用したサービス プリンシパルの作成</span><span class="sxs-lookup"><span data-stu-id="4b3ae-129">Create a service principal with a password</span></span>

<span data-ttu-id="4b3ae-130">パスワードを使用してサービス プリンシパルを作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に加えて `--password` パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-130">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) and the `--password` parameter to create the service principal with a password.</span></span> <span data-ttu-id="4b3ae-131">ロールまたはスコープを指定しない場合、既定値は、現在のサブスクリプションの **Contributor** ロールになります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-131">When you do not provide a role or scope, it defaults to the **Contributor** role for the current subscription.</span></span> <span data-ttu-id="4b3ae-132">`--password` または `--cert` パラメーターを使用せずにサービス プリンシパルを作成すると、パスワード認証が使用され、パスワードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-132">If you create a service principal without using either the `--password` or `--cert` parameter, password authentication is used and a password is generated for you.</span></span>

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
 > <span data-ttu-id="4b3ae-133">安全でないパスワードを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-133">Don't create an insecure password.</span></span>  <span data-ttu-id="4b3ae-134">[Azure AD のパスワードの規則と制限](/azure/active-directory/active-directory-passwords-policy)に関するガイダンスに従ってください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-134">Follow the [Azure AD password rules and restrictions](/azure/active-directory/active-directory-passwords-policy) guidance.</span></span>

### <a name="create-a-service-principal-with-a-self-signed-certificate"></a><span data-ttu-id="4b3ae-135">自己署名証明書を使用したサービス プリンシパルの作成</span><span class="sxs-lookup"><span data-stu-id="4b3ae-135">Create a service principal with a self-signed certificate</span></span>

<span data-ttu-id="4b3ae-136">自己署名証明書を作成するには、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に加えて `--create-cert` パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-136">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) and the `--create-cert` parameter to create a self-signed certificate.</span></span>

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

<span data-ttu-id="4b3ae-137">`fileWithCertAndPrivateKey` 応答の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-137">Copy the value of the `fileWithCertAndPrivateKey` response.</span></span> <span data-ttu-id="4b3ae-138">これは、認証に使用される証明書ファイルです。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-138">This is the certificate file which will be used for authentication.</span></span>

<span data-ttu-id="4b3ae-139">証明書を使用する際のその他のオプションについては、[az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-139">For more options when using certificates, see [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac).</span></span>

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="4b3ae-140">サービス プリンシパルに関する情報を取得する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-140">Get information about the service principal</span></span>

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

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="4b3ae-141">サービス プリンシパルを使ってサインインする</span><span class="sxs-lookup"><span data-stu-id="4b3ae-141">Sign in using the service principal</span></span>

<span data-ttu-id="4b3ae-142">`az ad sp show` の *appId* と、"*パスワード*" または作成した証明書のパスを使用して、アプリの新しいサービス プリンシパルとしてログインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-142">You can now log in as the new service principal for your app using the *appId* from `az ad sp show`, and either the *password* or the path to the created certificate.</span></span>  <span data-ttu-id="4b3ae-143">*tenant* 値に `az ad sp create-for-rbac` の結果を指定します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-143">Supply the *tenant* value from the results of `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password-or-path-to-cert} --tenant {tenant}
``` 

<span data-ttu-id="4b3ae-144">サインインに成功すると、次の出力が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-144">You will see this output after a successful sign-on:</span></span>

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

<span data-ttu-id="4b3ae-145">アプリを実行するための資格情報として、`id`、`password`、`tenant` の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-145">Use the `id`, `password`, and `tenant` values as the credentials for running your app.</span></span> 

## <a name="managing-roles"></a><span data-ttu-id="4b3ae-146">ロールを管理する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-146">Managing roles</span></span> 

> [!NOTE]
> <span data-ttu-id="4b3ae-147">Azure のロールベースのアクセス制御 (RBAC) は、ユーザー プリンシパルとサービス プリンシパルのロールを定義して管理するためのモデルです。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-147">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span>
> <span data-ttu-id="4b3ae-148">ロールに関連付けられる一連のアクセス許可によって、プリンシパルが各種の操作 (読み取り、アクセス、書き込み、または管理) を実行できるリソースが決まります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-148">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span>
> <span data-ttu-id="4b3ae-149">RBAC とロールの詳細については、[RBAC の組み込みロール](/azure/active-directory/role-based-access-built-in-roles)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-149">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="4b3ae-150">Azure CLI 2.0 には、ロールの割り当てを管理するために、次のコマンドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-150">The Azure CLI 2.0 provides the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="4b3ae-151">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="4b3ae-151">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="4b3ae-152">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="4b3ae-152">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="4b3ae-153">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="4b3ae-153">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="4b3ae-154">サービス プリンシパルの既定のロールは、**Contributor** です。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-154">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="4b3ae-155">このロールは、広範なアクセス許可が与えられているため、アプリと Azure サービスとの対話用には最適でない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-155">It may not be the best choice for an app's interactions with Azure services, given its broad permissions.</span></span> <span data-ttu-id="4b3ae-156">**Reader** ロールは、より制限が厳しく、読み取り専用のアクセスに適しています。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-156">The **Reader** role is more restrictive and is a good choice for read-only access.</span></span> <span data-ttu-id="4b3ae-157">Azure Portal では、ロールごとのアクセス許可に関する詳しい情報を確認したり、カスタム ロールを作成したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-157">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="4b3ae-158">次の例では、先ほどの例に **Reader** ロールを追加し、**Contributor** ロールを削除しています。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-158">In this example, add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

<span data-ttu-id="4b3ae-159">変更を確認するには、現在割り当てられているロールを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-159">Verify the changes by listing the currently assigned roles:</span></span>

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
> <span data-ttu-id="4b3ae-160">ロールを割り当てることのできるアクセス許可がアカウントに設定されていない場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-160">If your account does not have sufficient permissions to assign a role, you see an error message.</span></span>
> <span data-ttu-id="4b3ae-161">このメッセージは、アカウントで、スコープ "/subscriptions/{guid} に対するアクション Microsoft.Authorization/roleAssignments/write の実行が承認されていない" ことを示しています。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-161">The message states your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'."</span></span>
   
## <a name="change-the-credentials-of-a-security-principal"></a><span data-ttu-id="4b3ae-162">セキュリティ プリンシパルの資格情報を変更する</span><span class="sxs-lookup"><span data-stu-id="4b3ae-162">Change the credentials of a security principal</span></span>

<span data-ttu-id="4b3ae-163">セキュリティ上、アクセス許可の確認とパスワードの更新を定期的に行うことが大切です。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-163">It's a good security practice to review permissions and update passwords regularly.</span></span> <span data-ttu-id="4b3ae-164">アプリの変更に合わせて、セキュリティ資格情報を管理したり変更したりする場合もあります。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-164">You may also want to manage and modify the security credentials as your app changes.</span></span>

### <a name="reset-a-service-principal-password"></a><span data-ttu-id="4b3ae-165">サービス プリンシパルのパスワードをリセットする</span><span class="sxs-lookup"><span data-stu-id="4b3ae-165">Reset a service principal password</span></span>

<span data-ttu-id="4b3ae-166">サービス プリンシパルの現在のパスワードをリセットするには、`az ad sp reset-credentials` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-166">Use `az ad sp reset-credentials` to reset the current password for the service principal.</span></span>

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

<span data-ttu-id="4b3ae-167">`--password` オプションを指定しなかった場合は、CLI によって安全なパスワードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4b3ae-167">The CLI generates a secure password if you leave out the `--password` option.</span></span>
