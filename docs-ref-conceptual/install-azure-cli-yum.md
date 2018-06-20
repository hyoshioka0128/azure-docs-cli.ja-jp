---
title: yum を使用して Linux に Azure CLI 2.0 をインストールする
description: yum で Azure CLI 2.0 をインストールする方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: b3c82825af3d1d2420b0111d1a370a17f37d9426
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2018
ms.locfileid: "32043705"
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="ef017-103">yum での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="ef017-103">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="ef017-104">RHEL、Fedora、CentOS など、`yum` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="ef017-104">If you are running a distribution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="ef017-105">このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="ef017-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="ef017-106">Install</span><span class="sxs-lookup"><span data-stu-id="ef017-106">Install</span></span>

1. <span data-ttu-id="ef017-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ef017-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="ef017-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="ef017-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="ef017-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="ef017-109">Install with the `yum install` command.</span></span> 

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="ef017-110">その後、Azure CLI は `az` コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ef017-110">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="ef017-111">ログインするには、`az login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ef017-111">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="ef017-112">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef017-112">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="ef017-113">アップデート</span><span class="sxs-lookup"><span data-stu-id="ef017-113">Update</span></span>

<span data-ttu-id="ef017-114">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="ef017-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="ef017-115">アンインストール</span><span class="sxs-lookup"><span data-stu-id="ef017-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="ef017-116">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ef017-116">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="ef017-117">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="ef017-117">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="ef017-118">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="ef017-118">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
