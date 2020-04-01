---
title: Azure CLI で Azure サービス プリンシパルを使用する
description: Azure CLI でサービス プリンシパルを作成および使用する方法について説明します。
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 02/15/2019
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: c18adbee84fd3e5c73367b07bbd0b03ac61008cd
ms.sourcegitcommit: b5ecfc168489cd0d96462d6decf83e8b26a10194
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2020
ms.locfileid: "80417868"
---
# <a name="create-an-azure-service-principal-with-the-azure-cli"></a><span data-ttu-id="787c8-103">Azure CLI で Azure サービス プリンシパルを作成する</span><span class="sxs-lookup"><span data-stu-id="787c8-103">Create an Azure service principal with the Azure CLI</span></span>

<span data-ttu-id="787c8-104">Azure サービスを使用する自動化ツールのアクセス許可は、常に制限されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="787c8-105">完全な特権を持つユーザーとしてアプリケーションをサインインさせる代わりに、Azure にはサービス プリンシパルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="787c8-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="787c8-106">Azure サービス プリンシパルは、Azure リソースにアクセスするアプリケーション、ホステッド サービス、および自動化ツールで使用するために作成される ID です。</span><span class="sxs-lookup"><span data-stu-id="787c8-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="787c8-107">このアクセスはサービス プリンシパルに割り当てられているロールによって制限されるため、どのリソースに、どのレベルでアクセスできるかを制御することができます。</span><span class="sxs-lookup"><span data-stu-id="787c8-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="787c8-108">セキュリティ上の理由から、自動化ツールにはユーザー ID でのログインを許可するのではなく、常にサービス プリンシパルを使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="787c8-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="787c8-109">この記事では、Azure CLI を使用して、サービス プリンシパルの作成、情報取得、およびリセットを行うための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="787c8-109">This article shows you the steps for creating, getting information about, and resetting a service principal with the Azure CLI.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="787c8-110">サービス プリンシパルの作成</span><span class="sxs-lookup"><span data-stu-id="787c8-110">Create a service principal</span></span>

<span data-ttu-id="787c8-111">サービス プリンシパルは、[az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) コマンドを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="787c8-111">Create a service principal with the [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) command.</span></span> <span data-ttu-id="787c8-112">サービス プリンシパルを作成する際に、サービス プリンシパルが使用するサインイン認証の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="787c8-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="787c8-113">ご利用のアカウントにサービス プリンシパルを作成するためのアクセス許可がない場合は、`az ad sp create-for-rbac` から "この操作を完了するのに十分な特権がありません" というエラー メッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-113">If your account doesn't have permission to create a service principal, `az ad sp create-for-rbac` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="787c8-114">サービス プリンシパルを作成するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="787c8-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="787c8-115">サービス プリンシパルで使用できる認証には、パスワードベースの認証と証明書ベースの認証の 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="787c8-116">パスワードベースの認証</span><span class="sxs-lookup"><span data-stu-id="787c8-116">Password-based authentication</span></span>

