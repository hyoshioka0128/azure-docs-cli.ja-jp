---
title: "Azure CLI 2.0 対話モード"
description: "対話モードで Azure CLI 2.0 を使用します。"
keywords: "Azure CLI 2.0, 対話モード"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 
ms.openlocfilehash: fb260d7385728acd0c699488ecb5b108afefd08c
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2018
---
# <a name="interactive-azure-cli-20"></a><span data-ttu-id="7adaa-104">対話型 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="7adaa-104">Interactive Azure CLI 2.0</span></span>

<span data-ttu-id="7adaa-105">Azure CLI 2.0 を対話モードで使用するには、`az interactive` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-105">You can use Azure CLI 2.0 in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="7adaa-106">これにより対話型シェルに移動します。このシェルでは、コマンドがオートコンプリート入力されるほか、コマンドやそのパラメーターの説明、およびコマンドの例にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-106">That places you in an interactive shell where your commands are auto-completed and you have access to descriptions of commands and their parameters and command examples.</span></span>

![対話モード](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="7adaa-108">黒の背景でも読みやすさは変わらないため、ここでは既定のスタイルを使用していません。</span><span class="sxs-lookup"><span data-stu-id="7adaa-108">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="7adaa-109">まだアカウントにログインしていない場合は、`login` コマンドを使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="7adaa-109">If you're not already logged in to your account, use the `login` command to do that.</span></span>

## <a name="configure"></a><span data-ttu-id="7adaa-110">構成</span><span class="sxs-lookup"><span data-stu-id="7adaa-110">Configure</span></span>

<span data-ttu-id="7adaa-111">対話モードでは、必要に応じて、コマンドの説明、パラメーターの説明、およびコマンドの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-111">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="7adaa-112">説明と例のオン/オフを切り替えるには、`F1` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-112">You can turn descriptions and examples on or off using `F1`.</span></span>

![説明と例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="7adaa-114">パラメーターの既定値の表示のオン/オフを切り替えるには、`F2` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-114">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![既定値](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="7adaa-116">`F3` では、一部のキー ジェスチャの表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-116">`F3` toggles the display of some key gestures.</span></span>

![ジェスチャ](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="7adaa-118">Scope (スコープ)</span><span class="sxs-lookup"><span data-stu-id="7adaa-118">Scope</span></span>

<span data-ttu-id="7adaa-119">対話モードのスコープを、`vm`、`vm image` などの特定のコマンド グループに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-119">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="7adaa-120">これを行うと、すべてのコマンドがそのスコープ内で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-120">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="7adaa-121">そのコマンド グループですべての作業を行う場合は、これを使って簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-121">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="7adaa-122">次のコマンドを入力する代わりに、</span><span class="sxs-lookup"><span data-stu-id="7adaa-122">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="7adaa-123">次のように、vm コマンド グループにスコープを指定して、対象のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-123">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="7adaa-124">下位レベルのコマンド グループにもスコープを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-124">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="7adaa-125">`vm image` にスコープを指定するには、`%%vm image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-125">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="7adaa-126">この場合、既に `vm` にスコープを指定しているため、`%%image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-126">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="7adaa-127">この時点で、`%%..` を使用すると、スコープを `vm` に戻すことができます。また、`%%` だけを指定すると、スコープをルートに指定できます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-127">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="7adaa-128">クエリ</span><span class="sxs-lookup"><span data-stu-id="7adaa-128">Query</span></span>

<span data-ttu-id="7adaa-129">最後に実行したコマンドの結果に対して、JMESPath クエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-129">You can execute a JMESPath query on the results of the last command that you executed.</span></span>
<span data-ttu-id="7adaa-130">たとえば、VM を作成した後、その VM が完全にプロビジョニングされていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-130">For example, after you create a VM, you can make sure it has fully provisioned.</span></span>

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

<span data-ttu-id="7adaa-131">コマンドの結果に対してクエリを実行する方法の詳細については、[Azure 2.0 でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7adaa-131">To learn more about querying the results of your commands, see [Query command results with Azure 2.0](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="7adaa-132">Bash コマンド</span><span class="sxs-lookup"><span data-stu-id="7adaa-132">Bash commands</span></span>

<span data-ttu-id="7adaa-133">`#[cmd]` を使用して、対話モードのままシェル コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-133">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="7adaa-134">例</span><span class="sxs-lookup"><span data-stu-id="7adaa-134">Examples</span></span>

<span data-ttu-id="7adaa-135">一部のコマンドには例が多数あります。</span><span class="sxs-lookup"><span data-stu-id="7adaa-135">Some commands have lots of examples.</span></span>
<span data-ttu-id="7adaa-136">次の例のページにスクロールするには、`CTRL-N` を使用します。前のページに戻るには、`CTRL-Y` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7adaa-136">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="7adaa-138">`::#` を使用して、特定の例を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="7adaa-138">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
