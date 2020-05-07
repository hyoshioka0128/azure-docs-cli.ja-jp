---
title: Azure CLI 対話モード
description: 対話モードで Azure CLI を使用します。
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 09/09/2018
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 7b3ee1e284e7f771c661bb65bf8b8ab53dafd77f
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "77779518"
---
# <a name="azure-cli-interactive-mode"></a><span data-ttu-id="94636-103">Azure CLI 対話モード</span><span class="sxs-lookup"><span data-stu-id="94636-103">Azure CLI interactive mode</span></span>

<span data-ttu-id="94636-104">Azure CLI を対話モードで使用するには、`az interactive` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="94636-104">You can use Azure CLI in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="94636-105">このモードにより対話型シェルに移動することで、オートコンプリート、コマンドの説明、および例にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="94636-105">This mode places you in an interactive shell with auto-completion, command descriptions, and examples.</span></span>

![対話モード](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="94636-107">黒の背景でも読みやすさは変わらないため、ここでは既定のスタイルを使用していません。</span><span class="sxs-lookup"><span data-stu-id="94636-107">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="94636-108">まだアカウントにサインインしていない場合は、`login` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-108">If you're not already signed in to your account, use the `login` command.</span></span>

## <a name="configure"></a><span data-ttu-id="94636-109">[構成]</span><span class="sxs-lookup"><span data-stu-id="94636-109">Configure</span></span>

<span data-ttu-id="94636-110">対話モードでは、必要に応じて、コマンドの説明、パラメーターの説明、およびコマンドの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="94636-110">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="94636-111">説明と例のオン/オフを切り替えるには、`F1` を使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-111">Turn descriptions and examples on or off using `F1`.</span></span>

![説明と例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="94636-113">パラメーターの既定値の表示のオン/オフを切り替えるには、`F2` を使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-113">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![既定値](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="94636-115">`F3` では、一部のキー ジェスチャの表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="94636-115">`F3` toggles the display of some key gestures.</span></span>

![ジェスチャ](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="94636-117">スコープ</span><span class="sxs-lookup"><span data-stu-id="94636-117">Scope</span></span>

<span data-ttu-id="94636-118">対話モードのスコープを、`vm`、`vm image` などの特定のコマンド グループに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="94636-118">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="94636-119">これを行うと、すべてのコマンドがそのスコープ内で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="94636-119">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="94636-120">そのコマンド グループですべての作業を行う場合は、これを使って簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="94636-120">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="94636-121">次のコマンドを入力する代わりに、</span><span class="sxs-lookup"><span data-stu-id="94636-121">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="94636-122">次のように、vm コマンド グループにスコープを指定して、対象のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="94636-122">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="94636-123">下位レベルのコマンド グループにもスコープを指定できます。</span><span class="sxs-lookup"><span data-stu-id="94636-123">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="94636-124">`vm image` にスコープを指定するには、`%%vm image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-124">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="94636-125">この場合、既に `vm` にスコープを指定しているため、`%%image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-125">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="94636-126">この時点で、`vm` を使用すると、スコープを `%%..` に戻すことができます。また、`%%` だけを指定すると、スコープをルートに指定できます。</span><span class="sxs-lookup"><span data-stu-id="94636-126">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="94636-127">クエリ</span><span class="sxs-lookup"><span data-stu-id="94636-127">Query</span></span>

<span data-ttu-id="94636-128">`??` と、その後に JMESPath クエリを指定して、最後に実行したコマンドの結果に対して、JMESPath クエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="94636-128">You can execute a JMESPath query on the results of the last command that you executed by using `??`followed by a JMESPath query.</span></span>
<span data-ttu-id="94636-129">たとえば、グループの作成後に、その新しいグループの ID を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="94636-129">For example, after you created a group, you can retrieve the id of the new group.</span></span>

```azurecli
az>> group create -n myRG -l westEurope
az>> "?? id"
```

<span data-ttu-id="94636-130">この構文では前に実行したコマンドの結果を引数として使用することもできます。\* たとえば、すべてのグループを一覧表示した後に、最初のグループ内で西ヨーロッパにある `virtualMachine` の種類のリソースをすべて一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="94636-130">You can also use this syntax to use the result of the previous command as an argument for your next command.\* For instance after having listed all groups, list all the resources of type `virtualMachine`on the first group whose location is westeurope.</span></span> 

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait -o json
az>> group list -o json
az>> resource list -g "?? [?location=='westeurope'].name | [0]" --query "[?type=='Microsoft.Compute/virtualMachines'].name
```

<span data-ttu-id="94636-131">コマンドの結果に対してクエリを実行する方法の詳細については、[Azure CLI でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="94636-131">To learn more about querying the results of your commands, see [Query command results with the Azure CLI](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="94636-132">Bash コマンド</span><span class="sxs-lookup"><span data-stu-id="94636-132">Bash commands</span></span>

<span data-ttu-id="94636-133">`#[cmd]` を使用して、対話モードのままシェル コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="94636-133">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="94636-134">例</span><span class="sxs-lookup"><span data-stu-id="94636-134">Examples</span></span>

<span data-ttu-id="94636-135">一部のコマンドには例が多数あります。</span><span class="sxs-lookup"><span data-stu-id="94636-135">Some commands have lots of examples.</span></span>
<span data-ttu-id="94636-136">次の例のページにスクロールするには、`CTRL-N` を使用します。前のページに戻るには、`CTRL-Y` を使用します。</span><span class="sxs-lookup"><span data-stu-id="94636-136">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![使用例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="94636-138">`::#` を使用して、特定の例を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="94636-138">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
