---
title: "Azure CLI 2.0 の出力形式"
description: "テーブル、リスト、または JSON への Azure CLI 2.0 の出力形式を設定する方法について説明します。"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a5d629675b468421e3abee41b9c8bffd7e96e5b0
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="50fad-103">Azure CLI 2.0 コマンドの出力形式</span><span class="sxs-lookup"><span data-stu-id="50fad-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="50fad-104">Azure CLI 2.0 では、既定の出力オプションとして JSON が使用されますが、任意のコマンドの出力形式を設定するためのさまざまな方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="50fad-104">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="50fad-105">`--output` (または `--out` か `-o`) パラメーターを使用して、コマンドの出力形式を、次の表に記載されている出力の種類のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="50fad-105">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table.</span></span>

<span data-ttu-id="50fad-106">--output</span><span class="sxs-lookup"><span data-stu-id="50fad-106">--output</span></span> | <span data-ttu-id="50fad-107">[説明]</span><span class="sxs-lookup"><span data-stu-id="50fad-107">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="50fad-108">JSON 文字列。</span><span class="sxs-lookup"><span data-stu-id="50fad-108">json string.</span></span> <span data-ttu-id="50fad-109">`json` は既定値です。</span><span class="sxs-lookup"><span data-stu-id="50fad-109">`json` is the default.</span></span>
`jsonc`  | <span data-ttu-id="50fad-110">色付けされた JSON 文字列。</span><span class="sxs-lookup"><span data-stu-id="50fad-110">colorized json string.</span></span>
`table`  | <span data-ttu-id="50fad-111">列見出し付きのテーブル。</span><span class="sxs-lookup"><span data-stu-id="50fad-111">table with column headings.</span></span>
`tsv`    | <span data-ttu-id="50fad-112">タブ区切りの値。</span><span class="sxs-lookup"><span data-stu-id="50fad-112">tab-separated values.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a><span data-ttu-id="50fad-113">JSON オプションの使用</span><span class="sxs-lookup"><span data-stu-id="50fad-113">Using the json option</span></span>

<span data-ttu-id="50fad-114">次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="50fad-114">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="50fad-115">結果は次の形式になります (簡潔にするために、出力の一部のみを示しています)。</span><span class="sxs-lookup"><span data-stu-id="50fad-115">The results are in this form (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "demorg1"
        }
      ]
    },
          ...
          ...
          ...
]
```

## <a name="using-the-table-option"></a><span data-ttu-id="50fad-116">table オプションの使用</span><span class="sxs-lookup"><span data-stu-id="50fad-116">Using the table option</span></span>

<span data-ttu-id="50fad-117">table オプションを使用すると、一連の出力は読みやすくなりますが、上記の .json の例とは異なり、単純な `--output table` では入れ子になったオブジェクトが出力に含まれないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="50fad-117">The table option provides an easy to read set of output, but note that nested objects are not included in the output with the simple `--output table`, unlike the preceding .json example.</span></span>  <span data-ttu-id="50fad-118">同じ例で 'table' 出力形式を使用すると、最も一般的なプロパティ値の精選された一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="50fad-118">Using the same example with 'table' output format provides a curated list of most common property values.</span></span>

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

<span data-ttu-id="50fad-119">`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="50fad-119">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="50fad-120">次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="50fad-120">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli-interactive
az vm list --query "[].{ resource: resourceGroup, name: name }" -o table
```

```
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

## <a name="using-the-tsv-option"></a><span data-ttu-id="50fad-121">tsv オプションの使用</span><span class="sxs-lookup"><span data-stu-id="50fad-121">Using the tsv option</span></span>

<span data-ttu-id="50fad-122">'tsv' 出力形式では、見出しとダッシュが含まれない、単純なテキスト ベースのタブ区切りの出力が返されます。</span><span class="sxs-lookup"><span data-stu-id="50fad-122">'tsv' output format returns a simple text-based and tab-separated output with no headings and dashes.</span></span> <span data-ttu-id="50fad-123">この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="50fad-123">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="50fad-124">前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。</span><span class="sxs-lookup"><span data-stu-id="50fad-124">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus  DemoVM010           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus  demovm212           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus  demovm213           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus  KBDemo001VM         None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines   14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None   None    westus  KBDemo020           None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="50fad-125">次の例は、`tsv` の出力を `grep` や `cut` のようなコマンドにパイプ処理し、`list` 出力から特定の値をさらに解析する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="50fad-125">The next example shows how the `tsv` output can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="50fad-126">`grep` コマンドは "RGD" というテキストが含まれている項目のみを選択し、`cut` コマンドは出力に表示する 8 番目のフィールド (タブ区切り) の値のみを選択します。</span><span class="sxs-lookup"><span data-stu-id="50fad-126">The `grep` command selects only items that have text "RGD" in them and then the `cut` command selects only the eighth field (separated by tabs) value to show in the output.</span></span>

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a><span data-ttu-id="50fad-127">既定の出力形式の設定</span><span class="sxs-lookup"><span data-stu-id="50fad-127">Setting the default output format</span></span>

<span data-ttu-id="50fad-128">`az configure` コマンドを使用して、環境を設定したり、出力形式の既定の設定などの基本設定を確立したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="50fad-128">You can use the `az configure` command to set up your environment or establish preferences such as default settings for output formats.</span></span> <span data-ttu-id="50fad-129">一般的な使用では、最も簡単な既定の出力形式は "table" 形式であるため、出力形式の選択を求めるメッセージが表示されたら **3** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50fad-129">For common use, the easiest output format default is the "table" format - select **3** when prompted for output format choices.</span></span>

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```
