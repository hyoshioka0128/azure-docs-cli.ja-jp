---
title: "Azure CLI 2.0 でのクエリ コマンドの結果"
description: "--query を使用して、Azure CLI 2.0 コマンドの出力に対して JMESPath クエリを実行します。"
keywords: "Azure CLI 2.0, JMESPath, クエリ, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 5979acc5-21a5-41e2-a4b6-3183bfe6aa22
ms.openlocfilehash: 8ab4a5e38f06199c5f044b8526c581828ba61927
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="e53b1-104">Azure CLI 2.0 での JMESPath クエリの使用</span><span class="sxs-lookup"><span data-stu-id="e53b1-104">Using JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="e53b1-105">Azure CLI 2.0 は、`--query` パラメーターを使用して、`az` コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-105">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="e53b1-106">JMESPath は、JSON 出力用の強力なクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="e53b1-106">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="e53b1-107">JMESPath クエリに慣れていない場合は、[JMESPath.org/tutorial](http://JMESPath.org/tutorial.html) にあるチュートリアルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-107">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="e53b1-108">`Query` パラメーターは、Azure CLI 2.0 内のすべてのリソースの種類 (Container Services、Web Apps、VM など) でサポートされており、さまざまな目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-108">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="e53b1-109">以下に、いくつかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-109">We have listed several examples below.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="e53b1-110">単純なプロパティの選択</span><span class="sxs-lookup"><span data-stu-id="e53b1-110">Selecting simple properties</span></span>

<span data-ttu-id="e53b1-111">`table` 出力形式を指定した単純な `list` コマンドは、各リソースの種類の最も一般的で単純なプロパティの精選されたセットを、読みやすい表形式で返します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-111">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

```azurecli-interactive
az vm list --out table
```

```
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

<span data-ttu-id="e53b1-112">`--query` パラメーターを使用すると、サブスクリプション内のすべての仮想マシンのリソース グループ名と VM 名だけを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-112">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query [*].[name, resourceGroup] --out table
```

```
Column1     Column2
---------   -----------
DemoVM010   DEMORG1
demovm111   DEMORG1
demovm211   DEMORG1
demovm212   DEMORG1
demovm213   DEMORG1
demovm214   DEMORG1
demovm222   DEMORG1
KBDemo001VM RGDEMO001
KBDemo020   RGDEMO001
```

<span data-ttu-id="e53b1-113">前の例では、列見出しが "Column1" と "Column2" であることがわかります。</span><span class="sxs-lookup"><span data-stu-id="e53b1-113">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="e53b1-114">選択したプロパティにわかりやすいラベルまたは名前を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-114">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="e53b1-115">次の例では、選択したプロパティ "name" および "resourceGroup" にラベル "VMName" および "RGName" を追加しました。</span><span class="sxs-lookup"><span data-stu-id="e53b1-115">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


```azurecli-interactive
az vm list \
  --query "[].{RGName:resourceGroup, VMName:name}" --out table
```

```
RGName     VMName
---------  -----------
DEMORG1    DemoVM010
DEMORG1    demovm111
DEMORG1    demovm211
DEMORG1    demovm212
DEMORG1    demovm213
DEMORG1    demovm214
DEMORG1    demovm222
RGDEMO001  KBDemo001VM
RGDEMO001  KBDemo020
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="e53b1-116">入れ子になった複雑なプロパティの選択</span><span class="sxs-lookup"><span data-stu-id="e53b1-116">Selecting complex nested properties</span></span>

<span data-ttu-id="e53b1-117">選択の対象となるプロパティが、JSON 出力の中で深く入れ子になっている場合は、その入れ子になっているプロパティの完全パスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e53b1-117">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="e53b1-118">次の例は、vm list コマンドで VMName および OS の種類を選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e53b1-118">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

```azurecli-interactive
az vm list \
  --query "[].{VMName:name, OSType:storageProfile.osDisk.osType}" --out table
```

```
VMName       OSType
-----------  --------
DemoVM010    Linux
demovm111    Linux
demovm211    Linux
demovm212    Linux
demovm213    Linux
demovm214    Linux
demovm222    Linux
KBDemo001VM  Linux
KBDemo020    Linux
```

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="e53b1-119">contains 関数を使用したフィルター処理</span><span class="sxs-lookup"><span data-stu-id="e53b1-119">Filter with the contains function</span></span>

<span data-ttu-id="e53b1-120">JMESPath の `contains` 関数を使用すると、クエリで返される結果を絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-120">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="e53b1-121">次の例では、名前に "RGD" というテキストが含まれている VM のみをコマンドで選択します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-121">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>  

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup, 'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

<span data-ttu-id="e53b1-122">次の例では、vmSize が 'Standard_DS1' と等しい VM が結果として返されます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-122">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

```azurecli-interactive
az vm list \
  --query "[?contains(hardwareProfile.vmSize, 'Standard_DS1')]" --out table
```

```
ResourceGroup    VMName     VmId                                  Location    ProvisioningState
---------------  ---------  ------------------------------------  ----------  -------------------
DEMORG1          DemoVM010  cbd56d9b-9340-44bc-a722-25f15b578444  westus      Succeeded
DEMORG1          demovm111  c1c024eb-3837-4075-9117-bfbc212fa7da  westus      Succeeded
DEMORG1          demovm211  95eda642-417f-4036-9475-67246ac0f0d0  westus      Succeeded
DEMORG1          demovm212  4bdac85d-c2f7-410f-9907-ca7921d930b4  westus      Succeeded
DEMORG1          demovm213  2131c664-221a-4b7f-9653-f6d542fbfa34  westus      Succeeded
DEMORG1          demovm214  48f419af-d27a-4df0-87f3-9481007c2e5a  westus      Succeeded
DEMORG1          demovm222  e0f59516-1d69-4d54-b8a2-f6c4a5d031de  westus      Succeeded
```

## <a name="filter-with-grep"></a><span data-ttu-id="e53b1-123">grep を使用したフィルター処理</span><span class="sxs-lookup"><span data-stu-id="e53b1-123">Filter with grep</span></span>

<span data-ttu-id="e53b1-124">`tsv` 出力形式は、ヘッダーのない、タブ区切りのテキストです。</span><span class="sxs-lookup"><span data-stu-id="e53b1-124">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="e53b1-125">これを `grep` や `cut` のようなコマンドにパイプ処理して、`list` 出力から特定の値をさらに解析することができます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-125">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="e53b1-126">次の例では、名前に "RGD" というテキストが含まれている VM のみを `grep` コマンドで選択します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-126">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="e53b1-127">`cut` コマンドは、出力に表示する、8 番目のフィールド (タブ区切り) の値のみを選択します。</span><span class="sxs-lookup"><span data-stu-id="e53b1-127">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="e53b1-128">jpterm を使用した調査</span><span class="sxs-lookup"><span data-stu-id="e53b1-128">Explore with jpterm</span></span>

<span data-ttu-id="e53b1-129">コマンドの出力を [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) にパイプ処理して、そこで JMESPath クエリを使用して調べることもできます。</span><span class="sxs-lookup"><span data-stu-id="e53b1-129">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

