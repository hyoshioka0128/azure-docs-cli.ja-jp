---
title: "Azure CLI 2.0 を使ってみる"
description: "Linux、Mac、または Windows 上で、Azure CLI 2.0 の使用を開始します。"
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
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 5d6d7abb34fa2be571a9a49f0f84380538592807
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2017
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="965e3-104">Azure CLI 2.0 を使ってみる</span><span class="sxs-lookup"><span data-stu-id="965e3-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="965e3-105">Azure CLI 2.0 は、Azure リソースを管理するための、Azure の新しいコマンド ライン エクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="965e3-105">The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.</span></span>
<span data-ttu-id="965e3-106">ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用できるほか、macOS、Linux、Windows に[インストール](install-azure-cli.md)してコマンド ラインで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="965e3-107">Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="965e3-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span>
<span data-ttu-id="965e3-108">この記事では、その基本的な使い方と核となる概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="965e3-108">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

<span data-ttu-id="965e3-109">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="965e3-109">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

## <a name="connect"></a><span data-ttu-id="965e3-110">接続</span><span class="sxs-lookup"><span data-stu-id="965e3-110">Connect</span></span>

<span data-ttu-id="965e3-111">最も簡単に始められるのは、[Cloud Shell を起動](/azure/cloud-shell/quickstart)する方法です。</span><span class="sxs-lookup"><span data-stu-id="965e3-111">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="965e3-112">Cloud Shell は、Azure Portal の上部のナビゲーションから起動します。</span><span class="sxs-lookup"><span data-stu-id="965e3-112">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell アイコン](media/get-started-with-azure-cli/shell-icon.png)

2. <span data-ttu-id="965e3-114">使用するサブスクリプションを選択し、ストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="965e3-114">Choose the subscription you want to use and create a storage account.</span></span>

   ![ストレージ アカウントの作成](media/get-started-with-azure-cli/storage-prompt.png)

<span data-ttu-id="965e3-116">CLI を[インストール](install-azure-cli.md)し、コマンド ラインからローカルで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-116">You can also [install](install-azure-cli.md) the CLI and run it locally from the command line.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="965e3-117">リソース グループの作成</span><span class="sxs-lookup"><span data-stu-id="965e3-117">Create a Resource Group</span></span>

<span data-ttu-id="965e3-118">必要な設定がすべて整ったら、Azure CLI を使って Azure にリソースを作成してみましょう。</span><span class="sxs-lookup"><span data-stu-id="965e3-118">Now that we've got everything set up, let's use the Azure CLI to create resources within Azure.</span></span>

<span data-ttu-id="965e3-119">まずリソース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="965e3-119">First, create a Resource Group.</span></span>  <span data-ttu-id="965e3-120">Azure ではリソース グループを使うことで、複数のリソースを論理上のグループとして管理することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-120">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group.</span></span>  <span data-ttu-id="965e3-121">たとえばアプリケーションまたはプロジェクトのリソース グループを作成し、仮想マシンやデータベース、CDN サービスをそこに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-121">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="965e3-122">"MyResourceGroup" という名前のリソース グループを Azure の *westus2* リージョンに作成しましょう。</span><span class="sxs-lookup"><span data-stu-id="965e3-122">Let's create a resource group named "MyResourceGroup" in the *westus2* region of Azure.</span></span>  <span data-ttu-id="965e3-123">そのためには、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="965e3-123">To do so type the following command:</span></span>

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

<span data-ttu-id="965e3-124">リソース グループが作成されると、`az group create` コマンドによって、新しく作成されたリソースのいくつかのプロパティが出力されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-124">Once the resource group has been created, the `az group create` command outputs several properties of the newly created resource:</span></span>

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="965e3-125">Linux 仮想マシンの作成</span><span class="sxs-lookup"><span data-stu-id="965e3-125">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="965e3-126">リソース グループが完成したら、そこに Linux VM を作成します。</span><span class="sxs-lookup"><span data-stu-id="965e3-126">Now that we have our resource group, let's create a Linux VM within it.</span></span>

<span data-ttu-id="965e3-127">次のコマンドで、一般的な UbuntuLTS イメージを使用して、10 GB と 20 GB の 2 つのストレージ ディスクがアタッチされた Linux VM を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-127">You can create a Linux VM using the popular UbuntuLTS image, with two attached storage disks of 10 GB and 20 GB, with the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

