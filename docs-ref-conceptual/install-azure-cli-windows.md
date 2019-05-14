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
ms.openlocfilehash: c5c499800e49dcdc536337e7655ec1ee280d48f2
ms.sourcegitcommit: 65bf8561a6e047e4eab52186e066a2e8c21f1d40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "65240547"
---
# <a name="install-azure-cli-on-windows"></a><span data-ttu-id="45d21-103">Windows での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="45d21-103">Install Azure CLI on Windows</span></span>

<span data-ttu-id="45d21-104">Windows では、MSI を使用して Azure CLI がインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="45d21-104">For Windows the Azure CLI is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="45d21-105">Windows Subsystem for Linux (WSL) 用にインストールする場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="45d21-105">When installing for Windows Subsystem for Linux (WSL), packages are available for your Linux distribution.</span></span> <span data-ttu-id="45d21-106">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45d21-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

## <a name="install-or-update"></a><span data-ttu-id="45d21-107">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="45d21-107">Install or update</span></span>

<span data-ttu-id="45d21-108">再頒布可能 MSI は、Windows での Azure CLI のインストールまたは更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="45d21-108">The MSI distributable is used for installing or updating the Azure CLI on Windows.</span></span> <span data-ttu-id="45d21-109">MSI インストーラーの使用前に現在のバージョンをアンインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="45d21-109">You don't need to uninstall any current versions before using the MSI installer.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="45d21-110">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="45d21-110">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

<span data-ttu-id="45d21-111">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45d21-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="45d21-112">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="45d21-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="45d21-113">PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="45d21-113">PowerShell offers some tab completion features not available from Windows Command Prompt.</span></span> <span data-ttu-id="45d21-114">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="45d21-114">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="45d21-115">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45d21-115">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="uninstall"></a><span data-ttu-id="45d21-116">アンインストール</span><span class="sxs-lookup"><span data-stu-id="45d21-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="45d21-117">Windows の "アプリと機能" の一覧から Azure CLI をアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="45d21-117">You uninstall the Azure CLI from the Windows "Apps and Features" list.</span></span> <span data-ttu-id="45d21-118">アンインストールするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="45d21-118">To uninstall:</span></span>

| <span data-ttu-id="45d21-119">プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="45d21-119">Platform</span></span> | <span data-ttu-id="45d21-120">Instructions</span><span class="sxs-lookup"><span data-stu-id="45d21-120">Instructions</span></span> |
|---|---|
| <span data-ttu-id="45d21-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="45d21-121">Windows 10</span></span> | <span data-ttu-id="45d21-122">[スタート] > [設定] > [アプリ]</span><span class="sxs-lookup"><span data-stu-id="45d21-122">Start > Settings > Apps</span></span> |
| <span data-ttu-id="45d21-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="45d21-123">Windows 8</span></span><br/><span data-ttu-id="45d21-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45d21-124">Windows 7</span></span> | <span data-ttu-id="45d21-125">[スタート] > [コントロール パネル] > [プログラム] > [プログラムのアンインストール]</span><span class="sxs-lookup"><span data-stu-id="45d21-125">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="45d21-126">この画面に移動したら、プログラムの検索バーに "__Azure CLI__" と入力します。</span><span class="sxs-lookup"><span data-stu-id="45d21-126">Once on this screen type __Azure CLI__ into the program search bar.</span></span> <span data-ttu-id="45d21-127">アンインストールするプログラムが "__Microsoft CLI 2.0 for Azure__" として一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="45d21-127">The program to uninstall is listed as __Microsoft CLI 2.0 for Azure__.</span></span> <span data-ttu-id="45d21-128">このアプリケーションを選択し、`Uninstall` ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="45d21-128">Select this application, then click the `Uninstall` button.</span></span>

## <a name="next-steps"></a><span data-ttu-id="45d21-129">次の手順</span><span class="sxs-lookup"><span data-stu-id="45d21-129">Next Steps</span></span>

<span data-ttu-id="45d21-130">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="45d21-130">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="45d21-131">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="45d21-131">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
