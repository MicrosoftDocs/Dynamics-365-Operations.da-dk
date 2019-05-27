---
title: Manuel afskrivning
description: Denne artikel indeholder en oversigt over den manulle afskrivningsmetode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e385e60e10146a0855a467af57a0a31fcc53bd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558729"
---
# <a name="manual-depreciation"></a><span data-ttu-id="f21ee-103">Manuel afskrivning</span><span class="sxs-lookup"><span data-stu-id="f21ee-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f21ee-104">Denne artikel indeholder en oversigt over den manulle afskrivningsmetode.</span><span class="sxs-lookup"><span data-stu-id="f21ee-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="f21ee-105">Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Manuel** i feltet **Metode** på siden **Afskrivningsprofiler**, bestemmes den afskrivning, der tildeles afskrivningsprofilen for anlægsaktiver, af den procentdel, du har angivet for hvert interval i kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="f21ee-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="f21ee-106">De intervaller, som du angiver procentdele for, bogføres i overensstemmelse med den værdi, du vælger i feltet **Periodefrekvens** i oversigtspanelet **Generelt** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="f21ee-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="f21ee-107">Her er de værdier, du kan vælge imellem:</span><span class="sxs-lookup"><span data-stu-id="f21ee-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="f21ee-108">Årligt</span><span class="sxs-lookup"><span data-stu-id="f21ee-108">Yearly</span></span>
-   <span data-ttu-id="f21ee-109">Månedligt</span><span class="sxs-lookup"><span data-stu-id="f21ee-109">Monthly</span></span>
-   <span data-ttu-id="f21ee-110">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="f21ee-110">Quarterly</span></span>
-   <span data-ttu-id="f21ee-111">Halvårlig</span><span class="sxs-lookup"><span data-stu-id="f21ee-111">Half-Yearly</span></span>
-   <span data-ttu-id="f21ee-112">Dagligt</span><span class="sxs-lookup"><span data-stu-id="f21ee-112">Daily</span></span>

<span data-ttu-id="f21ee-113">Når du har valgt periodefrekvensen, skal du klikke på **Manuelle planer** og oprette procentdele for hvert posteringsinterval.</span><span class="sxs-lookup"><span data-stu-id="f21ee-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="f21ee-114">De manuelle planer og posteringsintervaller definerer tilsammen afskrivningsbeløbet som vist i eksemplerne senere i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="f21ee-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="f21ee-115">Manuel afskrivning beregnes altid som en procentdel af anskaffelsesprisen.</span><span class="sxs-lookup"><span data-stu-id="f21ee-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="f21ee-116">Ved manuel afskrivning skal de procentdele, som du angiver for afskrivningsintervallerne, ikke udgøre en samlet procent på 100.</span><span class="sxs-lookup"><span data-stu-id="f21ee-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="f21ee-117">Manuel afskrivning er en fleksibel afskrivningsmetode, der ofte bruges til at definere en ekstraordinær afskrivningsprofil på siden **Bøger**, f.eks. en ikke-periodisk afskrivning til et specielt formål (f.eks. skat).</span><span class="sxs-lookup"><span data-stu-id="f21ee-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="f21ee-118">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f21ee-118">Examples</span></span>
<span data-ttu-id="f21ee-119">Anskaffelsesprisen: 11.000,00 forventet scrapværdi: 1.000,00 I følgende tabel vises de intervaller og procentdele, som du har angivet på siden **Planer for anlægsaktivets afskrivningsprofil**.</span><span class="sxs-lookup"><span data-stu-id="f21ee-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="f21ee-120">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="f21ee-120">Interval number</span></span> | <span data-ttu-id="f21ee-121">Procentdel</span><span class="sxs-lookup"><span data-stu-id="f21ee-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="f21ee-122">1</span><span class="sxs-lookup"><span data-stu-id="f21ee-122">1</span></span>               | <span data-ttu-id="f21ee-123">10,00</span><span class="sxs-lookup"><span data-stu-id="f21ee-123">10.00</span></span>      |
| <span data-ttu-id="f21ee-124">2</span><span class="sxs-lookup"><span data-stu-id="f21ee-124">2</span></span>               | <span data-ttu-id="f21ee-125">50,00</span><span class="sxs-lookup"><span data-stu-id="f21ee-125">50.00</span></span>      |
| <span data-ttu-id="f21ee-126">3</span><span class="sxs-lookup"><span data-stu-id="f21ee-126">3</span></span>               | <span data-ttu-id="f21ee-127">8,00</span><span class="sxs-lookup"><span data-stu-id="f21ee-127">8.00</span></span>       |

