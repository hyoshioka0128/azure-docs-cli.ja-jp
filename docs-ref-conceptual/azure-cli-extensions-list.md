---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 03/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: ceca7ed92435ab03b196e60dee37195330f6f3c7
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/28/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 で使用可能な拡張機能

この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から直接入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli
az extension list-available --output table
```

| Name | バージョン | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Azure Enhanced Monitoring Extension for SAP を管理します。 |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | コマンドのエイリアスをサポートします。 |  |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.1.0 | その他のプレビューの Azure Batch コマンドです。 |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.1 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します。 |  |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.1 | Azure プライベート DNS のパブリック プレビューをサポートします。 |  |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | リージョン間でイメージをコピーします。 |  |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループのプレビューをサポートします。 | [はい] |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理パートナーのプレビューをサポートします。 | [はい] |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.4 | Azure MySQL および Azure PostgreSQL をサポートします。 |  |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | サブスクリプション定義のプレビューをサポートします。 | [はい] |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | appservice リソースを作成してデプロイします。 | [はい] |
