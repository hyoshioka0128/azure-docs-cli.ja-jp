---
title: "Azure CLI 2.0 で複数のクラウドを管理する"
description: "Azure CLI 2.0 でさまざまなクラウドの作成、ログイン、管理を行います。"
keywords: "Azure CLI 2.0, Azure, クラウド, データセンター, 政府機関, リージョン, 中国, ドイツ"
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="97fc9-104">Azure CLI 2.0 で複数のクラウドを管理する</span><span class="sxs-lookup"><span data-stu-id="97fc9-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="97fc9-105">Azure に複数のサブスクリプションが関連付けられている場合は、複数のクラウドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-105">If you have multiple subscriptions associated with Azure, you may have more than one cloud available.</span></span> <span data-ttu-id="97fc9-106">各クラウドには独自の関連エンドポイントと機能があり、多くの場合、さまざまなデータ保護標準や要件がある特定のリージョンに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="97fc9-106">Each cloud has its own associated endpoints and capabilities, and is often associated with a particular region that has different data protection standards or requirements.</span></span>

<span data-ttu-id="97fc9-107">複数のクラウドを効果的に使用するには、アクティブなクラウドを切り替えることができ、新しいクラウドを作成できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fc9-107">To effectively work with multiple clouds, you will need to be able to switch between which is currently active, and possibly create new clouds.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="97fc9-108">クラウドの一覧表示</span><span class="sxs-lookup"><span data-stu-id="97fc9-108">Listing clouds</span></span>

<span data-ttu-id="97fc9-109">[cloud list](/cli/azure/cloud#list) コマンドを使って、使用できるクラウドを一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-109">You may list your available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="97fc9-110">これで、どのクラウドが現在アクティブであり、どれが現在のプロファイルであるかがわかります。また、リージョン サフィックスとホスト名に関する情報も示されます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-110">This will tell you which cloud is currently active, what its current profile is, and can provide information on regional suffixes and host names.</span></span>

<span data-ttu-id="97fc9-111">使用できるクラウドと現在アクティブなクラウドの一覧を取得するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="97fc9-111">To get a list of the available clouds and the currently active one:</span></span>

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

## <a name="switching-the-active-cloud"></a><span data-ttu-id="97fc9-112">アクティブなクラウドの切り替え</span><span class="sxs-lookup"><span data-stu-id="97fc9-112">Switching the active cloud</span></span>

<span data-ttu-id="97fc9-113">現在アクティブなクラウドを切り替えるには、[cloud set](/cli/azure/cloud#set) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="97fc9-113">In order to switch the currently active cloud, you run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="97fc9-114">このコマンドは、1 つの必須の引数として、クラウドの名前を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="97fc9-114">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="97fc9-115">アクティブ クラウドでまだ認証を行っていない場合は、他の CLI 操作を実行する前に、認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="97fc9-115">If you have never authenticated for the active cloud, you will need to do so before performing any other CLI operations.</span></span> <span data-ttu-id="97fc9-116">認証の手順については、「[Log in with Azure CLI 2.0 (Azure CLI 2.0 を使用してログインする)](/cli/azure/authenticate-azure-cli)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97fc9-116">For instructions on authenticating, see [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="register-or-unregister-a-cloud"></a><span data-ttu-id="97fc9-117">クラウドの登録または登録解除</span><span class="sxs-lookup"><span data-stu-id="97fc9-117">Register or unregister a cloud</span></span>

<span data-ttu-id="97fc9-118">独自のエンドポイントがあるか、別のプロファイルが必要な場合は、新しいクラウドを登録します。</span><span class="sxs-lookup"><span data-stu-id="97fc9-118">Register a new cloud if you have your own endpoints or require a different profile.</span></span> <span data-ttu-id="97fc9-119">[cloud register](/cli/azure/cloud#register) コマンドを実行すると、クラウドが作成されます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-119">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="97fc9-120">このコマンドには、名前を指定する必要があります。また、オプションで、機能とエンドポイントのセットも指定できます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-120">This command requires a name, and optionally a set of capabilities and endpoint designations.</span></span>

<span data-ttu-id="97fc9-121">リソース マネージャー用の特別なエンドポイントと特定のプロファイルを備えたクラウドを作成するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="97fc9-121">To create a cloud with a specialized endpoint for the resource manager, with a specific profile:</span></span>

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

<span data-ttu-id="97fc9-122">これでクラウドが作成されますが、自動的には選択され "_ません_"。</span><span class="sxs-lookup"><span data-stu-id="97fc9-122">This creates the cloud, but does _not_ automatically select it.</span></span>

<span data-ttu-id="97fc9-123">作成したクラウドが不要になった場合は、次のように、[cloud unregister](/cli/azure/cloud#unregister) コマンドで登録解除することができます。</span><span class="sxs-lookup"><span data-stu-id="97fc9-123">If you no longer require the created cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```

