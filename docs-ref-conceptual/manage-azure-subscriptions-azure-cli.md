---
title: "Azure CLI 2.0 を使用して Azure サブスクリプションを管理する"
description: "Linux、Mac、または Windows 上で Azure CLI 2.0 を使用して Azure サブスクリプションを管理します。"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 9f03e52fa72a8dbd5753904839a833db01ffb59b
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="98fb8-103">複数の Azure サブスクリプションの管理</span><span class="sxs-lookup"><span data-stu-id="98fb8-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="98fb8-104">ほとんどの Azure ユーザーは、サブスクリプションを 1 つしか持っていません。</span><span class="sxs-lookup"><span data-stu-id="98fb8-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="98fb8-105">ただし、複数の組織に属している場合や、組織がグループ間で特定のリソースへのアクセスを分けている場合、Azure に複数のサブスクリプションを持っていることがあります。</span><span class="sxs-lookup"><span data-stu-id="98fb8-105">However, if you are part of multiple organizations or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="98fb8-106">複数のサブスクリプションは、CLI を使用して簡単に管理することができ、サブスクリプションを選択して操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="98fb8-106">Multiple subscriptions can be easily managed with the CLI, and operations can be performed by selecting a subscription.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="98fb8-107">テナント、ユーザー、サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="98fb8-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="98fb8-108">Azure におけるテナント、ユーザー、サブスクリプションが混同されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="98fb8-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="98fb8-109">一般に、"_テナント_" とは、組織全体を含む Azure Active Directory エンティティです。</span><span class="sxs-lookup"><span data-stu-id="98fb8-109">In general, a _tenant_ is the Azure Active Directory entity which encompasses a whole organization.</span></span> <span data-ttu-id="98fb8-110">このテナントは、少なくとも 1 つの "_サブスクリプション_" を持ち、少なくとも 1 人の "_ユーザー_" が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98fb8-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="98fb8-111">ユーザーとは個人であり、1 つのテナント (ユーザーが属している組織) にのみ関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="98fb8-111">A user is an individual, and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="98fb8-112">ユーザーは、Azure にログインしてリソースをプロビジョニングおよび使用するアカウントです。</span><span class="sxs-lookup"><span data-stu-id="98fb8-112">Users are those accounts which log in to Azure to provision and use resources.</span></span> <span data-ttu-id="98fb8-113">1 人のユーザーが複数の "_サブスクリプション_" にアクセスできる場合があります。サブスクリプションとは、Azure をはじめとするクラウド サービスを使用するための Microsoft との契約です。</span><span class="sxs-lookup"><span data-stu-id="98fb8-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="98fb8-114">各リソースは、サブスクリプションに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="98fb8-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="98fb8-115">テナント、ユーザー、サブスクリプションの違いの詳細については、[Azure クラウド用語集](/azure/azure-glossary-cloud-terminology)のページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98fb8-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>
<span data-ttu-id="98fb8-116">Azure Active Directory テナントに新しいサブスクリプションを追加する方法については、「[Azure サブスクリプションを Azure Active Directory に追加する方法](/azure/active-directory/active-directory-how-subscriptions-associated-directory)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98fb8-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>

## <a name="working-with-multiple-subscriptions"></a><span data-ttu-id="98fb8-117">複数のサブスクリプションの操作</span><span class="sxs-lookup"><span data-stu-id="98fb8-117">Working with multiple subscriptions</span></span>

<span data-ttu-id="98fb8-118">サブスクリプションに含まれているリソースにアクセスするには、アクティブなサブスクリプションを切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="98fb8-118">To access the resources contained within a subscription, you need to switch your active subscription.</span></span> <span data-ttu-id="98fb8-119">サブスクリプションのすべての操作は、`az account` コマンドを使用して実行します。このコマンドは、個人アカウントを参照するのではなく、サブスクリプションが表すサービス契約を参照します。</span><span class="sxs-lookup"><span data-stu-id="98fb8-119">All work with subscriptions is done through the `az account` command, which refers to the service agreement that a subscription represents and not your individual account.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

<span data-ttu-id="98fb8-120">使用可能なサブスクリプションの操作を開始するには、アカウントで使用できるサブスクリプションの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="98fb8-120">To start working with your available subscriptions, get a list of those available in your account:</span></span>

```azurecli-interactive
az account list --output table
```

```Output
Name                                         CloudName    SubscriptionId                        State     IsDefault
-------------------------------------------  -----------  ------------------------------------  --------  -----------
My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
```

<span data-ttu-id="98fb8-121">アクティブなサブスクリプションを変更するには、`az account set` を使用します。</span><span class="sxs-lookup"><span data-stu-id="98fb8-121">In order to change the active subscription, you can use `az account set`:</span></span>

```azurecli-interactive
az account set --subscription "My Demos"
```

<span data-ttu-id="98fb8-122">サブスクリプションは、サブスクリプション ID またはサブスクリプション名を使用して選択できます。</span><span class="sxs-lookup"><span data-stu-id="98fb8-122">You can use either the subscription ID or the subscription name to select the subscription.</span></span>
