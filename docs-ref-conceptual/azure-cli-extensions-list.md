---
title: Azure CLI 2.0 で使用可能な拡張機能
description: Azure CLI 2.0 で公式にサポートされている拡張機能の完全な一覧です。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 08/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 09735708946e40fd0d515bcd43bbf4798c70673d
ms.sourcegitcommit: 4cf5784b741dd55c0a4240443d3180d8ec83526c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2018
ms.locfileid: "43144899"
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 で使用可能な拡張機能

この記事では、Microsoft によって提供およびサポートされている、Azure CLI 2.0 で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から直接入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli
az extension list-available --output table
```

| Name | Version | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.1 | コマンドのエイリアスをサポートします | [はい] |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.4.1 | Azure Batch サービスを操作するための追加コマンド |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.5.1 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します |  |
| [botservice](https://github.com/Azure/azure-cli-extensions) | 0.0.3 | Azure Bot Service 2017-12-01 プレビュー機能をサポートします | [はい] |
| [dev-spaces-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.6 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 | [はい] |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | DNS ゾーン向けの Azure CLI 拡張機能 |  |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | Azure EventGrid 2018-05-01 プレビュー機能をサポートします | [はい] |
| [express-route-cross-connection](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route-cross-connection) | 0.1.0 | ExpressRoute のクロス接続を使用して、顧客の ExpressRoute 回線を管理します。 |  |
| [find](https://github.com/Azure/azure-cli-extensions/tree/master/src/find) | 0.1.0 | CLI 情報に対するインテリジェントな照会。 | [はい] |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.7 | リージョン間での管理対象 VM イメージのコピーをサポートします |  |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | Azure Key Vault のコマンドをプレビューします。 | [はい] |
| [log-analytics](https://github.com/Azure/azure-cli-extensions/tree/master/src/log-analytics) | 0.1.2 | Azure Log Analytics のクエリ機能をサポートします。 | [はい] |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループ向け Azure CLI 拡張機能 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [mesh](https://github.com/Azure/azure-cli-extensions) | 0.9.1 | Microsoft Azure Service Fabric Mesh のサポート - パブリック プレビュー | [はい] |
| [rdbms-vnet](https://github.com/Azure/azure-cli-extensions) | 10.0.0 | Azure MySQL および Azure PostgreSQL のリソースで仮想ネットワーク ルールをサポートします |  |
| [signalr](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | SignalR 管理プレビューをサポートします。 | [はい] |
| [storage-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/storage-preview) | 0.1.3 | 次期ストレージ機能のプレビューを提供します。 | [はい] |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション管理プレビューをサポートします。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.7 | appservice のリソースを管理する Azure CLI 拡張機能 | [はい] |
