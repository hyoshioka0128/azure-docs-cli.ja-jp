---
title: Azure CLI を使用して Azure サブスクリプションを管理する
description: Azure CLI を使用して Azure サブスクリプションを管理します。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/15/2018
ms.topic: conceptual
ms.produdct: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.service: active-directory
ms.openlocfilehash: fdc8ffca38a6a581ae63b0518df72f6e09110d07
ms.sourcegitcommit: 1a38729d6ae93c49137b3d49b6a9ec8a75eff190
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36262711"
---
# <a name="manage-multiple-azure-subscriptions"></a>複数の Azure サブスクリプションの管理

ほとんどの Azure ユーザーは、サブスクリプションを 1 つしか持っていません。 ただし、複数の組織に属している場合や、組織がグループ間で特定のリソースへのアクセスを分けている場合、Azure に複数のサブスクリプションを持っていることがあります。 複数のサブスクリプションを CLI を使用して簡単に管理するには、すべてのコマンドに対してグローバル サブスクリプションを設定するか、コマンドごとにサブスクリプションを選択します。

## <a name="tenants-users-and-subscriptions"></a>テナント、ユーザー、サブスクリプション

Azure におけるテナント、ユーザー、サブスクリプションが混同されている場合があります。 "_テナント_" とは、組織全体を含む Azure Active Directory エンティティです。 このテナントは、少なくとも 1 つの "_サブスクリプション_" を持ち、少なくとも 1 人の "_ユーザー_" が含まれます。 ユーザーとは個人であり、1 つのテナント (ユーザーが属している組織) にのみ関連付けられています。 ユーザーは、Azure にログインしてリソースをプロビジョニングおよび使用するアカウントです。
1 人のユーザーが複数の "_サブスクリプション_" にアクセスできる場合があります。サブスクリプションとは、Azure をはじめとするクラウド サービスを使用するための Microsoft との契約です。 各リソースは、サブスクリプションに関連付けられています。

テナント、ユーザー、サブスクリプションの違いの詳細については、[Azure クラウド用語集](/azure/azure-glossary-cloud-terminology)のページをご覧ください。  Azure Active Directory テナントに新しいサブスクリプションを追加する方法については、「[Azure サブスクリプションを Azure Active Directory に追加する方法](/azure/active-directory/active-directory-how-subscriptions-associated-directory)」をご覧ください。
複数のテナントを使用するときは、特定のテナントへのサインインが必要になる場合があります。 これを行うには、[Azure CLI を使用したサインイン](/cli/azure/authenticate-azure-cli)に関するページをご覧ください。

## <a name="work-with-multiple-subscriptions"></a>複数のサブスクリプションの操作

サブスクリプションに含まれているリソースにアクセスするには、アクティブなサブスクリプションを切り替える必要があります。 サブスクリプションの切り替えは、[az account set](/cli/azure/account#az-account-set) を使用してすべての Azure CLI コマンドに対して実行するか、`--subscription` 引数を使用してコマンドごとに実行します。

開始するには、利用可能なサブスクリプションの一覧が必要です。 これを取得するには、[az account list](/cli/azure/account#az-account-list) コマンドを使用します。

```azurecli-interactive
az account list --output table
```

アクティブなサブスクリプションをグローバルに変更するには、`az account set` を使用して、サブスクリプション ID またはサブスクリプション名を指定します。

```azurecli-interactive
az account set --subscription "My Demos"
```

コマンドに対して特定のサブスクリプションを使用するには、`--subscription` 引数を使用するだけです。 この引数には、サブスクリプション ID またはサブスクリプション名を指定します。

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
