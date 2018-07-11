---
title: Azure CLI 2.0 を使ってみる
description: コマンドの基本を学習し、Azure CLI 2.0 を使い始めます。
keywords: Azure CLI, CLI ヘルプ, Azure ヘルプ, クエリ, 自動化,
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: c973d31312fbe0f9232bf3f0f3ed5f3b70b6559a
ms.sourcegitcommit: 308f9eb433a05b814999ac404f63d181169fffeb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439943"
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="5a133-104">Azure CLI 2.0 を使ってみる</span><span class="sxs-lookup"><span data-stu-id="5a133-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="5a133-105">Azure CLI 2.0 へようこそ。</span><span class="sxs-lookup"><span data-stu-id="5a133-105">Welcome to the Azure CLI 2.0!</span></span> <span data-ttu-id="5a133-106">CLI は、Azure サービスを迅速かつ効率的に使用するためのツールで、オートメーションに重点が置されています。</span><span class="sxs-lookup"><span data-stu-id="5a133-106">The CLI is a tool designed to get you working quickly and efficiently with Azure services, with an emphasis on automation.</span></span> <span data-ttu-id="5a133-107">この記事では、CLI の機能と、生産性の向上に役立つリソースへのリンクを紹介します。</span><span class="sxs-lookup"><span data-stu-id="5a133-107">This article introduces features of the CLI and links out to resources that help you be productive.</span></span>

## <a name="install-and-sign-in"></a><span data-ttu-id="5a133-108">インストールとサインイン</span><span class="sxs-lookup"><span data-stu-id="5a133-108">Install and sign in</span></span>

<span data-ttu-id="5a133-109">[CLI をインストール](install-azure-cli.md)するか、[Azure Cloud Shell](/azure/cloud-shell/overview) を試します (まだこの操作を行っていない場合)。</span><span class="sxs-lookup"><span data-stu-id="5a133-109">If you haven't already, [install the CLI](install-azure-cli.md) or try out the [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>

