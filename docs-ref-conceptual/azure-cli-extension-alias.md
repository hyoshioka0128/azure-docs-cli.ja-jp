---
title: Azure CLI 2.0 のエイリアス拡張機能
description: Azure CLI 2.0 のエイリアス拡張機能を使用する方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 39996693d6b796c2d9a45cd909121829f00291a8
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2018
ms.locfileid: "34306269"
---
# <a name="the-azure-cli-20-alias-extension"></a><span data-ttu-id="fc00b-103">Azure CLI 2.0 のエイリアス拡張機能</span><span class="sxs-lookup"><span data-stu-id="fc00b-103">The Azure CLI 2.0 alias extension</span></span>

<span data-ttu-id="fc00b-104">エイリアス拡張機能を使用すると、既存のコマンドを使用して、Azure CLI のカスタム コマンドを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-104">The alias extension allows users to define custom commands for the Azure CLI by using existing commands.</span></span> <span data-ttu-id="fc00b-105">エイリアスを使用すると、ショートカットが許可され、位置引数を使用する機能が提供されるため、ワークフローを簡潔でシンプルに保つことができます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-105">Aliases help keep your workflow concise and simple by allowing shortcuts and giving you the ability to use positional arguments.</span></span> <span data-ttu-id="fc00b-106">エイリアスには Jinja2 テンプレート エンジンが使用されているため、高度な引数の処理にも対応できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-106">Since aliases are powered by the Jinja2 template engine, they even offer advanced argument processing.</span></span>

> [!NOTE]
> <span data-ttu-id="fc00b-107">エイリアス拡張機能はパブリック プレビュー段階にあります。</span><span class="sxs-lookup"><span data-stu-id="fc00b-107">The Alias Extension is in public preview.</span></span> <span data-ttu-id="fc00b-108">機能と構成ファイルの形式は変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc00b-108">The features and configuration file format may change.</span></span>

## <a name="install-the-alias-extension"></a><span data-ttu-id="fc00b-109">エイリアス拡張機能のインストール</span><span class="sxs-lookup"><span data-stu-id="fc00b-109">Install the alias extension</span></span>

<span data-ttu-id="fc00b-110">エイリアス拡張機能を使用するために最低限必要な Azure CLI バージョンは **2.0.28** です。</span><span class="sxs-lookup"><span data-stu-id="fc00b-110">The minimum required Azure CLI version to use the alias extension is **2.0.28**.</span></span> <span data-ttu-id="fc00b-111">CLI のバージョンを確認するには、`az --version` を実行してください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-111">To check your CLI version, run `az --version`.</span></span> <span data-ttu-id="fc00b-112">インストールを更新する必要がある場合は、「[Azure CLI 2.0 のインストール](./install-azure-cli.md)」の説明に従ってください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-112">If you need to update your installation,  follow the instructions in [Install the Azure CLI 2.0](./install-azure-cli.md).</span></span>

