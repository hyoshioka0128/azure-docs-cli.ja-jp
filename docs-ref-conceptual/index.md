---
title: Azure CLI 2.0
description: Azure CLI 2.0 の概要。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: ffa435f8c6ee5aa82d2efe2e09d7bcb1f1dc434b
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967692"
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。
ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。

Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。 Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

[Cloud Shell](/azure/cloud-shell/overview) を使用して CLI をブラウザーで実行することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)することもできます。
CLI を実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。
最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。

Azure CLI 2.0 で一般的なタスクを開始する際には、次のサンプルが役立ちます。

- [Linux virtual machines](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows Virtual Machines](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。

Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。

> [!NOTE]
> 以前のバージョンの CLI (Azure CLI 1.0) を使用している場合は、引き続きそれを使用できます。
> ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI 2.0 に更新することをお勧めします。
> 両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。
