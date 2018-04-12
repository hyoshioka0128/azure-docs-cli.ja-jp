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
ms.openlocfilehash: 794ea005816b33fe78ca6c15b86dcf94ace3eaa8
ms.sourcegitcommit: c9da729f4a42a839f13106f7589deaa0ca19cc4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="405da-103">Azure CLI 2.0 で使用可能な拡張機能</span><span class="sxs-lookup"><span data-stu-id="405da-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="405da-104">この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="405da-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="405da-105">拡張機能の一覧は、CLI から直接入手することもできます。</span><span class="sxs-lookup"><span data-stu-id="405da-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="405da-106">取得するには、[az extension list-available](/cli/azure/extension#az-extension-list-available) を実行します。</span><span class="sxs-lookup"><span data-stu-id="405da-106">To get it, run [az extension list-available](/cli/azure/extension#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="405da-107">Name</span><span class="sxs-lookup"><span data-stu-id="405da-107">Name</span></span> | <span data-ttu-id="405da-108">バージョン</span><span class="sxs-lookup"><span data-stu-id="405da-108">Version</span></span> | <span data-ttu-id="405da-109">まとめ</span><span class="sxs-lookup"><span data-stu-id="405da-109">Summary</span></span> | <span data-ttu-id="405da-110">プレビュー</span><span class="sxs-lookup"><span data-stu-id="405da-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="405da-111">aem</span><span class="sxs-lookup"><span data-stu-id="405da-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="405da-112">0.1.1</span></span> | <span data-ttu-id="405da-113">Azure Enhanced Monitoring Extension for SAP を管理します。</span><span class="sxs-lookup"><span data-stu-id="405da-113">Manage Azure Enhanced Monitoring Extensions for SAP.</span></span> |  |
| [<span data-ttu-id="405da-114">alias</span><span class="sxs-lookup"><span data-stu-id="405da-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-115">0.3.0</span><span class="sxs-lookup"><span data-stu-id="405da-115">0.3.0</span></span> | <span data-ttu-id="405da-116">コマンドのエイリアスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-116">Support for command aliases.</span></span> | <span data-ttu-id="405da-117">[はい]</span><span class="sxs-lookup"><span data-stu-id="405da-117">Yes</span></span> |
| [<span data-ttu-id="405da-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="405da-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="405da-119">2.1.0</span><span class="sxs-lookup"><span data-stu-id="405da-119">2.1.0</span></span> | <span data-ttu-id="405da-120">その他のプレビューの Azure Batch コマンドです。</span><span class="sxs-lookup"><span data-stu-id="405da-120">Additional preview Azure Batch commands.</span></span> |  |
| [<span data-ttu-id="405da-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="405da-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="405da-122">0.4.1</span><span class="sxs-lookup"><span data-stu-id="405da-122">0.4.1</span></span> | <span data-ttu-id="405da-123">Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します。</span><span class="sxs-lookup"><span data-stu-id="405da-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service.</span></span> |  |
| [<span data-ttu-id="405da-124">dns</span><span class="sxs-lookup"><span data-stu-id="405da-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="405da-125">0.0.2</span></span> | <span data-ttu-id="405da-126">Azure プライベート DNS のパブリック プレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-126">Support for the Azure Private DNS Public Preview.</span></span> |  |
| [<span data-ttu-id="405da-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="405da-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="405da-128">0.0.5</span></span> | <span data-ttu-id="405da-129">リージョン間でイメージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="405da-129">Copy images from region to region.</span></span> |  |
| [<span data-ttu-id="405da-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="405da-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="405da-131">0.1.0</span></span> | <span data-ttu-id="405da-132">管理グループのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-132">Support for Management Groups preview.</span></span> | <span data-ttu-id="405da-133">[はい]</span><span class="sxs-lookup"><span data-stu-id="405da-133">Yes</span></span> |
| [<span data-ttu-id="405da-134">managementpartner</span><span class="sxs-lookup"><span data-stu-id="405da-134">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-135">0.1.2</span><span class="sxs-lookup"><span data-stu-id="405da-135">0.1.2</span></span> | <span data-ttu-id="405da-136">管理パートナーのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-136">Support for Management Partner preview.</span></span> | <span data-ttu-id="405da-137">[はい]</span><span class="sxs-lookup"><span data-stu-id="405da-137">Yes</span></span> |
| [<span data-ttu-id="405da-138">rdbms</span><span class="sxs-lookup"><span data-stu-id="405da-138">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-139">0.0.5</span><span class="sxs-lookup"><span data-stu-id="405da-139">0.0.5</span></span> | <span data-ttu-id="405da-140">Azure MySQL および Azure PostgreSQL をサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-140">Support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="405da-141">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="405da-141">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-142">0.1.1</span><span class="sxs-lookup"><span data-stu-id="405da-142">0.1.1</span></span> | <span data-ttu-id="405da-143">サブスクリプション定義のプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="405da-143">Support for subscription definitions preview.</span></span> | <span data-ttu-id="405da-144">[はい]</span><span class="sxs-lookup"><span data-stu-id="405da-144">Yes</span></span> |
| [<span data-ttu-id="405da-145">webapp</span><span class="sxs-lookup"><span data-stu-id="405da-145">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="405da-146">0.2.0</span><span class="sxs-lookup"><span data-stu-id="405da-146">0.2.0</span></span> | <span data-ttu-id="405da-147">appservice リソースを作成してデプロイします。</span><span class="sxs-lookup"><span data-stu-id="405da-147">Create and deploy appservice resources.</span></span> | <span data-ttu-id="405da-148">[はい]</span><span class="sxs-lookup"><span data-stu-id="405da-148">Yes</span></span> |
