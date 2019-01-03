---
title: Azure CLI 対話モード
description: 対話モードで Azure CLI を使用します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 7a6b89953d60fe98910f8141a606ac1fcba318ae
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593440"
---
# <a name="azure-cli-interactive-mode"></a><span data-ttu-id="a6b87-103">Azure CLI 対話モード</span><span class="sxs-lookup"><span data-stu-id="a6b87-103">Azure CLI interactive mode</span></span>

<span data-ttu-id="a6b87-104">Azure CLI を対話モードで使用するには、`az interactive` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-104">You can use Azure CLI in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="a6b87-105">このモードにより対話型シェルに移動することで、オートコンプリート、コマンドの説明、および例にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="a6b87-105">This mode places you in an interactive shell with auto-completion, command descriptions, and examples.</span></span>

![対話モード](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="a6b87-107">黒の背景でも読みやすさは変わらないため、ここでは既定のスタイルを使用していません。</span><span class="sxs-lookup"><span data-stu-id="a6b87-107">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="a6b87-108">まだアカウントにサインインしていない場合は、`login` コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-108">If you're not already signed in to your account, use the `login` command.</span></span>

## <a name="configure"></a><span data-ttu-id="a6b87-109">構成</span><span class="sxs-lookup"><span data-stu-id="a6b87-109">Configure</span></span>

<span data-ttu-id="a6b87-110">対話モードでは、必要に応じて、コマンドの説明、パラメーターの説明、およびコマンドの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-110">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="a6b87-111">説明と例のオン/オフを切り替えるには、`F1` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-111">Turn descriptions and examples on or off using `F1`.</span></span>

![説明と例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="a6b87-113">パラメーターの既定値の表示のオン/オフを切り替えるには、`F2` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-113">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![既定値](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="a6b87-115">`F3` では、一部のキー ジェスチャの表示を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-115">`F3` toggles the display of some key gestures.</span></span>

![ジェスチャ](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="a6b87-117">Scope (スコープ)</span><span class="sxs-lookup"><span data-stu-id="a6b87-117">Scope</span></span>

<span data-ttu-id="a6b87-118">対話モードのスコープを、`vm`、`vm image` などの特定のコマンド グループに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-118">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="a6b87-119">これを行うと、すべてのコマンドがそのスコープ内で解釈されます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-119">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="a6b87-120">そのコマンド グループですべての作業を行う場合は、これを使って簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-120">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="a6b87-121">次のコマンドを入力する代わりに、</span><span class="sxs-lookup"><span data-stu-id="a6b87-121">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="a6b87-122">次のように、vm コマンド グループにスコープを指定して、対象のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-122">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="a6b87-123">下位レベルのコマンド グループにもスコープを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-123">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="a6b87-124">`vm image` にスコープを指定するには、`%%vm image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-124">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="a6b87-125">この場合、既に `vm` にスコープを指定しているため、`%%image` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-125">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="a6b87-126">この時点で、`%%..` を使用すると、スコープを `vm` に戻すことができます。また、`%%` だけを指定すると、スコープをルートに指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-126">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="a6b87-127">クエリ</span><span class="sxs-lookup"><span data-stu-id="a6b87-127">Query</span></span>

<span data-ttu-id="a6b87-128">最後に実行したコマンドの結果に対して、JMESPath クエリを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-128">You can execute a JMESPath query on the results of the last command that you executed.</span></span>
<span data-ttu-id="a6b87-129">たとえば、VM を作成した後、その VM が完全にプロビジョニングされていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-129">For example, after you create a VM, you can make sure it has fully provisioned.</span></span>

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait -o json
az>> ? [*].provisioningState
```

```json
[
  "Creating"
]
```

<span data-ttu-id="a6b87-130">コマンドの結果に対してクエリを実行する方法の詳細については、[Azure CLI でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a6b87-130">To learn more about querying the results of your commands, see [Query command results with the Azure CLI](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="a6b87-131">Bash コマンド</span><span class="sxs-lookup"><span data-stu-id="a6b87-131">Bash commands</span></span>

<span data-ttu-id="a6b87-132">`#[cmd]` を使用して、対話モードのままシェル コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-132">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="a6b87-133">例</span><span class="sxs-lookup"><span data-stu-id="a6b87-133">Examples</span></span>

<span data-ttu-id="a6b87-134">一部のコマンドには例が多数あります。</span><span class="sxs-lookup"><span data-stu-id="a6b87-134">Some commands have lots of examples.</span></span>
<span data-ttu-id="a6b87-135">次の例のページにスクロールするには、`CTRL-N` を使用します。前のページに戻るには、`CTRL-Y` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6b87-135">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="a6b87-137">`::#` を使用して、特定の例を確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6b87-137">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
