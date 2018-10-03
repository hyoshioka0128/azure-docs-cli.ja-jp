---
title: Azure CLI の概要
description: コマンドの基本を学習し、Azure CLI を使い始めます。
keywords: Azure CLI, CLI ヘルプ, Azure ヘルプ, クエリ, 自動化,
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: d23548a9cdfe307c2597d992dc014125f80704d0
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177999"
---
# <a name="get-started-with-azure-cli"></a><span data-ttu-id="98c96-104">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="98c96-104">Get started with Azure CLI</span></span>

<span data-ttu-id="98c96-105">Azure CLI へようこそ。</span><span class="sxs-lookup"><span data-stu-id="98c96-105">Welcome to the Azure CLI!</span></span> <span data-ttu-id="98c96-106">CLI は、Azure サービスを迅速かつ効率的に使用するためのツールで、オートメーションに重点が置されています。</span><span class="sxs-lookup"><span data-stu-id="98c96-106">The CLI is a tool designed to get you working quickly and efficiently with Azure services, with an emphasis on automation.</span></span> <span data-ttu-id="98c96-107">この記事では、CLI の機能と、生産性の向上に役立つリソースへのリンクを紹介します。</span><span class="sxs-lookup"><span data-stu-id="98c96-107">This article introduces features of the CLI and links out to resources that help you be productive.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="98c96-108">Azure Cloud Shell でのインストールまたは実行</span><span class="sxs-lookup"><span data-stu-id="98c96-108">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="98c96-109">Azure CLI で作業を開始するには、お使いのブラウザーから Azure Cloud Shell 環境で実行するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="98c96-109">The easiest way to get started with the Azure CLI is by running it in an Azure Cloud Shell environment through your browser.</span></span> <span data-ttu-id="98c96-110">Cloud Shell については、「[Azure Cloud Shell の Bash のクイックスタート](/azure/cloud-shell/quickstart)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98c96-110">To learn about Cloud Shell, see  [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

