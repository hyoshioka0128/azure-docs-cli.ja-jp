---
title: "Azure CLI 2.0 を使用してログインする"
description: "Linux、Mac、または Windows 上で Azure 2.0 CLI を使用してログインします。"
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
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: fea893ebd55811527e0e92375ffc081a52cdbb57
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: ja-JP
---
# <a name="log-in-with-azure-cli-20"></a>Azure CLI 2.0 を使用してログインする

Azure CLI を使用してログインと認証を行うには、いくつかの方法があります。 最も簡単に始められるのは、ブラウザーから対話形式でログインするか、コマンド ラインでログインする方法です。 お勧めは、サービス プリンシパルを使用する方法です。サービス プリンシパルは、リソースの操作に使用できる非対話型のアカウントを作成する方法を提供します。 サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化スクリプトをより安全にすることができます。

CLI で実行するコマンドは、既定のサブスクリプションに対して実行されます。  複数のサブスクリプションがある場合は、[既定のサブスクリプションを確認](manage-azure-subscriptions-azure-cli.md)し、それを適切に変更することができます。

## <a name="interactive-log-in"></a>対話形式のログイン

Web ブラウザーから対話形式でログインします。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>コマンド ライン

コマンド ラインで、資格情報を指定します。

> [!Note]
> この方法は、Microsoft アカウント、または 2 要素認証が有効になっているアカウントでは機能しません。

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>サービス プリンシパルによるログイン

サービス プリンシパルは、Azure Active Directory を使用してルールを適用できるユーザー アカウントに似ています。
サービス プリンシパルによる認証は、リソースを操作するスクリプトまたはアプリケーションからの Azure リソースの使用を保護するための最適な方法です。
ユーザーに持たせるロールを、コマンドの `az role` セットを通じて定義します。
サービス プリンシパルのロールの詳細と例については、[az role のリファレンス記事](https://docs.microsoft.com/cli/azure/role.md)を参照してください。

1. まだサービス プリンシパルがない場合は、サービス プリンシパルを[作成](create-an-azure-service-principal-azure-cli.md)します。

1. サービス プリンシパルを使用してログインします。

   ```azurecli
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   テナントを取得するには、対話形式でログインし、サブスクリプションから tenantId を取得します。

   ```azurecli
   az login
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```