---
title: "Azure CLI 2.0 を使用して Azure サブスクリプションを管理する"
description: "Linux、Mac、または Windows 上で Azure CLI 2.0 を使用して Azure サブスクリプションを管理します。"
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 9f03e52fa72a8dbd5753904839a833db01ffb59b
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2018
---
# <a name="manage-multiple-azure-subscriptions"></a>複数の Azure サブスクリプションの管理

ほとんどの Azure ユーザーは、サブスクリプションを 1 つしか持っていません。 ただし、複数の組織に属している場合や、組織がグループ間で特定のリソースへのアクセスを分けている場合、Azure に複数のサブスクリプションを持っていることがあります。 複数のサブスクリプションは、CLI を使用して簡単に管理することができ、サブスクリプションを選択して操作を実行できます。

## <a name="tenants-users-and-subscriptions"></a>テナント、ユーザー、サブスクリプション

Azure におけるテナント、ユーザー、サブスクリプションが混同されている場合があります。 一般に、"_テナント_" とは、組織全体を含む Azure Active Directory エンティティです。 このテナントは、少なくとも 1 つの "_サブスクリプション_" を持ち、少なくとも 1 人の "_ユーザー_" が含まれます。 ユーザーとは個人であり、1 つのテナント (ユーザーが属している組織) にのみ関連付けられています。 ユーザーは、Azure にログインしてリソースをプロビジョニングおよび使用するアカウントです。 1 人のユーザーが複数の "_サブスクリプション_" にアクセスできる場合があります。サブスクリプションとは、Azure をはじめとするクラウド サービスを使用するための Microsoft との契約です。 各リソースは、サブスクリプションに関連付けられています。

テナント、ユーザー、サブスクリプションの違いの詳細については、[Azure クラウド用語集](/azure/azure-glossary-cloud-terminology)のページをご覧ください。
Azure Active Directory テナントに新しいサブスクリプションを追加する方法については、「[Azure サブスクリプションを Azure Active Directory に追加する方法](/azure/active-directory/active-directory-how-subscriptions-associated-directory)」をご覧ください。

## <a name="working-with-multiple-subscriptions"></a>複数のサブスクリプションの操作

サブスクリプションに含まれているリソースにアクセスするには、アクティブなサブスクリプションを切り替える必要があります。 サブスクリプションのすべての操作は、`az account` コマンドを使用して実行します。このコマンドは、個人アカウントを参照するのではなく、サブスクリプションが表すサービス契約を参照します。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

使用可能なサブスクリプションの操作を開始するには、アカウントで使用できるサブスクリプションの一覧を取得します。

```azurecli-interactive
az account list --output table
```

```Output
Name                                         CloudName    SubscriptionId                        State     IsDefault
-------------------------------------------  -----------  ------------------------------------  --------  -----------
My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
```

アクティブなサブスクリプションを変更するには、`az account set` を使用します。

```azurecli-interactive
az account set --subscription "My Demos"
```

サブスクリプションは、サブスクリプション ID またはサブスクリプション名を使用して選択できます。
