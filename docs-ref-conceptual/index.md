---
title: Azure CLI 2.0 の概要
description: Azure CLI 2.0 の概要。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 55c5ea3ad69df60d211cc076e3570e9f07040af7
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388390"
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。
ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。

Azure CLI 2.0 は簡単に使い始めることができ、Azure Resource Manager を操作対象とする自動化スクリプトを作成するにも最適です。 Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a>実行またはインストール

CLI はローカルにインストールできます。また、Azure Cloud Shell を使用してブラウザーで実行したり、Docker コンテナーで実行したりすることもできます。

* Azure Cloud Shell を使用したブラウザーでの実行方法については、「[Azure Cloud Shell の Bash のクイック スタート](/azure/cloud-shell/quickstart)」または「[Azure Cloud Shell の PowerShell のクイック スタート](/azure/cloud-shell/quickstart-powershell)」をご覧ください。
* CLI のインストール方法については、[Azure CLI 2.0 のインストール](install-azure-cli.md)に関するページをご覧ください。
* Docker コンテナーとして実行する方法については、「[Docker コンテナーでの Azure CLI 2.0 の実行](run-azure-cli-docker.md)」をご覧ください

## <a name="get-started"></a>作業開始

CLI の基本については、[概要](get-started-with-azure-cli.md)の記事をお読みください。 次のサンプルでは、一般的なユース ケースが紹介されています。

- [Linux virtual machines](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows Virtual Machines](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。

> [!NOTE]
> 以前のバージョンの CLI (Azure CLI 1.0) を使用している場合は、引き続きそれを使用できます。
> ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI 2.0 に更新することをお勧めします。
> 両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。
