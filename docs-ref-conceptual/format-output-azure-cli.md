---
title: Azure CLI 2.0 の出力形式
description: テーブル、リスト、または JSON への Azure CLI 2.0 の出力形式を設定する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 016465080e95af3ab0650146e955dd8cffc569e8
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2018
ms.locfileid: "34305980"
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="2ba12-103">Azure CLI 2.0 コマンドの出力形式</span><span class="sxs-lookup"><span data-stu-id="2ba12-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="2ba12-104">Azure CLI 2.0 では、既定の出力オプションとして JSON が使用されますが、任意のコマンドの出力形式を設定するためのさまざまな方法が用意されています。</span><span class="sxs-lookup"><span data-stu-id="2ba12-104">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="2ba12-105">`--output` (または `--out` か `-o`) パラメーターを使用して、コマンドの出力形式を、次の表に記載されている出力の種類のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="2ba12-105">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table:</span></span>

<span data-ttu-id="2ba12-106">--output</span><span class="sxs-lookup"><span data-stu-id="2ba12-106">--output</span></span> | <span data-ttu-id="2ba12-107">[説明]</span><span class="sxs-lookup"><span data-stu-id="2ba12-107">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="2ba12-108">JSON 文字列。</span><span class="sxs-lookup"><span data-stu-id="2ba12-108">JSON string.</span></span> <span data-ttu-id="2ba12-109">これは、既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="2ba12-109">This setting is the default.</span></span>
`jsonc`  | <span data-ttu-id="2ba12-110">色付けされた JSON。</span><span class="sxs-lookup"><span data-stu-id="2ba12-110">Colorized JSON.</span></span>
`table`  | <span data-ttu-id="2ba12-111">列見出しとしてキーが使用されている ASCII テーブル。</span><span class="sxs-lookup"><span data-stu-id="2ba12-111">ASCII table with keys as column headings.</span></span>
`tsv`    | <span data-ttu-id="2ba12-112">タブ区切りの値 (キーなし)</span><span class="sxs-lookup"><span data-stu-id="2ba12-112">Tab-separated values, with no keys</span></span>

## <a name="json-output-format"></a><span data-ttu-id="2ba12-113">JSON 出力形式</span><span class="sxs-lookup"><span data-stu-id="2ba12-113">JSON output format</span></span>

<span data-ttu-id="2ba12-114">次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-114">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="2ba12-115">次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。</span><span class="sxs-lookup"><span data-stu-id="2ba12-115">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/.../resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
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

## <a name="table-output-format"></a><span data-ttu-id="2ba12-116">テーブル出力形式</span><span class="sxs-lookup"><span data-stu-id="2ba12-116">Table output format</span></span>

<span data-ttu-id="2ba12-117">`table` 出力形式では、行と列に並んだデータとして書式設定されたわかりやすい出力が提供されるため、簡単に読み取ったりスキャンしたりできます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-117">The `table` output format provides plain output formatted as rows and columns of collated data, making it easy to read and scan.</span></span> <span data-ttu-id="2ba12-118">入れ子になったオブジェクトはテーブル出力には含まれませんが、クエリの一部としてフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-118">Nested objects are not included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="2ba12-119">この形式ではテーブル データから一部のフィールドが除外されるため、人の目ですばやく検索できるデータ概要が必要な場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="2ba12-119">Some fields are also omitted from the table data, so this format is best when you want a quick, human-searchable overview of data.</span></span>

```azurecli-interactive
az vm list --out table
```

```output
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

<span data-ttu-id="2ba12-120">`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="2ba12-121">次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2ba12-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli
az vm list --query "[].{resource:resourceGroup, name:name}" -o table
```

```output
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

