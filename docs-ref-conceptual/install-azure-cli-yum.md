---
title: yum を使用して Linux に Azure CLI をインストールする
description: yum で Azure CLI をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: faa1855efe9651ee104880740338c30e7dd84810
ms.sourcegitcommit: f40bd067ece4e6ec13e259782ed8db3e33b61a75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/18/2018
ms.locfileid: "53593236"
---
# <a name="install-azure-cli-with-yum"></a><span data-ttu-id="febb2-103">yum での Azure CLI のインストール</span><span class="sxs-lookup"><span data-stu-id="febb2-103">Install Azure CLI with yum</span></span>

<span data-ttu-id="febb2-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="febb2-104">For Linux distributions with  `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="febb2-105">このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="febb2-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="febb2-106">Install</span><span class="sxs-lookup"><span data-stu-id="febb2-106">Install</span></span>

1. <span data-ttu-id="febb2-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="febb2-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="febb2-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="febb2-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="febb2-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="febb2-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="febb2-110">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="febb2-110">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="febb2-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="febb2-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="febb2-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="febb2-112">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="febb2-113">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="febb2-113">Troubleshooting</span></span>

<span data-ttu-id="febb2-114">ここでは、`yum` でのインストール時に発生する一般的な問題をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="febb2-114">Here are some common problems seen when installing with `yum`.</span></span> <span data-ttu-id="febb2-115">ここで取り上げていない問題が発生した場合は、[GitHub で問題を報告](https://github.com/Azure/azure-cli/issues)してください。</span><span class="sxs-lookup"><span data-stu-id="febb2-115">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

[!INCLUDE[troubleshoot-wsl.md](includes/troubleshoot-wsl.md)]

## <a name="update"></a><span data-ttu-id="febb2-116">アップデート</span><span class="sxs-lookup"><span data-stu-id="febb2-116">Update</span></span>

<span data-ttu-id="febb2-117">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="febb2-117">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="febb2-118">アンインストール</span><span class="sxs-lookup"><span data-stu-id="febb2-118">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="febb2-119">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="febb2-119">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="febb2-120">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="febb2-120">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="febb2-121">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="febb2-121">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

   ```bash
   MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
   sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
   ```

## <a name="next-steps"></a><span data-ttu-id="febb2-122">次の手順</span><span class="sxs-lookup"><span data-stu-id="febb2-122">Next Steps</span></span>

<span data-ttu-id="febb2-123">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="febb2-123">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="febb2-124">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="febb2-124">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
