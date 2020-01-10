---
title: Azure CLI でクラウドを選択する
description: Azure CLI で複数のクラウドの作成、サインイン、管理を行います。
author: sptramer
manager: carmonm
ms.author: sttramer
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: f102414b9539c9f8ad7d088c2ddf802583c22721
ms.sourcegitcommit: 503cf343422ab8d2a587d2ccb795953b8ad66376
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/31/2019
ms.locfileid: "75559611"
---
# <a name="select-clouds-with-the-azure-cli"></a><span data-ttu-id="dc6ac-103">Azure CLI でクラウドを選択する</span><span class="sxs-lookup"><span data-stu-id="dc6ac-103">Select clouds with the Azure CLI</span></span>

<span data-ttu-id="dc6ac-104">異なるリージョンにわたって作業したり、[Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/) を使用したりする場合、複数のクラウドの使用が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-104">If you work across different regions or use [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/), you may need to use more than one cloud.</span></span> <span data-ttu-id="dc6ac-105">Microsoft はお客様が使用可能な、リージョンの法規に従ったクラウドを提供します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-105">Microsoft provides clouds for compliance with regional laws, which are available for your use.</span></span> <span data-ttu-id="dc6ac-106">この記事では、クラウドに関する情報の取得、現行クラウドの変更、新規クラウドの登録または登録解除の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-106">This article shows you how to get information on clouds, change the current cloud, and register or unregister new clouds.</span></span>

## <a name="list-available-clouds"></a><span data-ttu-id="dc6ac-107">使用可能なクラウドを一覧表示する</span><span class="sxs-lookup"><span data-stu-id="dc6ac-107">List available clouds</span></span>

