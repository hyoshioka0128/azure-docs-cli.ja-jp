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
ms.openlocfilehash: 96092c0cced4e0f88aa8898525bc3dd348550407
ms.sourcegitcommit: 29d7366a0902488f4f4d39c2cb0e89368d5186ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="c569c-103">Azure CLI 2.0 で JMESPath クエリを使用する</span><span class="sxs-lookup"><span data-stu-id="c569c-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="c569c-104">Azure CLI 2.0 では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。</span><span class="sxs-lookup"><span data-stu-id="c569c-104">The Azure CLI 2.0 uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="c569c-105">JMESPath は、CLI の出力からデータを選択して表示できるようにする、JSON 用のクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="c569c-105">JMESPath is a query language for JSON, giving you the ability to select and present data from CLI output.</span></span> <span data-ttu-id="c569c-106">これらのクエリは、その他の表示書式設定を実行する前に、JSON 出力に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="c569c-106">These queries are executed on the JSON output, before performing any other display formatting.</span></span>

<span data-ttu-id="c569c-107">`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c569c-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="c569c-108">この記事の例では、一般的なユース ケースについて説明し、JMESPath の機能を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c569c-108">This article's examples cover common use cases and demonstrate how to use the features of JMESPath.</span></span>

## <a name="work-with-dictionary-output"></a><span data-ttu-id="c569c-109">ディクショナリ出力を使用する</span><span class="sxs-lookup"><span data-stu-id="c569c-109">Work with dictionary output</span></span>

<span data-ttu-id="c569c-110">JSON ディクショナリを返すコマンドは、キー名のみで探索できます。</span><span class="sxs-lookup"><span data-stu-id="c569c-110">Commands that return a JSON dictionary can be explored by their key names alone.</span></span> <span data-ttu-id="c569c-111">キーのパスは、`.` 文字を区切り記号として使用します。</span><span class="sxs-lookup"><span data-stu-id="c569c-111">Key paths use the `.` character as a separator.</span></span> <span data-ttu-id="c569c-112">次の例では、Linux VM に接続できる SSH 公開キーの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="c569c-112">The following example pulls a list of the public SSH keys allowed to connect to a Linux VM:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

<span data-ttu-id="c569c-113">複数の値を取得して、順序付けられた配列に配置することもできます。</span><span class="sxs-lookup"><span data-stu-id="c569c-113">You can also get multiple values, putting them in an ordered array.</span></span> <span data-ttu-id="c569c-114">この配列にキー情報はありませんが、配列の要素の順序はクエリ対象のキーの順序と一致します。</span><span class="sxs-lookup"><span data-stu-id="c569c-114">The array doesn't have any key information, but the order of the array's elements matches the order of the queried keys.</span></span> <span data-ttu-id="c569c-115">次の例では、Azure のイメージ オファリング名と OS ディスクのサイズを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c569c-115">The following example shows how to retrieve the Azure image offering name and the size of the OS disk:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

<span data-ttu-id="c569c-116">出力にキーが必要な場合は、代替ディクショナリ構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c569c-116">If you want keys in your output, you can use an alternate dictionary syntax.</span></span> <span data-ttu-id="c569c-117">ディクショナリに複数の要素を選択すると、`{displayKey:keyPath, ...}` の書式を使用して `keyPath` JMESPath 式でフィルター処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="c569c-117">Multiple element selection into a dictionary uses the format `{displayKey:keyPath, ...}` to filter on the `keyPath` JMESPath expression.</span></span> <span data-ttu-id="c569c-118">これは、`{displayKey: value}` として出力に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c569c-118">This displays in the output as `{displayKey: value}`.</span></span> <span data-ttu-id="c569c-119">次の例では、すぐ前の例のクエリを受け取り、出力にキーを割り当てることでわかりやすくしています。</span><span class="sxs-lookup"><span data-stu-id="c569c-119">The next example takes the last example's query, and makes it clearer by assigning keys to the output:</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

<span data-ttu-id="c569c-120">`table` 出力形式で情報を表示する場合は、ディクショナリ表示が特に便利です。</span><span class="sxs-lookup"><span data-stu-id="c569c-120">When displaying information in the `table` output format, dictionary display is especially useful.</span></span> <span data-ttu-id="c569c-121">これにより独自の列ヘッダーを設定できるため、出力がいっそう読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="c569c-121">This allows for setting your own column headers, making output even easier to read.</span></span> <span data-ttu-id="c569c-122">出力形式の詳細については、「[Azure CLI 2.0 コマンドの出力形式](/cli/azure/format-output-azure-cli)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c569c-122">For more information on output formats, see [Output formats for Azure CLI 2.0 commands](/cli/azure/format-output-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="c569c-123">特定のキーはフィルター処理され、テーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="c569c-123">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="c569c-124">これらのキーは、`id`、`type`、および`etag` です。</span><span class="sxs-lookup"><span data-stu-id="c569c-124">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="c569c-125">この情報を表示する必要がある場合は、キーの名前を変更し、フィルター処理を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="c569c-125">If you need to see this information, you can change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a><span data-ttu-id="c569c-126">一覧の出力を使用する</span><span class="sxs-lookup"><span data-stu-id="c569c-126">Work with list output</span></span>

<span data-ttu-id="c569c-127">複数の値を返す可能性のある CLI コマンドは、常に配列を返します。</span><span class="sxs-lookup"><span data-stu-id="c569c-127">CLI commands that may return more than one value always return an array.</span></span> <span data-ttu-id="c569c-128">配列の要素にはインデックスでアクセスできますが、CLI では順序が保証されていません。</span><span class="sxs-lookup"><span data-stu-id="c569c-128">Arrays can have their elements accessed by index, but there's never an order guarantee from the CLI.</span></span> <span data-ttu-id="c569c-129">値の配列にクエリを実行する最善の方法は、`[]` 演算子でそれらをフラット化することです。</span><span class="sxs-lookup"><span data-stu-id="c569c-129">The best way to query an array of values is to flatten them with the `[]` operator.</span></span> <span data-ttu-id="c569c-130">この演算子は、配列のキーの後、または式の最初の要素として記述します。</span><span class="sxs-lookup"><span data-stu-id="c569c-130">The operator is written after the key for the array, or as the first element in the expression.</span></span> <span data-ttu-id="c569c-131">フラット化に続いて配列の各要素に対してクエリが実行され、結果の値を新しい配列に配置します。</span><span class="sxs-lookup"><span data-stu-id="c569c-131">Flattening runs the query following it against each individual element in the array, and places the resulting values into a new array.</span></span> <span data-ttu-id="c569c-132">次の例では、名前とリソース グループ内の各 VM で実行されている OS を出力します。</span><span class="sxs-lookup"><span data-stu-id="c569c-132">The following example prints out the name and OS running on each VM in a resource group.</span></span> 

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

<span data-ttu-id="c569c-133">キーのパスの一部である配列も、同様にフラット化することができます。</span><span class="sxs-lookup"><span data-stu-id="c569c-133">Arrays that are part of a key path can be flattened as well.</span></span> <span data-ttu-id="c569c-134">次の例は、VM が接続されている NIC の Azure オブジェクト ID を取得するクエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="c569c-134">This example demonstrates a query that gets the Azure object IDs for the NICs a VM is connected to.</span></span>

```azurecli
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a><span data-ttu-id="c569c-135">述語を使用して配列出力をフィルター処理する</span><span class="sxs-lookup"><span data-stu-id="c569c-135">Filter array output with predicates</span></span>

