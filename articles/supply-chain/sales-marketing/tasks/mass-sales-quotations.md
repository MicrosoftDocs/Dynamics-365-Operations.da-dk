---
title: Opret flere salgstilbud
description: Denne procedure viser, hvordan til effektivt du kan oprette tilbud, der tilbyder en række produkter eller ydelser, der skal sendes til flere kunder.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bbe96e8e8fc2b7139c5d3064825f6ab527fc67e
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830301"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="97f4c-103">Opret flere salgstilbud</span><span class="sxs-lookup"><span data-stu-id="97f4c-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97f4c-104">Denne procedure viser, hvordan til effektivt du kan oprette tilbud, der tilbyder en række produkter eller ydelser, der skal sendes til flere kunder.</span><span class="sxs-lookup"><span data-stu-id="97f4c-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="97f4c-105">Oprettelse af dette massetilbud er baseret på tilbudsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="97f4c-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="97f4c-106">Du kan køre procedure på dine egne data eller i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="97f4c-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="97f4c-107">Oprette en tilbudsskabelon</span><span class="sxs-lookup"><span data-stu-id="97f4c-107">Create a quotation template</span></span>
1. <span data-ttu-id="97f4c-108">Gå til Salg og marketing > Opsætning > Tilbud > Skabelongrupper.</span><span class="sxs-lookup"><span data-stu-id="97f4c-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="97f4c-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="97f4c-109">Click New.</span></span>
3. <span data-ttu-id="97f4c-110">Skriv et id efter eget valg i feltet Gruppe-id.</span><span class="sxs-lookup"><span data-stu-id="97f4c-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="97f4c-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="97f4c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97f4c-112">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="97f4c-112">Click Save.</span></span>
6. <span data-ttu-id="97f4c-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-113">Close the page.</span></span>
7. <span data-ttu-id="97f4c-114">Gå til Salg og marketing > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="97f4c-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="97f4c-115">Click New.</span></span>
9. <span data-ttu-id="97f4c-116">Vælg 'Debitor' i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="97f4c-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="97f4c-117">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="97f4c-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="97f4c-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97f4c-118">Click OK.</span></span>
    * <span data-ttu-id="97f4c-119">For at et tilbud kan blive en skabelon, skal du udføre nogle trin i opsætningen af tilbudshovedet.</span><span class="sxs-lookup"><span data-stu-id="97f4c-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="97f4c-120">Dette skal gøres, før du føjer linjer til tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="97f4c-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="97f4c-121">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="97f4c-122">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="97f4c-122">Click Change view.</span></span>
14. <span data-ttu-id="97f4c-123">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="97f4c-123">Click Header view.</span></span>
15. <span data-ttu-id="97f4c-124">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97f4c-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="97f4c-125">Indtast eller vælg en værdi i feltet Gruppe-id.</span><span class="sxs-lookup"><span data-stu-id="97f4c-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="97f4c-126">Skriv en værdi i feltet Skabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="97f4c-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="97f4c-127">Vælg Ja i feltet Aktiv.</span><span class="sxs-lookup"><span data-stu-id="97f4c-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="97f4c-128">Kun aktive skabeloner kan bruges, når du anvender en skabelon på et nyt salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="97f4c-129">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="97f4c-130">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="97f4c-130">Click Change view.</span></span>
21. <span data-ttu-id="97f4c-131">Klik på Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="97f4c-131">Click Line view.</span></span>
22. <span data-ttu-id="97f4c-132">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="97f4c-133">Skriv en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="97f4c-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-134">Close the page.</span></span>
25. <span data-ttu-id="97f4c-135">Angiv et tal i feltet Rabatprocentdel.</span><span class="sxs-lookup"><span data-stu-id="97f4c-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="97f4c-136">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="97f4c-136">Click Add line.</span></span>
27. <span data-ttu-id="97f4c-137">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="97f4c-138">Skriv en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="97f4c-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-139">Close the page.</span></span>
30. <span data-ttu-id="97f4c-140">Angiv en ny pris i feltet Enhedspris, eller rediger den aktuelle pris.</span><span class="sxs-lookup"><span data-stu-id="97f4c-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="97f4c-141">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="97f4c-141">Click Add line.</span></span>
32. <span data-ttu-id="97f4c-142">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="97f4c-143">Skriv en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="97f4c-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="97f4c-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-144">Close the page.</span></span>
35. <span data-ttu-id="97f4c-145">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="97f4c-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="97f4c-146">Angiv et tal i feltet Rabat.</span><span class="sxs-lookup"><span data-stu-id="97f4c-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="97f4c-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="97f4c-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="97f4c-148">Anvende skabelonen til at oprette et enkelt tilbud</span><span class="sxs-lookup"><span data-stu-id="97f4c-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="97f4c-149">Gå til Salg og marketing > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="97f4c-150">Bemærk, at det tilbud, du lige har oprettet, er markeret som skabelon.</span><span class="sxs-lookup"><span data-stu-id="97f4c-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="97f4c-151">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="97f4c-151">Click New.</span></span>
3. <span data-ttu-id="97f4c-152">Vælg 'Debitor' i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="97f4c-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="97f4c-153">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="97f4c-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="97f4c-154">Udvid afsnittet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="97f4c-154">Expand the Template section.</span></span>
6. <span data-ttu-id="97f4c-155">Indtast eller vælg en værdi i feltet Gruppe-id.</span><span class="sxs-lookup"><span data-stu-id="97f4c-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="97f4c-156">Indtast eller vælg en værdi i feltet Skabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="97f4c-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="97f4c-157">Vælg 'Baseret på skabelonværdier' i feltet Beregningsmåde.</span><span class="sxs-lookup"><span data-stu-id="97f4c-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="97f4c-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97f4c-158">Click OK.</span></span>
    * <span data-ttu-id="97f4c-159">Det nye tilbud er nu oprettet baseret på dataene og vilkårene i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="97f4c-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="97f4c-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-160">Close the page.</span></span>
11. <span data-ttu-id="97f4c-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97f4c-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="97f4c-162">Anvende skabelonen til at oprette flere tilbud</span><span class="sxs-lookup"><span data-stu-id="97f4c-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="97f4c-163">Gå til Salg og marketing > Salgstilbud > Opdatering af tilbud > Opret flere tilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="97f4c-164">Vælg 'Debitor' i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="97f4c-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="97f4c-165">Indtast eller vælg en værdi i feltet Gruppe-id.</span><span class="sxs-lookup"><span data-stu-id="97f4c-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="97f4c-166">Indtast eller vælg en værdi i feltet Skabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="97f4c-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="97f4c-167">Vælg 'Baseret på skabelonværdier' i feltet Beregningsmåde.</span><span class="sxs-lookup"><span data-stu-id="97f4c-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="97f4c-168">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="97f4c-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="97f4c-169">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="97f4c-169">Click Filter.</span></span>
8. <span data-ttu-id="97f4c-170">Indstil filteret til at dække en række kunder, du vil medtage i af denne oprettelse af flere tilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="97f4c-171">Brug følgende format "Customer1..CustomerN".</span><span class="sxs-lookup"><span data-stu-id="97f4c-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="97f4c-172">For eksempel kan du angive filteret: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="97f4c-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="97f4c-173">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97f4c-173">Click OK.</span></span>
10. <span data-ttu-id="97f4c-174">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97f4c-174">Click OK.</span></span>
11. <span data-ttu-id="97f4c-175">Gå til Salg og marketing > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="97f4c-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="97f4c-176">Kontroller, at der er oprettet tilbud for alle de debitorer, der er angivet i masseopdateringsrutinen, på basis af den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="97f4c-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

