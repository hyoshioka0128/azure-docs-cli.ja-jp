---
title: Docker コンテナーでの Azure CLI の実行
description: Azure CLI をホストする Docker コンテナーを実行する方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 40e6865ce07b6ccb8e84a2666f0bcd6df3b5cfcf
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177761"
---
# <a name="run-azure-cli-in-a-docker-container"></a><span data-ttu-id="8f378-103">Docker コンテナーでの Azure CLI の実行</span><span class="sxs-lookup"><span data-stu-id="8f378-103">Run Azure CLI in a Docker container</span></span>

<span data-ttu-id="8f378-104">Docker を使用して、Azure CLI がプレインストールされたスタンドアロン Linux コンテナーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8f378-104">You can use Docker to run a standalone Linux container with the Azure CLI pre-installed.</span></span> <span data-ttu-id="8f378-105">Docker を使用すると、CLI を実行する分離環境をすぐに準備できます。</span><span class="sxs-lookup"><span data-stu-id="8f378-105">Docker gets you started quickly with an isolated environment to run the CLI in.</span></span> <span data-ttu-id="8f378-106">独自のデプロイのベースとしてイメージを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f378-106">The image can also be used as a base for your own deployments.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="8f378-107">Docker コンテナーでの実行</span><span class="sxs-lookup"><span data-stu-id="8f378-107">Run in a Docker container</span></span>

<span data-ttu-id="8f378-108">`docker run` を使用して、CLI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="8f378-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="8f378-109">お使いのユーザー環境から SSH キーを取得する場合は、`-v ${HOME}/.ssh:/root/.ssh` を使用して、その環境にご自身の SSH キーをマウントします。</span><span class="sxs-lookup"><span data-stu-id="8f378-109">If you want to pick up the SSH keys from your user environment, use `-v ${HOME}/.ssh:/root/.ssh` to mount your SSH keys in the environment.</span></span>
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh microsoft/azure-cli
> ```

<span data-ttu-id="8f378-110">CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="8f378-110">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span> <span data-ttu-id="8f378-111">サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8f378-111">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="8f378-112">さまざまな認証方法の詳細については、「[Azure CLI を使用してサインインする](authenticate-azure-cli.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f378-112">To learn more about different authentication methods, see [Sign in with the Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="update-docker-image"></a><span data-ttu-id="8f378-113">Docker イメージの更新</span><span class="sxs-lookup"><span data-stu-id="8f378-113">Update Docker image</span></span>

<span data-ttu-id="8f378-114">Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f378-114">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="8f378-115">そのため、CLI をホストするコンテナーをデータ ストアとして使用することは避けるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="8f378-115">For this reason, you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="8f378-116">`docker pull` でローカル イメージを更新します。</span><span class="sxs-lookup"><span data-stu-id="8f378-116">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="8f378-117">Docker イメージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="8f378-117">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="8f378-118">CLI イメージを実行しているコンテナーを停止した後、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="8f378-118">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```

## <a name="next-steps"></a><span data-ttu-id="8f378-119">次の手順</span><span class="sxs-lookup"><span data-stu-id="8f378-119">Next Steps</span></span>

<span data-ttu-id="8f378-120">これで Azure CLI を使用する準備ができました。次は、その機能と一般的なコマンドを簡単に見ていきましょう。</span><span class="sxs-lookup"><span data-stu-id="8f378-120">Now that you're ready to use the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8f378-121">Azure CLI の概要</span><span class="sxs-lookup"><span data-stu-id="8f378-121">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
