---
title: Knytte kildeskattekoder til kildeskattegrupper og definere formlen til beregning af kildeskat
description: Dette emne forklarer, hvordan du kan oprette grupper for kildeskat (TDS – Tax Deducted at Source) og knytte kildeskattekoder til kildeskattegrupper. Hvis du vil beregne kildskat for en kildeskattegruppe, skal du definere formlen for de kildeskattekoder, der er tilknyttet den.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023127"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="0d73f-104">Knytte kildeskattekoder til kildeskattegrupper og definere formlen til beregning af kildeskat</span><span class="sxs-lookup"><span data-stu-id="0d73f-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d73f-105">Dette emne forklarer, hvordan du kan oprette grupper for kildeskat (TDS – Tax Deducted at Source) og knytte kildeskattekoder til kildeskattegrupper.</span><span class="sxs-lookup"><span data-stu-id="0d73f-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="0d73f-106">Hvis du vil beregne kildskat for en kildeskattegruppe, skal du definere formlen for de kildeskattekoder, der er tilknyttet den.</span><span class="sxs-lookup"><span data-stu-id="0d73f-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="0d73f-107">Benyt følgende fremgangsmåde for at konfigurere en kildeskattegruppe, knytte kildeskattekoder til den og definere formlen til beregning af kildeskat.</span><span class="sxs-lookup"><span data-stu-id="0d73f-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="0d73f-108">Gå til **Skat \> Indirekte skatter \> A-skat \> Grupper for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="0d73f-109">[![Siden Grupper for A-skat](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="0d73f-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="0d73f-110">Vælg **Ny** i handlingsruden for at oprette en gruppe for A-skat til kildeskat, og angiv de nødvendige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="0d73f-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="0d73f-111">I feltet **Skattetype** skal du vælge **KIldeskat**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="0d73f-112">I oversigtspanelet **Opsætning** skal du vælge **Tilføj** for at oprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="0d73f-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="0d73f-113">Vælg kildeskattekoden for kildeskattegruppen i feltet **Kode for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="0d73f-114">Feltet **Navn på A-skat** viser navnet på kildeskattekoden, og feltet **Værdi** viser værdien.</span><span class="sxs-lookup"><span data-stu-id="0d73f-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="0d73f-115">Hvis du vil ignorere grænseværdien og den tærskel for fritagelse, der er defineret for den kildeskattekomponent, som er tilknyttet kildeskattekoden i skattetranskationer, skal du markere afkrydsningsfeltet **Ignorer grænseværdi**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="0d73f-116">Hvis du vil forhindre, at skattegruppen indgår i beregninger for transaktioner, skal du markere afkrydsningsfeltet **Fritaget**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="0d73f-117">I handlingsruden skal du vælge **Designer** for at åbne formeldesigneren, så du kan definere formlen til beregning af kildeskat for kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="0d73f-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="0d73f-118">På siden **Designer** viser fanen **Skatter** de kildeskattekoder, der er valgt for kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="0d73f-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="0d73f-119">[![Siden Designer](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="0d73f-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="0d73f-120">Vælg **Alt+N** under fanen **Beregning** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="0d73f-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="0d73f-121">Feltet **Id** viser det automatisk genererede prioritets-id for skatteberegningen.</span><span class="sxs-lookup"><span data-stu-id="0d73f-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="0d73f-122">Vælg den kildeskattekode, du vil definere formlen for, i feltet **Skattekode**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="0d73f-123">Alle de kildeskattekoder, der er valgt for kildeskattegruppen, kan vælges i dette felt.</span><span class="sxs-lookup"><span data-stu-id="0d73f-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="0d73f-124">Vælg grundlaget for beregning af kildeskat i feltet **Skattegrundlag**:</span><span class="sxs-lookup"><span data-stu-id="0d73f-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="0d73f-125">**Bruttobeløb** – Beregn skattebeløbet ud fra bruttotransaktionsbeløbet (dvs. fakturabeløbet) ved hjælp af det beregningsudtryk, der er defineret for skattekoden.</span><span class="sxs-lookup"><span data-stu-id="0d73f-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="0d73f-126">**Uden bruttobeløb** – Beregn kildeskatten baseret på det beregningsudtryk, der er defineret for skattekoden.</span><span class="sxs-lookup"><span data-stu-id="0d73f-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d73f-127">Feltet **Skattegrundlag** kan ikke angives til **Uden bruttobeløb** for kildeskattekoden med et prioritets-id på **1**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="0d73f-128">Skatteberegningen er baseret på den formel, der er defineret i feltet **Beregningsudtryk** for hver skattekode, der knyttes til kildeskattegruppen.</span><span class="sxs-lookup"><span data-stu-id="0d73f-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="0d73f-129">Vælg knappen plustegn (**+**), minustegn (**-**), multiplikationstegn (**\**_) eller divisionstegn (_*/**) for at angive beregningsudtrykket for den valgte kildeskattekode i feltet **Beregningsudtryk**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d73f-130">Der kan ikke defineres et beregningsudtryk for kildeskattekoden med et prioritets-id på **1**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="0d73f-131">Hvis du vil definere beregningsudtrykket for kildeskattekoden i feltet **Beregningsudtryk**, skal du tilføje kildeskattekoder, der er tilgængelige under fanen **Skatter**. Hvis du vil tilføje kildeskattekoder i feltet **Beregningsudtryk**, kan du bruge en af følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="0d73f-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="0d73f-132">Træk den nødvendige skattekode fra fanen **Skatter** til feltet **Beregningsudtryk**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="0d73f-133">Dobbeltklik på den krævede skattekode under fanen **Skatter**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="0d73f-134">Vælg og hold (eller højreklik) den krævede skattekode nede under fanen **Skatter**, og vælg derefter **Tilføj skattekode**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d73f-135">Indsæt et beregningsudtryk før hver kildeskattekode.</span><span class="sxs-lookup"><span data-stu-id="0d73f-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="0d73f-136">De kildeskattekoder, der er føjet til beregningsudtrykket, vises i kantede parenteser (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="0d73f-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="0d73f-137">Hvis du vil fjerne det beregningsudtryk, der er defineret for en skattekode i **feltet Beregningsudtryk**, skal du vælge knappen **C**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="0d73f-138">Hvis du vil slette en post under fanen **Beregning**, skal du vælge **Slet**.</span><span class="sxs-lookup"><span data-stu-id="0d73f-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="0d73f-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d73f-139">Close the page.</span></span>
