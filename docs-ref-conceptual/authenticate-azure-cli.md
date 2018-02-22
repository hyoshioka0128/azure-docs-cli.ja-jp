---
title: "Azure CLI 2.0 を使用してログインする"
description: "対話形式またはローカル資格情報で Azure CLI 2.0 を使用してログインします"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a140f8f54ad72f7f3b5e2d63e2300d0aa2c061ac
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="log-in-with-azure-cli-20"></a>Azure CLI 2.0 を使用してログインする

Azure CLI を使用してログインと認証を行うには、いくつかの方法があります。 最も簡単に始められるのは、Azure Cloud Shell または `az login` コマンドのいずれかを使用して、ブラウザーから対話形式でログインする方法です。
アクセス許可が制限されたアカウントである、サービス プリンシパルを使用することをお勧めします。 サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化スクリプトをより安全にすることができます。

プライベートの資格情報はローカルに保存されません。 代わりに、認証トークンが Azure によって生成され、保存されます。 ログイン後、ログイン トークンは、使用しなくても 14 日間経過するまでは有効です。 その時点で、再認証する必要があります。

ログインすると、CLI コマンドが既定のサブスクリプションに対して実行されます。 複数のサブスクリプションがある場合は、[既定のサブスクリプションを変更](manage-azure-subscriptions-azure-cli.md)できます。

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

サービス プリンシパルは、特定のユーザーに関連付けられていないアカウントであり、定義済みのロールによってアクセス許可を割り当てることができます。 サービス プリンシパルを使用した認証は、セキュリティで保護されたスクリプトやプログラムを記述するのに最適な方法で、アクセス許可の制限と、ローカルに保存された静的な資格情報の両方を適用できます。 サービス プリンシパルの詳細については、[Azure CLI を使用した Azure サービス プリンシパルの作成](create-an-azure-service-principal-azure-cli.md)に関するページをご覧ください。

サービス プリンシパルでログインするには、ユーザー名、パスワードまたは証明書 PEM ファイル、およびサービス プリンシパルに関連付けられているテナントを指定します。

```azurecli
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

tenant 値は、サービス プリンシパルに関連付けられている Azure Active Directory テナントです。 値として、.onmicrosoft.com ドメインまたはテナントの Azure オブジェクト ID を指定できます。
現在のログインのテナント オブジェクト ID を取得するには、次のコマンドを使用します。

```azurecli
az account show --query 'tenantId' -o tsv
```