<span data-ttu-id="f21ee-128">I følgende tabel vises, hvordan afskrivningen beregnes for hvert interval.</span><span class="sxs-lookup"><span data-stu-id="f21ee-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="f21ee-129">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="f21ee-129">Interval number</span></span> | <span data-ttu-id="f21ee-130">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="f21ee-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="f21ee-131">Den bogførte nettoværdi ved intervallets afslutning</span><span class="sxs-lookup"><span data-stu-id="f21ee-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f21ee-132">1</span><span class="sxs-lookup"><span data-stu-id="f21ee-132">1</span></span>                | <span data-ttu-id="f21ee-133">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="f21ee-134">10.000 (11.000 - 1.000)</span><span class="sxs-lookup"><span data-stu-id="f21ee-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="f21ee-135">2</span><span class="sxs-lookup"><span data-stu-id="f21ee-135">2</span></span>                | <span data-ttu-id="f21ee-136">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="f21ee-137">5.000 (10.000 - 5.000)</span><span class="sxs-lookup"><span data-stu-id="f21ee-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="f21ee-138">3</span><span class="sxs-lookup"><span data-stu-id="f21ee-138">3</span></span>                | <span data-ttu-id="f21ee-139">(11.000 - 1.000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="f21ee-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="f21ee-140">4.200 (5.000 - 800)</span><span class="sxs-lookup"><span data-stu-id="f21ee-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="f21ee-141">Hvis du vælger **Månedligt** i feltet **Periodefrekvens**, opretter du 12 manuelle planlagte intervaller.</span><span class="sxs-lookup"><span data-stu-id="f21ee-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="f21ee-142">I følgende tabel vises afskrivningsbeløbene for de første to intervaller.</span><span class="sxs-lookup"><span data-stu-id="f21ee-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="f21ee-143">Interval</span><span class="sxs-lookup"><span data-stu-id="f21ee-143">Interval</span></span> | <span data-ttu-id="f21ee-144">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="f21ee-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="f21ee-145">Januar</span><span class="sxs-lookup"><span data-stu-id="f21ee-145">January</span></span>  | <span data-ttu-id="f21ee-146">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="f21ee-147">Februar</span><span class="sxs-lookup"><span data-stu-id="f21ee-147">February</span></span> | <span data-ttu-id="f21ee-148">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="f21ee-149">Hvis du vælger <strong>Halvårlig</strong> i feltet *<strong><em>Periodefrekvens</em>*</strong>, opretter du to manuelle planlagte intervaller.</span><span class="sxs-lookup"><span data-stu-id="f21ee-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="f21ee-150">I følgende tabel vises afskrivningsbeløbene for disse to intervaller.</span><span class="sxs-lookup"><span data-stu-id="f21ee-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="f21ee-151">Interval</span><span class="sxs-lookup"><span data-stu-id="f21ee-151">Interval</span></span>    | <span data-ttu-id="f21ee-152">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="f21ee-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="f21ee-153">30. juni</span><span class="sxs-lookup"><span data-stu-id="f21ee-153">June 30</span></span>     | <span data-ttu-id="f21ee-154">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="f21ee-155">31. december</span><span class="sxs-lookup"><span data-stu-id="f21ee-155">December 31</span></span> | <span data-ttu-id="f21ee-156">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="f21ee-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="f21ee-157">Den samlede procentdel for alle intervaller behøver ikke være 100.</span><span class="sxs-lookup"><span data-stu-id="f21ee-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="f21ee-158">Men du modtager en meddelelse, hvis værdien i feltet **Akkumuleret procent** på siden **Planer for anlægsaktivets afskrivningsprofil** ikke er **100**.</span><span class="sxs-lookup"><span data-stu-id="f21ee-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



