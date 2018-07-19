---
title: Azure CLI 2.0 を使用してサインインする
description: 対話形式またはローカル資格情報で Azure CLI 2.0 を使用してサインインします
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/09/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azurecli
ms.service: active-directory
ms.component: authentication
ms.openlocfilehash: a0e05b3306cc273486b1b5fc887ceedbf78cb779
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967760"
---
# <a name="sign-in-with-azure-cli-20"></a>Azure CLI 2.0 を使用してサインインする

Azure CLI を使用して認証を行うには、いくつかの方法があります。 最も簡単に始められるのは、Azure Cloud Shell または `az login` コマンドのいずれかを使用して、ブラウザーから対話形式でサインインする方法です。
アクセス許可が制限されたアカウントである、サービス プリンシパルを使用することをお勧めします。 サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化スクリプトをより安全にすることができます。

プライベートの資格情報はローカルに保存されません。 代わりに、認証トークンが Azure によって生成され、保存されます。 サインイン後、認証トークンは、使用しなくても 14 日間経過するまでは有効です。 その時点で、再認証する必要があります。

サインインすると、CLI コマンドが既定のサブスクリプションに対して実行されます。 複数のサブスクリプションがある場合は、[既定のサブスクリプションを変更](manage-azure-subscriptions-azure-cli.md)できます。

## <a name="interactive-sign-in"></a>対話形式でのサインイン

Azure CLI の既定の認証方法では、サインインに Web ブラウザーとアクセス トークンを使用します。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>コマンド ライン

コマンド ラインで、Azure ユーザー資格情報を指定します。

> [!Note]
> この方法は、Microsoft アカウント、または 2 要素認証が有効になっているアカウントでは機能しません。

```azurecli
az login -u <username> -p <password>
```

> [!IMPORTANT]
> `az login` を対話形式で使用しているときに、コンソールにパスワードが表示されないようにするには、`bash` では `read -s` コマンドを使用します。
>
> ```bash
> read -sp "Azure password: " AZ_PASS && echo && az login -u <username> -p $AZ_PASS
> ```
>
> PowerShell では、`Read-Host -AsSecureString` コマンドレットを使用して、文字列変換をセキュリティで保護します。
>
> ```powershell
> $securePass =  Read-Host "Azure password: " -AsSecureString;
> $AzPass = [Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($securePass));
> az login -u <username> -p $AzPass;
> $AzPass = ""
> ```

## <a name="sign-in-with-a-specific-tenant"></a>特定のテナントでサインインする

複数のテナントを使用する場合は、`--tenant` 引数を使用して、サインインするテナントを選択できます。 この引数の値として、`.onmicrosoft.com` ドメインまたはテナントの Azure オブジェクト ID を指定できます。 対話的にサインインしたり、`--user` 引数と `--password` 引数で資格情報を指定したりできます。

```azurecli
az login --tenant <tenant>
```

## <a name="sign-in-with-a-service-principal"></a>サービス プリンシパルを使ってサインインする

サービス プリンシパルは、特定のユーザーに関連付けられていないアカウントであり、定義済みのロールによってアクセス許可を割り当てることができます。 サービス プリンシパルを使用した認証は、セキュリティで保護されたスクリプトやプログラムを記述するのに最適な方法で、アクセス許可の制限と、ローカルに保存された静的な資格情報の両方を適用できます。 サービス プリンシパルの詳細については、[Azure CLI を使用した Azure サービス プリンシパルの作成](create-an-azure-service-principal-azure-cli.md)に関するページをご覧ください。

サービス プリンシパルでサインインするには、ユーザー名、パスワードまたは証明書 PEM ファイル、およびサービス プリンシパルに関連付けられているテナントを指定します。

```azurecli
az login --service-principal -u <app-url> -p <password-or-cert> --tenant <tenant>
```

tenant 値は、サービス プリンシパルに関連付けられている Azure Active Directory テナントです。 値として、`.onmicrosoft.com` ドメインまたはテナントの Azure オブジェクト ID を指定できます。
現在アクティブなアカウントのテナント オブジェクト ID を取得するには、次のコマンドを使用します。

```azurecli-interactive
az account show --query 'tenantId' -o tsv
```

> [!IMPORTANT]
> `az login` を対話形式で使用しているときに、コンソールにパスワードが表示されないようにするには、`bash` では `read -s` コマンドを使用します。
>
> ```bash
> read -sp "Azure password: " AZ_PASS && echo && az login --service-principal -u <app-url> -p $AZ_PASS --tenant <tenant>
> ```
>
> PowerShell では、`Read-Host -AsSecureString` コマンドレットを使用して、文字列変換をセキュリティで保護します。
>
> ```powershell
> $securePass =  Read-Host "Azure password: " -AsSecureString;
> $AzPass = [Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($securePass));
> az login --service-principal -u <app-url> -p $AzPass --tenant <tenant>;
> $AzPass = ""
> ```
