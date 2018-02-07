---
title: "apt を使用して Linux に Azure CLI 2.0 をインストールする"
description: "apt パッケージ マネージャーで Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure apt, azure debian, azure ubuntu"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: fdd9f0061d5d38ed5a349b11eb0f5f27786bc1ab
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="868c2-104">apt での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="868c2-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="868c2-105">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="868c2-105">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="868c2-106">このパッケージは、Ubuntu Wheezy と Ubuntu Xenial でテストされています。</span><span class="sxs-lookup"><span data-stu-id="868c2-106">This package has been tested with Ubuntu Wheezy and Ubuntu Xenial.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="868c2-107">[インストール]</span><span class="sxs-lookup"><span data-stu-id="868c2-107">Install</span></span>

1. <span data-ttu-id="868c2-108">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="868c2-108">Modify your sources list:</span></span>

   - <span data-ttu-id="868c2-109">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="868c2-109">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="868c2-110">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="868c2-110">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="868c2-111">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="868c2-111">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="868c2-112">Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="868c2-112">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="868c2-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="868c2-113">Troubleshooting</span></span>

<span data-ttu-id="868c2-114">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="868c2-114">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="868c2-115">問題がここに示されていない場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="868c2-115">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="868c2-116">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="868c2-116">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="868c2-117">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="868c2-117">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="868c2-118">このエラーは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="868c2-118">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="868c2-119">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="868c2-119">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="868c2-120">プライマリの</span><span class="sxs-lookup"><span data-stu-id="868c2-120">Update</span></span>

<span data-ttu-id="868c2-121">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="868c2-121">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="868c2-122">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="868c2-122">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="868c2-123">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="868c2-123">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="868c2-124">アンインストール</span><span class="sxs-lookup"><span data-stu-id="868c2-124">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="868c2-125">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="868c2-125">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="868c2-126">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="868c2-126">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="868c2-127">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="868c2-127">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
