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
ms.openlocfilehash: 4522242952e5d257449c9c593885c62de2f56d0f
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178033"
---
# <a name="use-jmespath-queries-with-azure-cli"></a><span data-ttu-id="3e0ed-103">Azure CLI で JMESPath クエリを使用する</span><span class="sxs-lookup"><span data-stu-id="3e0ed-103">Use JMESPath queries with Azure CLI</span></span> 

<span data-ttu-id="3e0ed-104">Azure CLI では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-104">The Azure CLI uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="3e0ed-105">JMESPath は、CLI の出力からデータを選択して表示できるようにする、JSON 用のクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-105">JMESPath is a query language for JSON, giving you the ability to select and present data from CLI output.</span></span> <span data-ttu-id="3e0ed-106">これらのクエリは、表示書式設定の前に、JSON 出力に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-106">These queries are executed on the JSON output before any display formatting.</span></span>

<span data-ttu-id="3e0ed-107">`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="3e0ed-108">この記事の例では、一般的なユース ケースについて説明し、JMESPath の機能を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-108">This article's examples cover common use cases and demonstrate how to use the features of JMESPath.</span></span>

## <a name="work-with-dictionary-output"></a><span data-ttu-id="3e0ed-109">ディクショナリ出力を使用する</span><span class="sxs-lookup"><span data-stu-id="3e0ed-109">Work with dictionary output</span></span>

<span data-ttu-id="3e0ed-110">JSON ディクショナリを返すコマンドは、キー名のみで探索できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-110">Commands that return a JSON dictionary can be explored by their key names alone.</span></span> <span data-ttu-id="3e0ed-111">キーのパスは、`.` 文字を区切り記号として使用します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-111">Key paths use the `.` character as a separator.</span></span> <span data-ttu-id="3e0ed-112">次の例では、Linux VM に接続できる SSH 公開キーの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-112">The following example pulls a list of the public SSH keys allowed to connect to a Linux VM:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

<span data-ttu-id="3e0ed-113">複数値は、順序付けられた配列に配置できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-113">Multiple values can be put into an ordered array.</span></span> <span data-ttu-id="3e0ed-114">次の例では、Azure のイメージ オファリング名と OS ディスクのサイズを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-114">The following example shows how to retrieve the Azure image offering name and the size of the OS disk:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

<span data-ttu-id="3e0ed-115">出力にキーが必要な場合は、代替ディクショナリ構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-115">If you want keys in your output, you can use an alternate dictionary syntax.</span></span>  <span data-ttu-id="3e0ed-116">ディクショナリに要素を選択すると、`{displayKey:keyPath, ...}` の書式を使用して `keyPath` JMESPath 式でフィルター処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-116">Element selection into a dictionary uses the format `{displayKey:keyPath, ...}` to filter on the `keyPath` JMESPath expression.</span></span> <span data-ttu-id="3e0ed-117">出力値では、キー/値のペアが `{displayKey: value}` に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-117">In the output values, the key/value pairs are changed to `{displayKey: value}`.</span></span> <span data-ttu-id="3e0ed-118">次の例では、すぐ前の例のクエリを受け取り、出力にキーを割り当てることでわかりやすくしています。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-118">The next example takes the last example's query, and makes it clearer by assigning keys to the output:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

<span data-ttu-id="3e0ed-119">`table` 出力形式で情報を表示する場合は、ディクショナリ表示を使用すると独自の列ヘッダーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-119">When displaying information in the `table` output format, dictionary display allows setting your own column headers.</span></span> <span data-ttu-id="3e0ed-120">出力形式の詳細については、[Azure CLI コマンドの出力形式](/cli/azure/format-output-azure-cli)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-120">For more information on output formats, see [Output formats for Azure CLI commands](/cli/azure/format-output-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="3e0ed-121">特定のキーはフィルター処理され、テーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-121">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="3e0ed-122">これらのキーは、`id`、`type`、および`etag` です。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-122">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="3e0ed-123">この情報を表示する必要がある場合は、キーの名前を変更し、フィルター処理を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-123">If you need to see this information, you can change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a><span data-ttu-id="3e0ed-124">一覧の出力を使用する</span><span class="sxs-lookup"><span data-stu-id="3e0ed-124">Work with list output</span></span>

<span data-ttu-id="3e0ed-125">複数の値を返すことができる CLI コマンドは、配列を返します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-125">CLI commands that may return  more than one value return an array.</span></span> <span data-ttu-id="3e0ed-126">配列要素にはインデックスでアクセスしますが、毎回同じ順序で返されるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-126">Array elements are accessed by index and may not be returned in the same order every time.</span></span> <span data-ttu-id="3e0ed-127">`[]` 演算子を使用して配列要素をフラット化することで、すべての配列要素に対して一度にクエリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-127">You can query all array elements at once by flattening them with the `[]` operator.</span></span> <span data-ttu-id="3e0ed-128">この演算子は、配列の後、または式の最初の要素として配置します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-128">The operator is put after the array or as the first element in an expression.</span></span> <span data-ttu-id="3e0ed-129">配列をフラット化すると、その後、配列の各要素に対してクエリが実行されます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-129">Flattening an array runs the query after it against each element of the array.</span></span>

<span data-ttu-id="3e0ed-130">次の例では、名前とリソース グループ内の各 VM で実行されている OS を出力します。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-130">The following example prints out the name and OS running on each VM in a resource group.</span></span>

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

<span data-ttu-id="3e0ed-131">キーのパスの一部である配列も、同様にフラット化することができます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-131">Arrays that are part of a key path can be flattened as well.</span></span> <span data-ttu-id="3e0ed-132">次のクエリにより、VM が接続されている NIC の Azure オブジェクト ID が取得されます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-132">The following query gets the Azure object IDs for the NICs a VM is connected to.</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a><span data-ttu-id="3e0ed-133">述語を使用して配列出力をフィルター処理する</span><span class="sxs-lookup"><span data-stu-id="3e0ed-133">Filter array output with predicates</span></span>

<span data-ttu-id="3e0ed-134">JMESPath には、表示されるデータを除外する[フィルター式](http://jmespath.org/specification.html#filterexpressions)が用意されています。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-134">JMESPath offers [filtering expressions](http://jmespath.org/specification.html#filterexpressions) to filter out the data displayed.</span></span> <span data-ttu-id="3e0ed-135">これらの式は強力で、[JMESPath 組み込み関数](http://jmespath.org/specification.html#built-in-functions)と組み合わせて、部分一致を実行したり、標準的な形式へとデータを操作したりするときに特に有用です。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-135">These expressions are powerful, especially when combined with [JMESPath built-in functions](http://jmespath.org/specification.html#built-in-functions) to do partial matches or manipulate data into a standard format.</span></span> <span data-ttu-id="3e0ed-136">フィルター式は配列データに対してのみ機能し、その他の状況で使用した場合は `null` 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-136">Filtering expressions only work on array data, and when used in any other situation, return the `null` value.</span></span> <span data-ttu-id="3e0ed-137">たとえば、`vm list` などのコマンドの出力を取得し、フィルター処理して特定の種類の VM を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-137">For example, you can take the output of commands like `vm list` and filter on it to look for specific types of VMs.</span></span> <span data-ttu-id="3e0ed-138">次の例では、VM の種類を絞り込んで Windows VM のみを取得し、その名前を出力することで、前の例を強化しています。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-138">The following example expands on the previous by filtering out the VM type to capture only Windows VMs and print their name.</span></span>

```azurecli-interactive
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="3e0ed-139">対話形式でのクエリの実験</span><span class="sxs-lookup"><span data-stu-id="3e0ed-139">Experiment with queries interactively</span></span>

<span data-ttu-id="3e0ed-140">JMESPath の学習を開始できるように、[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python パッケージには、クエリの実験を行うための対話型環境が用意されています。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-140">To start learning JMESPath, the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package offers an interactive environment to experiment with queries.</span></span> <span data-ttu-id="3e0ed-141">データを入力としてパイプ処理してから、データを抽出するようにプログラム内クエリを記述および編集できます。</span><span class="sxs-lookup"><span data-stu-id="3e0ed-141">Data is piped as input, and then in-program queries are written and edited to extract the data.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
