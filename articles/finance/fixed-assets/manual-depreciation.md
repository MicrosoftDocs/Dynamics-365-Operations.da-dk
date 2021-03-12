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
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228e6c94042942a26793eb0bebc1186dd4767e7f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969023"
---
# <a name="manual-depreciation"></a><span data-ttu-id="45933-103">Manuel afskrivning</span><span class="sxs-lookup"><span data-stu-id="45933-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45933-104">Denne artikel indeholder en oversigt over den manulle afskrivningsmetode.</span><span class="sxs-lookup"><span data-stu-id="45933-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="45933-105">Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Manuel** i feltet **Metode** på siden **Afskrivningsprofiler**, bestemmes den afskrivning, der tildeles afskrivningsprofilen for anlægsaktiver, af den procentdel, du har angivet for hvert interval i kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="45933-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="45933-106">De intervaller, som du angiver procentdele for, bogføres i overensstemmelse med den værdi, du vælger i feltet **Periodefrekvens** i oversigtspanelet **Generelt** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="45933-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="45933-107">Her er de værdier, du kan vælge imellem:</span><span class="sxs-lookup"><span data-stu-id="45933-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="45933-108">Årligt</span><span class="sxs-lookup"><span data-stu-id="45933-108">Yearly</span></span>
-   <span data-ttu-id="45933-109">Månedligt</span><span class="sxs-lookup"><span data-stu-id="45933-109">Monthly</span></span>
-   <span data-ttu-id="45933-110">Kvartalsvis</span><span class="sxs-lookup"><span data-stu-id="45933-110">Quarterly</span></span>
-   <span data-ttu-id="45933-111">Halvårlig</span><span class="sxs-lookup"><span data-stu-id="45933-111">Half-Yearly</span></span>
-   <span data-ttu-id="45933-112">Dagligt</span><span class="sxs-lookup"><span data-stu-id="45933-112">Daily</span></span>

<span data-ttu-id="45933-113">Når du har valgt periodefrekvensen, skal du klikke på **Manuelle planer** og oprette procentdele for hvert posteringsinterval.</span><span class="sxs-lookup"><span data-stu-id="45933-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="45933-114">De manuelle planer og posteringsintervaller definerer tilsammen afskrivningsbeløbet som vist i eksemplerne senere i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="45933-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="45933-115">Manuel afskrivning beregnes altid som en procentdel af anskaffelsesprisen.</span><span class="sxs-lookup"><span data-stu-id="45933-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="45933-116">Ved manuel afskrivning skal de procentdele, som du angiver for afskrivningsintervallerne, ikke udgøre en samlet procent på 100.</span><span class="sxs-lookup"><span data-stu-id="45933-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="45933-117">Manuel afskrivning er en fleksibel afskrivningsmetode, der ofte bruges til at definere en ekstraordinær afskrivningsprofil på siden **Bøger**, f.eks. en ikke-periodisk afskrivning til et specielt formål (f.eks. skat).</span><span class="sxs-lookup"><span data-stu-id="45933-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="45933-118">Eksempler</span><span class="sxs-lookup"><span data-stu-id="45933-118">Examples</span></span>
<span data-ttu-id="45933-119">Anskaffelsesprisen: 11.000,00 forventet scrapværdi: 1.000,00 I følgende tabel vises de intervaller og procentdele, som du har angivet på siden **Planer for anlægsaktivets afskrivningsprofil**.</span><span class="sxs-lookup"><span data-stu-id="45933-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="45933-120">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="45933-120">Interval number</span></span> | <span data-ttu-id="45933-121">Procentdel</span><span class="sxs-lookup"><span data-stu-id="45933-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="45933-122">1</span><span class="sxs-lookup"><span data-stu-id="45933-122">1</span></span>               | <span data-ttu-id="45933-123">10,00</span><span class="sxs-lookup"><span data-stu-id="45933-123">10.00</span></span>      |
| <span data-ttu-id="45933-124">2</span><span class="sxs-lookup"><span data-stu-id="45933-124">2</span></span>               | <span data-ttu-id="45933-125">50,00</span><span class="sxs-lookup"><span data-stu-id="45933-125">50.00</span></span>      |
| <span data-ttu-id="45933-126">3</span><span class="sxs-lookup"><span data-stu-id="45933-126">3</span></span>               | <span data-ttu-id="45933-127">8,00</span><span class="sxs-lookup"><span data-stu-id="45933-127">8.00</span></span>       |

