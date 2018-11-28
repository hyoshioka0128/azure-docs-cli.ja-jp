---
title: Azure CLI でのクエリ コマンドの結果
description: Azure CLI コマンドの出力に対して JMESPath クエリを実行する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/12/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 53aa2d1011eb76c27a503e6b15c20aa05e13b448
ms.sourcegitcommit: f92d5b3ccd409be126f1e7c06b9f1adc98dad78b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2018
ms.locfileid: "52159390"
---
# <a name="query-azure-cli-command-output"></a><span data-ttu-id="08819-103">Azure CLI コマンドの出力のクエリ</span><span class="sxs-lookup"><span data-stu-id="08819-103">Query Azure CLI command output</span></span>

<span data-ttu-id="08819-104">Azure CLI では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-104">The Azure CLI uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="08819-105">JMESPath は、CLI の出力からデータを選択して変更できるようにする、JSON 用のクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="08819-105">JMESPath is a query language for JSON, giving you the ability to select and modify data from CLI output.</span></span> <span data-ttu-id="08819-106">クエリは、表示書式設定の前に JSON 出力に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="08819-106">Queries are executed on the JSON output before any display formatting.</span></span>

<span data-ttu-id="08819-107">`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="08819-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="08819-108">この記事では、一連の簡単な例を使って、JMESPath の機能の使用方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="08819-108">This article covers how to use the features of JMESPath with a series of small, simple examples.</span></span>

## <a name="dictionary-and-list-cli-results"></a><span data-ttu-id="08819-109">CLI の結果である辞書とリスト</span><span class="sxs-lookup"><span data-stu-id="08819-109">Dictionary and list CLI results</span></span>

<span data-ttu-id="08819-110">JSON 以外の出力形式を使用している場合でも、CLI コマンドの結果は、クエリのためにまず JSON として扱われます。</span><span class="sxs-lookup"><span data-stu-id="08819-110">Even when using an output format other than JSON, CLI command results are first treated as JSON for queries.</span></span> <span data-ttu-id="08819-111">CLI の結果は、JSON 配列または JSON 辞書です。</span><span class="sxs-lookup"><span data-stu-id="08819-111">CLI results are either a JSON array or dictionary.</span></span> <span data-ttu-id="08819-112">配列はインデックスを作成できるオブジェクトのシーケンスであり、辞書はキーを使用してアクセスされる順序指定されていないオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="08819-112">Arrays are sequences of objects that can be indexed, and dictionaries are unordered objects accessed with keys.</span></span> <span data-ttu-id="08819-113">複数のオブジェクトを返すことが "_できる_" コマンドは配列を返し、"_常に_" 単一オブジェクト "_のみ_" を返すコマンドは辞書を返します。</span><span class="sxs-lookup"><span data-stu-id="08819-113">Commands that _could_ return more than one object return an array, and commands that _always_ return _only_ a single object return a dictionary.</span></span>

## <a name="get-properties-in-a-dictionary"></a><span data-ttu-id="08819-114">辞書のプロパティを取得する</span><span class="sxs-lookup"><span data-stu-id="08819-114">Get properties in a dictionary</span></span>

<span data-ttu-id="08819-115">結果として辞書を使用すると、キーだけで最上位からプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="08819-115">Working with dictionary results, you can access properties from the top level with just the key.</span></span> <span data-ttu-id="08819-116">`.` (__部分式__) 文字は、入れ子になった辞書のプロパティにアクセスする際に使用します。</span><span class="sxs-lookup"><span data-stu-id="08819-116">The `.` (__subexpression__) character is used to access properties of nested dictionaries.</span></span> <span data-ttu-id="08819-117">クエリを導入する前に、`az vm show` コマンドの未変更の出力を見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="08819-117">Before introducing queries, take a look at the unmodified output of the `az vm show` command:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM -o json
```

