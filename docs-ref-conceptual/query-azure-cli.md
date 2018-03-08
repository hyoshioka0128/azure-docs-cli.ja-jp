---
title: "Azure CLI 2.0 でのクエリ コマンドの結果"
description: "Azure CLI 2.0 コマンドの出力に対して JMESPath クエリを実行する方法について説明します。"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/22/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 2a0cdc34bbaf0864885588ecaddff725c744c90e
ms.sourcegitcommit: 5a4c7205087d2f6c4800cf25178f0543a6157d99
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a>Azure CLI 2.0 で JMESPath クエリを使用する

Azure CLI 2.0 では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。 JMESPath は、CLI の出力からデータを選択して表示できるようにする、JSON 用のクエリ言語です。 これらのクエリは、その他の表示書式設定を実行する前に、JSON 出力に対して実行されます。

`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。 この記事の例では、一般的なユース ケースについて説明し、JMESPath の機能を使用する方法を示します。

## <a name="work-with-dictionary-output"></a>ディクショナリ出力を使用する

JSON ディクショナリを返すコマンドは、キー名のみで探索できます。 キーのパスは、`.` 文字を区切り記号として使用します。 次の例では、Linux VM に接続できる SSH 公開キーの一覧を取得します。

```azurecli
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

複数の値を取得して、順序付けられた配列に配置することもできます。 この配列にキー情報はありませんが、配列の要素の順序はクエリ対象のキーの順序と一致します。 次の例では、Azure のイメージ オファリング名と OS ディスクのサイズを取得する方法を示します。

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

出力にキーが必要な場合は、代替ディクショナリ構文を使用できます。 ディクショナリに複数の要素を選択すると、`{displayKey:keyPath, ...}` の書式を使用して `keyPath` JMESPath 式でフィルター処理が行われます。 これは、`{displayKey: value}` として出力に表示されます。 次の例では、すぐ前の例のクエリを受け取り、出力にキーを割り当てることでわかりやすくしています。

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

`table` 出力形式で情報を表示する場合は、ディクショナリ表示が特に便利です。 これにより独自の列ヘッダーを設定できるため、出力がいっそう読みやすくなります。 出力形式の詳細については、「[Azure CLI 2.0 コマンドの出力形式](/cli/azure/format-output-azure-cli)」を参照してください。

> [!NOTE]
> 特定のキーはフィルター処理され、テーブル ビューには出力されません。 これらのキーは、`id`、`type`、および`etag` です。 この情報を表示する必要がある場合は、キーの名前を変更し、フィルター処理を回避することができます。
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a>一覧の出力を使用する

複数の値を返す可能性のある CLI コマンドは、常に配列を返します。 配列の要素にはインデックスでアクセスできますが、CLI では順序が保証されていません。 値の配列にクエリを実行する最善の方法は、`[]` 演算子でそれらをフラット化することです。 この演算子は、配列のキーの後、または式の最初の要素として記述します。 フラット化に続いて配列の各要素に対してクエリが実行され、結果の値を新しい配列に配置します。 次の例では、名前とリソース グループ内の各 VM で実行されている OS を出力します。 

```azurecli
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

キーのパスの一部である配列も、同様にフラット化することができます。 次の例は、VM が接続されている NIC の Azure オブジェクト ID を取得するクエリを示しています。

```azurecli
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a>述語を使用して配列出力をフィルター処理する

JMESPath には、表示されるデータを除外する[フィルター式](http://jmespath.org/specification.html#filterexpressions)が用意されています。 これらの式は強力で、[JMESPath 組み込み関数](http://jmespath.org/specification.html#built-in-functions)と組み合わせて、部分一致を実行したり、標準的な形式へとデータを操作したりするときに特に有用です。 フィルター式は配列データに対してのみ機能し、その他の状況で使用した場合は `null` 値が返されます。 たとえば、`vm list` などのコマンドの出力を取得し、フィルター処理して特定の種類の VM を検索することができます。 次の例では、VM の種類を絞り込んで Windows VM のみを取得し、その名前を出力することで、前の例を強化しています。

```azurecli
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a>対話形式でのクエリの実験

JMESPath 式を試すにあたり、簡単にクエリを編集したり、出力を調べたりできる方法で作業することができます。 対話型環境が、[JMESPath ターミナル](https://github.com/jmespath/jmespath.terminal) Python パッケージによって提供されています。これにより、入力としてデータをパイプ処理し、そのデータを抽出するプログラム内クエリを記述できます。

```bash
pip install jmespath-terminal
az vm list | jpterm
```
