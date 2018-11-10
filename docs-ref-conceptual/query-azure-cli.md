---
title: Azure CLI でのクエリ コマンドの結果
description: Azure CLI コマンドの出力に対して JMESPath クエリを実行する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 1736d1677fb6c7fc83a092493e8706c2d5edfccd
ms.sourcegitcommit: 0d6b08048b5b35bf0bb3d7b91ff567adbaab2a8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "51222533"
---
# <a name="use-jmespath-queries-with-azure-cli"></a>Azure CLI で JMESPath クエリを使用する 

Azure CLI では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。 JMESPath は、CLI の出力からデータを選択して表示できるようにする、JSON 用のクエリ言語です。 これらのクエリは、表示書式設定の前に、JSON 出力に対して実行されます。

`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。 この記事の例では、一般的なユース ケースについて説明し、JMESPath の機能を使用する方法を示します。

## <a name="work-with-dictionary-output"></a>ディクショナリ出力を使用する

JSON ディクショナリを返すコマンドは、キー名のみで探索できます。 キーのパスは、`.` 文字を区切り記号として使用します。 次の例では、Linux VM に接続できる SSH 公開キーの一覧を取得します。

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

複数値は、順序付けられた配列に配置できます。 次の例では、Azure のイメージ オファリング名と OS ディスクのサイズを取得する方法を示します。

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

出力にキーが必要な場合は、代替ディクショナリ構文を使用できます。  ディクショナリに要素を選択すると、`{displayKey:keyPath, ...}` の書式を使用して `keyPath` JMESPath 式でフィルター処理が行われます。 出力値では、キー/値のペアが `{displayKey: value}` に変更されます。 次の例では、すぐ前の例のクエリを受け取り、出力にキーを割り当てることでわかりやすくしています。

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

`table` 出力形式で情報を表示する場合は、ディクショナリ表示を使用すると独自の列ヘッダーを設定できます。 出力形式の詳細については、[Azure CLI コマンドの出力形式](/cli/azure/format-output-azure-cli)に関するページをご覧ください。

> [!NOTE]
> 特定のキーはフィルター処理され、テーブル ビューには出力されません。 これらのキーは、`id`、`type`、および`etag` です。 この情報を表示する必要がある場合は、キーの名前を変更し、フィルター処理を回避することができます。
>
> ```azurecli-interactive
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a>一覧の出力を使用する

複数の値を返すことができる CLI コマンドは、配列を返します。 配列要素にはインデックスでアクセスしますが、毎回同じ順序で返されるとは限りません。 `[]` 演算子を使用して配列要素をフラット化することで、すべての配列要素に対して一度にクエリを実行できます。 この演算子は、配列の後、または式の最初の要素として配置します。 配列をフラット化すると、その後、配列の各要素に対してクエリが実行されます。

次の例では、名前とリソース グループ内の各 VM で実行されている OS を出力します。

```azurecli-interactive
az vm list -g QueryDemo --query '[].{name:name, image:storageProfile.imageReference.offer}'
```

```json
[
  {
    "image": "CentOS",
    "name": "CentBox"
  },
  {
    "image": "openSUSE-Leap",
    "name": "SUSEBox"
  },
  {
    "image": "UbuntuServer",
    "name": "TestVM"
  },
  {
    "image": "UbuntuServer",
    "name": "Test2"
  },
  {
    "image": "WindowsServer",
    "name": "WinServ"
  }
]
```

キーのパスの一部である配列も、同様にフラット化することができます。 次のクエリにより、VM が接続されている NIC の Azure オブジェクト ID が取得されます。

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a>述語を使用して配列出力をフィルター処理する

JMESPath には、表示されるデータを除外する[フィルター式](http://jmespath.org/specification.html#filterexpressions)が用意されています。 これらの式は強力で、[JMESPath 組み込み関数](http://jmespath.org/specification.html#built-in-functions)と組み合わせて、部分一致を実行したり、標準的な形式へとデータを操作したりするときに特に有用です。 フィルター式は配列データに対してのみ機能し、その他の状況で使用した場合は `null` 値が返されます。 たとえば、`vm list` などのコマンドの出力を取得し、フィルター処理して特定の種類の VM を検索することができます。 次の例では、VM の種類を絞り込んで Windows VM のみを取得し、その名前を出力することで、前の例を強化しています。

```azurecli-interactive
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a>対話形式でのクエリの実験

JMESPath の学習を開始できるように、[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python パッケージには、クエリの実験を行うための対話型環境が用意されています。 データを入力としてパイプ処理してから、データを抽出するようにプログラム内クエリを記述および編集できます。

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
