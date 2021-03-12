---
title: Handlingssøgning
description: I denne artikel beskrives handlingssøgningsfunktionen. Med handlingssøgning kan du finde og køre handlinger på en side.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9962451e8b72677e1a006dd9c1b8b8b268c93e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798641"
---
# <a name="action-search"></a><span data-ttu-id="5653e-104">Handlingssøgning</span><span class="sxs-lookup"><span data-stu-id="5653e-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5653e-105">I denne artikel beskrives handlingssøgningsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="5653e-105">This article describes the action search functionality.</span></span> <span data-ttu-id="5653e-106">Med handlingssøgning kan du finde og køre handlinger på en side.</span><span class="sxs-lookup"><span data-stu-id="5653e-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="5653e-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="5653e-107">Introduction</span></span>

<span data-ttu-id="5653e-108">Sider viser primært kommandoer i handlingsruder, både standardhandlingsruden, som vises øverst på en side, og værktøjslinjerne, der vises i forskellige afsnit på siden.</span><span class="sxs-lookup"><span data-stu-id="5653e-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="5653e-109">I tidligere versioner kan du med en nøgletipfunktion hurtigt få adgang til en knap i en handlingsrude ved at trykke på Alt-tasten og derefter en række bogstaver.</span><span class="sxs-lookup"><span data-stu-id="5653e-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="5653e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="5653e-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="5653e-111">De vigtigste tip er ikke længere tilgængelige, men er blevet erstattet af handlingssøgefunktionen.</span><span class="sxs-lookup"><span data-stu-id="5653e-111">The action search feature replaces Key Tips, which are no longer available.</span></span> <span data-ttu-id="5653e-112">Med denne nye funktion kan du hurtigt søge efter og køre en knap fra alle synlige handlingsruder.</span><span class="sxs-lookup"><span data-stu-id="5653e-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="5653e-113">Brug af handlingssøgning</span><span class="sxs-lookup"><span data-stu-id="5653e-113">Using action search</span></span>

<span data-ttu-id="5653e-114">Hvis du vil bruge handlingssøgefunktionen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5653e-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="5653e-115">Klik på feltet **handlingssøgning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5653e-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="5653e-116">(Feltet **handlingssøgning** indeholder et forstørrelsesglasikonet.)</span><span class="sxs-lookup"><span data-stu-id="5653e-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="5653e-117">Skriv hele navnet eller en del af navnet på den knap, du vil køre.</span><span class="sxs-lookup"><span data-stu-id="5653e-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="5653e-118">Du kan også søge ved hjælp af ord fra knappens "sti".</span><span class="sxs-lookup"><span data-stu-id="5653e-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="5653e-119">(Se næste afsnit i denne artikel for at få flere oplysninger). Typisk vises en knap omtrent øverst på listen over resultater, når du har skrevet to til fire tegn.</span><span class="sxs-lookup"><span data-stu-id="5653e-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="5653e-120">Søg efter og kør knappen på listen over resultater (ved hjælp af musen eller tastaturet).</span><span class="sxs-lookup"><span data-stu-id="5653e-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="5653e-121">Når knappen er kørt, returneres fokus til din sidste position på siden, så du kan fortsætte med at arbejde.</span><span class="sxs-lookup"><span data-stu-id="5653e-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="5653e-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="5653e-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="5653e-123">Du kan også starte handlingssøgning ved at trykke på Ctrl+/ eller Alt+Q.</span><span class="sxs-lookup"><span data-stu-id="5653e-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="5653e-124">Tryk på tastaturgenvejen igen for at returnere fokus til din sidste position på siden.</span><span class="sxs-lookup"><span data-stu-id="5653e-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="5653e-125">Om listen over resultater</span><span class="sxs-lookup"><span data-stu-id="5653e-125">Understanding the results list</span></span>

