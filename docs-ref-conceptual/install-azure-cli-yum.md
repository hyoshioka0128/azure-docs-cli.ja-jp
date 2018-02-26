---
title: "yum を使用して Linux に Azure CLI 2.0 をインストールする"
description: "yum で Azure CLI 2.0 をインストールする方法"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5b7afe999d1afe5be40c4957d9cd0f832b680099
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2018
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="6ab21-103">yum での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="6ab21-103">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="6ab21-104">RHEL、Fedora、CentOS など、`yum` が付属するディストリビューションを実行している場合は、Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="6ab21-104">If you are running a distribution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="6ab21-105">このパッケージは、RHEL 7、Fedora 19 以降、CentOS 7 でテストされています。</span><span class="sxs-lookup"><span data-stu-id="6ab21-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="6ab21-106">Install</span><span class="sxs-lookup"><span data-stu-id="6ab21-106">Install</span></span>

1. <span data-ttu-id="6ab21-107">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="6ab21-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="6ab21-108">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="6ab21-109">`yum install` コマンドを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="6ab21-109">Install with the `yum install` command.</span></span> 

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="6ab21-110">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-110">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="6ab21-111">プライマリの</span><span class="sxs-lookup"><span data-stu-id="6ab21-111">Update</span></span>

<span data-ttu-id="6ab21-112">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-112">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="6ab21-113">アンインストール</span><span class="sxs-lookup"><span data-stu-id="6ab21-113">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="6ab21-114">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-114">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="6ab21-115">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-115">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="6ab21-116">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="6ab21-116">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
