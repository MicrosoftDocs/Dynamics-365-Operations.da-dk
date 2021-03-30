---
title: Oprette og opdatere åbningstider
description: I dette emne beskrives, hvordan du opretter og opdaterer åbningstider i Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 00c532dfa9ceed2cda6652496d874cb82785dc7b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230634"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="e0b65-103">Oprette og opdatere åbningstider</span><span class="sxs-lookup"><span data-stu-id="e0b65-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e0b65-104">Oversigt</span><span class="sxs-lookup"><span data-stu-id="e0b65-104">Overview</span></span>

<span data-ttu-id="e0b65-105">Detailhandlere kan på ét samlet sted oprette, vedligeholde og administrere åbningstider for forskellige butikker på tværs af geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="e0b65-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="e0b65-106">Åbningstiderne kan derefter vises i POS-terminaler.</span><span class="sxs-lookup"><span data-stu-id="e0b65-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="e0b65-107">På denne måde kan kasserere dele åbningstider med kunder og bedre hjælpe dem, hvis de er interesserede i at vide, hvad andre butikker har på lager.</span><span class="sxs-lookup"><span data-stu-id="e0b65-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="e0b65-108">Åbningstiderne kan også udskrives på kvitteringer, hvis kunderne senere vil vende tilbage til butikken.</span><span class="sxs-lookup"><span data-stu-id="e0b65-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="e0b65-109">Der kan konfigureres flere åbningstider på tværs af forskellige kanaler.</span><span class="sxs-lookup"><span data-stu-id="e0b65-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="e0b65-110">Disse kanaler omfatter fysiske butikker, callcentre, mobilenheder og e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="e0b65-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="e0b65-111">Hvis en kunde har en afhentningsordre i en anden butik, kan kassereren vælge datoer, hvor varen til afhentning er tilgængelig i den pågældende butik.</span><span class="sxs-lookup"><span data-stu-id="e0b65-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="e0b65-112">Butiksopslaget giver en reference til datoerne og åbningstiderne.</span><span class="sxs-lookup"><span data-stu-id="e0b65-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="e0b65-113">Kassereren kan vælge en dato og et sted og kan også udskrive en afhentningskvittering, der omfatter åbningstiderne.</span><span class="sxs-lookup"><span data-stu-id="e0b65-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="e0b65-114">Denne funktionalitet er tilgængelig i Microsoft Dynamics 365 Retail version 8.1.2 og nyere.</span><span class="sxs-lookup"><span data-stu-id="e0b65-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="e0b65-115">Konfigurere åbningstider</span><span class="sxs-lookup"><span data-stu-id="e0b65-115">Configure store hours</span></span>

<span data-ttu-id="e0b65-116">Når du vil konfigurere åbningstider, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e0b65-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="e0b65-117">Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Åbningstider**.</span><span class="sxs-lookup"><span data-stu-id="e0b65-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="e0b65-118">Vælg **Ny** for at oprette en ny åbningstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e0b65-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="e0b65-119">Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="e0b65-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="e0b65-120">I dialogboksen **Tilføj et interval** skal du definere datointervallet, åbningstiderne og de helligdage, der kræves.</span><span class="sxs-lookup"><span data-stu-id="e0b65-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="e0b65-121">Hvis der ikke skal skiftes åbningstider, skal du vælge **Slutter aldrig** i feltet **Slutdato**.</span><span class="sxs-lookup"><span data-stu-id="e0b65-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="e0b65-122">Hvis åbningstiderne gælder for en bestemt måned, uge eller dag, skal du angive de relevante datoer i felterne **Startdato** og **Slutdato**.</span><span class="sxs-lookup"><span data-stu-id="e0b65-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0b65-123">Du kan oprette flere skabeloner med overlappende start- og slutdatoer.</span><span class="sxs-lookup"><span data-stu-id="e0b65-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="e0b65-124">Du kan derfor f.eks. definere åbningstider for butikker i forskellige tidszoner.</span><span class="sxs-lookup"><span data-stu-id="e0b65-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="e0b65-125">![Dialogboksen Tilføj et interval](../dev-itpro/media/Storehours1.png "Dialogboksen Tilføj et interval")</span><span class="sxs-lookup"><span data-stu-id="e0b65-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="e0b65-126">Knyt åbningstidsskabelonen til de butikker, hvor den vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="e0b65-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="e0b65-127">Vælg de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.</span><span class="sxs-lookup"><span data-stu-id="e0b65-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="e0b65-128">Der kan kun knyttes én åbningstidsskabelon til hver butik.</span><span class="sxs-lookup"><span data-stu-id="e0b65-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="e0b65-129">Brug pileknapperne til at vælge butikker, områder eller organisationer.</span><span class="sxs-lookup"><span data-stu-id="e0b65-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="e0b65-130">Kalenderen vil være tilgængelig for butikkerne eller butiksgrupperne, og den vil være synlig på POS som reference.</span><span class="sxs-lookup"><span data-stu-id="e0b65-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="e0b65-131">![Dialogboksen Vælg organisationsnoder](../dev-itpro/media/Storehours2.png "Dialogboksen Vælg organisationsnoder")</span><span class="sxs-lookup"><span data-stu-id="e0b65-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="e0b65-132">På siden **Distributionsplan** skal du køre jobbene **1070** og **1090** for at gøre åbningstiderne tilgængelige for POS.</span><span class="sxs-lookup"><span data-stu-id="e0b65-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="e0b65-133">Føje åbningstider til udskrevne kvitteringer</span><span class="sxs-lookup"><span data-stu-id="e0b65-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="e0b65-134">Benyt følgende fremgangsmåde for at føje åbningstider til de udskrevne POS-kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="e0b65-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="e0b65-135">Åbn kvitteringsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="e0b65-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="e0b65-136">Vælg **Sidefod** i nederste venstre hjørne.</span><span class="sxs-lookup"><span data-stu-id="e0b65-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="e0b65-137">Træk elementet **Åbningstider** fra venstre rude til sidefoden nederst i kvitteringsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="e0b65-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="e0b65-138">Du kan redigere standardlabelen på elementet **Åbningstider** efter behov.</span><span class="sxs-lookup"><span data-stu-id="e0b65-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="e0b65-139">Gem kvitteringen, og luk kvitteringsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="e0b65-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="e0b65-140">På siden **Distributionsplan** skal du køre jobbene **1070** og **1090**.</span><span class="sxs-lookup"><span data-stu-id="e0b65-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="e0b65-141">Log på POS'et.</span><span class="sxs-lookup"><span data-stu-id="e0b65-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="e0b65-142">Udfør et salg, og vælg for at udskrive en kvittering.</span><span class="sxs-lookup"><span data-stu-id="e0b65-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="e0b65-143">POS-kvitteringer viser nu åbningstiderne.</span><span class="sxs-lookup"><span data-stu-id="e0b65-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="e0b65-144">Hvis der er helligdage i skabelonen, vises de på kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="e0b65-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="e0b65-145">![Kvitteringseksempel](../dev-itpro/media/Storehours3.png "Kvitteringseksempel")</span><span class="sxs-lookup"><span data-stu-id="e0b65-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]