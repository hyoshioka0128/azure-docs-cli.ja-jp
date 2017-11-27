---
title: "yum での Azure CLI 2.0 のインストール"
description: "yum で Azure CLI 2.0 をインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure yum,azure rhel, azure fedora, azure centos"
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
ms.openlocfilehash: de695454c6f3109679b9eb9f6c0d77348d354518
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="0c211-104">yum での Azure CLI 2.0 のインストール</span><span class="sxs-lookup"><span data-stu-id="0c211-104">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="0c211-105">RHEL、Fedora、CentOS など、`yum` に付属するディストリビューションを実行している場合は、システムにインストールできる Azure CLI 用の利用可能なパッケージがあります。</span><span class="sxs-lookup"><span data-stu-id="0c211-105">If you are running a distirbution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="0c211-106">CLI を使用するには、Python 2.7.x または Python 3.x が必要です。</span><span class="sxs-lookup"><span data-stu-id="0c211-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="0c211-107">ディストリビューションにいずれのパッケージもない場合は、[Python をインストール](https://www.python.org/downloads/)してください。</span><span class="sxs-lookup"><span data-stu-id="0c211-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="0c211-108">インストール</span><span class="sxs-lookup"><span data-stu-id="0c211-108">Install</span></span> 

1. <span data-ttu-id="0c211-109">Microsoft リポジトリ キーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="0c211-109">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="0c211-110">ローカル `azure-cli` リポジトリ情報を作成します。</span><span class="sxs-lookup"><span data-stu-id="0c211-110">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="0c211-111">`yum` パッケージのインデックスを更新し、インストールを行います。</span><span class="sxs-lookup"><span data-stu-id="0c211-111">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="0c211-112">`az` コマンドで Azure CLI を実行します。</span><span class="sxs-lookup"><span data-stu-id="0c211-112">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="0c211-113">更新</span><span class="sxs-lookup"><span data-stu-id="0c211-113">Update</span></span>

<span data-ttu-id="0c211-114">`yum update` コマンドで Azure CLI を更新します。</span><span class="sxs-lookup"><span data-stu-id="0c211-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="0c211-115">アンインストール</span><span class="sxs-lookup"><span data-stu-id="0c211-115">Uninstall</span></span>

<span data-ttu-id="0c211-116">Azure CLI が不要であると判断した場合は、アンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="0c211-116">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="0c211-117">アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="0c211-117">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="0c211-118">Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="0c211-118">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="0c211-119">また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。</span><span class="sxs-lookup"><span data-stu-id="0c211-119">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="0c211-120">システムからパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0c211-120">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="0c211-121">CLI を再インストールする予定がない場合は、リポジトリ情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="0c211-121">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="0c211-122">リポジトリ情報を削除した場合は、Microsoft GPG 署名キーも削除します。</span><span class="sxs-lookup"><span data-stu-id="0c211-122">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
