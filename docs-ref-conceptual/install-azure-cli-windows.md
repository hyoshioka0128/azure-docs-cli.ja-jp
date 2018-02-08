---
title: "Windows での Azure CLI のインストール"
description: "Windows で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure インストール windows, azure cli windows, azure windows"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: fc84b80e44a994495ef97cf9d7ec4e4a79a5c5b3
ms.sourcegitcommit: b41c5ed4a26c771a1a32b4560131f7a65b80fd33
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2018
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="04c3e-104">Windows での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="04c3e-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="04c3e-105">Windows では、MSI を使用して Azure CLI バイナリがインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="04c3e-105">On Windows the Azure CLI binary is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="04c3e-106">Windows Subsystem for Linux (WSL) を実行している場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="04c3e-106">If you are running Windows Subsystem for Linux (WSL), there are packages available for your Linux distribution.</span></span> <span data-ttu-id="04c3e-107">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04c3e-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="04c3e-108">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="04c3e-108">Install or update</span></span>

<span data-ttu-id="04c3e-109">再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="04c3e-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="04c3e-110">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="04c3e-110">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)

<span data-ttu-id="04c3e-111">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04c3e-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="04c3e-112">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="04c3e-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="04c3e-113">PowerShell は、CMD からは利用できないタブ補完機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="04c3e-113">PowerShell offers some tab completion features not available from CMD.</span></span>

## <a name="uninstall"></a><span data-ttu-id="04c3e-114">アンインストール</span><span class="sxs-lookup"><span data-stu-id="04c3e-114">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="04c3e-115">アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="04c3e-115">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> 

> [!div class="nextstepaction"]
> [<span data-ttu-id="04c3e-116">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="04c3e-116">Download the MSI installer</span></span>](https://azurecliprod.blob.core.windows.net/msi/azure-cli-latest.msi)