<span data-ttu-id="965e3-128">上のコマンドを実行すると、Azure CLI 2.0 は、~/.ssh ディレクトリに格納されている SSH キー ペアを探します。</span><span class="sxs-lookup"><span data-stu-id="965e3-128">When you run the preceding command, the Azure CLI 2.0 looks for an SSH key pair stored under your ~/.ssh directory.</span></span>  <span data-ttu-id="965e3-129">SSH キー ペアがまだそこに格納されていない場合は、次のように --generate-ssh-keys パラメーターを渡して、Azure CLI に自動的に作成させることができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-129">If you don't already have an SSH key pair stored there, you can ask the Azure CLI to automatically create one for you by passing the --generate-ssh-keys parameter:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

<span data-ttu-id="965e3-130">VM の作成が完了し、アクセスして使用できるようになると、`az vm create` コマンドから出力が返されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-130">The `az vm create` command returns output once the VM has been fully created and is ready to be accessed and used.</span></span> <span data-ttu-id="965e3-131">出力には、パブリック IP アドレスなど、新しく作成した VM のいくつかのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="965e3-131">The output includes several properties of the newly created VM including its public IP address:</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="965e3-132">VM が作成されたら、その VM のパブリック IP アドレスを **SSH** で使用し、新しい Linux VM にログオンすることができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-132">Now that the VM has been created, you can log on to your new Linux VM using **SSH** with the public IP address of the VM you created:</span></span>

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a><span data-ttu-id="965e3-133">Windows Server 仮想マシンの作成</span><span class="sxs-lookup"><span data-stu-id="965e3-133">Create a Windows Server Virtual Machine</span></span>

<span data-ttu-id="965e3-134">`az vm create` コマンドを使用して、Windows Server 2016 Datacenter ベースの VM を作成し、Linux VM 用に使用したのと同じ "MyResourceGroup" リソース グループに追加しましょう。</span><span class="sxs-lookup"><span data-stu-id="965e3-134">Let's now create a Windows Server 2016 Datacenter-based VM using the `az vm create` command and add it to the same "MyResourceGroup" resource group that we used for our Linux VM.</span></span>  <span data-ttu-id="965e3-135">Linux VM の例のように、`--data-disk-sizes-gb` パラメーターを使用して 2 つのストレージ ディスクも接続します。</span><span class="sxs-lookup"><span data-stu-id="965e3-135">Like the Linux VM example, we'll also attach two storage disks using the `--data-disk-sizes-gb` parameter.</span></span>

<span data-ttu-id="965e3-136">Azure では、簡単に推測できるユーザー名とパスワードを使用しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="965e3-136">Azure requires that you avoid using easily guessed usernames/passwords.</span></span> <span data-ttu-id="965e3-137">使用できる文字のほか、ユーザー名とパスワードの最小の長さについて特定の規則があります。</span><span class="sxs-lookup"><span data-stu-id="965e3-137">There are specific rules for what characters can be used as well as the minimum length of both username and password.</span></span>  

> [!NOTE]
> <span data-ttu-id="965e3-138">このコマンドを実行すると、ユーザー名とパスワードの入力を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-138">You will be prompted to enter your username and password when running this command.</span></span>

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

<span data-ttu-id="965e3-139">VM の作成が完了し、アクセスして使用できるようになると、`az vm create` コマンドから結果が出力されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-139">The `az vm create` command output results once the VM has been fully created and is ready to be accessed and used.</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="965e3-140">リモート デスクトップと VM のパブリック IP アドレス (`az vm create` の出力で返されるアドレス) を使用して、新しく作成した Windows Server VM にログオンします。</span><span class="sxs-lookup"><span data-stu-id="965e3-140">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM (which is returned in the output from `az vm create`).</span></span>  
<span data-ttu-id="965e3-141">Windows ベースのシステムでは、`mstsc` コマンドを使ってコマンド ラインから同じ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="965e3-141">If you are on a Windows-based system, you can do this from the command line using the `mstsc` command:</span></span>

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="965e3-142">VM を作成したときと同じユーザー名/パスワードの組み合わせを指定してログインしてください。</span><span class="sxs-lookup"><span data-stu-id="965e3-142">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="965e3-143">その他の Azure リソースの作成</span><span class="sxs-lookup"><span data-stu-id="965e3-143">Creating other resources in Azure</span></span>

