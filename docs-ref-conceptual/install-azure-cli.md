---
title: "Azure CLI 2.0 のインストール"
description: "Azure CLI 2.0 のリファレンス ドキュメント"
keywords: "Azure CLI 2.0, Azure CLI 2.0 のリファレンス, Azure CLI 2.0 のインストール, Azure Python CLI, Azure CLI 2.0 のアンインストール"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 7065ed5270ef9bfc70beea81d0bc442a7b4df38c
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.contentlocale: ja-JP
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="848e9-104">Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="848e9-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="848e9-105">今すぐ Azure CLI の新しいバージョンをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="848e9-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="848e9-106">Azure のリソース管理を目的とした優れたネイティブ コマンド ライン エクスペリエンスを実現するために強化して更新しました。</span><span class="sxs-lookup"><span data-stu-id="848e9-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="848e9-107">macOS、Linux、および Windows で使用できます。</span><span class="sxs-lookup"><span data-stu-id="848e9-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="848e9-108">最新リリースについては、[リリース ノート](release-notes-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="848e9-109">Azure CLI の以前のバージョンが必要な場合は、[Azure 1.0 をインストールする](/azure/cli-install-nodejs)方法を参照してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-109">If you need the previous version of the Azure CLI, here's how to [install Azure 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="848e9-110">macOS</span><span class="sxs-lookup"><span data-stu-id="848e9-110">macOS</span></span>

1. <span data-ttu-id="848e9-111">1 つの `curl` コマンドで Azure CLI 2.0 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-111">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="848e9-112">場合によっては、変更を有効にするために、コマンド シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="848e9-112">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="848e9-113">コマンド プロンプトから `az` コマンドを使用して、Azure CLI 2.0 を実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-113">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="848e9-114">InstallAzureCli を使用してインストールした場合、`az component update` はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="848e9-114">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="848e9-115">最新の CLI に更新するには、`curl -L https://aka.ms/InstallAzureCli | bash` をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-115">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="848e9-116">アンインストールするには、[手動のアンインストール手順](#uninstall)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-116">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="848e9-117">Windows</span><span class="sxs-lookup"><span data-stu-id="848e9-117">Windows</span></span>

<span data-ttu-id="848e9-118">MSI を使用して CLI をインストールし、Windows コマンド ラインで使用するか、Bash on Ubuntu on Windows で apt-get を使用して、CLI をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="848e9-118">You can install the CLI with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="848e9-119">Windows コマンド ライン用の MSI</span><span class="sxs-lookup"><span data-stu-id="848e9-119">MSI for the Windows command-line</span></span> 

<span data-ttu-id="848e9-120">Windows に CLI をインストールして、Windows コマンド ラインで使用するには、[msi](https://aka.ms/InstallAzureCliWindows) をダウンロードして実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-120">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="848e9-121">msi を使用してインストールする場合、`az component` はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="848e9-121">When you install with the msi, `az component` isn't supported.</span></span>
> <span data-ttu-id="848e9-122">最新の CLI に更新するには、[msi](https://aka.ms/InstallAzureCliWindows) をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-122">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="848e9-123">CLI をアンインストールするには、[msi](https://aka.ms/InstallAzureCliWindows) をもう一度実行して、アンインストールを選択します。</span><span class="sxs-lookup"><span data-stu-id="848e9-123">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="848e9-124">Bash on Ubuntu on Windows 用の apt-get</span><span class="sxs-lookup"><span data-stu-id="848e9-124">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="848e9-125">Bash on Windows をインストールしていない場合は、[インストールします](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="848e9-125">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="848e9-126">Bash シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="848e9-126">Open the Bash shell.</span></span>

3. <span data-ttu-id="848e9-127">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="848e9-127">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="848e9-128">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-128">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="848e9-129">apt-get を使用してインストールした場合、`az component` はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="848e9-129">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="848e9-130">CLI を更新するには、`sudo apt-get update && sudo apt-get install azure-cli` をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-130">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="848e9-131">アンインストールするには、`sudo apt-get remove azure-cli` を実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-131">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux"></a><span data-ttu-id="848e9-132">Linux</span><span class="sxs-lookup"><span data-stu-id="848e9-132">Linux</span></span>

1. <span data-ttu-id="848e9-133">Linux では、固有の[前提条件](#linux-prerequisites)をインストールすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="848e9-133">On Linux, you may need to install specific [prerequisites](#linux-prerequisites).</span></span>

2. <span data-ttu-id="848e9-134">1 つの `curl` コマンドで Azure CLI 2.0 をインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-134">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="848e9-135">場合によっては、変更を有効にするために、コマンド シェルを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="848e9-135">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="848e9-136">コマンド プロンプトから `az` コマンドを使用して、Azure CLI 2.0 を実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-136">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="848e9-137">InstallAzureCli を使用してインストールした場合、`az component update` はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="848e9-137">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="848e9-138">最新の CLI に更新するには、`curl -L https://aka.ms/InstallAzureCli | bash` をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-138">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="848e9-139">アンインストールするには、[手動のアンインストール手順](#uninstall)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-139">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="docker"></a><span data-ttu-id="848e9-140">Docker</span><span class="sxs-lookup"><span data-stu-id="848e9-140">Docker</span></span>

<span data-ttu-id="848e9-141">Microsoft では、Azure CLI が事前構成されている Docker イメージを保持しています。</span><span class="sxs-lookup"><span data-stu-id="848e9-141">We maintain a Docker image preconfigured with the Azure CLI.</span></span>

<span data-ttu-id="848e9-142">`docker run` を使用して Azure CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-142">Install the Azure CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="848e9-143">利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-143">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="848e9-144">ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。</span><span class="sxs-lookup"><span data-stu-id="848e9-144">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> <span data-ttu-id="848e9-145">Docker イメージでは、[`component` 機能](/cli/azure/component)がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="848e9-145">The Docker image does not support the [`component` feature](/cli/azure/component).</span></span>
> <span data-ttu-id="848e9-146">Azure CLI 2.0 を更新するには、`docker run` を使用して、最新のイメージまたは必要とする特定のイメージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-146">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="apt-get"></a><span data-ttu-id="848e9-147">apt-get</span><span class="sxs-lookup"><span data-stu-id="848e9-147">apt-get</span></span>

<span data-ttu-id="848e9-148">Debian/Ubuntu ベースのシステムでは、`apt-get` を使用して Azure CLI 2.0 をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="848e9-148">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="848e9-149">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="848e9-149">Modify your sources list.</span></span>

   - <span data-ttu-id="848e9-150">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="848e9-150">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="848e9-151">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="848e9-151">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="848e9-152">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-152">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="848e9-153">apt-get を使用してインストールした場合、`az component` はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="848e9-153">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="848e9-154">CLI を更新するには、`sudo apt-get update && sudo apt-get install azure-cli` をもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-154">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="848e9-155">アンインストールするには、`sudo apt-get remove azure-cli` を実行します。</span><span class="sxs-lookup"><span data-stu-id="848e9-155">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux-prerequisites"></a><span data-ttu-id="848e9-156">Linux の前提条件</span><span class="sxs-lookup"><span data-stu-id="848e9-156">Linux Prerequisites</span></span>

1. <span data-ttu-id="848e9-157">[Python](https://www.python.org/downloads) をインストールしていない場合は、インストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-157">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="848e9-158">お使いの Linux ディストリビューションに応じて、前提条件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-158">Depending on your Linux distribution, install the prerequisites.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a><span data-ttu-id="848e9-159">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="848e9-159">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="848e9-160">curl リダイレクトでのエラー</span><span class="sxs-lookup"><span data-stu-id="848e9-160">Errors with curl redirection</span></span>

<span data-ttu-id="848e9-161">`curl` コマンドで `-L` パラメーターに関連するエラーが発生した場合や、"Object moved" というエラーが発生した場合は、aka.ms URL の代わりに完全な URL を使用してみてください。</span><span class="sxs-lookup"><span data-stu-id="848e9-161">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a><span data-ttu-id="848e9-162">アンインストール</span><span class="sxs-lookup"><span data-stu-id="848e9-162">Uninstall</span></span>

<span data-ttu-id="848e9-163">https://aka.ms/InstallAzureCli のスクリプトを使用して CLI をインストールした場合は、次の手順でアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="848e9-163">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="848e9-164">インストールされたファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="848e9-164">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="848e9-165">`<install location>/.bash_profile` から `<install location>/lib/azure-cli/az.completion` という行を削除します。</span><span class="sxs-lookup"><span data-stu-id="848e9-165">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="848e9-166">既定のインストール場所は `/Users/<username>` です。</span><span class="sxs-lookup"><span data-stu-id="848e9-166">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="848e9-167">apt-get、Docker、または msi を使用して CLI をインストールした場合は、同じツールを使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="848e9-167">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="848e9-168">問題とフィードバックの報告</span><span class="sxs-lookup"><span data-stu-id="848e9-168">Reporting issues and feedback</span></span>

<span data-ttu-id="848e9-169">ツールにバグを発見した場合は、GitHub リポジトリの [[Issues (問題)]](https://github.com/Azure/azure-cli/issues) セクションで問題を報告してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-169">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="848e9-170">コマンド ラインからフィードバックを送るには、`az feedback` コマンドを試してください。</span><span class="sxs-lookup"><span data-stu-id="848e9-170">To provide feedback from the command line, try the `az feedback` command.</span></span>