<span data-ttu-id="08819-118">このコマンドは辞書を出力します。</span><span class="sxs-lookup"><span data-stu-id="08819-118">The command will output a dictionary.</span></span> <span data-ttu-id="08819-119">一部の内容は省略されています。</span><span class="sxs-lookup"><span data-stu-id="08819-119">Some content has been omitted.</span></span>

```json
{
  "additionalCapabilities": null,
  "availabilitySet": null,
  "diagnosticsProfile": {
    "bootDiagnostics": {
      "enabled": true,
      "storageUri": "https://xxxxxx.blob.core.windows.net/"
    }
  },
  ...
  "osProfile": {
    "adminPassword": null,
    "adminUsername": "azureuser",
    "allowExtensionOperations": true,
    "computerName": "TestVM",
    "customData": null,
    "linuxConfiguration": {
      "disablePasswordAuthentication": true,
      "provisionVmAgent": true,
      "ssh": {
        "publicKeys": [
          {
            "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMobZNJTqgjWn/IB5xlilvE4Y+BMYpqkDnGRUcA0g9BYPgrGSQquCES37v2e3JmpfDPHFsaR+CPKlVr2GoVJMMHeRcMJhj50ZWq0hAnkJBhlZVWy8S7dwdGAqPyPmWM2iJDCVMVrLITAJCno47O4Ees7RCH6ku7kU86b1NOanvrNwqTHr14wtnLhgZ0gQ5GV1oLWvMEVg1YFMIgPRkTsSQKWCG5lLqQ45aU/4NMJoUxGyJTL9i8YxMavaB1Z2npfTQDQo9+womZ7SXzHaIWC858gWNl9e5UFyHDnTEDc14hKkf1CqnGJVcCJkmSfmrrHk/CkmF0ZT3whTHO1DhJTtV stramer@contoso",
            "path": "/home/azureuser/.ssh/authorized_keys"
          }
        ]
      }
    },
    "secrets": [],
    "windowsConfiguration": null
  },
  ....
}
```

<span data-ttu-id="08819-120">次のコマンドでは、クエリを追加して、VM への接続を許可された SSH 公開キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="08819-120">The following command gets the SSH public keys authorized to connect to the VM by adding a query:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys -o json
```

```json
[
  {
    "keyData": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMobZNJTqgjWn/IB5xlilvE4Y+BMYpqkDnGRUcA0g9BYPgrGSQquCES37v2e3JmpfDPHFsaR+CPKlVr2GoVJMMHeRcMJhj50ZWq0hAnkJBhlZVWy8S7dwdGAqPyPmWM2iJDCVMVrLITAJCno47O4Ees7RCH6ku7kU86b1NOanvrNwqTHr14wtnLhgZ0gQ5GV1oLWvMEVg1YFMIgPRkTsSQKWCG5lLqQ45aU/4NMJoUxGyJTL9i8YxMavaB1Z2npfTQDQo9+womZ7SXzHaIWC858gWNl9e5UFyHDnTEDc14hKkf1CqnGJVcCJkmSfmrrHk/CkmF0ZT3whTHO1DhJTtV stramer@contoso",
    "path": "/home/azureuser/.ssh/authorized_keys"
  }
]
```

<span data-ttu-id="08819-121">複数のプロパティを取得するには、式をコンマ区切りリストとして角かっこ `[ ]` (__複数選択リスト__) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="08819-121">To get more than one property, put expressions in square brackets  `[ ]` (a __multiselect list__) as a comma-separated list.</span></span> <span data-ttu-id="08819-122">VM 名、管理者ユーザー、SSH キーのすべてを一度に取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="08819-122">To get the VM name, admin user, and SSH key all at once use the command:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query '[name, osProfile.adminUsername, osProfile.linuxConfiguration.ssh.publicKeys[0].keyData]' -o json
```

