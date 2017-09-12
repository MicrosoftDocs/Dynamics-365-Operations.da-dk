--- 
title: Oprette callcenter-ordrer
description: "Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="c1997-103">Oprette callcenter-ordrer</span><span class="sxs-lookup"><span data-stu-id="c1997-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c1997-104">Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden.</span><span class="sxs-lookup"><span data-stu-id="c1997-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="c1997-105">Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter.</span><span class="sxs-lookup"><span data-stu-id="c1997-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="c1997-106">Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.</span><span class="sxs-lookup"><span data-stu-id="c1997-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="c1997-107">Gå til Detail og handel > Kunder > Kundeservice.</span><span class="sxs-lookup"><span data-stu-id="c1997-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="c1997-108">Angiv søgekriterierne til at søge efter kunden i feltet Søgetekst.</span><span class="sxs-lookup"><span data-stu-id="c1997-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="c1997-109">Til denne eksempelprocedure skal du skrive "karen" og trykke på tab.</span><span class="sxs-lookup"><span data-stu-id="c1997-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="c1997-110">Klik på Søg.</span><span class="sxs-lookup"><span data-stu-id="c1997-110">Click Search.</span></span>
    * <span data-ttu-id="c1997-111">Da der kun er én kunde med navnet Karen i demodataene, vælges de automatisk.</span><span class="sxs-lookup"><span data-stu-id="c1997-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="c1997-112">Klik på Ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c1997-112">Click New sales order.</span></span>
5. <span data-ttu-id="c1997-113">Udvis eller skjul sektionen Salgsordrehoved.</span><span class="sxs-lookup"><span data-stu-id="c1997-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="c1997-114">Vælg kildekoden til kataloget.</span><span class="sxs-lookup"><span data-stu-id="c1997-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="c1997-115">Hvis der ikke er nogen aktive kildekoder, kan du lukke feltet Kilde og springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="c1997-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="c1997-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="c1997-116">Click Add line.</span></span>
8. <span data-ttu-id="c1997-117">Indtast ordet til varesøgning i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="c1997-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="c1997-118">Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab.</span><span class="sxs-lookup"><span data-stu-id="c1997-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="c1997-119">Så vises vinduet til varesøgning.</span><span class="sxs-lookup"><span data-stu-id="c1997-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="c1997-120">Vælg det produkt, der skal føjes til salgsordren</span><span class="sxs-lookup"><span data-stu-id="c1997-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="c1997-121">Angiv salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="c1997-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="c1997-122">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="c1997-122">Click Create.</span></span>
12. <span data-ttu-id="c1997-123">Klik på Fuldført for at hente kundebetalingen.</span><span class="sxs-lookup"><span data-stu-id="c1997-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="c1997-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c1997-124">Click Add.</span></span>
    * <span data-ttu-id="c1997-125">Linket Tilføj findes under fanen Betalinger.</span><span class="sxs-lookup"><span data-stu-id="c1997-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="c1997-126">Udvid fanen Betalinger, hvis den er skjult.</span><span class="sxs-lookup"><span data-stu-id="c1997-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="c1997-127">Vælg betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="c1997-127">Select the payment method.</span></span>
    * <span data-ttu-id="c1997-128">Til denne procedure skal du vælge kontantbetalingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="c1997-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="c1997-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c1997-129">Close the page.</span></span>
16. <span data-ttu-id="c1997-130">Indtast beløbet.</span><span class="sxs-lookup"><span data-stu-id="c1997-130">Enter the amount.</span></span>
    * <span data-ttu-id="c1997-131">Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="c1997-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="c1997-132">Det giver dig mulighed for at fuldføre ordren som fuldt ud betalt.</span><span class="sxs-lookup"><span data-stu-id="c1997-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="c1997-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c1997-133">Click OK.</span></span>
18. <span data-ttu-id="c1997-134">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="c1997-134">Click Submit.</span></span>


