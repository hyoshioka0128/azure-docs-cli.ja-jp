---
title: Azure CLI で使用可能な拡張機能
description: Azure CLI で公式にサポートされている拡張機能の完全な一覧です。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/11/2019
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 29966e17d287e296dfd0027bd9f8e37b507905ee
ms.sourcegitcommit: e16002dc9b28c9d35637d3601d3d8a2d92e6e85d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2019
ms.locfileid: "66837707"
---
# <a name="available-extensions-for-the-azure-cli"></a>Azure CLI で使用可能な拡張機能

この記事では、Microsoft によってサポートされている、Azure CLI で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli-interactive
az extension list-available --output table
```

| Name | バージョン | まとめ | プレビュー |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します |  |
| [aks-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/aks-preview) | 0.4.3 | 次期 AKS 機能のプレビューを提供します | はい |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.2 | コマンドのエイリアスをサポートします | はい |
| [appconfig](https://github.com/Azure/azure-cli-extensions) | 0.5.0 | 次期アプリ構成機能のプレビューを提供します。 | はい |
| [application-insights](https://github.com/Azure/azure-cli-extensions/tree/master/src/application-insights) | 0.1.1 | Application Insights コンポーネントの管理と、それらのコンポーネントのメトリック、イベント、およびログのクエリをサポートします。 | はい |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 3.0.4 | Azure Batch サービスを操作するための追加コマンド |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.7.0 | Azure IoT Hub、IoT Edge、および IoT Device Provisioning Service にデータ プレーン コマンド レイヤーを提供します |  |
| [azure-cli-ml](https://docs.microsoft.com/en-us/azure/machine-learning/service/) | 1.0.43 | Microsoft Azure コマンド ライン ツールの AzureML コマンド モジュール |  |
| [azure-devops](https://github.com/Microsoft/azure-devops-cli-extension) | 0.10.0 | Azure DevOps を管理するためのツールです。 |  |
| [azure-firewall](https://github.com/Azure/azure-cli-extensions/tree/master/src/azure-firewall) | 0.1.2 | Azure Firewall のリソースを管理します。 | はい |
| [db-up](https://github.com/Azure/azure-cli-extensions/tree/master/src/db-up) | 0.1.12 | Azure データベースのワークフローを簡略化するための、その他のコマンド。 | はい |
| [dev-spaces](https://github.com/Azure/azure-cli-extensions) | 1.0.1 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 |  |
| [dev-spaces-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.6 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 | はい |
| [dms-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/dms-preview) | 0.8.1 | 新しい Database Migration Service のシナリオをサポートします。 | はい |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | DNS ゾーン向けの Azure CLI 拡張機能 |  |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.4.2 | Microsoft Azure コマンド ライン ツールの EventGrid コマンド モジュールです。 | はい |
| [express-route](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route) | 0.1.3 | ExpressRoute プレビュー機能を管理します。 | はい |
| [express-route-cross-connection](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route-cross-connection) | 0.1.1 | ExpressRoute のクロス接続を使用して、顧客の ExpressRoute 回線を管理します。 |  |
| [find](https://github.com/Azure/azure-cli-extensions/tree/master/src/find) | 0.3.0 | CLI 情報に対するインテリジェントな照会。 | はい |
| [front-door](https://github.com/Azure/azure-cli-extensions/tree/master/src/front-door) | 0.1.6 | ネットワークの Front Door を管理します。 | はい |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | リージョン間での管理対象 VM イメージのコピーをサポートします |  |
| [interactive](https://github.com/Azure/azure-cli) | 0.4.3 | Microsoft Azure コマンド ライン対話型シェル | はい |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | Azure Key Vault のコマンドをプレビューします。 | はい |
| [log-analytics](https://github.com/Azure/azure-cli-extensions/tree/master/src/log-analytics) | 0.1.3 | Azure Log Analytics のクエリ機能をサポートします。 | はい |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 管理グループ向け Azure CLI 拡張機能 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [mesh](https://github.com/Azure/azure-cli-extensions) | 0.10.5 | Microsoft Azure Service Fabric Mesh のサポート - パブリック プレビュー | はい |
| [mixed-reality](https://github.com/Azure/azure-cli-extensions) | 0.0.1 | Mixed Reality Azure CLI 拡張機能。 |  |
| [netappfiles-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/netappfiles-preview) | 0.3.0 | 次期 Azure NetApp Files (ANF) 機能のプレビューを提供します。 | はい |
| [privatedns](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | プライベート DNS ゾーンを管理するためのコマンド | はい |
| [resource-graph](https://github.com/Azure/azure-cli-extensions/tree/master/src/resource-graph) | 0.1.10 | Resource Graph を使用した Azure リソースのクエリをサポートします。 | はい |
| [sap-hana](https://github.com/Azure/azure-hanaonazure-cli-extension) | 0.3.7 | SAP HanaOnAzure インスタンスを操作するための追加コマンド。 |  |
| [storage-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/storage-preview) | 0.2.6 | 次期ストレージ機能のプレビューを提供します。 | はい |
| [サブスクリプション](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | サブスクリプション管理プレビューをサポートします。 |  |
| [virtual-network-tap](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-network-tap) | 0.1.0 | 仮想ネットワーク タップ (VTAP) を管理します。 | はい |
| [virtual-wan](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-wan) | 0.1.0 | 仮想 WAN、ハブ、VPN ゲートウェイ、および VPN サイトを管理します。 | はい |
| [vm-repair](https://github.com/Azure/azure-cli-extensions/tree/master/src/vm-repair) | 0.1.0 | VM を修正する自動修復コマンド。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.17 | Azure App Service のその他のコマンド。 | はい |