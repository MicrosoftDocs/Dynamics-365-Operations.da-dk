---
title: Få vist og eksportere feltbeskrivelser
description: I denne artikel beskrives, hvordan du får vist feltbeskrivelser, og hvordan du bruger siden Felt beskrivelser til at eksportere beskrivelser.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e110c7fe6881825fe2b075c1795bc4f7e938da4
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811501"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="8438b-103">Få vist og eksportere feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8438b-104">I denne artikel beskrives, hvordan du får vist feltbeskrivelser, og hvordan du bruger siden Felt beskrivelser til at eksportere beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="8438b-105">Nogle af de mere komplekse felter har feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="8438b-106">Disse beskrivelser vises, når du peger på et felt.</span><span class="sxs-lookup"><span data-stu-id="8438b-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="8438b-107">Du kan også se og eksportere beskrivelser på siden **Feltbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="8438b-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="8438b-108">Ikke alle sider har feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="8438b-109">Vi vil kun levere beskrivelser for de mest komplekse felter og ikke for felter, hvis funktion er indlysende.</span><span class="sxs-lookup"><span data-stu-id="8438b-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="8438b-110">Derfor har nogle sider ikke nogen feltbeskrivelser, nogle sider har kun få beskrivelser, og nogle af de mere komplekse sider, som f.eks. mange af parametersiderne, har mange beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="8438b-111">Hvis du har adgang til udviklingsmiljøet, kan du tilføje nye feltbeskrivelser og tilpasse eksisterende beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="8438b-112">For eksempel kan du føje virksomhedsspecifikke oplysninger til en feltbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8438b-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="8438b-113">Du kan finde flere oplysninger under [Tilpasse beskrivelse af felter](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="8438b-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="8438b-114">Se feltbeskrivelser i brugergrænsefladen</span><span class="sxs-lookup"><span data-stu-id="8438b-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="8438b-115">Du kan se feltbeskrivelser ved at holde musen over et felt.</span><span class="sxs-lookup"><span data-stu-id="8438b-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="8438b-116">Hvis ingen beskrivelse er tilgængelig, kan du se navnet på feltet, når du peger på feltet.</span><span class="sxs-lookup"><span data-stu-id="8438b-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="8438b-117">I Dynamics AX 7.0 (februar 2016) kan feltbeskrivelser kun ses på siden **Beskrivelse af felter**.</span><span class="sxs-lookup"><span data-stu-id="8438b-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="8438b-118">I følgende illustration ses den feltbeskrivelse, der vises, når du peger på feltet **Lås varer under optælling**.</span><span class="sxs-lookup"><span data-stu-id="8438b-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="8438b-119">[![Eksempel på feltbeskrivelse](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="8438b-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="8438b-120">Bruge siden Feltbeskrivelser til at få vist og eksportere hjælp</span><span class="sxs-lookup"><span data-stu-id="8438b-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="8438b-121">På siden **Feltbeskrivelser** kan du få vist og eksportere feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="8438b-122">Du kan se de tilgængelige beskrivelser én side ad gangen.</span><span class="sxs-lookup"><span data-stu-id="8438b-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="8438b-123">Se en sides beskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-123">View the descriptions for a page</span></span>

<span data-ttu-id="8438b-124">For at se beskrivelserne for en side skal du følge dette trin.</span><span class="sxs-lookup"><span data-stu-id="8438b-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="8438b-125">I feltet **Vælg en side** skal du skrive navnet på siden.</span><span class="sxs-lookup"><span data-stu-id="8438b-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="8438b-126">Du kan også klikke på pilen for at åbne en liste over alle siderne og derefter gennemse eller filtrere listen.</span><span class="sxs-lookup"><span data-stu-id="8438b-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="8438b-127">Du kan enten bruge navnet på den side, der vises i brugergrænsefladen (f.eks. **Kunder**) eller kodenavnet (AOT-navnet), der bliver tilgængeligt, når du højreklikker på en side (f.eks. **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="8438b-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="8438b-128">Du kan finde oplysninger om de forskellige måder at filtrere listen over sider i afsnittet "Sådan søger du efter en side" senere i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="8438b-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="8438b-129">Hvis du vælger **Ja** i indstillingen **Inkludér felter uden en beskrivelse**, vises alle felter på siden, også selvom de ikke har en feltbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8438b-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="8438b-130">Eksportér en sides beskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-130">Export the descriptions for a page</span></span>

<span data-ttu-id="8438b-131">For at eksportere beskrivelserne for en side skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="8438b-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="8438b-132">Vælg en side i feltet **Vælg en side**.</span><span class="sxs-lookup"><span data-stu-id="8438b-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="8438b-133">Klik på **Åbn i Microsoft Office**-knappen i øverste højre hjørne, og klik derefter på **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="8438b-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="8438b-134">Sådan søger du efter en side</span><span class="sxs-lookup"><span data-stu-id="8438b-134">Searching for a page</span></span>

