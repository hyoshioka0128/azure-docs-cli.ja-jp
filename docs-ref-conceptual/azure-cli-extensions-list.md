---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/02/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e7cf22d1611c224e1d7af351210e12fe0124fad0
ms.sourcegitcommit: 26e0816dad17cc3584d1724493feecf5f5faa1f5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 で使用可能な拡張機能

この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から直接入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli
az extension list-available --output table
```

| Name | バージョン | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します。 |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.3.0 | コマンドのエイリアスをサポートします。 | [はい] |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.1.0 | その他のプレビューの Azure Batch コマンドです。 |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.1 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します。 |  |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | Azure プライベート DNS のパブリック プレビューをサポートします。 |  |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | リージョン間でイメージをコピーします。 |  |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループのプレビューをサポートします。 | [はい] |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします。 | [はい] |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | Azure MySQL および Azure PostgreSQL をサポートします。 |  |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション定義のプレビューをサポートします。 | [はい] |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | appservice リソースを作成してデプロイします。 | [はい] |
