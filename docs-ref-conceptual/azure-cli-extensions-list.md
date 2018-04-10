---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/02/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e7cf22d1611c224e1d7af351210e12fe0124fad0
ms.sourcegitcommit: 26e0816dad17cc3584d1724493feecf5f5faa1f5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="2a5d8-103">Azure CLI 2.0 で使用可能な拡張機能</span><span class="sxs-lookup"><span data-stu-id="2a5d8-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="2a5d8-104">この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="2a5d8-105">拡張機能の一覧は、CLI から直接入手することもできます。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="2a5d8-106">取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="2a5d8-107">Name</span><span class="sxs-lookup"><span data-stu-id="2a5d8-107">Name</span></span> | <span data-ttu-id="2a5d8-108">バージョン</span><span class="sxs-lookup"><span data-stu-id="2a5d8-108">Version</span></span> | <span data-ttu-id="2a5d8-109">まとめ</span><span class="sxs-lookup"><span data-stu-id="2a5d8-109">Summary</span></span> | <span data-ttu-id="2a5d8-110">プレビュー</span><span class="sxs-lookup"><span data-stu-id="2a5d8-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="2a5d8-111">aem</span><span class="sxs-lookup"><span data-stu-id="2a5d8-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="2a5d8-112">0.1.1</span></span> | <span data-ttu-id="2a5d8-113">Azure Enhanced Monitoring Extension for SAP を管理します。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-113">Manage Azure Enhanced Monitoring Extensions for SAP.</span></span> |  |
| [<span data-ttu-id="2a5d8-114">alias</span><span class="sxs-lookup"><span data-stu-id="2a5d8-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-115">0.3.0</span><span class="sxs-lookup"><span data-stu-id="2a5d8-115">0.3.0</span></span> | <span data-ttu-id="2a5d8-116">コマンドのエイリアスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-116">Support for command aliases.</span></span> | <span data-ttu-id="2a5d8-117">[はい]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-117">Yes</span></span> |
| [<span data-ttu-id="2a5d8-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="2a5d8-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="2a5d8-119">2.1.0</span><span class="sxs-lookup"><span data-stu-id="2a5d8-119">2.1.0</span></span> | <span data-ttu-id="2a5d8-120">その他のプレビューの Azure Batch コマンドです。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-120">Additional preview Azure Batch commands.</span></span> |  |
| [<span data-ttu-id="2a5d8-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="2a5d8-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="2a5d8-122">0.4.1</span><span class="sxs-lookup"><span data-stu-id="2a5d8-122">0.4.1</span></span> | <span data-ttu-id="2a5d8-123">Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service.</span></span> |  |
| [<span data-ttu-id="2a5d8-124">dns</span><span class="sxs-lookup"><span data-stu-id="2a5d8-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="2a5d8-125">0.0.2</span></span> | <span data-ttu-id="2a5d8-126">Azure プライベート DNS のパブリック プレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-126">Support for the Azure Private DNS Public Preview.</span></span> |  |
| [<span data-ttu-id="2a5d8-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="2a5d8-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="2a5d8-128">0.0.5</span></span> | <span data-ttu-id="2a5d8-129">リージョン間でイメージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-129">Copy images from region to region.</span></span> |  |
| [<span data-ttu-id="2a5d8-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="2a5d8-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="2a5d8-131">0.1.0</span></span> | <span data-ttu-id="2a5d8-132">管理グループのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-132">Support for Management Groups preview.</span></span> | <span data-ttu-id="2a5d8-133">[はい]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-133">Yes</span></span> |
| [<span data-ttu-id="2a5d8-134">managementpartner</span><span class="sxs-lookup"><span data-stu-id="2a5d8-134">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-135">0.1.2</span><span class="sxs-lookup"><span data-stu-id="2a5d8-135">0.1.2</span></span> | <span data-ttu-id="2a5d8-136">管理パートナーのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-136">Support for Management Partner preview.</span></span> | <span data-ttu-id="2a5d8-137">[はい]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-137">Yes</span></span> |
| [<span data-ttu-id="2a5d8-138">rdbms</span><span class="sxs-lookup"><span data-stu-id="2a5d8-138">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-139">0.0.5</span><span class="sxs-lookup"><span data-stu-id="2a5d8-139">0.0.5</span></span> | <span data-ttu-id="2a5d8-140">Azure MySQL および Azure PostgreSQL をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-140">Support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="2a5d8-141">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="2a5d8-141">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-142">0.1.1</span><span class="sxs-lookup"><span data-stu-id="2a5d8-142">0.1.1</span></span> | <span data-ttu-id="2a5d8-143">サブスクリプション定義のプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-143">Support for subscription definitions preview.</span></span> | <span data-ttu-id="2a5d8-144">[はい]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-144">Yes</span></span> |
| [<span data-ttu-id="2a5d8-145">webapp</span><span class="sxs-lookup"><span data-stu-id="2a5d8-145">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2a5d8-146">0.2.0</span><span class="sxs-lookup"><span data-stu-id="2a5d8-146">0.2.0</span></span> | <span data-ttu-id="2a5d8-147">appservice リソースを作成してデプロイします。</span><span class="sxs-lookup"><span data-stu-id="2a5d8-147">Create and deploy appservice resources.</span></span> | <span data-ttu-id="2a5d8-148">[はい]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-148">Yes</span></span> |
