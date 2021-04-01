---
title: Konfigurere appfeltnavne i lagerstedsappen
description: I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i lagerstedsapp i Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 4c22a4314c36ba7112456ef264df500af98996f3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232953"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a><span data-ttu-id="3f61d-103">Konfigurere appfeltnavne i lagerstedsappen</span><span class="sxs-lookup"><span data-stu-id="3f61d-103">Configure app field names in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f61d-104">I dette emne beskrives, hvordan du definerer og konfigurerer feltnavne og prioriteter i lagerstedsapp i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3f61d-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="3f61d-105">Dette emne vedrører funktioner i Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="3f61d-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="3f61d-106">Det gælder ikke for funktioner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="3f61d-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="3f61d-107">Lagersted er et program, du kan bruge til at udføre opgaver i forbindelse med lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="3f61d-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="3f61d-108">Du kan definere og konfigurere de feltnavne, der bruges i appen, samt konfigurere den prioritet, der skal tildeles feltnavnene.</span><span class="sxs-lookup"><span data-stu-id="3f61d-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="3f61d-109">I dette emne beskrives, hvordan du definerer og konfigurerer disse feltnavne og prioriteter i lagerstedsappen, og hvordan de bruges i Lagersted.</span><span class="sxs-lookup"><span data-stu-id="3f61d-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="3f61d-110">Du kan finde flere oplysninger om at konfigurere forbindelsen til Lagersted i selvstudiet [Oversigt over installation og konfiguration af lagerstedsappen](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="3f61d-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the warehouse app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="3f61d-111">Konfigurere feltnavne for lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="3f61d-111">Configure warehouse app field names</span></span>

