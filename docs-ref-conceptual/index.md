---
title: Azure CLI の概要
description: Azure コマンド ライン インターフェイス (CLI) の概要を説明します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 3b9589c769a90e82c35aa64c583dffdac4e4f063
ms.sourcegitcommit: 1987a39809f9865034b27130e56f30b2bd1eb72c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2019
ms.locfileid: "56421985"
---
# <a name="azure-command-line-interface-cli"></a>Azure コマンド ライン インターフェイス (CLI)

Azure コマンド ライン インターフェイス (CLI) は、Azure リソースを管理するための、Microsoft のクロスプラットフォーム コマンド ライン エクスペリエンスです。
ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用することも、macOS、Linux、または Windows に[インストール](install-azure-cli.md)してコマンド ラインから実行することもできます。

Azure CLI は簡単に使い始めることができ、Azure Resource Manager を操作対象とする自動化スクリプトを作成するにも最適です。
Azure CLI を使用すると、次のコマンドを入力するだけで、簡単に Azure 内に VM を作成できます。

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

> [!NOTE]
>
> スクリプトおよび Microsoft ドキュメント サイトでは、Azure CLI の例は `bash` シェル向けに記述されています。 1 行の例であれば任意のプラットフォームで実行できます。 行継続 (`\`) または変数の代入を含む、より長い例は、PowerShell などの他のシェルで動作するように変更する必要があります。

## <a name="run-or-install"></a>実行またはインストール

CLI はローカルにインストールできます。また、Azure Cloud Shell を使用してブラウザーで実行したり、Docker コンテナーで実行したりすることもできます。 CLI の現在のバージョンを取得するには、`az --version` を実行します。

* Azure Cloud Shell を使用したブラウザーでの実行方法については、「[Azure Cloud Shell の Bash のクイック スタート](/azure/cloud-shell/quickstart)」または「[Azure Cloud Shell の PowerShell のクイック スタート](/azure/cloud-shell/quickstart-powershell)」をご覧ください。
* CLI のインストール方法については、「[Azure CLI のインストール](install-azure-cli.md)」を参照してください。
* Docker コンテナーとして実行する方法については、「[Docker コンテナーでの Azure CLI の実行](run-azure-cli-docker.md)」を参照してください

## <a name="build-your-skills-with-microsoft-learn"></a>Microsoft Learn でスキルを身に付ける

- [Azure CLI で仮想マシンを管理する](/learn/modules/manage-virtual-machines-with-azure-cli/)
- [CLI で Azure サービスを制御する](/learn/modules/control-azure-services-with-cli/)
- [対話型学習の詳細...](/learn/browse/?products=azure-clis)

## <a name="get-started"></a>作業開始

CLI の基本については、[概要](get-started-with-azure-cli.md)の記事をお読みください。 次のサンプルでは、一般的なユース ケースが紹介されています。

- [Linux Virtual Machines](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows Virtual Machines](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web Apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

個々の Azure CLI コマンドの使用方法が記載された詳細な[リファレンス](/cli/azure/reference-index)も用意されています。

> [!NOTE]
> 以前のバージョンの CLI (Azure クラシック CLI) を使用している場合は、引き続きそれを使用できます。
> ただし、最適なエクスペリエンスを実現するために、最新バージョンの Azure CLI に更新することをお勧めします。
> 両方の CLI を使用する場合は、`azure` がクラシック CLI で、`az` が最新の CLI であることを覚えておいてください。