<span data-ttu-id="965e3-144">ここまでは、リソース グループ、Linux VM、Windows Server VM の作成方法を見てきました。</span><span class="sxs-lookup"><span data-stu-id="965e3-144">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="965e3-145">その他にも、さまざまな種類の Azure リソースを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-145">You can create many other types of Azure resources as well.</span></span>  

<span data-ttu-id="965e3-146">すべての新しいリソースは、一貫した `az <resource type name> create` 名前付けパターンを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-146">All new resources are created using a consistent `az <resource type name> create` naming pattern.</span></span>  <span data-ttu-id="965e3-147">たとえば、新しく作成した VM に関連付けるための Azure Network Load Balancer を作成するには、次の create コマンドを使います。</span><span class="sxs-lookup"><span data-stu-id="965e3-147">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

<span data-ttu-id="965e3-148">また、次の create コマンドを使って、インフラストラクチャ用に新しいプライベート仮想ネットワーク (Azure では通常 "VNet" と呼ばれます) を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-148">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following create command:</span></span>

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

<span data-ttu-id="965e3-149">Azure と Azure CLI の優れている点は、それらを使ってクラウドベースのインフラストラクチャを実現できるだけでなく、管理の行き届いたプラットフォーム サービスを作成できることです。</span><span class="sxs-lookup"><span data-stu-id="965e3-149">What makes Azure and the Azure CLI powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span>  <span data-ttu-id="965e3-150">その管理されたプラットフォーム サービスにインフラストラクチャを組み合わせることで、さらに強力なソリューションを構築することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-150">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="965e3-151">たとえば Azure CLI を使って Azure AppService を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-151">For example, you can use the Azure CLI to create an Azure AppService.</span></span>  <span data-ttu-id="965e3-152">Azure AppService は、管理されたプラットフォーム サービスであり、インフラストラクチャには一切気を遣わずに Web アプリをホストできるのが特徴です。</span><span class="sxs-lookup"><span data-stu-id="965e3-152">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span>  <span data-ttu-id="965e3-153">Azure AppService の作成後、次の create コマンドを使用して、AppService 内に 2 つの新しい Azure Web アプリを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-153">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following create commands:</span></span>

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

<span data-ttu-id="965e3-154">`az <resource type name> create` パターンの基本を理解すると、何でも簡単に作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="965e3-154">Once you understand the basics of the `az <resource type name> create` pattern, it becomes easy to create anything.</span></span> <span data-ttu-id="965e3-155">以下に、いくつかの一般的な Azure リソースの種類と、それを作成するための Azure CLI create コマンドを示します。</span><span class="sxs-lookup"><span data-stu-id="965e3-155">Following are some popular Azure resource types and the corresponding Azure CLI create commands to create them:</span></span>

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

<span data-ttu-id="965e3-156">上記の各コマンドに渡すことができるリソース固有の追加パラメーターと、作成できるリソースの種類の詳細については、[リファレンス ドキュメント](/cli/azure)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="965e3-156">Visit the [Reference documentation](/cli/azure) to learn more about the additional resource-specific parameters that you can pass to each of the preceding commands and the resource types you can create.</span></span> 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a><span data-ttu-id="965e3-157">便利なヒント: --no-wait を使用して作成操作を最適化する</span><span class="sxs-lookup"><span data-stu-id="965e3-157">Useful tip: Optimizing create operations using --no-wait</span></span>

<span data-ttu-id="965e3-158">既定では、Azure CLI 2.0 を使用してリソースを作成するときに、`az <resource type name> create` コマンドは、リソースが作成されて使用できるようになるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="965e3-158">By default when you create resources using the Azure CLI 2.0, the `az <resource type name> create` command waits until the resource has been created and is ready for you to use.</span></span>  <span data-ttu-id="965e3-159">たとえば、VM を作成する場合、`az vm create` コマンドは、既定では VM が作成されて SSH または RDP でアクセスできるようになるまで戻ってきません。</span><span class="sxs-lookup"><span data-stu-id="965e3-159">For example, if you create a VM, the `az vm create` command will, by default, not return until the VM is created and is ready for you to SSH or RDP into it.</span></span>

