---
title: Forbrugsafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Forbrug.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c48877058edf8251ef6eb5dd63d7eecd1866f33
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="consumption-depreciation"></a><span data-ttu-id="00cec-103">Forbrugsafskrivning</span><span class="sxs-lookup"><span data-stu-id="00cec-103">Consumption depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="00cec-104">Denne artikel indeholder en oversigt over afskrivningsmetoden Forbrug.</span><span class="sxs-lookup"><span data-stu-id="00cec-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="00cec-105">Hvis du konfigurerer en afskrivningsprofil for anlægsaktiver og vælger **Forbrug** i feltet **Metode** på siden **Afskrivningsprofiler**, tildeles anlægsaktiver til denne afskrivningsprofilen baseret på deres brug.</span><span class="sxs-lookup"><span data-stu-id="00cec-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="00cec-106">Du behøver ikke at definere procenter og intervaller på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="00cec-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="00cec-107">Når du har oprettet en afskrivningsprofil, der bruger metoden Forbrug, kan du angive metoden på forskellige måder.</span><span class="sxs-lookup"><span data-stu-id="00cec-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="00cec-108">Definere og bruge forbrugsafskrivning</span><span class="sxs-lookup"><span data-stu-id="00cec-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="00cec-109">Opret afskrivningsprofilen på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="00cec-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="00cec-110">I forbindelse med beregninger af forbrug skal afskrivningsprofilen have et id og et navn, og **Forbrug** skal være valgt i feltet **Metode**.</span><span class="sxs-lookup"><span data-stu-id="00cec-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="00cec-111">På siden **Forbrugsfaktorer** skal du konfigurere forbrugsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="00cec-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="00cec-112">De enkelte forbrugsfaktorer skal have et id og et navn samt en forbrugsfaktor, der er angivet som enten en mængde eller procent.</span><span class="sxs-lookup"><span data-stu-id="00cec-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="00cec-113">På siden **Forbrugsenheder** skal du konfigurere forbrugsenheder.</span><span class="sxs-lookup"><span data-stu-id="00cec-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="00cec-114">Hver forbrugsenhed skal have et id og et navn.</span><span class="sxs-lookup"><span data-stu-id="00cec-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="00cec-115">Afskrivningsenheder bruges til at beregne forbrugsafskrivning på siden **Forbrugsafskrivning**.</span><span class="sxs-lookup"><span data-stu-id="00cec-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="00cec-116">En km (kilometer), et kg (kilogram) eller en time er eksempler på enheder.</span><span class="sxs-lookup"><span data-stu-id="00cec-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="00cec-117">På siden **Anlægsaktiver** skal du definere individuelle anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="00cec-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="00cec-118">Til de enkelte anlægsaktiver skal du vælge værdimodeller og afskrivningsmodeller, der har afskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="00cec-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="00cec-119">Du skal oprette værdimodeller eller afskrivningsmodeller til forbrugsafskrivning, hvis du har anlægsaktiver, der bruger afskrivningsprofiler, som er baseret på metoden Forbrug.</span><span class="sxs-lookup"><span data-stu-id="00cec-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="00cec-120">Denne konfiguration udføres enten under fanen **Afskrivning** på siden **Værdimodeller** eller i oversigtspanelet **Generelt** på siden **Afskrivningsprofil**.</span><span class="sxs-lookup"><span data-stu-id="00cec-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="00cec-121">Du kan bruge samme værdimodel til flere anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="00cec-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="00cec-122">Afskrivningsmetoder er del af den værdimodel eller afskrivningskladde, som du vælger til hvert anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="00cec-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="00cec-123">Du kan ikke tilføje eller redigere afskrivningsprofiler direkte på siden **Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="00cec-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="00cec-124">Du kan kun ændre afskrivningsprofilerne på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="00cec-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="00cec-125">På siden **Værdimodeller** eller siden **Afskrivningsmodeller** skal du i feltgruppen **Forbrugsafskrivning** angive oplysninger i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="00cec-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="00cec-126">Forbrugsfaktor</span><span class="sxs-lookup"><span data-stu-id="00cec-126">Consumption factor</span></span>
    -   <span data-ttu-id="00cec-127">Enhed</span><span class="sxs-lookup"><span data-stu-id="00cec-127">Unit</span></span>
    -   <span data-ttu-id="00cec-128">Enhedsafskrivning</span><span class="sxs-lookup"><span data-stu-id="00cec-128">Unit depreciation</span></span>
    -   <span data-ttu-id="00cec-129">Forventet forbrug</span><span class="sxs-lookup"><span data-stu-id="00cec-129">Estimated consumption</span></span>

    <span data-ttu-id="00cec-130">I feltet **Bogført forbrug** vises forbrugsafskrivning i enheder, der allerede er bogført enten for kombinationen af anlægsaktiv og værdimodel eller for afskrivningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="00cec-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="00cec-131">Værdien i dette felt kan ikke opdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="00cec-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="00cec-132">Eksempler</span><span class="sxs-lookup"><span data-stu-id="00cec-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="00cec-133">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="00cec-133">Example 1</span></span>

<span data-ttu-id="00cec-134">Der er defineret følgende forbrugsfaktor pr. 31. januar:</span><span class="sxs-lookup"><span data-stu-id="00cec-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="00cec-135">Antallet er 1.000.</span><span class="sxs-lookup"><span data-stu-id="00cec-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="00cec-136">Den enhedsafskrivningspris, der er angivet for anlægsaktivet, er 1,5.</span><span class="sxs-lookup"><span data-stu-id="00cec-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="00cec-137">Afskrivningsforslaget den 31. januar er som følger: Antal × Enhedsafskrivning 1.000 × 1,5 = 1.500, hvis den faktor, der er angivet for anlægsaktivet, er en procentfaktor, den mængde, der anslås i feltet **Forkalkuleret forbrug** for værdimodellen for anlægsaktivet, ganges med den procentdel, der er angivet for den valgte slutdato.</span><span class="sxs-lookup"><span data-stu-id="00cec-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="00cec-138">Resultatmængden foreslås derefter som afskrivningsmængden for perioden.</span><span class="sxs-lookup"><span data-stu-id="00cec-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="00cec-139">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="00cec-139">Example 2</span></span>

<span data-ttu-id="00cec-140">Der er defineret følgende faktorer for forbrugsafskrivning pr. 31. januar:</span><span class="sxs-lookup"><span data-stu-id="00cec-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="00cec-141">Procentsatsen er 10 procent.</span><span class="sxs-lookup"><span data-stu-id="00cec-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="00cec-142">Den enhedsafskrivningspris, der er angivet for anlægsaktivet, er 1,5.</span><span class="sxs-lookup"><span data-stu-id="00cec-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="00cec-143">Det forkalkulerede antal for anlægsaktivet er 2.000.</span><span class="sxs-lookup"><span data-stu-id="00cec-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="00cec-144">Afskrivningsforslaget den 31. januar er som følger: Anslået mængde × Procent × Enhedsafskrivning 2.000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="00cec-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