```json
[
  "TestVM",
  "azureuser",
  "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMobZNJTqgjWn/IB5xlilvE4Y+BMYpqkDnGRUcA0g9BYPgrGSQquCES37v2e3JmpfDPHFsaR+CPKlVr2GoVJMMHeRcMJhj50ZWq0hAnkJBhlZVWy8S7dwdGAqPyPmWM2iJDCVMVrLITAJCno47O4Ees7RCH6ku7kU86b1NOanvrNwqTHr14wtnLhgZ0gQ5GV1oLWvMEVg1YFMIgPRkTsSQKWCG5lLqQ45aU/4NMJoUxGyJTL9i8YxMavaB1Z2npfTQDQo9+womZ7SXzHaIWC858gWNl9e5UFyHDnTEDc14hKkf1CqnGJVcCJkmSfmrrHk/CkmF0ZT3whTHO1DhJTtV stramer@contoso"
]
```

<span data-ttu-id="08819-123">これらの値は、クエリで指定された順序で結果の配列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="08819-123">These values are listed in the result array in the order they were given in the query.</span></span> <span data-ttu-id="08819-124">結果は配列であるため、結果に関連付けられたキーはありません。</span><span class="sxs-lookup"><span data-stu-id="08819-124">Since the result is an array, there are no keys associated with the results.</span></span>

## <a name="rename-properties-in-a-query"></a><span data-ttu-id="08819-125">クエリでプロパティの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="08819-125">Rename properties in a query</span></span>

<span data-ttu-id="08819-126">複数の値のクエリを実行するときに、配列ではなく、辞書を取得するには、`{ }` (__複数選択ハッシュ__) 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="08819-126">To get a dictionary instead of an array when querying for multiple values, use the `{ }` (__multiselect hash__) operator.</span></span>
<span data-ttu-id="08819-127">複数選択ハッシュの形式は、`{displayName:JMESPathExpression, ...}` です。</span><span class="sxs-lookup"><span data-stu-id="08819-127">The format for a multiselect hash is `{displayName:JMESPathExpression, ...}`.</span></span>
<span data-ttu-id="08819-128">`displayName` は出力に表示される文字列であり、`JMESPathExpression` は評価する JMESPath 式です。</span><span class="sxs-lookup"><span data-stu-id="08819-128">`displayName` will be the string shown in output, and `JMESPathExpression` is the JMESPath expression to evaluate.</span></span> <span data-ttu-id="08819-129">複数選択リストをハッシュに変更して、前のセクションの例を変更します。</span><span class="sxs-lookup"><span data-stu-id="08819-129">Modifying the example from the last section by changing the multiselect list to a hash:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query '{VMName:name, admin:osProfile.adminUsername, sshKey:osProfile.linuxConfiguration.ssh.publicKeys[0].keyData }' -o json
```

```json
{
  "VMName": "TestVM",
  "admin": "azureuser",
  "ssh-key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMobZNJTqgjWn/IB5xlilvE4Y+BMYpqkDnGRUcA0g9BYPgrGSQquCES37v2e3JmpfDPHFsaR+CPKlVr2GoVJMMHeRcMJhj50ZWq0hAnkJBhlZVWy8S7dwdGAqPyPmWM2iJDCVMVrLITAJCno47O4Ees7RCH6ku7kU86b1NOanvrNwqTHr14wtnLhgZ0gQ5GV1oLWvMEVg1YFMIgPRkTsSQKWCG5lLqQ45aU/4NMJoUxGyJTL9i8YxMavaB1Z2npfTQDQo9+womZ7SXzHaIWC858gWNl9e5UFyHDnTEDc14hKkf1CqnGJVcCJkmSfmrrHk/CkmF0ZT3whTHO1DhJTtV stramer@contoso"
}
```

## <a name="get-properties-in-an-array"></a><span data-ttu-id="08819-130">配列内のプロパティを取得する</span><span class="sxs-lookup"><span data-stu-id="08819-130">Get properties in an array</span></span>

<span data-ttu-id="08819-131">配列には独自のプロパティはありませんが、インデックスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="08819-131">An array has no properties of its own, but it can be indexed.</span></span> <span data-ttu-id="08819-132">この機能は、前の例の式 `publicKeys[0]` で示されています。これは、`publicKeys` 配列の最初の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="08819-132">This feature is shown in the last example with the expression `publicKeys[0]`, which gets the first element of the `publicKeys` array.</span></span> <span data-ttu-id="08819-133">CLI の出力が順序付けられているという保証はないため、順序が確かである場合や取得する要素を気にかけない場合を除き、インデックスを使用しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="08819-133">There's no guarantee CLI output is ordered, so avoid using indexing unless you're sure of the order or don't care what element you get.</span></span> <span data-ttu-id="08819-134">配列内の要素のプロパティにアクセスするには、"_フラット化_" と "_フィルター処理_" の 2 つの操作のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-134">To access the properties of elements in an array, you do one of two operations: _flattening_ and _filtering_.</span></span> <span data-ttu-id="08819-135">このセクションでは、配列をフラット化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="08819-135">This section covers how to flatten an array.</span></span>

<span data-ttu-id="08819-136">配列のフラット化は、`[]` JMESPath 演算子を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-136">Flattening an array is done with the `[]` JMESPath operator.</span></span> <span data-ttu-id="08819-137">`[]` 演算子の後のすべての式が、現在の配列内の各要素に適用されます。</span><span class="sxs-lookup"><span data-stu-id="08819-137">All expressions after the `[]` operator are applied to each element in the current array.</span></span>
<span data-ttu-id="08819-138">`[]` がクエリの先頭にある場合、CLI コマンドの結果がフラット化されます。</span><span class="sxs-lookup"><span data-stu-id="08819-138">If `[]` appears at the start of the query, it flattens the CLI command result.</span></span> <span data-ttu-id="08819-139">この機能を使用して、`az vm list` の結果を検査できます。</span><span class="sxs-lookup"><span data-stu-id="08819-139">The results of `az vm list` can be inspected with this feature.</span></span>
<span data-ttu-id="08819-140">リソース グループ内の各 VM の名前、OS、管理者名を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="08819-140">To get the name, OS, and administrator name for each VM in a resource group:</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query '[].{Name:name, OS:storageProfile.osDisk.osType, admin:osProfile.adminUsername}' -o json
```