<span data-ttu-id="fc00b-113">[az extension add](/cli/azure/extension#az-extension-add) コマンドを使用して拡張機能をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fc00b-113">Install the extension with the [az extension add](/cli/azure/extension#az-extension-add) command.</span></span>

```azurecli-interactive
az extension add --name alias
```

<span data-ttu-id="fc00b-114">[az extension list](/cli/azure/extension#az-extension-list) を使用して拡張機能のインストールを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc00b-114">Verify the installation of the extension with [az extension list](/cli/azure/extension#az-extension-list).</span></span> <span data-ttu-id="fc00b-115">エイリアス拡張機能が正しくインストールされていれば、コマンドの出力に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-115">If the alias extension was installed properly, it's listed in the command output.</span></span>

```azurecli-interactive
az extension list --output table --query '[].{Name:name}'
```

```output
Name
------
alias
```

## <a name="keep-the-extension-up-to-date"></a><span data-ttu-id="fc00b-116">拡張機能を最新の状態に保つ</span><span class="sxs-lookup"><span data-stu-id="fc00b-116">Keep the extension up to date</span></span>

<span data-ttu-id="fc00b-117">エイリアス拡張機能は活発に開発が行われており、新しいバージョンが定期的にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-117">The alias extension is under active development and new versions are released regularly.</span></span> <span data-ttu-id="fc00b-118">CLI を更新したときに、新しいバージョンが自動的にインストールされるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="fc00b-118">New versions are not automatically installed whenever you update the CLI.</span></span> <span data-ttu-id="fc00b-119">[az extension update](/cli/azure/extension#az-extension-update) を使用して拡張機能の更新プログラムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fc00b-119">Install the updates for the extension with [az extension update](/cli/azure/extension#az-extension-update).</span></span>

```azurecli-interactive
az extension update --name alias
```

## <a name="manage-aliases-for-the-azure-cli"></a><span data-ttu-id="fc00b-120">Azure CLI のエイリアスを管理する</span><span class="sxs-lookup"><span data-stu-id="fc00b-120">Manage aliases for the Azure CLI</span></span>

<span data-ttu-id="fc00b-121">エイリアスの拡張機能により、便利で使い慣れたエイリアス管理コマンドを利用できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-121">The alias extension provides convenient and familiar commands to manage aliases.</span></span> <span data-ttu-id="fc00b-122">使用可能なすべてのコマンドおよびパラメーターの詳細を表示するには、`--help` でエイリアス コマンドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fc00b-122">To view all the available commands and parameter details, invoke the alias command with `--help`.</span></span>

```azurecli-interactive
az alias --help
```

## <a name="create-simple-alias-commands"></a><span data-ttu-id="fc00b-123">単純なエイリアス コマンドを作成する</span><span class="sxs-lookup"><span data-stu-id="fc00b-123">Create simple alias commands</span></span>

<span data-ttu-id="fc00b-124">エイリアスの用途の 1 つは、既存のコマンド グループやコマンド名の短縮です。</span><span class="sxs-lookup"><span data-stu-id="fc00b-124">One use of aliases is for shortening existing command groups or command names.</span></span> <span data-ttu-id="fc00b-125">たとえば、`group` コマンド グループを `rg` に、`list` コマンドを `ls` に短縮できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-125">For example, you can shorten the `group` command group to `rg` and the `list` command to `ls`.</span></span>

```azurecli-interactive
az alias create --name rg --command group
az alias create --name ls --command list
```

<span data-ttu-id="fc00b-126">新しく定義したこれらのエイリアスは、定義が存在する任意の場所で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fc00b-126">These newly defined aliases can now be used anywhere that their definition would be.</span></span>

```azurecli-interactive
az rg list
az rg ls
az vm ls
```

<span data-ttu-id="fc00b-127">コマンドの一部として `az` を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-127">Do not include `az` as part of the command.</span></span>

<span data-ttu-id="fc00b-128">エイリアスは、完全なコマンドのショートカットにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-128">Aliases can also be shortcuts for complete commands.</span></span> <span data-ttu-id="fc00b-129">次の例では、使用可能なリソース グループとその位置がテーブル出力で表示されています。</span><span class="sxs-lookup"><span data-stu-id="fc00b-129">The next example lists available resource groups and their locations in table output:</span></span>

```azurecli-interactive
az alias create --name ls-groups --command "group list --query '[].{Name:name, Location:location}' --output table"
```

<span data-ttu-id="fc00b-130">これで `ls-groups` を他の CLI コマンドのように実行できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-130">Now `ls-groups` can be run like any other CLI command.</span></span>

```azurecli-interactive
az ls-groups
```

## <a name="create-an-alias-command-with-arguments"></a><span data-ttu-id="fc00b-131">引数付きのエイリアス コマンドを作成する</span><span class="sxs-lookup"><span data-stu-id="fc00b-131">Create an alias command with arguments</span></span>

<span data-ttu-id="fc00b-132">エイリアス名に `{{ arg_name }}` として含めることで、位置引数をエイリアス コマンドに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-132">You can also add positional arguments to an alias command by including them as `{{ arg_name }}` in the alias name.</span></span> <span data-ttu-id="fc00b-133">中かっこ内には空白が必要です。</span><span class="sxs-lookup"><span data-stu-id="fc00b-133">The whitespace inside the braces is required.</span></span>

```azurecli-interactive
az alias create --name "alias_name {{ arg1 }} {{ arg2 }} ..." --command "invoke_including_args"
```

<span data-ttu-id="fc00b-134">次の例のエイリアスは、位置引数を使用して VM のパブリック IP アドレスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fc00b-134">The next example alias shows how to use positional arguments to get the public IP address for a VM.</span></span>

```azurecli-interactive
az alias create \
    --name "get-vm-ip {{ resourceGroup }} {{ vmName }}" \
    --command "vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }}
        --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress"
```

<span data-ttu-id="fc00b-135">このコマンドを実行するときに、位置引数に値を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc00b-135">When running this command, you give values to the positional arguments.</span></span>

```azurecli-interactive
az get-vm-ip MyResourceGroup MyVM
```

<span data-ttu-id="fc00b-136">エイリアスによって呼び出したコマンドで環境変数を使用することもできます。この環境変数は実行時に評価されます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-136">You can also use environment variables in commands invoked by aliases, which are evaluated at runtime.</span></span> <span data-ttu-id="fc00b-137">次の例では、`create-rg` エイリアスを追加します。これにより、`eastus` 内にリソース グループが作成され、`owner` タグが追加されます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-137">The next example adds the `create-rg` alias, which creates a resource group in `eastus` and adds an `owner` tag.</span></span> <span data-ttu-id="fc00b-138">このタグには、ローカル環境変数 `USER` の値が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-138">This tag is assigned the value of the local environment variable `USER`.</span></span>

```azurecli-interactive
az alias create \
    --name "create-rg {{ groupName }}" \
    --command "group create --name {{ groupName }} --location eastus --tags owner=\$USER"
```

<span data-ttu-id="fc00b-139">エイリアスのコマンド内に環境変数を登録するには、ドル記号 `$` をエスケープする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc00b-139">To register the environment variables inside the command of the alias, the dollar sign `$` must be escaped.</span></span>

## <a name="process-arguments-using-jinja2-templates"></a><span data-ttu-id="fc00b-140">Jinja2 テンプレートを使用した引数の処理</span><span class="sxs-lookup"><span data-stu-id="fc00b-140">Process arguments using Jinja2 templates</span></span>

<span data-ttu-id="fc00b-141">エイリアス拡張機能での引数の置換は、[Jinja2](http://jinja.pocoo.org/docs/2.10/) によって実行されるため、ユーザーは Jinja2 テンプレート エンジンの機能にフル アクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="fc00b-141">Argument substitution in the alias extension is performed by [Jinja2](http://jinja.pocoo.org/docs/2.10/), giving you full access to the capabilities of the Jinja2 template engine.</span></span> <span data-ttu-id="fc00b-142">テンプレートを使用すると、文字列上のデータの抽出や置換などのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-142">Templates allow you to perform actions like data extraction and substitution on strings.</span></span>

<span data-ttu-id="fc00b-143">Jinja2 テンプレートにより、基になるコマンドとは異なるさまざまな種類の引数を受け入れるエイリアスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-143">With Jinja2 templates, you can write aliases which take different types of arguments than the underlying command.</span></span> <span data-ttu-id="fc00b-144">たとえば、ストレージ URL を受け入れるエイリアスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-144">For example, you can make an alias which takes a storage URL.</span></span> <span data-ttu-id="fc00b-145">この URL が解析され、アカウント名とコンテナー名がストレージ コマンドに渡されます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-145">Then this URL is parsed to pass the account and container names to the storage command.</span></span>

```azurecli-interactive
az alias create \
    --name 'storage-ls {{ url }}' \
    --command "storage blob list
        --account-name {{ url.replace('https://', '').split('.')[0] }}
        --container-name {{ url.replace('https://', '').split('/')[1] }}"
```

<span data-ttu-id="fc00b-146">Jinja2 テンプレート エンジンについては、[Jinja2 のドキュメント](http://jinja.pocoo.org/docs/2.10/templates/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-146">To learn about the Jinja2 template engine, see [the Jinja2 documentation](http://jinja.pocoo.org/docs/2.10/templates/).</span></span>

## <a name="alias-configuration-file"></a><span data-ttu-id="fc00b-147">エイリアス構成ファイル</span><span class="sxs-lookup"><span data-stu-id="fc00b-147">Alias configuration file</span></span>

<span data-ttu-id="fc00b-148">エイリアス構成ファイルを変更することで、エイリアスを作成および変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-148">Another way to create and modify aliases is to alter the alias configuration file.</span></span> <span data-ttu-id="fc00b-149">エイリアス コマンド定義は、`$AZURE_USER_CONFIG/alias` にある構成ファイルに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-149">Alias command definitions are written into a configuration file, located at `$AZURE_USER_CONFIG/alias`.</span></span> <span data-ttu-id="fc00b-150">`AZURE_USER_CONFIG` の既定値は、macOS と Linux の場合は `$HOME/.azure`、Windows の場合は `%USERPROFILE%\.azure` です。</span><span class="sxs-lookup"><span data-stu-id="fc00b-150">The default value of `AZURE_USER_CONFIG` is `$HOME/.azure` on macOS and Linux, and `%USERPROFILE%\.azure` on Windows.</span></span> <span data-ttu-id="fc00b-151">エイリアス構成ファイルは、INI 構成ファイル形式で記述されます。</span><span class="sxs-lookup"><span data-stu-id="fc00b-151">The alias configuration file is written in the INI configuration file format.</span></span> <span data-ttu-id="fc00b-152">エイリアス コマンドの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc00b-152">The format for alias commands is:</span></span>

```ini
[alias_name]
command = invoked_commands
```

<span data-ttu-id="fc00b-153">位置引数を含むエイリアスの場合、エイリアス コマンドの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc00b-153">For aliases that contain positional arguments, the format for alias commands is:</span></span>

```ini
[alias_name {{ arg1 }} {{ arg2 }} ...]
command = invoked_commands_including_args
```

## <a name="create-an-alias-command-with-arguments-via-the-alias-configuration-file"></a><span data-ttu-id="fc00b-154">エイリアス構成ファイルで引数付きのエイリアス コマンドを作成する</span><span class="sxs-lookup"><span data-stu-id="fc00b-154">Create an alias command with arguments via the alias configuration file</span></span>

<span data-ttu-id="fc00b-155">引数付きのサンプル エイリアス コマンドを含むエイリアス構成ファイルを次に示します。これは、VM のパブリック IP アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="fc00b-155">Below is an alias configuration file that contains an example alias command with arguments, which gets the public IP address for a VM.</span></span> <span data-ttu-id="fc00b-156">呼び出されたコマンドが単一行であることと、エイリアスで定義された引数が含まれることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-156">Ensure that the invoked command is in a single line, and contains the same arguments defined in the alias.</span></span>

```ini
[get-vm-ip {{ resourceGroup }} {{ vmName }}]
command = vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }} --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress
```

## <a name="uninstall-the-alias-extension"></a><span data-ttu-id="fc00b-157">エイリアス拡張機能のアンインストール</span><span class="sxs-lookup"><span data-stu-id="fc00b-157">Uninstall the alias extension</span></span>

<span data-ttu-id="fc00b-158">拡張機能をアンインストールするには、[az extension remove](/cli/azure/extension#az-extension-remove) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc00b-158">To uninstall the extension, use the [az extension remove](/cli/azure/extension#az-extension-remove) command.</span></span>

```azurecli-interactive
az extension remove --name alias
```

<span data-ttu-id="fc00b-159">拡張機能に関するバグなどの問題が原因でアンインストールした場合は、Microsoft が修正プログラムを提供できるように、[GitHub に問題を提出](https://github.com/Azure/azure-cli-extensions/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="fc00b-159">If you uninstalled due to a bug or other problem with the extension, please [file a GitHub issue](https://github.com/Azure/azure-cli-extensions/issues) so that we can provide a fix.</span></span>
