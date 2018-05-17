---
title: Azure CLI 2.0
description: Azure CLI 2.0 の概要。
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: ee82c06e5b5b614b5557c6e6426d2da488468318
ms.sourcegitcommit: 15d6dfaee2075d0abceb2aa2423f0b6ef7b2ac9b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2018
---
# <a name="azure-cli-20"></a><span data-ttu-id="5dfce-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="5dfce-103">Azure CLI 2.0</span></span>

<span data-ttu-id="5dfce-104">Azure CLI 2.0 は、Azure リソースを管理するための、Azure の新しいコマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="5dfce-104">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="5dfce-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用できるほか、macOS、Linux、Windows に[インストール](install-azure-cli.md)してコマンド ラインで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="5dfce-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="5dfce-106">Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="5dfce-106">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="5dfce-107">Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5dfce-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="5dfce-108">[Cloud Shell](/azure/cloud-shell/overview) を使用して CLI をブラウザーで実行することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)することもできます。</span><span class="sxs-lookup"><span data-stu-id="5dfce-108">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="5dfce-109">CLI を実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="5dfce-109">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="5dfce-110">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5dfce-110">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="5dfce-111">Azure CLI 2.0 の基本的な使い方については、次のサンプルが参考になります。</span><span class="sxs-lookup"><span data-stu-id="5dfce-111">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="5dfce-112">Linux 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="5dfce-112">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- <span data-ttu-id="5dfce-113">対話型操作: [Linux 仮想マシンを作成する](https://docs.microsoft.com/learn/azure-cli-2-0/index)</span><span class="sxs-lookup"><span data-stu-id="5dfce-113">Interactive: [Create Linux Virtual Machines](https://docs.microsoft.com/learn/azure-cli-2-0/index)</span></span>
- [<span data-ttu-id="5dfce-114">Windows 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="5dfce-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="5dfce-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="5dfce-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="5dfce-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="5dfce-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="5dfce-117">個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="5dfce-117">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="5dfce-118">Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="5dfce-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="5dfce-119">以前のバージョンの CLI (Azure CLI) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5dfce-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="5dfce-120">両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="5dfce-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
