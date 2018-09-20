---
title: Azure CLI 2.0 の概要
description: Azure CLI 2.0 の概要。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 55c5ea3ad69df60d211cc076e3570e9f07040af7
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388390"
---
# <a name="azure-cli-20"></a><span data-ttu-id="a4c66-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="a4c66-103">Azure CLI 2.0</span></span>

<span data-ttu-id="a4c66-104">Azure CLI 2.0 は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="a4c66-104">The Azure CLI 2.0 is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="a4c66-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="a4c66-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="a4c66-106">Azure CLI 2.0 は簡単に使い始めることができ、Azure Resource Manager を操作対象とする自動化スクリプトを作成するにも最適です。</span><span class="sxs-lookup"><span data-stu-id="a4c66-106">Azure CLI 2.0 is simple to get started with, and best used for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="a4c66-107">Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a4c66-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a><span data-ttu-id="a4c66-108">実行またはインストール</span><span class="sxs-lookup"><span data-stu-id="a4c66-108">Run or Install</span></span>

<span data-ttu-id="a4c66-109">CLI はローカルにインストールできます。また、Azure Cloud Shell を使用してブラウザーで実行したり、Docker コンテナーで実行したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a4c66-109">You can install the CLI locally, run it in the browser with Azure Cloud Shell, or run in a Docker container.</span></span>

* <span data-ttu-id="a4c66-110">Azure Cloud Shell を使用したブラウザーでの実行方法については、「[Azure Cloud Shell の Bash のクイック スタート](/azure/cloud-shell/quickstart)」または「[Azure Cloud Shell の PowerShell のクイック スタート](/azure/cloud-shell/quickstart-powershell)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a4c66-110">To run in your browser with Azure Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart) or [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="a4c66-111">CLI のインストール方法については、[Azure CLI 2.0 のインストール](install-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a4c66-111">To install the CLI, see [Install the Azure CLI 2.0](install-azure-cli.md).</span></span>
* <span data-ttu-id="a4c66-112">Docker コンテナーとして実行する方法については、「[Docker コンテナーでの Azure CLI 2.0 の実行](run-azure-cli-docker.md)」をご覧ください</span><span class="sxs-lookup"><span data-stu-id="a4c66-112">To run as a Docker container, see [Run Azure CLI 2.0 in a Docker Container](run-azure-cli-docker.md)</span></span>

## <a name="get-started"></a><span data-ttu-id="a4c66-113">作業開始</span><span class="sxs-lookup"><span data-stu-id="a4c66-113">Get started</span></span>

<span data-ttu-id="a4c66-114">CLI の基本については、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="a4c66-114">Read the [Get Started](get-started-with-azure-cli.md) article to learn the CLI basics.</span></span> <span data-ttu-id="a4c66-115">次のサンプルでは、一般的なユース ケースが紹介されています。</span><span class="sxs-lookup"><span data-stu-id="a4c66-115">The following samples demonstrate some common uses cases:</span></span>

- [<span data-ttu-id="a4c66-116">Linux virtual machines</span><span class="sxs-lookup"><span data-stu-id="a4c66-116">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a4c66-117">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="a4c66-117">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a4c66-118">Web Apps</span><span class="sxs-lookup"><span data-stu-id="a4c66-118">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a4c66-119">SQL Database</span><span class="sxs-lookup"><span data-stu-id="a4c66-119">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="a4c66-120">個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="a4c66-120">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

> [!NOTE]
> <span data-ttu-id="a4c66-121">以前のバージョンの CLI (Azure CLI 1.0) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a4c66-121">If you use the previous version of the CLI (Azure CLI 1.0), you can continue to use it.</span></span>
> <span data-ttu-id="a4c66-122">ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI 2.0 に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a4c66-122">However, we recommend updating to use the latest version of Azure CLI 2.0 for the best experience.</span></span>
> <span data-ttu-id="a4c66-123">両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="a4c66-123">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