<span data-ttu-id="5653e-126">Ofte skal du kende både placeringen af en knap og dens sammenhæng for fuldt ud at forstå formålet med denne knap.</span><span class="sxs-lookup"><span data-stu-id="5653e-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="5653e-127">Derfor vises yderligere oplysninger på listen over resultater for at hjælpe dig med at forstå, præcist hvilke knapper der vises på listen.</span><span class="sxs-lookup"><span data-stu-id="5653e-127">Therefore, the results list shows additional information to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="5653e-128">Især vises knappens "sti".</span><span class="sxs-lookup"><span data-stu-id="5653e-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="5653e-129">Stien kan indeholde etiketter til de følgende elementer i brugergrænsefladen, alt efter hvad der er relevant:</span><span class="sxs-lookup"><span data-stu-id="5653e-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="5653e-130">Fanen Handlingsrude</span><span class="sxs-lookup"><span data-stu-id="5653e-130">Action Pane tab</span></span>
- <span data-ttu-id="5653e-131">Knapgruppe</span><span class="sxs-lookup"><span data-stu-id="5653e-131">Button group</span></span>
- <span data-ttu-id="5653e-132">Menuknappen (Hvis knappen er inde i en menuknap)</span><span class="sxs-lookup"><span data-stu-id="5653e-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="5653e-133">Menuseparator (Hvis knappen er inde i en navngivet gruppe inde i en menuknap)</span><span class="sxs-lookup"><span data-stu-id="5653e-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="5653e-134">Gruppe eller fane på siden (f.eks navnet på et oversigtspanel)</span><span class="sxs-lookup"><span data-stu-id="5653e-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="5653e-135">Du har for eksempel indtastet **tot** i feltet **handlingssøgning** og er nu at undersøge listen over resultater.</span><span class="sxs-lookup"><span data-stu-id="5653e-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="5653e-136">Den første post for en knap, der hedder **Totaler**, er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="5653e-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="5653e-137">Også knapstien **Salgsordre** &gt; **Vis** vises.</span><span class="sxs-lookup"><span data-stu-id="5653e-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="5653e-138">**Salgsordredelen** af stien svarer til fanen **Salgsordre** fane i handlingsruden, og **visningsdelen** af stien svarer til gruppen **Visning** under denne fane. På samme måde fortæller stien til knappen **Slutrabat** (**Sælg** &gt; **Beregn**) dig, at denne knap er placeret i gruppen **Beregn** under fanen **Sælg** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5653e-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="5653e-139">Derfor hjælper disse oplysninger dig til at forstå, nøjagtigt hvilken knap der udløses af handlingssøgningen (hvis du vælger denne knap på resultatlisten).</span><span class="sxs-lookup"><span data-stu-id="5653e-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="5653e-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="5653e-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="5653e-141">I det forrige eksempel viste handlingssøgning resultater fra standardhandlingsruden øverst på en side.</span><span class="sxs-lookup"><span data-stu-id="5653e-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="5653e-142">Handlingssøgning viser også resultaterne fra synlige værktøjslinjer, der er placeret andre steder på siden.</span><span class="sxs-lookup"><span data-stu-id="5653e-142">However, action search also shows results from visible toolbars that are in other places on the page.</span></span> <span data-ttu-id="5653e-143">For eksempel søger du efter knappen **Disponibel lagerbeholdning**, der er placeret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="5653e-143">For example, you're searching for the **On-hand inventory** button that is on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5653e-144">I dette tilfælde fortæller knapstien i resultatlisten (**Salgsordrelinjer** &gt; **Lager** &gt; **Vis**) dig, at knappen er placeret under overskriften **Vis** på menuknappen **Lager** i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="5653e-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="5653e-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="5653e-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5653e-146">Der er nogle knapper, der ikke vises i søgningen Handling.</span><span class="sxs-lookup"><span data-stu-id="5653e-146">There are some buttons that do not show up in Action search.</span></span> <span data-ttu-id="5653e-147">Disse omfatter knapper til at slette dialogbokse og knapper fra underformularer.</span><span class="sxs-lookup"><span data-stu-id="5653e-147">These include drop dialog buttons and buttons from subforms.</span></span> 

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="5653e-148">Handlingssøgning vs. navigationsøgning</span><span class="sxs-lookup"><span data-stu-id="5653e-148">Action search vs. Navigation search</span></span>

<span data-ttu-id="5653e-149">Hvor handlingssøgning har til formål at finde og udføre handlinger på en side, er der en separat søgemekanisme til at søge efter og navigere til sider.</span><span class="sxs-lookup"><span data-stu-id="5653e-149">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="5653e-150">Du kan få flere oplysninger om denne funktion i artiklen [Navigationssøgning](navigation-search.md).</span><span class="sxs-lookup"><span data-stu-id="5653e-150">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
