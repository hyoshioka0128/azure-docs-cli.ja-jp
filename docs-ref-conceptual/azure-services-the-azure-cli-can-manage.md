---
title: Azure CLI で管理できる Azure サービス
description: Azure CLI リファレンス、App Configuration、App Service、Active Directory (AD)、Backup、Cognitive Search、Cosmos DB、Data Lake Storage、Database、MariaDB、MySQL、PostgreSQL、PostgreSQL、DevOps、DevTest Labs、DNS、Functions、IoT、IoT Central、IoT Edge、IoT Hub、Kubernetes Service (AKS)、Lab Services、Machine Learning、Managed Applications、Private Link、Resource Manager、Spring Cloud、SQL Database、Batch、Cognitive Services、Container Instances、Container Registry、Data Lake Analytics、Event Grid、Event Hubs、HDInsight、Key Vault、Load Balancer、Managed Disks、Media Services、Notification Hubs、Service Bus、Service Fabric、Storage アカウント、Traffic Manager、Virtual Machine Scale Sets、Virtual Network、Compute、ネットワーク、モノのインターネット、開発者ツール、データベース、Analytics、管理とガバナンス、ハイブリッド、ストレージ、セキュリティ、AI、AI + 機械学習を提供するサービスへのリンク
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 03/01/2020
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 9f754e5223da0c2d2d9e4b0714ff09f8b900e361
ms.sourcegitcommit: 93d8137f37e974f7d314a0b1deb65ac563c2e2c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "80075969"
---
# <a name="azure-services-the-azure-cli-can-manage"></a><span data-ttu-id="1904f-103">Azure CLI で管理できる Azure サービス</span><span class="sxs-lookup"><span data-stu-id="1904f-103">Azure services the Azure CLI can manage</span></span>

<span data-ttu-id="1904f-104">Azure CLI は多くの Azure サービスで利用でき、Azure リソースを作成して管理するための柔軟で強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="1904f-104">The Azure CLI is available across many Azure services, and is a flexible yet powerful tool to create and manage Azure resources.</span></span>  <span data-ttu-id="1904f-105">この記事では、Azure CLI が管理できる Azure サービスの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="1904f-105">This article provides the list of Azure services the Azure CLI can manage.</span></span>

<span data-ttu-id="1904f-106">次のサービスでは Azure CLI リファレンスを利用できます。</span><span class="sxs-lookup"><span data-stu-id="1904f-106">Azure CLI references are available for the following:</span></span>  