<span data-ttu-id="787c8-117">パスワード ベースの認証では、認証パラメーターは使用せず、自動的に作成されるランダム パスワードと共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-117">Without any authentication parameters, password-based authentication is used with a random password created for you.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName
  ```

> [!IMPORTANT]
> <span data-ttu-id="787c8-118">Azure CLI 2.0.68 の時点で、ユーザーが定義したパスワードを使ってサービス プリンシパルを作成する `--password` パラメーターは、脆弱なパスワードの予期しない使用を避けるために__サポートされなくなりました__。</span><span class="sxs-lookup"><span data-stu-id="787c8-118">As of Azure CLI 2.0.68, the `--password` parameter to create a service principal with a user-defined password is __no longer supported__ to prevent the accidental use of weak passwords.</span></span>

<span data-ttu-id="787c8-119">パスワード認証によるサービス プリンシパルの出力には、`password` キーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="787c8-119">The output for a service principal with password authentication includes the `password` key.</span></span> <span data-ttu-id="787c8-120">この値は__必ず__コピーしてください。取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="787c8-120">__Make sure__ you copy this value - it can't be retrieved.</span></span> <span data-ttu-id="787c8-121">パスワードを忘れた場合は、[サービス プリンシパルの資格情報をリセット](#reset-credentials)します。</span><span class="sxs-lookup"><span data-stu-id="787c8-121">If you forget the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="787c8-122">`appId` キーと `tenant` キーは `az ad sp create-for-rbac` の出力に表示され、サービス プリンシパルの認証で使用されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-122">The `appId` and `tenant` keys appear in the output of `az ad sp create-for-rbac` and are used in service principal authentication.</span></span>
<span data-ttu-id="787c8-123">これらの値を記録してください。ただし、[az ad sp list](/cli/azure/ad/sp#az-ad-sp-list) を使用していつでも取得できます。</span><span class="sxs-lookup"><span data-stu-id="787c8-123">Record their values, but they can be retrieved at any point with [az ad sp list](/cli/azure/ad/sp#az-ad-sp-list).</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="787c8-124">証明書ベースの認証</span><span class="sxs-lookup"><span data-stu-id="787c8-124">Certificate-based authentication</span></span>

<span data-ttu-id="787c8-125">証明書ベースの認証の場合は、`--cert` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-125">For certificate-based authentication, use the `--cert` argument.</span></span> <span data-ttu-id="787c8-126">この引数を使用するには、既存の証明書を保持しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-126">This argument requires that you hold an existing certificate.</span></span> <span data-ttu-id="787c8-127">このサービス プリンシパルを使用する任意のツールから、証明書の秘密キーにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="787c8-127">Make sure any tool that uses this service principal has access to the certificate's private key.</span></span> <span data-ttu-id="787c8-128">証明書は、PEM、CER、または DER などの ASCII 形式でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="787c8-128">Certificates should be in an ASCII format such as PEM, CER, or DER.</span></span> <span data-ttu-id="787c8-129">文字列として証明書を渡すか、`@path` 形式を使用してファイルから証明書を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="787c8-129">Pass the certificate as a string, or use the `@path` format to load the certificate from a file.</span></span>

> [!NOTE]
> <span data-ttu-id="787c8-130">PEM ファイルを使用する場合は、ファイル内で **PRIVATE KEY** (秘密キー) に **CERTIFICATE** (証明書) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-130">When using a PEM file, the **CERTIFICATE** must be appended to the **PRIVATE KEY** within the file.</span></span>

```azurecli-interactive
az ad sp create-for-rbac --name ServicePrincipalName --cert "-----BEGIN CERTIFICATE-----
...
-----END CERTIFICATE-----"
```

```azurecli-interactive
az ad sp create-for-rbac --name ServicePrincipalName --cert @/path/to/cert.pem
```

<span data-ttu-id="787c8-131">`--keyvault` 引数を追加すると、Azure Key Vault 内の証明書を使用できます。</span><span class="sxs-lookup"><span data-stu-id="787c8-131">The `--keyvault` argument can be added to use a certificate in Azure Key Vault.</span></span> <span data-ttu-id="787c8-132">ここでは、`--cert` 値は証明書の名前を表します。</span><span class="sxs-lookup"><span data-stu-id="787c8-132">In this case, the `--cert` value is the name of the certificate.</span></span>

```azurecli-interactive
az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
```

<span data-ttu-id="787c8-133">認証用の "_自己署名_" 証明書を作成するには、`--create-cert` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-133">To create a _self-signed_ certificate for authentication, use the `--create-cert` argument:</span></span>

```azurecli-interactive
az ad sp create-for-rbac --name ServicePrincipalName --create-cert
```

<span data-ttu-id="787c8-134">コンソール出力:</span><span class="sxs-lookup"><span data-stu-id="787c8-134">Console output:</span></span>

```
Creating a role assignment under the scope of "/subscriptions/myId"
Please copy C:\myPath\myNewFile.pem to a safe place.
When you run 'az login', provide the file path in the --password argument
{
  "appId": "myAppId",
  "displayName": "myDisplayName",
  "fileWithCertAndPrivateKey": "C:\\myPath\\myNewFile.pem",
  "name": "http://myName",
  "password": null,
  "tenant": "myTenantId"
}
```

<span data-ttu-id="787c8-135">新しい PEM ファイルの内容:</span><span class="sxs-lookup"><span data-stu-id="787c8-135">Contents of the new PEM file:</span></span>
```
-----BEGIN PRIVATE KEY-----
myPrivateKeyValue
-----END PRIVATE KEY-----
-----BEGIN CERTIFICATE-----
myCertificateValue
-----END CERTIFICATE-----
```

> [!NOTE]
> <span data-ttu-id="787c8-136">`az ad sp create-for-rbac --create-cert` コマンドはサービス プリンシパルと PEM ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="787c8-136">The `az ad sp create-for-rbac --create-cert` command creates the service principal and a PEM file.</span></span> <span data-ttu-id="787c8-137">PEM ファイルには、正しく書式設定された **PRIVATE KEY** (秘密キー) と **CERTIFICATE** (証明書) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="787c8-137">The PEM file contains a correctly formatted **PRIVATE KEY** and **CERTIFICATE**.</span></span>

<span data-ttu-id="787c8-138">`--keyvault` 引数を追加すると、証明書を Azure Key Vault に格納できます。</span><span class="sxs-lookup"><span data-stu-id="787c8-138">The `--keyvault` argument can be added to store the certificate in Azure Key Vault.</span></span> <span data-ttu-id="787c8-139">`--keyvault` を使用する場合は、`--cert` 引数が__必要__です。</span><span class="sxs-lookup"><span data-stu-id="787c8-139">When using `--keyvault`, the `--cert` argument is __required__.</span></span>

```azurecli-interactive
az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
```

<span data-ttu-id="787c8-140">証明書を Key Vault に格納しない場合は、出力に `fileWithCertAndPrivateKey` キーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="787c8-140">Unless you store the certificate in Key Vault, the output includes the `fileWithCertAndPrivateKey` key.</span></span> <span data-ttu-id="787c8-141">このキーの値を見ると、生成された証明書の格納場所がわかります。</span><span class="sxs-lookup"><span data-stu-id="787c8-141">This key's value tells you where the generated certificate is stored.</span></span>
<span data-ttu-id="787c8-142">証明書は__必ず__安全な場所にコピーしてください。そうしないと、このサービス プリンシパルでサインインすることができません。</span><span class="sxs-lookup"><span data-stu-id="787c8-142">__Make sure__ that you copy the certificate to a secure location, or you can't sign in with this service principal.</span></span>

<span data-ttu-id="787c8-143">Key Vault に格納されている証明書の場合、[az keyvault secret show](/cli/azure/keyvault/secret#az-keyvault-secret-show) を使用して証明書の秘密キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="787c8-143">For certificates stored in Key Vault, retrieve the certificate's private key with [az keyvault secret show](/cli/azure/keyvault/secret#az-keyvault-secret-show).</span></span> <span data-ttu-id="787c8-144">Key Vault では、証明書のシークレットの名前は、証明書の名前と同じです。</span><span class="sxs-lookup"><span data-stu-id="787c8-144">In Key Vault, the name of the certificate's secret is the same as the certificate name.</span></span> <span data-ttu-id="787c8-145">証明書の秘密キーにアクセスできない場合は、[サービス プリンシパルの資格情報をリセット](#reset-credentials)します。</span><span class="sxs-lookup"><span data-stu-id="787c8-145">If you lose access to a certificate's private key, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="787c8-146">`appId` キーと `tenant` キーは `az ad sp create-for-rbac` の出力に表示され、サービス プリンシパルの認証で使用されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-146">The `appId` and `tenant` keys appear in the output of `az ad sp create-for-rbac` and are used in service principal authentication.</span></span>
<span data-ttu-id="787c8-147">これらの値を記録してください。ただし、[az ad sp list](/cli/azure/ad/sp#az-ad-sp-list) を使用していつでも取得できます。</span><span class="sxs-lookup"><span data-stu-id="787c8-147">Record their values, but they can be retrieved at any point with [az ad sp list](/cli/azure/ad/sp#az-ad-sp-list).</span></span>

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="787c8-148">既存のサービス プリンシパルの取得</span><span class="sxs-lookup"><span data-stu-id="787c8-148">Get an existing service principal</span></span>

<span data-ttu-id="787c8-149">[az ad sp list](/cli/azure/ad/sp#az-ad-sp-list) を使用して、テナント内のサービス プリンシパルの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="787c8-149">A list of the service principals in a tenant can be retrieved with [az ad sp list](/cli/azure/ad/sp#az-ad-sp-list).</span></span> <span data-ttu-id="787c8-150">既定では、このコマンドによって、テナントの最初の 100 個のサービス プリンシパルが返されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-150">By default this command returns the first 100 service principals for your tenant.</span></span> <span data-ttu-id="787c8-151">テナントのサービス プリンシパルをすべて取得するには、`--all` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-151">To get all of a tenant's service principals, use the `--all` argument.</span></span> <span data-ttu-id="787c8-152">この一覧の取得には時間がかかる場合があるため、次の引数のいずれかを使用して一覧をフィルター処理することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="787c8-152">Getting this list can take a long time, so it's recommended that you filter the list with one of the following arguments:</span></span>

* <span data-ttu-id="787c8-153">`--display-name` は、指定した名前に一致する "_プレフィックス_" を持つサービス プリンシパルを要求します。</span><span class="sxs-lookup"><span data-stu-id="787c8-153">`--display-name` requests service principals that have a _prefix_ that match the provided name.</span></span> <span data-ttu-id="787c8-154">サービス プリンシパルの表示名は、作成時に `--name` パラメーターで設定した値です。</span><span class="sxs-lookup"><span data-stu-id="787c8-154">The display name of a service principal is the value set with the `--name` parameter during creation.</span></span> <span data-ttu-id="787c8-155">サービス プリンシパルの作成時に `--name` を設定していない場合、名前のプレフィックスは `azure-cli-` になります。</span><span class="sxs-lookup"><span data-stu-id="787c8-155">If you didn't set `--name` during service principal creation, the name prefix is `azure-cli-`.</span></span>
* <span data-ttu-id="787c8-156">`--spn` は、正確に一致するサービス プリンシパル名でフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="787c8-156">`--spn` filters on exact service principal name matching.</span></span> <span data-ttu-id="787c8-157">サービス プリンシパル名は常に `https://` で始まります。</span><span class="sxs-lookup"><span data-stu-id="787c8-157">The service principal name always starts with `https://`.</span></span>
  <span data-ttu-id="787c8-158">`--name` に使用した値が URI ではない場合、この値は `https://` とこれに続く表示名となります。</span><span class="sxs-lookup"><span data-stu-id="787c8-158">if the value you used for `--name` wasn't a URI, this value is `https://` followed by the display name.</span></span>
