---
title: Opret en genopfyldningsordre til konsignation
description: "Denne procedure viser, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: c9d142e50d39f9e98adeef170da93b8137de4131
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="7b65f-103">Opret en genopfyldningsordre til konsignation</span><span class="sxs-lookup"><span data-stu-id="7b65f-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b65f-104">Denne procedure viser, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager.</span><span class="sxs-lookup"><span data-stu-id="7b65f-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="7b65f-105">Det viser også, hvordan du registrerer modtagelse af produkter, så konsignationslageret registreres som disponibel lagerbeholdning, der ejes af leverandøren.</span><span class="sxs-lookup"><span data-stu-id="7b65f-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="7b65f-106">Denne procedure vil normalt ske via en indkøber.</span><span class="sxs-lookup"><span data-stu-id="7b65f-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="7b65f-107">Du kan bruge denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="7b65f-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="7b65f-108">Denne procedure er til en funktion, der blev tilføjet i Dynamics 365 for Operations, version 1611.</span><span class="sxs-lookup"><span data-stu-id="7b65f-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="7b65f-109">Opret en genopfyldningsordre til konsignation</span><span class="sxs-lookup"><span data-stu-id="7b65f-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="7b65f-110">Gå til Indkøb og forsyning > Konsignation > Genopfyldningsordrer til konsignation.</span><span class="sxs-lookup"><span data-stu-id="7b65f-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="7b65f-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7b65f-111">Click New.</span></span>
3. <span data-ttu-id="7b65f-112">Vælg leverandøren US-104 i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="7b65f-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="7b65f-113">Du skal vælge en leverandør, der er registreret som ejer på siden Lagerejere.</span><span class="sxs-lookup"><span data-stu-id="7b65f-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="7b65f-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7b65f-114">Click OK.</span></span>
5. <span data-ttu-id="7b65f-115">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="7b65f-115">Click Add line.</span></span>
6. <span data-ttu-id="7b65f-116">I feltet Varenummer skal du skrive M9211CI.</span><span class="sxs-lookup"><span data-stu-id="7b65f-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="7b65f-117">Du skal vælge en vare, der er oprettet til konsignationslageret.</span><span class="sxs-lookup"><span data-stu-id="7b65f-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="7b65f-118">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="7b65f-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="7b65f-119">Angiv en dato i feltet Ønsket leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="7b65f-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="7b65f-120">De ønskede og bekræftede datoer, der bruges af MRP-programmet for den forventede ankomst af varer.</span><span class="sxs-lookup"><span data-stu-id="7b65f-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="7b65f-121">Angiv en dato i feltet Bekræftet leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="7b65f-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="7b65f-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="7b65f-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="7b65f-123">Klik på fanen Lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="7b65f-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="7b65f-124">Opdater siden for at få vist ejeren i feltet Ejer af lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="7b65f-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="7b65f-125">Leverandør US-104 er nu anført som ejer.</span><span class="sxs-lookup"><span data-stu-id="7b65f-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="7b65f-126">Kontroller lagerposteringsstatussen</span><span class="sxs-lookup"><span data-stu-id="7b65f-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="7b65f-127">Klik på lager.</span><span class="sxs-lookup"><span data-stu-id="7b65f-127">Click Inventory.</span></span>
2. <span data-ttu-id="7b65f-128">Klik på Transaktioner.</span><span class="sxs-lookup"><span data-stu-id="7b65f-128">Click Transactions.</span></span>
3. <span data-ttu-id="7b65f-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7b65f-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7b65f-130">Bemærk, at feltet Modtagelse er indstillet til Bestilt.</span><span class="sxs-lookup"><span data-stu-id="7b65f-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="7b65f-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7b65f-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="7b65f-132">Modtag varer</span><span class="sxs-lookup"><span data-stu-id="7b65f-132">Receive items</span></span>
1. <span data-ttu-id="7b65f-133">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="7b65f-133">Click Product receipt.</span></span>
2. <span data-ttu-id="7b65f-134">Skriv en værdi i feltet Ekstern produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="7b65f-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="7b65f-135">Skriv et tal i feltet Antal, der er lavere end det tal, der vises.</span><span class="sxs-lookup"><span data-stu-id="7b65f-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="7b65f-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7b65f-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="7b65f-137">Kontroller lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="7b65f-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="7b65f-138">Klik på lager.</span><span class="sxs-lookup"><span data-stu-id="7b65f-138">Click Inventory.</span></span>
2. <span data-ttu-id="7b65f-139">Klik på Beholdning.</span><span class="sxs-lookup"><span data-stu-id="7b65f-139">Click On-hand.</span></span>
3. <span data-ttu-id="7b65f-140">Klik på Oversigt.</span><span class="sxs-lookup"><span data-stu-id="7b65f-140">Click Overview.</span></span>
    * <span data-ttu-id="7b65f-141">De varer, der er modtaget som konsignationslager, der ejes af leverandøren, er disponible.</span><span class="sxs-lookup"><span data-stu-id="7b65f-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="7b65f-142">Det resterende antal på genopfyldningsordren til konsignation vises i feltet Bestilt i alt.</span><span class="sxs-lookup"><span data-stu-id="7b65f-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="7b65f-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7b65f-143">Close the page.</span></span>
5. <span data-ttu-id="7b65f-144">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="7b65f-144">Click Close.</span></span>