<span data-ttu-id="8438b-135">Der er flere måder at søge efter en side i feltet **Vælg en side**.</span><span class="sxs-lookup"><span data-stu-id="8438b-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="8438b-136">Ofte skal du klikke på pilen i feltet **Vælg en side** for at åbne rullelisten og derefter vælge en filtreret liste over sider.</span><span class="sxs-lookup"><span data-stu-id="8438b-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="8438b-137">Skriv en del af navnet, og åbn derefter rullelisten, så du kan vælge fra en filtreret liste over sider.</span><span class="sxs-lookup"><span data-stu-id="8438b-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="8438b-138">Åbn rullelisten, og klik derefter på enten overskriften **Sidens navn** øverst på listen, eller på overskriften **Sidens AOT-navn**.</span><span class="sxs-lookup"><span data-stu-id="8438b-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="8438b-139">Der åbnes en dialogboks, hvor du kan bruge avancerede filtreringsindstillinger som f.eks. **Sidens navn begynder med**.</span><span class="sxs-lookup"><span data-stu-id="8438b-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="8438b-140">Indtast sidens fulde navn.</span><span class="sxs-lookup"><span data-stu-id="8438b-140">Type the full name of the page.</span></span> <span data-ttu-id="8438b-141">Når du bruger denne valgmulighed, er det bedst at åbne rullelisten, og se, hvad der ellers er på listen, selvom feltbeskrivelser bliver vist.</span><span class="sxs-lookup"><span data-stu-id="8438b-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="8438b-142">Hvis der er et enkelt nøjagtigt match, vises feltbeskrivelserne for den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="8438b-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="8438b-143">Hvis der er mere end ét nøjagtigt match, vises der ingen beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="8438b-144">Du skal åbne rullelisten og vælge den ønskede side.</span><span class="sxs-lookup"><span data-stu-id="8438b-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="8438b-145">Hvis det navn, du har skrevet, er en del af navnet på en anden side, kan du se beskrivelserne for din side.</span><span class="sxs-lookup"><span data-stu-id="8438b-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="8438b-146">Men hvis du åbner rullelisten, ser du flere sider, der indeholder navnet.</span><span class="sxs-lookup"><span data-stu-id="8438b-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="8438b-147">Der vises f.eks. ingen beskrivelser, når du skriver **Optælling** i feltet **Vælg en side**.</span><span class="sxs-lookup"><span data-stu-id="8438b-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="8438b-148">Du åbner rullelisten og ser, at der både er to sider, der har navnet **Optælling**, og flere andre sider med ordet "Optælling" i navnet.</span><span class="sxs-lookup"><span data-stu-id="8438b-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="8438b-149">Hvis du vælger den side, der har AOT-navnet **InventJournalCount**, vises feltbeskrivelserne til denne side.</span><span class="sxs-lookup"><span data-stu-id="8438b-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="8438b-150">Hvis du åbner rullelisten igen, kan du nu se, at listen indeholder alle de sider, der har "InventJournalCount" nu som en del af deres AOT-navn.</span><span class="sxs-lookup"><span data-stu-id="8438b-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8438b-151">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="8438b-151">Troubleshooting</span></span>

<span data-ttu-id="8438b-152">Dette afsnit indeholder oplysninger, der kan hjælpe dig med at foretage fejlfinding af problemer, der evt. kan opstå, når du bruger feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="8438b-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="8438b-153">Jeg kan ikke finde en feltbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8438b-153">I can't find a field description</span></span>

<span data-ttu-id="8438b-154">Vi er i gang med at tilføje beskrivelser for de mere komplekse felter.</span><span class="sxs-lookup"><span data-stu-id="8438b-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="8438b-155">Hvis du har brug for hjælp til et bestemt felt, så fortæl os det ved at skrive en kommentar til dette emne.</span><span class="sxs-lookup"><span data-stu-id="8438b-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="8438b-156">Feltbeskrivelsen kan ikke hjælpe mig.</span><span class="sxs-lookup"><span data-stu-id="8438b-156">The field description isn't helpful</span></span>

<span data-ttu-id="8438b-157">Fortæl os det ved at føje en kommentar til dette emne.</span><span class="sxs-lookup"><span data-stu-id="8438b-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="8438b-158">Hvis du kan, bedes du beskrive de yderligere oplysninger, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="8438b-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="8438b-159">Jeg kan ikke finde et felt på siden Feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="8438b-160">Du kan få vist alle felter på en side ved at vælge **Ja** under indstillingen **Inkludér felter uden en beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="8438b-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="8438b-161">Klik på feltet **Vælg en side** for at kontrollere, at du har valgt den rigtige side.</span><span class="sxs-lookup"><span data-stu-id="8438b-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="8438b-162">Hvis det navn, du har skrevet, er en del af et andet feltnavn, har du måske valgt siden med det lange navn.</span><span class="sxs-lookup"><span data-stu-id="8438b-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="8438b-163">Jeg kan ikke finde en side på siden Feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="8438b-164">Du kan finde oplysninger om de forskellige måder, du kan finde sider på, i afsnittet "Sådan søger du efter en side" tidligere i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="8438b-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="8438b-165">Hvis du har skrevet det nøjagtige navn på siden, vises feltbeskrivelserne vises muligvis ikke, hvis der er mere end én side med det samme navn.</span><span class="sxs-lookup"><span data-stu-id="8438b-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="8438b-166">Klik på pilen i feltet **Vælg en side** for at åbne en filtreret liste over de sider, der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="8438b-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8438b-167">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8438b-167">Additional resources</span></span>

[<span data-ttu-id="8438b-168">Tilpasse feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="8438b-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
