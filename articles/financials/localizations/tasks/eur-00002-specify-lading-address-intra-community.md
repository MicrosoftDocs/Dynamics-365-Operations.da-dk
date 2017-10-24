--- 
title: "Angive en fragtadresse for en fællesskabspostering"
description: "Denne fremgangsmåde viser, hvordan du angiver en læsningsadresse for en transaktion handel i EU."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc54b59f6cf8aec8d489955c57cbcf34c4e6be0a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="specify-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="0c71c-103">Angive en fragtadresse for en fællesskabspostering</span><span class="sxs-lookup"><span data-stu-id="0c71c-103">Specify a lading address for an intra-community transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c71c-104">Denne fremgangsmåde viser, hvordan du angiver en læsningsadresse for en transaktion handel i EU.</span><span class="sxs-lookup"><span data-stu-id="0c71c-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="0c71c-105">Eksempelvis bestiller en virksomhed i Tyskland varer fra en leverandør med en tysk firmaadresse.</span><span class="sxs-lookup"><span data-stu-id="0c71c-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="0c71c-106">Denne leverandør har et lagersted i Italien og leverer varerne derfra.</span><span class="sxs-lookup"><span data-stu-id="0c71c-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="0c71c-107">Denne levering skal rapporteres i Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0c71c-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="0c71c-108">Samme funktionsmåde gælder for returvarer fra kunder.</span><span class="sxs-lookup"><span data-stu-id="0c71c-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="0c71c-109">Denne procedure gælder for alle europæiske lande.</span><span class="sxs-lookup"><span data-stu-id="0c71c-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="0c71c-110">Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland.</span><span class="sxs-lookup"><span data-stu-id="0c71c-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="0c71c-111">Før du kan fuldføre denne procedure, skal du konfigurere Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="0c71c-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="0c71c-112">Denne procedure er kun beregnet til bogholdere.</span><span class="sxs-lookup"><span data-stu-id="0c71c-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="0c71c-113">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0c71c-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0c71c-114">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0c71c-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0c71c-115">Click New.</span></span>
3. <span data-ttu-id="0c71c-116">Indtast eller vælg en værdi</span><span class="sxs-lookup"><span data-stu-id="0c71c-116">Enter or select a value</span></span>
    * <span data-ttu-id="0c71c-117">Vælg f.eks. DE-001.</span><span class="sxs-lookup"><span data-stu-id="0c71c-117">For example, select DE-001.</span></span> <span data-ttu-id="0c71c-118">Denne kreditor har en tysk firmaadresse.</span><span class="sxs-lookup"><span data-stu-id="0c71c-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="0c71c-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0c71c-119">Click OK.</span></span>
5. <span data-ttu-id="0c71c-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0c71c-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0c71c-121">Indtast eller vælg værdien D0001 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="0c71c-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0c71c-122">Click Save.</span></span>
8. <span data-ttu-id="0c71c-123">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="0c71c-124">Klik på Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-124">Click Transportation details.</span></span>
10. <span data-ttu-id="0c71c-125">Angiv en dato og et klokkeslæt i feltet Dato og klokkeslæt for læsning.</span><span class="sxs-lookup"><span data-stu-id="0c71c-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="0c71c-126">Klik på Tilføj adresse,</span><span class="sxs-lookup"><span data-stu-id="0c71c-126">Click Add address.</span></span>
12. <span data-ttu-id="0c71c-127">Klik på Ny, og opret en ny adresse med formålet Læsning.</span><span class="sxs-lookup"><span data-stu-id="0c71c-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="0c71c-128">Skriv Italien i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0c71c-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="0c71c-129">Vælg værdien Læsning.</span><span class="sxs-lookup"><span data-stu-id="0c71c-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="0c71c-130">Bemærk, at adressens formål for være Læsning.</span><span class="sxs-lookup"><span data-stu-id="0c71c-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="0c71c-131">Indtast eller vælg værdien ITA i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="0c71c-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="0c71c-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0c71c-132">Click Save.</span></span>
17. <span data-ttu-id="0c71c-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-133">Close the page.</span></span>
18. <span data-ttu-id="0c71c-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0c71c-134">Click Save.</span></span>
    * <span data-ttu-id="0c71c-135">Kontroller, at læsningsadressen er korrekt.</span><span class="sxs-lookup"><span data-stu-id="0c71c-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="0c71c-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-136">Close the page.</span></span>
20. <span data-ttu-id="0c71c-137">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="0c71c-138">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="0c71c-138">Click Confirm.</span></span>
22. <span data-ttu-id="0c71c-139">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="0c71c-140">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="0c71c-140">Click Invoice.</span></span>
24. <span data-ttu-id="0c71c-141">Skriv en værdi i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="0c71c-142">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="0c71c-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="0c71c-143">Klik på Modtag fra: Antal produktkvitteringer for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="0c71c-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="0c71c-144">Vælg 'Bestilt antal' i feltet Standardmængde for linjer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="0c71c-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0c71c-145">Click OK.</span></span>
29. <span data-ttu-id="0c71c-146">Klik på Transportdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0c71c-146">Click Transportation details.</span></span>
    * <span data-ttu-id="0c71c-147">Kontroller, at varerne er afsendt fra Italien.</span><span class="sxs-lookup"><span data-stu-id="0c71c-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="0c71c-148">Hvis det er nødvendigt, kan du redigere læsningsoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="0c71c-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="0c71c-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-149">Close the page.</span></span>
31. <span data-ttu-id="0c71c-150">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="0c71c-150">Click Post.</span></span>
32. <span data-ttu-id="0c71c-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0c71c-151">Close the page.</span></span>
33. <span data-ttu-id="0c71c-152">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0c71c-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="0c71c-153">Klik på Overførsel.</span><span class="sxs-lookup"><span data-stu-id="0c71c-153">Click Transfer.</span></span>
35. <span data-ttu-id="0c71c-154">Vælg Ja i feltet Kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="0c71c-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="0c71c-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0c71c-155">Click OK.</span></span>
37. <span data-ttu-id="0c71c-156">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0c71c-156">Click the General tab.</span></span>
    * <span data-ttu-id="0c71c-157">Find en nyoprettet linje, og kontroller, at afsenderen har leveret varerne fra Italien.</span><span class="sxs-lookup"><span data-stu-id="0c71c-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  


