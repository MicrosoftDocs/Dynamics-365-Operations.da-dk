---
title: "Handlingssøgning"
description: "I dette emne beskrives handlingssøgningsfunktionen i Microsoft Dynamics 365 for Finance and Operations. Med handlingssøgning kan du finde og køre handlinger på en side."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 80beefe142eb46d7c330a472ffa594a8a35a296b
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="action-search"></a><span data-ttu-id="b5a42-104">Handlingssøgning</span><span class="sxs-lookup"><span data-stu-id="b5a42-104">Action search</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b5a42-105">I dette emne beskrives handlingssøgningsfunktionen i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5a42-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b5a42-106">Med handlingssøgning kan du finde og køre handlinger på en side.</span><span class="sxs-lookup"><span data-stu-id="b5a42-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="b5a42-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="b5a42-107">Introduction</span></span>
------------

<span data-ttu-id="b5a42-108">Siderne i Microsoft Dynamics 365 for Finance and Operations viser primært kommandoer i handlingsruder, både standardhandlingsruden, som vises øverst på en side, og værktøjslinjerne, der vises i forskellige afsnit af siden.</span><span class="sxs-lookup"><span data-stu-id="b5a42-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="b5a42-109">I tidligere versioner kan du med en nøgletipfunktion hurtigt få adgang til en knap i en handlingsrude ved at trykke på Alt-tasten og derefter en række bogstaver.</span><span class="sxs-lookup"><span data-stu-id="b5a42-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="b5a42-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) I den aktuelle version af Finance and Operations er nøgletip dog ikke længere tilgængelige, men er blevet erstattet af handlingssøgningsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="b5a42-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="b5a42-111">Med denne nye funktion kan du hurtigt søge efter og køre en knap fra alle synlige handlingsruder.</span><span class="sxs-lookup"><span data-stu-id="b5a42-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="b5a42-112">Brug af handlingssøgning</span><span class="sxs-lookup"><span data-stu-id="b5a42-112">Using action search</span></span>
<span data-ttu-id="b5a42-113">Hvis du vil bruge handlingssøgefunktionen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b5a42-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="b5a42-114">Klik på feltet **handlingssøgning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b5a42-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="b5a42-115">(Feltet **handlingssøgning** indeholder et forstørrelsesglasikonet.)</span><span class="sxs-lookup"><span data-stu-id="b5a42-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="b5a42-116">Skriv hele navnet eller en del af navnet på den knap, du vil køre.</span><span class="sxs-lookup"><span data-stu-id="b5a42-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="b5a42-117">Du kan også søge ved hjælp af ord fra knappens "sti".</span><span class="sxs-lookup"><span data-stu-id="b5a42-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="b5a42-118">(Se næste afsnit i denne artikel for at få flere oplysninger). Typisk vises en knap omtrent øverst på listen over resultater, når du har skrevet to til fire tegn.</span><span class="sxs-lookup"><span data-stu-id="b5a42-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="b5a42-119">Søg efter og kør knappen på listen over resultater (ved hjælp af musen eller tastaturet).</span><span class="sxs-lookup"><span data-stu-id="b5a42-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="b5a42-120">Når knappen er kørt, returneres fokus til din sidste position på siden, så du kan fortsætte med at arbejde.</span><span class="sxs-lookup"><span data-stu-id="b5a42-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="b5a42-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="b5a42-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="b5a42-122">Du kan også starte handlingssøgning ved at trykke på Ctrl+/ eller Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="b5a42-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="b5a42-123">Tryk på tastaturgenvejen igen for at returnere fokus til din sidste position på siden.</span><span class="sxs-lookup"><span data-stu-id="b5a42-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="b5a42-124">Om listen over resultater</span><span class="sxs-lookup"><span data-stu-id="b5a42-124">Understanding the results list</span></span>
<span data-ttu-id="b5a42-125">Ofte skal du i Finance and Operations kende både placeringen af en knap og dens sammenhæng for fuldt ud at forstå formålet med denne knap.</span><span class="sxs-lookup"><span data-stu-id="b5a42-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="b5a42-126">Derfor vises yderligere oplysninger for hvert element på listen over resultater for at hjælpe dig med at forstå, præcis hvilke knapper der vises på listen.</span><span class="sxs-lookup"><span data-stu-id="b5a42-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="b5a42-127">Især vises knappens "sti".</span><span class="sxs-lookup"><span data-stu-id="b5a42-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="b5a42-128">Stien kan indeholde etiketter til de følgende elementer i brugergrænsefladen, alt efter hvad der er relevant:</span><span class="sxs-lookup"><span data-stu-id="b5a42-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="b5a42-129">Fanen Handlingsrude</span><span class="sxs-lookup"><span data-stu-id="b5a42-129">Action Pane tab</span></span>
-   <span data-ttu-id="b5a42-130">Knapgruppe</span><span class="sxs-lookup"><span data-stu-id="b5a42-130">Button group</span></span>
-   <span data-ttu-id="b5a42-131">Menuknappen (Hvis knappen er inde i en menuknap)</span><span class="sxs-lookup"><span data-stu-id="b5a42-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="b5a42-132">Menuseparator (Hvis knappen er inde i en navngivet gruppe inde i en menuknap)</span><span class="sxs-lookup"><span data-stu-id="b5a42-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="b5a42-133">Gruppe eller fane på siden (f.eks navnet på et oversigtspanel)</span><span class="sxs-lookup"><span data-stu-id="b5a42-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="b5a42-134">Du har for eksempel indtastet **tot** i feltet **handlingssøgning** og er nu at undersøge listen over resultater.</span><span class="sxs-lookup"><span data-stu-id="b5a42-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="b5a42-135">Den første post for en knap, der hedder **Totaler**, er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="b5a42-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="b5a42-136">Også knapstien **Salgsordre** &gt; **Vis** vises.</span><span class="sxs-lookup"><span data-stu-id="b5a42-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="b5a42-137">**Salgsordredelen** af stien svarer til fanen **Salgsordre** fane i handlingsruden, og **visningsdelen** af stien svarer til gruppen **Visning** under denne fane. På samme måde fortæller stien til knappen **Slutrabat** (**Sælg** &gt; **Beregn**) dig, at denne knap er placeret i gruppen **Beregn** under fanen **Sælg** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b5a42-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="b5a42-138">Derfor hjælper disse oplysninger dig til at forstå, nøjagtigt hvilken knap der udløses af handlingssøgningen (hvis du vælger denne knap på resultatlisten).</span><span class="sxs-lookup"><span data-stu-id="b5a42-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="b5a42-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="b5a42-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="b5a42-140">I det forrige eksempel viste handlingssøgning resultater fra standardhandlingsruden øverst på en side.</span><span class="sxs-lookup"><span data-stu-id="b5a42-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="b5a42-141">Handlingssøgning viser også resultaterne fra synlige værktøjslinjer, der er placeret andre steder på siden.</span><span class="sxs-lookup"><span data-stu-id="b5a42-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="b5a42-142">For eksempel søger du efter knappen **Disponibel lagerbeholdning**, der er placeret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b5a42-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b5a42-143">I dette tilfælde fortæller knapstien i resultatlisten (**Salgsordrelinjer** &gt; **Lager** &gt; **Vis**) dig, at knappen er placeret under overskriften **Vis** på menuknappen **Lager** i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b5a42-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="b5a42-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="b5a42-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="b5a42-145">Handlingssøgning vs. navigationsøgning</span><span class="sxs-lookup"><span data-stu-id="b5a42-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="b5a42-146">Hvor handlingssøgning har til formål at finde og udføre handlinger på en side, er der en separat søgemekanisme til at søge efter og navigere til sider i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5a42-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="b5a42-147">Du kan få flere oplysninger om denne funktion i artiklen [Navigationssøgning](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="b5a42-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




