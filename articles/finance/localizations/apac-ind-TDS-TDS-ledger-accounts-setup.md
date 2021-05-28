---
title: Konfigurere finanskonti for kildeskat
description: Dette emne beskriver, hvordan du kan konfigurere finanskonti for funktionen til kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023117"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="1080f-103">Konfigurere finanskonti for kildeskat</span><span class="sxs-lookup"><span data-stu-id="1080f-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1080f-104">Dette emne beskriver, hvordan du kan konfigurere finanskonti for funktionen til kildeskat (TDS – Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="1080f-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="1080f-105">Du kan bruge siden **Kontoplan** til at konfigurere finanskonti til kildeskat.</span><span class="sxs-lookup"><span data-stu-id="1080f-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="1080f-106">Gå til **Finans \> Kontoplan \> Konti \> Hovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="1080f-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="1080f-107">Vælg **Alt+N** under fanen **Oversigt** for at oprette en finanskonto for kildeskat, og angiv de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1080f-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="1080f-108">Vælg **A-skat** i feltet **Bogføringstype** under fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="1080f-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="1080f-109">Finanskonti af bogføringstypen **A-skat** kan kun defineres som debitorkonti, der bruges til bogføring af det skyldige skattebeløb for en kildeskattekode.</span><span class="sxs-lookup"><span data-stu-id="1080f-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="1080f-110">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1080f-110">Close the page.</span></span>
