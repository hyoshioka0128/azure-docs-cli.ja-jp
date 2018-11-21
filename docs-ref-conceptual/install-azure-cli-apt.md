---
title: apt を使用して Linux に Azure CLI をインストールする
description: apt パッケージ マネージャーで Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 11/12/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 0d4311e88fec9903c1aab1410cc71328f896dc65
ms.sourcegitcommit: 728a050f13d3682122be4a8993596cc4185a45ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2018
ms.locfileid: "51680936"
---
# <a name="install-azure-cli-with-apt"></a><span data-ttu-id="37ed4-103">apt での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="37ed4-103">Install Azure CLI with apt</span></span>

<span data-ttu-id="37ed4-104">Ubuntu や Debian など、`apt` が付属するディストリビューションを実行している場合は、Azure CLI 用に 64 ビット パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="37ed4-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there's a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="37ed4-105">このパッケージは、以下でテストされています。</span><span class="sxs-lookup"><span data-stu-id="37ed4-105">This package has been tested with:</span></span>

* <span data-ttu-id="37ed4-106">Ubuntu trusty、xenial、artful、および bionic</span><span class="sxs-lookup"><span data-stu-id="37ed4-106">Ubuntu trusty, xenial, artful, and bionic</span></span>
* <span data-ttu-id="37ed4-107">Debian wheezy、jessie、および stretch</span><span class="sxs-lookup"><span data-stu-id="37ed4-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="37ed4-108">Install</span><span class="sxs-lookup"><span data-stu-id="37ed4-108">Install</span></span>

1. <div id="install-step-1"/><span data-ttu-id="37ed4-109">ソース リストを変更します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-109">Modify your sources list:</span></span>

    ```bash
    sudo apt-get install apt-transport-https lsb-release software-properties-common -y
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

2. <div id="signingKey"/><span data-ttu-id="37ed4-110">Microsoft の署名キーを取得します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-110">Get the Microsoft signing key:</span></span>

   ```bash
   sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
        --keyserver packages.microsoft.com \
        --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
   ```

3. <span data-ttu-id="37ed4-111">CLI をインストールします。</span><span class="sxs-lookup"><span data-stu-id="37ed4-111">Install the CLI:</span></span>

   ```bash
   sudo apt-get update
   sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > <span data-ttu-id="37ed4-112">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="37ed4-112">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="37ed4-113">署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-113">If you receive signing errors, make sure you have [the latest signing key](#signingKey).</span></span>

<span data-ttu-id="37ed4-114">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="37ed4-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="37ed4-115">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-115">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="37ed4-116">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-116">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="37ed4-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="37ed4-117">Troubleshooting</span></span>

<span data-ttu-id="37ed4-118">ここでは、`apt` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="37ed4-119">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-119">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-does-not-return-the-base-distribution-version"></a><span data-ttu-id="37ed4-120">lsb_release では、ベース ディストリビューション バージョンが返されません</span><span class="sxs-lookup"><span data-stu-id="37ed4-120">lsb_release does not return the base distribution version</span></span>

<span data-ttu-id="37ed4-121">Linux Mint など、Ubuntu や Debian から派生する一部のディストリビューションでは、正しいバージョン名が `lsb_release` から返されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="37ed4-121">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="37ed4-122">この値は、インストール プロセスで、インストールするパッケージを特定するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="37ed4-122">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="37ed4-123">ディストリビューションの派生元バージョンの名前がわかっている場合は、[インストール手順 1.](#install-step-1) で `AZ_REPO` 値を手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="37ed4-123">If you know the name of the version your distribution is derived from, you can set the `AZ_REPO` value manually in [install step 1](#install-step-1).</span></span> <span data-ttu-id="37ed4-124">それ以外の場合は、ご自身のディストリビューションについて、ベース ディストリビューション名を調べて、`AZ_REPO` を正しい値に設定する方法をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-124">Otherwise, look up information for your distribution on how to determine the base distribution name and set `AZ_REPO` to the correct value.</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="37ed4-125">"No dirmngr" で apt-key が失敗する</span><span class="sxs-lookup"><span data-stu-id="37ed4-125">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="37ed4-126">`apt-key` コマンドの実行時に、次のようなエラーが出力されることがあります。</span><span class="sxs-lookup"><span data-stu-id="37ed4-126">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="37ed4-127">このエラーは、`apt-key` に必要なコンポーネントがないためです。</span><span class="sxs-lookup"><span data-stu-id="37ed4-127">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="37ed4-128">これを解決するには、`dirmngr` パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="37ed4-128">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a><span data-ttu-id="37ed4-129">apt-key がハングする</span><span class="sxs-lookup"><span data-stu-id="37ed4-129">apt-key hangs</span></span>

<span data-ttu-id="37ed4-130">ファイアウォールの内側でポート 11371 への発信接続がブロックされている場合、`apt-key` コマンドが無期限にハングすることがあります。</span><span class="sxs-lookup"><span data-stu-id="37ed4-130">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span>
<span data-ttu-id="37ed4-131">ご使用のファイアウォールでは、発信接続用に HTTP プロキシが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="37ed4-131">Your firewall may require an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key --keyring /etc/apt/trusted.gpg.d/Microsoft.gpg adv \
    --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ \
    --keyserver packages.microsoft.com \
    --recv-keys BC528686B50D79E339D3721CEB3E94ADBE1229CF
```

<span data-ttu-id="37ed4-132">プロキシがあるかどうかを確認するには、システム管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-132">To determine if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="37ed4-133">プロキシでログインが不要な場合は、ユーザーとパスワードの情報を指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-133">If your proxy does not require a login, then leave out the user and password information.</span></span>

## <a name="update"></a><span data-ttu-id="37ed4-134">アップデート</span><span class="sxs-lookup"><span data-stu-id="37ed4-134">Update</span></span>

<span data-ttu-id="37ed4-135">CLI パッケージを更新するには、`apt-get upgrade` を使用します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-135">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> <span data-ttu-id="37ed4-136">署名キーは 2018 年 5 月に更新され、置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="37ed4-136">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="37ed4-137">署名のエラーが発生した場合は、[最新の署名キー](#signingKey)を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="37ed4-137">If you receive signing errors, make sure you have [the latest signing key](#signingKey).</span></span>
>
> [!NOTE]
> <span data-ttu-id="37ed4-138">このコマンドにより、システムにインストールされている、依存関係が変更されていないすべてのパッケージがアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="37ed4-138">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="37ed4-139">CLI だけをアップグレードするには、`apt-get install` を使用します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-139">To upgrade the CLI only, use `apt-get install`.</span></span>
> 
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="37ed4-140">アンインストール</span><span class="sxs-lookup"><span data-stu-id="37ed4-140">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="37ed4-141">`apt-get remove` を使用してアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="37ed4-141">Uninstall with `apt-get remove`:</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="37ed4-142">CLI を再インストールする予定がない場合は、Azure CLI リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-142">If you don't plan to reinstall the CLI, remove the Azure CLI repository information:</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="37ed4-143">署名キーを削除します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-143">Remove the signing key:</span></span>

    ```bash
    sudo rm /etc/apt/trusted.gpg.d/Microsoft.gpg
    ```

4. <span data-ttu-id="37ed4-144">不要なパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="37ed4-144">Remove any unneeded packages:</span></span>

   ```bash
   sudo apt autoremove
   ```

## <a name="next-steps"></a><span data-ttu-id="37ed4-145">次の手順</span><span class="sxs-lookup"><span data-stu-id="37ed4-145">Next Steps</span></span>

<span data-ttu-id="37ed4-146">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="37ed4-146">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="37ed4-147">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="37ed4-147">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)