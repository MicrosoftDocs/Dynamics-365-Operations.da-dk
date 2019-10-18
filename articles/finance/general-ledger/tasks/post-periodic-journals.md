---
title: Bogføre periodiske kladder
description: Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fdf630e9d292d0e016b6624a82b047d32bab898
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175348"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="cc2e8-103">Bogføre periodiske kladder</span><span class="sxs-lookup"><span data-stu-id="cc2e8-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc2e8-104">Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="cc2e8-105">Når du opretter den periodiske kladde, angiver du periodeintervallet for gentagelsen, eksempelvis dage eller måneder.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="cc2e8-106">Denne opgaveguide opretter en periodisk kladde med en månedlig gentagelse.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="cc2e8-107">Gå til **Navigationsrude > Moduler > Finans > Periodiske opgaver > Periodiske kladder**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="cc2e8-108">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-108">Click **New**.</span></span>
3. <span data-ttu-id="cc2e8-109">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="cc2e8-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cc2e8-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="cc2e8-112">Beskrivelsen vil være navnet på den periodiske kladde, når den hentes senere, så sørg for at give den et navn, der er relevant.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="cc2e8-113">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="cc2e8-114">En periodisk kladde vil typisk omfatte flere kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="cc2e8-115">denne opgaveguide tilføjer dog kun én linje.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="cc2e8-116">Indtast en dato i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="cc2e8-117">Feltet **Dato** indeholder bogføringsdatoen for den næste overførsel til kassekladden.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="cc2e8-118">For journaler, der vil blive hentet hver måned, anbefales det at bruge datoen i den måned, hvor den bogføres, typisk den første eller den sidste dato i perioden.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="cc2e8-119">Det er muligt at lade feltet være tomt og give en dato, når kladden er hentet, ved hjælp af feltet Tom dato.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="cc2e8-120">Feltet opdateres automatisk til den næste tilbagevendende dato, når der hentes transaktioner.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="cc2e8-121">I feltet **Konto** skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="cc2e8-122">Vælg en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="cc2e8-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-123">Close the page.</span></span>
11. <span data-ttu-id="cc2e8-124">Angiv et tal i feltet **Debet**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="cc2e8-125">I feltet **Modkonto** skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="cc2e8-126">Vælg "Måneder" i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="cc2e8-127">Angiv "1" i feltet **Antal enheder**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="cc2e8-128">Indtast en dato i feltet **Sidste dato**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="cc2e8-129">Angivelse af sidste dato i den forløbne periode vil forhindre, at gentagelseskladden ved en fejltagelse oprettes i den forkerte startperiode.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="cc2e8-130">Sidste dato opdateres senere, hver gang den periodiske kladde hentes.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="cc2e8-131">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-131">Click **Save**.</span></span>
17. <span data-ttu-id="cc2e8-132">Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="cc2e8-133">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-133">Click **New**.</span></span>
19. <span data-ttu-id="cc2e8-134">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="cc2e8-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="cc2e8-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="cc2e8-137">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="cc2e8-138">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="cc2e8-139">Klik i **handlingsruden** på **Periodisk kladde**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="cc2e8-140">Klik på **Hent kladde**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="cc2e8-141">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="cc2e8-142">**Til dato** fungerer som skæringsdato for de periodiske bilagslinjer.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="cc2e8-143">Baseret på gentagelsesindstilling, Sidste dato og Til dato kan den samme linje indgå mere end én gang i den kladde, der er resultatet.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="cc2e8-144">Til dato opdateres automatisk på basis af sessionsdatoen for sidste gang, den periodiske linje blev overført til en kladde.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="cc2e8-145">Skriv eller vælg en værdi i feltet **Nummer på periodisk kladde**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="cc2e8-146">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="cc2e8-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-147">Click **OK**.</span></span> <span data-ttu-id="cc2e8-148">Periodisk kladde kan nu gennemgås, godkendes eller bogføres afhængigt af krav og konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc2e8-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
