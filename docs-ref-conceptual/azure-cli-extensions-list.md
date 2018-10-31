---
title: Azure CLI で使用可能な拡張機能
description: Azure CLI で公式にサポートされている拡張機能の完全な一覧です。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/21/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 0cf781f97e44b8752f5d03b9dbe4239489878856
ms.sourcegitcommit: 6d9169ed547df151f99e5a3ac86578634486419a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2018
ms.locfileid: "49652517"
---
# <a name="available-extensions-for-the-azure-cli"></a>Azure CLI で使用可能な拡張機能

この記事では、Microsoft によってサポートされている、Azure CLI で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli
az extension list-available --output table
```

| Name | Version | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.1 | コマンドのエイリアスをサポートします | [はい] |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.5.1 | Azure Batch サービスを操作するための追加コマンド |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.6.0 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します |  |
| [azure-firewall](https://github.com/Azure/azure-cli-extensions/tree/master/src/azure-firewall) | 0.1.0 | Azure Firewall のリソースを管理します。 | [はい] |
| [botservice](https://github.com/Azure/azure-cli-extensions) | 0.4.1 | ネイティブの Bot Service CLI コマンド モジュールの問題のバグ修正。 | [はい] |
| [dev-spaces-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.6 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 | [はい] |
| [dms-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/dms-preview) | 0.5.0 | 新しい Database Migration Service のシナリオをサポートします。 | [はい] |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | DNS ゾーン向けの Azure CLI 拡張機能 |  |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | Azure EventGrid 2018-05-01 プレビュー機能をサポートします | [はい] |
| [express-route](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route) | 0.1.2 | ExpressRoute プレビュー機能を管理します。 | [はい] |
| [express-route-cross-connection](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route-cross-connection) | 0.1.0 | ExpressRoute のクロス接続を使用して、顧客の ExpressRoute 回線を管理します。 |  |
| [find](https://github.com/Azure/azure-cli-extensions/tree/master/src/find) | 0.2.0 | CLI 情報に対するインテリジェントな照会。 | [はい] |
| [front-door](https://github.com/Azure/azure-cli-extensions/tree/master/src/front-door) | 0.1.1 | ネットワークの Front Door を管理します。 | [はい] |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.8 | リージョン間での管理対象 VM イメージのコピーをサポートします |  |
| [interactive](https://github.com/Azure/azure-cli) | 0.4.0 | Microsoft Azure コマンド ライン対話型シェル | [はい] |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | Azure Key Vault のコマンドをプレビューします。 | [はい] |
| [log-analytics](https://github.com/Azure/azure-cli-extensions/tree/master/src/log-analytics) | 0.1.3 | Azure Log Analytics のクエリ機能をサポートします。 | [はい] |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループ向け Azure CLI 拡張機能 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [mesh](https://github.com/Azure/azure-cli-extensions) | 0.9.1 | Microsoft Azure Service Fabric Mesh のサポート - パブリック プレビュー | [はい] |
| [rdbms-vnet](https://github.com/Azure/azure-cli-extensions) | 10.0.0 | Azure MySQL および Azure PostgreSQL のリソースで仮想ネットワーク ルールをサポートします |  |
| [resource-graph](https://github.com/Azure/azure-cli-extensions/tree/master/src/resource-graph) | 0.1.8 | Resource Graph を使用した Azure リソースのクエリをサポートします。 | [はい] |
| [sap-hana](https://github.com/Azure/azure-hanaonazure-cli-extension) | 0.1.6 | SAP HanaOnAzure インスタンスを操作するための追加コマンド。 |  |
| [signalr](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | SignalR 管理プレビューをサポートします。 | [はい] |
| [storage-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/storage-preview) | 0.1.6 | 次期ストレージ機能のプレビューを提供します。 | [はい] |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション管理プレビューをサポートします。 |  |
| [virtual-network-tap](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-network-tap) | 0.1.0 | 仮想ネットワーク タップ (VTAP) を管理します。 | [はい] |
| [virtual-wan](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-wan) | 0.1.0 | 仮想 WAN、ハブ、VPN ゲートウェイ、および VPN サイトを管理します。 | [はい] |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.11 | Azure App Service のその他のコマンド。 | [はい] |