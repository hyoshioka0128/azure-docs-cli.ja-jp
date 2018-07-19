---
title: Azure CLI 2.0 で複数のクラウドを管理する
description: Azure CLI 2.0 で複数のクラウドの作成、サインイン、管理を行います。
author: sptramer
manager: carmonm
ms.author: sttramer
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 836bf920adaae7bff8482c697bf105f0d457c658
ms.sourcegitcommit: fb3fed8701aff6c46af856e8fdc3e56ff9a678bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38228939"
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="00c55-103">Azure CLI 2.0 で複数のクラウドを管理する</span><span class="sxs-lookup"><span data-stu-id="00c55-103">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="00c55-104">異なるリージョンにわたって作業したり、[Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/) を使用したりする場合、複数のクラウドの使用が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="00c55-104">If you work across different regions or use [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/), you may need to use more than one cloud.</span></span> <span data-ttu-id="00c55-105">Microsoft はお客様が使用可能な、リージョンの法規に従ったクラウドを提供します。</span><span class="sxs-lookup"><span data-stu-id="00c55-105">Microsoft provides clouds for compliance with regional laws, which are available for your use.</span></span> <span data-ttu-id="00c55-106">この記事では、お客様のアカウントで使用可能なクラウドに関する情報の取得、現行クラウドの変更、Azure Stack で使用する新規クラウドの登録または登録解除の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="00c55-106">This article shows you how to get information on clouds available to your account, change the current cloud, and register or unregister new clouds for use with Azure Stack.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="00c55-107">クラウドの一覧表示</span><span class="sxs-lookup"><span data-stu-id="00c55-107">Listing clouds</span></span>

