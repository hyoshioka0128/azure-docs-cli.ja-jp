---
title: "Azure CLI 2.0 を使用してログインする"
description: "Linux、Mac、または Windows 上で Azure 2.0 CLI を使用してログインします。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: 4ab4f0de38614eff00f55bad96ea886bb007f3c0
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2017
---
# <a name="log-in-with-azure-cli-20"></a><span data-ttu-id="f34d9-104">Azure CLI 2.0 を使用してログインする</span><span class="sxs-lookup"><span data-stu-id="f34d9-104">Log in with Azure CLI 2.0</span></span>

<span data-ttu-id="f34d9-105">Azure CLI を使用してログインと認証を行うには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="f34d9-105">There are several ways to log in and authenticate with the Azure CLI.</span></span> <span data-ttu-id="f34d9-106">最も簡単に始められるのは、ブラウザーから対話形式でログインするか、コマンド ラインでログインする方法です。</span><span class="sxs-lookup"><span data-stu-id="f34d9-106">The simplest way to get started is to log in interactively through your browser, or to log in at the command line.</span></span> <span data-ttu-id="f34d9-107">お勧めは、サービス プリンシパルを使用する方法です。サービス プリンシパルは、リソースの操作に使用できる非対話型のアカウントを作成する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="f34d9-107">Our recommended approach is to use service principals, which provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="f34d9-108">サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化スクリプトをより安全にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f34d9-108">By granting just the appropriate permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="f34d9-109">CLI で実行するコマンドは、既定のサブスクリプションに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="f34d9-109">Commands that you run with the CLI are run against your default subscription.</span></span>  <span data-ttu-id="f34d9-110">複数のサブスクリプションがある場合は、[既定のサブスクリプションを確認](manage-azure-subscriptions-azure-cli.md)し、それを適切に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="f34d9-110">If you have more than one subscription, you may want to [confirm your default subscription](manage-azure-subscriptions-azure-cli.md) and change it appropriately.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="f34d9-111">対話形式のログイン</span><span class="sxs-lookup"><span data-stu-id="f34d9-111">Interactive log-in</span></span>

<span data-ttu-id="f34d9-112">Web ブラウザーから対話形式でログインします。</span><span class="sxs-lookup"><span data-stu-id="f34d9-112">Log in interactively from your web browser.</span></span>

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a><span data-ttu-id="f34d9-113">コマンド ライン</span><span class="sxs-lookup"><span data-stu-id="f34d9-113">Command line</span></span>

<span data-ttu-id="f34d9-114">コマンド ラインで、資格情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="f34d9-114">Provide your credentials on the command line.</span></span>

> [!Note]
> <span data-ttu-id="f34d9-115">この方法は、Microsoft アカウント、または 2 要素認証が有効になっているアカウントでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="f34d9-115">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a><span data-ttu-id="f34d9-116">サービス プリンシパルによるログイン</span><span class="sxs-lookup"><span data-stu-id="f34d9-116">Logging in with a service principal</span></span>

<span data-ttu-id="f34d9-117">サービス プリンシパルは、Azure Active Directory を使用してルールを適用できるユーザー アカウントに似ています。</span><span class="sxs-lookup"><span data-stu-id="f34d9-117">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span>
<span data-ttu-id="f34d9-118">サービス プリンシパルによる認証は、リソースを操作するスクリプトまたはアプリケーションからの Azure リソースの使用を保護するための最適な方法です。</span><span class="sxs-lookup"><span data-stu-id="f34d9-118">Authenticating with a service principal is the best way to secure the usage of your Azure resources from either your scripts or applications that manipulate resources.</span></span>
<span data-ttu-id="f34d9-119">ユーザーに持たせるロールを、コマンドの `az role` セットを通じて定義します。</span><span class="sxs-lookup"><span data-stu-id="f34d9-119">You define the roles you want your users to have via the `az role` set of commands.</span></span>
<span data-ttu-id="f34d9-120">サービス プリンシパルのロールの詳細と例については、[az role のリファレンス記事](https://docs.microsoft.com/cli/azure/role.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f34d9-120">You can learn more and see examples of service principal roles in our [az role reference articles](https://docs.microsoft.com/cli/azure/role.md).</span></span>

1. <span data-ttu-id="f34d9-121">まだサービス プリンシパルがない場合は、サービス プリンシパルを[作成](create-an-azure-service-principal-azure-cli.md)します。</span><span class="sxs-lookup"><span data-stu-id="f34d9-121">If you don't already have a service principal, [create one](create-an-azure-service-principal-azure-cli.md).</span></span>

1. <span data-ttu-id="f34d9-122">サービス プリンシパルを使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="f34d9-122">Log in with the service principal.</span></span>

   ```azurecli-interactive
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   <span data-ttu-id="f34d9-123">テナントを取得するには、対話形式でログインし、サブスクリプションから tenantId を取得します。</span><span class="sxs-lookup"><span data-stu-id="f34d9-123">To get your tenant, log in interactively and then get the tenantId from your subscription.</span></span>

   ```azurecli
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```