---
title: Windows での Azure CLI のインストール
description: Windows で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 30b9621c82af259e3de762127fd20b31eb249234
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2018
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="58825-103">Windows での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="58825-103">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="58825-104">Windows では、MSI を使用して Azure CLI バイナリがインストールされるので、Windows コマンド プロンプト (CMD) または PowerShell から CLI にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="58825-104">On Windows the Azure CLI binary is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="58825-105">Windows Subsystem for Linux (WSL) を実行している場合は、お使いの Linux ディストリビューションで使用できるパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="58825-105">If you are running Windows Subsystem for Linux (WSL), there are packages available for your Linux distribution.</span></span> <span data-ttu-id="58825-106">サポートされているパッケージ マネージャーの一覧または WSL での手動インストール方法については、[メインのインストール ページ](install-azure-cli.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58825-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="58825-107">インストールまたは更新</span><span class="sxs-lookup"><span data-stu-id="58825-107">Install or update</span></span>

<span data-ttu-id="58825-108">再頒布可能 MSI は、Windows での `az` コマンドのインストール、更新、およびアンインストールに使用されます。</span><span class="sxs-lookup"><span data-stu-id="58825-108">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="58825-109">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="58825-109">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

<span data-ttu-id="58825-110">インストーラーによって、コンピューターに変更を加えるかどうかを尋ねるメッセージが表示されたら、[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="58825-110">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="58825-111">これで、Windows コマンド プロンプトまたは PowerShell のいずれかから、`az` コマンドで Azure CLI を実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="58825-111">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="58825-112">PowerShell では、Windows コマンド プロンプトでは利用できないタブ補完機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="58825-112">PowerShell offers some tab completion features not available from Windows Command Prompt.</span></span> <span data-ttu-id="58825-113">ログインするには、`az login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="58825-113">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="58825-114">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58825-114">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="uninstall"></a><span data-ttu-id="58825-115">アンインストール</span><span class="sxs-lookup"><span data-stu-id="58825-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="58825-116">アンインストールするには、MSI をもう一度実行して、"アンインストール" オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="58825-116">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="58825-117">MSI インストーラーのダウンロード</span><span class="sxs-lookup"><span data-stu-id="58825-117">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)
