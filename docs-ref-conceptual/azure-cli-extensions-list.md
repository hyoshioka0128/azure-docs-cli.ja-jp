---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/25/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: f22565e4b9bb4fe0656aae90724bf124611ef3c8
ms.sourcegitcommit: 2836d0739f55ba06cbc7c556fdf3e698a3fd1e4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 で使用可能な拡張機能

この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から直接入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli
az extension list-available --output table
```

| Name | バージョン | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.1 | コマンドのエイリアスをサポートします | [はい] |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.2.1 | Azure Batch サービスを操作するための追加コマンド |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.3 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します |  |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | DNS ゾーン向けの Azure CLI 拡張機能 |  |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | リージョン間でイメージをコピーする Azure CLI 拡張機能。 |  |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループ向け Azure CLI 拡張機能 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | Azure MySQL および Azure PostgreSQL をサポートする Azure CLI 拡張機能。 |  |
| [signalr](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | SignalR 管理プレビューをサポートします。 | [はい] |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション管理プレビューをサポートします。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | appservice のリソースを管理する Azure CLI 拡張機能 | [はい] |
