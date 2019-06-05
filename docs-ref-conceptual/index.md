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
ms.openlocfilehash: 0c91b8d49c7854f3963985aa64bbd3c052660f9c
ms.sourcegitcommit: f1031052dd021ebcc253e4b3a5e6b919d862fab2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "64564285"
---
# <a name="azure-command-line-interface-cli"></a><span data-ttu-id="ea358-103">Azure コマンド ライン インターフェイス (CLI)</span><span class="sxs-lookup"><span data-stu-id="ea358-103">Azure Command-Line Interface (CLI)</span></span>

<span data-ttu-id="ea358-104">Azure コマンド ライン インターフェイス (CLI) は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="ea358-104">The Azure command-line interface (CLI) is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span> <span data-ttu-id="ea358-105">Azure CLI は覚えやすい、Azure リソースを操作するカスタム オートメーションのビルドに最適なツールです。</span><span class="sxs-lookup"><span data-stu-id="ea358-105">The Azure CLI is easy to learn and the perfect tool for building custom automation that works with Azure resources.</span></span>

| <span data-ttu-id="ea358-106"><center>![Windows ロゴ](./media/Windows_logo_-_2012.png)</span><span class="sxs-lookup"><span data-stu-id="ea358-106"><center>![Windows logo](./media/Windows_logo_-_2012.png)</span></span><br/><span data-ttu-id="ea358-107">Windows 10</center></span><span class="sxs-lookup"><span data-stu-id="ea358-107">Windows 10</center></span></span> | <span data-ttu-id="ea358-108"><center>![Ubuntu ロゴ](./media/cof_orange_hex.png)</span><span class="sxs-lookup"><span data-stu-id="ea358-108"><center>![Ubuntu logo](./media/cof_orange_hex.png)</span></span><br/><span data-ttu-id="ea358-109">Ubuntu 16.04+</center></span><span class="sxs-lookup"><span data-stu-id="ea358-109">Ubuntu 16.04+</center></span></span> | <span data-ttu-id="ea358-110"><center>![macOS ロゴ](./media/Apple_logo_black.png)</span><span class="sxs-lookup"><span data-stu-id="ea358-110"><center>![macOS logo](./media/Apple_logo_black.png)</span></span><br/><span data-ttu-id="ea358-111">macOS</center></span><span class="sxs-lookup"><span data-stu-id="ea358-111">macOS</center></span></span> | <span data-ttu-id="ea358-112"><center>![Azure Cloud Shell ロゴ](./media/cloud-check.png)</span><span class="sxs-lookup"><span data-stu-id="ea358-112"><center>![Azure Cloud Shell logo](./media/cloud-check.png)</span></span><br/><span data-ttu-id="ea358-113">Azure Cloud Shell</center></span><span class="sxs-lookup"><span data-stu-id="ea358-113">Azure Cloud Shell</center></span></span> |
|---|---|---|---|
| [<span data-ttu-id="ea358-114">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="ea358-114">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows) | [<span data-ttu-id="ea358-115">Ubuntu のインストール手順</span><span class="sxs-lookup"><span data-stu-id="ea358-115">Ubuntu install instructions</span></span>](./install-azure-cli-apt.md) | [<span data-ttu-id="ea358-116">macOS のインストール手順</span><span class="sxs-lookup"><span data-stu-id="ea358-116">macOS install instructions</span></span>](./install-azure-cli-macos.md) | [<span data-ttu-id="ea358-117">Azure Cloud Shell 上のブラウザーでの実行</span><span class="sxs-lookup"><span data-stu-id="ea358-117">Run in your browser on Azure Cloud Shell</span></span>](https://shell.azure.com) |

[<span data-ttu-id="ea358-118">サポートされているすべてのインストール プラットフォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea358-118">See all of the supported installation platforms.</span></span>](./install-azure-cli.md)

## <a name="azure-cli-resources"></a><span data-ttu-id="ea358-119">Azure CLI リソース</span><span class="sxs-lookup"><span data-stu-id="ea358-119">Azure CLI Resources</span></span>

> [!NOTE]
>
> <span data-ttu-id="ea358-120">スクリプトおよび Microsoft ドキュメント サイトでは、Azure CLI の例は `bash` シェル向けに記述されています。</span><span class="sxs-lookup"><span data-stu-id="ea358-120">In scripts and on the Microsoft documentation site, Azure CLI examples are written for the `bash` shell.</span></span> <span data-ttu-id="ea358-121">1 行の例であれば任意のプラットフォームで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ea358-121">One-line examples will run on any platform.</span></span> <span data-ttu-id="ea358-122">行継続 (`\`) または変数の代入を含む、より長い例は、PowerShell などの他のシェルで動作するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea358-122">Longer examples which include line continuations (`\`) or variable assignment need to be modified to work on other shells, including PowerShell.</span></span>

| <span data-ttu-id="ea358-123">作業開始</span><span class="sxs-lookup"><span data-stu-id="ea358-123">Get started</span></span> | <span data-ttu-id="ea358-124">Microsoft Learn でスキルを身に付ける</span><span class="sxs-lookup"><span data-stu-id="ea358-124">Build your skills with Microsoft Learn</span></span> | <span data-ttu-id="ea358-125">お問い合わせ</span><span class="sxs-lookup"><span data-stu-id="ea358-125">Contact Us</span></span> |
|-------------|----------------------------------------|------------|
| [<span data-ttu-id="ea358-126">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="ea358-126">Get Started with the Azure CLI</span></span>](get-started-with-azure-cli.md) | [<span data-ttu-id="ea358-127">Azure CLI で仮想マシンを管理する</span><span class="sxs-lookup"><span data-stu-id="ea358-127">Manage virtual machines with the Azure CLI</span></span>](/learn/modules/manage-virtual-machines-with-azure-cli/) | [<span data-ttu-id="ea358-128">機能の要求</span><span class="sxs-lookup"><span data-stu-id="ea358-128">Request features</span></span>](https://github.com/Azure/azure-cli/issues/new?template=Feature_request.md) |
| [<span data-ttu-id="ea358-129">Web アプリケーションを GitHub からデプロイする</span><span class="sxs-lookup"><span data-stu-id="ea358-129">Deploy a web application from GitHub</span></span>](/azure/app-service/scripts/cli-deploy-github?toc=%2fcli%2fazure%2ftoc.json) | [<span data-ttu-id="ea358-130">CLI で Azure サービスを制御する</span><span class="sxs-lookup"><span data-stu-id="ea358-130">Control Azure services with the CLI</span></span>](/learn/modules/control-azure-services-with-cli/) | [<span data-ttu-id="ea358-131">StackOverflow で質問する</span><span class="sxs-lookup"><span data-stu-id="ea358-131">Get help on StackOverflow</span></span>](https://stackoverflow.com/questions/tagged/azure-cli) |
| [<span data-ttu-id="ea358-132">Postgres データベースを作成する</span><span class="sxs-lookup"><span data-stu-id="ea358-132">Create a Postgres database</span></span>](/azure/postgresql/quickstart-create-server-up-azure-cli?toc=%2fcli%2fazure%2ftoc.json) |  [<span data-ttu-id="ea358-133">アプリケーションを Azure Storage に接続する</span><span class="sxs-lookup"><span data-stu-id="ea358-133">Connect an application to Azure Storage</span></span>](/learn/modules/connect-an-app-to-azure-storage/) | [<span data-ttu-id="ea358-134">レポートに関する問題</span><span class="sxs-lookup"><span data-stu-id="ea358-134">Report issues</span></span>](https://github.com/Azure/azure-cli/issues/new?template=Bug_report.md) |
| [<span data-ttu-id="ea358-135">Kubernetes クラスターの作成</span><span class="sxs-lookup"><span data-stu-id="ea358-135">Create a Kubernetes cluster</span></span>](/azure/aks/kubernetes-walkthrough?toc=%2fcli%2fazure%2ftoc.json) | [<span data-ttu-id="ea358-136">対話型学習の詳細...</span><span class="sxs-lookup"><span data-stu-id="ea358-136">More interactive learning...</span></span>](/learn/browse/?products=azure-clis) | |
| [<span data-ttu-id="ea358-137">仮想マシンの作成</span><span class="sxs-lookup"><span data-stu-id="ea358-137">Create a virtual machine</span></span>](/cli/azure/azure-cli-vm-tutorial) | | |
