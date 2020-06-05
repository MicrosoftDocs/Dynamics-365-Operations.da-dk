---
title: Analyse af aktivfejl
description: I dette emne beskrives analyse af aktivfejl i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32cd8fb55cd9245a9a7c426a7c956bb40c3fdb0e
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383544"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="a2d9c-103">Analyse af aktivfejl</span><span class="sxs-lookup"><span data-stu-id="a2d9c-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a2d9c-104">I Styring af aktiver kan du analysere registreringer af aktivfejl for at få et overblik over det samlede antal registrerede fejl i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="a2d9c-105">Fejlregistreringer kan analyseres fra forskellige perspektiver, f.eks. med fokus på aktiver, aktivtyper, arbejdssteder, fejlsymptomer eller fejltyper.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="a2d9c-106">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Analyse af aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="a2d9c-107">I dialogboksen **Analyseberegning af aktivfejl** kan du bruge feltet **Niveau** til at angive, hvor detaljeret aktivfejllinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="a2d9c-108">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktivfejllinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="a2d9c-109">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle aktivfejllinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="a2d9c-110">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver, fejldatoer, fejlårsager og fejlrettelser i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="a2d9c-111">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="a2d9c-112">Klik på en eller flere af knapperne **Sammenlæg pr.** under fanen **Analyse af aktivfejl** for at få vist detaljeringsniveauet.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="a2d9c-113">Aktiverede knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="a2d9c-114">Aktivér eller deaktiver knapper ved at klikke på dem.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="a2d9c-115">Klik på **Opdater beregninger** for at få vist dine valg på skærmen.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="a2d9c-116">Når du aktiverer eller deaktiverer knappen **Sammenlæg pr.**, skal du huske at klikke på knappen **Opdater beregninger**.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="a2d9c-117">Dette er nødvendigt, da en stor mængde data behandles, mens du genberegner fejlsandsynlighed.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="a2d9c-118">Eksempler</span><span class="sxs-lookup"><span data-stu-id="a2d9c-118">Examples</span></span>

<span data-ttu-id="a2d9c-119">Der er mange måder at analysere fejlregistreringer på.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="a2d9c-120">Denne sektion har fem eksempler på, hvordan forskellige datavalg giver mere indsigt og detaljer ved analyse af registreringer af aktivfejl.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="a2d9c-121">Sammenlæg pr. symptomer</span><span class="sxs-lookup"><span data-stu-id="a2d9c-121">Group by symptoms</span></span>

<span data-ttu-id="a2d9c-122">I skærmbilledet herunder er det kun knappen **Symptom**, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="a2d9c-123">Der er foretaget fejlregistrering af tre fejlsymptomer: "Air leak", "Blown fuse" og "Equipment jammed".</span><span class="sxs-lookup"><span data-stu-id="a2d9c-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="a2d9c-124">I kolonnen **Sandsynlighed %** giver alle procenter en sum af 100 %.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="a2d9c-125">Sandsynlighed er baseret på alle **Symptom**-registreringer i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Figur 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="a2d9c-127">Sammenlæg pr. symptomer og tidsperiode</span><span class="sxs-lookup"><span data-stu-id="a2d9c-127">Group by symptoms and time period</span></span>

<span data-ttu-id="a2d9c-128">I skærmbilledet nedenfor tilføjes **År** og **Måned** for at vise, hvordan du kan få vist fejlregistreringer i løbet af en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="a2d9c-129">Fejlsymptomerne vises nu som registreringer pr. år/måned.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="a2d9c-130">Hvis du tilføjer alle procentsatser for hver måned i kolonnen **Sandsynlighed %**, bliver de sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="a2d9c-131">Sandsynlighed er baseret på **Symptom**-registreringerne i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="a2d9c-132">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="a2d9c-134">Sammenlæg pr. flere symptomer og aktiver</span><span class="sxs-lookup"><span data-stu-id="a2d9c-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="a2d9c-135">Kombinationen af aktiver og en aktivtype bruges som udgangspunkt for de beregninger, der vises i de tre skærmbilleder nedenfor, som øges i detaljeringsgraden.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="a2d9c-136">Generelt vil knapperne i handlingsrudegrupper **Gruppér efter dato**, **Gruppér efter aktiv**, **Gruppér efter arbejdssted** samt knappen **Fejl** (fejl-id) normalt indeholde perioder eller aktivrelationer.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="a2d9c-137">Knapperne **Symptom**, **Område**, **Type**, **Årsag** og **Afhjælpning** er de kategoriseringer, der bruges i fejlstyring til at analysere registreringer af aktivfejl og udpege problematiske områder.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="a2d9c-138">**Sammenlæg pr. symptom, aktiv og aktivtype**</span><span class="sxs-lookup"><span data-stu-id="a2d9c-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="a2d9c-139">I skærmbilledet nedenfor blev **Aktiv** og **Aktivtype** tilføjet for at give flere oplysninger om fejlregistreringer.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="a2d9c-140">Fejlsymptomerne er nu opdelt i kombinationerne **Aktiv** / **Aktivtype** / **Symptom**.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="a2d9c-141">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for henholdsvis kombinationen **Aktiv** / **Aktivtype** / **Symptom**, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="a2d9c-142">Sandsynlighed er baseret på **Symptom**-registreringer i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="a2d9c-143">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="a2d9c-145">**Sammenlæg pr. to symptomer, aktiv og aktivtype**</span><span class="sxs-lookup"><span data-stu-id="a2d9c-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="a2d9c-146">I skærmbilledet nedenfor er **Område** lagt til **Symptom**, **Aktiv** og **Aktivtype** for at give flere oplysninger om fejlregistreringer.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="a2d9c-147">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="a2d9c-148">Sandsynlighed er baseret på kombinationen af **Symptom** og **Område** i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="a2d9c-149">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlområde, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlområde.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Figur 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="a2d9c-151">**Sammenlæg pr.tre symptomer, aktiv og aktivtype**</span><span class="sxs-lookup"><span data-stu-id="a2d9c-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="a2d9c-152">I skærmbilledet nedenfor er **Type** tilføjet, og den mest detaljerede beregning vises i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="a2d9c-153">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="a2d9c-154">Sandsynlighed er baseret på kombinationen af **Symptom**, **Område** og **Type** i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="a2d9c-155">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på en fejltype, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for denne fejltype.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="a2d9c-157">Du kan få vist en oversigt over alle fejlregistreringer, der er oprettet på arbejdsordrer og vedligeholdelsesanmodninger, ved at klikke på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="a2d9c-158">Vælg en registrering af aktivfejl på siden **Aktivfejl**, og udvid ruden **Relaterede oplysninger** for at få vist oplysninger om den relaterede arbejdsordre eller vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="a2d9c-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

