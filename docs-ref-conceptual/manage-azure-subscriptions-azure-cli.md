---
title: "Azure CLI 2.0 を使用して Azure サブスクリプションを管理する"
description: "Linux、Mac、または Windows 上で Azure CLI 2.0 を使用して Azure サブスクリプションを管理します。"
keywords: "Azure CLI 2.0, Linux, Mac, Windows, OS X, サブスクリプション"
author: kamaljit
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: 383fb6ebd90ac79f60869187b402d53d4f1791fd
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2017
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="a9f44-104">複数の Azure サブスクリプションの管理</span><span class="sxs-lookup"><span data-stu-id="a9f44-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="a9f44-105">Azure を使い始めたばかりの場合、所有しているサブスクリプションは 1 つだけだと思われます。</span><span class="sxs-lookup"><span data-stu-id="a9f44-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="a9f44-106">一方、しばらく前から Azure を使用している場合は、複数の Azure サブスクリプションを作成済みであることも考えられます。</span><span class="sxs-lookup"><span data-stu-id="a9f44-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="a9f44-107">その場合は、特定のサブスクリプションに対してコマンドを実行するように Azure CLI 2.0 を構成できます。</span><span class="sxs-lookup"><span data-stu-id="a9f44-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. <span data-ttu-id="a9f44-108">アカウント内のすべてのサブスクリプションの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9f44-108">Get a list of all subscriptions in your account.</span></span>

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

1. <span data-ttu-id="a9f44-109">既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a9f44-109">Set the default.</span></span>
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > <span data-ttu-id="a9f44-110">`--subscription` パラメーターには、サブスクリプション名またはサブスクリプション ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9f44-110">The `--subscription` parameter takes either the subscription name or the subscription ID.</span></span>

<span data-ttu-id="a9f44-111">`az account list --output table` コマンドをもう一度実行して、変更を検証できます。</span><span class="sxs-lookup"><span data-stu-id="a9f44-111">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="a9f44-112">既定のサブスクリプションを設定すると、後続のすべての Azure CLI コマンドは、このサブスクリプションに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="a9f44-112">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>