---
title: Testvariabler for kvalitetsstyring
description: Dette emne beskriver, hvordan du opretter testvariabler, som kan bruges til kvalitative test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956594"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="db6bb-103">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="db6bb-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db6bb-104">Dette emne beskriver, hvordan du opretter testvariabler, som kan bruges til kvalitative test for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="db6bb-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="db6bb-105">For hver kvalitativ test, der er defineret på siden **Test**, skal du definere en testvariabel og dens mulige udfald (resultater).</span><span class="sxs-lookup"><span data-stu-id="db6bb-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="db6bb-106">(For kvalitative test er feltet **Type** på siden **Test** angivet til *Indstilling*.)</span><span class="sxs-lookup"><span data-stu-id="db6bb-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="db6bb-107">Du kan bruge siden **Testvariabler** til at konfigurere, redigere og få vist de mulige udfald for en testvariabel, der er knyttet til en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="db6bb-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="db6bb-108">For hvert udfald tildeler du udfaldsstatussen *Bestået* eller *Mislykket* for at angive, om testen er bestået eller mislykket, når udfaldet er valgt som et testresultat.</span><span class="sxs-lookup"><span data-stu-id="db6bb-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="db6bb-109">Du kan bruge siden **Testgrupper** til at tildele en testvariabel og et standardudfald for den til en individuel kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="db6bb-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="db6bb-110">For hver testvariabel anbefales det, at du definerer mindst to udfald: En med udfaldsstatussen *Bestået*, og en, der har udfaldsstatussen *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="db6bb-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="db6bb-111">Der er ingen grænse for det samlede antal variabler eller udfald, der kan defineres.</span><span class="sxs-lookup"><span data-stu-id="db6bb-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="db6bb-112">Desuden kan flere test bruge samme testvariabler til at registrere resultater.</span><span class="sxs-lookup"><span data-stu-id="db6bb-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="db6bb-113">Eksempler på testvariabler</span><span class="sxs-lookup"><span data-stu-id="db6bb-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="db6bb-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="db6bb-114">Example 1</span></span>

<span data-ttu-id="db6bb-115">En produktionsvirksomhed udfører to test af producerede materialer.</span><span class="sxs-lookup"><span data-stu-id="db6bb-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="db6bb-116">I én test knyttes pH-niveauet til en farvestribe.</span><span class="sxs-lookup"><span data-stu-id="db6bb-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="db6bb-117">Acceptable pH-niveauer har lysere farver, og uacceptable pH-niveauer har mørkere farver.</span><span class="sxs-lookup"><span data-stu-id="db6bb-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="db6bb-118">I en anden test udføres flere visuelle inspektioner, og kvalitetsmedarbejdere bruger deres vurderingsevne til at afgøre, om varen er bestået eller mislykket i den visuelle inspektion.</span><span class="sxs-lookup"><span data-stu-id="db6bb-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="db6bb-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="db6bb-119">Example 2</span></span>

<span data-ttu-id="db6bb-120">En produktionsvirksomhed, der fremstiller småkager, anvender en inspektionstest for det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="db6bb-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="db6bb-121">Denne inspektionstest har adskillige variabler.</span><span class="sxs-lookup"><span data-stu-id="db6bb-121">This inspection test has several variables.</span></span> <span data-ttu-id="db6bb-122">En af variablerne er smag, og de mulige udfald er "god" og "dårlig".</span><span class="sxs-lookup"><span data-stu-id="db6bb-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="db6bb-123">Farve er en anden variabel, og de mulige udfald er "for mørk", "for lys" og "korrekt".</span><span class="sxs-lookup"><span data-stu-id="db6bb-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="db6bb-124">Oprette en testvariabel</span><span class="sxs-lookup"><span data-stu-id="db6bb-124">Create a test variable</span></span>

<span data-ttu-id="db6bb-125">Benyt denne fremgangsmåde for at oprette en testvariabel.</span><span class="sxs-lookup"><span data-stu-id="db6bb-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="db6bb-126">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Testvariabler**.</span><span class="sxs-lookup"><span data-stu-id="db6bb-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="db6bb-127">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="db6bb-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db6bb-128">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="db6bb-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db6bb-129">**Variabel** – Angiv et entydigt id eller navn til variablen.</span><span class="sxs-lookup"><span data-stu-id="db6bb-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="db6bb-130">**Beskrivelse** – Indtast en detaljeret beskrivelse af variablen.</span><span class="sxs-lookup"><span data-stu-id="db6bb-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="db6bb-131">Mens den nye række stadig er markeret, skal du vælge **Udfald** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="db6bb-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="db6bb-132">På siden **Udfald for testvariabler** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="db6bb-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db6bb-133">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="db6bb-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db6bb-134">**Udfald** – Angiv et entydigt id eller navn til udfaldet.</span><span class="sxs-lookup"><span data-stu-id="db6bb-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="db6bb-135">**Beskrivelse** – Indtast en detaljeret beskrivelse af udfaldet.</span><span class="sxs-lookup"><span data-stu-id="db6bb-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="db6bb-136">**Udfaldsstatus** – Vælg *Bestået* eller *Mislykket* for at angive, om testen er bestået eller mislykket, når udfaldet er valgt som et testresultat.</span><span class="sxs-lookup"><span data-stu-id="db6bb-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="db6bb-137">Gentag det foregående trin for hvert ekstra udfald.</span><span class="sxs-lookup"><span data-stu-id="db6bb-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="db6bb-138">Sørg for, at mindst ét udfald har udfaldsstatussen *Bestået*, og at mindst ét har udfaldsstatussen *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="db6bb-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="db6bb-139">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="db6bb-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db6bb-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="db6bb-140">Additional resources</span></span>

- [<span data-ttu-id="db6bb-141">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="db6bb-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="db6bb-142">Test for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="db6bb-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="db6bb-143">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="db6bb-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
