---
title: Konfigurere felter til mobilappen Lokationsstyring
description: I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i mobilappen Lokationsstyring.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808816"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="620dd-103">Konfigurere felter til mobilappen Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="620dd-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="620dd-104">I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i mobilappen Lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="620dd-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="620dd-105">Dette emne vedrører funktioner i Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="620dd-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="620dd-106">Det gælder ikke for funktioner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="620dd-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="620dd-107">Mobilappen Lokationsstyring er et program, du kan bruge til at udføre opgaver i forbindelse med lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="620dd-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="620dd-108">Du kan definere og konfigurere de feltnavne, der bruges i appen, samt konfigurere den prioritet, der skal tildeles feltnavnene.</span><span class="sxs-lookup"><span data-stu-id="620dd-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="620dd-109">I dette emne beskrives, hvordan du definerer og konfigurerer disse feltnavne og prioriteter i mobilappen Lokationsstyring, og hvordan de bruges.</span><span class="sxs-lookup"><span data-stu-id="620dd-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="620dd-110">Konfigurere feltnavne for lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="620dd-110">Configure warehouse app field names</span></span>

<span data-ttu-id="620dd-111">Når du bruger Lagersted på din mobilenhed, kan du konfigurere, hvordan metadata skal vises på din enhed på siden **Feltnavne for lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="620dd-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="620dd-112">I et nyt firma skal du vælge **Opret standardopsætning** for at oprette alle de feltnavne, der skal bruges i arbejdsprocesser på mobilenheden til lagerstedet, og derefter tildele dem en foretrukken inputtilstand og inputtype.</span><span class="sxs-lookup"><span data-stu-id="620dd-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="620dd-113">Når du har oprettet alle feltnavne, kan du vælge følgende indstillinger for input.</span><span class="sxs-lookup"><span data-stu-id="620dd-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="620dd-114">Indstilling</span><span class="sxs-lookup"><span data-stu-id="620dd-114">Option</span></span></th>
<th><span data-ttu-id="620dd-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="620dd-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="620dd-116">Foretrukket inputtilstand</span><span class="sxs-lookup"><span data-stu-id="620dd-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="620dd-117">Denne indstilling angiver, om et scanningsfelt eller et inputfelt til manuel indtastning skal vises for det valgte feltnavn.</span><span class="sxs-lookup"><span data-stu-id="620dd-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="620dd-118">Det er nyttigt at skelne mellem felterne ud fra, om der bruges stregkoder til feltet.</span><span class="sxs-lookup"><span data-stu-id="620dd-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="620dd-119"><strong>Bemærk:</strong> For feltnavne, hvor den foretrukne inputtilstand er indstillet til <strong>Scanning</strong>, kan du angive oplysningerne manuelt, hvis stregkoden er ikke kan læses eller er beskadiget.</span><span class="sxs-lookup"><span data-stu-id="620dd-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="620dd-120">Inputtype</span><span class="sxs-lookup"><span data-stu-id="620dd-120">Input type</span></span></td>
<td><span data-ttu-id="620dd-121">Denne indstilling definerer, hvilke inputtype der skal bruges til navnet på det valgte felt.</span><span class="sxs-lookup"><span data-stu-id="620dd-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="620dd-122">Der er fire valgmuligheder:</span><span class="sxs-lookup"><span data-stu-id="620dd-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="620dd-123"><strong>Valg</strong> - Indeholder en liste over indstillinger at vælge imellem.</span><span class="sxs-lookup"><span data-stu-id="620dd-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="620dd-124">Feltnavne med denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="620dd-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="620dd-125"><strong>Dato</strong> - Feltnavne, der er angivet som dato, viser et datoformat i etiketten.</span><span class="sxs-lookup"><span data-stu-id="620dd-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="620dd-126">Dette hjælper lagermedarbejdere med at se, hvilket format datoen skal indtastes i.</span><span class="sxs-lookup"><span data-stu-id="620dd-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="620dd-127">Feltnavne med denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="620dd-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="620dd-128"><strong>Alfa</strong> - Hvis denne indstilling er valgt, bruges tastaturet, når du indtaster oplysninger i programmet manuelt.</span><span class="sxs-lookup"><span data-stu-id="620dd-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="620dd-129">Tastaturoplevelsen kan ændres, afhængigt af hvilken enhed der bruges.</span><span class="sxs-lookup"><span data-stu-id="620dd-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="620dd-130"><strong>Numerisk</strong> - Til feltnavne, der kun bruger numerisk input, kan du vælge denne indstilling for at få vist et brugerdefineret numerisk tastatur med inputfelt i stedet for tastaturet på enheden.</span><span class="sxs-lookup"><span data-stu-id="620dd-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="620dd-131">Konfigurere feltprioritet for lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="620dd-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="620dd-132">På siden **Feltprioritet for lagerstedsapp** kan du placere feltnavnene i forskellige prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="620dd-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="620dd-133">Dette gør det muligt at afgøre, hvilke oplysninger der vises på siden for hovedopgaven, når lagermedarbejderne udfører opgaver ved hjælp af programmet.</span><span class="sxs-lookup"><span data-stu-id="620dd-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="620dd-134">Hvis du klikker på **Opret standardopsætning**, oprettes et standardsæt af prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="620dd-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="620dd-135">Det er muligt at oprette så mange prioriterede grupper som ønsket, men kun tre prioriterede grupper vil blive vist på opgavesiden.</span><span class="sxs-lookup"><span data-stu-id="620dd-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="620dd-136">Når systemet sender metadata til programmet, tildeler det hvert felt en relativ prioritet afhængigt af dets prioriterede gruppe, og appen viser de tre første højt prioriterede grupper, der er indeholdt i metadataene på opgavesiden.</span><span class="sxs-lookup"><span data-stu-id="620dd-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="620dd-137">Resten af overløbsmetadataene vises på en side med sekundære oplysninger.</span><span class="sxs-lookup"><span data-stu-id="620dd-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="620dd-138">Følgende tabel viser et eksempel på fem prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="620dd-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="620dd-139">Prioritetsgruppe</span><span class="sxs-lookup"><span data-stu-id="620dd-139">Priority group</span></span></th>
<th><span data-ttu-id="620dd-140">Tildelte felter</span><span class="sxs-lookup"><span data-stu-id="620dd-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="620dd-141">Prioritet 10</span><span class="sxs-lookup"><span data-stu-id="620dd-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="620dd-142">Post</span><span class="sxs-lookup"><span data-stu-id="620dd-142">Item</span></span></li>
<li><span data-ttu-id="620dd-143">Mængde</span><span class="sxs-lookup"><span data-stu-id="620dd-143">Quantity</span></span></li>
<li><span data-ttu-id="620dd-144">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="620dd-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="620dd-145">Prioritet 20</span><span class="sxs-lookup"><span data-stu-id="620dd-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="620dd-146">Klyngeplacering</span><span class="sxs-lookup"><span data-stu-id="620dd-146">Cluster position</span></span></li>
<li><span data-ttu-id="620dd-147">Klynge</span><span class="sxs-lookup"><span data-stu-id="620dd-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="620dd-148">Prioritet 30</span><span class="sxs-lookup"><span data-stu-id="620dd-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="620dd-149">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="620dd-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="620dd-150">Prioritet 40</span><span class="sxs-lookup"><span data-stu-id="620dd-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="620dd-151">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="620dd-151">Configuration</span></span></li>
<li><span data-ttu-id="620dd-152">Farve</span><span class="sxs-lookup"><span data-stu-id="620dd-152">Color</span></span></li>
<li><span data-ttu-id="620dd-153">Størrelse</span><span class="sxs-lookup"><span data-stu-id="620dd-153">Size</span></span></li>
<li><span data-ttu-id="620dd-154">Skabelon</span><span class="sxs-lookup"><span data-stu-id="620dd-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="620dd-155">Prioritet 50</span><span class="sxs-lookup"><span data-stu-id="620dd-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="620dd-156">Placering</span><span class="sxs-lookup"><span data-stu-id="620dd-156">Location</span></span></li>
<li><span data-ttu-id="620dd-157">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="620dd-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="620dd-158">For eksempel når en lagermedarbejder udfører en opgave på en mobilenhed, hvis de metadata, der bliver vist i appen, består af følgende felter:</span><span class="sxs-lookup"><span data-stu-id="620dd-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="620dd-159">Post</span><span class="sxs-lookup"><span data-stu-id="620dd-159">Item</span></span>
-   <span data-ttu-id="620dd-160">Mængde</span><span class="sxs-lookup"><span data-stu-id="620dd-160">Quantity</span></span>
-   <span data-ttu-id="620dd-161">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="620dd-161">Unit of measure</span></span>
-   <span data-ttu-id="620dd-162">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="620dd-162">Item description</span></span>
-   <span data-ttu-id="620dd-163">Størrelse og sted</span><span class="sxs-lookup"><span data-stu-id="620dd-163">Size and Location</span></span>

