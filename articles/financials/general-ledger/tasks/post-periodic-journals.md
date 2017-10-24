--- 
title: "Bogføre periodiske kladder"
description: "Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8eae11e0501db78e467e517b29a2bc19f5765e75
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="93cfb-103">Bogføre periodiske kladder</span><span class="sxs-lookup"><span data-stu-id="93cfb-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93cfb-104">Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes.</span><span class="sxs-lookup"><span data-stu-id="93cfb-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="93cfb-105">Når du opretter den periodiske kladde, angiver du periodeintervallet for gentagelsen, eksempelvis dage eller måneder.</span><span class="sxs-lookup"><span data-stu-id="93cfb-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="93cfb-106">Denne opgaveguide opretter en periodisk kladde med en månedlig gentagelse.</span><span class="sxs-lookup"><span data-stu-id="93cfb-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="93cfb-107">Gå til Finans > Periodiske opgaver > Periodiske kladder.</span><span class="sxs-lookup"><span data-stu-id="93cfb-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="93cfb-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cfb-108">Click New.</span></span>
3. <span data-ttu-id="93cfb-109">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="93cfb-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="93cfb-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="93cfb-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="93cfb-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93cfb-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="93cfb-112">Beskrivelsen vil være navnet på den periodiske kladde, når den hentes senere, så sørg for at give den et navn, der er relevant.</span><span class="sxs-lookup"><span data-stu-id="93cfb-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="93cfb-113">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="93cfb-113">Click Lines.</span></span>
    * <span data-ttu-id="93cfb-114">En periodisk kladde vil typisk omfatte flere kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="93cfb-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="93cfb-115">denne opgaveguide tilføjer dog kun én linje.</span><span class="sxs-lookup"><span data-stu-id="93cfb-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="93cfb-116">Indtast en dato i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="93cfb-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="93cfb-117">Feltet Dato indeholder bogføringsdatoen for den næste overførsel til kassekladden.</span><span class="sxs-lookup"><span data-stu-id="93cfb-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="93cfb-118">For journaler, der vil blive hentet hver måned, anbefales det at bruge datoen i den måned, hvor den bogføres, typisk den første eller den sidste dato i perioden.</span><span class="sxs-lookup"><span data-stu-id="93cfb-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="93cfb-119">Det er muligt at lade feltet være tomt og give en dato, når kladden er hentet, ved hjælp af feltet Tom dato.</span><span class="sxs-lookup"><span data-stu-id="93cfb-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="93cfb-120">Feltet opdateres automatisk til den næste tilbagevendende dato, når der hentes transaktioner.</span><span class="sxs-lookup"><span data-stu-id="93cfb-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="93cfb-121">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="93cfb-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="93cfb-122">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93cfb-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="93cfb-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="93cfb-123">Close the page.</span></span>
11. <span data-ttu-id="93cfb-124">Angiv et tal i feltet Debet.</span><span class="sxs-lookup"><span data-stu-id="93cfb-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="93cfb-125">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="93cfb-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="93cfb-126">Vælg "Måneder" i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="93cfb-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="93cfb-127">Angiv "1" feltet Antal enheder.</span><span class="sxs-lookup"><span data-stu-id="93cfb-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="93cfb-128">Indtast en dato i feltet Sidste dato.</span><span class="sxs-lookup"><span data-stu-id="93cfb-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="93cfb-129">Angivelse af sidste dato i den forløbne periode vil forhindre, at gentagelseskladden ved en fejltagelse oprettes i den forkerte startperiode.</span><span class="sxs-lookup"><span data-stu-id="93cfb-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="93cfb-130">Sidste dato opdateres senere, hver gang den periodiske kladde hentes.</span><span class="sxs-lookup"><span data-stu-id="93cfb-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="93cfb-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="93cfb-131">Click Save.</span></span>
17. <span data-ttu-id="93cfb-132">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="93cfb-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="93cfb-133">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="93cfb-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="93cfb-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="93cfb-134">Click New.</span></span>
20. <span data-ttu-id="93cfb-135">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="93cfb-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="93cfb-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="93cfb-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="93cfb-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="93cfb-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="93cfb-138">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="93cfb-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="93cfb-139">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="93cfb-139">Click Lines.</span></span>
25. <span data-ttu-id="93cfb-140">Klik på Periodisk kladde.</span><span class="sxs-lookup"><span data-stu-id="93cfb-140">Click Period journal.</span></span>
26. <span data-ttu-id="93cfb-141">Klik på Hent kladde.</span><span class="sxs-lookup"><span data-stu-id="93cfb-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="93cfb-142">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="93cfb-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="93cfb-143">Til datoen fungerer som skæringsdato for de periodiske bilagslinjer.</span><span class="sxs-lookup"><span data-stu-id="93cfb-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="93cfb-144">Baseret på gentagelsesindstilling, Sidste dato og Til dato kan den samme linje indgå mere end én gang i den kladde, der er resultatet.</span><span class="sxs-lookup"><span data-stu-id="93cfb-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="93cfb-145">Til dato opdateres automatisk på basis af sessionsdatoen for sidste gang, den periodiske linje blev overført til en kladde.</span><span class="sxs-lookup"><span data-stu-id="93cfb-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="93cfb-146">Skriv eller vælg en værdi i feltet Nummer på periodisk kladde.</span><span class="sxs-lookup"><span data-stu-id="93cfb-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="93cfb-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="93cfb-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="93cfb-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93cfb-148">Click OK.</span></span>
    * <span data-ttu-id="93cfb-149">Periodisk kladde kan nu gennemgås, godkendes eller bogføres afhængigt af krav og konfiguration.</span><span class="sxs-lookup"><span data-stu-id="93cfb-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