```json
[
  {
    "Name": "Test-2",
    "OS": "Linux",
    "admin": "sttramer"
  },
  {
    "Name": "TestVM",
    "OS": "Linux",
    "admin": "azureuser"
  },
  {
    "Name": "WinTest",
    "OS": "Windows",
    "admin": "winadmin"
  }
]
```

<span data-ttu-id="08819-141">`--output table` 出力形式と組み合わせた場合、列名は複数選択ハッシュの `displayKey` 値と一致します。</span><span class="sxs-lookup"><span data-stu-id="08819-141">When combined with the `--output table` output format, the column names match up with the `displayKey` value of the multiselect hash:</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query '[].{Name:name, OS:storageProfile.osDisk.osType, Admin:osProfile.adminUsername}' --output table
```

```output
Name     OS       Admin
-------  -------  ---------
Test-2   Linux    sttramer
TestVM   Linux    azureuser
WinTest  Windows  winadmin
```

> [!NOTE]
>
> <span data-ttu-id="08819-142">特定のキーはフィルター処理され、テーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="08819-142">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="08819-143">これらのキーは、`id`、`type`、および`etag` です。</span><span class="sxs-lookup"><span data-stu-id="08819-143">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="08819-144">これらの値を表示するには、複数選択ハッシュのキー名を変更します。</span><span class="sxs-lookup"><span data-stu-id="08819-144">To see these values, you can change the key name in a multiselect hash.</span></span>
>
> ```azurecli-interactive
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

