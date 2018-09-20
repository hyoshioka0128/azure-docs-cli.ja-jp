---
title: Azure CLI 2.0 を使用してサインインする
description: 対話形式またはローカル資格情報で Azure CLI 2.0 を使用してサインインします
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azurecli
ms.service: active-directory
ms.component: authentication
ms.openlocfilehash: ef77f407284752ad4f4a1585f8a4036b32b3eb1b
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388322"
---
# <a name="sign-in-with-azure-cli-20"></a>Azure CLI 2.0 を使用してサインインする

Azure CLI には、いくつかの認証の種類があります。 [Azure Cloud Shell](/azure/cloud-shell/overview) を使用すると自動的にログインできるため、最も簡単に作業を開始できます。 ローカルでは、ご使用のブラウザーで `az login` コマンドを使用して、対話形式でサインインできます。 スクリプトを記述するときは、サービス プリンシパルを使用することをお勧めします。 サービス プリンシパルに必要とされる適切なアクセス許可だけを付与することによって、自動化をより安全に維持できます。

CLI によってサインイン情報が保存されることは、まったくありません。 代わりに、認証トークンが Azure によって生成され、保存されます。 サインイン後、認証トークンは、使用しなくても 90 日経過するまでは有効です。

サインインすると、CLI コマンドが既定のサブスクリプションに対して実行されます。 複数のサブスクリプションがある場合は、[既定のサブスクリプションを変更](manage-azure-subscriptions-azure-cli.md)できます。

## <a name="sign-in-interactively"></a>対話操作でサインインする

Azure CLI の既定の認証方法では、サインインに Web ブラウザーとアクセス トークンを使用します。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="sign-in-with-credentials-on-the-command-line"></a>コマンド ラインで資格情報を使用してサインインする

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

`--tenant` 引数を使用すると、サインインするテナントを選択できます。 この引数の値として、`.onmicrosoft.com` ドメインまたはテナントの Azure オブジェクト ID を指定できます。 対話形式のサインイン方法とコマンドラインによるサインイン方法の両方で、`--tenant` を使用できます。

```azurecli
az login --tenant <tenant>
```

## <a name="sign-in-with-a-service-principal"></a>サービス プリンシパルを使ってサインインする

サービス プリンシパルは、特定のユーザーに関連付けられていないアカウントであり、定義済みのロールによってアクセス許可を割り当てることができます。 サービス プリンシパルを使用した認証は、セキュリティで保護されたスクリプトやプログラムを記述するのに最適な方法で、アクセス許可の制限と、ローカルに保存された静的な資格情報の両方を適用できます。 サービス プリンシパルの詳細については、[Azure CLI を使用した Azure サービス プリンシパルの作成](create-an-azure-service-principal-azure-cli.md)に関するページをご覧ください。

サービス プリンシパルを使ってサインインするには、以下が必要です。

* サービス プリンシパルに関連付けられている URL または名前
* サービス プリンシパルのパスワード、またはサービス プリンシパルを PEM 形式で作成するために使用する X509 証明書
* `.onmicrosoft.com` ドメインまたは Azure オブジェクト ID として、サービス プリンシパルに関連付けられているテナント

```azurecli
az login --service-principal -u <app-url> -p <password-or-cert> --tenant <tenant>
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
