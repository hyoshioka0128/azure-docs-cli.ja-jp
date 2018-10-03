---
title: Azure CLI の出力形式
description: テーブル、リスト、または JSON への Azure CLI の出力形式を設定する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 5b5d962e244037d9c904fc5c75314661130d1910
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178067"
---
# <a name="output-formats-for-azure-cli-commands"></a><span data-ttu-id="509b4-103">Azure CLI コマンドの出力形式</span><span class="sxs-lookup"><span data-stu-id="509b4-103">Output formats for Azure CLI commands</span></span>

<span data-ttu-id="509b4-104">Azure CLI では既定の出力形式として JSON が使用されますが、他の形式も用意されています。</span><span class="sxs-lookup"><span data-stu-id="509b4-104">The Azure CLI uses JSON as its default output format, but offers other formats.</span></span>  <span data-ttu-id="509b4-105">CLI の出力を書式設定するには、`--output` (`--out` または `-o`) パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="509b4-105">Use the `--output` (`--out` or `-o`) parameter to format CLI output.</span></span> <span data-ttu-id="509b4-106">引数値と出力の種類は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="509b4-106">The argument values and types of output are:</span></span>

<span data-ttu-id="509b4-107">--output</span><span class="sxs-lookup"><span data-stu-id="509b4-107">--output</span></span> | <span data-ttu-id="509b4-108">説明</span><span class="sxs-lookup"><span data-stu-id="509b4-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="509b4-109">JSON 文字列。</span><span class="sxs-lookup"><span data-stu-id="509b4-109">JSON string.</span></span> <span data-ttu-id="509b4-110">これは、既定の設定です。</span><span class="sxs-lookup"><span data-stu-id="509b4-110">This setting is the default.</span></span>
`jsonc`  | <span data-ttu-id="509b4-111">色付けされた JSON。</span><span class="sxs-lookup"><span data-stu-id="509b4-111">Colorized JSON.</span></span>
`yaml`   | <span data-ttu-id="509b4-112">YAML。JSON に代わる、コンピューターが読み取り可能な形式。</span><span class="sxs-lookup"><span data-stu-id="509b4-112">YAML, a machine-readable alternative to JSON.</span></span>
`table`  | <span data-ttu-id="509b4-113">列見出しとしてキーが使用されている ASCII テーブル。</span><span class="sxs-lookup"><span data-stu-id="509b4-113">ASCII table with keys as column headings.</span></span>
`tsv`    | <span data-ttu-id="509b4-114">タブ区切りの値 (キーなし)</span><span class="sxs-lookup"><span data-stu-id="509b4-114">Tab-separated values, with no keys</span></span>

## <a name="json-output-format"></a><span data-ttu-id="509b4-115">JSON 出力形式</span><span class="sxs-lookup"><span data-stu-id="509b4-115">JSON output format</span></span>

<span data-ttu-id="509b4-116">次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-116">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="509b4-117">次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。</span><span class="sxs-lookup"><span data-stu-id="509b4-117">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="yaml-output-format"></a><span data-ttu-id="509b4-118">YAML 出力形式</span><span class="sxs-lookup"><span data-stu-id="509b4-118">YAML output format</span></span>

