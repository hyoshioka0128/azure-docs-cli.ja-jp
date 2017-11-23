---
title: "Azure CLI 2.0 を使ってみる"
description: "Linux、Mac、または Windows 上で、Azure CLI 2.0 の使用を開始します。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 3354d1c6518ea2d0ef0db227a13b86cb59d0575e
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2017
---
# <a name="get-started-with-azure-cli-20"></a>Azure CLI 2.0 を使ってみる

Azure CLI 2.0 は、Azure リソースを管理するための、Azure の新しいコマンド ライン エクスペリエンスです。
ブラウザーの [Azure Cloud Shell](/azure/cloud-shell/overview) で使用できるほか、macOS、Linux、Windows に[インストール](install-azure-cli.md)してコマンド ラインで実行することもできます。

Azure CLI 2.0 は、コマンド ラインから Azure リソースを管理したり、Azure Resource Manager を操作対象とする自動化スクリプトを作成したりするために最適化されています。
この記事では、その基本的な使い方と核となる概念について説明します。

最新リリースについては、[リリース ノート](release-notes-azure-cli.md)をご覧ください。

## <a name="connect"></a>接続

最も簡単に始められるのは、[Cloud Shell を起動](/azure/cloud-shell/quickstart)する方法です。

1. Cloud Shell は、Azure Portal の上部のナビゲーションから起動します。

   ![Shell アイコン](media/get-started-with-azure-cli/shell-icon.png)

2. 使用するサブスクリプションを選択し、ストレージ アカウントを作成します。

   ![ストレージ アカウントの作成](media/get-started-with-azure-cli/storage-prompt.png)

CLI を[インストール](install-azure-cli.md)し、コマンド ラインからローカルで実行することもできます。 CLI をインストールしたら、`az login` を実行し、既定のサブスクリプションでログインします。

## <a name="create-a-resource-group"></a>リソース グループの作成

必要な設定がすべて整ったら、Azure CLI を使って Azure にリソースを作成してみましょう。

まずリソース グループを作成します。  Azure ではリソース グループを使うことで、複数のリソースを論理上のグループとして管理することができます。  たとえばアプリケーションまたはプロジェクトのリソース グループを作成し、仮想マシンやデータベース、CDN サービスをそこに追加することができます。

"MyResourceGroup" という名前のリソース グループを Azure の *westus2* リージョンに作成しましょう。  そのためには、次のコマンドを入力します。

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

リソース グループが作成されると、`az group create` コマンドによって、新しく作成されたリソースのいくつかのプロパティが出力されます。

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a>Linux 仮想マシンの作成

リソース グループが完成したら、そこに Linux VM を作成します。

次のコマンドで、一般的な UbuntuLTS イメージを使用して、10 GB と 20 GB の 2 つのストレージ ディスクがアタッチされた Linux VM を作成することができます。

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

上のコマンドを実行すると、Azure CLI 2.0 は、~/.ssh ディレクトリに格納されている SSH キー ペアを探します。  SSH キー ペアがまだそこに格納されていない場合は、次のように --generate-ssh-keys パラメーターを渡して、Azure CLI に自動的に作成させることができます。

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

VM の作成が完了し、アクセスして使用できるようになると、`az vm create` コマンドから出力が返されます。 出力には、パブリック IP アドレスなど、新しく作成した VM のいくつかのプロパティが含まれます。

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

VM が作成されたら、その VM のパブリック IP アドレスを **SSH** で使用し、新しい Linux VM にログオンすることができます。

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a>Windows Server 仮想マシンの作成

`az vm create` コマンドを使用して、Windows Server 2016 Datacenter ベースの VM を作成し、Linux VM 用に使用したのと同じ "MyResourceGroup" リソース グループに追加しましょう。  Linux VM の例のように、`--data-disk-sizes-gb` パラメーターを使用して 2 つのストレージ ディスクも接続します。

Azure では、簡単に推測できるユーザー名とパスワードを使用しないようにする必要があります。 使用できる文字のほか、ユーザー名とパスワードの最小の長さについて特定の規則があります。  

