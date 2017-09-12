--- 
title: "Oprette et rykkerforløb"
description: "Brug denne opgaveguide til at oprette et rykkerforløb."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="6cda2-103">Oprette et rykkerforløb</span><span class="sxs-lookup"><span data-stu-id="6cda2-103">Create a collection letter sequence</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cda2-104">Brug denne opgaveguide til at oprette et rykkerforløb.</span><span class="sxs-lookup"><span data-stu-id="6cda2-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="6cda2-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6cda2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6cda2-106">Gå til Kredit og inkasso > Opsætning > Konfigurer rykkerforløb.</span><span class="sxs-lookup"><span data-stu-id="6cda2-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="6cda2-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6cda2-107">Click New.</span></span>
3. <span data-ttu-id="6cda2-108">Angiv et sekvens-id, der repræsenterer rækkefølgen, i feltet Rykkerforløb.</span><span class="sxs-lookup"><span data-stu-id="6cda2-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="6cda2-109">Det vil blive brugt, når du opretter en posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="6cda2-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="6cda2-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6cda2-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6cda2-111">Betalingsbetingelserne er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="6cda2-111">The terms of payment is optional.</span></span> <span data-ttu-id="6cda2-112">Hvis du indtaster en værdi her, vil rykkerens gebyrfaktura bruge disse betalingsbetingelser i stedet for betalingsbetingelserne, der er gemt sammen med kunden.</span><span class="sxs-lookup"><span data-stu-id="6cda2-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="6cda2-113">I feltet til rykkerkoden skal du vælge koden for den første rykker, du vil sende.</span><span class="sxs-lookup"><span data-stu-id="6cda2-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="6cda2-114">Den første rykker oprettes på grundlag af fakturaens forfaldsdato, den værdi, som du har angivet som frist i feltet Dage på denne linje, og andre oplysninger, som du angiver på denne linje.</span><span class="sxs-lookup"><span data-stu-id="6cda2-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="6cda2-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6cda2-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6cda2-116">Valutaen for gebyret er som standard debitorvalutaen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="6cda2-117">Valutakoden kan være forskellig fra fakturaens valuta.</span><span class="sxs-lookup"><span data-stu-id="6cda2-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="6cda2-118">Klik på Tilføj for at tilføje den næste rykker, der skal sendes i rækkefølgen</span><span class="sxs-lookup"><span data-stu-id="6cda2-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="6cda2-119">I mange tilfælde er den første rykker blot en advarsel.</span><span class="sxs-lookup"><span data-stu-id="6cda2-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="6cda2-120">Hvis det er nødvendigt, kan du tilføje gebyrer.</span><span class="sxs-lookup"><span data-stu-id="6cda2-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="6cda2-121">I feltet til rykkerkoden skal du vælge den næste rykker, der skal sendes i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="6cda2-122">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6cda2-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="6cda2-123">I hovedkontoen skal du vælge den omsætningskonto, der skal bruges til gebyrer.</span><span class="sxs-lookup"><span data-stu-id="6cda2-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="6cda2-124">Angiv det gebyr, der opkræves, når denne rykker bogføres.</span><span class="sxs-lookup"><span data-stu-id="6cda2-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="6cda2-125">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6cda2-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="6cda2-126">Vælg en varemomsgruppe, hvis der skal beregnes moms på gebyret.</span><span class="sxs-lookup"><span data-stu-id="6cda2-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="6cda2-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6cda2-128">Angiv den mindste forfaldne saldo, der kræves, før der sendes en rykker.</span><span class="sxs-lookup"><span data-stu-id="6cda2-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="6cda2-129">Angiv antallet af respitdage, som du vil tillade.</span><span class="sxs-lookup"><span data-stu-id="6cda2-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="6cda2-130">Dette er antallet af dage efter forfaldsdatoen, hvor der kan oprettes en rykker.</span><span class="sxs-lookup"><span data-stu-id="6cda2-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="6cda2-131">Der bruges til beregning af forfaldsdatoen, afhænger af placeringen af rykkeren i rykkersekvensen: ⦁ respitperioden for rykker 1, der er relateret til forfaldsdatoen på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="6cda2-132">⦁ Respitperioden for rykkere 2 og højere er i forhold til den dato, hvor den forrige rykker bogføres eller udskrives, afhængigt af valget i feltet Opdater rykkerkode på siden Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="6cda2-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="6cda2-133">Klik på Tilføj for at tilføje den sidste rykker i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="6cda2-134">Du kan tilføje op til fem rykkerkoder for et rykkerforløb.</span><span class="sxs-lookup"><span data-stu-id="6cda2-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="6cda2-135">I feltet til rykkerkoden skal du vælge den næste rykker, der skal sendes i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="6cda2-136">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6cda2-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="6cda2-137">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="6cda2-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="6cda2-138">Indtast et tal i feltet Gebyr i valuta.</span><span class="sxs-lookup"><span data-stu-id="6cda2-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="6cda2-139">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6cda2-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="6cda2-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6cda2-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="6cda2-141">Skriv et tal i feltet Mindste forsinkede saldo.</span><span class="sxs-lookup"><span data-stu-id="6cda2-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="6cda2-142">Angiv et tal i feltet Dage.</span><span class="sxs-lookup"><span data-stu-id="6cda2-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="6cda2-143">Marker dette afkrydsningsfeltet, hvis du vil spærre kunden for yderligere leveringer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="6cda2-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="6cda2-144">For at fjerne spærringen af kontoen skal du vælge Nej i feltet Fakturering og levering er sat på hold på siden Debitorer.</span><span class="sxs-lookup"><span data-stu-id="6cda2-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="6cda2-145">Udvid oversigtspanelet Note.</span><span class="sxs-lookup"><span data-stu-id="6cda2-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="6cda2-146">Angiv den tekst, der skal vises i rykkeren for den valgte rykkerkode.</span><span class="sxs-lookup"><span data-stu-id="6cda2-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="6cda2-147">Du kan oversætte denne tekst til flere sprog ved hjælp af menuen Oversættelser over notefeltet.</span><span class="sxs-lookup"><span data-stu-id="6cda2-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


