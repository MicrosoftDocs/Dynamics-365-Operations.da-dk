---
title: Designe grænsefladen til kørsel af produktion
description: Dette emne beskriver, hvordan du kan designe indholdet af brugergrænsefladen for hver konfiguration.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 4e2b3746e690623e347e0319ab1b55f2645a5e23
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814674"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="9ee6e-103">Designe grænsefladen til kørsel af produktion</span><span class="sxs-lookup"><span data-stu-id="9ee6e-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ee6e-104">Du kan designe indholdet af brugergrænsefladen for hver konfiguration, der bruges af grænsefladen til kørsel af produktion.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="9ee6e-105">Arbejdere i én arbejdscelle skal f.eks. kunne åbne jobinstruktioner i produktionen, mens der i en anden arbejdscelle ikke er brug for instruktioner.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="9ee6e-106">Hvis det er tilfældet, skal der oprettes to konfigurationer, én med en knap til åbning af vedhæftede dokumenter og én uden denne knap.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="9ee6e-107">Designe en fane</span><span class="sxs-lookup"><span data-stu-id="9ee6e-107">Design a tab</span></span>

<span data-ttu-id="9ee6e-108">På siden **Konfigurer kørsel af produktion** kan du oprette og konfigurere faner ved at vælge **Design faner** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="9ee6e-109">Hver fane er inddelt i fire sektioner, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="9ee6e-110">![Fanelayout](media/pfe-tab-layout.png "Fanelayout")</span><span class="sxs-lookup"><span data-stu-id="9ee6e-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="9ee6e-111">Følgende elementer vises i illustrationen:</span><span class="sxs-lookup"><span data-stu-id="9ee6e-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="9ee6e-112">Primær værktøjslinje</span><span class="sxs-lookup"><span data-stu-id="9ee6e-112">Primary toolbar</span></span>
1. <span data-ttu-id="9ee6e-113">Sekundær værktøjslinje</span><span class="sxs-lookup"><span data-stu-id="9ee6e-113">Secondary toolbar</span></span>
1. <span data-ttu-id="9ee6e-114">Hovedvisning</span><span class="sxs-lookup"><span data-stu-id="9ee6e-114">Main view</span></span>
1. <span data-ttu-id="9ee6e-115">Detaljeret visning</span><span class="sxs-lookup"><span data-stu-id="9ee6e-115">Detailed view</span></span>

<span data-ttu-id="9ee6e-116">Følg disse trin for at oprette og konfigurere en ny fane:</span><span class="sxs-lookup"><span data-stu-id="9ee6e-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="9ee6e-117">Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-117">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

1. <span data-ttu-id="9ee6e-118">Vælg **Design faner** i handlingsruden for at åbne siden **Design faner**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="9ee6e-119">![Siden Design faner](media/pfe-design-tabs.png "Siden Design faner")</span><span class="sxs-lookup"><span data-stu-id="9ee6e-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="9ee6e-120">Vælg **Ny** i handlingsrude.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="9ee6e-121">Foretag følgende indstillinger i overskriften på siden:</span><span class="sxs-lookup"><span data-stu-id="9ee6e-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="9ee6e-122">**Fanenavn** - Angiv et navn til fanen.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="9ee6e-123">**Hovedvisning** - Vælg mellem de to foruddefinerede joblister (*Aktive job*, *Alle job* eller *Min maskine*).</span><span class="sxs-lookup"><span data-stu-id="9ee6e-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="9ee6e-124">**Detaljevisning** - Vælg mellem en tom værdi eller **Jobdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="9ee6e-125">Hvis du vælger den tomme værdi, vil der ikke være detaljeret visning under fanen. Hvis du vælger **Jobdetaljer**, indeholder detaljeret visning en detaljeret beskrivelse af det job, der er valgt på joblisten i hovedvisningen.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="9ee6e-126">Vælg, hvilke knapper der skal være tilgængelige på den primære værktøjslinje, i sektionen **Primær værktøjslinje**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="9ee6e-127">I kolonnen **Tilgængelige handlinger** vises en liste over alle de knapper, der kan tilføjes.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="9ee6e-128">I kolonnerne **Valgte handlinger** vises en liste over alle de knapper, der er medtaget i den aktuelle konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="9ee6e-129">Brug knapperne mellem kolonnerne til at flytte markerede elementer mellem kolonnerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="9ee6e-130">Brug op- og ned-knapperne ud for kolonnen **Valgte handlinger** til at styre den rækkefølge, som knapperne vises i i brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="9ee6e-131">Vælg, hvilke knapper der skal være tilgængelige på den sekundære værktøjslinje, i sektionen **Sekundær** **værktøjslinje**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="9ee6e-132">I kolonnen **Tilgængelige handlinger** vises en liste over alle de knapper, der kan tilføjes.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="9ee6e-133">I kolonnerne **Valgte handlinger** vises en liste over alle de knapper, der er medtaget i den aktuelle konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="9ee6e-134">Brug knapperne mellem kolonnerne til at flytte markerede elementer mellem kolonnerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="9ee6e-135">Brug op- og ned-knapperne ud for kolonnen **Valgte handlinger** til at styre den rækkefølge, som knapperne vises i i brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="9ee6e-136">Knytte en fane til en konfiguration</span><span class="sxs-lookup"><span data-stu-id="9ee6e-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="9ee6e-137">Når du har designet alle de faner, du har brug for, kan du knytte dem til en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="9ee6e-138">Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-138">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

    <span data-ttu-id="9ee6e-139">![Konfiguration af udførelse af produktionsgulv](media/pfe-config-prod-floor-execution.png "Konfiguration af udførelse af produktionsgulv")</span><span class="sxs-lookup"><span data-stu-id="9ee6e-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="9ee6e-140">Vælg **Tilføj** i oversigtspanelet **Valg af fane**.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="9ee6e-141">Der føjes en ny række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-141">A new row is added to the grid.</span></span> <span data-ttu-id="9ee6e-142">For denne nye række skal du vælge navnet på en fane, som du vil føje til konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="9ee6e-143">Fortsæt med at tilføje flere faner efter behov.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="9ee6e-144">Brug knapperne **Flyt op** og **Flyt ned** på værktøjslinjen til at arrangere fanerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="9ee6e-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="9ee6e-145">Fanerne vises fra venstre mod højre i den rækkefølge, der vises i skærmbilledet ovenfor (fanen øverst vises til venstre).</span><span class="sxs-lookup"><span data-stu-id="9ee6e-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]