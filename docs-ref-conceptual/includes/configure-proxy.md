---
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/28/2019
ms.topic: include
ms.prod: azure
ms.technology: azure-cli
ms.openlocfilehash: 676f33377a4e7122941bc789c51465b7f34aa1d3
ms.sourcegitcommit: 08043c47d3ccf23522b91e6bba3932e312c04c7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "66516262"
---
<span data-ttu-id="e3e6e-101">プロキシのために外部リソースに接続できない場合、シェルに `HTTP_PROXY` および `HTTPS_PROXY` 変数を正しく設定していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-101">If you're unable to connect to an external resource due to a proxy, make sure that you've correctly set the `HTTP_PROXY` and `HTTPS_PROXY` variables in your shell.</span></span> <span data-ttu-id="e3e6e-102">これらのプロキシ用にどのホストとポートを使用するかについては、システム管理者に問い合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-102">You will need to contact your system administrator to know what host(s) and port(s) to use for these proxies.</span></span>

<span data-ttu-id="e3e6e-103">これらの値は、多くの Linux プログラムで使用されます (インストール プロセスで使用されるものも含む)。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-103">These values are respected by many Linux programs, including those which are used in the install process.</span></span> <span data-ttu-id="e3e6e-104">これらの値を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-104">To set these values:</span></span>

```bash
# No auth
export HTTP_PROXY=http://[proxy]:[port]
export HTTPS_PROXY=https://[proxy]:[port]

# Basic auth
export HTTP_PROXY=http://[username]:[password]@[proxy]:[port]
export HTTPS_PROXY=https://[username]:[password]@[proxy]:[port]
```

> [!IMPORTANT]
> <span data-ttu-id="e3e6e-105">プロキシの内側にいる場合は、これらのシェル変数を CLI によって Azure サービスに接続するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-105">If you are behind a proxy, these shell variables must be set to connect to Azure services with the CLI.</span></span>
> <span data-ttu-id="e3e6e-106">基本認証を使用しない場合は、`.bashrc` ファイルでこれらの変数をエクスポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-106">If you are not using basic auth, it's recommended to export these variables in your `.bashrc` file.</span></span>
> <span data-ttu-id="e3e6e-107">常に、貴社のビジネスのセキュリティ ポリシーと、システム管理者の要件に従ってください。</span><span class="sxs-lookup"><span data-stu-id="e3e6e-107">Always follow your business' security policies and the requirements of your system administrator.</span></span>
