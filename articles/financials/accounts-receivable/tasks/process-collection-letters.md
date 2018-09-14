--- 
title: Behandle rykkere
description: "Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a1bdf9528b52daa7bb719ea5a751a01e56a8c963
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="71428-103">Behandle rykkere</span><span class="sxs-lookup"><span data-stu-id="71428-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71428-104">Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere.</span><span class="sxs-lookup"><span data-stu-id="71428-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="71428-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="71428-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="71428-106">Konfigurere et rykkerforløb i en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="71428-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="71428-107">Gå til Kredit og inkasso > Opsætning > Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="71428-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="71428-108">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="71428-108">Click Edit.</span></span>
    * <span data-ttu-id="71428-109">Vælg et rykkerforløb på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="71428-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="71428-110">Hvis du ikke vil oprette rykkere for transaktioner med denne posteringsprofil, skal du lade feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="71428-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="71428-111">Under fanen Tabelbegrænsninger kan du ændre den måde, som rykkere behandles på.</span><span class="sxs-lookup"><span data-stu-id="71428-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="71428-112">Hvis dette felt er indstillet til Ja, oprettes rykkerne for denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="71428-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="71428-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71428-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="71428-114">Opret rykkere</span><span class="sxs-lookup"><span data-stu-id="71428-114">Create collection letters</span></span>
1. <span data-ttu-id="71428-115">Gå til Kredit og inkasso > Rykker > Opret rykkere.</span><span class="sxs-lookup"><span data-stu-id="71428-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="71428-116">Du skal vælge de posteringstyper, du vil rykke for.</span><span class="sxs-lookup"><span data-stu-id="71428-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="71428-117">Alle åbne transaktioner for disse typer medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="71428-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="71428-118">Vælg en indstilling i feltet Rykker.</span><span class="sxs-lookup"><span data-stu-id="71428-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="71428-119">Angiv datoen for rykkeren.</span><span class="sxs-lookup"><span data-stu-id="71428-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="71428-120">Der findes to posteringsprofilindstillinger: Konto – Brug den posteringsprofil, der er tildelt kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="71428-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="71428-121">Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="71428-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="71428-122">Vælg en posteringsprofil, hvis du har ændret "Anvend posteringsprofil fra" til Vælg.</span><span class="sxs-lookup"><span data-stu-id="71428-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="71428-123">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="71428-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="71428-124">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="71428-124">Click Filter.</span></span>
6. <span data-ttu-id="71428-125">Angiv Kunde-id i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="71428-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="71428-126">Indtast for eksempel "US-001".</span><span class="sxs-lookup"><span data-stu-id="71428-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="71428-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71428-127">Click OK.</span></span>
8. <span data-ttu-id="71428-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71428-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="71428-129">Udskrive rykkere</span><span class="sxs-lookup"><span data-stu-id="71428-129">Print collection letters</span></span>
1. <span data-ttu-id="71428-130">Gå til Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere.</span><span class="sxs-lookup"><span data-stu-id="71428-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="71428-131">Vælg "Oprettet" i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="71428-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="71428-132">Vælg "Ikke udskrevet" i feltet Udskrevet.</span><span class="sxs-lookup"><span data-stu-id="71428-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="71428-133">Klik på Udskriv.</span><span class="sxs-lookup"><span data-stu-id="71428-133">Click Print.</span></span>
5. <span data-ttu-id="71428-134">Klik på Rykkernota.</span><span class="sxs-lookup"><span data-stu-id="71428-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="71428-135">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="71428-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="71428-136">Angiv skæringsdatoen for bogføringer</span><span class="sxs-lookup"><span data-stu-id="71428-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="71428-137">Klik på OK for at udskrive rykkeren.</span><span class="sxs-lookup"><span data-stu-id="71428-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="71428-138">Bogføre rykkeren</span><span class="sxs-lookup"><span data-stu-id="71428-138">Post the collection letter</span></span>
1. <span data-ttu-id="71428-139">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="71428-139">Click Post.</span></span>
2. <span data-ttu-id="71428-140">Angiv rykkerens bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="71428-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="71428-141">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="71428-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="71428-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71428-142">Click OK.</span></span>
5. <span data-ttu-id="71428-143">Vælg "Bogført" i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="71428-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="71428-144">Vælg en indstilling i feltet Udskrevet.</span><span class="sxs-lookup"><span data-stu-id="71428-144">In the Printed field, select an option.</span></span>