<span data-ttu-id="3f61d-112">Når du bruger Lagersted på din mobilenhed, kan du konfigurere, hvordan metadata skal vises på din enhed på siden **Feltnavne for lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="3f61d-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="3f61d-113">I et nyt firma skal du vælge **Opret standardopsætning** for at oprette alle de feltnavne, der skal bruges i arbejdsprocesser på mobilenheden til lagerstedet, og derefter tildele dem en foretrukken inputtilstand og inputtype.</span><span class="sxs-lookup"><span data-stu-id="3f61d-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="3f61d-114">Når du har oprettet alle feltnavne, kan du vælge følgende indstillinger for input.</span><span class="sxs-lookup"><span data-stu-id="3f61d-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f61d-115">Indstilling</span><span class="sxs-lookup"><span data-stu-id="3f61d-115">Option</span></span></th>
<th><span data-ttu-id="3f61d-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3f61d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f61d-117">Foretrukket inputtilstand</span><span class="sxs-lookup"><span data-stu-id="3f61d-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="3f61d-118">Denne indstilling angiver, om et scanningsfelt eller et inputfelt til manuel indtastning skal vises for det valgte feltnavn.</span><span class="sxs-lookup"><span data-stu-id="3f61d-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="3f61d-119">Det er nyttigt at skelne mellem felterne ud fra, om der bruges stregkoder til feltet.</span><span class="sxs-lookup"><span data-stu-id="3f61d-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="3f61d-120"><strong>Bemærk:</strong> For feltnavne, hvor den foretrukne inputtilstand er indstillet til <strong>Scanning</strong>, kan du angive oplysningerne manuelt, hvis stregkoden er ikke kan læses eller er beskadiget.</span><span class="sxs-lookup"><span data-stu-id="3f61d-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f61d-121">Inputtype</span><span class="sxs-lookup"><span data-stu-id="3f61d-121">Input type</span></span></td>
<td><span data-ttu-id="3f61d-122">Denne indstilling definerer, hvilke inputtype der skal bruges til navnet på det valgte felt.</span><span class="sxs-lookup"><span data-stu-id="3f61d-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="3f61d-123">Der er fire valgmuligheder:</span><span class="sxs-lookup"><span data-stu-id="3f61d-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="3f61d-124"><strong>Valg</strong> - Indeholder en liste over indstillinger at vælge imellem.</span><span class="sxs-lookup"><span data-stu-id="3f61d-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="3f61d-125">Feltnavne med denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="3f61d-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3f61d-126"><strong>Dato</strong> - Feltnavne, der er angivet som dato, viser et datoformat i etiketten.</span><span class="sxs-lookup"><span data-stu-id="3f61d-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="3f61d-127">Dette hjælper lagermedarbejdere med at se, hvilket format datoen skal indtastes i.</span><span class="sxs-lookup"><span data-stu-id="3f61d-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="3f61d-128">Feltnavne med denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="3f61d-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3f61d-129"><strong>Alfa</strong> - Hvis denne indstilling er valgt, bruges tastaturet, når du indtaster oplysninger i programmet manuelt.</span><span class="sxs-lookup"><span data-stu-id="3f61d-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="3f61d-130">Tastaturoplevelsen kan ændres, afhængigt af hvilken enhed der bruges.</span><span class="sxs-lookup"><span data-stu-id="3f61d-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="3f61d-131"><strong>Numerisk</strong> - Til feltnavne, der kun bruger numerisk input, kan du vælge denne indstilling for at få vist et brugerdefineret numerisk tastatur med inputfelt i stedet for tastaturet på enheden.</span><span class="sxs-lookup"><span data-stu-id="3f61d-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="3f61d-132">Konfigurere feltprioritet for lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="3f61d-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="3f61d-133">På siden **Feltprioritet for lagerstedsapp** kan du placere feltnavnene i forskellige prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="3f61d-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="3f61d-134">Dette gør det muligt at afgøre, hvilke oplysninger der vises på siden for hovedopgaven, når lagermedarbejderne udfører opgaver ved hjælp af programmet.</span><span class="sxs-lookup"><span data-stu-id="3f61d-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="3f61d-135">Hvis du klikker på **Opret standardopsætning**, oprettes et standardsæt af prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="3f61d-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="3f61d-136">Det er muligt at oprette så mange prioriterede grupper som ønsket, men kun tre prioriterede grupper vil blive vist på opgavesiden.</span><span class="sxs-lookup"><span data-stu-id="3f61d-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="3f61d-137">Når systemet sender metadata til programmet, tildeler det hvert felt en relativ prioritet afhængigt af dets prioriterede gruppe, og appen viser de tre første højt prioriterede grupper, der er indeholdt i metadataene på opgavesiden.</span><span class="sxs-lookup"><span data-stu-id="3f61d-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="3f61d-138">Resten af overløbsmetadataene vises på en side med sekundære oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3f61d-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="3f61d-139">Følgende tabel viser et eksempel på fem prioriterede grupper.</span><span class="sxs-lookup"><span data-stu-id="3f61d-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f61d-140">Prioritetsgruppe</span><span class="sxs-lookup"><span data-stu-id="3f61d-140">Priority group</span></span></th>
<th><span data-ttu-id="3f61d-141">Tildelte felter</span><span class="sxs-lookup"><span data-stu-id="3f61d-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="3f61d-142">Prioritet 10</span><span class="sxs-lookup"><span data-stu-id="3f61d-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="3f61d-143">Post</span><span class="sxs-lookup"><span data-stu-id="3f61d-143">Item</span></span></li>
<li><span data-ttu-id="3f61d-144">Mængde</span><span class="sxs-lookup"><span data-stu-id="3f61d-144">Quantity</span></span></li>
<li><span data-ttu-id="3f61d-145">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="3f61d-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3f61d-146">Prioritet 20</span><span class="sxs-lookup"><span data-stu-id="3f61d-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="3f61d-147">Klyngeplacering</span><span class="sxs-lookup"><span data-stu-id="3f61d-147">Cluster position</span></span></li>
<li><span data-ttu-id="3f61d-148">Klynge</span><span class="sxs-lookup"><span data-stu-id="3f61d-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3f61d-149">Prioritet 30</span><span class="sxs-lookup"><span data-stu-id="3f61d-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="3f61d-150">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3f61d-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3f61d-151">Prioritet 40</span><span class="sxs-lookup"><span data-stu-id="3f61d-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="3f61d-152">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f61d-152">Configuration</span></span></li>
<li><span data-ttu-id="3f61d-153">Farve</span><span class="sxs-lookup"><span data-stu-id="3f61d-153">Color</span></span></li>
<li><span data-ttu-id="3f61d-154">Størrelse</span><span class="sxs-lookup"><span data-stu-id="3f61d-154">Size</span></span></li>
<li><span data-ttu-id="3f61d-155">Skabelon</span><span class="sxs-lookup"><span data-stu-id="3f61d-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3f61d-156">Prioritet 50</span><span class="sxs-lookup"><span data-stu-id="3f61d-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="3f61d-157">Placering</span><span class="sxs-lookup"><span data-stu-id="3f61d-157">Location</span></span></li>
<li><span data-ttu-id="3f61d-158">Nummerplade</span><span class="sxs-lookup"><span data-stu-id="3f61d-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f61d-159">For eksempel når en lagermedarbejder udfører en opgave på en mobilenhed, hvis de metadata, der bliver vist i appen, består af følgende felter:</span><span class="sxs-lookup"><span data-stu-id="3f61d-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="3f61d-160">Post</span><span class="sxs-lookup"><span data-stu-id="3f61d-160">Item</span></span>
-   <span data-ttu-id="3f61d-161">Mængde</span><span class="sxs-lookup"><span data-stu-id="3f61d-161">Quantity</span></span>
-   <span data-ttu-id="3f61d-162">Måleenhed</span><span class="sxs-lookup"><span data-stu-id="3f61d-162">Unit of measure</span></span>
-   <span data-ttu-id="3f61d-163">Varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="3f61d-163">Item description</span></span>
-   <span data-ttu-id="3f61d-164">Størrelse og sted</span><span class="sxs-lookup"><span data-stu-id="3f61d-164">Size and Location</span></span>

<span data-ttu-id="3f61d-165">Baseret på den feltprioritet i lagerstedsappen, der er angivet i ovenstående tabel, vises følgende 3 rækker af oplysninger på opgavesiden:</span><span class="sxs-lookup"><span data-stu-id="3f61d-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="3f61d-166">Række 1: Vare, Antal, Måleenhed</span><span class="sxs-lookup"><span data-stu-id="3f61d-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="3f61d-167">Række 2: Beskrivelse af varen</span><span class="sxs-lookup"><span data-stu-id="3f61d-167">Row 2: Item description</span></span>
-   <span data-ttu-id="3f61d-168">Række 3: Størrelse</span><span class="sxs-lookup"><span data-stu-id="3f61d-168">Row 3: Size</span></span>

<span data-ttu-id="3f61d-169">De resterende metadata, f.eks. placering, vises ikke på opgavesiden, men vises på en side med oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3f61d-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="3f61d-170">Hvis du vil vide mere og se eksempler på brugergrænsefladen, kan du se i blogindlægget [Præsentation af Finance and Operations – Lagersted](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="3f61d-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="3f61d-171">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3f61d-171">Additional resources</span></span>
--------

[<span data-ttu-id="3f61d-172">Oversigt over installation og konfiguration af lagerstedsappen</span><span class="sxs-lookup"><span data-stu-id="3f61d-172">Install and configure the warehouse app overview</span></span>](install-configure-warehousing-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]