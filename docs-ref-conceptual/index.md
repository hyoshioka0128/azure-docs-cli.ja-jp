---
title: Azure CLI の概要
description: Azure CLI の概要。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 047a953a0ab8ccaf145d56e4d774d2bf9852ed6f
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177727"
---
# <a name="azure-cli"></a><span data-ttu-id="9d2f7-103">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="9d2f7-103">Azure CLI</span></span>

<span data-ttu-id="9d2f7-104">Azure CLI は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-104">The Azure CLI is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="9d2f7-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="9d2f7-106">Azure CLI は簡単に使い始めることができ、Azure Resource Manager を操作対象とする自動化スクリプトを作成するにも最適です。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-106">The Azure CLI is simple to get started with, and best used for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="9d2f7-107">Azure CLI を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-107">Using the Azure CLI, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a><span data-ttu-id="9d2f7-108">実行またはインストール</span><span class="sxs-lookup"><span data-stu-id="9d2f7-108">Run or Install</span></span>

<span data-ttu-id="9d2f7-109">CLI はローカルにインストールできます。また、Azure Cloud Shell を使用してブラウザーで実行したり、Docker コンテナーで実行したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-109">You can install the CLI locally, run it in the browser with Azure Cloud Shell, or run in a Docker container.</span></span>

* <span data-ttu-id="9d2f7-110">Azure Cloud Shell を使用したブラウザーでの実行方法については、「[Azure Cloud Shell の Bash のクイック スタート](/azure/cloud-shell/quickstart)」または「[Azure Cloud Shell の PowerShell のクイック スタート](/azure/cloud-shell/quickstart-powershell)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-110">To run in your browser with Azure Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart) or [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="9d2f7-111">CLI のインストール方法については、「[Azure CLI のインストール](install-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-111">To install the CLI, see [Install the Azure CLI](install-azure-cli.md).</span></span>
* <span data-ttu-id="9d2f7-112">Docker コンテナーとして実行する方法については、「[Docker コンテナーでの Azure CLI の実行](run-azure-cli-docker.md)」を参照してください</span><span class="sxs-lookup"><span data-stu-id="9d2f7-112">To run as a Docker container, see [Run Azure CLI in a Docker Container](run-azure-cli-docker.md)</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="9d2f7-113">Microsoft Learn でスキルを身に付ける</span><span class="sxs-lookup"><span data-stu-id="9d2f7-113">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="9d2f7-114">Azure CLI で仮想マシンを管理する</span><span class="sxs-lookup"><span data-stu-id="9d2f7-114">Manage virtual machines with the Azure CLI</span></span>](/learn/modules/manage-virtual-machines-with-azure-cli/)
- [<span data-ttu-id="9d2f7-115">CLI で Azure サービスを制御する</span><span class="sxs-lookup"><span data-stu-id="9d2f7-115">Control Azure services with the CLI</span></span>](/learn/modules/control-azure-services-with-cli/)
- [<span data-ttu-id="9d2f7-116">対話型学習の詳細...</span><span class="sxs-lookup"><span data-stu-id="9d2f7-116">More interactive learning...</span></span>](/learn/browse/?products=azure-clis)

## <a name="get-started"></a><span data-ttu-id="9d2f7-117">作業開始</span><span class="sxs-lookup"><span data-stu-id="9d2f7-117">Get started</span></span>

<span data-ttu-id="9d2f7-118">CLI の基本については、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-118">Read the [Get Started](get-started-with-azure-cli.md) article to learn the CLI basics.</span></span> <span data-ttu-id="9d2f7-119">次のサンプルでは、一般的なユース ケースが紹介されています。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-119">The following samples demonstrate some common uses cases:</span></span>

- [<span data-ttu-id="9d2f7-120">Linux virtual machines</span><span class="sxs-lookup"><span data-stu-id="9d2f7-120">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9d2f7-121">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="9d2f7-121">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9d2f7-122">Web Apps</span><span class="sxs-lookup"><span data-stu-id="9d2f7-122">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="9d2f7-123">SQL Database</span><span class="sxs-lookup"><span data-stu-id="9d2f7-123">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="9d2f7-124">個々の Azure CLI コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-124">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI command.</span></span>

> [!NOTE]
> <span data-ttu-id="9d2f7-125">以前のバージョンの CLI (Azure クラシック CLI) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-125">If you use the previous version of the CLI (Azure classic CLI), you can continue to use it.</span></span>
> <span data-ttu-id="9d2f7-126">ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-126">However, we recommend updating to use the latest version of the Azure CLI for the best experience.</span></span>
> <span data-ttu-id="9d2f7-127">両方の CLI を使用する場合は、`azure` がクラシック CLI で、`az` が最新の CLI であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="9d2f7-127">If you use both CLIs, remember that `azure` is the classic CLI and that `az` is the most recent CLI.</span></span>
