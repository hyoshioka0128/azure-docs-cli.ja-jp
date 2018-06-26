---
title: Azure CLI を使用して Azure サブスクリプションを管理する
description: Azure CLI を使用して Azure サブスクリプションを管理します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/15/2018
ms.topic: conceptual
ms.produdct: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.service: active-directory
ms.openlocfilehash: fdc8ffca38a6a581ae63b0518df72f6e09110d07
ms.sourcegitcommit: 1a38729d6ae93c49137b3d49b6a9ec8a75eff190
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36262711"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="33469-103">複数の Azure サブスクリプションの管理</span><span class="sxs-lookup"><span data-stu-id="33469-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="33469-104">ほとんどの Azure ユーザーは、サブスクリプションを 1 つしか持っていません。</span><span class="sxs-lookup"><span data-stu-id="33469-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="33469-105">ただし、複数の組織に属している場合や、組織がグループ間で特定のリソースへのアクセスを分けている場合、Azure に複数のサブスクリプションを持っていることがあります。</span><span class="sxs-lookup"><span data-stu-id="33469-105">However, if you are part of multiple organizations or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="33469-106">複数のサブスクリプションを CLI を使用して簡単に管理するには、すべてのコマンドに対してグローバル サブスクリプションを設定するか、コマンドごとにサブスクリプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="33469-106">Multiple subscriptions can be easily managed with the CLI either by setting a global subscription for all commands, or selecting a subscription on a per-command basis.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="33469-107">テナント、ユーザー、サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="33469-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="33469-108">Azure におけるテナント、ユーザー、サブスクリプションが混同されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="33469-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="33469-109">"_テナント_" とは、組織全体を含む Azure Active Directory エンティティです。</span><span class="sxs-lookup"><span data-stu-id="33469-109">A _tenant_ is the Azure Active Directory entity which encompasses a whole organization.</span></span> <span data-ttu-id="33469-110">このテナントは、少なくとも 1 つの "_サブスクリプション_" を持ち、少なくとも 1 人の "_ユーザー_" が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33469-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="33469-111">ユーザーとは個人であり、1 つのテナント (ユーザーが属している組織) にのみ関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="33469-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="33469-112">ユーザーは、Azure にログインしてリソースをプロビジョニングおよび使用するアカウントです。</span><span class="sxs-lookup"><span data-stu-id="33469-112">Users are those accounts which log in to Azure to provision and use resources.</span></span>
<span data-ttu-id="33469-113">1 人のユーザーが複数の "_サブスクリプション_" にアクセスできる場合があります。サブスクリプションとは、Azure をはじめとするクラウド サービスを使用するための Microsoft との契約です。</span><span class="sxs-lookup"><span data-stu-id="33469-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="33469-114">各リソースは、サブスクリプションに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="33469-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="33469-115">テナント、ユーザー、サブスクリプションの違いの詳細については、[Azure クラウド用語集](/azure/azure-glossary-cloud-terminology)のページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="33469-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="33469-116">Azure Active Directory テナントに新しいサブスクリプションを追加する方法については、「[Azure サブスクリプションを Azure Active Directory に追加する方法](/azure/active-directory/active-directory-how-subscriptions-associated-directory)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="33469-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="33469-117">複数のテナントを使用するときは、特定のテナントへのサインインが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="33469-117">When working with multiple tenants, you may need to sign in to a specific tenant.</span></span> <span data-ttu-id="33469-118">これを行うには、[Azure CLI を使用したサインイン](/cli/azure/authenticate-azure-cli)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="33469-118">To do this, see [Sign in with Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="work-with-multiple-subscriptions"></a><span data-ttu-id="33469-119">複数のサブスクリプションの操作</span><span class="sxs-lookup"><span data-stu-id="33469-119">Work with multiple subscriptions</span></span>

<span data-ttu-id="33469-120">サブスクリプションに含まれているリソースにアクセスするには、アクティブなサブスクリプションを切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="33469-120">To access the resources contained within a subscription, you need to switch your active subscription.</span></span> <span data-ttu-id="33469-121">サブスクリプションの切り替えは、[az account set](/cli/azure/account#az-account-set) を使用してすべての Azure CLI コマンドに対して実行するか、`--subscription` 引数を使用してコマンドごとに実行します。</span><span class="sxs-lookup"><span data-stu-id="33469-121">Switching your subscription can be done for all Azure CLI commands with [az account set](/cli/azure/account#az-account-set), or done on a per-command basis by using the `--subscription` argument.</span></span>

<span data-ttu-id="33469-122">開始するには、利用可能なサブスクリプションの一覧が必要です。</span><span class="sxs-lookup"><span data-stu-id="33469-122">To start, you will need a list of your available subscriptions.</span></span> <span data-ttu-id="33469-123">これを取得するには、[az account list](/cli/azure/account#az-account-list) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="33469-123">To get it, use the [az account list](/cli/azure/account#az-account-list) command:</span></span>

```azurecli-interactive
az account list --output table
```

<span data-ttu-id="33469-124">アクティブなサブスクリプションをグローバルに変更するには、`az account set` を使用して、サブスクリプション ID またはサブスクリプション名を指定します。</span><span class="sxs-lookup"><span data-stu-id="33469-124">To change the active subscription globally, use `az account set` along with either the subscription ID or subscription name:</span></span>

```azurecli-interactive
az account set --subscription "My Demos"
```

<span data-ttu-id="33469-125">コマンドに対して特定のサブスクリプションを使用するには、`--subscription` 引数を使用するだけです。</span><span class="sxs-lookup"><span data-stu-id="33469-125">To use a specific subscription for a command, just use the `--subscription` argument.</span></span> <span data-ttu-id="33469-126">この引数には、サブスクリプション ID またはサブスクリプション名を指定します。</span><span class="sxs-lookup"><span data-stu-id="33469-126">This argument takes either a subscription ID or subscription name:</span></span>

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