> [!NOTE]
> このコマンドを実行すると、ユーザー名とパスワードの入力を求めるメッセージが表示されます。

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

VM の作成が完了し、アクセスして使用できるようになると、`az vm create` コマンドから結果が出力されます。

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

リモート デスクトップと VM のパブリック IP アドレス (`az vm create` の出力で返されるアドレス) を使用して、新しく作成した Windows Server VM にログオンします。  
Windows ベースのシステムでは、`mstsc` コマンドを使ってコマンド ラインから同じ操作を実行できます。

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

VM を作成したときと同じユーザー名/パスワードの組み合わせを指定してログインしてください。

## <a name="creating-other-resources-in-azure"></a>その他の Azure リソースの作成

ここまでは、リソース グループ、Linux VM、Windows Server VM の作成方法を見てきました。 その他にも、さまざまな種類の Azure リソースを作成することができます。  

すべての新しいリソースは、一貫した `az <resource type name> create` 名前付けパターンを使用して作成されます。  たとえば、新しく作成した VM に関連付けるための Azure Network Load Balancer を作成するには、次の create コマンドを使います。

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

また、次の create コマンドを使って、インフラストラクチャ用に新しいプライベート仮想ネットワーク (Azure では通常 "VNet" と呼ばれます) を作成することもできます。

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

Azure と Azure CLI の優れている点は、それらを使ってクラウドベースのインフラストラクチャを実現できるだけでなく、管理の行き届いたプラットフォーム サービスを作成できることです。  その管理されたプラットフォーム サービスにインフラストラクチャを組み合わせることで、さらに強力なソリューションを構築することもできます。

たとえば Azure CLI を使って Azure AppService を作成することができます。  Azure AppService は、管理されたプラットフォーム サービスであり、インフラストラクチャには一切気を遣わずに Web アプリをホストできるのが特徴です。  Azure AppService の作成後、次の create コマンドを使用して、AppService 内に 2 つの新しい Azure Web アプリを作成することができます。

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

`az <resource type name> create` パターンの基本を理解すると、何でも簡単に作成できるようになります。 以下に、いくつかの一般的な Azure リソースの種類と、それを作成するための Azure CLI create コマンドを示します。

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

上記の各コマンドに渡すことができるリソース固有の追加パラメーターと、作成できるリソースの種類の詳細については、[リファレンス ドキュメント](/cli/azure)を参照してください。 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a>便利なヒント: --no-wait を使用して作成操作を最適化する

既定では、Azure CLI 2.0 を使用してリソースを作成するときに、`az <resource type name> create` コマンドは、リソースが作成されて使用できるようになるまで待ちます。  たとえば、VM を作成する場合、`az vm create` コマンドは、既定では VM が作成されて SSH または RDP でアクセスできるようになるまで戻ってきません。

この方法を使用するのは、依存関係のある複数のステップを含む (続行する前に前のタスクを正常に完了しておく必要がある) 自動化スクリプトを簡単に記述できるためです。

続行する前にリソースの作成を待つ必要がない場合は、`no-wait` オプションを使用して、バックグラウンドで作成アクションを開始することができます。 他のコマンドには引き続き CLI を使用できます。

たとえば、次のように `az vm create` を使用すると、VM のデプロイが開始され、より短い時間で (VM が完全に起動される前に) 制御が戻ります。

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

`--no-wait` を使用すると、自動化スクリプトのパフォーマンスを大幅に最適化することができます。

## <a name="listing-resources-and-formatting-output"></a>リソースの一覧表示と出力の書式設定

Azure CLI 内で `list` コマンドを使用すると、Azure で実行されているリソースを検出し、一覧表示することができます。 

create コマンドの場合と同様に、Azure CLI 2.0 では、すべてのリソースの種類で一環した共通の `az <resource type name> list` 名前付けパターンを使用してリソースを一覧表示することができます。  リソースの一覧を望ましい形式で表示するためのフィルター処理や並べ替えに使用できる、さまざまな出力形式とクエリ オプションがあります。

たとえば、`az vm list` は、保持しているすべての VM の一覧を表示します。   

