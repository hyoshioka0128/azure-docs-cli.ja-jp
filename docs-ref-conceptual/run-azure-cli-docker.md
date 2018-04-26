---
title: Docker コンテナーでの Azure CLI 2.0 の実行
description: Azure CLI 2.0 をホストする Docker コンテナーを実行する方法
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e394dc5cd375ec6d3393f45f38694f71369379d4
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a><span data-ttu-id="dccec-103">Docker コンテナーでの Azure CLI 2.0 の実行</span><span class="sxs-lookup"><span data-stu-id="dccec-103">Run Azure CLI 2.0 in a Docker container</span></span>

<span data-ttu-id="dccec-104">Docker を使用して、Azure CLI 2.0 がプレインストールされたスタンドアロン Linux コンテナーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="dccec-104">You can use Docker to run a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="dccec-105">Docker を使用すると、CLI を試すことができる環境をすばやく準備して、CLI が自分に適しているかどうかを判断したり、独自のデプロイのベースとしてイメージを使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="dccec-105">Docker lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or use our image as a base for your own deployment.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="dccec-106">Docker コンテナーでの実行</span><span class="sxs-lookup"><span data-stu-id="dccec-106">Run in a Docker container</span></span>

<span data-ttu-id="dccec-107">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="dccec-107">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

<span data-ttu-id="dccec-108">CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="dccec-108">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span> <span data-ttu-id="dccec-109">ログインするには、`az login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="dccec-109">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="dccec-110">さまざまなログイン方法の詳細については、「[Azure CLI 2.0 を使用してログインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dccec-110">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="dccec-111">ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。</span><span class="sxs-lookup"><span data-stu-id="dccec-111">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a><span data-ttu-id="dccec-112">Docker イメージの更新</span><span class="sxs-lookup"><span data-stu-id="dccec-112">Update Docker image</span></span>

<span data-ttu-id="dccec-113">Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dccec-113">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="dccec-114">そのため、CLI をデータ ストアとしてホストするコンテナーの使用は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="dccec-114">For this reason you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="dccec-115">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="dccec-115">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="dccec-116">Docker イメージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="dccec-116">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="dccec-117">CLI イメージを実行しているコンテナーを停止した後、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="dccec-117">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```