<span data-ttu-id="08819-145">コマンドから返される最上位の結果だけでなく、配列もフラット化できます。</span><span class="sxs-lookup"><span data-stu-id="08819-145">Any array can be flattened, not just the top-level result returned by the command.</span></span> <span data-ttu-id="08819-146">前のセクションでは、式 `osProfile.linuxConfiguration.ssh.publicKeys[0].keyData` を使用して、サインイン用の SSH 公開キーを取得しました。</span><span class="sxs-lookup"><span data-stu-id="08819-146">In the last section, the expression `osProfile.linuxConfiguration.ssh.publicKeys[0].keyData` was used to get the SSH public key for sign-in.</span></span> <span data-ttu-id="08819-147">"_すべての_" SSH 公開キーを取得するには、この式を `osProfile.linuxConfiguration.ssh.publicKeys[].keyData` と記述します。</span><span class="sxs-lookup"><span data-stu-id="08819-147">To get _every_ SSH public key, the expression could instead be written as `osProfile.linuxConfiguration.ssh.publicKeys[].keyData`.</span></span>
<span data-ttu-id="08819-148">このクエリ式では、`osProfile.linuxConfiguration.ssh.publicKeys` 配列をフラット化し、各要素に対して `keyData` 式を実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-148">This query expression flattens the `osProfile.linuxConfiguration.ssh.publicKeys` array, and then runs the `keyData` expression on each element:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query '{VMName:name, admin:osProfile.adminUsername, sshKeys:osProfile.linuxConfiguration.ssh.publicKeys[].keyData }' -o json
```

```json
{
  "VMName": "TestVM",
  "admin": "azureuser",
  "sshKeys": [
    "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDMobZNJTqgjWn/IB5xlilvE4Y+BMYpqkDnGRUcA0g9BYPgrGSQquCES37v2e3JmpfDPHFsaR+CPKlVr2GoVJMMHeRcMJhj50ZWq0hAnkJBhlZVWy8S7dwdGAqPyPmWM2iJDCVMVrLITAJCno47O4Ees7RCH6ku7kU86b1NOanvrNwqTHr14wtnLhgZ0gQ5GV1oLWvMEVg1YFMIgPRkTsSQKWCG5lLqQ45aU/4NMJoUxGyJTL9i8YxMavaB1Z2npfTQDQo9+womZ7SXzHaIWC858gWNl9e5UFyHDnTEDc14hKkf1CqnGJVcCJkmSfmrrHk/CkmF0ZT3whTHO1DhJTtV stramer@contoso\n"
  ]
}
```

## <a name="filter-arrays"></a><span data-ttu-id="08819-149">配列をフィルター処理する</span><span class="sxs-lookup"><span data-stu-id="08819-149">Filter arrays</span></span>

<span data-ttu-id="08819-150">配列からデータを取得するときに使用するもう 1 つの操作は "_フィルター処理_" です。</span><span class="sxs-lookup"><span data-stu-id="08819-150">The other operation used to get data from an array is _filtering_.</span></span> <span data-ttu-id="08819-151">フィルター処理は、`[?...]` JMESPath 演算子を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-151">Filtering is done with the `[?...]` JMESPath operator.</span></span>
<span data-ttu-id="08819-152">この演算子は、その内容として述語を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="08819-152">This operator takes a predicate as its contents.</span></span> <span data-ttu-id="08819-153">述語とは、`true` または `false` に評価できるステートメントです。</span><span class="sxs-lookup"><span data-stu-id="08819-153">A predicate is any statement that can be evaluated to either `true` or `false`.</span></span> <span data-ttu-id="08819-154">述語が `true` に評価された式が出力に含まれます。</span><span class="sxs-lookup"><span data-stu-id="08819-154">Expressions where the predicate evaluates to `true` are included in the output.</span></span>

<span data-ttu-id="08819-155">JMESPath では、標準の比較演算子と論理演算子が提供されています。</span><span class="sxs-lookup"><span data-stu-id="08819-155">JMESPath offers the standard comparison and logical operators.</span></span> <span data-ttu-id="08819-156">これらには、`<`、`<=`、`>`、`>=`、`==`、`!=` が含まれます。</span><span class="sxs-lookup"><span data-stu-id="08819-156">These include `<`, `<=`, `>`, `>=`, `==`, and `!=`.</span></span> <span data-ttu-id="08819-157">JMESPath では、論理 AND (`&&`)、論理 OR (`||`)、論理 NOT (`!`) もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="08819-157">JMESPath also supports logical and (`&&`), or (`||`), and not (`!`).</span></span> <span data-ttu-id="08819-158">式をかっこ内にグループ化できるので、より複雑な述語式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="08819-158">Expressions can be grouped within parenthesis, allowing for more complex predicate expressions.</span></span> <span data-ttu-id="08819-159">述語と論理演算の詳細については、[JMESPath の仕様](http://jmespath.org/specification.html)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="08819-159">For the full details on predicates and logical operations, see the [JMESPath specification](http://jmespath.org/specification.html).</span></span>

<span data-ttu-id="08819-160">前のセクションでは、配列をフラット化して、リソース グループ内のすべての VM の完全なリストを取得しました。</span><span class="sxs-lookup"><span data-stu-id="08819-160">In the last section, we flattened an array to get the complete list of all VMs in a resource group.</span></span> <span data-ttu-id="08819-161">フィルターを使用すると、この出力を Linux VM だけに制限できます。</span><span class="sxs-lookup"><span data-stu-id="08819-161">Using filters, this output can be restricted to only Linux VMs:</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query "[?storageProfile.osDisk.osType=='Linux'].{Name:name,  admin:osProfile.adminUsername}" --output table
```

