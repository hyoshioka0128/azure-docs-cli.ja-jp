---
title: Azure CLI 2.0 の出力形式
description: テーブル、リスト、または JSON への Azure CLI 2.0 の出力形式を設定する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 07a5e9d913257d6aeb20a68263a6256ffadbe627
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388509"
---
# <a name="output-formats-for-azure-cli-20-commands"></a>Azure CLI 2.0 コマンドの出力形式

Azure CLI 2.0 では既定の出力形式として JSON が使用されますが、他の形式も用意されています。  CLI の出力を書式設定するには、`--output` (`--out` または `-o`) パラメーターを使用します。 引数値と出力の種類は、次のとおりです。

--output | 説明
---------|-------------------------------
`json`   | JSON 文字列。 これは、既定の設定です。
`jsonc`  | 色付けされた JSON。
`table`  | 列見出しとしてキーが使用されている ASCII テーブル。
`tsv`    | タブ区切りの値 (キーなし)

## <a name="json-output-format"></a>JSON 出力形式

次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。

```azurecli-interactive
az vm list --output json
```

次の出力では、簡潔にするため、また置き換えた情報を識別するために、一部のフィールドが省略されています。

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

## <a name="table-output-format"></a>テーブル出力形式

`table` 形式では出力が ASCII テーブルとして生成されるため、読み取りやスキャンが容易になります。 入れ子になったオブジェクトはテーブル出力には含まれませんが、クエリの一部としてフィルター処理することもできます。 この形式では一部のフィールドがテーブルに含まれないため、人の目ですばやく検索できるデータ概要が必要な場合に最適です。

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

`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。 次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。

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
> 一部のキーは、既定でテーブル ビューには出力されません。 `id`、`type`、および `etag` が、これに相当します。 出力でこれらを表示する必要がある場合は、JMESPath キー更新機能を使用してキー名を変更し、フィルター処理を回避します。
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

クエリを使用してデータをフィルター処理する方法の詳細については、「[Azure CLI 2.0 で JMESPath クエリを使用する](/cli/azure/query-azure-cli)」を参照してください。

## <a name="tsv-output-format"></a>TSV 出力形式

`tsv` 出力形式では、追加の書式設定、キー、またはその他の記号なしで、タブと改行で区切られた値が返されます。 この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。 `table` 形式と同じく、`tsv` では、入れ子になったオブジェクトは出力されません。

前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。

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

次の例は、`tsv` の出力を Bash の他のコマンドにパイプ処理する方法を示しています。 `grep` によって "RGD" というテキストが含まれている項目を選択し、`cut` コマンドによって 8 番目のフィールドの値を選択して、VM の名前を出力に表示します。

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

タブ区切りのフィールドを処理できるように、値は、JSON オブジェクトの出力と同じ順序で表示されます。 コマンドの実行間で、この順序に一貫性があることが保証されます。

## <a name="set-the-default-output-format"></a>既定の出力形式を設定する

対話型の `az configure` コマンドを使用して、環境を設定し、出力形式の既定の設定を確立します。 既定の出力形式は `json` です。

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

ご利用環境の構成方法の詳細については、「[Azure CLI 2.0 configuration (Azure CLI 2.0 の構成)](/cli/azure/azure-cli-configuration)」を参照してください。