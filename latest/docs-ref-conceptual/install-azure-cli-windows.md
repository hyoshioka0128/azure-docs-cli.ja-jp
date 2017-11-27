---
title: "Windows での Azure CLI のインストール"
description: "Windows で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure インストール windows, azure cli windows, azure windows"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 96a123575226f281accf125cb5bb29ee7d14ef2a
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="1cdd5-104">Windows での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="1cdd5-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="1cdd5-105">Windows では、MSI からネイティブ バイナリをインストールできます。これは、Windows コマンド プロンプトまたは PowerShell から使用できます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-105">On Windows, you can install a native binary from an MSI, which you can use through the Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="1cdd5-106">Windows Subsystem for Linux (WSL) を使用している場合は、実行しているディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-106">If you are running Windows Subsystem for Linux (WSL) there are packages available for the distribution you are running.</span></span> <span data-ttu-id="1cdd5-107">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update-with-msi"></a><span data-ttu-id="1cdd5-108">MSI でのインストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="1cdd5-108">Install or update with MSI</span></span>

<span data-ttu-id="1cdd5-109">再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span> <span data-ttu-id="1cdd5-110">[MSI インストーラーをダウンロード](https://aka.ms/InstallAzureCliWindows)して実行し、インストールまたは更新できます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-110">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) and then run it to install or update.</span></span>

<span data-ttu-id="1cdd5-111">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="1cdd5-112">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span>

## <a name="uninstall-with-msi"></a><span data-ttu-id="1cdd5-113">MSI でのアンインストール</span><span class="sxs-lookup"><span data-stu-id="1cdd5-113">Uninstall with MSI</span></span>

<span data-ttu-id="1cdd5-114">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-114">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="1cdd5-115">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-115">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="1cdd5-116">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-116">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="1cdd5-117">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-117">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="1cdd5-118">アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-118">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> <span data-ttu-id="1cdd5-119">MSI インストーラーが使用できなくなっている場合は、[ダウンロード](https://aka.ms/InstallAzureCliWindows)できます。</span><span class="sxs-lookup"><span data-stu-id="1cdd5-119">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) if you no longer have it available.</span></span>