> [!NOTE]
> <span data-ttu-id="2ba12-122">特定のキーはフィルター処理され、テーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="2ba12-122">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="2ba12-123">`id`、`type`、および `etag` が、これに相当します。</span><span class="sxs-lookup"><span data-stu-id="2ba12-123">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="2ba12-124">出力でこれらを表示する必要がある場合は、JMESPath キー更新機能を使用してキー名を変更し、フィルター処理を回避します。</span><span class="sxs-lookup"><span data-stu-id="2ba12-124">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="2ba12-125">クエリを使用してデータをフィルター処理する方法の詳細については、「[Azure CLI 2.0 で JMESPath クエリを使用する](/cli/azure/query-azure-cli)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ba12-125">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI 2.0](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="2ba12-126">TSV 出力形式</span><span class="sxs-lookup"><span data-stu-id="2ba12-126">TSV output format</span></span>

<span data-ttu-id="2ba12-127">`tsv` 出力形式では、追加の書式設定、キー、またはその他の記号なしで、タブと改行で区切られた値が返されます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-127">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="2ba12-128">この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2ba12-128">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="2ba12-129">`table` 形式と同じく、`tsv` 出力オプションでは、入れ子になったオブジェクトは出力されません。</span><span class="sxs-lookup"><span data-stu-id="2ba12-129">Like the `table` format, the `tsv` output option does not print nested objects.</span></span>

<span data-ttu-id="2ba12-130">前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-130">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```output
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010 None    None    westus  DemoVM010           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212 None    None    westus  demovm212           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213 None    None    westus  demovm213           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM None    None    westus  KBDemo001VM         None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines   14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus  KBDemo020           None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines    36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="2ba12-131">次の例は、`tsv` の出力を UNIX システムの他のコマンドにパイプ処理し、特定のデータを抽出する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2ba12-131">The next example shows how the `tsv` output can be piped to other commands on UNIX systems to extract more specific data.</span></span> <span data-ttu-id="2ba12-132">`grep` コマンドは "RGD" というテキストが含まれている項目を選択し、`cut` コマンドは 8 番目のフィールド (タブ区切り) の値を選択して、VM の名前を出力に表示します。</span><span class="sxs-lookup"><span data-stu-id="2ba12-132">The `grep` command selects items that have text "RGD" in them, and then the `cut` command selects the eighth field (separated by tabs) to show the name of the VM in output.</span></span>

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

<span data-ttu-id="2ba12-133">タブ区切りのフィールドを処理できるように、値は、JSON オブジェクトの出力と同じ順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-133">For the purposes of processing tab-separated fields, the values are in the same order that they appear in the printed JSON object.</span></span> <span data-ttu-id="2ba12-134">コマンドの実行間で、この順序に一貫性があることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="2ba12-134">This order is guaranteed to be consistent between runs of the command.</span></span>

## <a name="set-the-default-output-format"></a><span data-ttu-id="2ba12-135">既定の出力形式を設定する</span><span class="sxs-lookup"><span data-stu-id="2ba12-135">Set the default output format</span></span>

<span data-ttu-id="2ba12-136">対話型の `az configure` コマンドを使用して、環境を設定し、出力形式の既定の設定を確立します。</span><span class="sxs-lookup"><span data-stu-id="2ba12-136">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="2ba12-137">既定の出力形式は `json` です。</span><span class="sxs-lookup"><span data-stu-id="2ba12-137">The default output format is `json`.</span></span> 

```azurecli-interactive
az configure
```

```output
Welcome to the Azure CLI! This command will guide you through logging in and setting some default values.

Your settings can be found at /home/defaultuser/.azure/config
Your current configuration is as follows:

  ...

Do you wish to change your settings? (y/N): y

What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab- and Newline-delimited, great for GREP, AWK, etc.
Please enter a choice [1]:
```

<span data-ttu-id="2ba12-138">ご利用環境の構成方法の詳細については、「[Azure CLI 2.0 configuration (Azure CLI 2.0 の構成)](/cli/azure/azure-cli-configuration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ba12-138">To learn more about configuring your environment, see [Azure CLI 2.0 configuration](/cli/azure/azure-cli-configuration).</span></span>