<span data-ttu-id="00c55-108">使用可能なクラウドを [az cloud list](/cli/azure/cloud#az-cloud-list) コマンドで一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="00c55-108">You can list available clouds with the [az cloud list](/cli/azure/cloud#az-cloud-list) command.</span></span> <span data-ttu-id="00c55-109">これにより、現在アクティブなクラウド、その現在のプロファイル、およびリージョン サフィックスとホスト名に関する情報が得られます。</span><span class="sxs-lookup"><span data-stu-id="00c55-109">This tells you which cloud is currently active, what its current profile is, and information on regional suffixes and host names.</span></span>

<span data-ttu-id="00c55-110">アクティブなクラウドと、すべての使用可能クラウドの一覧を取得するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="00c55-110">To get the active cloud and a list of all the available clouds:</span></span>

```azurecli-interactive
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

<span data-ttu-id="00c55-111">現在アクティブなクラウドには `IsActive` 列に `True` と表示されます。</span><span class="sxs-lookup"><span data-stu-id="00c55-111">The currently active cloud has `True` in the `IsActive` column.</span></span> <span data-ttu-id="00c55-112">一度にアクティブにできるクラウドは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="00c55-112">Only one cloud can be active at any time.</span></span> <span data-ttu-id="00c55-113">Azure サービスに使用するエンドポイントなど、クラウドに関するより詳細な情報を得るには、`cloud show` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="00c55-113">To get more detailed information on a cloud, including the endpoints that it uses for Azure services, use the `cloud show` command:</span></span>

```azurecli-interactive
az cloud show --name AzureChinaCloud --output json
```

```output
{
  "endpoints": {
    "activeDirectory": "https://login.chinacloudapi.cn",
    "activeDirectoryDataLakeResourceId": null,
    "activeDirectoryGraphResourceId": "https://graph.chinacloudapi.cn/",
    "activeDirectoryResourceId": "https://management.core.chinacloudapi.cn/",
    "batchResourceId": "https://batch.chinacloudapi.cn/",
    "gallery": "https://gallery.chinacloudapi.cn/",
    "management": "https://management.core.chinacloudapi.cn/",
    "resourceManager": "https://management.chinacloudapi.cn",
    "sqlManagement": "https://management.core.chinacloudapi.cn:8443/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json"
  },
  "isActive": false,
  "name": "AzureChinaCloud",
  "profile": "latest",
  "suffixes": {
    "azureDatalakeAnalyticsCatalogAndJobEndpoint": null,
    "azureDatalakeStoreFileSystemEndpoint": null,
    "keyvaultDns": ".vault.azure.cn",
    "sqlServerHostname": ".database.chinacloudapi.cn",
    "storageEndpoint": "core.chinacloudapi.cn"
  }
}
```

## <a name="switching-the-active-cloud"></a><span data-ttu-id="00c55-114">アクティブなクラウドの切り替え</span><span class="sxs-lookup"><span data-stu-id="00c55-114">Switching the active cloud</span></span>

<span data-ttu-id="00c55-115">現在アクティブなクラウドを切り替えるには、[az cloud set](/cli/azure/cloud#az-cloud-set) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="00c55-115">To switch the currently active cloud, run the [az cloud set](/cli/azure/cloud#az-cloud-set) command.</span></span> <span data-ttu-id="00c55-116">このコマンドは、1 つの必須の引数として、クラウドの名前を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="00c55-116">This command takes one required argument, the name of the cloud.</span></span>

```azurecli-interactive
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="00c55-117">アクティブ化されたクラウドの認証が期限切れになった場合は、他の CLI タスクを実行する前に、再認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="00c55-117">If your authentication for the activated cloud has expired, you need to re-authenticate before performing any other CLI tasks.</span></span> <span data-ttu-id="00c55-118">新しいクラウドに初めて切り替える場合は、アクティブなサブスクリプションの設定も行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="00c55-118">If this is your first time switching to the new cloud, you also need to set the active subscription.</span></span>
> <span data-ttu-id="00c55-119">認証の手順については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00c55-119">For instructions on authenticating, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span> <span data-ttu-id="00c55-120">サブスクリプションの管理については、[Azure CLI 2.0 での Azure サブスクリプションの管理](manage-azure-subscriptions-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="00c55-120">For information on subscription management, see [Manage Azure subscriptions with Azure CLI 2.0](manage-azure-subscriptions-azure-cli.md)</span></span>

## <a name="register-a-cloud"></a><span data-ttu-id="00c55-121">クラウドを登録する</span><span class="sxs-lookup"><span data-stu-id="00c55-121">Register a cloud</span></span>

<span data-ttu-id="00c55-122">Azure Stack 用の独自のエンドポイントがある場合は、新しいクラウドを登録します。</span><span class="sxs-lookup"><span data-stu-id="00c55-122">Register a new cloud if you have your own endpoints for Azure Stack.</span></span> <span data-ttu-id="00c55-123">[az cloud register](/cli/azure/cloud#az-cloud-register) コマンドを実行すると、クラウドが作成されます。</span><span class="sxs-lookup"><span data-stu-id="00c55-123">Creating a cloud is done with the [az cloud register](/cli/azure/cloud#az-cloud-register) command.</span></span> <span data-ttu-id="00c55-124">このコマンドは、名前と、関連するエンドポイントを持つ機能のセットを必要とします。</span><span class="sxs-lookup"><span data-stu-id="00c55-124">This command requires a name and a set of capabilities with associated endpoints.</span></span> <span data-ttu-id="00c55-125">Azure Stack で使用するクラウドの登録方法については、「[Azure Stack での Azure CLI 2.0 による API バージョンのプロファイルの使用](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00c55-125">To learn how to register a cloud for use with Azure Stack, see [Use API version profiles with Azure CLI 2.0 in Azure Stack](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack).</span></span>

<span data-ttu-id="00c55-126">中国、米国政府、またはドイツのリージョンについては、独自のクラウドを登録する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="00c55-126">You do not need to register your own cloud for China, US Government, or German regions.</span></span> <span data-ttu-id="00c55-127">これらは Microsoft が管理しているため、既定値で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="00c55-127">These are managed by Microsoft and available by default.</span></span>  <span data-ttu-id="00c55-128">使用可能なエンドポイント設定に関する詳細については、[`az cloud register` のドキュメント](/cli/azure/cloud#az-cloud-register)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00c55-128">For more information on all of the available endpoint settings, see the [documentation for `az cloud register`](/cli/azure/cloud#az-cloud-register).</span></span>

<span data-ttu-id="00c55-129">クラウドを登録しても、自動的にそのクラウドに切り替わるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="00c55-129">Registering a cloud does not automatically switch to it.</span></span> <span data-ttu-id="00c55-130">前述のように、`az cloud set` コマンドを使用して、新規作成したクラウドを選択してください。</span><span class="sxs-lookup"><span data-stu-id="00c55-130">Use the `az cloud set` command to select the newly created cloud as described above.</span></span>

## <a name="update-an-existing-cloud"></a><span data-ttu-id="00c55-131">既存のクラウドを更新する</span><span class="sxs-lookup"><span data-stu-id="00c55-131">Update an existing cloud</span></span>

<span data-ttu-id="00c55-132">権限がある場合は、既存のクラウドを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="00c55-132">If you have permissions, you can also update an existing cloud.</span></span> <span data-ttu-id="00c55-133">この更新は、別の Azure プロファイルへの切り替え、エンドポイントの追加、またはエンドポイントの変更が必要な場合に行いますい。</span><span class="sxs-lookup"><span data-stu-id="00c55-133">Do this when you need to switch to a different Azure profile, add an endpoint, or change an endpoint.</span></span>
<span data-ttu-id="00c55-134">これは [az cloud update](/cli/azure/cloud#az-cloud-update) コマンドを使用して実行します。このコマンドでは `az cloud register` と同じ引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="00c55-134">You do this with the [az cloud update](/cli/azure/cloud#az-cloud-update) command, which takes the same arguments as `az cloud register`.</span></span>

## <a name="unregister-a-cloud"></a><span data-ttu-id="00c55-135">クラウドを登録解除する</span><span class="sxs-lookup"><span data-stu-id="00c55-135">Unregister a cloud</span></span>

<span data-ttu-id="00c55-136">登録済みのクラウドが不要になった場合は、次のように、[az cloud unregister](/cli/azure/cloud#az-cloud-unregister) コマンドを使用して登録解除できます。</span><span class="sxs-lookup"><span data-stu-id="00c55-136">If you no longer require a registered cloud, it can be unregistered with the [az cloud unregister](/cli/azure/cloud#az-cloud-unregister) command:</span></span>

```azurecli-interactive
az cloud unregister --name MyCloud
```
