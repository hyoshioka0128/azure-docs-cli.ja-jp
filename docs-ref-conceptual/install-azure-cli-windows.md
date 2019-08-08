---
title: Windows での Azure CLI のインストール
description: Windows で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/01/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 6c972ba69344f9e8bcd14a96a90e9dadb6cd8132
ms.sourcegitcommit: 61965f5d95d0dae3752ad6a0e5a93db27a623c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "68830961"
---
# <a name="install-azure-cli-on-windows"></a><span data-ttu-id="52e0a-103">Windows での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="52e0a-103">Install Azure CLI on Windows</span></span>

<span data-ttu-id="52e0a-104">Windows では、MSI を使用して Azure CLI がインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-104">For Windows the Azure CLI is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="52e0a-105">Windows Subsystem for Linux (WSL) 用にインストールする場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="52e0a-105">When installing for Windows Subsystem for Linux (WSL), packages are available for your Linux distribution.</span></span> <span data-ttu-id="52e0a-106">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52e0a-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

## <a name="install-or-update"></a><span data-ttu-id="52e0a-107">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="52e0a-107">Install or update</span></span>

<span data-ttu-id="52e0a-108">再頒布可能 MSI は、Windows での Azure CLI のインストールまたは更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-108">The MSI distributable is used for installing or updating the Azure CLI on Windows.</span></span> <span data-ttu-id="52e0a-109">MSI インストーラーの使用前に現在のバージョンをアンインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="52e0a-109">You don't need to uninstall any current versions before using the MSI installer.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="52e0a-110">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="52e0a-110">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

<span data-ttu-id="52e0a-111">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52e0a-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="52e0a-112">Azure CLI は PowerShell を使用してインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-112">You can also install the Azure CLI using PowerShell.</span></span> <span data-ttu-id="52e0a-113">管理者として PowerShell を開始し、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-113">Start PowerShell as administrator and run the following command:</span></span>

   ```PowerShell
   Invoke-WebRequest -Uri https://aka.ms/installazurecliwindows -OutFile .\AzureCLI.msi; Start-Process msiexec.exe -Wait -ArgumentList '/I AzureCLI.msi /quiet'
   ```
<span data-ttu-id="52e0a-114">これにより、最新バージョンの Windows 用 Azure CLI がダウンロードされインストールされます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-114">This will download and install the latest version of the Azure CLI for Windows.</span></span> <span data-ttu-id="52e0a-115">既にインストールされているバージョンがある場合、既存のバージョンが更新されます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-115">If you already have a version installed, it will update the existing version.</span></span> <span data-ttu-id="52e0a-116">インストールが完了したら、Azure CLI を使用するには PowerShell を再度開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="52e0a-116">After the installation is complete, you will need to reopen PowerShell to use the Azure CLI.</span></span>

<span data-ttu-id="52e0a-117">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="52e0a-117">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="52e0a-118">PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-118">PowerShell offers some tab completion features not available from Windows Command Prompt.</span></span> <span data-ttu-id="52e0a-119">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-119">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="52e0a-120">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52e0a-120">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="52e0a-121">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="52e0a-121">Troubleshooting</span></span>

<span data-ttu-id="52e0a-122">ここでは、Windows でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-122">Here are some common problems seen when installing on Windows.</span></span> <span data-ttu-id="52e0a-123">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="52e0a-123">If you experience a problem not covered here, [file an issue on GitHub](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="52e0a-124">プロキシによる接続のブロック</span><span class="sxs-lookup"><span data-stu-id="52e0a-124">Proxy blocks connection</span></span>