<span data-ttu-id="dc6ac-108">使用可能なクラウドを [az cloud list](/cli/azure/cloud#az-cloud-list) コマンドで一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-108">You can list available clouds with the [az cloud list](/cli/azure/cloud#az-cloud-list) command.</span></span> <span data-ttu-id="dc6ac-109">このコマンドにより、現在アクティブなクラウド、その現在のプロファイル、およびリージョン サフィックスとホスト名に関する情報が得られます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-109">This command shows which cloud is currently active, what its current profile is, and information on regional suffixes and host names.</span></span>

<span data-ttu-id="dc6ac-110">アクティブなクラウドと、すべての使用可能クラウドの一覧を取得するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-110">To get the active cloud and a list of all the available clouds:</span></span>

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

<span data-ttu-id="dc6ac-111">現在アクティブなクラウドには `IsActive` 列に `True` と表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-111">The currently active cloud has `True` in the `IsActive` column.</span></span> <span data-ttu-id="dc6ac-112">一度にアクティブにできるクラウドは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-112">Only one cloud can be active at any time.</span></span> <span data-ttu-id="dc6ac-113">Azure サービスに使用するエンドポイントなど、クラウドに関するより詳細な情報を得るには、`cloud show` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-113">To get more detailed information on a cloud, including the endpoints that it uses for Azure services, use the `cloud show` command:</span></span>

```azurecli-interactive
az cloud show --name AzureChinaCloud --output json
```

```json
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

## <a name="switch-the-active-cloud"></a><span data-ttu-id="dc6ac-114">アクティブなクラウドを切り替える</span><span class="sxs-lookup"><span data-stu-id="dc6ac-114">Switch the active cloud</span></span>

<span data-ttu-id="dc6ac-115">構成ファイルを使用して既定のクラウドを設定する方法については、「[CLI 構成値と環境変数](/cli/azure/azure-cli-configuration?view=azure-cli-latest#cli-configuration-values-and-environment-variables)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-115">To set the default cloud using a configuration file, see [CLI configuration values and environment variables](/cli/azure/azure-cli-configuration?view=azure-cli-latest#cli-configuration-values-and-environment-variables).</span></span>  <span data-ttu-id="dc6ac-116">アクティブなクラウドを切り替えるには、[az cloud set](/cli/azure/cloud#az-cloud-set) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-116">To switch the active cloud, run the [az cloud set](/cli/azure/cloud#az-cloud-set) command.</span></span> <span data-ttu-id="dc6ac-117">このコマンドは、1 つの必須の引数として、クラウドの名前を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-117">This command takes one required argument, the name of the cloud.</span></span>

```azurecli-interactive
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="dc6ac-118">アクティブ化されたクラウドの認証が期限切れになった場合は、他の CLI タスクを実行する前に、再認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-118">If your authentication for the activated cloud has expired, you need to re-authenticate before performing any other CLI tasks.</span></span> <span data-ttu-id="dc6ac-119">新しいクラウドに初めて切り替える場合は、アクティブなサブスクリプションの設定も行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-119">If this is your first time switching to the new cloud, you also need to set the active subscription.</span></span>
> <span data-ttu-id="dc6ac-120">認証の手順については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-120">For instructions on authenticating, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span> <span data-ttu-id="dc6ac-121">サブスクリプションの管理については、[Azure CLI での Azure サブスクリプションの管理](manage-azure-subscriptions-azure-cli.md)に関するページをご覧ください</span><span class="sxs-lookup"><span data-stu-id="dc6ac-121">For information on subscription management, see [Manage Azure subscriptions with Azure CLI](manage-azure-subscriptions-azure-cli.md)</span></span>

## <a name="register-a-new-cloud"></a><span data-ttu-id="dc6ac-122">新しいクラウドを登録する</span><span class="sxs-lookup"><span data-stu-id="dc6ac-122">Register a new cloud</span></span>

<span data-ttu-id="dc6ac-123">Azure Stack 用の独自のエンドポイントがある場合は、新しいクラウドを登録します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-123">Register a new cloud if you have your own endpoints for Azure Stack.</span></span> <span data-ttu-id="dc6ac-124">[az cloud register](/cli/azure/cloud#az-cloud-register) コマンドを実行すると、クラウドが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-124">Creating a cloud is done with the [az cloud register](/cli/azure/cloud#az-cloud-register) command.</span></span> <span data-ttu-id="dc6ac-125">このコマンドには、名前と一連のサービス エンドポイントが必要です。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-125">This command requires a name and a set of service endpoints.</span></span> <span data-ttu-id="dc6ac-126">Azure Stack で使用するクラウドの登録方法については、[Azure Stack での Azure CLI による API バージョンのプロファイルの使用](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-126">To learn how to register a cloud for use with Azure Stack, see [Use API version profiles with Azure CLI in Azure Stack](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack).</span></span>

<span data-ttu-id="dc6ac-127">中国、米国政府、またはドイツのリージョンについては、情報を登録する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-127">You don't need to register information for the China, US Government, or German regions.</span></span> <span data-ttu-id="dc6ac-128">これらのクラウドは Microsoft が管理しているため、既定値で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-128">These clouds are managed by Microsoft and available by default.</span></span>  <span data-ttu-id="dc6ac-129">使用可能なエンドポイント設定に関する詳細については、[`az cloud register` のドキュメント](/cli/azure/cloud#az-cloud-register)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-129">For more information on all of the available endpoint settings, see the [documentation for `az cloud register`](/cli/azure/cloud#az-cloud-register).</span></span>

<span data-ttu-id="dc6ac-130">クラウドを登録しても、自動的にそのクラウドに切り替わるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-130">Registering a cloud doesn't automatically switch to it.</span></span> <span data-ttu-id="dc6ac-131">`az cloud set` コマンドを使用して、新規作成したクラウドを選択してください。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-131">Use the `az cloud set` command to select the newly created cloud.</span></span>

## <a name="update-an-existing-cloud"></a><span data-ttu-id="dc6ac-132">既存のクラウドを更新する</span><span class="sxs-lookup"><span data-stu-id="dc6ac-132">Update an existing cloud</span></span>

<span data-ttu-id="dc6ac-133">権限がある場合は、既存のクラウドを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-133">If you have permissions, you can also update an existing cloud.</span></span> <span data-ttu-id="dc6ac-134">クラウドを更新すると、別の Azure サービス プロファイルに切り替わるか、接続エンドポイントが変更されます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-134">Updating a cloud switches to a different Azure services profile or modifies the connection endpoints.</span></span>
<span data-ttu-id="dc6ac-135">クラウドの更新は [az cloud update](/cli/azure/cloud#az-cloud-update) コマンドを使用して実行します。このコマンドでは `az cloud register` と同じ引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-135">Update a cloud with the [az cloud update](/cli/azure/cloud#az-cloud-update) command, which takes the same arguments as `az cloud register`.</span></span>

## <a name="unregister-a-cloud"></a><span data-ttu-id="dc6ac-136">クラウドを登録解除する</span><span class="sxs-lookup"><span data-stu-id="dc6ac-136">Unregister a cloud</span></span>

<span data-ttu-id="dc6ac-137">作成したクラウドが不要になった場合は、次のように、[az cloud unregister](/cli/azure/cloud#az-cloud-unregister) コマンドで登録解除することができます。</span><span class="sxs-lookup"><span data-stu-id="dc6ac-137">If you no longer need a created cloud, it can be unregistered with the [az cloud unregister](/cli/azure/cloud#az-cloud-unregister) command:</span></span>

```azurecli-interactive
az cloud unregister --name MyCloud
```
