---
title: Konfigurere A-skat-afregningsperioder for TDS-skattetypen
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere afregningsperioder for afgifter fratrukket ved kilden (TDS).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023105"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="e67f2-103">Konfigurere A-skat-afregningsperioder for TDS-skattetypen</span><span class="sxs-lookup"><span data-stu-id="e67f2-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e67f2-104">Dette emne indeholder en forklaring på, hvordan du kan konfigurere afregningsperioder for afgifter fratrukket ved kilden (TDS).</span><span class="sxs-lookup"><span data-stu-id="e67f2-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="e67f2-105">Gå til **Moms \> Indirekte skatter \> A-skat \> Afregningsperioder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="e67f2-106">[![Siden Afregningsperioder for A-skat](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="e67f2-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="e67f2-107">Vælg **TDS** i feltet **Skattetype** for at konfigurere afregningsperioder for TDS-skattetypen.</span><span class="sxs-lookup"><span data-stu-id="e67f2-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="e67f2-108">Vælg **Ny** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="e67f2-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="e67f2-109">I feltet **Afregningsperiode** skal du angive et navn for TDS-afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="e67f2-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="e67f2-110">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="e67f2-111">Vælg den TDS-myndighed, som du definerer TDS-afregningsperioden for, i feltet **A-skattemyndighed**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="e67f2-112">Vælg typen af periodeinterval for TDS-afregningsperioden i feltet **Periodeinterval** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="e67f2-113">Angiv antallet af enheder for periodeintervaltypen i feltet **Antal enheder**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="e67f2-114">Vælg startdatoen for TDS-afregningsperioden i feltet **Fra dato** i oversigtspanelet **Perioder**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="e67f2-115">Vælg slutdatoen i feltet **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="e67f2-116">Hvis du vil oprette en efterfølgende TDS-afregningsperiode for en eksisterende periode baseret på periodeintervallet og periodeenhederne, skal du vælge **Ny periode**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="e67f2-117">Hvis du vil have vist detaljerede oplysninger om den periodiske TDS-afregning, der køres for en bestemt afregningsperiode, skal du vælge **A-skattebetalinger** for at åbne siden **Betaling af A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e67f2-118">Du kan køre den periodiske TDS-udligningsproces ved at gå til **Finans \> Periodisk \> A-skat \> Betaling af A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e67f2-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="e67f2-119">[![Siden Betaling af A-skat](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="e67f2-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="e67f2-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e67f2-120">Close the page.</span></span>
