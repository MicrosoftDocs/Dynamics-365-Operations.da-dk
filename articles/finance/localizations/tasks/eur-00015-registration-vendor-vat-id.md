---
title: EUR-00015 Registrering af kreditors moms-id
description: Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb72a5f187afe9ebe1081acd6fe0b039c370718e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227900"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="7cc9b-103">EUR-00015 Registrering af kreditors moms-id</span><span class="sxs-lookup"><span data-stu-id="7cc9b-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cc9b-104">Denne fremgangsmåde viser, hvordan du tilføjer moms-registrerings-id'er og SE-nummer på en kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="7cc9b-105">Denne proces er ens for juridiske enheder og kunder.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="7cc9b-106">Før du kan udføre denne procedure, skal du konfigurere moms-id'er.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="7cc9b-107">Denne procedure gælder for alle europæiske lande/områder.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="7cc9b-108">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse i Tyskland.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="7cc9b-109">Denne fremgangsmåde er beregnet til en datastyringsadministrator, en debitorchef eller en kreditorchef.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="7cc9b-110">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="7cc9b-111">Gå til Kreditor > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="7cc9b-112">Find og vælg debitor DE-01001 på listen.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="7cc9b-113">Klik på Registrerings-id'er.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="7cc9b-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-114">Click Add.</span></span>
5. <span data-ttu-id="7cc9b-115">Vælg moms-id.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-115">Select VAT ID.</span></span>
6. <span data-ttu-id="7cc9b-116">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="7cc9b-117">Angiv et moms-id i Tyskland for den valgte kreditor.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="7cc9b-118">Id'et skal svare til det angivne format for registreringstype.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="7cc9b-119">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-119">Click the General tab.</span></span>
8. <span data-ttu-id="7cc9b-120">Angiv en dato i feltet Gældende.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="7cc9b-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-121">Click Save.</span></span>
10. <span data-ttu-id="7cc9b-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-122">Click New.</span></span>
11. <span data-ttu-id="7cc9b-123">Skriv en værdi i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="7cc9b-124">Angiv for eksempel ITA.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="7cc9b-125">Indtast eller vælg en værdi i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="7cc9b-126">Vælg for eksempel ITA.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="7cc9b-127">Vælg Ja i feltet Primært til land/område.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="7cc9b-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-128">Click Save.</span></span>
15. <span data-ttu-id="7cc9b-129">Klik på fanen Oversigt.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="7cc9b-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-130">Click Add.</span></span>
17. <span data-ttu-id="7cc9b-131">Indtast eller vælg en værdi i feltet Registreringstype.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="7cc9b-132">Vælg f.eks. Moms-id.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="7cc9b-133">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="7cc9b-134">Du kan f.eks. angive et moms-id i Italien.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="7cc9b-135">Id'et skal have samme format som registreringstypen.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="7cc9b-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-136">Click Save.</span></span>
20. <span data-ttu-id="7cc9b-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-137">Close the page.</span></span>
21. <span data-ttu-id="7cc9b-138">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7cc9b-139">Vælg f.eks. DE-01001.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="7cc9b-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="7cc9b-141">Udvid sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="7cc9b-142">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-142">Click Edit.</span></span>
25. <span data-ttu-id="7cc9b-143">Indtast eller vælg en værdi i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="7cc9b-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-144">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]