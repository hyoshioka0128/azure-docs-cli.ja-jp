---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/19/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 049ad9bd657ed76cf80ba0ab3262028458718dec
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="02ed9-103">Azure CLI 2.0 で使用可能な拡張機能</span><span class="sxs-lookup"><span data-stu-id="02ed9-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="02ed9-104">この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="02ed9-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="02ed9-105">拡張機能の一覧は、CLI から直接入手することもできます。</span><span class="sxs-lookup"><span data-stu-id="02ed9-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="02ed9-106">取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。</span><span class="sxs-lookup"><span data-stu-id="02ed9-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="02ed9-107">Name</span><span class="sxs-lookup"><span data-stu-id="02ed9-107">Name</span></span> | <span data-ttu-id="02ed9-108">バージョン</span><span class="sxs-lookup"><span data-stu-id="02ed9-108">Version</span></span> | <span data-ttu-id="02ed9-109">まとめ</span><span class="sxs-lookup"><span data-stu-id="02ed9-109">Summary</span></span> | <span data-ttu-id="02ed9-110">プレビュー</span><span class="sxs-lookup"><span data-stu-id="02ed9-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="02ed9-111">aem</span><span class="sxs-lookup"><span data-stu-id="02ed9-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="02ed9-112">0.1.1</span></span> | <span data-ttu-id="02ed9-113">Azure Enhanced Monitoring Extension for SAP を管理します</span><span class="sxs-lookup"><span data-stu-id="02ed9-113">Manage Azure Enhanced Monitoring Extensions for SAP</span></span> |  |
| [<span data-ttu-id="02ed9-114">alias</span><span class="sxs-lookup"><span data-stu-id="02ed9-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-115">0.5.0</span><span class="sxs-lookup"><span data-stu-id="02ed9-115">0.5.0</span></span> | <span data-ttu-id="02ed9-116">コマンドのエイリアスをサポートします</span><span class="sxs-lookup"><span data-stu-id="02ed9-116">Support for command aliases</span></span> | <span data-ttu-id="02ed9-117">[はい]</span><span class="sxs-lookup"><span data-stu-id="02ed9-117">Yes</span></span> |
| [<span data-ttu-id="02ed9-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="02ed9-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="02ed9-119">2.2.1</span><span class="sxs-lookup"><span data-stu-id="02ed9-119">2.2.1</span></span> | <span data-ttu-id="02ed9-120">Azure Batch サービスを操作するための追加コマンド</span><span class="sxs-lookup"><span data-stu-id="02ed9-120">Additional commands for working with Azure Batch service</span></span> |  |
| [<span data-ttu-id="02ed9-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="02ed9-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="02ed9-122">0.4.3</span><span class="sxs-lookup"><span data-stu-id="02ed9-122">0.4.3</span></span> | <span data-ttu-id="02ed9-123">Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します</span><span class="sxs-lookup"><span data-stu-id="02ed9-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service</span></span> |  |
| [<span data-ttu-id="02ed9-124">dns</span><span class="sxs-lookup"><span data-stu-id="02ed9-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="02ed9-125">0.0.2</span></span> | <span data-ttu-id="02ed9-126">DNS ゾーン向けの Azure CLI 拡張機能</span><span class="sxs-lookup"><span data-stu-id="02ed9-126">An Azure CLI Extension for DNS zones</span></span> |  |
| [<span data-ttu-id="02ed9-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="02ed9-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="02ed9-128">0.0.5</span></span> | <span data-ttu-id="02ed9-129">リージョン間でイメージをコピーする Azure CLI 拡張機能。</span><span class="sxs-lookup"><span data-stu-id="02ed9-129">An Azure CLI Extension that copies images from region to region.</span></span> |  |
| [<span data-ttu-id="02ed9-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="02ed9-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="02ed9-131">0.1.0</span></span> | <span data-ttu-id="02ed9-132">管理グループ向け Azure CLI 拡張機能</span><span class="sxs-lookup"><span data-stu-id="02ed9-132">An Azure CLI Extension for Management Groups</span></span> |  |
| [<span data-ttu-id="02ed9-133">managementpartner</span><span class="sxs-lookup"><span data-stu-id="02ed9-133">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-134">0.1.2</span><span class="sxs-lookup"><span data-stu-id="02ed9-134">0.1.2</span></span> | <span data-ttu-id="02ed9-135">管理パートナーのプレビューをサポートします</span><span class="sxs-lookup"><span data-stu-id="02ed9-135">Support for Management Partner preview</span></span> |  |
| [<span data-ttu-id="02ed9-136">rdbms</span><span class="sxs-lookup"><span data-stu-id="02ed9-136">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-137">0.0.5</span><span class="sxs-lookup"><span data-stu-id="02ed9-137">0.0.5</span></span> | <span data-ttu-id="02ed9-138">Azure MySQL および Azure PostgreSQL をサポートする Azure CLI 拡張機能。</span><span class="sxs-lookup"><span data-stu-id="02ed9-138">An Azure CLI Extension providing support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="02ed9-139">サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="02ed9-139">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-140">0.1.1</span><span class="sxs-lookup"><span data-stu-id="02ed9-140">0.1.1</span></span> | <span data-ttu-id="02ed9-141">サブスクリプション管理プレビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="02ed9-141">Support for subscription management preview.</span></span> |  |
| [<span data-ttu-id="02ed9-142">webapp</span><span class="sxs-lookup"><span data-stu-id="02ed9-142">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="02ed9-143">0.2.1</span><span class="sxs-lookup"><span data-stu-id="02ed9-143">0.2.1</span></span> | <span data-ttu-id="02ed9-144">appservice のリソースを管理する Azure CLI 拡張機能</span><span class="sxs-lookup"><span data-stu-id="02ed9-144">An Azure CLI Extension to manage appservice resources</span></span> | <span data-ttu-id="02ed9-145">[はい]</span><span class="sxs-lookup"><span data-stu-id="02ed9-145">Yes</span></span> |
