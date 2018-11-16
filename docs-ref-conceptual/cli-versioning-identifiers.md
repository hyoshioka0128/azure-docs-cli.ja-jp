---
title: 各 Azure CLI 製品の違い
description: Azure CLI 製品の名前とバージョンがどのように設定されているか、およびそのアップグレード方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/12/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 4370616459ad4e466128ff26123c10f55bfdd7d8
ms.sourcegitcommit: 728a050f13d3682122be4a8993596cc4185a45ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2018
ms.locfileid: "51680902"
---
# <a name="differences-between-azure-cli-products"></a><span data-ttu-id="b9cf0-103">各 Azure CLI 製品の違い</span><span class="sxs-lookup"><span data-stu-id="b9cf0-103">Differences between Azure CLI products</span></span>

<span data-ttu-id="b9cf0-104">2018 年 6 月末の時点で、明示的なバージョン番号が Azure CLI 製品名から削除されました。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-104">As of the end of June 2018, explicit version numbers have been removed from Azure CLI product names.</span></span> <span data-ttu-id="b9cf0-105">ドキュメントで "Azure CLI" を使用するように記載されているが、どの製品バージョンを指しているのかが明確ではなかった場合に時折生じていた混乱が、この変更により解消されます。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-105">This change helps eliminate confusion that sometimes showed up in documentation where users were told to use "the Azure CLI" but it was unclear what version of the product was being referenced.</span></span> <span data-ttu-id="b9cf0-106">前の製品名に慣れている方は、どのように変更されたかを以下でご確認ください。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-106">If you're familiar with the old product names, here is how they have changed:</span></span>

* <span data-ttu-id="b9cf0-107">Azure CLI バージョン 2.0 以降は、ただ "Azure CLI" と呼ばれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-107">Azure CLI versions 2.0 and later are now referred to only as "Azure CLI."</span></span>
* <span data-ttu-id="b9cf0-108">それよりも前のバージョンの Azure CLI (1.x 以下) は、"Azure クラシック CLI" と呼ばれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-108">Earlier Azure CLI versions (1.x and lower) are now referred to as "Azure classic CLI."</span></span>

<span data-ttu-id="b9cf0-109">名前が Azure クラシック CLI に変更されたことで、このツールがクラシック デプロイ モデルのみでの使用を意図していることが明確になっています。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-109">The name change to Azure classic CLI makes it clear that this tool is meant to be used only with the classic deployment model.</span></span> <span data-ttu-id="b9cf0-110">また、クラシック CLI については、今後は更新も保守も行われません。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-110">The classic CLI is also no longer updated or maintained.</span></span> <span data-ttu-id="b9cf0-111">この理由やその他のさまざまな理由から、クラシック デプロイは、Azure Resource Manager モデルを使用できるように移動し、最新バージョンの Azure CLI に移行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-111">For this reason, and many more, it's recommended that you move any classic deployments to use the Azure Resource Manager model and migrate to the latest available version of the Azure CLI.</span></span>

<span data-ttu-id="b9cf0-112">クラシック CLI を使用している場合は、以下の記事で移行プロセスについてご確認ください。</span><span class="sxs-lookup"><span data-stu-id="b9cf0-112">If you are still using the classic CLI, you can learn about the process of migrating in the following articles:</span></span>

* [<span data-ttu-id="b9cf0-113">クラシックから Azure Resource Manager に移行する</span><span class="sxs-lookup"><span data-stu-id="b9cf0-113">Migrate from Classic to Azure Resource Manager</span></span>](/azure/virtual-machines/linux/migration-classic-resource-manager-overview)
* [<span data-ttu-id="b9cf0-114">Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="b9cf0-114">Install the Azure CLI</span></span>](install-azure-cli.md)
* [<span data-ttu-id="b9cf0-115">Azure クラシック CLI から Azure CLI への移行</span><span class="sxs-lookup"><span data-stu-id="b9cf0-115">Migrating from Azure classic CLI to Azure CLI</span></span>](https://github.com/Azure/azure-cli/blob/dev/doc/classic_cli_migration.md)
