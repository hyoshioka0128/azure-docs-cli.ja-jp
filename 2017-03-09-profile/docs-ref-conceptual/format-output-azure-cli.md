---
title: "Azure CLI 2.0 の出力形式"
description: "--output を使用して、テーブル、リスト、または JSON への Azure CLI 2.0 の出力形式を設定します。"
keywords: "Azure CLI 2.0, 出力, 形式, テーブル, リスト, json, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 74bdb727-481d-45f7-a44e-15d18dc55483
ms.openlocfilehash: 3e99c2533031dc063a50996f26712d4df92f65c9
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2017
---
# <a name="output-formats-for-azure-cli-20-commands"></a>Azure CLI 2.0 コマンドの出力形式

Azure CLI 2.0 では、既定の出力オプションとして JSON が使用されますが、任意のコマンドの出力形式を設定するためのさまざまな方法が用意されています。  `--output` (または `--out` か `-o`) パラメーターを使用して、コマンドの出力形式を、次の表に記載されている出力の種類のいずれかに設定します。

--output | Description
---------|-------------------------------
`json`   | JSON 文字列。 `json` は既定値です。
`jsonc`  | 色付けされた JSON 文字列。
`table`  | 列見出し付きのテーブル。
`tsv`    | タブ区切りの値。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a>JSON オプションの使用

次の例では、既定の JSON 形式で、サブスクリプション内の仮想マシンの一覧が表示されます。

```azurecli-interactive
az vm list --output json
```

結果は次の形式になります (簡潔にするために、出力の一部のみを示しています)。

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

## <a name="using-the-table-option"></a>table オプションの使用

table オプションを使用すると、一連の出力は読みやすくなりますが、上記の .json の例とは異なり、単純な `--output table` では入れ子になったオブジェクトが出力に含まれないことに注意してください。  同じ例で 'table' 出力形式を使用すると、最も一般的なプロパティ値の精選された一覧が表示されます。

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

`--query` パラメーターを使用すると、一覧の出力に表示するプロパティと列をカスタマイズすることができます。 次の例は、`list` コマンドで VM 名とリソース グループ名だけを選択する方法を示しています。

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

## <a name="using-the-tsv-option"></a>tsv オプションの使用

'tsv' 出力形式では、見出しとダッシュが含まれない、単純なテキスト ベースのタブ区切りの出力が返されます。 この形式を使用すると、なんらかの形式でテキストを処理する必要がある他のコマンドやツールで出力を簡単に利用できるようになります。 前の例で `tsv` オプションを使用すると、タブ区切りの結果が出力されます。

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

次の例は、`tsv` の出力を `grep` や `cut` のようなコマンドにパイプ処理し、`list` 出力から特定の値をさらに解析する方法を示しています。 `grep` コマンドは "RGD" というテキストが含まれている項目のみを選択し、`cut` コマンドは出力に表示する 8 番目のフィールド (タブ区切り) の値のみを選択します。

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a>既定の出力形式の設定

`az configure` コマンドを使用して、環境を設定したり、出力形式の既定の設定などの基本設定を確立したりすることができます。 一般的な使用では、最も簡単な既定の出力形式は "table" 形式であるため、出力形式の選択を求めるメッセージが表示されたら **3** を選択します。

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```