| <span data-ttu-id="1904f-107">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="1904f-107">Category</span></span> | <span data-ttu-id="1904f-108">サービスのドキュメント</span><span class="sxs-lookup"><span data-stu-id="1904f-108">Service Documentation</span></span>
|-|-|
|<span data-ttu-id="1904f-109">AI + 機械学習</span><span class="sxs-lookup"><span data-stu-id="1904f-109">AI + Machine Learning</span></span>| [<span data-ttu-id="1904f-110">Azure Machine Learning</span><span class="sxs-lookup"><span data-stu-id="1904f-110">Azure Machine Learning</span></span>](/azure/machine-learning/)
||[<span data-ttu-id="1904f-111">Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="1904f-111">Cognitive Services</span></span>](/azure/cognitive-services/)
|<span data-ttu-id="1904f-112">Analytics</span><span class="sxs-lookup"><span data-stu-id="1904f-112">Analytics</span></span>|[<span data-ttu-id="1904f-113">Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="1904f-113">Azure Data Lake Storage</span></span>](/azure/storage/blobs/data-lake-storage-introduction/)
||[<span data-ttu-id="1904f-114">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1904f-114">Data Lake Analytics</span></span>](/azure/data-lake-analytics/)
||[<span data-ttu-id="1904f-115">Event Hubs</span><span class="sxs-lookup"><span data-stu-id="1904f-115">Event Hubs</span></span>](/azure/event-hubs/)
||[<span data-ttu-id="1904f-116">HDInsight</span><span class="sxs-lookup"><span data-stu-id="1904f-116">HDInsight</span></span>](/azure/hdinsight/)
|<span data-ttu-id="1904f-117">ブロックチェーン</span><span class="sxs-lookup"><span data-stu-id="1904f-117">Blockchain</span></span>|[<span data-ttu-id="1904f-118">Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="1904f-118">Azure Cosmos DB</span></span>](/azure/cosmos-db/)
|<span data-ttu-id="1904f-119">Compute</span><span class="sxs-lookup"><span data-stu-id="1904f-119">Compute</span></span>|[<span data-ttu-id="1904f-120">App Service</span><span class="sxs-lookup"><span data-stu-id="1904f-120">App Service</span></span>](/azure/app-service/)
||[<span data-ttu-id="1904f-121">Azure Functions</span><span class="sxs-lookup"><span data-stu-id="1904f-121">Azure Functions</span></span>](/azure/azure-functions/)
||[<span data-ttu-id="1904f-122">Azure Kubernetes Service (AKS)</span><span class="sxs-lookup"><span data-stu-id="1904f-122">Azure Kubernetes Service (AKS)</span></span>](/azure/aks/)
||[<span data-ttu-id="1904f-123">Azure Spring Cloud</span><span class="sxs-lookup"><span data-stu-id="1904f-123">Azure Spring Cloud</span></span>](/azure/spring-cloud/)
||[<span data-ttu-id="1904f-124">Batch</span><span class="sxs-lookup"><span data-stu-id="1904f-124">Batch</span></span>](/azure/batch/)
||[<span data-ttu-id="1904f-125">Container Instances</span><span class="sxs-lookup"><span data-stu-id="1904f-125">Container Instances</span></span>](/azure/container-instances/)
||[<span data-ttu-id="1904f-126">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1904f-126">Service Fabric</span></span>](/azure/service-fabric/)
||[<span data-ttu-id="1904f-127">Virtual Machine Scale Sets</span><span class="sxs-lookup"><span data-stu-id="1904f-127">Virtual Machine Scale Sets</span></span>](/azure/virtual-machine-scale-sets/)
|<span data-ttu-id="1904f-128">Containers</span><span class="sxs-lookup"><span data-stu-id="1904f-128">Containers</span></span>|[<span data-ttu-id="1904f-129">Azure Functions</span><span class="sxs-lookup"><span data-stu-id="1904f-129">Azure Functions</span></span>](/azure/azure-functions/)
||[<span data-ttu-id="1904f-130">Azure Kubernetes Service (AKS)</span><span class="sxs-lookup"><span data-stu-id="1904f-130">Azure Kubernetes Service (AKS)</span></span>](/azure/aks/)
||[<span data-ttu-id="1904f-131">Container Instances</span><span class="sxs-lookup"><span data-stu-id="1904f-131">Container Instances</span></span>](/azure/container-instances/)
||[<span data-ttu-id="1904f-132">Container Registry</span><span class="sxs-lookup"><span data-stu-id="1904f-132">Container Registry</span></span>](/azure/container-registry/)
||[<span data-ttu-id="1904f-133">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1904f-133">Service Fabric</span></span>](/azure/service-fabric/)
|<span data-ttu-id="1904f-134">データベース</span><span class="sxs-lookup"><span data-stu-id="1904f-134">Databases</span></span>|[<span data-ttu-id="1904f-135">Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="1904f-135">Azure Cosmos DB</span></span>](/azure/cosmos-db/)
||[<span data-ttu-id="1904f-136">Azure Database for MariaDB</span><span class="sxs-lookup"><span data-stu-id="1904f-136">Azure Database for MariaDB</span></span>](/azure/mariadb/)
||[<span data-ttu-id="1904f-137">Azure Database for MySQL</span><span class="sxs-lookup"><span data-stu-id="1904f-137">Azure Database for MySQL</span></span>](/azure/mysql/)
||[<span data-ttu-id="1904f-138">Azure Database for PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="1904f-138">Azure Database for PostgreSQL</span></span>](/azure/postgresql/)
||[<span data-ttu-id="1904f-139">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="1904f-139">Azure SQL Database</span></span>](/azure/sql-database/)
|<span data-ttu-id="1904f-140">開発者ツール</span><span class="sxs-lookup"><span data-stu-id="1904f-140">Developer Tools</span></span>|[<span data-ttu-id="1904f-141">App Configuration</span><span class="sxs-lookup"><span data-stu-id="1904f-141">App Configuration</span></span>](/azure/azure-app-configuration/)
||[<span data-ttu-id="1904f-142">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="1904f-142">Azure DevOps</span></span>](/azure/devops/)
||[<span data-ttu-id="1904f-143">Azure DevTest Labs</span><span class="sxs-lookup"><span data-stu-id="1904f-143">Azure DevTest Labs</span></span>](/azure/lab-services/)
||[<span data-ttu-id="1904f-144">Azure Lab Services</span><span class="sxs-lookup"><span data-stu-id="1904f-144">Azure Lab Services</span></span>](/azure/lab-services/classroom-labs/)
|<span data-ttu-id="1904f-145">DevOps</span><span class="sxs-lookup"><span data-stu-id="1904f-145">DevOps</span></span>|[<span data-ttu-id="1904f-146">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="1904f-146">Azure DevOps</span></span>](/azure/devops/)
||[<span data-ttu-id="1904f-147">Azure DevTest Labs</span><span class="sxs-lookup"><span data-stu-id="1904f-147">Azure DevTest Labs</span></span>](/azure/lab-services/)
|<span data-ttu-id="1904f-148">ハイブリッド</span><span class="sxs-lookup"><span data-stu-id="1904f-148">Hybrid</span></span>|[<span data-ttu-id="1904f-149">Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="1904f-149">Azure Active Directory (AD)</span></span>](/azure/active-directory/)
||[<span data-ttu-id="1904f-150">Azure Database for PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="1904f-150">Azure Database for PostgreSQL</span></span>](/azure/postgresql/)
||[<span data-ttu-id="1904f-151">Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="1904f-151">Azure DevOps</span></span>](/azure/devops/)
||[<span data-ttu-id="1904f-152">Azure IoT Edge</span><span class="sxs-lookup"><span data-stu-id="1904f-152">Azure IoT Edge</span></span>](/azure/iot-edge/)
||[<span data-ttu-id="1904f-153">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="1904f-153">Azure SQL Database</span></span>](/azure/sql-database/)
|<span data-ttu-id="1904f-154">ID</span><span class="sxs-lookup"><span data-stu-id="1904f-154">Identity</span></span>|[<span data-ttu-id="1904f-155">Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="1904f-155">Azure Active Directory (AD)</span></span>](/azure/active-directory/)
|<span data-ttu-id="1904f-156">統合</span><span class="sxs-lookup"><span data-stu-id="1904f-156">Integration</span></span>|[<span data-ttu-id="1904f-157">Event Grid</span><span class="sxs-lookup"><span data-stu-id="1904f-157">Event Grid</span></span>](/azure/event-grid/)
||[<span data-ttu-id="1904f-158">Service Bus</span><span class="sxs-lookup"><span data-stu-id="1904f-158">Service Bus</span></span>](/azure/service-bus/)
|<span data-ttu-id="1904f-159">モノのインターネット (IoT)</span><span class="sxs-lookup"><span data-stu-id="1904f-159">Internet of Things</span></span>|[<span data-ttu-id="1904f-160">Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="1904f-160">Azure Cosmos DB</span></span>](/azure/cosmos-db/)
||[<span data-ttu-id="1904f-161">Azure Functions</span><span class="sxs-lookup"><span data-stu-id="1904f-161">Azure Functions</span></span>](/azure/azure-functions/)
||[<span data-ttu-id="1904f-162">Azure IoT Central</span><span class="sxs-lookup"><span data-stu-id="1904f-162">Azure IoT Central</span></span>](/azure/iot-central/)
||[<span data-ttu-id="1904f-163">Azure IoT Edge</span><span class="sxs-lookup"><span data-stu-id="1904f-163">Azure IoT Edge</span></span>](/azure/iot-edge/)
||[<span data-ttu-id="1904f-164">Azure IoT Hub</span><span class="sxs-lookup"><span data-stu-id="1904f-164">Azure IoT Hub</span></span>](/azure/iot-hub/)
||[<span data-ttu-id="1904f-165">Azure Machine Learning</span><span class="sxs-lookup"><span data-stu-id="1904f-165">Azure Machine Learning</span></span>](/azure/machine-learning/)
||[<span data-ttu-id="1904f-166">Event Grid</span><span class="sxs-lookup"><span data-stu-id="1904f-166">Event Grid</span></span>](/azure/event-grid/)
|<span data-ttu-id="1904f-167">管理とガバナンス</span><span class="sxs-lookup"><span data-stu-id="1904f-167">Management and Governance</span></span>|[<span data-ttu-id="1904f-168">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="1904f-168">Azure Backup</span></span>](/azure/backup/)
||[<span data-ttu-id="1904f-169">Azure Managed Applications</span><span class="sxs-lookup"><span data-stu-id="1904f-169">Azure Managed Applications</span></span>](/azure/azure-resource-manager/managed-applications/)
||[<span data-ttu-id="1904f-170">Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="1904f-170">Azure Resource Manager</span></span>](/azure/azure-resource-manager/)
||[<span data-ttu-id="1904f-171">Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="1904f-171">Traffic Manager</span></span>](/azure/traffic-manager/)
|<span data-ttu-id="1904f-172">メディア</span><span class="sxs-lookup"><span data-stu-id="1904f-172">Media</span></span>|[<span data-ttu-id="1904f-173">Media Services</span><span class="sxs-lookup"><span data-stu-id="1904f-173">Media Services</span></span>](/azure/media-services/)
|<span data-ttu-id="1904f-174">モバイル</span><span class="sxs-lookup"><span data-stu-id="1904f-174">Mobile</span></span>|[<span data-ttu-id="1904f-175">App Service</span><span class="sxs-lookup"><span data-stu-id="1904f-175">App Service</span></span>](/azure/app-service/)
|<span data-ttu-id="1904f-176">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="1904f-176">Networking</span></span>|[<span data-ttu-id="1904f-177">Azure DNS</span><span class="sxs-lookup"><span data-stu-id="1904f-177">Azure DNS</span></span>](/azure/dns/)
||[<span data-ttu-id="1904f-178">Azure Private Link</span><span class="sxs-lookup"><span data-stu-id="1904f-178">Azure Private Link</span></span>](/azure/private-link/)
||[<span data-ttu-id="1904f-179">Load Balancer</span><span class="sxs-lookup"><span data-stu-id="1904f-179">Load Balancer</span></span>](/azure/load-balancer/)
||[<span data-ttu-id="1904f-180">Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="1904f-180">Traffic Manager</span></span>](/azure/traffic-manager/)
||[<span data-ttu-id="1904f-181">Virtual Network</span><span class="sxs-lookup"><span data-stu-id="1904f-181">Virtual Network</span></span>](/azure/virtual-network/)
|<span data-ttu-id="1904f-182">Security</span><span class="sxs-lookup"><span data-stu-id="1904f-182">Security</span></span>|[<span data-ttu-id="1904f-183">Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="1904f-183">Azure Active Directory (AD)</span></span>](/azure/active-directory/)
||[<span data-ttu-id="1904f-184">Key Vault</span><span class="sxs-lookup"><span data-stu-id="1904f-184">Key Vault</span></span>](/azure/key-vault/)
|<span data-ttu-id="1904f-185">ストレージ</span><span class="sxs-lookup"><span data-stu-id="1904f-185">Storage</span></span>|[<span data-ttu-id="1904f-186">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="1904f-186">Azure Backup</span></span>](/azure/backup/)
||[<span data-ttu-id="1904f-187">Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="1904f-187">Azure Data Lake Storage</span></span>](/azure/storage/blobs/data-lake-storage-introduction/)
||[<span data-ttu-id="1904f-188">Managed Disks</span><span class="sxs-lookup"><span data-stu-id="1904f-188">Managed Disks</span></span>](/azure/virtual-machines/windows/managed-disks-overview/)
||[<span data-ttu-id="1904f-189">ストレージ アカウント</span><span class="sxs-lookup"><span data-stu-id="1904f-189">Storage Accounts</span></span>](/azure/storage/common/storage-account-overview/)
|<span data-ttu-id="1904f-190">Web</span><span class="sxs-lookup"><span data-stu-id="1904f-190">Web</span></span>|[<span data-ttu-id="1904f-191">App Service</span><span class="sxs-lookup"><span data-stu-id="1904f-191">App Service</span></span>](/azure/app-service/)
||[<span data-ttu-id="1904f-192">Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="1904f-192">Azure Cognitive Search</span></span>](/azure/search/)
||[<span data-ttu-id="1904f-193">Azure Spring Cloud</span><span class="sxs-lookup"><span data-stu-id="1904f-193">Azure Spring Cloud</span></span>](/azure/spring-cloud/)
||[<span data-ttu-id="1904f-194">Notification Hubs</span><span class="sxs-lookup"><span data-stu-id="1904f-194">Notification Hubs</span></span>](/azure/notification-hubs/)

## <a name="see-also"></a><span data-ttu-id="1904f-195">関連項目</span><span class="sxs-lookup"><span data-stu-id="1904f-195">See also</span></span>

- [<span data-ttu-id="1904f-196">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="1904f-196">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
- [<span data-ttu-id="1904f-197">Azure CLI の完全なコマンド リファレンス一覧</span><span class="sxs-lookup"><span data-stu-id="1904f-197">Full command reference list for the Azure CLI</span></span>](/cli/azure/reference-index)
- [<span data-ttu-id="1904f-198">Azure CLI の使用に関する人気のある記事</span><span class="sxs-lookup"><span data-stu-id="1904f-198">Popular articles on using the Azure CLI</span></span>](popular-articles-using-the-azure-cli.md)