<span data-ttu-id="509b4-119">`yaml` 形式では、出力が [YAML](http://yaml.org/) として、つまりプレーン テキスト データのシリアル化形式として出力されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-119">The `yaml` format prints output as [YAML](http://yaml.org/), a plain-text data serialization format.</span></span> <span data-ttu-id="509b4-120">YAML は JSON より読みやすくなる傾向があり、その形式に簡単にマップされます。</span><span class="sxs-lookup"><span data-stu-id="509b4-120">YAML tends to be easier to read than JSON, and easily maps to that format.</span></span> <span data-ttu-id="509b4-121">一部のアプリケーションおよび CLI コマンドは、構成の入力として、JSON ではなく YAML を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="509b4-121">Some applications and CLI commands take YAML as configuration input, instead of JSON.</span></span>

```azurecli-interactive
az vm list --out yaml
```

<span data-ttu-id="509b4-122">次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。</span><span class="sxs-lookup"><span data-stu-id="509b4-122">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

```yaml
- availabilitySet: null
  diagnosticsProfile: null
  hardwareProfile:
    vmSize: Standard_DS1_v2
  id: /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010
  identity: null
  instanceView: null
  licenseType: null
  location: westus
  name: ExampleVM1
  networkProfile:
    networkInterfaces:
    - id: /subscriptions/.../resourceGroups/DemoRG1/providers/Microsoft.Network/networkInterfaces/DemoVM010Nic
      primary: null
      resourceGroup: DemoRG1
  ...
...
```

## <a name="table-output-format"></a><span data-ttu-id="509b4-123">テーブル出力形式</span><span class="sxs-lookup"><span data-stu-id="509b4-123">Table output format</span></span>

<span data-ttu-id="509b4-124">`table` 形式では出力が ASCII テーブルとして生成されるため、読み取りやスキャンが容易になります。</span><span class="sxs-lookup"><span data-stu-id="509b4-124">The `table` format prints output as an ASCII table, making it easy to read and scan.</span></span> <span data-ttu-id="509b4-125">入れ子になったオブジェクトはテーブル出力には含まれませんが、クエリの一部としてフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="509b4-125">Nested objects aren't included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="509b4-126">この形式では一部のフィールドがテーブルに含まれないため、人の目ですばやく検索できるデータ概要が必要な場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="509b4-126">Some fields aren't included in the table, so this format is best when you want a quick, human-searchable overview of data.</span></span>

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

<span data-ttu-id="509b4-127">`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="509b4-127">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="509b4-128">次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="509b4-128">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

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
> <span data-ttu-id="509b4-129">一部のキーは、既定でテーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="509b4-129">Some keys are not printed in the table view by default.</span></span> <span data-ttu-id="509b4-130">`id`、`type`、および `etag` が、これに相当します。</span><span class="sxs-lookup"><span data-stu-id="509b4-130">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="509b4-131">出力でこれらを表示する必要がある場合は、JMESPath キー更新機能を使用してキー名を変更し、フィルター処理を回避します。</span><span class="sxs-lookup"><span data-stu-id="509b4-131">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="509b4-132">クエリを使用してデータをフィルター処理する方法の詳細については、「[Azure CLI で JMESPath クエリを使用する](/cli/azure/query-azure-cli)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="509b4-132">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="509b4-133">TSV 出力形式</span><span class="sxs-lookup"><span data-stu-id="509b4-133">TSV output format</span></span>

<span data-ttu-id="509b4-134">`tsv` 出力形式では、追加の書式設定、キー、またはその他の記号なしで、タブと改行で区切られた値が返されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-134">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="509b4-135">この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="509b4-135">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="509b4-136">`table` 形式と同じく、`tsv` では、入れ子になったオブジェクトは出力されません。</span><span class="sxs-lookup"><span data-stu-id="509b4-136">Like the `table` format, `tsv` doesn't print nested objects.</span></span>

<span data-ttu-id="509b4-137">前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-137">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```output
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="509b4-138">次の例は、`tsv` の出力を Bash の他のコマンドにパイプ処理する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="509b4-138">The next example shows how `tsv` output can be piped to other commands in bash.</span></span> <span data-ttu-id="509b4-139">`grep` によって "RGD" というテキストが含まれている項目を選択し、`cut` コマンドによって 8 番目のフィールドの値を選択して、VM の名前を出力に表示します。</span><span class="sxs-lookup"><span data-stu-id="509b4-139">`grep` selects items that have text "RGD" in them, then the `cut` command selects the eighth field to show the name of the VM in output.</span></span>

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

<span data-ttu-id="509b4-140">タブ区切りのフィールドを処理できるように、値は、JSON オブジェクトの出力と同じ順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-140">For the purposes of processing tab-separated fields, the values are in the same order that they appear in the printed JSON object.</span></span> <span data-ttu-id="509b4-141">コマンドの実行間で、この順序に一貫性があることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="509b4-141">This order is guaranteed to be consistent between runs of the command.</span></span>

## <a name="set-the-default-output-format"></a><span data-ttu-id="509b4-142">既定の出力形式を設定する</span><span class="sxs-lookup"><span data-stu-id="509b4-142">Set the default output format</span></span>

<span data-ttu-id="509b4-143">対話型の `az configure` コマンドを使用して、環境を設定し、出力形式の既定の設定を確立します。</span><span class="sxs-lookup"><span data-stu-id="509b4-143">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="509b4-144">既定の出力形式は `json` です。</span><span class="sxs-lookup"><span data-stu-id="509b4-144">The default output format is `json`.</span></span>

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

<span data-ttu-id="509b4-145">ご利用環境の構成方法の詳細については、「[Azure CLI の構成](/cli/azure/azure-cli-configuration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="509b4-145">To learn more about configuring your environment, see [Azure CLI configuration](/cli/azure/azure-cli-configuration).</span></span>
