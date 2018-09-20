---
title: Docker コンテナーでの Azure CLI 2.0 の実行
description: Azure CLI 2.0 をホストする Docker コンテナーを実行する方法
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 277d9d3423af4941fb7f7fb57130fa1b7af7d32e
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388339"
---
# <a name="run-azure-cli-20-in-a-docker-container"></a>Docker コンテナーでの Azure CLI 2.0 の実行

Docker を使用して、Azure CLI 2.0 がプレインストールされたスタンドアロン Linux コンテナーを実行できます。 Docker を使用すると、CLI を実行する分離環境をすぐに準備できます。 独自のデプロイのベースとしてイメージを使用することもできます。

## <a name="run-in-a-docker-container"></a>Docker コンテナーでの実行

`docker run` を使用して、CLI をインストールしてください。

   ```bash
   docker run -it microsoft/azure-cli
   ```

> [!NOTE]
> お使いのユーザー環境から SSH キーを取得する場合は、`-v ${HOME}/.ssh:/root/.ssh` を使用して、その環境にご自身の SSH キーをマウントします。
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh microsoft/azure-cli
> ```

CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。 サインインするには、[az login](/cli/azure/reference-index#az-login) コマンドを実行します。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

さまざまな認証方法の詳細については、「[Azure CLI 2.0 を使用してサインインする](authenticate-azure-cli.md)」を参照してください。

## <a name="update-docker-image"></a>Docker イメージの更新

Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。 そのため、CLI をホストするコンテナーをデータ ストアとして使用することは避けるようにしてください。

`docker pull` でローカル イメージを更新します。

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a>Docker イメージのアンインストール

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

CLI イメージを実行しているコンテナーを停止した後、それを削除します。

```bash
docker rmi microsoft/azure-cli
```
