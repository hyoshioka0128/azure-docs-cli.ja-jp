---
title: Azure CLI 構成オプション
description: Azure CLI を構成する方法
keywords: Azure CLI, 構成, 設定, Azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/11/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: d23f576a1f7447ffab0606b4554a81ae5c536e85
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593780"
---
# <a name="azure-cli-configuration"></a><span data-ttu-id="48287-104">Azure CLI の構成</span><span class="sxs-lookup"><span data-stu-id="48287-104">Azure CLI configuration</span></span>

<span data-ttu-id="48287-105">Azure CLI を使用すると、ログ記録、データ収集、既定の引数値などの設定をユーザーが構成できます。</span><span class="sxs-lookup"><span data-stu-id="48287-105">The Azure CLI allows for user configuration for settings such as logging, data collection, and default argument values.</span></span>
<span data-ttu-id="48287-106">CLI には、いくつかの既定値を管理するための便利なコマンドとして、`az configure` が用意されています。</span><span class="sxs-lookup"><span data-stu-id="48287-106">The CLI offers a convenience command for managing some defaults, `az configure`.</span></span> <span data-ttu-id="48287-107">他の値については、構成ファイルまたは環境変数を使用して設定できます。</span><span class="sxs-lookup"><span data-stu-id="48287-107">Other values can be set in a configuration file or with environment variables.</span></span>

<span data-ttu-id="48287-108">CLI で使用される構成値は、次の優先順位で上から順番に評価されます。</span><span class="sxs-lookup"><span data-stu-id="48287-108">Configuration values used by the CLI are evaluated in the following precedence, with items higher on the list taking priority.</span></span>

1. <span data-ttu-id="48287-109">コマンドライン パラメーター</span><span class="sxs-lookup"><span data-stu-id="48287-109">Command-line parameters</span></span>
2. <span data-ttu-id="48287-110">環境変数</span><span class="sxs-lookup"><span data-stu-id="48287-110">Environment variables</span></span>
3. <span data-ttu-id="48287-111">構成ファイルの値または `az configure` で設定された値</span><span class="sxs-lookup"><span data-stu-id="48287-111">Values in the configuration file or set with `az configure`</span></span>

## <a name="cli-configuration-with-az-configure"></a><span data-ttu-id="48287-112">az configure での CLI 構成</span><span class="sxs-lookup"><span data-stu-id="48287-112">CLI configuration with az configure</span></span>