<span data-ttu-id="52e0a-125">プロキシにより接続がブロックされているため MSI インストーラーをダウンロードできない場合、プロキシを正しく構成していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-125">If you can't download the MSI installer because your proxy is blocking the connection, make sure that you have your proxy properly configured.</span></span> <span data-ttu-id="52e0a-126">Windows 10 の場合、これらの設定は `Settings > Network & Internet > Proxy` ウィンドウで管理されます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-126">For Windows 10, these settings are managed in the `Settings > Network & Internet > Proxy` pane.</span></span> <span data-ttu-id="52e0a-127">必要な設定またはお使いのマシンの構成が管理されている状況や高度なセットアップが必要な状況については、システム管理者にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="52e0a-127">Contact your system administrator for the required settings, or for situations where your machine may be configuration-managed or require advanced setup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52e0a-128">また、これらの設定は、CLI を使用した Azure サービスに PowerShell またはコマンド プロンプトの両方からアクセスできるようにするためにも必要です。</span><span class="sxs-lookup"><span data-stu-id="52e0a-128">These settings are also required to be able to access Azure services with the CLI, from both PowerShell or the Command Prompt.</span></span> <span data-ttu-id="52e0a-129">これを行うには、PowerShell で次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-129">In PowerShell, you do this with the following command:</span></span>
>
> ```powershell
> (New-Object System.Net.WebClient).Proxy.Credentials = `
>   [System.Net.CredentialCache]::DefaultNetworkCredentials
> ```

<span data-ttu-id="52e0a-130">MSI を取得するには、プロキシで次のアドレスへの HTTPS 接続を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52e0a-130">In order to get the MSI, your proxy needs to allow HTTPS connections to the following addresses:</span></span>

* `https://aka.ms/`
* `https://azurecliprod.blob.core.windows.net/`

## <a name="uninstall"></a><span data-ttu-id="52e0a-131">アンインストール</span><span class="sxs-lookup"><span data-stu-id="52e0a-131">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="52e0a-132">Windows の "アプリと機能" の一覧から Azure CLI をアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="52e0a-132">You uninstall the Azure CLI from the Windows "Apps and Features" list.</span></span> <span data-ttu-id="52e0a-133">アンインストールするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="52e0a-133">To uninstall:</span></span>

| <span data-ttu-id="52e0a-134">プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="52e0a-134">Platform</span></span> | <span data-ttu-id="52e0a-135">Instructions</span><span class="sxs-lookup"><span data-stu-id="52e0a-135">Instructions</span></span> |
|---|---|
| <span data-ttu-id="52e0a-136">Windows 10</span><span class="sxs-lookup"><span data-stu-id="52e0a-136">Windows 10</span></span> | <span data-ttu-id="52e0a-137">[スタート] > [設定] > [アプリ]</span><span class="sxs-lookup"><span data-stu-id="52e0a-137">Start > Settings > Apps</span></span> |
| <span data-ttu-id="52e0a-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52e0a-138">Windows 8</span></span><br/><span data-ttu-id="52e0a-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52e0a-139">Windows 7</span></span> | <span data-ttu-id="52e0a-140">[スタート] > [コントロール パネル] > [プログラム] > [プログラムのアンインストール]</span><span class="sxs-lookup"><span data-stu-id="52e0a-140">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="52e0a-141">この画面に移動したら、プログラムの検索バーに "__Azure CLI__" と入力します。</span><span class="sxs-lookup"><span data-stu-id="52e0a-141">Once on this screen type __Azure CLI__ into the program search bar.</span></span> <span data-ttu-id="52e0a-142">アンインストールするプログラムが "__Microsoft CLI 2.0 for Azure__" として一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="52e0a-142">The program to uninstall is listed as __Microsoft CLI 2.0 for Azure__.</span></span> <span data-ttu-id="52e0a-143">このアプリケーションを選択し、`Uninstall` ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="52e0a-143">Select this application, then click the `Uninstall` button.</span></span>

## <a name="next-steps"></a><span data-ttu-id="52e0a-144">次の手順</span><span class="sxs-lookup"><span data-stu-id="52e0a-144">Next Steps</span></span>

<span data-ttu-id="52e0a-145">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="52e0a-145">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="52e0a-146">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="52e0a-146">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
