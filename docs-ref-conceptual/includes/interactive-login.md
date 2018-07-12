---
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/02/2018
ms.topic: include
ms.openlocfilehash: b6eb0e478ebfbbeb6e2b52d0f2b3309cf2281940
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967930"
---
1. <span data-ttu-id="b2207-101">`login` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="b2207-101">Run the `login` command.</span></span>

    ```azurecli-interactive
    az login
    ```

    <span data-ttu-id="b2207-102">CLI によって既定のブラウザーを確認し、アクセスして、開くことができる場合は、サインイン ページにすぐにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="b2207-102">If the CLI can determine your default browser and has access to open it, it will do so and direct you  immediately to a sign in page.</span></span>

    <span data-ttu-id="b2207-103">それ以外の場合は、ブラウザー ページを開いて、お使いのブラウザーで [https://aka.ms/devicelogin](https://aka.ms/devicelogin) に移動した後、コマンド ラインの指示に従って認証コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="b2207-103">Otherwise, you need to open a browser page and follow the instructions on the command line to enter an  authorization code after navigating to [https://aka.ms/devicelogin](https://aka.ms/devicelogin) in your browser.</span></span>

2. <span data-ttu-id="b2207-104">ブラウザーでアカウントの資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="b2207-104">Sign in with your account credentials in the browser.</span></span>