---
title: "apt を使用して Linux に Azure CLI 2.0 をインストールする"
description: "apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/06/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 840e5e7d6531fe92d30235f621e381589266d1d3
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="e155e-103">apt での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="e155e-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="e155e-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能な 64 ビット パッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="e155e-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="e155e-105">このパッケージは、以下でテストされています。</span><span class="sxs-lookup"><span data-stu-id="e155e-105">This package has been tested with:</span></span>

* <span data-ttu-id="e155e-106">Ubuntu trusty、xenial、および artful</span><span class="sxs-lookup"><span data-stu-id="e155e-106">Ubuntu trusty, xenial, and artful</span></span>
* <span data-ttu-id="e155e-107">Debian wheezy、jessie、および stretch</span><span class="sxs-lookup"><span data-stu-id="e155e-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="e155e-108">Install</span><span class="sxs-lookup"><span data-stu-id="e155e-108">Install</span></span>

1. <span data-ttu-id="e155e-109">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="e155e-109">Modify your sources list:</span></span>

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="e155e-110">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="e155e-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="e155e-111">Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e155e-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e155e-112">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e155e-112">Troubleshooting</span></span>

<span data-ttu-id="e155e-113">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="e155e-113">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="e155e-114">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="e155e-114">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="e155e-115">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="e155e-115">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="e155e-116">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="e155e-116">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="e155e-117">このエラーは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="e155e-117">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="e155e-118">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="e155e-118">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="e155e-119">プライマリの</span><span class="sxs-lookup"><span data-stu-id="e155e-119">Update</span></span>

<span data-ttu-id="e155e-120">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e155e-120">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="e155e-121">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="e155e-121">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="e155e-122">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="e155e-122">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="e155e-123">アンインストール</span><span class="sxs-lookup"><span data-stu-id="e155e-123">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="e155e-124">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="e155e-124">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="e155e-125">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="e155e-125">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="e155e-126">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="e155e-126">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
