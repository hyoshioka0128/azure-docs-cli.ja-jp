---
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/26/2018
ms.topic: include
ms.openlocfilehash: ee0b2b0c8c557aa54255f28429bb3a174c0e21a9
ms.sourcegitcommit: a8aac038e6ede0b1b352ca6163a04b61ff4eed5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/28/2018
ms.locfileid: "52450345"
---
### <a name="cli-fails-to-install-or-run-on-windows-subsystem-for-linux"></a><span data-ttu-id="637c5-101">Windows Subsystem for Linux で CLI をインストールまたは実行できない</span><span class="sxs-lookup"><span data-stu-id="637c5-101">CLI fails to install or run on Windows Subsystem for Linux</span></span>

<span data-ttu-id="637c5-102">[Windows Subsystem for Linux (WSL)](/windows/wsl/about) は Windows プラットフォームを基盤とするシステム呼び出し変換レイヤーであるため、Azure CLI をインストールまたは実行しようとするとエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="637c5-102">Since [Windows Subsystem for Linux (WSL)](/windows/wsl/about) is a system call translation layer on top of the Windows platform, you might experience an error when trying to install or run the Azure CLI.</span></span> <span data-ttu-id="637c5-103">CLI は、WSL にバグが含まれる可能性のあるいくつかの機能に依存しています。</span><span class="sxs-lookup"><span data-stu-id="637c5-103">The CLI relies on some features that may have a bug in WSL.</span></span> <span data-ttu-id="637c5-104">どのように CLI をインストールしてもエラーが発生する場合は、CLI のインストール プロセスではなく WSL に問題があると考えられます。</span><span class="sxs-lookup"><span data-stu-id="637c5-104">If you experience an error no matter how you install the CLI, there's a good chance it's an issue with WSL and not with the CLI install process.</span></span>

<span data-ttu-id="637c5-105">WSL インストールのトラブルシューティングを行い、問題を解決するには、以下を行ってください。</span><span class="sxs-lookup"><span data-stu-id="637c5-105">To troubleshoot your WSL installation and possibly resolve issues:</span></span>

* <span data-ttu-id="637c5-106">可能であれば、同じインストール プロセスを Linux マシンまたは VM で実行し、正常にインストールできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="637c5-106">If you can, run an identical install process on a Linux machine or VM to see if it succeeds.</span></span> <span data-ttu-id="637c5-107">インストールできる場合、問題はほぼ間違いなく WSL に関連するものです。</span><span class="sxs-lookup"><span data-stu-id="637c5-107">If it does, your issue is almost certainly related to WSL.</span></span> <span data-ttu-id="637c5-108">Azure で Linux VM を開始するには、[Azure portal での Linux 仮想マシンの作成](/azure/virtual-machines/linux/quick-create-portal)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="637c5-108">To start a Linux VM in Azure, see the [create a Linux VM in the Azure Portal](/azure/virtual-machines/linux/quick-create-portal) documentation.</span></span>
* <span data-ttu-id="637c5-109">最新バージョンの WSL を実行していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="637c5-109">Make sure that you're running the latest version of WSL.</span></span> <span data-ttu-id="637c5-110">最新バージョンを入手するには、[Windows 10 インストールを更新](https://support.microsoft.com/help/4027667/windows-10-update)してください。</span><span class="sxs-lookup"><span data-stu-id="637c5-110">To get the latest version, [update your Windows 10 installation](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
* <span data-ttu-id="637c5-111">現在の問題に対処している、WSL 関連の[未解決案件](https://github.com/Microsoft/WSL/issues)がないか確認します。</span><span class="sxs-lookup"><span data-stu-id="637c5-111">Check for any [open issues](https://github.com/Microsoft/WSL/issues) with WSL which might address your problem.</span></span>
  <span data-ttu-id="637c5-112">この問題を回避する方法についての提案や、問題が修正される予定のリリースに関する情報が掲載されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="637c5-112">Often there will be suggestions on how to work around the problem, or information about a release where the issue will be fixed.</span></span>
* <span data-ttu-id="637c5-113">現在の問題に関する案件がまだない場合は、[WSL に関する新規案件を提出](https://github.com/Microsoft/WSL/issues/new)します。その際は、必ず、可能な限り多くの情報を提供してください。</span><span class="sxs-lookup"><span data-stu-id="637c5-113">If there are no existing issues for your problem, [file a new issue with WSL](https://github.com/Microsoft/WSL/issues/new) and make sure that you include as much information as possible.</span></span>

<span data-ttu-id="637c5-114">引き続き WSL でのインストールまたは実行の問題が発生する場合は、[Windows 用の CLI のインストール](../install-azure-cli-windows.md)を検討してください。</span><span class="sxs-lookup"><span data-stu-id="637c5-114">If you continue to have issues installing or running on WSL, consider [installing the CLI for Windows](../install-azure-cli-windows.md).</span></span>
