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
ms.openlocfilehash: 65e8e78275b0f40a2298934fe8bc9368bbf796a7
ms.sourcegitcommit: 59f0b667f2202bae8914e6fc8dc5c9dc79fef91c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="a7894-104">apt での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="a7894-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="a7894-105">Ubuntu、Debian など、`apt` に付属するディストリビューションを実行している場合は、システムにインストールできる Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="a7894-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="a7894-106">[インストール]</span><span class="sxs-lookup"><span data-stu-id="a7894-106">Install</span></span>

1. <span data-ttu-id="a7894-107">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="a7894-107">Modify your sources list:</span></span>

   - <span data-ttu-id="a7894-108">32 ビット システム</span><span class="sxs-lookup"><span data-stu-id="a7894-108">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="a7894-109">64 ビット システム</span><span class="sxs-lookup"><span data-stu-id="a7894-109">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="a7894-110">次の sudo コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a7894-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="a7894-111">Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="a7894-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a7894-112">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a7894-112">Troubleshooting</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="a7894-113">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="a7894-113">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="a7894-114">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a7894-114">When running the `apt-key` command, you may see output similar to the following error.</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="a7894-115">これは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="a7894-115">This is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="a7894-116">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a7894-116">You can resolve this by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="a7894-117">プライマリの</span><span class="sxs-lookup"><span data-stu-id="a7894-117">Update</span></span>

<span data-ttu-id="a7894-118">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a7894-118">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="a7894-119">これにより、依存関係が変更されていない、システム上のすべてのインストール済みパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="a7894-119">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="a7894-120">CLI のみをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="a7894-120">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="a7894-121">アンインストール</span><span class="sxs-lookup"><span data-stu-id="a7894-121">Uninstall</span></span>

<span data-ttu-id="a7894-122">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="a7894-122">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="a7894-123">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="a7894-123">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="a7894-124">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="a7894-124">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="a7894-125">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="a7894-125">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="a7894-126">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="a7894-126">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="a7894-127">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="a7894-127">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="a7894-128">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a7894-128">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
