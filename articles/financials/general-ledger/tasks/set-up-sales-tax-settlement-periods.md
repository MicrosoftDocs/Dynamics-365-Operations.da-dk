--- 
title: Konfigurer momsafregningsperioder
description: Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0511d2c950139f9ac101af6e555f2c4523200aa5
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ceaf0-103">Konfigurer momsafregningsperioder</span><span class="sxs-lookup"><span data-stu-id="ceaf0-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ceaf0-104">Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ceaf0-105">Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ceaf0-106">Alle momskoder, der er knyttet til afregningsperioden, udlignes.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ceaf0-107">Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="ceaf0-108">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="ceaf0-109">Gå til Moms > Indirekte skatter > Moms > Momsafregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="ceaf0-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-110">Click New.</span></span>
3. <span data-ttu-id="ceaf0-111">Skriv en værdi i feltet Afregningsperiode.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="ceaf0-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ceaf0-113">I feltet Momsmyndighed skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ceaf0-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ceaf0-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ceaf0-116">Klik på rullelisten i feltet Betalingsbetingelse for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ceaf0-117">De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ceaf0-118">Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="ceaf0-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ceaf0-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ceaf0-121">Vælg en type for intervaller for afregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="ceaf0-122">Angiv antallet af enheder i periodeintervallet pr. periode.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ceaf0-123">For eksempel har en kvart 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="ceaf0-124">Markér eller fjern markeringen af afkrydsningsfeltet Brug batchbehandling til afregning af moms.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="ceaf0-125">Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ceaf0-126">Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="ceaf0-127">Udvid fanen Periodeintervaller.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="ceaf0-128">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-128">Click Add.</span></span>
16. <span data-ttu-id="ceaf0-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ceaf0-130">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="ceaf0-131">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="ceaf0-132">Klik på Nyt periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-132">Click New period interval.</span></span>
    * <span data-ttu-id="ceaf0-133">Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ceaf0-134">Du kan vende tilbage og tilføje nye periodeintervaller efter behov.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="ceaf0-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ceaf0-135">Close the page.</span></span>