<span data-ttu-id="98c96-111">CLI をインストールする準備ができたら、[インストール手順](install-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98c96-111">When you're ready to install the CLI, see the [installation instructions](install-azure-cli.md).</span></span>

## <a name="sign-in"></a><span data-ttu-id="98c96-112">[サインイン]</span><span class="sxs-lookup"><span data-stu-id="98c96-112">Sign in</span></span>

<span data-ttu-id="98c96-113">ローカル インストールで CLI コマンドを使用する前に、[az login](/cli/azure/reference-index#az-login) でサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98c96-113">Before using any CLI commands with a local install, you need to sign in with [az login](/cli/azure/reference-index#az-login).</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="98c96-114">対話型以外のサインイン方法も用意されています。詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98c96-114">There are ways to sign in non-interactively, which are covered in detail in [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="common-commands"></a><span data-ttu-id="98c96-115">一般的なコマンド</span><span class="sxs-lookup"><span data-stu-id="98c96-115">Common commands</span></span>

<span data-ttu-id="98c96-116">次の表は、CLI で使用される一般的なコマンドの一部を示しており、リファレンス ドキュメントにリンクされています。</span><span class="sxs-lookup"><span data-stu-id="98c96-116">This table lists some common commands used in the CLI and links to their reference documentation.</span></span>

| <span data-ttu-id="98c96-117">リソースの種類</span><span class="sxs-lookup"><span data-stu-id="98c96-117">Resource type</span></span> | <span data-ttu-id="98c96-118">Azure CLI コマンド グループ</span><span class="sxs-lookup"><span data-stu-id="98c96-118">Azure CLI command group</span></span> |
|---------------|-------------------------|
| [<span data-ttu-id="98c96-119">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="98c96-119">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="98c96-120">az group</span><span class="sxs-lookup"><span data-stu-id="98c96-120">az group</span></span>](/cli/azure/group) |
| [<span data-ttu-id="98c96-121">仮想マシン</span><span class="sxs-lookup"><span data-stu-id="98c96-121">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="98c96-122">az vm</span><span class="sxs-lookup"><span data-stu-id="98c96-122">az vm</span></span>](/cli/azure/vm) |
| [<span data-ttu-id="98c96-123">ストレージ アカウント</span><span class="sxs-lookup"><span data-stu-id="98c96-123">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="98c96-124">az storage account</span><span class="sxs-lookup"><span data-stu-id="98c96-124">az storage account</span></span>](/cli/azure/storage/account) |
| [<span data-ttu-id="98c96-125">Key Vault</span><span class="sxs-lookup"><span data-stu-id="98c96-125">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="98c96-126">az keyvault</span><span class="sxs-lookup"><span data-stu-id="98c96-126">az keyvault</span></span>](/cli/azure/keyvault) |
| [<span data-ttu-id="98c96-127">Web アプリケーション</span><span class="sxs-lookup"><span data-stu-id="98c96-127">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="98c96-128">az webapp</span><span class="sxs-lookup"><span data-stu-id="98c96-128">az webapp</span></span>](/cli/azure/webapp) |
| [<span data-ttu-id="98c96-129">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="98c96-129">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="98c96-130">az sql server</span><span class="sxs-lookup"><span data-stu-id="98c96-130">az sql server</span></span>](/cli/azure/sql/server) |
| [<span data-ttu-id="98c96-131">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="98c96-131">CosmosDB</span></span>](/azure/cosmos-db) | [<span data-ttu-id="98c96-132">az cosmosdb</span><span class="sxs-lookup"><span data-stu-id="98c96-132">az cosmosdb</span></span>](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a><span data-ttu-id="98c96-133">コマンドを見つける</span><span class="sxs-lookup"><span data-stu-id="98c96-133">Finding commands</span></span>

<span data-ttu-id="98c96-134">CLI のコマンドは、"_グループ_" の "_サブコマンド_" として整理されています。</span><span class="sxs-lookup"><span data-stu-id="98c96-134">Commands in the CLI are organized as _commands_ of _groups_.</span></span> <span data-ttu-id="98c96-135">各グループは、Azure のサービスを表し、コマンドはそのサービスに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="98c96-135">Each group represents an Azure service, and commands operate on that service.</span></span>

<span data-ttu-id="98c96-136">コマンドを検索するには、[az find](/cli/azure/reference-index#az-find) を使用します。</span><span class="sxs-lookup"><span data-stu-id="98c96-136">To search for commands, use [az find](/cli/azure/reference-index#az-find).</span></span> <span data-ttu-id="98c96-137">たとえば、`secret` を含むコマンド名を検索するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="98c96-137">For example, to search for command names containing `secret`, use the following command:</span></span>

```azurecli-interactive
az find -q secret
```

<span data-ttu-id="98c96-138">コマンドと、グループのサブグループの完全な一覧を取得するには、`--help` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="98c96-138">Use the `--help` argument to get a complete list of commands and subgroups of a group.</span></span> <span data-ttu-id="98c96-139">たとえば、ネットワーク セキュリティ グループ (NSG) で使用する CLI コマンドを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="98c96-139">For example, to find the CLI commands for working with Network Security Groups (NSGs):</span></span>

```azurecli-interactive
az network nsg --help
```

<span data-ttu-id="98c96-140">CLI では Bash シェルにコマンドの完全タブ補完が用意されています。</span><span class="sxs-lookup"><span data-stu-id="98c96-140">The CLI has full tab completion for commands under the bash shell.</span></span>

## <a name="globally-available-arguments"></a><span data-ttu-id="98c96-141">グローバルに使用できる引数</span><span class="sxs-lookup"><span data-stu-id="98c96-141">Globally available arguments</span></span>

<span data-ttu-id="98c96-142">引数の中には、すべてのコマンドで使用できるものがあります。</span><span class="sxs-lookup"><span data-stu-id="98c96-142">There are some arguments that are available for every command.</span></span>

* <span data-ttu-id="98c96-143">`--help` は、コマンドとその引数に関する CLI 参照情報を出力し、利用可能なサブグループとコマンドの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="98c96-143">`--help` prints CLI reference information about commands and their arguments and lists available subgroups and commands.</span></span>
* <span data-ttu-id="98c96-144">`--output` は出力形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="98c96-144">`--output` changes the output format.</span></span> <span data-ttu-id="98c96-145">使用可能な出力形式は `json`、`jsonc` (色付けされた JSON)、`tsv` (タブ区切り値)、および `table` (人間が判読できる ASCII テーブル) です。</span><span class="sxs-lookup"><span data-stu-id="98c96-145">The available output formats are `json`, `jsonc` (colorized JSON), `tsv` (Tab-Separated Values), and `table` (human-readable ASCII tables).</span></span> <span data-ttu-id="98c96-146">既定では、CLI は `json` を出力します。</span><span class="sxs-lookup"><span data-stu-id="98c96-146">By default the CLI outputs `json`.</span></span> <span data-ttu-id="98c96-147">使用可能な出力形式の詳細については、[Azure CLI の出力形式](format-output-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98c96-147">To learn more about the available output formats, see [Output formats for Azure CLI](format-output-azure-cli.md).</span></span>
* <span data-ttu-id="98c96-148">`--query` は、[JMESPath クエリ言語](http://jmespath.org/)を使用して、Azure サービスから返された出力をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="98c96-148">`--query` uses the [JMESPath query language](http://jmespath.org/) to filter the output returned from Azure services.</span></span> <span data-ttu-id="98c96-149">クエリの詳細については、[Azure CLI でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページ、および「[JMESPath tutorial (JMESPath チュートリアル)](http://jmespath.org/tutorial.html)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98c96-149">To learn To learn more about queries, see [Query command results with Azure CLI](query-azure-cli.md) and the [JMESPath tutorial](http://jmespath.org/tutorial.html).</span></span>
* <span data-ttu-id="98c96-150">`--verbose` は、操作中に Azure で作成されたリソースに関する情報と、その他の有用な情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="98c96-150">`--verbose` prints information about resources created in Azure during an operation, and other useful information.</span></span>
* <span data-ttu-id="98c96-151">`--debug` は、デバッグの目的で使用する、CLI 操作に関する詳細情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="98c96-151">`--debug` prints even more information about CLI operations, used for debugging purposes.</span></span> <span data-ttu-id="98c96-152">バグを見つけた場合は、バグ レポートを送信するときに、`--debug` フラグをオンにして生成した出力を提供してください。</span><span class="sxs-lookup"><span data-stu-id="98c96-152">If you find a bug, provide output generated with the `--debug` flag on when submitting a bug report.</span></span>

## <a name="interactive-mode"></a><span data-ttu-id="98c96-153">対話モード</span><span class="sxs-lookup"><span data-stu-id="98c96-153">Interactive mode</span></span>

<span data-ttu-id="98c96-154">CLI には対話モードが用意されています。このモードでは、ヘルプ情報が自動的に表示され、サブコマンドが選択しやすくなっています。</span><span class="sxs-lookup"><span data-stu-id="98c96-154">The CLI offers an interactive mode that automatically displays help information and makes it easier to select subcommands.</span></span> <span data-ttu-id="98c96-155">対話モードには [az interactive](/cli/azure/reference-index#az-interactive) コマンドで切り替えます。</span><span class="sxs-lookup"><span data-stu-id="98c96-155">You enter interactive mode with the [az interactive](/cli/azure/reference-index#az-interactive) command.</span></span>

```azurecli-interactive
az interactive
```

<span data-ttu-id="98c96-156">対話モードの詳細については、[Azure CLI 対話モード](interactive-azure-cli.md)に関する記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98c96-156">For more information on interactive mode, see [Azure CLI Interactive Mode](interactive-azure-cli.md).</span></span>

<span data-ttu-id="98c96-157">また、オートコンプリート、マウス オーバー ドキュメントなど、対話型エクスペリエンスを提供する [Visual Studio Code プラグイン](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="98c96-157">There's also a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) that offers an interactive experience, including autocomplete and mouse-over documentation.</span></span>

## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="98c96-158">クイックスタートとチュートリアルを利用して CLI の基本について学習する</span><span class="sxs-lookup"><span data-stu-id="98c96-158">Learn CLI basics with quickstarts and tutorials</span></span>

<span data-ttu-id="98c96-159">Azure CLI の使用を開始するには、詳細なチュートリアルをお試しください。チュートリアルでは、仮想マシンを設定し、CLI の機能を使用して Azure リソースにクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="98c96-159">To get you started with the Azure CLI, try an in-depth tutorial for setting up virtual machines and using the power of the CLI to query Azure resources.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="98c96-160">Azure CLI での仮想マシンの作成チュートリアル</span><span class="sxs-lookup"><span data-stu-id="98c96-160">Create virtual machines with the Azure CLI tutorial</span></span>](azure-cli-vm-tutorial.yml)

<span data-ttu-id="98c96-161">その他の人気のあるサービス用のクイック スタートもあります。</span><span class="sxs-lookup"><span data-stu-id="98c96-161">There are also quickstarts for other popular services.</span></span>

* [<span data-ttu-id="98c96-162">Azure CLI を使用したストレージ アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="98c96-162">Create a storage account using the Azure CLI</span></span>](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [<span data-ttu-id="98c96-163">CLI を使用した Azure Blob Storage との間でのオブジェクトの転送</span><span class="sxs-lookup"><span data-stu-id="98c96-163">Transfer objects to/from Azure Blob storage using the CLI</span></span>](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [<span data-ttu-id="98c96-164">Azure CLI を使用した単一の Azure SQL データベースの作成</span><span class="sxs-lookup"><span data-stu-id="98c96-164">Create a single Azure SQL database using the Azure CLI</span></span>](/azure/sql-database/sql-database-get-started-cli)
* [<span data-ttu-id="98c96-165">Azure CLI を使用した Azure Database for MySQL サーバーの作成</span><span class="sxs-lookup"><span data-stu-id="98c96-165">Create an Azure Database for MySQL server using the Azure CLI</span></span>](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [<span data-ttu-id="98c96-166">Azure CLI を使用した Azure Database for PostgreSQL の作成</span><span class="sxs-lookup"><span data-stu-id="98c96-166">Create an Azure Database for PostgreSQL using the Azure CLI</span></span>](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [<span data-ttu-id="98c96-167">Azure での Python Web アプリの作成</span><span class="sxs-lookup"><span data-stu-id="98c96-167">Create a Python web app in Azure</span></span>](/azure/app-service/app-service-web-get-started-python)
* [<span data-ttu-id="98c96-168">Azure Web Apps for Containers でのカスタム Docker Hub イメージの実行</span><span class="sxs-lookup"><span data-stu-id="98c96-168">Run a custom Docker Hub image in Azure Web Apps for Containers</span></span>](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a><span data-ttu-id="98c96-169">フィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="98c96-169">Give feedback</span></span>

<span data-ttu-id="98c96-170">機能強化とバグ解決に活かすために、CLI に関する皆様のご意見をお待ちしております。</span><span class="sxs-lookup"><span data-stu-id="98c96-170">We welcome your feedback for the CLI to help us make improvements and resolve bugs.</span></span> <span data-ttu-id="98c96-171">[GitHub で問題を報告](https://github.com/azure/azure-cli/issues)するか、CLI の組み込み機能を使用して、[az feedback](/cli/azure/reference-index#az-feedback) コマンドで一般的なフィードバックをお寄せください。</span><span class="sxs-lookup"><span data-stu-id="98c96-171">You can [file an issue on Github](https://github.com/azure/azure-cli/issues) or use the built-in features of the CLI to leave general feedback with the [az feedback](/cli/azure/reference-index#az-feedback) command.</span></span>

```azurecli-interactive
az feedback
```
