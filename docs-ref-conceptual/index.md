---
title: Azure CLI の概要
description: Azure コマンド ライン インターフェイス (CLI) の概要を説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 285567b00d8c303af3e78a01dc80946a08e4e8f8
ms.sourcegitcommit: 614811ea63ceb0e71bd99323846dc1b754e15255
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2018
ms.locfileid: "53805909"
---
# <a name="azure-command-line-interface-cli"></a><span data-ttu-id="e0749-103">Azure コマンド ライン インターフェイス (CLI)</span><span class="sxs-lookup"><span data-stu-id="e0749-103">Azure Command-Line Interface (CLI)</span></span>

<span data-ttu-id="e0749-104">Azure コマンド ライン インターフェイス (CLI) は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="e0749-104">The Azure command-line interface (CLI) is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="e0749-105">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0749-105">Use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="e0749-106">Azure CLI は簡単に使い始めることができ、Azure Resource Manager を操作対象とする自動化スクリプトを作成するにも最適です。</span><span class="sxs-lookup"><span data-stu-id="e0749-106">The Azure CLI is easy to get started with, and best used for building automation scripts that work with the Azure Resource Manager.</span></span>
<span data-ttu-id="e0749-107">Azure CLI を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e0749-107">Using the Azure CLI, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

> [!NOTE]
>
> <span data-ttu-id="e0749-108">スクリプトおよび Microsoft ドキュメント サイトでは、Azure CLI の例は `bash` シェル向けに記述されています。</span><span class="sxs-lookup"><span data-stu-id="e0749-108">In scripts and on the Microsoft documentation site, Azure CLI examples are written for the `bash` shell.</span></span> <span data-ttu-id="e0749-109">1 行の例であれば任意のプラットフォームで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0749-109">One-line examples will run on any platform.</span></span> <span data-ttu-id="e0749-110">行継続 (`\`) または変数の代入を含む、より長い例は、PowerShell などの他のシェルで動作するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0749-110">Longer examples which include line continutions (`\`) or variable assignment need to be modified to work on other shells, including PowerShell.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="e0749-111">実行またはインストール</span><span class="sxs-lookup"><span data-stu-id="e0749-111">Run or Install</span></span>

<span data-ttu-id="e0749-112">CLI はローカルにインストールできます。また、Azure Cloud Shell を使用してブラウザーで実行したり、Docker コンテナーで実行したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="e0749-112">You can install the CLI locally, run it in the browser with Azure Cloud Shell, or run in a Docker container.</span></span>

* <span data-ttu-id="e0749-113">Azure Cloud Shell を使用したブラウザーでの実行方法については、「[Azure Cloud Shell の Bash のクイック スタート](/azure/cloud-shell/quickstart)」または「[Azure Cloud Shell の PowerShell のクイック スタート](/azure/cloud-shell/quickstart-powershell)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e0749-113">To run in your browser with Azure Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart) or [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="e0749-114">CLI のインストール方法については、「[Azure CLI のインストール](install-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0749-114">To install the CLI, see [Install the Azure CLI](install-azure-cli.md).</span></span>
* <span data-ttu-id="e0749-115">Docker コンテナーとして実行する方法については、「[Docker コンテナーでの Azure CLI の実行](run-azure-cli-docker.md)」を参照してください</span><span class="sxs-lookup"><span data-stu-id="e0749-115">To run as a Docker container, see [Run Azure CLI in a Docker Container](run-azure-cli-docker.md)</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="e0749-116">Microsoft Learn でスキルを身に付ける</span><span class="sxs-lookup"><span data-stu-id="e0749-116">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="e0749-117">Azure CLI で仮想マシンを管理する</span><span class="sxs-lookup"><span data-stu-id="e0749-117">Manage virtual machines with the Azure CLI</span></span>](/learn/modules/manage-virtual-machines-with-azure-cli/)
- [<span data-ttu-id="e0749-118">CLI で Azure サービスを制御する</span><span class="sxs-lookup"><span data-stu-id="e0749-118">Control Azure services with the CLI</span></span>](/learn/modules/control-azure-services-with-cli/)
- [<span data-ttu-id="e0749-119">対話型学習の詳細...</span><span class="sxs-lookup"><span data-stu-id="e0749-119">More interactive learning...</span></span>](/learn/browse/?products=azure-clis)

## <a name="get-started"></a><span data-ttu-id="e0749-120">作業開始</span><span class="sxs-lookup"><span data-stu-id="e0749-120">Get started</span></span>

<span data-ttu-id="e0749-121">CLI の基本については、[概要](get-started-with-azure-cli.md)の記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="e0749-121">Read the [Get Started](get-started-with-azure-cli.md) article to learn the CLI basics.</span></span> <span data-ttu-id="e0749-122">次のサンプルでは、一般的なユース ケースが紹介されています。</span><span class="sxs-lookup"><span data-stu-id="e0749-122">The following samples demonstrate some common uses cases:</span></span>

- [<span data-ttu-id="e0749-123">Linux Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="e0749-123">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="e0749-124">Windows Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="e0749-124">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="e0749-125">Web Apps</span><span class="sxs-lookup"><span data-stu-id="e0749-125">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="e0749-126">SQL Database</span><span class="sxs-lookup"><span data-stu-id="e0749-126">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="e0749-127">個々の Azure CLI コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="e0749-127">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI command.</span></span>

> [!NOTE]
> <span data-ttu-id="e0749-128">以前のバージョンの CLI (Azure クラシック CLI) を使用している場合は、引き続きそれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0749-128">If you use the previous version of the CLI (Azure classic CLI), you can continue to use it.</span></span>
> <span data-ttu-id="e0749-129">ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI に更新することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0749-129">However, we recommend updating to use the latest version of the Azure CLI for the best experience.</span></span>
> <span data-ttu-id="e0749-130">両方の CLI を使用する場合は、`azure` がクラシック CLI で、`az` が最新の CLI であることを覚えておいてください。</span><span class="sxs-lookup"><span data-stu-id="e0749-130">If you use both CLIs, remember that `azure` is the classic CLI and that `az` is the most recent CLI.</span></span>