<span data-ttu-id="5a133-110">ローカル インストールで CLI コマンドを使用する前に、[az login](/cli/azure/reference-index#az-login) でサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a133-110">Before using any CLI commands with a local install, you need to sign in with [az login](/cli/azure/reference-index#az-login).</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="5a133-111">対話型以外のサインイン方法も用意されています。詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a133-111">There are ways to sign in non-interactively, which are covered in detail in [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="common-commands"></a><span data-ttu-id="5a133-112">一般的なコマンド</span><span class="sxs-lookup"><span data-stu-id="5a133-112">Common commands</span></span>

<span data-ttu-id="5a133-113">次の表は、CLI で使用される一般的なコマンドをいくつか示しており、それぞれが、リファレンス内の関連ドキュメント ページにリンクされています。</span><span class="sxs-lookup"><span data-stu-id="5a133-113">This table lists a few of the common commands used in the CLI links out to their documentation pages in the reference.</span></span>
<span data-ttu-id="5a133-114">こうしたグループのすべてのサブコマンドおよびそのドキュメントは、オンライン リファレンスまたは `--help` 引数を使用して確認できます。</span><span class="sxs-lookup"><span data-stu-id="5a133-114">All subcommands of these groups and their documentation can be looked up in online reference or with the `--help` argument.</span></span>

| <span data-ttu-id="5a133-115">リソースの種類</span><span class="sxs-lookup"><span data-stu-id="5a133-115">Resource type</span></span> | <span data-ttu-id="5a133-116">Azure CLI コマンド グループ</span><span class="sxs-lookup"><span data-stu-id="5a133-116">Azure CLI command group</span></span> |
|---------------|-------------------------|
| <span data-ttu-id="5a133-117">[[リソース グループ]](/azure/azure-resource-manager/resource-group-overview)</span><span class="sxs-lookup"><span data-stu-id="5a133-117">[Resource group](/azure/azure-resource-manager/resource-group-overview)</span></span> | [<span data-ttu-id="5a133-118">az group</span><span class="sxs-lookup"><span data-stu-id="5a133-118">az group</span></span>](/cli/azure/group) |
| [<span data-ttu-id="5a133-119">仮想マシン</span><span class="sxs-lookup"><span data-stu-id="5a133-119">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="5a133-120">az vm</span><span class="sxs-lookup"><span data-stu-id="5a133-120">az vm</span></span>](/cli/azure/vm) |
| [<span data-ttu-id="5a133-121">ストレージ アカウント</span><span class="sxs-lookup"><span data-stu-id="5a133-121">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="5a133-122">az storage account</span><span class="sxs-lookup"><span data-stu-id="5a133-122">az storage account</span></span>](/cli/azure/storage/account) |
| [<span data-ttu-id="5a133-123">Key Vault</span><span class="sxs-lookup"><span data-stu-id="5a133-123">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="5a133-124">az keyvault</span><span class="sxs-lookup"><span data-stu-id="5a133-124">az keyvault</span></span>](/cli/azure/keyvault) |
| [<span data-ttu-id="5a133-125">Web アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5a133-125">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="5a133-126">az webapp</span><span class="sxs-lookup"><span data-stu-id="5a133-126">az webapp</span></span>](/cli/azure/webapp) |
| [<span data-ttu-id="5a133-127">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="5a133-127">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="5a133-128">az sql server</span><span class="sxs-lookup"><span data-stu-id="5a133-128">az sql server</span></span>](/cli/azure/sql/server) |
| [<span data-ttu-id="5a133-129">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5a133-129">CosmosDB</span></span>](/azure/cosmos-db) | [<span data-ttu-id="5a133-130">az cosmosdb</span><span class="sxs-lookup"><span data-stu-id="5a133-130">az cosmosdb</span></span>](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a><span data-ttu-id="5a133-131">コマンドを見つける</span><span class="sxs-lookup"><span data-stu-id="5a133-131">Finding commands</span></span>

<span data-ttu-id="5a133-132">CLI のコマンドは、"_グループ_" の "_サブコマンド_" として提供されます。</span><span class="sxs-lookup"><span data-stu-id="5a133-132">Commands in the CLI are provided as _subcommands_ of _groups_.</span></span>
<span data-ttu-id="5a133-133">各グループが、Azure によって提供されるサービスを表しており、サブグループによって、そのサービスのコマンドが論理グループに分かれています。</span><span class="sxs-lookup"><span data-stu-id="5a133-133">Each group represents a service provided by Azure, and the subgroups divide commands for these services into logical groupings.</span></span>

<span data-ttu-id="5a133-134">コマンドを検索するには、[az find](/cli/azure/reference-index#az-find) を使用します。</span><span class="sxs-lookup"><span data-stu-id="5a133-134">To search for commands, use [az find](/cli/azure/reference-index#az-find).</span></span> <span data-ttu-id="5a133-135">たとえば、`secret` を含むコマンド名を検索するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a133-135">For example, to search for command names containing `secret`, use the following command:</span></span>

```azurecli-interactive
az find -q secret
```

<span data-ttu-id="5a133-136">使用するコマンドのグループがわかっている場合は、`--help` 引数の方が適していることがあります。</span><span class="sxs-lookup"><span data-stu-id="5a133-136">If you know which group of commands you want to work with, the `--help` argument may be a better choice.</span></span> <span data-ttu-id="5a133-137">これにより、コマンドの詳細情報が表示されます。また、コマンド グループで使用すると、利用可能なすべてのサブコマンドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a133-137">This displays not just detailed information for a command, but when used with a command group, displays all of the available subcommands.</span></span> <span data-ttu-id="5a133-138">たとえば、ネットワーク セキュリティ グループ (NSG) で使用すると、利用可能な NSG サブグループとコマンドを確認できます。</span><span class="sxs-lookup"><span data-stu-id="5a133-138">For example, when working with Network Security Groups (NSGs) you can find the available NSG subgroups and commands.</span></span>

```azurecli-interactive
az network nsg --help
```

<span data-ttu-id="5a133-139">CLI では Bash シェルにコマンドの完全タブ補完が用意されています。</span><span class="sxs-lookup"><span data-stu-id="5a133-139">The CLI has full tab completion for commands under the bash shell.</span></span>

## <a name="globally-available-arguments"></a><span data-ttu-id="5a133-140">グローバルに使用できる引数</span><span class="sxs-lookup"><span data-stu-id="5a133-140">Globally available arguments</span></span>

<span data-ttu-id="5a133-141">引数の中には、すべてのコマンドで使用できるものがあります。</span><span class="sxs-lookup"><span data-stu-id="5a133-141">There are some arguments that are available for every command.</span></span>

* <span data-ttu-id="5a133-142">`--help` は、コマンドとその引数に関する CLI 参照情報を出力し、利用可能なサブグループとコマンドの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="5a133-142">`--help` prints CLI reference information about commands and their arguments and lists available subgroups and commands.</span></span>
* <span data-ttu-id="5a133-143">`--output` は出力形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="5a133-143">`--output` changes the output format.</span></span> <span data-ttu-id="5a133-144">使用可能な出力形式は `json`、`jsonc` (色付けされた JSON)、`tsv` (タブ区切り値)、および `table` (人間が判読できる ASCII テーブル) です。</span><span class="sxs-lookup"><span data-stu-id="5a133-144">The available output formats are `json`, `jsonc` (colorized JSON), `tsv` (Tab-Separated Values), and `table` (human-readable ASCII tables).</span></span> <span data-ttu-id="5a133-145">既定では、CLI は `json` を出力します。</span><span class="sxs-lookup"><span data-stu-id="5a133-145">By default the CLI outputs `json`.</span></span> <span data-ttu-id="5a133-146">使用可能な出力形式の詳細については、[Azure CLI 2.0 の出力形式](format-output-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5a133-146">To learn more about the available output formats, see [Output formats for Azure CLI 2.0](format-output-azure-cli.md).</span></span>
* <span data-ttu-id="5a133-147">`--query` は、[JMESPath クエリ言語](http://jmespath.org/)を使用して、Azure サービスから返された出力をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5a133-147">`--query` uses the [JMESPath query language](http://jmespath.org/) to filter the output returned from Azure services.</span></span> <span data-ttu-id="5a133-148">クエリの詳細については、[Azure CLI 2.0 でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページ、および「[JMESPath tutorial (JMESPath チュートリアル)](http://jmespath.org/tutorial.html)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a133-148">To learn To learn more about queries, see [Query command results with Azure CLI 2.0](query-azure-cli.md) and the [JMESPath tutorial](http://jmespath.org/tutorial.html).</span></span>
* <span data-ttu-id="5a133-149">`--verbose` は、操作中に Azure で作成されたリソースに関する情報と、その他の有用な情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="5a133-149">`--verbose` prints information about resources created in Azure during an operation, and other useful information.</span></span>
* <span data-ttu-id="5a133-150">`--debug` は、デバッグの目的で使用する、CLI 操作に関する詳細情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="5a133-150">`--debug` prints even more information about CLI operations, used for debugging purposes.</span></span> <span data-ttu-id="5a133-151">バグが発生した場合は、バグ レポートを送信するときに、`--debug` フラグをオンにして生成した出力を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a133-151">If you encounter a bug, provide output generated with the `--debug` flag on when submitting a bug report.</span></span>


## <a name="interactive-mode"></a><span data-ttu-id="5a133-152">対話モード</span><span class="sxs-lookup"><span data-stu-id="5a133-152">Interactive mode</span></span>

<span data-ttu-id="5a133-153">CLI には対話モードが用意されています。このモードでは、ヘルプ情報が自動的に表示され、サブコマンドが選択しやすくなっています。</span><span class="sxs-lookup"><span data-stu-id="5a133-153">The CLI offers an interactive mode that automatically displays help information and makes it easier to select subcommands.</span></span> <span data-ttu-id="5a133-154">対話モードには [az interactive](/cli/azure/reference-index#az-interactive) コマンドで切り替えます。</span><span class="sxs-lookup"><span data-stu-id="5a133-154">You enter interactive mode with the [az interactive](/cli/azure/reference-index#az-interactive) command.</span></span>

```azurecli-interactive
az interactive
```

<span data-ttu-id="5a133-155">対話モードの詳細については、[Azure CLI 2.0 対話モード](interactive-azure-cli.md)に関する記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5a133-155">For more information on interactive mode, see [Azure CLI 2.0 Interactive Mode](interactive-azure-cli.md).</span></span>

<span data-ttu-id="5a133-156">また、オートコンプリート、マウス オーバー ドキュメントなど、対話型エクスペリエンスを提供する [Visual Studio Code プラグイン](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="5a133-156">There is also a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) that offers an interactive experience, including autocomplete and mouse-over documentation.</span></span>

## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="5a133-157">クイックスタートとチュートリアルを利用して CLI の基本について学習する</span><span class="sxs-lookup"><span data-stu-id="5a133-157">Learn CLI basics with quickstarts and tutorials</span></span>

<span data-ttu-id="5a133-158">Azure CLI 2.0 の使用を開始するには、詳細なチュートリアルをお試しください。チュートリアルでは、仮想マシンを設定し、CLI の機能を使用して Azure リソースにクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a133-158">To get you started with the Azure CLI 2.0, try an in-depth tutorial for setting up virtual machines and using the power of the CLI to query Azure resources.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="5a133-159">Azure CLI 2.0 での仮想マシンの作成チュートリアル</span><span class="sxs-lookup"><span data-stu-id="5a133-159">Create virtual machines with the Azure CLI 2.0 tutorial</span></span>](azure-cli-vm-tutorial.yml)

<span data-ttu-id="5a133-160">他のサービスに焦点を当てる必要がある場合、CLI を使用する Azure サービスについては、さまざまなクイックスタートがあります。</span><span class="sxs-lookup"><span data-stu-id="5a133-160">If you would rather focus on other services, there are a variety of quickstarts for Azure services that use the CLI.</span></span>

* [<span data-ttu-id="5a133-161">Azure CLI を使用したストレージ アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="5a133-161">Create a storage account using the Azure CLI</span></span>](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [<span data-ttu-id="5a133-162">CLI を使用した Azure Blob Storage との間でのオブジェクトの転送</span><span class="sxs-lookup"><span data-stu-id="5a133-162">Transfer objects to/from Azure Blob storage using the CLI</span></span>](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [<span data-ttu-id="5a133-163">Azure CLI を使用した単一の Azure SQL データベースの作成</span><span class="sxs-lookup"><span data-stu-id="5a133-163">Create a single Azure SQL database using the Azure CLI</span></span>](/azure/sql-database/sql-database-get-started-cli)
* [<span data-ttu-id="5a133-164">Azure CLI を使用した Azure Database for MySQL サーバーの作成</span><span class="sxs-lookup"><span data-stu-id="5a133-164">Create an Azure Database for MySQL server using the Azure CLI</span></span>](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [<span data-ttu-id="5a133-165">Azure CLI を使用した Azure Database for PostgreSQL の作成</span><span class="sxs-lookup"><span data-stu-id="5a133-165">Create an Azure Database for PostgreSQL using the Azure CLI</span></span>](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [<span data-ttu-id="5a133-166">Azure での Python Web アプリの作成</span><span class="sxs-lookup"><span data-stu-id="5a133-166">Create a Python web app in Azure</span></span>](/azure/app-service/app-service-web-get-started-python)
* [<span data-ttu-id="5a133-167">Azure Web Apps for Containers でのカスタム Docker Hub イメージの実行</span><span class="sxs-lookup"><span data-stu-id="5a133-167">Run a custom Docker Hub image in Azure Web Apps for Containers</span></span>](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a><span data-ttu-id="5a133-168">フィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="5a133-168">Give feedback</span></span>

<span data-ttu-id="5a133-169">機能強化とバグ解決に活かすために、CLI に関する皆様のご意見をお待ちしております。</span><span class="sxs-lookup"><span data-stu-id="5a133-169">We welcome your feedback for the CLI to help us make improvements and resolve bugs.</span></span> <span data-ttu-id="5a133-170">[GitHub で問題を報告](https://github.com/azure/azure-cli/issues)するか、CLI の組み込み機能を使用して、[az feedback](/cli/azure/reference-index#az-feedback) コマンドで一般的なフィードバックをお寄せください。</span><span class="sxs-lookup"><span data-stu-id="5a133-170">You can [file an issue on Github](https://github.com/azure/azure-cli/issues) or use the built-in features of the CLI to leave general feedback with the [az feedback](/cli/azure/reference-index#az-feedback) command.</span></span>

```azurecli-interactive
az feedback
```
