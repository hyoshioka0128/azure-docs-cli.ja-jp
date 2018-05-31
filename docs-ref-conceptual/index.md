---
title: Azure CLI 2.0
description: Azure CLI 2.0 の概要。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 9b6f7a5c79033c0b0bec2bf8b56eb40831484f1a
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2018
ms.locfileid: "34306252"
---
# <a name="azure-cli-20"></a><span data-ttu-id="d9728-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="d9728-103">Azure CLI 2.0</span></span>

<span data-ttu-id="d9728-104">Azure CLI 2.0 は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="d9728-104">The Azure CLI 2.0 is Microsoft's cross-platform command line experience for managing Azure resources.</span></span>
<span data-ttu-id="d9728-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="d9728-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="d9728-106">Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="d9728-106">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="d9728-107">Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d9728-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="d9728-108">[Cloud Shell](/azure/cloud-shell/overview) を使用して CLI をブラウザーで実行することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)することもできます。</span><span class="sxs-lookup"><span data-stu-id="d9728-108">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="d9728-109">CLI を実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="d9728-109">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="d9728-110">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d9728-110">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="d9728-111">Azure CLI 2.0 で一般的なタスクを開始する際には、次のサンプルが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d9728-111">The following samples help you get started with common tasks in Azure CLI 2.0:</span></span>
- [<span data-ttu-id="d9728-112">Linux virtual machines</span><span class="sxs-lookup"><span data-stu-id="d9728-112">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- <span data-ttu-id="d9728-113">対話型操作: [Linux 仮想マシンを作成する](https://docs.microsoft.com/learn/azure-cli-2-0/index)</span><span class="sxs-lookup"><span data-stu-id="d9728-113">Interactive: [Create Linux Virtual Machines](https://docs.microsoft.com/learn/azure-cli-2-0/index)</span></span>
- [<span data-ttu-id="d9728-114">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="d9728-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="d9728-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="d9728-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="d9728-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="d9728-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="d9728-117">個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="d9728-117">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="d9728-118">Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="d9728-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>

> [!NOTE]
> <span data-ttu-id="d9728-119">以前のバージョンの CLI (Azure CLI 1.0) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9728-119">If you use the previous version of the CLI (Azure CLI 1.0), you can continue to use it.</span></span>
> <span data-ttu-id="d9728-120">ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI 2.0 に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d9728-120">However, we recommend updating to use the latest version of Azure CLI 2.0 for the best experience.</span></span>
> <span data-ttu-id="d9728-121">両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="d9728-121">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
