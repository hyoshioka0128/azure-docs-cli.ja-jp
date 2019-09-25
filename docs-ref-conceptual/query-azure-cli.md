---
title: Azure CLI でのクエリ コマンドの結果
description: Azure CLI コマンドの出力に対して JMESPath クエリを実行する方法について説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/23/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 39f7c885a0971db9359926a6b2f80d0a763dc4fe
ms.sourcegitcommit: 5b9b4446c08b94256ced7f63c145b493ba8b50df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "71217434"
---
# <a name="query-azure-cli-command-output"></a><span data-ttu-id="a5fe4-103">Azure CLI コマンドの出力のクエリ</span><span class="sxs-lookup"><span data-stu-id="a5fe4-103">Query Azure CLI command output</span></span>

<span data-ttu-id="a5fe4-104">Azure CLI では、`--query` 引数を使用して、コマンドの結果に対して [JMESPath クエリ](http://jmespath.org)を実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-104">The Azure CLI uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="a5fe4-105">JMESPath は、CLI の出力からデータを選択して変更できるようにする、JSON 用のクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-105">JMESPath is a query language for JSON, giving you the ability to select and modify data from CLI output.</span></span> <span data-ttu-id="a5fe4-106">クエリは、表示書式設定の前に JSON 出力に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-106">Queries are executed on the JSON output before any display formatting.</span></span>

<span data-ttu-id="a5fe4-107">`--query` 引数は、Azure CLI のすべてのコマンドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="a5fe4-108">この記事では、一連の簡単な例を使って、JMESPath の機能の使用方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-108">This article covers how to use the features of JMESPath with a series of small, simple examples.</span></span>

## <a name="dictionary-and-list-cli-results"></a><span data-ttu-id="a5fe4-109">CLI の結果である辞書とリスト</span><span class="sxs-lookup"><span data-stu-id="a5fe4-109">Dictionary and list CLI results</span></span>

<span data-ttu-id="a5fe4-110">JSON 以外の出力形式を使用している場合でも、CLI コマンドの結果は、クエリのためにまず JSON として扱われます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-110">Even when using an output format other than JSON, CLI command results are first treated as JSON for queries.</span></span> <span data-ttu-id="a5fe4-111">CLI の結果は、JSON 配列または JSON 辞書です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-111">CLI results are either a JSON array or dictionary.</span></span> <span data-ttu-id="a5fe4-112">配列はインデックスを作成できるオブジェクトのシーケンスであり、辞書はキーを使用してアクセスされる順序指定されていないオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-112">Arrays are sequences of objects that can be indexed, and dictionaries are unordered objects accessed with keys.</span></span> <span data-ttu-id="a5fe4-113">複数のオブジェクトを返すことが "_できる_" コマンドは配列を返し、"_常に_" 単一オブジェクト "_のみ_" を返すコマンドは辞書を返します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-113">Commands that _could_ return more than one object return an array, and commands that _always_ return _only_ a single object return a dictionary.</span></span>

## <a name="get-properties-in-a-dictionary"></a><span data-ttu-id="a5fe4-114">辞書のプロパティを取得する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-114">Get properties in a dictionary</span></span>

<span data-ttu-id="a5fe4-115">結果として辞書を使用すると、キーだけで最上位からプロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-115">Working with dictionary results, you can access properties from the top level with just the key.</span></span> <span data-ttu-id="a5fe4-116">`.` (__部分式__) 文字は、入れ子になった辞書のプロパティにアクセスする際に使用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-116">The `.` (__subexpression__) character is used to access properties of nested dictionaries.</span></span> <span data-ttu-id="a5fe4-117">クエリを導入する前に、`az vm show` コマンドの未変更の出力を見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-117">Before introducing queries, take a look at the unmodified output of the `az vm show` command:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM -o json
```

<span data-ttu-id="a5fe4-118">このコマンドは辞書を出力します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-118">The command will output a dictionary.</span></span> <span data-ttu-id="a5fe4-119">一部の内容は省略されています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-119">Some content has been omitted.</span></span>

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

<span data-ttu-id="a5fe4-120">次のコマンドでは、クエリを追加して、VM への接続を許可された SSH 公開キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-120">The following command gets the SSH public keys authorized to connect to the VM by adding a query:</span></span>

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

## <a name="get-a-single-value"></a><span data-ttu-id="a5fe4-121">単一の値を取得する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-121">Get a single value</span></span>

<span data-ttu-id="a5fe4-122">一般的なケースとして、Azure リソース ID、リソース名、ユーザー名、パスワードなどの CLI コマンドから "_1 つ_" の値のみを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-122">A common case is that you need to only get _one_ value out of a CLI command, such as an Azure resource ID, a resource name, a username, or a password.</span></span> <span data-ttu-id="a5fe4-123">その場合、ローカルの環境変数に値を格納する必要が発生することも少なくありません。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-123">In that case, you also often want to store the value in a local environment variable.</span></span> <span data-ttu-id="a5fe4-124">1 つのプロパティを取得するには、まず、クエリから 1 つのプロパティのみを取得していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-124">To get a single property, first make sure that you're only getting one property out of the query.</span></span> <span data-ttu-id="a5fe4-125">最後の例を管理者ユーザー名のみを取得するように変更します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-125">Modifying the last example to get only the admin username:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'osProfile.adminUsername' -o json
```

```JSON
"azureuser"
```

<span data-ttu-id="a5fe4-126">これは有効な単一の値のように見えますが、`"` 文字が出力の一部として返されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-126">This looks like a valid single value, but note that the `"` characters are returned as part of the output.</span></span> <span data-ttu-id="a5fe4-127">これは、オブジェクトが JSON 文字列であることを示します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-127">This indicates that the object is a JSON string.</span></span> <span data-ttu-id="a5fe4-128">この値をコマンドからの出力として環境変数に直接割り当てた場合、引用符はシェルによって解釈 "__されない__" ことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-128">It's important to note that when you assign this value directly as output from the command to an environment variable, the quotes may __not__ be interpreted by the shell:</span></span>

```bash
USER=$(az vm show -g QueryDemo -n TestVM --query 'osProfile.adminUsername' -o json)
echo $USER
```

```output
"azureuser"
```

<span data-ttu-id="a5fe4-129">これは、ほぼ間違いなく望ましくない状態です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-129">This is almost certainly not what you want.</span></span> <span data-ttu-id="a5fe4-130">この場合、戻り値を型情報で囲まない出力形式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-130">In this case, you want to use an output format which doesn't enclose returned values with type information.</span></span> <span data-ttu-id="a5fe4-131">この目的のため CLI が提供する最適な出力オプションは `tsv` (タブ区切りの値) です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-131">The best output option that the CLI offers for this purpose is `tsv`, tab-separated values.</span></span> <span data-ttu-id="a5fe4-132">特に、単一値のみの値を取得するとき (ディクショナリまたは一覧ではなく)、`tsv` 出力が引用されることはなくなります。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-132">In particular, when retrieving a value that's only a single value (not a dictionary or list), `tsv` output is guaranteed to be unquoted.</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'osProfile.adminUsername' -o tsv
```

```output
azureuser
```

<span data-ttu-id="a5fe4-133">`tsv` 出力形式について詳しくは、「[Output formats - TSV output format (出力形式 - TSV 出力形式)](format-output-azure-cli.md#tsv-output-format)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-133">For more information about the `tsv` output format, see [Output formats - TSV output format](format-output-azure-cli.md#tsv-output-format)</span></span>

## <a name="get-multiple-values"></a><span data-ttu-id="a5fe4-134">複数の値を取得する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-134">Get multiple values</span></span>

<span data-ttu-id="a5fe4-135">複数のプロパティを取得するには、式をコンマ区切りリストとして角かっこ `[ ]` (__複数選択リスト__) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-135">To get more than one property, put expressions in square brackets  `[ ]` (a __multiselect list__) as a comma-separated list.</span></span> <span data-ttu-id="a5fe4-136">VM 名、管理者ユーザー、SSH キーのすべてを一度に取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-136">To get the VM name, admin user, and SSH key all at once use the command:</span></span>

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

<span data-ttu-id="a5fe4-137">これらの値は、クエリで指定された順序で結果の配列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-137">These values are listed in the result array in the order they were given in the query.</span></span> <span data-ttu-id="a5fe4-138">結果は配列であるため、結果に関連付けられたキーはありません。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-138">Since the result is an array, there are no keys associated with the results.</span></span>

## <a name="rename-properties-in-a-query"></a><span data-ttu-id="a5fe4-139">クエリでプロパティの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-139">Rename properties in a query</span></span>

<span data-ttu-id="a5fe4-140">複数の値のクエリを実行するときに、配列ではなく、辞書を取得するには、`{ }` (__複数選択ハッシュ__) 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-140">To get a dictionary instead of an array when querying for multiple values, use the `{ }` (__multiselect hash__) operator.</span></span>
<span data-ttu-id="a5fe4-141">複数選択ハッシュの形式は、`{displayName:JMESPathExpression, ...}` です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-141">The format for a multiselect hash is `{displayName:JMESPathExpression, ...}`.</span></span>
<span data-ttu-id="a5fe4-142">`displayName` は出力に表示される文字列であり、`JMESPathExpression` は評価する JMESPath 式です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-142">`displayName` will be the string shown in output, and `JMESPathExpression` is the JMESPath expression to evaluate.</span></span> <span data-ttu-id="a5fe4-143">複数選択リストをハッシュに変更して、前のセクションの例を変更します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-143">Modifying the example from the last section by changing the multiselect list to a hash:</span></span>

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

## <a name="get-properties-in-an-array"></a><span data-ttu-id="a5fe4-144">配列内のプロパティを取得する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-144">Get properties in an array</span></span>

<span data-ttu-id="a5fe4-145">配列には独自のプロパティはありませんが、インデックスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-145">An array has no properties of its own, but it can be indexed.</span></span> <span data-ttu-id="a5fe4-146">この機能は、前の例の式 `publicKeys[0]` で示されています。これは、`publicKeys` 配列の最初の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-146">This feature is shown in the last example with the expression `publicKeys[0]`, which gets the first element of the `publicKeys` array.</span></span> <span data-ttu-id="a5fe4-147">CLI の出力が順序付けられているという保証はないため、順序が確かである場合や取得する要素を気にかけない場合を除き、インデックスを使用しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-147">There's no guarantee CLI output is ordered, so avoid using indexing unless you're sure of the order or don't care what element you get.</span></span> <span data-ttu-id="a5fe4-148">配列内の要素のプロパティにアクセスするには、"_フラット化_" と "_フィルター処理_" の 2 つの操作のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-148">To access the properties of elements in an array, you do one of two operations: _flattening_ and _filtering_.</span></span> <span data-ttu-id="a5fe4-149">このセクションでは、配列をフラット化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-149">This section covers how to flatten an array.</span></span>

<span data-ttu-id="a5fe4-150">配列のフラット化は、`[]` JMESPath 演算子を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-150">Flattening an array is done with the `[]` JMESPath operator.</span></span> <span data-ttu-id="a5fe4-151">`[]` 演算子の後のすべての式が、現在の配列内の各要素に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-151">All expressions after the `[]` operator are applied to each element in the current array.</span></span>
<span data-ttu-id="a5fe4-152">`[]` がクエリの先頭にある場合、CLI コマンドの結果がフラット化されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-152">If `[]` appears at the start of the query, it flattens the CLI command result.</span></span> <span data-ttu-id="a5fe4-153">この機能を使用して、`az vm list` の結果を検査できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-153">The results of `az vm list` can be inspected with this feature.</span></span>
<span data-ttu-id="a5fe4-154">リソース グループ内の各 VM の名前、OS、管理者名を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-154">To get the name, OS, and administrator name for each VM in a resource group:</span></span>

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

<span data-ttu-id="a5fe4-155">`--output table` 出力形式と組み合わせた場合、列名は複数選択ハッシュの `displayKey` 値と一致します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-155">When combined with the `--output table` output format, the column names match up with the `displayKey` value of the multiselect hash:</span></span>

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
> <span data-ttu-id="a5fe4-156">特定のキーはフィルター処理され、テーブル ビューには出力されません。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-156">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="a5fe4-157">これらのキーは、`id`、`type`、および`etag` です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-157">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="a5fe4-158">これらの値を表示するには、複数選択ハッシュのキー名を変更します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-158">To see these values, you can change the key name in a multiselect hash.</span></span>
>
> ```azurecli-interactive
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

<span data-ttu-id="a5fe4-159">コマンドから返される最上位の結果だけでなく、配列もフラット化できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-159">Any array can be flattened, not just the top-level result returned by the command.</span></span> <span data-ttu-id="a5fe4-160">前のセクションでは、式 `osProfile.linuxConfiguration.ssh.publicKeys[0].keyData` を使用して、サインイン用の SSH 公開キーを取得しました。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-160">In the last section, the expression `osProfile.linuxConfiguration.ssh.publicKeys[0].keyData` was used to get the SSH public key for sign-in.</span></span> <span data-ttu-id="a5fe4-161">"_すべての_" SSH 公開キーを取得するには、この式を `osProfile.linuxConfiguration.ssh.publicKeys[].keyData` と記述します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-161">To get _every_ SSH public key, the expression could instead be written as `osProfile.linuxConfiguration.ssh.publicKeys[].keyData`.</span></span>
<span data-ttu-id="a5fe4-162">このクエリ式では、`osProfile.linuxConfiguration.ssh.publicKeys` 配列をフラット化し、各要素に対して `keyData` 式を実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-162">This query expression flattens the `osProfile.linuxConfiguration.ssh.publicKeys` array, and then runs the `keyData` expression on each element:</span></span>

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

## <a name="filter-arrays"></a><span data-ttu-id="a5fe4-163">配列をフィルター処理する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-163">Filter arrays</span></span>

<span data-ttu-id="a5fe4-164">配列からデータを取得するときに使用するもう 1 つの操作は "_フィルター処理_" です。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-164">The other operation used to get data from an array is _filtering_.</span></span> <span data-ttu-id="a5fe4-165">フィルター処理は、`[?...]` JMESPath 演算子を使用して実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-165">Filtering is done with the `[?...]` JMESPath operator.</span></span>
<span data-ttu-id="a5fe4-166">この演算子は、その内容として述語を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-166">This operator takes a predicate as its contents.</span></span> <span data-ttu-id="a5fe4-167">述語とは、`true` または `false` に評価できるステートメントです。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-167">A predicate is any statement that can be evaluated to either `true` or `false`.</span></span> <span data-ttu-id="a5fe4-168">述語が `true` に評価された式が出力に含まれます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-168">Expressions where the predicate evaluates to `true` are included in the output.</span></span>

<span data-ttu-id="a5fe4-169">JMESPath では、標準の比較演算子と論理演算子が提供されています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-169">JMESPath offers the standard comparison and logical operators.</span></span> <span data-ttu-id="a5fe4-170">これらには、`<`、`<=`、`>`、`>=`、`==`、`!=` が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-170">These include `<`, `<=`, `>`, `>=`, `==`, and `!=`.</span></span>
<span data-ttu-id="a5fe4-171">JMESPath では、論理 AND (`&&`)、論理 OR (`||`)、論理 NOT (`!`) もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-171">JMESPath also supports logical and (`&&`), or (`||`), and not (`!`).</span></span> <span data-ttu-id="a5fe4-172">式をかっこ内にグループ化できるので、より複雑な述語式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-172">Expressions can be grouped within parenthesis, allowing for more complex predicate expressions.</span></span> <span data-ttu-id="a5fe4-173">述語と論理演算の詳細については、[JMESPath の仕様](http://jmespath.org/specification.html)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-173">For the full details on predicates and logical operations, see the [JMESPath specification](http://jmespath.org/specification.html).</span></span>

<span data-ttu-id="a5fe4-174">前のセクションでは、配列をフラット化して、リソース グループ内のすべての VM の完全なリストを取得しました。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-174">In the last section, we flattened an array to get the complete list of all VMs in a resource group.</span></span> <span data-ttu-id="a5fe4-175">フィルターを使用すると、この出力を Linux VM だけに制限できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-175">Using filters, this output can be restricted to only Linux VMs:</span></span>

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
> <span data-ttu-id="a5fe4-176">JMESPath では、文字列は常に単一引用符 (`'`) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-176">In JMESPath, strings are always surrounded by single quotes (`'`).</span></span> <span data-ttu-id="a5fe4-177">フィルター述語の文字列の一部として二重引用符を使用すると、空の出力が返されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-177">If you use double quotes as part of a string in a filter predicate, you'll get empty output.</span></span>

<span data-ttu-id="a5fe4-178">JMESPath には、フィルター処理に役立つ組み込み関数もあります。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-178">JMESPath also has built-in functions that can help with filtering.</span></span> <span data-ttu-id="a5fe4-179">このような関数の 1 つである `contains(string, substring)` は、文字列に部分文字列が含まれているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-179">One such function is `contains(string, substring)`, which checks to see if a string contains a substring.</span></span> <span data-ttu-id="a5fe4-180">この関数を呼び出す前に式が評価されるので、最初の引数には完全な JMESPath 式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-180">Expressions are evaluated before calling the function, so the first argument can be a full JMESPath expression.</span></span> <span data-ttu-id="a5fe4-181">次の例では、OS ディスクに SSD ストレージを使用するすべての VM を検出します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-181">The next example finds all VMs using SSD storage for their OS disk:</span></span>

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

<span data-ttu-id="a5fe4-182">このクエリは少し長くなっています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-182">This query is a little long.</span></span> <span data-ttu-id="a5fe4-183">`storageProfile.osDisk.managedDisk.storageAccountType` キーが 2 回記述され、出力でキー更新されています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-183">The `storageProfile.osDisk.managedDisk.storageAccountType` key is mentioned twice, and rekeyed in the output.</span></span> <span data-ttu-id="a5fe4-184">これを短くする 1 つの方法として、データをフラット化して選択した後にフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-184">One way to shorten it is to apply the filter after flattening and selecting data.</span></span>

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

<span data-ttu-id="a5fe4-185">大きな配列では、データを選択する前にフィルターを適用する方が速い場合があります。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-185">For large arrays, it may be faster to apply the filter before selecting data.</span></span>

<span data-ttu-id="a5fe4-186">関数の全一覧については、[JMESPath の仕様の組み込み関数](http://jmespath.org/specification.html#built-in-functions)に関するセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-186">See the [JMESPath specification - Built-in Functions](http://jmespath.org/specification.html#built-in-functions) for the full list of functions.</span></span>

## <a name="change-output"></a><span data-ttu-id="a5fe4-187">出力を変更する</span><span class="sxs-lookup"><span data-stu-id="a5fe4-187">Change output</span></span>

<span data-ttu-id="a5fe4-188">JMESPath の関数には別の目的もあります。それは、クエリの結果を操作することです。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-188">JMESPath functions also have another purpose, which is to operate on the results of a query.</span></span> <span data-ttu-id="a5fe4-189">ブール値以外の値を返す関数では、式の結果が変更されます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-189">Any function that returns a non-boolean value changes the result of an expression.</span></span>
<span data-ttu-id="a5fe4-190">たとえば、`sort_by(array, &sort_expression)` を使用して、データをプロパティ値で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-190">For example, you can sort data by a property value with `sort_by(array, &sort_expression)`.</span></span> <span data-ttu-id="a5fe4-191">JMESPath では、関数の一部として後で評価する必要がある式に、特殊演算子の `&` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-191">JMESPath uses a special operator, `&`, for expressions that should be evaluated later as part of a function.</span></span> <span data-ttu-id="a5fe4-192">次の例は、VM のリストを OS ディスク サイズで並べ替える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-192">The next example shows how to sort a VM list by OS disk size:</span></span>

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

<span data-ttu-id="a5fe4-193">関数の全一覧については、[JMESPath の仕様の組み込み関数](http://jmespath.org/specification.html#built-in-functions)に関するセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-193">See the [JMESPath specification - Built-in Functions](http://jmespath.org/specification.html#built-in-functions) for the full list of functions.</span></span>

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="a5fe4-194">対話形式でのクエリの実験</span><span class="sxs-lookup"><span data-stu-id="a5fe4-194">Experiment with queries interactively</span></span>

<span data-ttu-id="a5fe4-195">JMESPath で実験を開始できるように、[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python パッケージには、クエリを操作するための対話型環境が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-195">To start experimenting with JMESPath, the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package offers an interactive environment to work with queries.</span></span> <span data-ttu-id="a5fe4-196">データを入力としてパイプ処理してから、クエリを記述し、エディターで実行します。</span><span class="sxs-lookup"><span data-stu-id="a5fe4-196">Data is piped as input, and then queries are written and run in the editor.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
