---
title: Docker コンテナーでの Azure CLI の実行
description: Azure CLI をホストする Docker コンテナーを実行する方法
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 01/29/2018
ms.topic: conceptual
ms.service: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 96a2bcf311cb504b08d44da3ea6033dbad9034b8
ms.sourcegitcommit: ee64dc738cfe689a2a479e32a87bf420f96c31c8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2020
ms.locfileid: "77780045"
---
# <a name="run-azure-cli-in-a-docker-container"></a><span data-ttu-id="9742d-103">Docker コンテナーでの Azure CLI の実行</span><span class="sxs-lookup"><span data-stu-id="9742d-103">Run Azure CLI in a Docker container</span></span>

<span data-ttu-id="9742d-104">Docker を使用して、Azure CLI がプレインストールされたスタンドアロン Linux コンテナーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9742d-104">You can use Docker to run a standalone Linux container with the Azure CLI pre-installed.</span></span> <span data-ttu-id="9742d-105">Docker を使用すると、CLI を実行する分離環境をすぐに準備できます。</span><span class="sxs-lookup"><span data-stu-id="9742d-105">Docker gets you started quickly with an isolated environment to run the CLI in.</span></span> <span data-ttu-id="9742d-106">独自のデプロイのベースとしてイメージを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="9742d-106">The image can also be used as a base for your own deployments.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="9742d-107">Docker コンテナーでの実行</span><span class="sxs-lookup"><span data-stu-id="9742d-107">Run in a Docker container</span></span>

> [!NOTE]
> <span data-ttu-id="9742d-108">Azure CLI は [Microsoft コンテナー レジストリ](https://azure.microsoft.com/services/container-registry)に移行されました。</span><span class="sxs-lookup"><span data-stu-id="9742d-108">The Azure CLI has migrated to [Microsoft Container Registry](https://azure.microsoft.com/services/container-registry).</span></span> <span data-ttu-id="9742d-109">Docker Hub 上の既存のタグは引き続きサポートされますが、新しいリリースは mcr.microsoft.com/azure-cli としてのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="9742d-109">Existing tags on Docker Hub are still supported, but new releases will only be available as mcr.microsoft.com/azure-cli.</span></span>

<span data-ttu-id="9742d-110">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="9742d-110">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it mcr.microsoft.com/azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="9742d-111">お使いのユーザー環境から SSH キーを取得する場合は、`-v ${HOME}/.ssh:/root/.ssh` を使用して、その環境にご自身の SSH キーをマウントします。</span><span class="sxs-lookup"><span data-stu-id="9742d-111">If you want to pick up the SSH keys from your user environment, use `-v ${HOME}/.ssh:/root/.ssh` to mount your SSH keys in the environment.</span></span>
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh mcr.microsoft.com/azure-cli
> ```

<span data-ttu-id="9742d-112">CLI は、`az` の `/usr/local/bin` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9742d-112">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span> <span data-ttu-id="9742d-113">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9742d-113">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="9742d-114">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9742d-114">To learn more about different authentication methods, see [Sign in with the Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="update-docker-image"></a><span data-ttu-id="9742d-115">Docker イメージの更新</span><span class="sxs-lookup"><span data-stu-id="9742d-115">Update Docker image</span></span>

<span data-ttu-id="9742d-116">Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9742d-116">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="9742d-117">そのため、CLI をホストするコンテナーをデータ ストアとして使用することは避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="9742d-117">For this reason, you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="9742d-118">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="9742d-118">Update your local image with `docker pull`.</span></span>

```bash
docker pull mcr.microsoft.com/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="9742d-119">Docker イメージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="9742d-119">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="9742d-120">CLI イメージを実行しているコンテナーを停止した後、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="9742d-120">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi mcr.microsoft.com/azure-cli
```

## <a name="next-steps"></a><span data-ttu-id="9742d-121">次の手順</span><span class="sxs-lookup"><span data-stu-id="9742d-121">Next Steps</span></span>

<span data-ttu-id="9742d-122">これで Azure CLI を使用する準備ができました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="9742d-122">Now that you're ready to use the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="9742d-123">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="9742d-123">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