```output
Name    Admin
------  ---------
Test-2  sttramer
TestVM  azureuser
```

> [!IMPORTANT]
>
> <span data-ttu-id="08819-162">JMESPath では、文字列は常に単一引用符 (`'`) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="08819-162">In JMESPath, strings are always surrounded by single quotes (`'`).</span></span> <span data-ttu-id="08819-163">フィルター述語の文字列の一部として二重引用符を使用すると、空の出力が返されます。</span><span class="sxs-lookup"><span data-stu-id="08819-163">If you use double quotes as part of a string in a filter predicate, you'll get empty output.</span></span>

<span data-ttu-id="08819-164">JMESPath には、フィルター処理に役立つ組み込み関数もあります。</span><span class="sxs-lookup"><span data-stu-id="08819-164">JMESPath also has built-in functions that can help with filtering.</span></span> <span data-ttu-id="08819-165">このような関数の 1 つである `contains(string, substring)` は、文字列に部分文字列が含まれているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="08819-165">One such function is `contains(string, substring)`, which checks to see if a string contains a substring.</span></span> <span data-ttu-id="08819-166">この関数を呼び出す前に式が評価されるので、最初の引数には完全な JMESPath 式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="08819-166">Expressions are evaluated before calling the function, so the first argument can be a full JMESPath expression.</span></span> <span data-ttu-id="08819-167">次の例では、OS ディスクに SSD ストレージを使用するすべての VM を検出します。</span><span class="sxs-lookup"><span data-stu-id="08819-167">The next example finds all VMs using SSD storage for their OS disk:</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query "[?contains(storageProfile.osDisk.managedDisk.storageAccountType,'SSD')].{Name:name, Storage:storageProfile.osDisk.managedDisk.storageAccountType}" -o json
```

```json
[
  {
    "Name": "TestVM",
    "Storage": "StandardSSD_LRS"
  },
  {
    "Name": "WinTest",
    "Storage": "StandardSSD_LRS"
  }
]
```

<span data-ttu-id="08819-168">このクエリは少し長くなっています。</span><span class="sxs-lookup"><span data-stu-id="08819-168">This query is a little long.</span></span> <span data-ttu-id="08819-169">`storageProfile.osDisk.managedDisk.storageAccountType` キーが 2 回記述され、出力でキー更新されています。</span><span class="sxs-lookup"><span data-stu-id="08819-169">The `storageProfile.osDisk.managedDisk.storageAccountType` key is mentioned twice, and rekeyed in the output.</span></span> <span data-ttu-id="08819-170">これを短くする 1 つの方法として、データをフラット化して選択した後にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="08819-170">One way to shorten it is to apply the filter after flattening and selecting data.</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query "[].{Name:name, Storage:storageProfile.osDisk.managedDisk.storageAccountType}[?contains(Storage,'SSD')]" -o json
```

