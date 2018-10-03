---
title: Windows での Azure CLI のインストール
description: Windows で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: c65cff52211b4c77e32c2992cd71392c8b0e44d6
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177965"
---
# <a name="install-azure-cli-on-windows"></a><span data-ttu-id="130cb-103">Windows での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="130cb-103">Install Azure CLI on Windows</span></span>

<span data-ttu-id="130cb-104">Windows では、MSI を使用して Azure CLI がインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="130cb-104">For Windows the Azure CLI is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="130cb-105">Windows Subsystem for Linux (WSL) 用にインストールする場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="130cb-105">When installing for Windows Subsystem for Linux (WSL), packages are available for your Linux distribution.</span></span> <span data-ttu-id="130cb-106">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="130cb-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="130cb-107">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="130cb-107">Install or update</span></span>

<span data-ttu-id="130cb-108">再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="130cb-108">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="130cb-109">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="130cb-109">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

<span data-ttu-id="130cb-110">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="130cb-110">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="130cb-111">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="130cb-111">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="130cb-112">PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="130cb-112">PowerShell offers some tab completion features not available from Windows Command Prompt.</span></span> <span data-ttu-id="130cb-113">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="130cb-113">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="130cb-114">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="130cb-114">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="uninstall"></a><span data-ttu-id="130cb-115">アンインストール</span><span class="sxs-lookup"><span data-stu-id="130cb-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="130cb-116">アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="130cb-116">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="130cb-117">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="130cb-117">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

## <a name="next-steps"></a><span data-ttu-id="130cb-118">次の手順</span><span class="sxs-lookup"><span data-stu-id="130cb-118">Next Steps</span></span>

<span data-ttu-id="130cb-119">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="130cb-119">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="130cb-120">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="130cb-120">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