```azurecli-interactive
az vm list 
```
返される値は、既定で JSON 形式になります (簡潔にするために、出力の一部のみを示しています)。

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...   
]
```

必要に応じて、`--output` オプションを使用して、出力形式を変更することもできます。  `az vm list` コマンドを実行すると、前に作成した Linux と Windows Server の両方の VM と共に、VM の最も一般的なプロパティが表示されます。その際、読みやすい *table* 形式オプションが使用されます。

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

ヘッダーのないテキストベースのタブ区切り形式にするには、*tsv* 出力オプションを使用することができます。  この形式は、grep などの他のテキストベースのツールに出力をパイプ処理する場合に便利です。 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
リソースの一覧表示と出力の書式設定のその他の方法の詳細については、[出力形式](format-output-azure-cli.md)に関する記事を参照してください。

## <a name="querying-resources-and-shaping-outputs"></a>リソースへのクエリ実行と出力の整形

多くの場合、特定の条件に合致するリソースのみに対してクエリを実行できるようにすることが望まれます。  

`list` コマンドの組み込みのサポートにより、リソース グループ名でリソースを簡単にフィルター処理できます。  たとえば、`--ResourceGroup` または `-g` パラメーターを `list` コマンドに渡し、特定のリソース グループ内のリソースだけを取得することができます。


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

クエリをさらに強力にサポートするために、`--query` パラメーターを使用して、"*任意*" の `az` コマンドの結果に対して JMESPath クエリを実行することができます。  JMESPath クエリは、返される任意の結果の出力のフィルター処理にも整形にも使用することができます。

たとえば、次のコマンドを実行すると、"My" という文字列を含む任意のリソース グループ内の任意の VM リソースに対するクエリを実行することができます。

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup, 'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

その後、別の値を出力できる JMESPath クエリの整形機能を使用して、さらに出力を絞り込むこともできます。  たとえば、次のコマンドは、OS が Linux ベースか Windows ベースかを判断するために、VM で使用されている OS ディスクの種類を取得します。

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup, 'MY')].{ VMName:name, OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

Azure CLI での JMESPath サポートは強力です。  使用方法の詳細については、[クエリ](query-azure-cli.md)に関する記事を参照してください。

## <a name="deleting-resources"></a>リソースの削除

Azure CLI で `delete` コマンドを使用すると、不要になったリソースを削除できます。 `create` コマンドの場合と同様に、任意のリソースに対して `delete` コマンドを使用することができます。

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

既定では、削除の確認を求めるメッセージが CLI によって表示されます。  自動化スクリプトでは、このメッセージの表示を抑制することができます。

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

`delete` コマンドを使用して、多数のリソースを一度に削除することもできます。 たとえば、次のコマンドは、この概要チュートリアルのすべてのサンプルで使用してきた "MyResourceGroup" リソース グループ内のすべてのリソースを削除します。

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a>サンプルの入手

Azure CLI の使用方法の詳細については、[Linux VM](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Web アプリ](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json) 用の最も一般的なスクリプトを参照してください。

## <a name="read-the-api-reference-docs"></a>API リファレンス ドキュメントの確認

[API リファレンス](/cli/azure)

## <a name="get-help"></a>問い合わせ

Azure CLI には、組み込みのヘルプ ドキュメントがあります。これは、コマンド ラインから実行できる Web ドキュメントと同じものです。

```azurecli-interactive
az [command-group [command]] -h
```

たとえば、VM に使用できるコマンドやサブグループを確認するには、次のコマンドを使用します。

```azurecli-interactive
az vm -h
```

VM を作成するためのコマンドのヘルプを表示するには、次のコマンドを使用します。

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a>Azure CLI 1.0 からの切り替え

Azure CLI 1.0 (azure.js) の使用方法を既に知っている場合は、コマンドがまったく同じではない部分に気が付くでしょう。
同じタスクを実行するコマンドが大きく異なる場合もあります。
Azure CLI 1.0 から Azure CLI 2.0 への切り替えをサポートするために、こちらの[コマンド対応表](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst)が用意されています。

## <a name="send-us-your-feedback"></a>フィードバックを送信します

```azurecli-interactive
az feedback
```
