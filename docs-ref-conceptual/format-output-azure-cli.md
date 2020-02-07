---
title: Azure CLI の出力形式
description: テーブル、リスト、または JSON への Azure CLI の出力形式を設定する方法について説明します。
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 09/23/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: adb488081076715eb080d1972bba18d285402e95
ms.sourcegitcommit: a233bb75e27a5c8772c173f195e74d12381b7a64
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2020
ms.locfileid: "76890458"
---
# <a name="output-formats-for-azure-cli-commands"></a><span data-ttu-id="87212-103">Azure CLI コマンドの出力形式</span><span class="sxs-lookup"><span data-stu-id="87212-103">Output formats for Azure CLI commands</span></span>

<span data-ttu-id="87212-104">Azure CLI では既定の出力形式として JSON が使用されますが、他の形式も用意されています。</span><span class="sxs-lookup"><span data-stu-id="87212-104">The Azure CLI uses JSON as its default output format, but offers other formats.</span></span>  <span data-ttu-id="87212-105">CLI の出力を書式設定するには、`--output` (`--out` または `-o`) パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="87212-105">Use the `--output` (`--out` or `-o`) parameter to format CLI output.</span></span> <span data-ttu-id="87212-106">引数値と出力の種類は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="87212-106">The argument values and types of output are:</span></span>

<span data-ttu-id="87212-107">--output</span><span class="sxs-lookup"><span data-stu-id="87212-107">--output</span></span> | <span data-ttu-id="87212-108">[説明]</span><span class="sxs-lookup"><span data-stu-id="87212-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="87212-109">JSON 文字列。</span><span class="sxs-lookup"><span data-stu-id="87212-109">JSON string.</span></span> <span data-ttu-id="87212-110">この設定が既定値です</span><span class="sxs-lookup"><span data-stu-id="87212-110">This setting is the default</span></span>
`jsonc`  | <span data-ttu-id="87212-111">色付けされた JSON</span><span class="sxs-lookup"><span data-stu-id="87212-111">Colorized JSON</span></span>
`yaml`   | <span data-ttu-id="87212-112">YAML。JSON に代わる、コンピューターが読み取り可能な形式</span><span class="sxs-lookup"><span data-stu-id="87212-112">YAML, a machine-readable alternative to JSON</span></span>
`table`  | <span data-ttu-id="87212-113">列見出しとしてキーが使用されている ASCII テーブル</span><span class="sxs-lookup"><span data-stu-id="87212-113">ASCII table with keys as column headings</span></span>
`tsv`    | <span data-ttu-id="87212-114">タブ区切りの値 (キーなし)</span><span class="sxs-lookup"><span data-stu-id="87212-114">Tab-separated values, with no keys</span></span>
`none`   | <span data-ttu-id="87212-115">エラーと警告以外は出力されません</span><span class="sxs-lookup"><span data-stu-id="87212-115">No output other than errors and warnings</span></span>

## <a name="json-output-format"></a><span data-ttu-id="87212-116">JSON 出力形式</span><span class="sxs-lookup"><span data-stu-id="87212-116">JSON output format</span></span>

<span data-ttu-id="87212-117">次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="87212-117">The following example displays the list of virtual machines in your subscriptions in the default JSON format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="87212-118">次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。</span><span class="sxs-lookup"><span data-stu-id="87212-118">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="yaml-output-format"></a><span data-ttu-id="87212-119">YAML 出力形式</span><span class="sxs-lookup"><span data-stu-id="87212-119">YAML output format</span></span>

