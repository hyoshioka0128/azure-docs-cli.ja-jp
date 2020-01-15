---
title: 各 Azure CLI 製品の違い
description: Azure CLI 製品の名前とバージョンがどのように設定されているか、およびそのアップグレード方法について説明します。
author: dbradish-microsoft
ms.author: dbradish
manager: barbkess
ms.date: 07/12/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azurecli
ms.openlocfilehash: 77b3629d0cc79d2b329007fd93b49022d5f29783
ms.sourcegitcommit: 18973ac471bbd12af2c8f8fa32a233b0abe5b020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2020
ms.locfileid: "75913597"
---
# <a name="differences-between-azure-cli-products"></a>各 Azure CLI 製品の違い

2018 年 6 月末の時点で、明示的なバージョン番号が Azure CLI 製品名から削除されました。 ドキュメントで "Azure CLI" を使用するように記載されているが、どの製品バージョンを指しているのかが明確ではなかった場合に時折生じていた混乱が、この変更により解消されます。 前の製品名に慣れている方は、どのように変更されたかを以下でご確認ください。

* Azure CLI バージョン 2.0 以降は、ただ "Azure CLI" と呼ばれるようになりました。
* それよりも前のバージョンの Azure CLI (1.x 以下) は、"Azure クラシック CLI" と呼ばれるようになりました。

名前が Azure クラシック CLI に変更されたことで、このツールがクラシック デプロイ モデルのみでの使用を意図していることが明確になっています。 また、クラシック CLI については、今後は更新も保守も行われません。 この理由やその他のさまざまな理由から、クラシック デプロイは、Azure Resource Manager モデルを使用できるように移動し、最新バージョンの Azure CLI に移行することをお勧めします。

クラシック CLI を使用している場合は、以下の記事で移行プロセスについてご確認ください。

* [クラシックから Azure Resource Manager に移行する](/azure/virtual-machines/linux/migration-classic-resource-manager-overview)
* [Azure CLI のインストール](install-azure-cli.md)
* [Azure クラシック CLI から Azure CLI への移行](https://github.com/Azure/azure-cli/blob/dev/doc/classic_cli_migration.md)