<span data-ttu-id="48287-113">CLI の既定値を [az configure](/cli/azure/reference-index#az-configure) コマンドで設定します。</span><span class="sxs-lookup"><span data-stu-id="48287-113">You set defaults for the CLI with the [az configure](/cli/azure/reference-index#az-configure) command.</span></span>
<span data-ttu-id="48287-114">このコマンドは 1 つの引数 `--defaults` を取ります。この引数は、スペースで区切られた `key=value` ペアのリストです。</span><span class="sxs-lookup"><span data-stu-id="48287-114">This command takes one argument, `--defaults`, which is a space-separated list of `key=value` pairs.</span></span> <span data-ttu-id="48287-115">指定した値は、必須の引数の代わりに、CLI によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="48287-115">The provided values are used by the CLI in place of required arguments.</span></span>

<span data-ttu-id="48287-116">次の表に、使用可能な構成キーの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="48287-116">The following table contains a list of available configuration keys.</span></span>

| <span data-ttu-id="48287-117">Name</span><span class="sxs-lookup"><span data-stu-id="48287-117">Name</span></span> | <span data-ttu-id="48287-118">説明</span><span class="sxs-lookup"><span data-stu-id="48287-118">Description</span></span> |
|------|-------------|
| <span data-ttu-id="48287-119">group</span><span class="sxs-lookup"><span data-stu-id="48287-119">group</span></span> | <span data-ttu-id="48287-120">すべてのコマンドに使用する既定のリソース グループ。</span><span class="sxs-lookup"><span data-stu-id="48287-120">The default resource group to use for all commands.</span></span> |
| <span data-ttu-id="48287-121">location</span><span class="sxs-lookup"><span data-stu-id="48287-121">location</span></span> | <span data-ttu-id="48287-122">すべてのコマンドに使用する既定の場所。</span><span class="sxs-lookup"><span data-stu-id="48287-122">The default location to use for all commands.</span></span> |
| <span data-ttu-id="48287-123">web</span><span class="sxs-lookup"><span data-stu-id="48287-123">web</span></span> | <span data-ttu-id="48287-124">`az webapp` コマンドに使用する既定のアプリ名。</span><span class="sxs-lookup"><span data-stu-id="48287-124">The default app name to use for `az webapp` commands.</span></span> |
| <span data-ttu-id="48287-125">vm</span><span class="sxs-lookup"><span data-stu-id="48287-125">vm</span></span> | <span data-ttu-id="48287-126">`az vm` コマンドに使用する既定の VM 名。</span><span class="sxs-lookup"><span data-stu-id="48287-126">The default VM name to use for `az vm` commands.</span></span> |
| <span data-ttu-id="48287-127">vmss</span><span class="sxs-lookup"><span data-stu-id="48287-127">vmss</span></span> | <span data-ttu-id="48287-128">`az vmss` コマンドに使用する既定の仮想マシン スケール セット (VMSS) 名。</span><span class="sxs-lookup"><span data-stu-id="48287-128">The default virtual machine scale set (VMSS) name to use for  `az vmss` commands.</span></span> |
| <span data-ttu-id="48287-129">acr</span><span class="sxs-lookup"><span data-stu-id="48287-129">acr</span></span> | <span data-ttu-id="48287-130">`az acr` コマンドに使用する既定のコンテナー レジストリ名。</span><span class="sxs-lookup"><span data-stu-id="48287-130">The default container registry name to use for `az acr` commands.</span></span> |

<span data-ttu-id="48287-131">例として、すべてのコマンドの既定のリソース グループと場所を設定する方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="48287-131">As an example, here's how you would set the default resource group and location for all commands.</span></span>

```azurecli-interactive
az configure --defaults location=westus2 group=MyResourceGroup
```

## <a name="cli-configuration-file"></a><span data-ttu-id="48287-132">CLI 構成ファイル</span><span class="sxs-lookup"><span data-stu-id="48287-132">CLI configuration file</span></span>

<span data-ttu-id="48287-133">CLI 構成ファイルには、CLI の動作の管理に使用されるその他の設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="48287-133">The CLI configuration file contains other settings that are used for managing CLI behavior.</span></span> <span data-ttu-id="48287-134">構成ファイル自体は `$AZURE_CONFIG_DIR/config` にあります。</span><span class="sxs-lookup"><span data-stu-id="48287-134">The configuration file itself is located at `$AZURE_CONFIG_DIR/config`.</span></span> <span data-ttu-id="48287-135">`AZURE_CONFIG_DIR` の既定値は、Linux と macOS の場合は `$HOME/.azure`、Windows の場合は `%USERPROFILE%\.azure` です。</span><span class="sxs-lookup"><span data-stu-id="48287-135">The default value of `AZURE_CONFIG_DIR` is `$HOME/.azure` on Linux and macOS, and `%USERPROFILE%\.azure` on Windows.</span></span>

<span data-ttu-id="48287-136">構成ファイルは、INI ファイル形式で記述されます。</span><span class="sxs-lookup"><span data-stu-id="48287-136">Configuration files are written in the INI file format.</span></span> <span data-ttu-id="48287-137">このファイルの形式は、セクション ヘッダーと、これに続くキーと値のエントリの一覧となります。</span><span class="sxs-lookup"><span data-stu-id="48287-137">This file format is defined by section headers, followed by a list of key-value entries.</span></span>

* <span data-ttu-id="48287-138">セクション ヘッダーは、`[section-name]` のように記述されます。</span><span class="sxs-lookup"><span data-stu-id="48287-138">Section headers are written as `[section-name]`.</span></span> <span data-ttu-id="48287-139">セクション名は、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="48287-139">Section names are case-sensitive.</span></span>
* <span data-ttu-id="48287-140">エントリは、`key=value` のように記述されます。</span><span class="sxs-lookup"><span data-stu-id="48287-140">Entries are written as `key=value`.</span></span> <span data-ttu-id="48287-141">キー名の大文字と小文字は、区別されません。</span><span class="sxs-lookup"><span data-stu-id="48287-141">Key names are not case-sensitive.</span></span>
* <span data-ttu-id="48287-142">`#` または `;` で始まる行はすべてコメントです。</span><span class="sxs-lookup"><span data-stu-id="48287-142">Comments are any line that begins with a `#` or `;`.</span></span> <span data-ttu-id="48287-143">インライン コメントは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="48287-143">Inline comments are not allowed.</span></span>

<span data-ttu-id="48287-144">ブール値は、大文字と小文字が区別されず、次の値によって表されます。</span><span class="sxs-lookup"><span data-stu-id="48287-144">Booleans are case-insensitive, and are represented by the following values.</span></span>

* <span data-ttu-id="48287-145">__True__:1、yes、true、on</span><span class="sxs-lookup"><span data-stu-id="48287-145">__True__: 1, yes, true, on</span></span>
* <span data-ttu-id="48287-146">__False__:0、no、false、off</span><span class="sxs-lookup"><span data-stu-id="48287-146">__False__: 0, no, false, off</span></span>

<span data-ttu-id="48287-147">次の例は、確認のプロンプトを無効にして、`/var/log/azure` ディレクトリへのログ記録を設定する CLI 構成ファイルです。</span><span class="sxs-lookup"><span data-stu-id="48287-147">Here's an example of a CLI configuration file that disables any confirmation prompts and sets up logging to the `/var/log/azure` directory.</span></span>

```ini
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

<span data-ttu-id="48287-148">使用できる構成値とその意味の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48287-148">See the next section for details on all of the available configuration values and what they mean.</span></span> <span data-ttu-id="48287-149">INI ファイル形式の詳細については、[INI に関する Python のドキュメント](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48287-149">For the full details on the INI file format, see the [Python documentation on INI](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure).</span></span>

## <a name="cli-configuration-values-and-environment-variables"></a><span data-ttu-id="48287-150">CLI 構成値と環境変数</span><span class="sxs-lookup"><span data-stu-id="48287-150">CLI configuration values and environment variables</span></span>

<span data-ttu-id="48287-151">次の表は、構成ファイルで指定できるすべてのセクションとオプションの名前を示しています。</span><span class="sxs-lookup"><span data-stu-id="48287-151">The following table contains all of the sections and option names that can be placed in a configuration file.</span></span> <span data-ttu-id="48287-152">対応する環境変数は、`AZURE_{section}_{name}` のようにすべて大文字で設定できます。</span><span class="sxs-lookup"><span data-stu-id="48287-152">Their corresponding environment variables are set as `AZURE_{section}_{name}`, in all caps.</span></span> <span data-ttu-id="48287-153">たとえば、`batchai` の既定値 `storage_account` は、`AZURE_BATCHAI_STORAGE_ACCOUNT` 変数で設定されます。</span><span class="sxs-lookup"><span data-stu-id="48287-153">For example, the `storage_account` default for `batchai` is set in the `AZURE_BATCHAI_STORAGE_ACCOUNT` variable.</span></span>

<span data-ttu-id="48287-154">既定値を指定すると、その引数は任意のコマンドで不要になります。</span><span class="sxs-lookup"><span data-stu-id="48287-154">When you provide a default value, that argument is no longer required by any command.</span></span> <span data-ttu-id="48287-155">代わりに、その既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="48287-155">Instead, the default value is used.</span></span>

| <span data-ttu-id="48287-156">セクション</span><span class="sxs-lookup"><span data-stu-id="48287-156">Section</span></span> | <span data-ttu-id="48287-157">Name</span><span class="sxs-lookup"><span data-stu-id="48287-157">Name</span></span>      | <span data-ttu-id="48287-158">type</span><span class="sxs-lookup"><span data-stu-id="48287-158">Type</span></span> | <span data-ttu-id="48287-159">説明</span><span class="sxs-lookup"><span data-stu-id="48287-159">Description</span></span>|
|---------|-----------|------|------------|
| <span data-ttu-id="48287-160">__core__</span><span class="sxs-lookup"><span data-stu-id="48287-160">__core__</span></span> | <span data-ttu-id="48287-161">output</span><span class="sxs-lookup"><span data-stu-id="48287-161">output</span></span> | <span data-ttu-id="48287-162">string</span><span class="sxs-lookup"><span data-stu-id="48287-162">string</span></span> | <span data-ttu-id="48287-163">既定の出力形式。</span><span class="sxs-lookup"><span data-stu-id="48287-163">The default output format.</span></span> <span data-ttu-id="48287-164">`json`、`jsonc`、`tsv`、`table` のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="48287-164">Can be one of `json`, `jsonc`, `tsv`, or `table`.</span></span> |
| | <span data-ttu-id="48287-165">disable\_confirm\_prompt</span><span class="sxs-lookup"><span data-stu-id="48287-165">disable\_confirm\_prompt</span></span> | <span data-ttu-id="48287-166">ブール値</span><span class="sxs-lookup"><span data-stu-id="48287-166">boolean</span></span> | <span data-ttu-id="48287-167">確認のプロンプトをオン/オフにします。</span><span class="sxs-lookup"><span data-stu-id="48287-167">Turn confirmation prompts on/off.</span></span> |
| | <span data-ttu-id="48287-168">collect\_telemetry</span><span class="sxs-lookup"><span data-stu-id="48287-168">collect\_telemetry</span></span> | <span data-ttu-id="48287-169">ブール値</span><span class="sxs-lookup"><span data-stu-id="48287-169">boolean</span></span> | <span data-ttu-id="48287-170">Microsoft による、CLI の使用に関する匿名データの収集を許可します。</span><span class="sxs-lookup"><span data-stu-id="48287-170">Allow Microsoft to collect anonymous data on the usage of the CLI.</span></span> <span data-ttu-id="48287-171">プライバシー情報については、[Azure CLI の使用条件](http://aka.ms/AzureCliLegal)に関するページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="48287-171">For privacy information, see the [Azure CLI Terms of Use](http://aka.ms/AzureCliLegal).</span></span> |
| <span data-ttu-id="48287-172">__logging__</span><span class="sxs-lookup"><span data-stu-id="48287-172">__logging__</span></span> | <span data-ttu-id="48287-173">enable\_log\_file</span><span class="sxs-lookup"><span data-stu-id="48287-173">enable\_log\_file</span></span> | <span data-ttu-id="48287-174">ブール値</span><span class="sxs-lookup"><span data-stu-id="48287-174">boolean</span></span> | <span data-ttu-id="48287-175">ログ記録をオン/オフにします。</span><span class="sxs-lookup"><span data-stu-id="48287-175">Turn logging on/off.</span></span> |
| | <span data-ttu-id="48287-176">log\_dir</span><span class="sxs-lookup"><span data-stu-id="48287-176">log\_dir</span></span> | <span data-ttu-id="48287-177">string</span><span class="sxs-lookup"><span data-stu-id="48287-177">string</span></span> | <span data-ttu-id="48287-178">ログを書き込むディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="48287-178">The directory to write logs to.</span></span> <span data-ttu-id="48287-179">この値の既定値は `${AZURE_CONFIG_DIR}/logs` です。</span><span class="sxs-lookup"><span data-stu-id="48287-179">By default this value is `${AZURE_CONFIG_DIR}/logs`.</span></span> |
| <span data-ttu-id="48287-180">__storage__</span><span class="sxs-lookup"><span data-stu-id="48287-180">__storage__</span></span> | <span data-ttu-id="48287-181">connection\_string</span><span class="sxs-lookup"><span data-stu-id="48287-181">connection\_string</span></span> | <span data-ttu-id="48287-182">string</span><span class="sxs-lookup"><span data-stu-id="48287-182">string</span></span> | <span data-ttu-id="48287-183">`az storage` コマンドに使用する既定の接続文字列。</span><span class="sxs-lookup"><span data-stu-id="48287-183">The default connection string to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="48287-184">アカウント</span><span class="sxs-lookup"><span data-stu-id="48287-184">account</span></span> | <span data-ttu-id="48287-185">string</span><span class="sxs-lookup"><span data-stu-id="48287-185">string</span></span> | <span data-ttu-id="48287-186">`az storage` コマンドに使用する既定のアカウント名。</span><span class="sxs-lookup"><span data-stu-id="48287-186">The default account name to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="48287-187">key</span><span class="sxs-lookup"><span data-stu-id="48287-187">key</span></span> | <span data-ttu-id="48287-188">string</span><span class="sxs-lookup"><span data-stu-id="48287-188">string</span></span> | <span data-ttu-id="48287-189">`az storage` コマンドに使用する既定のアカウント キー。</span><span class="sxs-lookup"><span data-stu-id="48287-189">The default account key to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="48287-190">sas\_token</span><span class="sxs-lookup"><span data-stu-id="48287-190">sas\_token</span></span> | <span data-ttu-id="48287-191">string</span><span class="sxs-lookup"><span data-stu-id="48287-191">string</span></span> | <span data-ttu-id="48287-192">`az storage` コマンドに使用する既定の SAS トークン。</span><span class="sxs-lookup"><span data-stu-id="48287-192">The default SAS token to use for `az storage` commands.</span></span> |
| <span data-ttu-id="48287-193">__batchai__</span><span class="sxs-lookup"><span data-stu-id="48287-193">__batchai__</span></span> | <span data-ttu-id="48287-194">storage\_account</span><span class="sxs-lookup"><span data-stu-id="48287-194">storage\_account</span></span> | <span data-ttu-id="48287-195">string</span><span class="sxs-lookup"><span data-stu-id="48287-195">string</span></span> | <span data-ttu-id="48287-196">`az batchai` コマンドに使用する既定のストレージ アカウント。</span><span class="sxs-lookup"><span data-stu-id="48287-196">The default storage account to use for `az batchai` commands.</span></span> |
| | <span data-ttu-id="48287-197">storage\_key</span><span class="sxs-lookup"><span data-stu-id="48287-197">storage\_key</span></span> | <span data-ttu-id="48287-198">string</span><span class="sxs-lookup"><span data-stu-id="48287-198">string</span></span> | <span data-ttu-id="48287-199">`az batchai` コマンドに使用する既定のストレージ キー。</span><span class="sxs-lookup"><span data-stu-id="48287-199">The default storage key to use for `az batchai` commands.</span></span> |
| <span data-ttu-id="48287-200">__batch__</span><span class="sxs-lookup"><span data-stu-id="48287-200">__batch__</span></span> | <span data-ttu-id="48287-201">アカウント</span><span class="sxs-lookup"><span data-stu-id="48287-201">account</span></span> | <span data-ttu-id="48287-202">string</span><span class="sxs-lookup"><span data-stu-id="48287-202">string</span></span> | <span data-ttu-id="48287-203">`az batch` コマンドに使用する既定の Azure Batch アカウント名。</span><span class="sxs-lookup"><span data-stu-id="48287-203">The default Azure Batch account name to use for `az batch` commands.</span></span> |
| | <span data-ttu-id="48287-204">access\_key</span><span class="sxs-lookup"><span data-stu-id="48287-204">access\_key</span></span> | <span data-ttu-id="48287-205">string</span><span class="sxs-lookup"><span data-stu-id="48287-205">string</span></span> | <span data-ttu-id="48287-206">`az batch` コマンドに使用する既定のアクセス キー。</span><span class="sxs-lookup"><span data-stu-id="48287-206">The default access key to use for `az batch` commands.</span></span> <span data-ttu-id="48287-207">`aad` 承認でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="48287-207">Only used with `aad` authorization.</span></span> |
| | <span data-ttu-id="48287-208">endpoint</span><span class="sxs-lookup"><span data-stu-id="48287-208">endpoint</span></span> | <span data-ttu-id="48287-209">string</span><span class="sxs-lookup"><span data-stu-id="48287-209">string</span></span> | <span data-ttu-id="48287-210">`az batch` コマンドに対する既定の接続先エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="48287-210">The default endpoint to connect to for `az batch` commands.</span></span> |
| | <span data-ttu-id="48287-211">auth\_mode</span><span class="sxs-lookup"><span data-stu-id="48287-211">auth\_mode</span></span> | <span data-ttu-id="48287-212">string</span><span class="sxs-lookup"><span data-stu-id="48287-212">string</span></span> | <span data-ttu-id="48287-213">`az batch` コマンドに使用する承認モード。</span><span class="sxs-lookup"><span data-stu-id="48287-213">The authorization mode to use for `az batch` commands.</span></span> <span data-ttu-id="48287-214">`shared_key` または `aad` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="48287-214">Can be `shared_key` or `aad`.</span></span> |

> [!NOTE]
> <span data-ttu-id="48287-215">構成ファイルに他の値が含まれる場合もありますが、その値は、`az configure` などの CLI コマンドで直接管理されます。</span><span class="sxs-lookup"><span data-stu-id="48287-215">You may see other values in your configuration file, but these are managed directly through CLI commands, including `az configure`.</span></span> <span data-ttu-id="48287-216">上記の表は、自身で変更する必要がある値のみを示しています。</span><span class="sxs-lookup"><span data-stu-id="48287-216">The ones listed in the table above are the only values you should change yourself.</span></span>