<span data-ttu-id="965e3-160">この方法を使用するのは、依存関係のある複数のステップを含む (続行する前に前のタスクを正常に完了しておく必要がある) 自動化スクリプトを簡単に記述できるためです。</span><span class="sxs-lookup"><span data-stu-id="965e3-160">We use this approach because it makes it easier to write automation scripts that contain multiple steps with dependencies (and need a prior task to have completed successfully before continuing).</span></span>

<span data-ttu-id="965e3-161">続行する前にリソースの作成を待つ必要がない場合は、`no-wait` オプションを使用して、バックグラウンドで作成アクションを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-161">If you do not need to wait on creation of a resource before continuing, you can use the `no-wait` option to start a create action in the background.</span></span> <span data-ttu-id="965e3-162">他のコマンドには引き続き CLI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="965e3-162">You can continue using the CLI for other commands.</span></span>

<span data-ttu-id="965e3-163">たとえば、次のように `az vm create` を使用すると、VM のデプロイが開始され、より短い時間で (VM が完全に起動される前に) 制御が戻ります。</span><span class="sxs-lookup"><span data-stu-id="965e3-163">For example, the following usage of the `az vm create` starts a VM deployment and then return much more quickly (and before the VM has fully booted):</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

<span data-ttu-id="965e3-164">`--no-wait` を使用すると、自動化スクリプトのパフォーマンスを大幅に最適化することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-164">Using the `--no-wait` approach can help you optimize the performance of your automation scripts considerably.</span></span>

## <a name="listing-resources-and-formatting-output"></a><span data-ttu-id="965e3-165">リソースの一覧表示と出力の書式設定</span><span class="sxs-lookup"><span data-stu-id="965e3-165">Listing resources and formatting output</span></span>

<span data-ttu-id="965e3-166">Azure CLI 内で `list` コマンドを使用すると、Azure で実行されているリソースを検出し、一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-166">You can use the `list` command within the Azure CLI to find and list the resources running in Azure.</span></span> 

<span data-ttu-id="965e3-167">create コマンドの場合と同様に、Azure CLI 2.0 では、すべてのリソースの種類で一環した共通の `az <resource type name> list` 名前付けパターンを使用してリソースを一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-167">Like with the create command, you can list resources using the Azure CLI 2.0 using a common `az <resource type name> list` naming pattern that is consistent across all resource types.</span></span>  <span data-ttu-id="965e3-168">リソースの一覧を望ましい形式で表示するためのフィルター処理や並べ替えに使用できる、さまざまな出力形式とクエリ オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="965e3-168">There are various output formats and query options available to filter and sort the list of resources in the way you prefer to see them.</span></span>

<span data-ttu-id="965e3-169">たとえば、`az vm list` は、保持しているすべての VM の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="965e3-169">For example, `az vm list` shows the list of all VMs you have.</span></span>   

