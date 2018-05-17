---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 5a71a5809aaaa26a4b67193c1a9ff70a6b8dec05
ms.sourcegitcommit: 1d18f667af28b59f5524a3499a4b7dc12af5163d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/09/2018
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
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.4 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します |  |
| [botservice](https://github.com/Azure/azure-cli-extensions) | 0.0.1 | Azure Bot Service 2017-12-01 プレビュー機能をサポートします | [はい] |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | DNS ゾーン向けの Azure CLI 拡張機能 |  |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | Azure EventGrid 2018-05-01 プレビュー機能をサポートします | [はい] |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.6 | リージョン間での管理対象 VM イメージのコピーをサポートします |  |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | Azure Key Vault のコマンドをプレビューします。 | [はい] |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループ向け Azure CLI 拡張機能 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | Azure MySQL および Azure PostgreSQL をサポートする Azure CLI 拡張機能。 |  |
| [signalr](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | SignalR 管理プレビューをサポートします。 | [はい] |
| [storage-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 次期ストレージ機能のプレビューを提供します。 | [はい] |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション管理プレビューをサポートします。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.6 | appservice のリソースを管理する Azure CLI 拡張機能 | [はい] |
