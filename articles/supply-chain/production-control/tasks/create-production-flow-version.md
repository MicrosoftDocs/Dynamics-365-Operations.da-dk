---
title: Oprette en produktionsflowversion
description: Denne procedure fokuserer på oprettelse af en ny produktionsflow-version.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d513e6898827de9a3fb1ed59006b817fb9006019
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424344"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="2c4a6-103">Oprette en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="2c4a6-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c4a6-104">Denne procedure fokuserer på oprettelse af en ny produktionsflow-version.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="2c4a6-105">For denne procedure skal produktionsparametre for lean manufacturing og måleenheder for klassen Tid være defineret.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="2c4a6-106">Du skal også definere en værdistrøm og en produktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="2c4a6-107">Du kan finde flere oplysninger om produktionsflows og aktiviteter inden for lean manufacturing i hvidbøgerne om lean manufacturing til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="2c4a6-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="2c4a6-109">Oprette et produktionsflow</span><span class="sxs-lookup"><span data-stu-id="2c4a6-109">Create a production flow</span></span>
1. <span data-ttu-id="2c4a6-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="2c4a6-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-111">Click New.</span></span>
3. <span data-ttu-id="2c4a6-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2c4a6-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2c4a6-114">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2c4a6-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2c4a6-116">Vælg en driftsenhed af typen værdistrøm.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="2c4a6-117">En værdistrøm er en driftsenhed, der spænder over alle værdistrømmens aktiviteter og flow.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="2c4a6-118">På dette stadium er driftsenheder begrænset til en juridisk enhed og har ikke yderligere funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="2c4a6-119">Klik på rullelisten i feltet Produktionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2c4a6-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2c4a6-121">Vælg en produktionsgruppe for produktionsflowet.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-121">Select a production group for the production flow.</span></span> <span data-ttu-id="2c4a6-122">Produktionsgrupper giver mulighed for definition af materiale, arbejdskraft og IGVF-konti for en produktionsproces.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="2c4a6-123">For at knytte regnskabskonteksten til et produktionsflow skal der vælges en produktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="2c4a6-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="2c4a6-125">Oprette en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="2c4a6-125">Create a production flow version</span></span>
1. <span data-ttu-id="2c4a6-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-126">Click Add.</span></span>
2. <span data-ttu-id="2c4a6-127">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="2c4a6-128">Hvis det er nødvendigt, kan du angive en udløbsdato for versionen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="2c4a6-129">Du kan opdatere den til enhver tid, selv for aktive versioner.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="2c4a6-130">Du kan bruge den til at planlægge at udfase en version.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="2c4a6-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-131">Click OK.</span></span>
4. <span data-ttu-id="2c4a6-132">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="2c4a6-133">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="2c4a6-134">ResolveChanges er taktenheden.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="2c4a6-135">Angiv et tal i feltet Gennemsnitlig takttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="2c4a6-136">Definer den gennemsnitlige takttid for versionen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="2c4a6-137">Definer en gennemsnitlig takttid for taktstyring af produktionsflowversionen.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="2c4a6-138">Takten defineres som antal pr. periode.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="2c4a6-139">I eksemplet er takttiden 0,2 timer pr. 10 styk.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="2c4a6-140">Dette svarer til en daglig gennemløbskapacitet på 400 styk for en arbejdstid på 8 timer.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="2c4a6-141">Skriv et tal i feltet Antal pr. cyklus.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="2c4a6-142">Definer mængden pr. cyklus i forhold til den gennemsnitlige takttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="2c4a6-143">Slå udvidelsen af afsnittet Versionsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="2c4a6-144">Angiv et tal i feltet Mimimumtakttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="2c4a6-145">Definer minimumtakttiden.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-145">Define the minimum takt time.</span></span> <span data-ttu-id="2c4a6-146">Minimumtakttiden skal være mindre end eller lig med den gennemsnitlige takttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="2c4a6-147">Angiv et tal i feltet Maksimumtakttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="2c4a6-148">Maksimumtakttiden skal være større end eller lig med den gennemsnitlige takttid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="2c4a6-149">Angiv et tal i feltet Periode for faktisk procestid (dage).</span><span class="sxs-lookup"><span data-stu-id="2c4a6-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="2c4a6-150">Angiv antallet af dage i Periode for faktisk procestid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="2c4a6-151">Periode for faktisk procestid er det antal dage, hvor jobs aggregeres, fra det faktiske minut bagud for at beregne den faktiske procestid.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="2c4a6-152">Værdien kan ændres når som helst og bruges kun til beregning af de faktiske procestider.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="2c4a6-153">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2c4a6-153">Click Save.</span></span>

