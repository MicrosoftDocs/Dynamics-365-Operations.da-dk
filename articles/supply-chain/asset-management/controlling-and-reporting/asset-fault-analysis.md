---
title: Analyse af aktivfejl
description: I dette emne beskrives analyse af aktivfejl i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918435"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="f5107-103">Analyse af aktivfejl</span><span class="sxs-lookup"><span data-stu-id="f5107-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f5107-104">I Styring af aktiver kan du analysere registreringer af aktivfejl for at få et overblik over det samlede antal registrerede fejl i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="f5107-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="f5107-105">Fejlregistreringer kan analyseres fra forskellige perspektiver, f.eks. med fokus på aktiver, aktivtyper, arbejdssteder, fejlsymptomer eller fejltyper.</span><span class="sxs-lookup"><span data-stu-id="f5107-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="f5107-106">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Analyse af aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="f5107-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="f5107-107">I dialogboksen **Analyseberegning af aktivfejl** kan du bruge feltet **Niveau** til at angive, hvor detaljeret aktivfejllinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="f5107-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="f5107-108">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktivfejllinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="f5107-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="f5107-109">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle aktivfejllinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="f5107-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="f5107-110">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver, fejldatoer, fejlårsager og fejlrettelser i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="f5107-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="f5107-111">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="f5107-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="f5107-112">Klik på en eller flere knapper i handlingsruden **Sammenlæg pr.** under fanen **Analyse af aktivfejl** for at få vist detaljeringsniveauet.</span><span class="sxs-lookup"><span data-stu-id="f5107-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="f5107-113">Aktiverede knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="f5107-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="f5107-114">Aktivér eller deaktiver knapper ved at klikke på dem.</span><span class="sxs-lookup"><span data-stu-id="f5107-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="f5107-115">Klik på **Opdater beregninger** for at få vist dine valg på skærmen.</span><span class="sxs-lookup"><span data-stu-id="f5107-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="f5107-116">Hver gang du aktiverer eller deaktiverer knapper i handlingsrudegrupperne **Sammenlæg pr.**, skal du huske at klikke på knappen **Opdater beregninger**, når du har ændret valgene.</span><span class="sxs-lookup"><span data-stu-id="f5107-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="f5107-117">Dette er nødvendigt, da en stor mængde data behandles, mens du genberegner fejlsandsynlighed.</span><span class="sxs-lookup"><span data-stu-id="f5107-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="f5107-118">Der er mange måder at analysere fejlregistreringer på.</span><span class="sxs-lookup"><span data-stu-id="f5107-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="f5107-119">Nedenfor vises eksempler i fem skærmbilleder af, hvordan forskellige datavalg giver forskellige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f5107-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="f5107-120">Du kan se, hvordan forskellige valg giver flere oplysninger og detaljer ved analyse af registreringer af aktivfejl.</span><span class="sxs-lookup"><span data-stu-id="f5107-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="f5107-121">I skærmbilledet herunder er det kun knappen **Symptom**, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="f5107-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="f5107-122">Der er foretaget fejlregistrering af tre fejlsymptomer: "Air leak", "Blown fuse" og "Equipment jammed".</span><span class="sxs-lookup"><span data-stu-id="f5107-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="f5107-123">I kolonnen **Sandsynlighed %** giver alle procenter en sum af 100 %.</span><span class="sxs-lookup"><span data-stu-id="f5107-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="f5107-124">Sandsynlighed er baseret på alle **Symptom**-registreringer i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="f5107-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Figur 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="f5107-126">I skærmbilledet nedenfor tilføjes **År** og **Måned** for at vise, hvordan du kan få vist fejlregistreringer i løbet af en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="f5107-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="f5107-127">Fejlsymptomerne vises nu som registreringer pr. år/måned.</span><span class="sxs-lookup"><span data-stu-id="f5107-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="f5107-128">Hvis du tilføjer alle procentsatser for hver måned i kolonnen **Sandsynlighed %**, bliver de sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="f5107-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="f5107-129">Sandsynlighed er baseret på **Symptom**-registreringerne i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="f5107-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f5107-130">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.</span><span class="sxs-lookup"><span data-stu-id="f5107-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="f5107-132">Kombinationen af aktiver og en aktivtype bruges som udgangspunkt for de beregninger, der vises i de tre skærmbilleder nedenfor, som øges i detaljeringsgraden.</span><span class="sxs-lookup"><span data-stu-id="f5107-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="f5107-133">Generelt vil knapperne i handlingsrudegrupper **Gruppér efter dato**, **Gruppér efter aktiv**, **Gruppér efter arbejdssted** samt knappen **Fejl** (fejl-id) normalt indeholde perioder eller aktivrelationer.</span><span class="sxs-lookup"><span data-stu-id="f5107-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="f5107-134">Knapperne **Symptom**, **Område**, **Type**, **Årsag** og **Afhjælpning** er de kategoriseringer, der bruges i fejlstyring til at analysere registreringer af aktivfejl og udpege problematiske områder.</span><span class="sxs-lookup"><span data-stu-id="f5107-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="f5107-135">I skærmbilledet nedenfor blev **Aktiv** og **Aktivtype** tilføjet for at give flere oplysninger om fejlregistreringer.</span><span class="sxs-lookup"><span data-stu-id="f5107-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f5107-136">Fejlsymptomerne er nu opdelt i kombinationerne **Aktiv** / **Aktivtype** / **Symptom**.</span><span class="sxs-lookup"><span data-stu-id="f5107-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="f5107-137">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for henholdsvis kombinationen **Aktiv** / **Aktivtype** / **Symptom**, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="f5107-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="f5107-138">Sandsynlighed er baseret på **Symptom**-registreringer i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="f5107-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="f5107-139">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlsymptom, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlsymptom.</span><span class="sxs-lookup"><span data-stu-id="f5107-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Figur 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="f5107-141">I skærmbilledet nedenfor er **Område** lagt til **Symptom**, **Aktiv** og **Aktivtype** for at give flere oplysninger om fejlregistreringer.</span><span class="sxs-lookup"><span data-stu-id="f5107-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="f5107-142">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="f5107-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f5107-143">Sandsynlighed er baseret på kombinationen af **Symptom** og **Område** i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="f5107-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="f5107-144">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på et fejlområde, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for dette fejlområde.</span><span class="sxs-lookup"><span data-stu-id="f5107-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Figur 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="f5107-146">I skærmbilledet nedenfor er **Type** tilføjet, og den mest detaljerede beregning vises i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f5107-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="f5107-147">Hvis du tilføjer alle procentsatser i kolonnen **Sandsynlighed %** for kombinationen af **Aktiv** / **Aktivtype** / **Symptom** på et aktiv, bliver de hver især sammenlagt 100 %.</span><span class="sxs-lookup"><span data-stu-id="f5107-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="f5107-148">Sandsynlighed er baseret på kombinationen af **Symptom**, **Område** og **Type** i denne fejlanalyse.</span><span class="sxs-lookup"><span data-stu-id="f5107-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="f5107-149">Hvis du har et stort antal linjer på et aktiv, men en stor procentdel ligger på en enkelt linje, vil det være en indikation på en fejltype, der skal undersøges mere nøjagtigt for at finde en metode til at begrænse antallet af registreringer for denne fejltype.</span><span class="sxs-lookup"><span data-stu-id="f5107-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="f5107-151">Du kan få vist en oversigt over alle fejlregistreringer, der er oprettet på arbejdsordrer og vedligeholdelsesanmodninger, ved at klikke på **Styring af aktiver** > **Forespørgsler** > **Aktivfejl** > **Aktivfejl**.</span><span class="sxs-lookup"><span data-stu-id="f5107-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="f5107-152">Vælg en registrering af aktivfejl på siden **Aktivfejl**, og udvid ruden **Relaterede oplysninger** for at få vist oplysninger om den relaterede arbejdsordre eller vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="f5107-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

