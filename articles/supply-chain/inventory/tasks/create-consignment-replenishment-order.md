---
title: Oprette en genopfyldningsordre til konsignation
description: Dette emne forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018347"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="9b1dc-103">Oprette en genopfyldningsordre til konsignation</span><span class="sxs-lookup"><span data-stu-id="9b1dc-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b1dc-104">Dette emne forklarer, hvordan du kan oprette en genopfyldningsordre til konsignation, hvor du kan spore den forventede levering fra en leverandør til dit konsignationslager.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="9b1dc-105">Det viser også, hvordan du registrerer modtagelse af produkter, så konsignationslageret registreres som disponibel lagerbeholdning, der ejes af leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="9b1dc-106">Denne procedure vil normalt ske via en indkøber.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="9b1dc-107">Du kan bruge denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="9b1dc-108">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="9b1dc-109">Oprette en genopfyldningsordre til konsignation</span><span class="sxs-lookup"><span data-stu-id="9b1dc-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="9b1dc-110">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Konsignation > Genopfyldningsordrer til konsignation**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="9b1dc-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-111">Select **New**.</span></span>
3. <span data-ttu-id="9b1dc-112">I feltet **Kreditorkonto** skal du vælge kreditor **US-104** (du skal vælge en kreditor, der er registreret som ejer på siden **lagerejere** ).</span><span class="sxs-lookup"><span data-stu-id="9b1dc-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="9b1dc-113">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-113">Select **OK**.</span></span>
5. <span data-ttu-id="9b1dc-114">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-114">Select **Add line**.</span></span>
6. <span data-ttu-id="9b1dc-115">I feltet **varenummer** skal du skrive `M9211CI` (du skal vælge en vare, der er oprettet til konsignationslager).</span><span class="sxs-lookup"><span data-stu-id="9b1dc-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="9b1dc-116">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="9b1dc-117">Angiv en dato i feltet **Ønsket leveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="9b1dc-118">De ønskede og bekræftede datoer, der bruges af MRP-programmet for den forventede ankomst af varer.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="9b1dc-119">Angiv en dato i feltet **Bekræftet leveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="9b1dc-120">Vis eller skjul sektionen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="9b1dc-121">Vælg fanen **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="9b1dc-122">Opdater siden for at få vist ejeren i feltet **Ejer af lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="9b1dc-123">Leverandør US-104 er nu anført som ejer.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="9b1dc-124">Kontroller lagerposteringsstatussen</span><span class="sxs-lookup"><span data-stu-id="9b1dc-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="9b1dc-125">Vælg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="9b1dc-126">Vælg **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="9b1dc-127">Bemærk, at feltet **Modtagelse** er indstillet til **Bestilt** i den ønskede række.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="9b1dc-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="9b1dc-129">Modtag varer</span><span class="sxs-lookup"><span data-stu-id="9b1dc-129">Receive items</span></span>
1. <span data-ttu-id="9b1dc-130">Vælg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="9b1dc-131">Skriv en værdi i feltet **Ekstern produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="9b1dc-132">Skriv et tal i feltet **Antal** , der er lavere end det tal, der vises der.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="9b1dc-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="9b1dc-134">Kontroller lagerbeholdningen</span><span class="sxs-lookup"><span data-stu-id="9b1dc-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="9b1dc-135">Vælg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="9b1dc-136">Vælg **Disponibelt lager**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="9b1dc-137">Vælg **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-137">Select **Overview**.</span></span> <span data-ttu-id="9b1dc-138">De varer, der er modtaget som konsignationslager, der ejes af leverandøren, er disponible.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="9b1dc-139">Det resterende antal på genopfyldningsordren til konsignation vises i feltet **Bestilt i alt**.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="9b1dc-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b1dc-140">Close the page.</span></span>

