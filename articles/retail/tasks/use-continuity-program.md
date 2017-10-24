--- 
title: Bruge et kontinuitetsprogram
description: "Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d3b5690bfbd10b77e784d35d0c4f4518de58333
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="use-a-continuity-program"></a><span data-ttu-id="f9af0-103">Bruge et kontinuitetsprogram</span><span class="sxs-lookup"><span data-stu-id="f9af0-103">Use a continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f9af0-104">Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f9af0-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="f9af0-105">For at udføre denne procedure skal brugeren være oprettet som bruger af et callcenter.</span><span class="sxs-lookup"><span data-stu-id="f9af0-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="f9af0-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="f9af0-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="f9af0-107">Gå til Detail og handel > Kunder > Kundeservice.</span><span class="sxs-lookup"><span data-stu-id="f9af0-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="f9af0-108">Skriv 'Karen' i feltet Søgetekst, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="f9af0-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="f9af0-109">Dialogboksen for avanceret søgning åbnes.</span><span class="sxs-lookup"><span data-stu-id="f9af0-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="f9af0-110">Hvis ikke, skal du klikke på Søg til højre for feltet.</span><span class="sxs-lookup"><span data-stu-id="f9af0-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="f9af0-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f9af0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f9af0-112">Der er én række, hvor Karen Berg vises.</span><span class="sxs-lookup"><span data-stu-id="f9af0-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="f9af0-113">Vælg rækken ved at klikke på markeringskolonnen yderst til venstre i gitteret.</span><span class="sxs-lookup"><span data-stu-id="f9af0-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="f9af0-114">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="f9af0-114">Click Select.</span></span>
5. <span data-ttu-id="f9af0-115">Klik på Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f9af0-115">Click New sales order.</span></span>
    * <span data-ttu-id="f9af0-116">Det er en god ide at notere salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="f9af0-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="f9af0-117">Du skal bruge det senere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="f9af0-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="f9af0-118">Skriv '88000' i feltet Varenummer, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="f9af0-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="f9af0-119">Dette er en kontinuitetsvare i USRT-demodata.</span><span class="sxs-lookup"><span data-stu-id="f9af0-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="f9af0-120">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="f9af0-120">Click Complete.</span></span>
8. <span data-ttu-id="f9af0-121">Vælg 'Visa' i feltet Betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="f9af0-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="f9af0-122">Klik på Tilføj kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f9af0-122">Click Add credit card.</span></span>
    * <span data-ttu-id="f9af0-123">Angiv de nødvendige kreditkortoplysninger på denne side.</span><span class="sxs-lookup"><span data-stu-id="f9af0-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="f9af0-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9af0-124">Click OK.</span></span>
11. <span data-ttu-id="f9af0-125">Vis sektionen Betaling.</span><span class="sxs-lookup"><span data-stu-id="f9af0-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="f9af0-126">Hvis du vil sende en ordre via et callcenter, skal der angives betalinger for ordren.</span><span class="sxs-lookup"><span data-stu-id="f9af0-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="f9af0-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9af0-127">Click OK.</span></span>
13. <span data-ttu-id="f9af0-128">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="f9af0-128">Click Submit.</span></span>
    * <span data-ttu-id="f9af0-129">Du har oprettet en ny kontinuitetsordre.</span><span class="sxs-lookup"><span data-stu-id="f9af0-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="f9af0-130">Derefter skal du køre to batchprocesser, der bruges til at behandle kontinuitetsordrerne.</span><span class="sxs-lookup"><span data-stu-id="f9af0-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="f9af0-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f9af0-131">Close the page.</span></span>
15. <span data-ttu-id="f9af0-132">Gå til Detail og handel > Kontiniutet > Udfør behandling af fortløbende betalinger.</span><span class="sxs-lookup"><span data-stu-id="f9af0-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="f9af0-133">Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="f9af0-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="f9af0-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9af0-134">Click OK.</span></span>
18. <span data-ttu-id="f9af0-135">Gå til Detail og handel > Kontiniutet > Opret fortløbende underordnede ordrer.</span><span class="sxs-lookup"><span data-stu-id="f9af0-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="f9af0-136">Denne proces opretter nye salgsordrer, der er baseret på indstillingerne for kontinuitetsprogrammerne.</span><span class="sxs-lookup"><span data-stu-id="f9af0-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="f9af0-137">Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="f9af0-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="f9af0-138">Vare '88000' er en kontinuitetsvare i USRT-demodata.</span><span class="sxs-lookup"><span data-stu-id="f9af0-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="f9af0-139">Indtast eller vælg en værdi i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f9af0-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="f9af0-140">Angiv nummeret på salgsordren, du noterede tidligere i proceduren.</span><span class="sxs-lookup"><span data-stu-id="f9af0-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="f9af0-141">Derved reduceres behandlingstiden til et minimum for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="f9af0-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="f9af0-142">Feltet Salgsordre er valgfrit – du kan behandle alle ordrer for alle ét program.</span><span class="sxs-lookup"><span data-stu-id="f9af0-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="f9af0-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f9af0-143">Click OK.</span></span>


