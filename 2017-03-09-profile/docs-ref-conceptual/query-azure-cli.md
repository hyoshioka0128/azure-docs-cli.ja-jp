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
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a>Azure CLI 2.0 での JMESPath クエリの使用

Azure CLI 2.0 は、`--query` パラメーターを使用して、`az` コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。 JMESPath は、JSON 出力用の強力なクエリ言語です。  JMESPath クエリに慣れていない場合は、[JMESPath.org/tutorial](http://JMESPath.org/tutorial.html) にあるチュートリアルを参照できます。

`Query` パラメーターは、Azure CLI 2.0 内のすべてのリソースの種類 (Container Services、Web Apps、VM など) でサポートされており、さまざまな目的で使用できます。  以下に、いくつかの例を示します。

## <a name="selecting-simple-properties"></a>単純なプロパティの選択

`table` 出力形式を指定した単純な `list` コマンドは、各リソースの種類の最も一般的で単純なプロパティの精選されたセットを、読みやすい表形式で返します。

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

`--query` パラメーターを使用すると、サブスクリプション内のすべての仮想マシンのリソース グループ名と VM 名だけを表示できます。

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

前の例では、列見出しが "Column1" と "Column2" であることがわかります。  選択したプロパティにわかりやすいラベルまたは名前を追加することもできます。  次の例では、選択したプロパティ "name" および "resourceGroup" にラベル "VMName" および "RGName" を追加しました。


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

## <a name="selecting-complex-nested-properties"></a>入れ子になった複雑なプロパティの選択

選択の対象となるプロパティが、JSON 出力の中で深く入れ子になっている場合は、その入れ子になっているプロパティの完全パスを指定する必要があります。 次の例は、vm list コマンドで VMName および OS の種類を選択する方法を示しています。

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

## <a name="filter-with-the-contains-function"></a>contains 関数を使用したフィルター処理

JMESPath の `contains` 関数を使用すると、クエリで返される結果を絞り込むことができます。
次の例では、名前に "RGD" というテキストが含まれている VM のみをコマンドで選択します。  

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

次の例では、vmSize が 'Standard_DS1' と等しい VM が結果として返されます。

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

## <a name="filter-with-grep"></a>grep を使用したフィルター処理

`tsv` 出力形式は、ヘッダーのない、タブ区切りのテキストです。 これを `grep` や `cut` のようなコマンドにパイプ処理して、`list` 出力から特定の値をさらに解析することができます。 次の例では、名前に "RGD" というテキストが含まれている VM のみを `grep` コマンドで選択します。  `cut` コマンドは、出力に表示する、8 番目のフィールド (タブ区切り) の値のみを選択します。

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a>jpterm を使用した調査

コマンドの出力を [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) にパイプ処理して、そこで JMESPath クエリを使用して調べることもできます。

```bash
pip install jmespath-terminal
az vm list | jpterm
```