```json
[
  {
    "Name": "TestVM",
    "Storage": "StandardSSD_LRS"
  },
  {
    "Name": "WinTest",
    "Storage": "StandardSSD_LRS"
  }
]
```

<span data-ttu-id="08819-171">大きな配列では、データを選択する前にフィルターを適用する方が速い場合があります。</span><span class="sxs-lookup"><span data-stu-id="08819-171">For large arrays, it may be faster to apply the filter before selecting data.</span></span>

<span data-ttu-id="08819-172">関数の全一覧については、[JMESPath の仕様の組み込み関数](http://jmespath.org/specification.html#built-in-functions)に関するセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="08819-172">See the [JMESPath specification - Built-in Functions](http://jmespath.org/specification.html#built-in-functions) for the full list of functions.</span></span>

## <a name="change-output"></a><span data-ttu-id="08819-173">出力を変更する</span><span class="sxs-lookup"><span data-stu-id="08819-173">Change output</span></span>

<span data-ttu-id="08819-174">JMESPath の関数には別の目的もあります。それは、クエリの結果を操作することです。</span><span class="sxs-lookup"><span data-stu-id="08819-174">JMESPath functions also have another purpose, which is to operate on the results of a query.</span></span> <span data-ttu-id="08819-175">ブール値以外の値を返す関数では、式の結果が変更されます。</span><span class="sxs-lookup"><span data-stu-id="08819-175">Any function that returns a non-boolean value changes the result of an expression.</span></span>
<span data-ttu-id="08819-176">たとえば、`sort_by(array, &sort_expression)` を使用して、データをプロパティ値で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="08819-176">For example, you can sort data by a property value with `sort_by(array, &sort_expression)`.</span></span> <span data-ttu-id="08819-177">JMESPath では、関数の一部として後で評価する必要がある式に、特殊演算子の `&` を使用します。</span><span class="sxs-lookup"><span data-stu-id="08819-177">JMESPath uses a special operator, `&`, for expressions that should be evaluated later as part of a function.</span></span> <span data-ttu-id="08819-178">次の例は、VM のリストを OS ディスク サイズで並べ替える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="08819-178">The next example shows how to sort a VM list by OS disk size:</span></span>

```azurecli-interactive
az vm list -g QueryDemo --query "sort_by([].{Name:name, Size:storageProfile.osDisk.diskSizeGb}, &Size)" --output table
```

```output
Name     Size
-------  ------
TestVM   30
Test-2   32
WinTest  127
```

<span data-ttu-id="08819-179">関数の全一覧については、[JMESPath の仕様の組み込み関数](http://jmespath.org/specification.html#built-in-functions)に関するセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="08819-179">See the [JMESPath specification - Built-in Functions](http://jmespath.org/specification.html#built-in-functions) for the full list of functions.</span></span>

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="08819-180">対話形式でのクエリの実験</span><span class="sxs-lookup"><span data-stu-id="08819-180">Experiment with queries interactively</span></span>

<span data-ttu-id="08819-181">JMESPath で実験を開始できるように、[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python パッケージには、クエリを操作するための対話型環境が用意されています。</span><span class="sxs-lookup"><span data-stu-id="08819-181">To start experimenting with JMESPath, the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package offers an interactive environment to work with queries.</span></span> <span data-ttu-id="08819-182">データを入力としてパイプ処理してから、クエリを記述し、エディターで実行します。</span><span class="sxs-lookup"><span data-stu-id="08819-182">Data is piped as input, and then queries are written and run in the editor.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
