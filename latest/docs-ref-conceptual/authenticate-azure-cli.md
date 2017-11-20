---
title: "Azure CLI 2.0 を使用してログインする"
description: "Linux、Mac、または Windows 上で Azure 2.0 CLI を使用してログインします。"
keywords: "Azure CLI 2.0, ログイン, Azure CLI, 認証, 承認, ログインする"
author: sptramer
ms.author: stttramer
manager: routlaw
ms.date: 11/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: dd05868f7378673836f47e743ed4088f2efd3dca
ms.sourcegitcommit: 5db22de971cf3983785cb209d92cbed1bbd69ecf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2017
---
# <a name="log-in-with-azure-cli-20"></a>Azure CLI 2.0 を使用してログインする

Azure CLI を使用してログインと認証を行うには、いくつかの方法があります。 最も簡単に始められるのは、ブラウザーから対話形式でログインするか、コマンド ラインでログインする方法です。 お勧めは、サービス プリンシパルを使用する方法です。サービス プリンシパルは、リソースの操作に使用できる非対話型のアカウントを作成する方法を提供します。 サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化スクリプトをより安全にすることができます。 

プライベートの資格情報はローカルに保存されません。 代わりに、認証トークンが Azure によって生成され、保存されます。 ログイン後、ローカルのログイン トークンは、使用しなくても 14 日間経過するまでは有効です。 その時点で、再認証する必要があります。

ログインすると、CLI コマンドが既定のサブスクリプションに対して実行されます。 複数のサブスクリプションがある場合は、[既定のサブスクリプションを変更](manage-azure-subscriptions-azure-cli.md)することもできます。

## <a name="interactive-log-in"></a>対話形式のログイン

Web ブラウザーから対話形式でログインします。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>コマンド ライン

コマンド ラインで、資格情報を指定します。

> [!Note]
> この方法は、Microsoft アカウント、または 2 要素認証が有効になっているアカウントでは機能しません。

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>サービス プリンシパルによるログイン

サービス プリンシパルは、Azure Active Directory を使用してルールを適用できるユーザー アカウントに似ています。
サービス プリンシパルによる認証は、リソースを操作するスクリプトまたはアプリケーションからの Azure リソースの使用を保護するための最適な方法です。 使用可能なサービス プリンシパルがなく、サービス プリンシパルを作成する場合は、[Azure CLI を使用した Azure サービス プリンシパルの作成](create-an-azure-service-principal-azure-cli.md)に関する記事をご覧ください。

サービス プリンシパルでログインするには、ユーザー名、パスワードまたは証明書 PEM ファイル、およびサービス プリンシパルに関連付けられているテナントを指定します。

```azurecli-interactive
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

tenant 値は、サービス プリンシパルに関連付けられている Azure Active Directory テナントです。 値として、.onmicrosoft.com ドメイン、またはテナントの Azure オブジェクト ID を指定できます。
現在のログインのテナント オブジェクト ID を取得するには、次のコマンドを使用します。

```azurecli
az account show --query 'tenanatId' -o tsv
```

