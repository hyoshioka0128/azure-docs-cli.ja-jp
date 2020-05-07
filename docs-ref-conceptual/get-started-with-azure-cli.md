---
title: Azure CLI の概要
description: コマンドの基本を学習し、Azure CLI を使い始めます。
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 01/30/2020
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: bc9b86db6fb9c5b3731550df9dda96debcbfba9f
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "79990114"
---
# <a name="get-started-with-azure-cli"></a><span data-ttu-id="befa5-103">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="befa5-103">Get started with Azure CLI</span></span>

<span data-ttu-id="befa5-104">Azure CLI へようこそ。</span><span class="sxs-lookup"><span data-stu-id="befa5-104">Welcome to the Azure CLI!</span></span>  <span data-ttu-id="befa5-105">この記事では、CLI について説明し、一般的なタスクの実行に役立つ情報を示します。</span><span class="sxs-lookup"><span data-stu-id="befa5-105">This article introduces the CLI and helps you complete common tasks.</span></span>

> [!NOTE]
>
> <span data-ttu-id="befa5-106">スクリプトおよび Microsoft ドキュメント サイトでは、Azure CLI の例は `bash` シェル向けに記述されています。</span><span class="sxs-lookup"><span data-stu-id="befa5-106">In scripts and on the Microsoft documentation site, Azure CLI examples are written for the `bash` shell.</span></span> <span data-ttu-id="befa5-107">1 行の例であれば任意のプラットフォームで実行できます。</span><span class="sxs-lookup"><span data-stu-id="befa5-107">One-line examples will run on any platform.</span></span> <span data-ttu-id="befa5-108">行継続 (`\`) または変数の代入を含む、より長い例は、PowerShell などの他のシェルで動作するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="befa5-108">Longer examples which include line continuations (`\`) or variable assignment need to be modified to work on other shells, including PowerShell.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="befa5-109">Azure Cloud Shell でのインストールまたは実行</span><span class="sxs-lookup"><span data-stu-id="befa5-109">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="befa5-110">Azure CLI で作業を開始するには、お使いのブラウザーから Azure Cloud Shell 環境で実行するのが最も簡単です。</span><span class="sxs-lookup"><span data-stu-id="befa5-110">The easiest way to get started with the Azure CLI is by running it in an Azure Cloud Shell environment through your browser.</span></span> <span data-ttu-id="befa5-111">Cloud Shell については、「[Azure Cloud Shell の Bash のクイックスタート](/azure/cloud-shell/quickstart)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-111">To learn about Cloud Shell, see  [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

<span data-ttu-id="befa5-112">CLI をインストールする準備ができたら、[インストール手順](install-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="befa5-112">When you're ready to install the CLI, see the [installation instructions](install-azure-cli.md).</span></span>

<span data-ttu-id="befa5-113">初めて CLI をインストールしたら、`az --version` を実行して、CLI の正しいバージョンがインストールされていること確認します。</span><span class="sxs-lookup"><span data-stu-id="befa5-113">After installing the CLI for the first time, check that it's installed and you've got the correct version by running `az --version`.</span></span>

> [!NOTE]
> <span data-ttu-id="befa5-114">Azure クラシック デプロイ モデルを使用している場合は、[Azure クラシック CLI をインストール](install-classic-cli.md)してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-114">If you're using the Azure classic deployment model, [install the Azure classic CLI](install-classic-cli.md).</span></span>

## <a name="sign-in"></a><span data-ttu-id="befa5-115">サインイン</span><span class="sxs-lookup"><span data-stu-id="befa5-115">Sign in</span></span>

<span data-ttu-id="befa5-116">ローカル インストールで CLI コマンドを使用する前に、[az login](/cli/azure/reference-index#az-login) でサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="befa5-116">Before using any CLI commands with a local install, you need to sign in with [az login](/cli/azure/reference-index#az-login).</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="befa5-117">ログインすると、ご使用のアカウントに関連付けられているサブスクリプションの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="befa5-117">After logging in, you see a list of subscriptions associated with your Azure account.</span></span> <span data-ttu-id="befa5-118">`isDefault: true` が示されているサブスクリプション情報が、ログイン後に、現在アクティブになっているサブスクリプションです。</span><span class="sxs-lookup"><span data-stu-id="befa5-118">The subscription information with `isDefault: true` is the currently activated subscription after logging in.</span></span> <span data-ttu-id="befa5-119">別のサブスクリプションを選択するには、切り替え先のサブスクリプション ID を指定して [az account set](/cli/azure/account#az-account-set) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="befa5-119">To select another subscription, use the [az account set](/cli/azure/account#az-account-set) command with the subscription ID to switch to.</span></span> <span data-ttu-id="befa5-120">サブスクリプションの選択の詳細については、「[複数の Azure サブスクリプションの使用](manage-azure-subscriptions-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-120">For more information about subscription selection, see [Use multiple Azure subscriptions](manage-azure-subscriptions-azure-cli.md).</span></span>

<span data-ttu-id="befa5-121">対話型以外のサインイン方法も用意されています。詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-121">There are ways to sign in non-interactively, which are covered in detail in [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="common-commands"></a><span data-ttu-id="befa5-122">一般的なコマンド</span><span class="sxs-lookup"><span data-stu-id="befa5-122">Common commands</span></span>

<span data-ttu-id="befa5-123">次の表は、CLI で使用される一般的なコマンドの一部を示しており、リファレンス ドキュメントにリンクされています。</span><span class="sxs-lookup"><span data-stu-id="befa5-123">This table lists some common commands used in the CLI and links to their reference documentation.</span></span>

| <span data-ttu-id="befa5-124">リソースの種類</span><span class="sxs-lookup"><span data-stu-id="befa5-124">Resource type</span></span> | <span data-ttu-id="befa5-125">Azure CLI コマンド グループ</span><span class="sxs-lookup"><span data-stu-id="befa5-125">Azure CLI command group</span></span> |
|---------------|-------------------------|
| [<span data-ttu-id="befa5-126">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="befa5-126">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="befa5-127">az group</span><span class="sxs-lookup"><span data-stu-id="befa5-127">az group</span></span>](/cli/azure/group) |
| [<span data-ttu-id="befa5-128">仮想マシン</span><span class="sxs-lookup"><span data-stu-id="befa5-128">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="befa5-129">az vm</span><span class="sxs-lookup"><span data-stu-id="befa5-129">az vm</span></span>](/cli/azure/vm) |
| [<span data-ttu-id="befa5-130">ストレージ アカウント</span><span class="sxs-lookup"><span data-stu-id="befa5-130">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="befa5-131">az storage account</span><span class="sxs-lookup"><span data-stu-id="befa5-131">az storage account</span></span>](/cli/azure/storage/account) |
| [<span data-ttu-id="befa5-132">Key Vault</span><span class="sxs-lookup"><span data-stu-id="befa5-132">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="befa5-133">az keyvault</span><span class="sxs-lookup"><span data-stu-id="befa5-133">az keyvault</span></span>](/cli/azure/keyvault) |
| [<span data-ttu-id="befa5-134">Web アプリケーション</span><span class="sxs-lookup"><span data-stu-id="befa5-134">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="befa5-135">az webapp</span><span class="sxs-lookup"><span data-stu-id="befa5-135">az webapp</span></span>](/cli/azure/webapp) |
| [<span data-ttu-id="befa5-136">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="befa5-136">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="befa5-137">az sql server</span><span class="sxs-lookup"><span data-stu-id="befa5-137">az sql server</span></span>](/cli/azure/sql/server) |
| [<span data-ttu-id="befa5-138">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="befa5-138">CosmosDB</span></span>](/azure/cosmos-db) | [<span data-ttu-id="befa5-139">az cosmosdb</span><span class="sxs-lookup"><span data-stu-id="befa5-139">az cosmosdb</span></span>](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a><span data-ttu-id="befa5-140">コマンドを見つける</span><span class="sxs-lookup"><span data-stu-id="befa5-140">Finding commands</span></span>

<span data-ttu-id="befa5-141">CLI のコマンドは、"_グループ_" の "_サブコマンド_" として整理されています。</span><span class="sxs-lookup"><span data-stu-id="befa5-141">Commands in the CLI are organized as _commands_ of _groups_.</span></span> <span data-ttu-id="befa5-142">各グループは、Azure のサービスを表し、コマンドはそのサービスに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="befa5-142">Each group represents an Azure service, and commands operate on that service.</span></span>

<span data-ttu-id="befa5-143">コマンドを検索するには、[az find](/cli/azure/reference-index#az-find) を使用します。</span><span class="sxs-lookup"><span data-stu-id="befa5-143">To search for commands, use [az find](/cli/azure/reference-index#az-find).</span></span> <span data-ttu-id="befa5-144">たとえば、`secret` を含むコマンド名を検索するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="befa5-144">For example, to search for command names containing `secret`, use the following command:</span></span>

```azurecli-interactive
az find secret
```

<span data-ttu-id="befa5-145">コマンドと、グループのサブグループの完全な一覧を取得するには、`--help` 引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="befa5-145">Use the `--help` argument to get a complete list of commands and subgroups of a group.</span></span> <span data-ttu-id="befa5-146">たとえば、ネットワーク セキュリティ グループ (NSG) で使用する CLI コマンドを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="befa5-146">For example, to find the CLI commands for working with Network Security Groups (NSGs):</span></span>

```azurecli-interactive
az network nsg --help
```

<span data-ttu-id="befa5-147">CLI では Bash シェルにコマンドの完全タブ補完が用意されています。</span><span class="sxs-lookup"><span data-stu-id="befa5-147">The CLI has full tab completion for commands under the bash shell.</span></span>

## <a name="globally-available-arguments"></a><span data-ttu-id="befa5-148">グローバルに使用できる引数</span><span class="sxs-lookup"><span data-stu-id="befa5-148">Globally available arguments</span></span>

<span data-ttu-id="befa5-149">引数の中には、すべてのコマンドで使用できるものがあります。</span><span class="sxs-lookup"><span data-stu-id="befa5-149">There are some arguments that are available for every command.</span></span>

* <span data-ttu-id="befa5-150">`--help` は、コマンドとその引数に関する CLI 参照情報を出力し、利用可能なサブグループとコマンドの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="befa5-150">`--help` prints CLI reference information about commands and their arguments and lists available subgroups and commands.</span></span>
* <span data-ttu-id="befa5-151">`--output` は出力形式を変更します。</span><span class="sxs-lookup"><span data-stu-id="befa5-151">`--output` changes the output format.</span></span> <span data-ttu-id="befa5-152">使用可能な出力形式は `json`、`jsonc` (色付けされた JSON)、`tsv` (タブ区切り値)、および `table` (人間が判読できる ASCII テーブル)、および `yaml` です。</span><span class="sxs-lookup"><span data-stu-id="befa5-152">The available output formats are `json`, `jsonc` (colorized JSON), `tsv` (Tab-Separated Values), `table` (human-readable ASCII tables), and `yaml`.</span></span> <span data-ttu-id="befa5-153">既定では、CLI は `json` を出力します。</span><span class="sxs-lookup"><span data-stu-id="befa5-153">By default the CLI outputs `json`.</span></span> <span data-ttu-id="befa5-154">使用可能な出力形式の詳細については、[Azure CLI の出力形式](format-output-azure-cli.md)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="befa5-154">To learn more about the available output formats, see [Output formats for Azure CLI](format-output-azure-cli.md).</span></span>
* <span data-ttu-id="befa5-155">`--query` は、[JMESPath クエリ言語](http://jmespath.org/)を使用して、Azure サービスから返された出力をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="befa5-155">`--query` uses the [JMESPath query language](http://jmespath.org/) to filter the output returned from Azure services.</span></span> <span data-ttu-id="befa5-156">クエリの詳細については、[Azure CLI でのコマンド結果に対するクエリの実行](query-azure-cli.md)に関するページ、および「[JMESPath tutorial (JMESPath チュートリアル)](http://jmespath.org/tutorial.html)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-156">To learn more about queries, see [Query command results with Azure CLI](query-azure-cli.md) and the [JMESPath tutorial](http://jmespath.org/tutorial.html).</span></span>
* <span data-ttu-id="befa5-157">`--verbose` は、操作中に Azure で作成されたリソースに関する情報と、その他の有用な情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="befa5-157">`--verbose` prints information about resources created in Azure during an operation, and other useful information.</span></span>
* <span data-ttu-id="befa5-158">`--debug` は、デバッグの目的で使用する、CLI 操作に関する詳細情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="befa5-158">`--debug` prints even more information about CLI operations, used for debugging purposes.</span></span> <span data-ttu-id="befa5-159">バグを見つけた場合は、バグ レポートを送信するときに、`--debug` フラグをオンにして生成した出力を提供してください。</span><span class="sxs-lookup"><span data-stu-id="befa5-159">If you find a bug, provide output generated with the `--debug` flag on when submitting a bug report.</span></span>

## <a name="interactive-mode"></a><span data-ttu-id="befa5-160">対話モード</span><span class="sxs-lookup"><span data-stu-id="befa5-160">Interactive mode</span></span>

<span data-ttu-id="befa5-161">CLI には対話モードが用意されています。このモードでは、ヘルプ情報が自動的に表示され、サブコマンドが選択しやすくなっています。</span><span class="sxs-lookup"><span data-stu-id="befa5-161">The CLI offers an interactive mode that automatically displays help information and makes it easier to select subcommands.</span></span> <span data-ttu-id="befa5-162">対話モードには [az interactive](/cli/azure/reference-index#az-interactive) コマンドで切り替えます。</span><span class="sxs-lookup"><span data-stu-id="befa5-162">You enter interactive mode with the [az interactive](/cli/azure/reference-index#az-interactive) command.</span></span>

```azurecli-interactive
az interactive
```

<span data-ttu-id="befa5-163">対話モードの詳細については、[Azure CLI 対話モード](interactive-azure-cli.md)に関する記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="befa5-163">For more information on interactive mode, see [Azure CLI Interactive Mode](interactive-azure-cli.md).</span></span>

<span data-ttu-id="befa5-164">また、オートコンプリート、マウス オーバー ドキュメントなど、対話型エクスペリエンスを提供する [Visual Studio Code プラグイン](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)も用意されています。</span><span class="sxs-lookup"><span data-stu-id="befa5-164">There's also a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) that offers an interactive experience, including autocomplete and mouse-over documentation.</span></span>

## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="befa5-165">クイックスタートとチュートリアルを利用して CLI の基本について学習する</span><span class="sxs-lookup"><span data-stu-id="befa5-165">Learn CLI basics with quickstarts and tutorials</span></span>

<span data-ttu-id="befa5-166">Azure CLI の使用を開始するには、詳細なチュートリアルをお試しください。チュートリアルでは、仮想マシンを設定し、CLI の機能を使用して Azure リソースにクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="befa5-166">To get you started with the Azure CLI, try an in-depth tutorial for setting up virtual machines and using the power of the CLI to query Azure resources.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="befa5-167">Azure CLI での仮想マシンの作成チュートリアル</span><span class="sxs-lookup"><span data-stu-id="befa5-167">Create virtual machines with the Azure CLI tutorial</span></span>](azure-cli-vm-tutorial.yml)

<span data-ttu-id="befa5-168">その他の人気のあるサービス用のクイック スタートもあります。</span><span class="sxs-lookup"><span data-stu-id="befa5-168">There are also quickstarts for other popular services.</span></span>

* [<span data-ttu-id="befa5-169">Azure CLI を使用したストレージ アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="befa5-169">Create a storage account using the Azure CLI</span></span>](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [<span data-ttu-id="befa5-170">CLI を使用した Azure Blob Storage との間でのオブジェクトの転送</span><span class="sxs-lookup"><span data-stu-id="befa5-170">Transfer objects to/from Azure Blob storage using the CLI</span></span>](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [<span data-ttu-id="befa5-171">Azure CLI を使用した単一の Azure SQL データベースの作成</span><span class="sxs-lookup"><span data-stu-id="befa5-171">Create a single Azure SQL database using the Azure CLI</span></span>](/azure/sql-database/sql-database-get-started-cli)
* [<span data-ttu-id="befa5-172">Azure CLI を使用した Azure Database for MySQL サーバーの作成</span><span class="sxs-lookup"><span data-stu-id="befa5-172">Create an Azure Database for MySQL server using the Azure CLI</span></span>](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [<span data-ttu-id="befa5-173">Azure CLI を使用した Azure Database for PostgreSQL の作成</span><span class="sxs-lookup"><span data-stu-id="befa5-173">Create an Azure Database for PostgreSQL using the Azure CLI</span></span>](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [<span data-ttu-id="befa5-174">Azure での Python Web アプリの作成</span><span class="sxs-lookup"><span data-stu-id="befa5-174">Create a Python web app in Azure</span></span>](/azure/app-service/app-service-web-get-started-python)
* [<span data-ttu-id="befa5-175">Azure Web Apps for Containers でのカスタム Docker Hub イメージの実行</span><span class="sxs-lookup"><span data-stu-id="befa5-175">Run a custom Docker Hub image in Azure Web Apps for Containers</span></span>](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a><span data-ttu-id="befa5-176">フィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="befa5-176">Give feedback</span></span>

<span data-ttu-id="befa5-177">機能強化とバグ解決に活かすために、CLI に関する皆様のご意見をお待ちしております。</span><span class="sxs-lookup"><span data-stu-id="befa5-177">We welcome your feedback for the CLI to help us make improvements and resolve bugs.</span></span> <span data-ttu-id="befa5-178">[GitHub で問題を報告](https://github.com/azure/azure-cli/issues)するか、CLI の組み込み機能を使用して、[az feedback](/cli/azure/reference-index#az-feedback) コマンドで一般的なフィードバックをお寄せください。</span><span class="sxs-lookup"><span data-stu-id="befa5-178">You can [file an issue on GitHub](https://github.com/azure/azure-cli/issues) or use the built-in features of the CLI to leave general feedback with the [az feedback](/cli/azure/reference-index#az-feedback) command.</span></span>

```azurecli-interactive
az feedback
```

## <a name="see-also"></a><span data-ttu-id="befa5-179">参照</span><span class="sxs-lookup"><span data-stu-id="befa5-179">See also</span></span>

* [<span data-ttu-id="befa5-180">Azure CLI で管理できるサービス</span><span class="sxs-lookup"><span data-stu-id="befa5-180">Services the Azure CLI can manage</span></span>](azure-services-the-azure-cli-can-manage.md)
* [<span data-ttu-id="befa5-181">Azure CLI の完全なコマンド リファレンス一覧</span><span class="sxs-lookup"><span data-stu-id="befa5-181">Full command reference list for the Azure CLI</span></span>](/cli/azure/reference-index)
* [<span data-ttu-id="befa5-182">Azure CLI の使用に関する人気のある記事</span><span class="sxs-lookup"><span data-stu-id="befa5-182">Popular articles on using the Azure CLI</span></span>](popular-articles-using-the-azure-cli.md)
