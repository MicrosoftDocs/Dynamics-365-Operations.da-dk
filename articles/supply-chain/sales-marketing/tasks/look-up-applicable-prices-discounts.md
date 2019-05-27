---
title: Slå gældende priser og rabatter op
description: Denne fremgangsmåde viser, hvordan du finder pris og/eller rabat for et produkt, der er gyldig for en bestemt debitor, uden at oprette en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95e651898da0e0fbd1221f61436ffac59db09e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549238"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="5c719-103">Slå gældende priser og rabatter op</span><span class="sxs-lookup"><span data-stu-id="5c719-103">Look up applicable prices and discounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c719-104">Denne fremgangsmåde viser, hvordan du finder pris og/eller rabat for et produkt, der er gyldig for en bestemt debitor, uden at oprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="5c719-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="5c719-105">Proceduren fører dig gennem et specifikt eksempel, og du skal følge eksemplet med USMF-demofirmaet for at vælge de nødvendige værdier.</span><span class="sxs-lookup"><span data-stu-id="5c719-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="5c719-106">Find den gældende pris</span><span class="sxs-lookup"><span data-stu-id="5c719-106">Find the applicable price</span></span>
1. <span data-ttu-id="5c719-107">Gå til Salg og marketing > Priser og rabatter > Find priser.</span><span class="sxs-lookup"><span data-stu-id="5c719-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="5c719-108">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="5c719-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5c719-109">Find og vælg debitor US-001 på listen.</span><span class="sxs-lookup"><span data-stu-id="5c719-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="5c719-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5c719-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5c719-111">Skriv 'T0004' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="5c719-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="5c719-112">Feltet Mængde er som standard indstillet til 1.</span><span class="sxs-lookup"><span data-stu-id="5c719-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="5c719-113">Men, hvis du kender størrelsen på den ordre, som debitoren har til hensigt at placere for det pågældende produkt, skal du angive denne værdi i stedet.</span><span class="sxs-lookup"><span data-stu-id="5c719-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="5c719-114">Disse oplysninger er relevante, hvis samhandelsaftaler med debitoren har mængdereduktioner, dvs. produktets pris afhænger af den minimummængde, der er købt.</span><span class="sxs-lookup"><span data-stu-id="5c719-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="5c719-115">Indtast en dato for, hvornår debitoren forventer at afgive en ordre, i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="5c719-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="5c719-116">Datoen kan være dags dato eller en dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="5c719-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="5c719-117">Systemet returnerer nu den pris, der gælder for det valgte produkt, når det er købt af den valgte debitor på den valgte dato med en bestemt mængde.</span><span class="sxs-lookup"><span data-stu-id="5c719-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="5c719-118">Hvis debitor US-001 f.eks. har købt 1 enhed af produkt T0004 i dag, vil debitoren blive opkrævet 350 kr. pr. enhed.</span><span class="sxs-lookup"><span data-stu-id="5c719-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="5c719-119">Prisen kommer fra en eksisterende og aktiv samhandelsaftale med debitoren.</span><span class="sxs-lookup"><span data-stu-id="5c719-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="5c719-120">Andre felter på siden giver flere detaljer om produktpris og produktomkostninger (hvis konfigureret på produktmasteren) samt beregner rentabilitet.</span><span class="sxs-lookup"><span data-stu-id="5c719-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="5c719-121">Hvis indstillingen Vis relaterede produktvarianter er valgt, betyder det, at der er flere samhandelsaftaler for produktets varianter.</span><span class="sxs-lookup"><span data-stu-id="5c719-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="5c719-122">Klik i afkrydsningsfeltet Vis relaterede produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="5c719-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="5c719-123">En liste over produktvarianterne vises sammen med oplysninger om deres dimensioner.</span><span class="sxs-lookup"><span data-stu-id="5c719-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="5c719-124">Markér den linje, der repræsenterer farven Hvid, på listen.</span><span class="sxs-lookup"><span data-stu-id="5c719-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="5c719-125">Bemærk, at produktprisen nu er forskellig fra den, der blev vist tidligere, da den ikke var angivet pr. dimension.</span><span class="sxs-lookup"><span data-stu-id="5c719-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="5c719-126">Klik på Vis salgspriser.</span><span class="sxs-lookup"><span data-stu-id="5c719-126">Click View sales prices.</span></span>
    * <span data-ttu-id="5c719-127">Siden Pris (salg) viser alle de samhandelsaftaler, der gælder for produktet, herunder dets varianter.</span><span class="sxs-lookup"><span data-stu-id="5c719-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="5c719-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c719-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="5c719-129">Find den gældende rabat</span><span class="sxs-lookup"><span data-stu-id="5c719-129">Find the applicable discount</span></span>
    * <span data-ttu-id="5c719-130">Kontrollér, at feltet Debitorkonto indeholder debitornummer US-001</span><span class="sxs-lookup"><span data-stu-id="5c719-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="5c719-131">Skriv 'T0012' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="5c719-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="5c719-132">Sørg for, at feltet Mængde er angivet til 1.</span><span class="sxs-lookup"><span data-stu-id="5c719-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="5c719-133">De følgende oplysninger om priser, der vises for produkt T0012, kommer fra en eller flere samhandelsaftaler: prisen pr. enhed er 1.000 kr., og rabatprocenten er 5.</span><span class="sxs-lookup"><span data-stu-id="5c719-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="5c719-134">Angiv antallet til '20'.</span><span class="sxs-lookup"><span data-stu-id="5c719-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="5c719-135">Den øgede ordremængde medfører den linjerabat, der tilbydes debitoren, så denne vil skifte fra 5 til 7 procent.</span><span class="sxs-lookup"><span data-stu-id="5c719-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="5c719-136">Det forventede Nettobeløb beregnes baseret på enhedspris, rabat og samlede mængde.</span><span class="sxs-lookup"><span data-stu-id="5c719-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="5c719-137">Klik på Vis linjerabat.</span><span class="sxs-lookup"><span data-stu-id="5c719-137">Click View line discount.</span></span>
    * <span data-ttu-id="5c719-138">Der er to linjerabataftaler for produkt T0012, der angiver en rabat på 5 procents rabat for en ordrelinjemængde fra 1 til 10, og 7 procents rabat på ordremængder over 10.</span><span class="sxs-lookup"><span data-stu-id="5c719-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="5c719-139">Bemærk, at rabatterne anvendes på en gruppe af produkter, i dette eksempel Gruppekode 01, hvor produkt T0012 er medlem.</span><span class="sxs-lookup"><span data-stu-id="5c719-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="5c719-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c719-140">Close the page.</span></span>