* <span data-ttu-id="787c8-159">`--show-mine` は、サインインしているユーザーによって作成されたサービス プリンシパルのみを要求します。</span><span class="sxs-lookup"><span data-stu-id="787c8-159">`--show-mine` requests only service principals created by the signed-in user.</span></span>
* <span data-ttu-id="787c8-160">`--filter` は OData フィルターを使用して、"_サーバー側_" のフィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="787c8-160">`--filter` takes an OData filter, and performs _server-side_ filtering.</span></span> <span data-ttu-id="787c8-161">この方法は、CLI の `--query` 引数を使用したクライアント側のフィルター処理よりも推奨されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-161">This method is recommended over filtering client-side with the CLI's `--query` argument.</span></span> <span data-ttu-id="787c8-162">OData フィルターの詳細については、[フィルターのための OData 式の構文](/rest/api/searchservice/odata-expression-syntax-for-azure-search)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="787c8-162">To learn about OData filters, see [OData expression syntax for filters](/rest/api/searchservice/odata-expression-syntax-for-azure-search).</span></span>

<span data-ttu-id="787c8-163">サービス プリンシパル オブジェクトについて返される情報は、詳細情報です。</span><span class="sxs-lookup"><span data-stu-id="787c8-163">The information returned for service principal objects is verbose.</span></span> <span data-ttu-id="787c8-164">サインインに必要な情報のみを取得するには、クエリ文字列 `[].{id:appId, tenant:appOwnerTenantId}` を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-164">To get only the information necessary for sign-in, use the query string `[].{id:appId, tenant:appOwnerTenantId}`.</span></span> <span data-ttu-id="787c8-165">たとえば、現在ログインしているユーザーによって作成されたすべてのサービス プリンシパルのサインイン情報を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-165">For example, to get the sign-in information for all service principals created by the currently logged in user:</span></span>

