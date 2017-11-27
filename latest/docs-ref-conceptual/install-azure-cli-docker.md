---
title: "Docker での Azure CLI のインストール"
description: "Azure CLI 2.0 で Docker コンテナーをインストールする方法"
keywords: "Azure CLI,Azure CLI のインストール,azure docker,azure docker イメージ,"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 76ecf2c9cd0e6e694a31ac160112d1348863f118
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-docker"></a>Docker での Azure CLI 2.0 のインストール

Docker を使用して、Azure CLI 2.0 が事前にインストールされているスタンドアロン Linux コンテナーをインストールできます。 これにより、CLI を試すことができる環境をすばやく準備して、その CLI が自分に適しているかどうかを判断できます。または、これを基本イメージとして使用できます。

## <a name="install-with-docker"></a>Docker によるインストール

`docker run` を使用して、CLI をインストールしてください。

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

利用可能なバージョンについては、[Docker のタグ](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)を参照してください。

CLI は、`/usr/local/bin` の `az` コマンドとしてイメージにインストールされます。

> [!NOTE]
> ユーザー環境から SSH キーを取得する場合は、`-v ${HOME}:/root` を使用して、$HOME を `/root` としてマウントできます。

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

### <a name="update-with-docker"></a>Docker での更新

Docker で更新するには、新しいイメージをプルし、さらに既存のすべてのコンテナーを再作成する必要があります。 このため、CLI をデータ ストアとしてホストするコンテナーの使用は避けることをお勧めします。

1. `docker pull` でローカル イメージを更新します。

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. 現時点で CLI イメージを使用しているコンテナーを取得します。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

  > [!NOTE]
  > イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。

3. コンテナーを停止し、もう一度作成します。

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="uninstall-with-docker"></a>Docker でのアンインストール

Azure CLI が不要であると判断した場合は、アンインストールすることができます。 アンインストールする前に、`az feedback` コマンドを使用して、アンインストールの理由と、CLI エクスペリエンスの改善方法について、ご意見をお聞かせください。 Microsoft では、できる限り Azure CLI のバグをなくし、使いやすいものにしたいと考えています。 また、[GitHub に問題を提出](https://github.com/Azure/azure-cli/issues)していただくこともできます。

CLI Docker イメージを適切にアンインストールには、それを実行しているすべてのコンテナーを削除し、ローカル イメージを削除する必要があります。

1. azure-cli イメージを実行しているコンテナーを取得します。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```
  > [!NOTE]
  > イメージの特定のバージョンをインストールした場合は、イメージ名の末尾に `:<version>` を追加する必要があります。

2. CLI イメージがあるすべてのコンテナーを削除します。

   ```bash
   docker rm 34a868beb2ab
   ```

3. ローカルにインストールされた CLI イメージを削除します。

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