<span data-ttu-id="c569c-136">JMESPath には、表示されるデータを除外する[フィルター式](http://jmespath.org/specification.html#filterexpressions)が用意されています。</span><span class="sxs-lookup"><span data-stu-id="c569c-136">JMESPath offers [filtering expressions](http://jmespath.org/specification.html#filterexpressions) to filter out the data displayed.</span></span> <span data-ttu-id="c569c-137">これらの式は強力で、[JMESPath 組み込み関数](http://jmespath.org/specification.html#built-in-functions)と組み合わせて、部分一致を実行したり、標準的な形式へとデータを操作したりするときに特に有用です。</span><span class="sxs-lookup"><span data-stu-id="c569c-137">These expressions are powerful, especially when combined with [JMESPath built-in functions](http://jmespath.org/specification.html#built-in-functions) to perform partial matches or manipulate data into a standard format.</span></span> <span data-ttu-id="c569c-138">フィルター式は配列データに対してのみ機能し、その他の状況で使用した場合は `null` 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c569c-138">Filtering expressions only work on array data, and when used in any other situation, return the `null` value.</span></span> <span data-ttu-id="c569c-139">たとえば、`vm list` などのコマンドの出力を取得し、フィルター処理して特定の種類の VM を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="c569c-139">For example, you can take the output of commands like `vm list` and filter on it to look for specific types of VMs.</span></span> <span data-ttu-id="c569c-140">次の例では、VM の種類を絞り込んで Windows VM のみを取得し、その名前を出力することで、前の例を強化しています。</span><span class="sxs-lookup"><span data-stu-id="c569c-140">The following example expands on the previous by filtering out the VM type to capture only Windows VMs and print their name.</span></span>

```azurecli
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="c569c-141">対話形式でのクエリの実験</span><span class="sxs-lookup"><span data-stu-id="c569c-141">Experiment with queries interactively</span></span>

<span data-ttu-id="c569c-142">JMESPath 式を試すにあたり、簡単にクエリを編集したり、出力を調べたりできる方法で作業することができます。</span><span class="sxs-lookup"><span data-stu-id="c569c-142">To experiment with JMESPath expressions, you might want to work in a way where you can quickly edit queries and inspect the output.</span></span> <span data-ttu-id="c569c-143">対話型環境が、[JMESPath ターミナル](https://github.com/jmespath/jmespath.terminal) Python パッケージによって提供されています。これにより、入力としてデータをパイプ処理し、そのデータを抽出するプログラム内クエリを記述できます。</span><span class="sxs-lookup"><span data-stu-id="c569c-143">An interactive environment is offered by the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package, which allows for piping data as input and then writing in-program queries to extract the data.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