<span data-ttu-id="620dd-164">Baseret på den feltprioritet i lagerstedsappen, der er angivet i ovenstående tabel, vises følgende 3 rækker af oplysninger på opgavesiden:</span><span class="sxs-lookup"><span data-stu-id="620dd-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="620dd-165">Række 1: Vare, Antal, Måleenhed</span><span class="sxs-lookup"><span data-stu-id="620dd-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="620dd-166">Række 2: Beskrivelse af varen</span><span class="sxs-lookup"><span data-stu-id="620dd-166">Row 2: Item description</span></span>
-   <span data-ttu-id="620dd-167">Række 3: Størrelse</span><span class="sxs-lookup"><span data-stu-id="620dd-167">Row 3: Size</span></span>

<span data-ttu-id="620dd-168">De resterende metadata, f.eks. placering, vises ikke på opgavesiden, men vises på en side med oplysninger.</span><span class="sxs-lookup"><span data-stu-id="620dd-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="620dd-169">Hvis du vil vide mere og se eksempler på brugergrænsefladen, kan du se i blogindlægget [Præsentation af Finance and Operations – Lagersted](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="620dd-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="620dd-170">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="620dd-170">Additional resources</span></span>
--------

[<span data-ttu-id="620dd-171">Installere og tilslutte mobilapp til lagerstedsadministration</span><span class="sxs-lookup"><span data-stu-id="620dd-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]