--- 
title: Definere kontinuitetsplaner
description: "Dette emne gennemgår oprettelse af et kontinuitetsprogram (kaldes også tilbagevendende ordrer)."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ac333989dd987fd3cb1d2b2769fbcdb93bdb4bd
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="define-continuity-schedules"></a><span data-ttu-id="61431-103">Definere kontinuitetsplaner</span><span class="sxs-lookup"><span data-stu-id="61431-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="61431-104">Dette emne gennemgår oprettelse af et kontinuitetsprogram (kaldes også tilbagevendende ordrer).</span><span class="sxs-lookup"><span data-stu-id="61431-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="61431-105">Dette emne bruger demodatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="61431-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="61431-106">Oprette kontinuitetsprogram</span><span class="sxs-lookup"><span data-stu-id="61431-106">Create continuity program</span></span>
1. <span data-ttu-id="61431-107">Gå til Detail og handel > Kontiniutet > Kontinuitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="61431-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="61431-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="61431-108">Click New.</span></span>
3. <span data-ttu-id="61431-109">I feltet Tidsplans-id skal du angive id'et for kontinuitetstidsplanen.</span><span class="sxs-lookup"><span data-stu-id="61431-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="61431-110">I feltet Ordrestart skal du vælge 'Første hændelse'.</span><span class="sxs-lookup"><span data-stu-id="61431-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="61431-111">Hvis en kunde afgiver en ny ordre for kontinuitetsprogrammet, er der to muligheder for produktlevering: 1.</span><span class="sxs-lookup"><span data-stu-id="61431-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="61431-112">Første hændelse: det første produkt i kontinuitetsprogrammet afsendes.</span><span class="sxs-lookup"><span data-stu-id="61431-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="61431-113">2</span><span class="sxs-lookup"><span data-stu-id="61431-113">2.</span></span> <span data-ttu-id="61431-114">Den aktuelle hændelse: Det aktuelle produkt afsendes.</span><span class="sxs-lookup"><span data-stu-id="61431-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="61431-115">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="61431-115">For example.</span></span> <span data-ttu-id="61431-116">Tre måneder inde i programmet modtager kunden det tredje i programmet.</span><span class="sxs-lookup"><span data-stu-id="61431-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="61431-117">Vælg 'Ja' for at bede om ordrens startdato.</span><span class="sxs-lookup"><span data-stu-id="61431-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="61431-118">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="61431-118">Click Add line.</span></span>
7. <span data-ttu-id="61431-119">Angiv varenummeret for første produkt ('0013') i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="61431-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="61431-120">Skriv 'CP'.</span><span class="sxs-lookup"><span data-stu-id="61431-120">Type 'CP'.</span></span>
9. <span data-ttu-id="61431-121">Angiv den dato, hvor det første produkt kan bestilles.</span><span class="sxs-lookup"><span data-stu-id="61431-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="61431-122">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="61431-122">Click Add line.</span></span>
11. <span data-ttu-id="61431-123">I feltet Varenummer skal du skrive "0014".</span><span class="sxs-lookup"><span data-stu-id="61431-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="61431-124">Fjern værdien, så feltet er tomt, i feltet Datointervalkode.</span><span class="sxs-lookup"><span data-stu-id="61431-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="61431-125">Fjern datointervallet for denne procedure.</span><span class="sxs-lookup"><span data-stu-id="61431-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="61431-126">Du skal angive datoen som trinvis fra startdatoen for første vare.</span><span class="sxs-lookup"><span data-stu-id="61431-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="61431-127">Her kan du angive intervallet for afsendelse af produkterne.</span><span class="sxs-lookup"><span data-stu-id="61431-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="61431-128">Skriv '30'.</span><span class="sxs-lookup"><span data-stu-id="61431-128">Type '30'.</span></span>
    * <span data-ttu-id="61431-129">For et månedligt program skal du angive 30 dage for intervallet.</span><span class="sxs-lookup"><span data-stu-id="61431-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="61431-130">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="61431-130">Click Add line.</span></span>
15. <span data-ttu-id="61431-131">I feltet Varenummer skal du skrive "0015".</span><span class="sxs-lookup"><span data-stu-id="61431-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="61431-132">Skriv 'Slut'.</span><span class="sxs-lookup"><span data-stu-id="61431-132">Type 'End'.</span></span>
17. <span data-ttu-id="61431-133">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="61431-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="61431-134">Tildele til kontinuitetsvare</span><span class="sxs-lookup"><span data-stu-id="61431-134">Assign to continuity item</span></span>
1. <span data-ttu-id="61431-135">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="61431-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="61431-136">Vælg vare '0016'.</span><span class="sxs-lookup"><span data-stu-id="61431-136">Select item '0016'.</span></span>
    * <span data-ttu-id="61431-137">I denne procedure skal du vælge varenummer 0016.</span><span class="sxs-lookup"><span data-stu-id="61431-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="61431-138">Normalt har du oprettet et frigivet produkt, hvor der anvendes en yderligere forretningslogik for kontinuitet, når det placeres i en salgsordre i callcenter.</span><span class="sxs-lookup"><span data-stu-id="61431-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="61431-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="61431-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61431-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="61431-140">Click Edit.</span></span>
5. <span data-ttu-id="61431-141">Udvis eller skjul sektionen Sælg.</span><span class="sxs-lookup"><span data-stu-id="61431-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="61431-142">Her kan du angive kontinuitetsprogrammet, som denne vare repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="61431-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="61431-143">Skriv det tidsplans-id, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="61431-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="61431-144">Når varen sælges i et callcenter, anvendes yderligere forretningslogik fra det valgte kontinuitetsprogram.</span><span class="sxs-lookup"><span data-stu-id="61431-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="61431-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="61431-145">Click Save.</span></span>


