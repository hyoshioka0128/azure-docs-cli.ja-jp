---
title: Azure CLI で使用可能な拡張機能
description: Azure CLI で公式にサポートされている拡張機能の完全な一覧です。
author: haroldrandom
ms.author: jianzen
manager: yonzhan,yungezz
ms.date: 05/20/2020
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 9c4d54b0021ef3fddf96f73fade6fe8fc4731d60
ms.sourcegitcommit: 4e616bbc65888e0cc77fdad9193e6123027f3bb2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2020
ms.locfileid: "83775693"
---
# <a name="available-extensions-for-the-azure-cli"></a>Azure CLI で使用可能な拡張機能

この記事では、Microsoft によってサポートされている、Azure CLI で使用可能な拡張機能の完全な一覧を示します。

拡張機能の一覧は、CLI から入手することもできます。 取得するには、[az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available) を実行します。

```azurecli-interactive
az extension list-available --output table
```

| 名前 | Version | まとめ | プレビュー |
|------|---------|---------|---------|
| [アカウント](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの SubscriptionClient 拡張機能 |  |
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Azure Enhanced Monitoring Extension for SAP を管理します |  |
| [ai-did-you-mean-this](https://github.com/Azure/azure-cli-extensions/ai-did-you-mean-this) | 0.1.1 | 障害発生時の回復オプションを推奨します。 |  |
| [ai-examples](https://github.com/Azure/azure-cli-extensions/tree/master/src/ai-examples) | 0.2.0 | AI を使用した例をヘルプ コンテンツに追加します。 | はい |
| [aks-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/aks-preview) | 0.4.45 | 次期 AKS 機能のプレビューを提供します | はい |
| [alertsmanagement](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの Alerts 拡張機能 |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.2 | コマンドのエイリアスをサポートします | はい |
| [application-insights](https://github.com/Azure/azure-cli-extensions/tree/master/src/application-insights) | 0.1.7 | Application Insights コンポーネントの管理と、それらのコンポーネントのメトリック、イベント、およびログのクエリをサポートします。 | はい |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 5.0.1 | Azure Batch サービスを操作するための追加コマンド |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.8.9 | Azure CLI 用 Azure IoT 拡張機能です。 |  |
| [azure-cli-ml](https://docs.microsoft.com/azure/machine-learning/service/) | 1.5.0 | Microsoft Azure コマンド ライン ツールの AzureML コマンド モジュール |  |
| [azure-devops](https://github.com/Microsoft/azure-devops-cli-extension) | 0.18.0 | Azure DevOps を管理するためのツールです。 |  |
| [azure-firewall](https://github.com/Azure/azure-cli-extensions/tree/master/src/azure-firewall) | 0.3.1 | Azure Firewall のリソースを管理します。 | はい |
| [azure-iot](https://github.com/azure/azure-iot-cli-extension) | 0.9.2 | Azure CLI 用 Azure IoT 拡張機能です。 |  |
| [blueprint](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの Blueprint 拡張機能 |  |
| [connectedk8s](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | Microsoft Azure コマンド ライン ツールの Connectedk8s 拡張機能 | はい |
| [connectedmachine](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Microsoft Azure コマンド ライン ツールの Connectedmachine 拡張機能 | はい |
| [connection-monitor-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/connection-monitor-preview) | 0.1.0 | Microsoft Azure コマンドライン接続モニター V2 拡張機能 | はい |
| [csvmware](https://github.com/Azure/az-vmware-cli) | 0.3.0 | Azure VMware Solution by CloudSimple を管理します。 | はい |
| [custom-providers](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの Custom Providers 拡張機能 |  |
| [databox](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの DataBox 拡張機能 |  |
| [databricks](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | Microsoft Azure コマンド ライン ツールの DatabricksClient 拡張機能 |  |
| [datashare](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの DataShareManagementClient 拡張機能 |  |
| [db-up](https://github.com/Azure/azure-cli-extensions/tree/master/src/db-up) | 0.1.13 | Azure データベースのワークフローを簡略化するための、その他のコマンド。 | はい |
| [deploy-to-azure](https://github.com/Azure/deploy-to-azure-cli-extension) | 0.2.0 | GitHub Actions を使用して Azure にデプロイします。 | はい |
| [dev-spaces](https://github.com/Azure/azure-cli-extensions) | 1.0.5 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 |  |
| [dev-spaces-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.6 | Dev Spaces は、高速で反復的な Kubernetes 開発エクスペリエンスをチームに提供します。 | はい |
| [dms-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/dms-preview) | 0.11.0 | 新しい Database Migration Service のシナリオをサポートします。 | はい |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.4.9 | Microsoft Azure コマンド ライン ツールの EventGrid コマンド モジュールです。 | はい |
| [express-route](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route) | 0.1.3 | ExpressRoute プレビュー機能を管理します。 | はい |
| [express-route-cross-connection](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route-cross-connection) | 0.1.1 | ExpressRoute のクロス接続を使用して、顧客の ExpressRoute 回線を管理します。 |  |
| [front-door](https://github.com/Azure/azure-cli-extensions/tree/master/src/front-door) | 1.0.6 | ネットワークの Front Door を管理します。 |  |
| [hack](https://github.com/Azure/azure-cli-extensions) | 0.4.2 | Microsoft Azure コマンド ライン ツールの Hack 拡張機能 | はい |
| [healthcareapis](https://github.com/Azure/azure-cli-extensions) | 0.1.3 | Microsoft Azure コマンド ライン ツールの HealthCareApis 拡張機能 |  |
| [hpc-cache](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの StorageCache 拡張機能 | はい |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.2.4 | リージョン間での管理対象 VM イメージのコピーをサポートします |  |
| [import-export](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Microsoft Azure コマンド ライン ツールの StorageImportExport 拡張機能 |  |
| [interactive](https://github.com/Azure/azure-cli) | 0.4.4 | Microsoft Azure コマンド ライン対話型シェル | はい |
| [internet-analyzer](https://github.com/Azure/azure-cli-extensions) | 0.1.0rc5 | Microsoft Azure コマンド ライン ツールの Internet Analyzer 拡張機能 | はい |
| [ip-group](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Microsoft Azure コマンド ライン ツールの IpGroup 拡張機能 |  |
| [k8sconfiguration](https://github.com/Azure/azure-cli-extensions) | 0.1.8 | Microsoft Azure コマンド ライン ツールの K8sconfiguration 拡張機能 | はい |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | Azure Key Vault のコマンドをプレビューします。 | はい |
| [kusto](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの KustoManagementClient 拡張機能 |  |
| [log-analytics](https://github.com/Azure/azure-cli-extensions/tree/master/src/log-analytics) | 0.1.4 | Azure Log Analytics のクエリ機能をサポートします。 | はい |
| [log-analytics-solution](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの Operations 拡張機能 |  |
| [logic](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの LogicManagementClient 拡張機能 |  |
| [メンテナンス](https://github.com/Azure/azure-cli-extensions) | 1.0.1 | Azure メンテナンス管理のサポート。 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 管理パートナーのプレビューをサポートします |  |
| [mesh](https://github.com/Azure/azure-cli-extensions) | 0.10.6 | Microsoft Azure Service Fabric Mesh のサポート - パブリック プレビュー | はい |
| [mixed-reality](https://github.com/Azure/azure-cli-extensions) | 0.0.1 | Mixed Reality Azure CLI 拡張機能。 |  |
| [netappfiles-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/netappfiles-preview) | 0.3.2 | 次期 Azure NetApp Files (ANF) 機能のプレビューを提供します。 | はい |
| [notification-hub](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | Microsoft Azure コマンド ライン ツールの Notification Hub 拡張機能 |  |
| [peering](https://github.com/Azure/azure-cli-extensions) | 0.1.0rc2 | Microsoft Azure コマンド ライン ツールのピアリング拡張機能 | はい |
| [portal](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Microsoft Azure コマンド ライン ツールの Portal 拡張機能 |  |
| [powerbidedicated](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | Microsoft Azure コマンド ライン ツールの PowerBIDedicated 拡張機能 | はい |
| [privatedns](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | プライベート DNS ゾーンを管理するためのコマンド | はい |
| [resource-graph](https://github.com/Azure/azure-cli-extensions/tree/master/src/resource-graph) | 1.1.0 | Resource Graph を使用した Azure リソースのクエリをサポートします。 | はい |
| [sap-hana](https://github.com/Azure/azure-hanaonazure-cli-extension) | 0.6.1 | SAP HanaOnAzure インスタンスを操作するための追加コマンド。 |  |
| [spring-cloud](https://github.com/Azure/azure-cli-extensions) | 0.2.3 | Microsoft Azure コマンド ライン ツールの spring-cloud 拡張機能 | はい |
| [storage-or-preview](https://github.com/Azure/azure-cli-extensions) | 0.4.0 | Microsoft Azure コマンド ライン ツールの Storage-ors-preview 拡張機能 | はい |
| [storage-ors-preview](https://github.com/Azure/azure-cli-extensions) | 0.3.1 | Microsoft Azure コマンド ライン ツールの Storage-ors-preview 拡張機能 | はい |
| [storage-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/storage-preview) | 0.2.10 | 次期ストレージ機能のプレビューを提供します。 | はい |
| [storagesync](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの MicrosoftStorageSync 拡張機能 |  |
| [stream-analytics](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | Microsoft Azure コマンド ライン ツールの stream-analytics 拡張機能 |  |
| [subscription](https://github.com/Azure/azure-cli-extensions) | 0.1.3 | サブスクリプション管理プレビューをサポートします。 |  |
| [サポート](https://github.com/azure/azure-cli-extensions/tree/master/src/support) | 1.0.2 | Microsoft Azure コマンド ライン ツールの Support 拡張機能 |  |
| [synapse](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | Microsoft Azure コマンド ライン ツールの Synapse 拡張機能 | はい |
| [timeseriesinsights](https://github.com/Azure/azure-cli-extensions/src/timeseriesinsights)。 | 0.1.1 | Microsoft Azure コマンド ライン ツールの TimeSeriesInsightsClient 拡張機能 |  |
| [virtual-network-tap](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-network-tap) | 0.1.0 | 仮想ネットワーク タップ (VTAP) を管理します。 | はい |
| [virtual-wan](https://github.com/Azure/azure-cli-extensions/tree/master/src/virtual-wan) | 0.1.3 | 仮想 WAN、ハブ、VPN ゲートウェイ、および VPN サイトを管理します。 | はい |
| [vm-repair](https://github.com/Azure/azure-cli-extensions/tree/master/src/vm-repair) | 0.2.7 | VM を修正する自動修復コマンド。 |  |
| [vmware](https://github.com/virtustream/azure-vmware-virtustream-cli-extension) | 0.6.0 | Azure VMware Solution コマンドをプレビューします。 | はい |
| [webapp](https://github.com/Azure/azure-cli-extensions/tree/master/src/webapp) | 0.2.24 | Azure App Service のその他のコマンド。 | はい |