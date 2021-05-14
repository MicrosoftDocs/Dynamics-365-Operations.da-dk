---
title: TaxTrans-post er ikke genereret
description: Dette emne indeholder fejlfindingsoplysninger, som kan hjælpe, når der ikke er genereret en TaxTrans-post.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947613"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="40002-103">TaxTrans-post er ikke genereret</span><span class="sxs-lookup"><span data-stu-id="40002-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40002-104">Hvis du vælger **Bogført moms** for en transaktion, men siden **Bogført moms** enten ikke viser nogen momslinjer eller mangler en momslinje, er **TaxTrans**-posten muligvis ikke blevet genereret.</span><span class="sxs-lookup"><span data-stu-id="40002-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="40002-105">[![Siden Bogført moms, der ikke indeholder linjeelementer](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="40002-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="40002-106">Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.</span><span class="sxs-lookup"><span data-stu-id="40002-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="40002-107">Kontrollere momsen, før du bogfører transaktionen</span><span class="sxs-lookup"><span data-stu-id="40002-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="40002-108">Før du bogfører transaktionen, skal du vælge **Moms** på siden **Bogføring af faktura** for at kontrollere beregningen.</span><span class="sxs-lookup"><span data-stu-id="40002-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="40002-109">[![Knappen Moms på siden Bogføring af faktura](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="40002-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="40002-110">Gennemse resultatet af beregningen på siden **Midlertidige posteringer af moms**.</span><span class="sxs-lookup"><span data-stu-id="40002-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="40002-111">Hvis der ikke er beregnet moms, skal du se i [Moms er ikke beregnet, eller momsbeløb er nul](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="40002-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="40002-112">Find TaxTrans-posten i al bogført moms</span><span class="sxs-lookup"><span data-stu-id="40002-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="40002-113">Gå til **Moms** \> **Forespørgsler og rapporter** \> **Momsforespørgsler** > **Bogført moms**.</span><span class="sxs-lookup"><span data-stu-id="40002-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="40002-114">Vælg filtersymbolet i kolonneoverskriften **Bilag** for at finde posten **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="40002-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="40002-115">Hvis du finder de momsposter, du søger efter, skal du kontrollere datoen.</span><span class="sxs-lookup"><span data-stu-id="40002-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="40002-116">Hvis datoen afviger fra datoen i kladdehovedet, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="40002-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="40002-117">[![Siden Bogført moms](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="40002-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="40002-118">Løse fejl for at kontrollere oplysninger</span><span class="sxs-lookup"><span data-stu-id="40002-118">Debug to check details</span></span>

1. <span data-ttu-id="40002-119">Yderligere oplysninger om, hvordan du kan løse fejl og finde ud af, om **TmpTaxWorkTrans** og **TaxUncommitted** er korrekt genereret, finder du i [Feltværdi i TaxTrans er forkert](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="40002-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="40002-120">Hvis **TaxTmpWorkTrans** eller **TaxUncommitted** er genereret korrekt, skal du tilføje et pausepunkt ved **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** for at finde årsagen til, at **TaxTrans** ikke er indsat.</span><span class="sxs-lookup"><span data-stu-id="40002-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="40002-121">[![Pausepunkter tilføjet i kode](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="40002-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="40002-122">[![Resultater af tilføjede pausepunkter](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="40002-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="40002-123">Afgøre, om der findes tilpasninger</span><span class="sxs-lookup"><span data-stu-id="40002-123">Determine whether customization exists</span></span>

<span data-ttu-id="40002-124">Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="40002-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="40002-125">Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="40002-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
