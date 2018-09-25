---
title: yum を使用して Linux に Azure CLI 2.0 をインストールする
description: yum で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 25eb473aa56d3ddd34f8e1808b84ebb5f6324f2b
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2018
ms.locfileid: "46470016"
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="d58e3-103">yum での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="d58e3-103">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="d58e3-104">RHEL、Fedora、CentOS など、`yum` が付属する Linux ディストリビューションには、Azure CLI 用のパッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="d58e3-104">For Linux distributions with  `yum` such as RHEL, Fedora, or CentOS, there's a package for the Azure CLI.</span></span> <span data-ttu-id="d58e3-105">このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="d58e3-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="d58e3-106">Install</span><span class="sxs-lookup"><span data-stu-id="d58e3-106">Install</span></span>

1. <span data-ttu-id="d58e3-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d58e3-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="d58e3-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="d58e3-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="d58e3-109">Install with the `yum install` command.</span></span>

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="d58e3-110">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d58e3-110">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="d58e3-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="d58e3-112">さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d58e3-112">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="d58e3-113">アップデート</span><span class="sxs-lookup"><span data-stu-id="d58e3-113">Update</span></span>

<span data-ttu-id="d58e3-114">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="d58e3-115">アンインストール</span><span class="sxs-lookup"><span data-stu-id="d58e3-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="d58e3-116">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-116">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="d58e3-117">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-117">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="d58e3-118">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="d58e3-118">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

## <a name="next-steps"></a><span data-ttu-id="d58e3-119">次の手順</span><span class="sxs-lookup"><span data-stu-id="d58e3-119">Next Steps</span></span>

<span data-ttu-id="d58e3-120">これで Azure CLI をインストールできました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="d58e3-120">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d58e3-121">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="d58e3-121">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