```azurecli-interactive
az vm list 
```
<span data-ttu-id="965e3-170">返される値は、既定で JSON 形式になります (簡潔にするために、出力の一部のみを示しています)。</span><span class="sxs-lookup"><span data-stu-id="965e3-170">The values returned are by default in JSON (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...   
]
```

<span data-ttu-id="965e3-171">必要に応じて、`--output` オプションを使用して、出力形式を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-171">You can optionally modify the output format using the `--output` option.</span></span>  <span data-ttu-id="965e3-172">`az vm list` コマンドを実行すると、前に作成した Linux と Windows Server の両方の VM と共に、VM の最も一般的なプロパティが表示されます。その際、読みやすい *table* 形式オプションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-172">Run the `az vm list` command to see both the Linux and Windows Server VMs created earlier, along with the most common properties of a VM, using the easy to read *table* format option:</span></span>

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="965e3-173">ヘッダーのないテキストベースのタブ区切り形式にするには、*tsv* 出力オプションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-173">The *tsv* output option can be used to get a text-based, tab-separated format without any headers.</span></span>  <span data-ttu-id="965e3-174">この形式は、grep などの他のテキストベースのツールに出力をパイプ処理する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="965e3-174">This format is useful when you want to pipe the output into another text-based tool like grep.</span></span> 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
<span data-ttu-id="965e3-175">リソースの一覧表示と出力の書式設定のその他の方法の詳細については、[出力形式](format-output-azure-cli.md)に関する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="965e3-175">Visit the [output formats](format-output-azure-cli.md) article to learn more about the additional ways to list resources and format the output.</span></span>

## <a name="querying-resources-and-shaping-outputs"></a><span data-ttu-id="965e3-176">リソースへのクエリ実行と出力の整形</span><span class="sxs-lookup"><span data-stu-id="965e3-176">Querying resources and shaping outputs</span></span>

<span data-ttu-id="965e3-177">多くの場合、特定の条件に合致するリソースのみに対してクエリを実行できるようにすることが望まれます。</span><span class="sxs-lookup"><span data-stu-id="965e3-177">Often you want to be able to query for only those resources that meet a specific condition.</span></span>  

<span data-ttu-id="965e3-178">`list` コマンドの組み込みのサポートにより、リソース グループ名でリソースを簡単にフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="965e3-178">The `list` command has built-in support that makes it easy to filter resources by Resource Group name.</span></span>  <span data-ttu-id="965e3-179">たとえば、`--ResourceGroup` または `-g` パラメーターを `list` コマンドに渡し、特定のリソース グループ内のリソースだけを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-179">For example, you can pass either a `--ResourceGroup` or `-g` parameter to a `list` command to only retrieve those resources within a specific resource group:</span></span>


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="965e3-180">クエリをさらに強力にサポートするために、`--query` パラメーターを使用して、"*任意*" の `az` コマンドの結果に対して JMESPath クエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-180">For even more powerful querying support, you can use the `--query` parameter to execute a JMESPath query on the results of *any* `az` command.</span></span>  <span data-ttu-id="965e3-181">JMESPath クエリは、返される任意の結果の出力のフィルター処理にも整形にも使用することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-181">JMESPath queries can be used both to filter as well as shape the output of any returned result.</span></span>

<span data-ttu-id="965e3-182">たとえば、次のコマンドを実行すると、"My" という文字列を含む任意のリソース グループ内の任意の VM リソースに対するクエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-182">For example, execute the following command to query for any VM resource within any resource group that contains the letters "My":</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="965e3-183">その後、別の値を出力できる JMESPath クエリの整形機能を使用して、さらに出力を絞り込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-183">We could then choose to further refine the output by using the shaping capability of JMESPath queries to output different values as well.</span></span>  <span data-ttu-id="965e3-184">たとえば、次のコマンドは、OS が Linux ベースか Windows ベースかを判断するために、VM で使用されている OS ディスクの種類を取得します。</span><span class="sxs-lookup"><span data-stu-id="965e3-184">For example, the following command retrieves the type of OS disk the VM is using to determine whether the OS is Linux or Windows based:</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

<span data-ttu-id="965e3-185">Azure CLI での JMESPath サポートは強力です。</span><span class="sxs-lookup"><span data-stu-id="965e3-185">The JMESPath support in Azure CLI is powerful.</span></span>  <span data-ttu-id="965e3-186">使用方法の詳細については、[クエリ](query-azure-cli.md)に関する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="965e3-186">Learn more about how to use it in our [query](query-azure-cli.md) article.</span></span>

## <a name="deleting-resources"></a><span data-ttu-id="965e3-187">リソースの削除</span><span class="sxs-lookup"><span data-stu-id="965e3-187">Deleting resources</span></span>

<span data-ttu-id="965e3-188">Azure CLI で `delete` コマンドを使用すると、不要になったリソースを削除できます。</span><span class="sxs-lookup"><span data-stu-id="965e3-188">You can use the `delete` command within Azure CLI to delete the resources you no longer need.</span></span> <span data-ttu-id="965e3-189">`create` コマンドの場合と同様に、任意のリソースに対して `delete` コマンドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-189">You can use the `delete` command with any resource just like you can with the `create` command.</span></span>

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

<span data-ttu-id="965e3-190">既定では、削除の確認を求めるメッセージが CLI によって表示されます。</span><span class="sxs-lookup"><span data-stu-id="965e3-190">By default the CLI prompts to confirm deletion.</span></span>  <span data-ttu-id="965e3-191">自動化スクリプトでは、このメッセージの表示を抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="965e3-191">You can suppress this prompt for automated scripts.</span></span>

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

<span data-ttu-id="965e3-192">`delete` コマンドを使用して、多数のリソースを一度に削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="965e3-192">You can also use the `delete` command to delete many resources at a time.</span></span> <span data-ttu-id="965e3-193">たとえば、次のコマンドは、この概要チュートリアルのすべてのサンプルで使用してきた "MyResourceGroup" リソース グループ内のすべてのリソースを削除します。</span><span class="sxs-lookup"><span data-stu-id="965e3-193">For example, the following command deletes all the resources in the "MyResourceGroup" resource group that we've used for all the samples in this Get Started tutorial.</span></span>

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a><span data-ttu-id="965e3-194">サンプルの入手</span><span class="sxs-lookup"><span data-stu-id="965e3-194">Get samples</span></span>

<span data-ttu-id="965e3-195">Azure CLI の使用方法の詳細については、[Linux VM](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Web アプリ](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) 用の最も一般的なスクリプトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="965e3-195">To learn more about ways to use the Azure CLI, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Web apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), and [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).</span></span>

## <a name="read-the-api-reference-docs"></a><span data-ttu-id="965e3-196">API リファレンス ドキュメントの確認</span><span class="sxs-lookup"><span data-stu-id="965e3-196">Read the API reference docs</span></span>

[<span data-ttu-id="965e3-197">API リファレンス</span><span class="sxs-lookup"><span data-stu-id="965e3-197">API reference</span></span>](/cli/azure)

## <a name="get-help"></a><span data-ttu-id="965e3-198">問い合わせ</span><span class="sxs-lookup"><span data-stu-id="965e3-198">Get help</span></span>

<span data-ttu-id="965e3-199">Azure CLI には、組み込みのヘルプ ドキュメントがあります。これは、コマンド ラインから実行できる Web ドキュメントと同じものです。</span><span class="sxs-lookup"><span data-stu-id="965e3-199">The Azure CLI has built-in help documentation, which matches our web documentation that you can run from the command line:</span></span>

```azurecli-interactive
az [command-group [command]] -h
```

<span data-ttu-id="965e3-200">たとえば、VM に使用できるコマンドやサブグループを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="965e3-200">For example, to see what commands and subgroups are available for VMs, use:</span></span>

```azurecli-interactive
az vm -h
```

<span data-ttu-id="965e3-201">VM を作成するためのコマンドのヘルプを表示するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="965e3-201">To get help with the command to create a VM, use:</span></span>

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a><span data-ttu-id="965e3-202">Azure CLI 1.0 からの切り替え</span><span class="sxs-lookup"><span data-stu-id="965e3-202">Switch from Azure CLI 1.0</span></span>

<span data-ttu-id="965e3-203">Azure CLI 1.0 (azure.js) の使用方法を既に知っている場合は、コマンドがまったく同じではない部分に気が付くでしょう。</span><span class="sxs-lookup"><span data-stu-id="965e3-203">If you already know how to use Azure CLI 1.0 (azure.js), you'll notice places where the commands aren't quite the same.</span></span>
<span data-ttu-id="965e3-204">同じタスクを実行するコマンドが大きく異なる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="965e3-204">Sometimes the commands to perform a task are significantly different.</span></span>
<span data-ttu-id="965e3-205">Azure CLI 1.0 から Azure CLI 2.0 への切り替えをサポートするために、こちらの[コマンド対応表](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst)が用意されています。</span><span class="sxs-lookup"><span data-stu-id="965e3-205">To help you make the switch from Azure CLI 1.0 to Azure CLI 2.0, we've started this [command mapping](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).</span></span>

## <a name="send-us-your-feedback"></a><span data-ttu-id="965e3-206">フィードバックを送信します</span><span class="sxs-lookup"><span data-stu-id="965e3-206">Send us your feedback</span></span>

```azurecli-interactive
az feedback
```