<span data-ttu-id="45933-128">I følgende tabel vises, hvordan afskrivningen beregnes for hvert interval.</span><span class="sxs-lookup"><span data-stu-id="45933-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="45933-129">Intervalnummer</span><span class="sxs-lookup"><span data-stu-id="45933-129">Interval number</span></span> | <span data-ttu-id="45933-130">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="45933-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="45933-131">Den bogførte nettoværdi ved intervallets afslutning</span><span class="sxs-lookup"><span data-stu-id="45933-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="45933-132">1</span><span class="sxs-lookup"><span data-stu-id="45933-132">1</span></span>                | <span data-ttu-id="45933-133">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="45933-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="45933-134">10.000 (11.000 - 1.000)</span><span class="sxs-lookup"><span data-stu-id="45933-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="45933-135">2</span><span class="sxs-lookup"><span data-stu-id="45933-135">2</span></span>                | <span data-ttu-id="45933-136">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="45933-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="45933-137">5.000 (10.000 - 5.000)</span><span class="sxs-lookup"><span data-stu-id="45933-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="45933-138">3</span><span class="sxs-lookup"><span data-stu-id="45933-138">3</span></span>                | <span data-ttu-id="45933-139">(11.000 - 1.000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="45933-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="45933-140">4.200 (5.000 - 800)</span><span class="sxs-lookup"><span data-stu-id="45933-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="45933-141">Hvis du vælger **Månedligt** i feltet **Periodefrekvens**, opretter du 12 manuelle planlagte intervaller.</span><span class="sxs-lookup"><span data-stu-id="45933-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="45933-142">I følgende tabel vises afskrivningsbeløbene for de første to intervaller.</span><span class="sxs-lookup"><span data-stu-id="45933-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="45933-143">Interval</span><span class="sxs-lookup"><span data-stu-id="45933-143">Interval</span></span> | <span data-ttu-id="45933-144">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="45933-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="45933-145">Januar</span><span class="sxs-lookup"><span data-stu-id="45933-145">January</span></span>  | <span data-ttu-id="45933-146">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="45933-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="45933-147">Februar</span><span class="sxs-lookup"><span data-stu-id="45933-147">February</span></span> | <span data-ttu-id="45933-148">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="45933-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="45933-149">Hvis du vælger <strong>Halvårlig</strong> i feltet *<strong><em>Periodefrekvens</em>*</strong>, opretter du to manuelle planlagte intervaller.</span><span class="sxs-lookup"><span data-stu-id="45933-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="45933-150">I følgende tabel vises afskrivningsbeløbene for disse to intervaller.</span><span class="sxs-lookup"><span data-stu-id="45933-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="45933-151">Interval</span><span class="sxs-lookup"><span data-stu-id="45933-151">Interval</span></span>    | <span data-ttu-id="45933-152">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="45933-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="45933-153">30. juni</span><span class="sxs-lookup"><span data-stu-id="45933-153">June 30</span></span>     | <span data-ttu-id="45933-154">(11.000 - 1.000) × 10 % = 1.000</span><span class="sxs-lookup"><span data-stu-id="45933-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="45933-155">31. december</span><span class="sxs-lookup"><span data-stu-id="45933-155">December 31</span></span> | <span data-ttu-id="45933-156">(11.000 - 1.000) × 50 % = 5.000</span><span class="sxs-lookup"><span data-stu-id="45933-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="45933-157">Den samlede procentdel for alle intervaller behøver ikke være 100.</span><span class="sxs-lookup"><span data-stu-id="45933-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="45933-158">Men du modtager en meddelelse, hvis værdien i feltet **Akkumuleret procent** på siden **Planer for anlægsaktivets afskrivningsprofil** ikke er **100**.</span><span class="sxs-lookup"><span data-stu-id="45933-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