```azurecli-interactive
az ad sp list --show-mine --query "[].{id:appId, tenant:appOwnerTenantId}"
```

> [!IMPORTANT]
>
> <span data-ttu-id="787c8-166">`az ad sp list` または [az ad sp show](/cli/azure/ad/sp#az-ad-sp-show) を使用するとユーザーとテナントは取得されますが、認証シークレット "_も_" 認証方法も取得されません。</span><span class="sxs-lookup"><span data-stu-id="787c8-166">`az ad sp list` or [az ad sp show](/cli/azure/ad/sp#az-ad-sp-show) get the user and tenant, but not any authentication secrets _or_ the authentication method.</span></span>
> <span data-ttu-id="787c8-167">Key Vault 内の証明書のシークレットは [az keyvault secret show](/cli/azure/keyvault/secret#az-keyvault-secret-show) を使用して取得できますが、既定では、それ以外のシークレットは保存されません。</span><span class="sxs-lookup"><span data-stu-id="787c8-167">Secrets for certificates in Key Vault can be retrieved with [az keyvault secret show](/cli/azure/keyvault/secret#az-keyvault-secret-show), but no other secrets are stored by default.</span></span>
> <span data-ttu-id="787c8-168">認証方法やシークレットを忘れた場合は、[サービス プリンシパルの資格情報をリセット](#reset-credentials)します。</span><span class="sxs-lookup"><span data-stu-id="787c8-168">If you forget an authentication method or secret, [reset the service principal credentials](#reset-credentials).</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="787c8-169">サービス プリンシパル ロールを管理する</span><span class="sxs-lookup"><span data-stu-id="787c8-169">Manage service principal roles</span></span>

<span data-ttu-id="787c8-170">Azure CLI には、ロールの割り当てを管理するために、次のコマンドが用意されています。</span><span class="sxs-lookup"><span data-stu-id="787c8-170">The Azure CLI has the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="787c8-171">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="787c8-171">az role assignment list</span></span>](/cli/azure/role/assignment#az-role-assignment-list)
* [<span data-ttu-id="787c8-172">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="787c8-172">az role assignment create</span></span>](/cli/azure/role/assignment#az-role-assignment-create)
* [<span data-ttu-id="787c8-173">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="787c8-173">az role assignment delete</span></span>](/cli/azure/role/assignment#az-role-assignment-delete)

<span data-ttu-id="787c8-174">サービス プリンシパルの既定のロールは**共同作成者**です。</span><span class="sxs-lookup"><span data-stu-id="787c8-174">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="787c8-175">このロールには、Azure アカウントの読み取りと書き込みを行うための完全なアクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-175">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="787c8-176">**閲覧者**ロールは制限がより厳しく、読み取り専用アクセスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="787c8-176">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="787c8-177">ロールベースのアクセス制御 (RBAC) とロールの詳細については、[RBAC の組み込みのロール](/azure/active-directory/role-based-access-built-in-roles)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="787c8-177">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="787c8-178">この例では、**閲覧者**ロールを追加し、**共同作成者**ロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="787c8-178">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

> [!NOTE]
> <span data-ttu-id="787c8-179">ロールを割り当てるためのアクセス許可がアカウントにない場合は、アカウントに "'Microsoft.Authorization/roleAssignments/write' のアクションを実行するためのアクセス権限がありません" というエラー メッセージが表示されます。ロールを管理するには、Azure Active Directory 管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="787c8-179">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="787c8-180">ロールを追加しても、以前に割り当てられたアクセス許可は制限され "_ません_"。</span><span class="sxs-lookup"><span data-stu-id="787c8-180">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="787c8-181">サービス プリンシパルのアクセス許可を制限するときは、__共同作成者__ロールを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-181">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="787c8-182">変更を確認するには、割り当てられているロールの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="787c8-182">The changes can be verified by listing the assigned roles:</span></span>

```azurecli-interactive
az role assignment list --assignee APP_ID
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="787c8-183">サービス プリンシパルを使用したサインイン</span><span class="sxs-lookup"><span data-stu-id="787c8-183">Sign in using a service principal</span></span>

<span data-ttu-id="787c8-184">サインインして、新しいサービス プリンシパルの資格情報とアクセス許可をテストします。</span><span class="sxs-lookup"><span data-stu-id="787c8-184">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="787c8-185">サービス プリンシパルでサインインするには、`appId`、`tenant`、および資格情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="787c8-185">To sign in with a service prinicpal, you need the `appId`, `tenant`, and credentials.</span></span>

<span data-ttu-id="787c8-186">パスワードを使用してサービス プリンシパルでサインインするには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-186">To sign in with a service principal using a password:</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

<span data-ttu-id="787c8-187">証明書を使用してサインインする場合、その証明書は、ASCII 形式の PEM または DER ファイルとしてローカルで使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-187">To sign in with a certificate, it must be available locally as a PEM or DER file, in ASCII format.</span></span> <span data-ttu-id="787c8-188">PEM ファイルを使用する場合は、ファイル内に **PRIVATE KEY** (秘密キー) と **CERTIFICATE** (証明書) を共に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="787c8-188">When using a PEM file, the **PRIVATE KEY** and **CERTIFICATE** must be appended together within the file.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password /path/to/cert
```

<span data-ttu-id="787c8-189">サービス プリンシパルを使用したサインインの詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="787c8-189">To learn more about signing in with a service principal, see [Sign in with the Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="787c8-190">資格情報をリセットする</span><span class="sxs-lookup"><span data-stu-id="787c8-190">Reset credentials</span></span>

<span data-ttu-id="787c8-191">サービス プリンシパルの資格情報を忘れた場合は、[az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-191">If you forget the credentials for a service principal, use [az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset).</span></span> <span data-ttu-id="787c8-192">リセット コマンドでは、`az ad sp create-for-rbac` と同じ引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="787c8-192">The reset command takes the same arguments as `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az ad sp credential reset --name APP_ID
```
