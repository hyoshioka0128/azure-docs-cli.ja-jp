---
title: Azure CLI 2.0
description: "Azure CLI 2.0 の概要。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 2f4f9950dd663ae85f41bf4efe114b15770ace5d
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: ja-JP
---
# <a name="azure-cli-20"></a><span data-ttu-id="ffd00-104">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="ffd00-104">Azure CLI 2.0</span></span>

<span data-ttu-id="ffd00-105">Azure CLI 2.0 は、Azure リソースを管理するための、Azure の新しいコマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="ffd00-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>  <span data-ttu-id="ffd00-106">macOS、Linux、および Windows で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffd00-106">It can be used on macOS, Linux, and Windows.</span></span> 

<span data-ttu-id="ffd00-107">Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="ffd00-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="ffd00-108">Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="ffd00-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="ffd00-109">ご利用のシステムで Azure CLI 2.0 を使用するための準備については、[インストール](install-azure-cli.md)に関する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd00-109">Review the [Install article](install-azure-cli.md) to get Azure CLI 2.0 up and running on your system.</span></span> <span data-ttu-id="ffd00-110">さらに実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="ffd00-110">Then read the [Get Started](get-started-with-azure-cli.md) article to begin using it.</span></span>
<span data-ttu-id="ffd00-111">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd00-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="ffd00-112">Azure CLI 2.0 の基本的な使い方については、次のサンプルが参考になります。</span><span class="sxs-lookup"><span data-stu-id="ffd00-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="ffd00-113">Linux 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="ffd00-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ffd00-114">Windows 仮想マシン</span><span class="sxs-lookup"><span data-stu-id="ffd00-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ffd00-115">Web Apps</span><span class="sxs-lookup"><span data-stu-id="ffd00-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ffd00-116">SQL Database</span><span class="sxs-lookup"><span data-stu-id="ffd00-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="ffd00-117">個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="ffd00-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="ffd00-118">Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="ffd00-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="ffd00-119">以前のバージョンの CLI (Azure CLI) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffd00-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="ffd00-120">両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="ffd00-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 