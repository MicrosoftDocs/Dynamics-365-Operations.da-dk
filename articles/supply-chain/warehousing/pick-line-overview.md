---
title: Konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt
description: I dette emne forklares det, hvordan du definerer, hvornår der skal vises en liste over alle arbejdslinjer for lagermedarbejdere, der behandler lagerarbejde på en mobilenhed. Denne funktion kan være nyttig for lagermedarbejdere, der ofte kræver en oversigt over pluklinjerne i en arbejdsordre, så de kan optimere plukrækkefølgen.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818866"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="5edf1-104">Konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt</span><span class="sxs-lookup"><span data-stu-id="5edf1-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5edf1-105">I dette emne forklares, hvordan du kan konfigurere indstillinger, der er relateret til pluklinjeoversigten for menupunkter for mobilenheder, der bruges til at behandle plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="5edf1-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="5edf1-106">Med pluklinjeoversigten kan lagermedarbejderne få vist og vælge fra en liste over alle de arbejdslinjer, der er relateret til deres aktuelle opgave.</span><span class="sxs-lookup"><span data-stu-id="5edf1-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="5edf1-107">Denne funktion kan hjælpe arbejdere med at optimere deres plukrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5edf1-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="5edf1-108">Funktionen indeholder indstillinger, der erstatter standardknappen **Spring over**, så arbejderne kan gå gennem linjerne én ad gangen i en fast rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5edf1-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="5edf1-109">(Det er dog stadig muligt at bruge denne knap).</span><span class="sxs-lookup"><span data-stu-id="5edf1-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="5edf1-110">Administratorer kan konfigurere de enkelte menupunkter individuelt for at styre, hvordan, hvornår og hvor mobilappen Lokationsstyring viser pluklinjeoversigten.</span><span class="sxs-lookup"><span data-stu-id="5edf1-110">Admins can configure each menu item individually to control how, when, and where the Warehouse Management mobile app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="5edf1-111">Aktivere funktionen Arbejdspluklinje, oversigt</span><span class="sxs-lookup"><span data-stu-id="5edf1-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="5edf1-112">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="5edf1-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="5edf1-113">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="5edf1-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5edf1-114">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5edf1-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5edf1-115">**Modul:** _Lokationsstyring_</span><span class="sxs-lookup"><span data-stu-id="5edf1-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="5edf1-116">**Funktionsnavn:** _Arbejdspluklinje, oversigt_</span><span class="sxs-lookup"><span data-stu-id="5edf1-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="5edf1-117">Konfigurere menupunkter for at få vist en liste over alle arbejdslinjer</span><span class="sxs-lookup"><span data-stu-id="5edf1-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="5edf1-118">Du kan konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt ved at følge nedenstående trin.</span><span class="sxs-lookup"><span data-stu-id="5edf1-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="5edf1-119">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="5edf1-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5edf1-120">Vælg eller opret et menupunkt, der er relateret til plukarbejde, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="5edf1-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="5edf1-121">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="5edf1-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="5edf1-122">**Brug eksisterende arbejde:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="5edf1-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="5edf1-123">**Styret af:** *Brugerstyret* eller *Systemstyret*</span><span class="sxs-lookup"><span data-stu-id="5edf1-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="5edf1-124">Du kan finde flere oplysninger om, hvordan du opretter menupunkter og bruger de forskellige indstillinger, der er tilgængelige på siden **Menupunkter for mobilenheder**, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="5edf1-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="5edf1-125">I oversigtspanelet **Generelt** kan du konfigurere funktionen ved at angive feltet **Vis liste over arbejdslinje** til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="5edf1-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="5edf1-126">**Vis kun efter anmodning** – arbejdere kan vælge at få vist pluklinjelisten ved at vælge **Spring til** i mobilappen Lokationsstyring .</span><span class="sxs-lookup"><span data-stu-id="5edf1-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="5edf1-127">**Vis ved start af alle pluk** – medarbejdere kan se listen, hver gang de påbegynder eller afslutter en pluklinje.</span><span class="sxs-lookup"><span data-stu-id="5edf1-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="5edf1-128">De kan også få vist listen igen ved at vælge knappen **Spring til** i mobilappen Lokationsstyring .</span><span class="sxs-lookup"><span data-stu-id="5edf1-128">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="5edf1-129">**Vis kun ved starten af første pluk** – medarbejderne ser listen, hver gang de påbegynder et nyt plukarbejde, men ikke efter hver linje.</span><span class="sxs-lookup"><span data-stu-id="5edf1-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="5edf1-130">De kan også få vist listen igen ved at vælge knappen **Spring til** i mobilappen Lokationsstyring .</span><span class="sxs-lookup"><span data-stu-id="5edf1-130">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="5edf1-131">**Vis aldrig** – Standardknappen **Spring over** i mobilappen Lokationsstyring vises, og visning af listen over arbejdslinjer er slået fra.</span><span class="sxs-lookup"><span data-stu-id="5edf1-131">**Never show** – The standard **Skip** button appears in the Warehouse Management mobile app, and display of the work line list is turned off.</span></span> <span data-ttu-id="5edf1-132">Knappen **Spring over** giver arbejdere mulighed for at gå gennem linjerne én ad gangen i en fast rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5edf1-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="5edf1-133">De kan også gå gennem listen så mange gange, de har brug for, indtil alle linjer er blevet behandlet.</span><span class="sxs-lookup"><span data-stu-id="5edf1-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="5edf1-134">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5edf1-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="5edf1-135">Hvis du angiver feltet **Vis liste over arbejdslinje** til en hvilken som helst værdi undtagen *Vis aldrig*, bliver knappen **Feltliste** i handlingsruden tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="5edf1-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="5edf1-136">Vælg **Feltliste** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5edf1-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="5edf1-137">På siden **Feltliste** skal du konfigurere de oplysninger, som mobilappen Lokationsstyring viser for hver linje på listen.</span><span class="sxs-lookup"><span data-stu-id="5edf1-137">On the **Field list** page, configure the information that the Warehouse Management mobile app shows for each line in the list.</span></span>

    - <span data-ttu-id="5edf1-138">Feltet **Primært kontrolelement** er altid angivet til *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="5edf1-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="5edf1-139">Derfor begynder hver række på listen med et linjenummer.</span><span class="sxs-lookup"><span data-stu-id="5edf1-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="5edf1-140">Brug de resterende **Visningsfelt**-felter til at tilføje op til syv yderligere visningsfelter efter dit behov.</span><span class="sxs-lookup"><span data-stu-id="5edf1-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="5edf1-141">I hvert **Visningsfelt**-felt skal du vælge navnet på et arbejdslinjefelt.</span><span class="sxs-lookup"><span data-stu-id="5edf1-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="5edf1-142">Hver linje vil derefter vise en værdi for det pågældende felt.</span><span class="sxs-lookup"><span data-stu-id="5edf1-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="5edf1-143">Værdierne vises i den rækkefølge, du vælger her.</span><span class="sxs-lookup"><span data-stu-id="5edf1-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="5edf1-144">Du kan lade nogle af **Visningsfelt**-felterne være tomme, hvis du ikke har brug for alle syv værdier.</span><span class="sxs-lookup"><span data-stu-id="5edf1-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="5edf1-145">Vælg **Gem** i handlingsruden, og luk derefter siden **Feltliste**.</span><span class="sxs-lookup"><span data-stu-id="5edf1-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]