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
ms.openlocfilehash: ffa435f8c6ee5aa82d2efe2e09d7bcb1f1dc434b
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967692"
---
# <a name="azure-cli-20"></a><span data-ttu-id="a755d-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="a755d-103">Azure CLI 2.0</span></span>

<span data-ttu-id="a755d-104">Azure CLI 2.0 は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="a755d-104">The Azure CLI 2.0 is Microsoft's cross-platform command line experience for managing Azure resources.</span></span>
<span data-ttu-id="a755d-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="a755d-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="a755d-106">Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="a755d-106">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="a755d-107">Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a755d-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="a755d-108">[Cloud Shell](/azure/cloud-shell/overview) を使用して CLI をブラウザーで実行することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)することもできます。</span><span class="sxs-lookup"><span data-stu-id="a755d-108">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="a755d-109">CLI を実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="a755d-109">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="a755d-110">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a755d-110">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="a755d-111">Azure CLI 2.0 で一般的なタスクを開始する際には、次のサンプルが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a755d-111">The following samples help you get started with common tasks in Azure CLI 2.0:</span></span>

- [<span data-ttu-id="a755d-112">Linux virtual machines</span><span class="sxs-lookup"><span data-stu-id="a755d-112">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a755d-113">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="a755d-113">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a755d-114">Web Apps</span><span class="sxs-lookup"><span data-stu-id="a755d-114">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="a755d-115">SQL Database</span><span class="sxs-lookup"><span data-stu-id="a755d-115">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="a755d-116">個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="a755d-116">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="a755d-117">Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="a755d-117">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>

> [!NOTE]
> <span data-ttu-id="a755d-118">以前のバージョンの CLI (Azure CLI 1.0) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a755d-118">If you use the previous version of the CLI (Azure CLI 1.0), you can continue to use it.</span></span>
> <span data-ttu-id="a755d-119">ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI 2.0 に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a755d-119">However, we recommend updating to use the latest version of Azure CLI 2.0 for the best experience.</span></span>
> <span data-ttu-id="a755d-120">両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="a755d-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
