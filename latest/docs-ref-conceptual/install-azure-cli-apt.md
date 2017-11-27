---
title: "apt での Azure CLI 2.0 のインストール"
description: "apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure apt, azure debian, azure ubuntu"
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
ms.openlocfilehash: 93d947d91973def1c05e2f5b2e7511bc1c5704a2
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="ff272-104">apt での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="ff272-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="ff272-105">Ubuntu、Debian など、`apt` に付属するディストリビューションを実行している場合は、システムにインストールできる Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="ff272-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="ff272-106">CLI を使用するには、Python 2.7.x または Python 3.x が必要です。</span><span class="sxs-lookup"><span data-stu-id="ff272-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="ff272-107">ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。</span><span class="sxs-lookup"><span data-stu-id="ff272-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="ff272-108">インストール</span><span class="sxs-lookup"><span data-stu-id="ff272-108">Install</span></span>

1. <span data-ttu-id="ff272-109">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="ff272-109">Modify your sources list:</span></span>
 
   - <span data-ttu-id="ff272-110">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="ff272-110">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="ff272-111">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="ff272-111">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="ff272-112">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ff272-112">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="ff272-113">Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ff272-113">You can run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="ff272-114">更新</span><span class="sxs-lookup"><span data-stu-id="ff272-114">Update</span></span>

<span data-ttu-id="ff272-115">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff272-115">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="ff272-116">これにより、依存関係が変更されていない、システム上のすべてのインストール済みパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="ff272-116">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="ff272-117">CLI のみをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff272-117">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="ff272-118">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ff272-118">Uninstall</span></span>

<span data-ttu-id="ff272-119">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff272-119">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="ff272-120">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="ff272-120">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="ff272-121">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="ff272-121">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="ff272-122">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="ff272-122">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="ff272-123">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="ff272-123">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="ff272-124">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="ff272-124">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="ff272-125">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ff272-125">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
