---
title: Azure CLI 2.0 対話モード
description: 対話モードで Azure CLI 2.0 を使用します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: f07689a323314c076f1eb2a8844875d9543d4b2e
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388577"
---
# <a name="interactive-azure-cli-20"></a><span data-ttu-id="4d444-103">対話型 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="4d444-103">Interactive Azure CLI 2.0</span></span>

<span data-ttu-id="4d444-104">Azure CLI 2.0 を対話モードで使用するには、`az interactive` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4d444-104">You can use Azure CLI 2.0 in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="4d444-105">このモードにより対話型シェルに移動することで、オートコンプリート、コマンドの説明、および例にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="4d444-105">This mode places you in an interactive shell with auto-completion, command descriptions, and examples.</span></span>

![対話モード](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="4d444-107">黒の背景でも読みやすさは変わらないため、ここでは既定のスタイルを使用していません。</span><span class="sxs-lookup"><span data-stu-id="4d444-107">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="4d444-108">まだアカウントにサインインしていない場合は、`login` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-108">If you're not already signed in to your account, use the `login` command.</span></span>

## <a name="configure"></a><span data-ttu-id="4d444-109">構成</span><span class="sxs-lookup"><span data-stu-id="4d444-109">Configure</span></span>

<span data-ttu-id="4d444-110">対話モードでは、必要に応じて、コマンドの説明、パラメーターの説明、およびコマンドの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d444-110">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="4d444-111">説明と例のオン/オフを切り替えるには、`F1` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-111">Turn descriptions and examples on or off using `F1`.</span></span>

![説明と例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="4d444-113">パラメーターの既定値の表示のオン/オフを切り替えるには、`F2` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-113">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![既定値](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="4d444-115">`F3` では、一部のキー ジェスチャの表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="4d444-115">`F3` toggles the display of some key gestures.</span></span>

![ジェスチャ](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="4d444-117">Scope (スコープ)</span><span class="sxs-lookup"><span data-stu-id="4d444-117">Scope</span></span>

<span data-ttu-id="4d444-118">対話モードのスコープを、`vm`、`vm image` などの特定のコマンド グループに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4d444-118">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="4d444-119">これを行うと、すべてのコマンドがそのスコープ内で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="4d444-119">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="4d444-120">そのコマンド グループですべての作業を行う場合は、これを使って簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="4d444-120">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="4d444-121">次のコマンドを入力する代わりに、</span><span class="sxs-lookup"><span data-stu-id="4d444-121">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="4d444-122">次のように、vm コマンド グループにスコープを指定して、対象のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="4d444-122">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="4d444-123">下位レベルのコマンド グループにもスコープを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4d444-123">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="4d444-124">`vm image` にスコープを指定するには、`%%vm image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-124">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="4d444-125">この場合、既に `vm` にスコープを指定しているため、`%%image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-125">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="4d444-126">この時点で、`%%..` を使用すると、スコープを `vm` に戻すことができます。また、`%%` だけを指定すると、スコープをルートに指定できます。</span><span class="sxs-lookup"><span data-stu-id="4d444-126">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="4d444-127">クエリ</span><span class="sxs-lookup"><span data-stu-id="4d444-127">Query</span></span>

<span data-ttu-id="4d444-128">最後に実行したコマンドの結果に対して、JMESPath クエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4d444-128">You can execute a JMESPath query on the results of the last command that you executed.</span></span>
<span data-ttu-id="4d444-129">たとえば、VM を作成した後、その VM が完全にプロビジョニングされていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="4d444-129">For example, after you create a VM, you can make sure it has fully provisioned.</span></span>

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```output
[
  "Creating"
]
```

<span data-ttu-id="4d444-130">コマンドの結果に対してクエリを実行する方法の詳細については、[Azure 2.0 でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4d444-130">To learn more about querying the results of your commands, see [Query command results with Azure 2.0](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="4d444-131">Bash コマンド</span><span class="sxs-lookup"><span data-stu-id="4d444-131">Bash commands</span></span>

<span data-ttu-id="4d444-132">`#[cmd]` を使用して、対話モードのままシェル コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4d444-132">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="4d444-133">例</span><span class="sxs-lookup"><span data-stu-id="4d444-133">Examples</span></span>

<span data-ttu-id="4d444-134">一部のコマンドには例が多数あります。</span><span class="sxs-lookup"><span data-stu-id="4d444-134">Some commands have lots of examples.</span></span>
<span data-ttu-id="4d444-135">次の例のページにスクロールするには、`CTRL-N` を使用します。前のページに戻るには、`CTRL-Y` を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d444-135">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="4d444-137">`::#` を使用して、特定の例を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="4d444-137">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
