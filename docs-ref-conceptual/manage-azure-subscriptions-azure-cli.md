---
title: Azure CLI を使用して Azure サブスクリプションを管理する
description: Azure CLI を使用して Azure サブスクリプションを管理します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.produdct: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 27f094b68812cb68a6a33a6977d4fd58e4178731
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593661"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="2310d-103">複数の Azure サブスクリプションの使用</span><span class="sxs-lookup"><span data-stu-id="2310d-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="2310d-104">ほとんどの Azure ユーザーは、サブスクリプションを 1 つしか持っていません。</span><span class="sxs-lookup"><span data-stu-id="2310d-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="2310d-105">ただし、複数の組織に属している場合や、組織がグループ間で特定のリソースへのアクセスを分けている場合、Azure に複数のサブスクリプションを持っていることがあります。</span><span class="sxs-lookup"><span data-stu-id="2310d-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="2310d-106">CLI では、サブスクリプションをグローバルに選択することも、コマンドごとに選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="2310d-106">The CLI supports selecting a subscription both globally and per command.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="2310d-107">テナント、ユーザー、サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="2310d-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="2310d-108">Azure におけるテナント、ユーザー、サブスクリプションが混同されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2310d-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="2310d-109">"_テナント_" とは、組織全体を含む Azure Active Directory エンティティです。</span><span class="sxs-lookup"><span data-stu-id="2310d-109">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="2310d-110">このテナントは、少なくとも 1 つの "_サブスクリプション_" を持ち、少なくとも 1 人の "_ユーザー_" が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2310d-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="2310d-111">ユーザーとは個人であり、1 つのテナント (ユーザーが属している組織) にのみ関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="2310d-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="2310d-112">ユーザーは、Azure にサインインしてリソースを作成、管理、および使用するアカウントです。</span><span class="sxs-lookup"><span data-stu-id="2310d-112">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="2310d-113">1 人のユーザーが複数の "_サブスクリプション_" にアクセスできる場合があります。サブスクリプションとは、Azure をはじめとするクラウド サービスを使用するための Microsoft との契約です。</span><span class="sxs-lookup"><span data-stu-id="2310d-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="2310d-114">各リソースは、サブスクリプションに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="2310d-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="2310d-115">テナント、ユーザー、サブスクリプションの違いの詳細については、[Azure クラウド用語集](/azure/azure-glossary-cloud-terminology)のページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2310d-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="2310d-116">Azure Active Directory テナントに新しいサブスクリプションを追加する方法については、「[Azure サブスクリプションを Azure Active Directory に追加する方法](/azure/active-directory/active-directory-how-subscriptions-associated-directory)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2310d-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="2310d-117">特定のテナントにサインインする方法を確認するには、[Azure CLI を使用したサインイン](/cli/azure/authenticate-azure-cli)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2310d-117">To learn how to sign in to a specific tenant, see [Sign in with Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="2310d-118">アクティブなサブスクリプションを変更する</span><span class="sxs-lookup"><span data-stu-id="2310d-118">Change the active subscription</span></span> 

<span data-ttu-id="2310d-119">サブスクリプションのリソースにアクセスするには、アクティブなサブスクリプションを切り替えるか、または `--subscription` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="2310d-119">To access the resources for a subscription, switch your active subscription or use the `--subscription` argument.</span></span> <span data-ttu-id="2310d-120">すべてのコマンドについてサブスクリプションを切り替えるには、[az account set](/cli/azure/account#az-account-set) を使用します。</span><span class="sxs-lookup"><span data-stu-id="2310d-120">Switching your subscription for all commands is done with [az account set](/cli/azure/account#az-account-set).</span></span>

<span data-ttu-id="2310d-121">アクティブなサブスクリプションを切り替えるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2310d-121">To switch your active subscription:</span></span>

1. <span data-ttu-id="2310d-122">[az account list](/cli/azure/account#az-account-list) コマンドを使用して、サブスクリプションの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="2310d-122">Get a list of your subscriptions with the [az account list](/cli/azure/account#az-account-list) command:</span></span>

    ```azurecli-interactive
    az account list --output table
    ```
2. <span data-ttu-id="2310d-123">サブスクリプション ID または切り替え先の名前を指定して、`az account set` を実行します。</span><span class="sxs-lookup"><span data-stu-id="2310d-123">Use `az account set` with the subscription ID or name you want to switch to.</span></span>

    ```azurecli-interactive
    az account set --subscription "My Demos"
    ```

<span data-ttu-id="2310d-124">異なるサブスクリプションで 1 つのコマンドのみを実行するには、`--subscription` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="2310d-124">To run only a single command with a different subscription, use the `--subscription` argument.</span></span> <span data-ttu-id="2310d-125">この引数には、サブスクリプション ID またはサブスクリプション名を指定します。</span><span class="sxs-lookup"><span data-stu-id="2310d-125">This argument takes either a subscription ID or subscription name:</span></span>

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
