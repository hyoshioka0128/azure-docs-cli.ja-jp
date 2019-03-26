---
title: apt を使用して Linux に Azure CLI をインストールする
description: apt パッケージ マネージャーで Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/19/2019
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: fa2e1db439b4836d7506409b3abcce74fb6e6695
ms.sourcegitcommit: 5864f72b9a6fbf82a4d98bf805b3a16a7da18556
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2019
ms.locfileid: "58343147"
---
# <a name="install-azure-cli-with-apt"></a><span data-ttu-id="e8700-103">apt での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="e8700-103">Install Azure CLI with apt</span></span>

<span data-ttu-id="e8700-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用に x86_64 パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e8700-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there's an x86_64 package available for the Azure CLI.</span></span> <span data-ttu-id="e8700-105">このパッケージは、以下でテストされています。</span><span class="sxs-lookup"><span data-stu-id="e8700-105">This package has been tested with:</span></span>

* <span data-ttu-id="e8700-106">Ubuntu trusty、xenial、artful、および bionic</span><span class="sxs-lookup"><span data-stu-id="e8700-106">Ubuntu trusty, xenial, artful, and bionic</span></span>
* <span data-ttu-id="e8700-107">Debian wheezy、jessie、および stretch</span><span class="sxs-lookup"><span data-stu-id="e8700-107">Debian wheezy, jessie, and stretch</span></span>

[!INCLUDE [current-version](includes/current-version.md)]

> [!NOTE]
>
> <span data-ttu-id="e8700-108">Azure CLI のパッケージによって独自の Python インタープリターがインストールされ、システム上の Python は使用されません。</span><span class="sxs-lookup"><span data-stu-id="e8700-108">The package for Azure CLI installs its own Python interpreter, and does not use the system Python.</span></span>

## <a name="install"></a><span data-ttu-id="e8700-109">Install</span><span class="sxs-lookup"><span data-stu-id="e8700-109">Install</span></span>

1. <span data-ttu-id="e8700-110">インストール プロセスに必要なパッケージを取得します。</span><span class="sxs-lookup"><span data-stu-id="e8700-110">Get packages needed for the install process:</span></span>

    ```bash
    sudo apt-get update
    sudo apt-get install curl apt-transport-https lsb-release gpg
    ```

2. <span data-ttu-id="e8700-111">Microsoft の署名キーをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8700-111">Download and install the Microsoft signing key:</span></span>

    ```bash
    curl -sL https://packages.microsoft.com/keys/microsoft.asc | \
        gpg --dearmor | \
        sudo tee /etc/apt/trusted.gpg.d/microsoft.asc.gpg > /dev/null
    ```

3. <div id="set-release"/><span data-ttu-id="e8700-112">Azure CLI  ソフトウェア リポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="e8700-112">Add the Azure CLI software repository:</span></span>

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

4. <span data-ttu-id="e8700-113">リポジトリ情報を更新し、`azure-cli` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8700-113">Update repository information and install the `azure-cli` package:</span></span>

    ```bash
    sudo apt-get update
    sudo apt-get install azure-cli
    ```

<span data-ttu-id="e8700-114">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8700-114">Run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="e8700-115">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8700-115">To sign in, use the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="e8700-116">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8700-116">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e8700-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e8700-117">Troubleshooting</span></span>

<span data-ttu-id="e8700-118">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="e8700-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="e8700-119">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="e8700-119">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-does-not-return-the-correct-base-distribution-version"></a><span data-ttu-id="e8700-120">lsb_release がベース ディストリビューション バージョンを返さない</span><span class="sxs-lookup"><span data-stu-id="e8700-120">lsb_release does not return the correct base distribution version</span></span>

<span data-ttu-id="e8700-121">Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e8700-121">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="e8700-122">この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e8700-122">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="e8700-123">ディストリビューションの派生元である Ubuntu バージョンまたは Debian バージョンのコード名がわかっている場合は、[リポジトリを追加する](#set-release)ときに `AZ_REPO` 値を手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="e8700-123">If you know the code name of the Ubuntu or Debian version your distribution is derived from, you can set the `AZ_REPO` value manually when [adding the repository](#set-release).</span></span> <span data-ttu-id="e8700-124">それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューションのコード名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="e8700-124">Otherwise, look up information for your distribution on how to determine the base distribution code name and set `AZ_REPO` to the correct value.</span></span>

### <a name="no-package-for-your-distribution"></a><span data-ttu-id="e8700-125">ご使用のディストリビューションのパッケージがない</span><span class="sxs-lookup"><span data-stu-id="e8700-125">No package for your distribution</span></span>

<span data-ttu-id="e8700-126">ディストリビューションがリリースされてから、そのディストリビューション用の Azure CLI パッケージが利用可能になるまではしばらくかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="e8700-126">Sometimes it may be a while after a distribution is released before there's an Azure CLI package available for it.</span></span> <span data-ttu-id="e8700-127">Azure CLI は、以降のバージョンの依存関係に関して弾力性を持つように、また可能な限り以降のバージョンに依存しないように設計されています。</span><span class="sxs-lookup"><span data-stu-id="e8700-127">The Azure CLI designed to be resilient with regards to future versions of dependencies and rely on as few of them as possible.</span></span> <span data-ttu-id="e8700-128">ベース ディストリビューションに使用できるパッケージがない場合は、以前のディストリビューション用のパッケージをお試しください。</span><span class="sxs-lookup"><span data-stu-id="e8700-128">If there's no package available for your base distribution, try a package for an earlier distribution.</span></span>

<span data-ttu-id="e8700-129">これを行うには、[リポジトリを追加する](#set-release)ときに `AZ_REPO` の値を手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="e8700-129">To do this, set the value of `AZ_REPO` manually when [adding the repository](#set-release).</span></span> <span data-ttu-id="e8700-130">Ubuntu ディストリビューションには `bionic` リポジトリーを使用し、Debian ディストリビューションには `stretch` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8700-130">For Ubuntu distributions use the `bionic` repository, and for Debian distributions use `stretch`.</span></span> <span data-ttu-id="e8700-131">Ubuntu Trusty および Debian Wheezy より前にリリースされたディストリビューションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e8700-131">Distributions released before Ubuntu Trusty and Debian Wheezy are not supported.</span></span>

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="e8700-132">アップデート</span><span class="sxs-lookup"><span data-stu-id="e8700-132">Update</span></span>

<span data-ttu-id="e8700-133">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8700-133">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="e8700-134">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="e8700-134">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="e8700-135">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8700-135">To upgrade the CLI only, use `apt-get install`.</span></span>
> 
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="e8700-136">アンインストール</span><span class="sxs-lookup"><span data-stu-id="e8700-136">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="e8700-137">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="e8700-137">Uninstall with `apt-get remove`:</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="e8700-138">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="e8700-138">If you don't plan to reinstall the CLI, remove the Azure CLI repository information:</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="e8700-139">署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="e8700-139">Remove the signing key:</span></span>

    ```bash
    sudo rm /etc/apt/trusted.gpg.d/microsoft.asc.gpg
    ```

4. <span data-ttu-id="e8700-140">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="e8700-140">Remove any unneeded packages:</span></span>

   ```bash
   sudo apt autoremove
   ```

## <a name="next-steps"></a><span data-ttu-id="e8700-141">次の手順</span><span class="sxs-lookup"><span data-stu-id="e8700-141">Next Steps</span></span>

<span data-ttu-id="e8700-142">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="e8700-142">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e8700-143">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="e8700-143">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
