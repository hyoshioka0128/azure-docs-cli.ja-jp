---
title: Azure CLI 2.0
description: "Azure CLI 2.0 の概要。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 2f4f9950dd663ae85f41bf4efe114b15770ace5d
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: ja-JP
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 は、Azure リソースを管理するための、Azure の新しいコマンド ライン エクスペリエンスです。  macOS、Linux、および Windows で使用できます。 

Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。 Azure CLI 2.0 を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

ご利用のシステムで Azure CLI 2.0 を使用するための準備については、[インストール](install-azure-cli.md)に関する記事を参照してください。 さらに実際に使う際には、[概要](get-started-with-azure-cli.md)の記事をお読みください。
最新リリースについては、[リリース ノート](release-notes-azure-cli.md)を参照してください。

Azure CLI 2.0 の基本的な使い方については、次のサンプルが参考になります。
- [Linux 仮想マシン](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows 仮想マシン](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

個々の Azure CLI 2.0 コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/)も用意されています。

Azure CLI 2.0 を今すぐ[使ってみましょう](get-started-with-azure-cli.md)。


> [!NOTE]
> 以前のバージョンの CLI (Azure CLI) を使用している場合は、引き続きそれを使用できます。
> 両方の CLI を使用する場合は、`azure` が古い CLI (Azure CLI) で、`az` が新しい CLI (Azure CLI 2.0) であることを覚えておいてください。 