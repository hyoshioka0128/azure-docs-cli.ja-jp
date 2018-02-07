---
title: "Docker コンテナーでの Azure CLI 2.0 の実行"
description: "Azure CLI 2.0 をホストする Docker コンテナーを実行する方法"
keywords: "Azure CLI,Azure CLI のインストール,azure docker,azure docker イメージ,"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 819ff0cdb0df6057a5dff8f8ab015796f06c6a9b
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a><span data-ttu-id="7ec49-104">Docker コンテナーでの Azure CLI 2.0 の実行</span><span class="sxs-lookup"><span data-stu-id="7ec49-104">Run Azure CLI 2.0 in a Docker container</span></span>

<span data-ttu-id="7ec49-105">Docker を使用して、Azure CLI 2.0 がプレインストールされたスタンドアロン Linux コンテナーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7ec49-105">You can use Docker to run a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="7ec49-106">Docker を使用すると、CLI を試すことができる環境をすばやく準備して、CLI が自分に適しているかどうかを判断したり、独自のデプロイのベースとしてイメージを使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="7ec49-106">Docker lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or use our image as a base for your own deployment.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="7ec49-107">Docker コンテナーでの実行</span><span class="sxs-lookup"><span data-stu-id="7ec49-107">Run in a Docker container</span></span>

<span data-ttu-id="7ec49-108">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="7ec49-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

<span data-ttu-id="7ec49-109">CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7ec49-109">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec49-110">ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。</span><span class="sxs-lookup"><span data-stu-id="7ec49-110">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a><span data-ttu-id="7ec49-111">Docker イメージの更新</span><span class="sxs-lookup"><span data-stu-id="7ec49-111">Update Docker image</span></span>

<span data-ttu-id="7ec49-112">Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ec49-112">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="7ec49-113">そのため、CLI をデータ ストアとしてホストするコンテナーの使用は避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="7ec49-113">For this reason you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="7ec49-114">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="7ec49-114">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="7ec49-115">Docker イメージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="7ec49-115">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="7ec49-116">CLI イメージを実行しているコンテナーを停止した後、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="7ec49-116">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```
