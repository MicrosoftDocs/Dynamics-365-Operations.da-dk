---
title: Brug af kontinuitetsprogram
description: Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b641fb6ba5edf359a2f1f2de7b5095d73b497cf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003622"
---
# <a name="using-continuity-program"></a><span data-ttu-id="7dfe7-103">Brug af kontinuitetsprogram</span><span class="sxs-lookup"><span data-stu-id="7dfe7-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dfe7-104">Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="7dfe7-105">For at udføre denne procedure skal brugeren være oprettet som bruger af et callcenter.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="7dfe7-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="7dfe7-107">Gå til Retail og Commerce > Kunder > Kundeservice.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="7dfe7-108">Skriv 'Karen' i feltet Søgetekst, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="7dfe7-109">Dialogboksen for avanceret søgning åbnes.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="7dfe7-110">Hvis ikke, skal du klikke på Søg til højre for feltet.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="7dfe7-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7dfe7-112">Der er én række, hvor Karen Berg vises.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="7dfe7-113">Vælg rækken ved at klikke på markeringskolonnen yderst til venstre i gitteret.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="7dfe7-114">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-114">Click Select.</span></span>
5. <span data-ttu-id="7dfe7-115">Klik på Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-115">Click New sales order.</span></span>
    * <span data-ttu-id="7dfe7-116">Det er en god ide at notere salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="7dfe7-117">Du skal bruge det senere i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="7dfe7-118">Skriv '88000' i feltet Varenummer, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="7dfe7-119">Dette er en kontinuitetsvare i USRT-demodata.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="7dfe7-120">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-120">Click Complete.</span></span>
8. <span data-ttu-id="7dfe7-121">Vælg 'Visa' i feltet Betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="7dfe7-122">Klik på Tilføj kreditkort.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-122">Click Add credit card.</span></span>
    * <span data-ttu-id="7dfe7-123">Angiv de nødvendige kreditkortoplysninger på denne side.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="7dfe7-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-124">Click OK.</span></span>
11. <span data-ttu-id="7dfe7-125">Vis sektionen Betaling.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="7dfe7-126">Hvis du vil sende en ordre via et callcenter, skal der angives betalinger for ordren.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="7dfe7-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-127">Click OK.</span></span>
13. <span data-ttu-id="7dfe7-128">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-128">Click Submit.</span></span>
    * <span data-ttu-id="7dfe7-129">Du har oprettet en ny kontinuitetsordre.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="7dfe7-130">Derefter skal du køre to batchprocesser, der bruges til at behandle kontinuitetsordrerne.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="7dfe7-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-131">Close the page.</span></span>
15. <span data-ttu-id="7dfe7-132">Gå til Retail og Commerce > Kontinuitet > Udfør behandling af fortløbende betalinger.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="7dfe7-133">Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="7dfe7-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-134">Click OK.</span></span>
18. <span data-ttu-id="7dfe7-135">Gå til Retail og Commerce > Kontinuitet > Opret fortløbende underordnede ordrer.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="7dfe7-136">Denne proces opretter nye salgsordrer, der er baseret på indstillingerne for kontinuitetsprogrammerne.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="7dfe7-137">Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="7dfe7-138">Vare '88000' er en kontinuitetsvare i USRT-demodata.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="7dfe7-139">Indtast eller vælg en værdi i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="7dfe7-140">Angiv nummeret på salgsordren, du noterede tidligere i proceduren.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="7dfe7-141">Derved reduceres behandlingstiden til et minimum for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="7dfe7-142">Feltet Salgsordre er valgfrit – du kan behandle alle ordrer for alle ét program.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="7dfe7-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7dfe7-143">Click OK.</span></span>

