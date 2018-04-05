---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 03/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: ceca7ed92435ab03b196e60dee37195330f6f3c7
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="ed141-103">Azure CLI 2.0 で使用可能な拡張機能</span><span class="sxs-lookup"><span data-stu-id="ed141-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="ed141-104">この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="ed141-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="ed141-105">拡張機能の一覧は、CLI から直接入手することもできます。</span><span class="sxs-lookup"><span data-stu-id="ed141-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="ed141-106">取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed141-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="ed141-107">Name</span><span class="sxs-lookup"><span data-stu-id="ed141-107">Name</span></span> | <span data-ttu-id="ed141-108">バージョン</span><span class="sxs-lookup"><span data-stu-id="ed141-108">Version</span></span> | <span data-ttu-id="ed141-109">まとめ</span><span class="sxs-lookup"><span data-stu-id="ed141-109">Summary</span></span> | <span data-ttu-id="ed141-110">プレビュー</span><span class="sxs-lookup"><span data-stu-id="ed141-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="ed141-111">aem</span><span class="sxs-lookup"><span data-stu-id="ed141-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-112">0.1.0</span><span class="sxs-lookup"><span data-stu-id="ed141-112">0.1.0</span></span> | <span data-ttu-id="ed141-113">Azure Enhanced Monitoring Extension for SAP を管理します。</span><span class="sxs-lookup"><span data-stu-id="ed141-113">Manage Azure Enhanced Monitoring Extensions for SAP.</span></span> |  |
| [<span data-ttu-id="ed141-114">alias</span><span class="sxs-lookup"><span data-stu-id="ed141-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-115">0.2.0</span><span class="sxs-lookup"><span data-stu-id="ed141-115">0.2.0</span></span> | <span data-ttu-id="ed141-116">コマンドのエイリアスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-116">Support for command aliases.</span></span> |  |
| [<span data-ttu-id="ed141-117">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="ed141-117">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="ed141-118">2.1.0</span><span class="sxs-lookup"><span data-stu-id="ed141-118">2.1.0</span></span> | <span data-ttu-id="ed141-119">その他のプレビューの Azure Batch コマンドです。</span><span class="sxs-lookup"><span data-stu-id="ed141-119">Additional preview Azure Batch commands.</span></span> |  |
| [<span data-ttu-id="ed141-120">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="ed141-120">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="ed141-121">0.4.1</span><span class="sxs-lookup"><span data-stu-id="ed141-121">0.4.1</span></span> | <span data-ttu-id="ed141-122">Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します。</span><span class="sxs-lookup"><span data-stu-id="ed141-122">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service.</span></span> |  |
| [<span data-ttu-id="ed141-123">dns</span><span class="sxs-lookup"><span data-stu-id="ed141-123">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-124">0.0.1</span><span class="sxs-lookup"><span data-stu-id="ed141-124">0.0.1</span></span> | <span data-ttu-id="ed141-125">Azure プライベート DNS のパブリック プレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-125">Support for the Azure Private DNS Public Preview.</span></span> |  |
| [<span data-ttu-id="ed141-126">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="ed141-126">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-127">0.0.5</span><span class="sxs-lookup"><span data-stu-id="ed141-127">0.0.5</span></span> | <span data-ttu-id="ed141-128">リージョン間でイメージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ed141-128">Copy images from region to region.</span></span> |  |
| [<span data-ttu-id="ed141-129">managementgroups</span><span class="sxs-lookup"><span data-stu-id="ed141-129">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-130">0.1.0</span><span class="sxs-lookup"><span data-stu-id="ed141-130">0.1.0</span></span> | <span data-ttu-id="ed141-131">管理グループのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-131">Support for Management Groups preview.</span></span> | <span data-ttu-id="ed141-132">[はい]</span><span class="sxs-lookup"><span data-stu-id="ed141-132">Yes</span></span> |
| [<span data-ttu-id="ed141-133">managementpartner</span><span class="sxs-lookup"><span data-stu-id="ed141-133">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-134">0.1.0</span><span class="sxs-lookup"><span data-stu-id="ed141-134">0.1.0</span></span> | <span data-ttu-id="ed141-135">管理パートナーのプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-135">Support for Management Partner preview.</span></span> | <span data-ttu-id="ed141-136">[はい]</span><span class="sxs-lookup"><span data-stu-id="ed141-136">Yes</span></span> |
| [<span data-ttu-id="ed141-137">rdbms</span><span class="sxs-lookup"><span data-stu-id="ed141-137">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-138">0.0.4</span><span class="sxs-lookup"><span data-stu-id="ed141-138">0.0.4</span></span> | <span data-ttu-id="ed141-139">Azure MySQL および Azure PostgreSQL をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-139">Support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="ed141-140">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="ed141-140">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-141">0.1.0</span><span class="sxs-lookup"><span data-stu-id="ed141-141">0.1.0</span></span> | <span data-ttu-id="ed141-142">サブスクリプション定義のプレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed141-142">Support for subscription definitions preview.</span></span> | <span data-ttu-id="ed141-143">[はい]</span><span class="sxs-lookup"><span data-stu-id="ed141-143">Yes</span></span> |
| [<span data-ttu-id="ed141-144">webapp</span><span class="sxs-lookup"><span data-stu-id="ed141-144">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="ed141-145">0.2.0</span><span class="sxs-lookup"><span data-stu-id="ed141-145">0.2.0</span></span> | <span data-ttu-id="ed141-146">appservice リソースを作成してデプロイします。</span><span class="sxs-lookup"><span data-stu-id="ed141-146">Create and deploy appservice resources.</span></span> | <span data-ttu-id="ed141-147">[はい]</span><span class="sxs-lookup"><span data-stu-id="ed141-147">Yes</span></span> |