<span data-ttu-id="87212-120">`yaml` 形式では、出力が [YAML](http://yaml.org/) として、つまりプレーン テキスト データのシリアル化形式として出力されます。</span><span class="sxs-lookup"><span data-stu-id="87212-120">The `yaml` format prints output as [YAML](http://yaml.org/), a plain-text data serialization format.</span></span> <span data-ttu-id="87212-121">YAML は JSON より読みやすくなる傾向があり、その形式に簡単にマップされます。</span><span class="sxs-lookup"><span data-stu-id="87212-121">YAML tends to be easier to read than JSON, and easily maps to that format.</span></span> <span data-ttu-id="87212-122">一部のアプリケーションおよび CLI コマンドは、構成の入力として、JSON ではなく YAML を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="87212-122">Some applications and CLI commands take YAML as configuration input, instead of JSON.</span></span>

```azurecli-interactive
az vm list --out yaml
```

<span data-ttu-id="87212-123">次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。</span><span class="sxs-lookup"><span data-stu-id="87212-123">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="table-output-format"></a><span data-ttu-id="87212-124">テーブル出力形式</span><span class="sxs-lookup"><span data-stu-id="87212-124">Table output format</span></span>

<span data-ttu-id="87212-125">`table` 形式では出力が ASCII テーブルとして生成されるため、読み取りやスキャンが容易になります。</span><span class="sxs-lookup"><span data-stu-id="87212-125">The `table` format prints output as an ASCII table, making it easy to read and scan.</span></span> <span data-ttu-id="87212-126">入れ子になったオブジェクトはテーブル出力には含まれませんが、クエリの一部としてフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="87212-126">Nested objects aren't included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="87212-127">この形式では一部のフィールドがテーブルに含まれないため、人の目ですばやく検索できるデータ概要が必要な場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="87212-127">Some fields aren't included in the table, so this format is best when you want a quick, human-searchable overview of data.</span></span>

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

<span data-ttu-id="87212-128">`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="87212-128">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="87212-129">次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="87212-129">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

```azurecli-interactive
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
> <span data-ttu-id="87212-130">一部のキーは、既定でテーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="87212-130">Some keys are not printed in the table view by default.</span></span> <span data-ttu-id="87212-131">`id`、`type`、および `etag` が、これに相当します。</span><span class="sxs-lookup"><span data-stu-id="87212-131">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="87212-132">出力でこれらを表示する必要がある場合は、JMESPath キー更新機能を使用してキー名を変更し、フィルター処理を回避します。</span><span class="sxs-lookup"><span data-stu-id="87212-132">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli-interactive
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="87212-133">クエリを使用してデータをフィルター処理する方法の詳細については、「[Azure CLI で JMESPath クエリを使用する](/cli/azure/query-azure-cli)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87212-133">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="87212-134">TSV 出力形式</span><span class="sxs-lookup"><span data-stu-id="87212-134">TSV output format</span></span>

<span data-ttu-id="87212-135">`tsv` 出力形式では、追加の書式設定、キー、またはその他の記号なしで、タブと改行で区切られた値が返されます。</span><span class="sxs-lookup"><span data-stu-id="87212-135">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="87212-136">この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="87212-136">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="87212-137">`table` 形式と同じく、`tsv` では、入れ子になったオブジェクトは出力されません。</span><span class="sxs-lookup"><span data-stu-id="87212-137">Like the `table` format, `tsv` doesn't print nested objects.</span></span>

<span data-ttu-id="87212-138">前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。</span><span class="sxs-lookup"><span data-stu-id="87212-138">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

```azurecli-interactive
az vm list --out tsv
```

```output
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo020   None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    36baa9-9b80-48a8-b4a9-854c7a858ece
```

<span data-ttu-id="87212-139">TSV 出力形式の制限の 1 つは、出力順序が保証されないことです。</span><span class="sxs-lookup"><span data-stu-id="87212-139">One restriction of the TSV output format is that there isn't a guarantee on output ordering.</span></span> <span data-ttu-id="87212-140">CLI では、順序を最大限維持するために、応答 JSON 内のキーをアルファベット順に並べ替え、次にそれらの値を TSV 出力用の順序で表示します。</span><span class="sxs-lookup"><span data-stu-id="87212-140">The CLI makes a best effort to preserve ordering by sorting keys in the response JSON alphebetically, and then printing their values in order for TSV output.</span></span> <span data-ttu-id="87212-141">これは、順序が常に同じであることを保証するものではありません。Azure サービスの応答形式が変更される可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="87212-141">This isn't a guarantee that the order is always identical though, since the Azure service response format may change.</span></span>

<span data-ttu-id="87212-142">一貫した順序を強制するには、`--query` パラメーターと[複数選択リスト](query-azure-cli.md#get-multiple-values)の形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87212-142">In order to enforce consistent ordering, you'll need to use the `--query` parameter and the [multiselect list](query-azure-cli.md#get-multiple-values) format.</span></span> <span data-ttu-id="87212-143">CLI コマンドが 1 つの JSON 辞書を返す場合は、一般的な形式 (`[key1, key2, ..., keyN]`) を使用してキーの順序を強制します。</span><span class="sxs-lookup"><span data-stu-id="87212-143">When a CLI command returns a single JSON dictionary, use the general format `[key1, key2, ..., keyN]` to force a key order.</span></span>  <span data-ttu-id="87212-144">配列を返す CLI コマンドの場合、一般的な形式 (`[].[key1, key2, ..., keyN]`) を使用して列の値を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="87212-144">For CLI commands which return an array, use the general format `[].[key1, key2, ..., keyN]` to order column values.</span></span>

<span data-ttu-id="87212-145">たとえば、上に表示されている情報を ID、場所、リソース グループ、VM 名で並べ替えるには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="87212-145">For example, to order the information displayed above by ID, location, resource group, and VM name:</span></span>

```azurecli-interactive
az vm list --out tsv --query '[].[id, location, resourceGroup, name]'
```

```output
/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    westus    DEMORG1    DemoVM010
/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    westus    DEMORG1    demovm212
/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    westus    DEMORG1    demovm213
/subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM     westus  RGDEMO001       KBDemo001VM
/subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo020       westus  RGDEMO001       KBDemo020
```

<span data-ttu-id="87212-146">次の例は、`tsv` の出力を Bash の他のコマンドにパイプ処理する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="87212-146">The next example shows how `tsv` output can be piped to other commands in bash.</span></span> <span data-ttu-id="87212-147">このクエリを使用して出力をフィルターにかけて順序を強制し、`grep` によって "RGD" というテキストが含まれている項目を選択し、`cut` コマンドによって 4 番目のフィールドの値を選択して VM の名前を出力に表示します。</span><span class="sxs-lookup"><span data-stu-id="87212-147">The query is used to filter output and force ordering, `grep` selects items that have text "RGD" in them, then the `cut` command selects the fourth field to show the name of the VM in output.</span></span>

```azurecli-interactive
az vm list --out tsv --query '[].[id, location, resourceGroup, name]' | grep RGD | cut -f4
```

```output
KBDemo001VM
KBDemo020
```

## <a name="set-the-default-output-format"></a><span data-ttu-id="87212-148">既定の出力形式を設定する</span><span class="sxs-lookup"><span data-stu-id="87212-148">Set the default output format</span></span>

<span data-ttu-id="87212-149">対話型の `az configure` コマンドを使用して、環境を設定し、出力形式の既定の設定を確立します。</span><span class="sxs-lookup"><span data-stu-id="87212-149">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="87212-150">既定の出力形式は `json` です。</span><span class="sxs-lookup"><span data-stu-id="87212-150">The default output format is `json`.</span></span>

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
 [1] json - JSON formatted output that most closely matches API responses.
 [2] jsonc - Colored JSON formatted output that most closely matches API responses.
 [3] table - Human-readable output format.
 [4] tsv - Tab- and Newline-delimited. Great for GREP, AWK, etc.
 [5] yaml - YAML formatted output. An alternative to JSON. Great for configuration files.
 [6] none - No output, except for errors and warnings.
Please enter a choice [1]:
```

<span data-ttu-id="87212-151">ご利用環境の構成方法の詳細については、「[Azure CLI の構成](/cli/azure/azure-cli-configuration)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87212-151">To learn more about configuring your environment, see [Azure CLI configuration](/cli/azure/azure-cli-configuration).</span></span>
