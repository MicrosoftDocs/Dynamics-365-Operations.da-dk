---
title: Fuldføre grundlæggende konfiguration af en frigivet produktmaster
description: Dette emne viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 668b60efa55fa553cf308d5bfc5da7e23f460366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987023"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="86516-103">Fuldføre grundlæggende konfiguration af en frigivet produktmaster</span><span class="sxs-lookup"><span data-stu-id="86516-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86516-104">Dette emne viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="86516-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="86516-105">Dette er den tredje procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="86516-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="86516-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="86516-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="86516-107">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="86516-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="86516-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="86516-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="86516-109">Vælg produktmasteren, der er frigivet i den anden procedure.</span><span class="sxs-lookup"><span data-stu-id="86516-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="86516-110">Denne produktmaster er oprettet med teknologien Dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="86516-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="86516-111">Vælg **Produkt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="86516-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="86516-112">Vælg **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="86516-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="86516-113">Vælg rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="86516-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="86516-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="86516-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="86516-115">Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner, der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="86516-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="86516-116">Vælg **Sted** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="86516-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="86516-117">Vælg rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="86516-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="86516-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="86516-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="86516-119">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="86516-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="86516-120">Vælg **Ingen** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="86516-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="86516-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="86516-121">Click **OK**.</span></span>
10. <span data-ttu-id="86516-122">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="86516-122">Click **Edit**.</span></span>
11. <span data-ttu-id="86516-123">Vælg rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="86516-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="86516-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="86516-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="86516-125">Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med indgående varer og vareafgange.</span><span class="sxs-lookup"><span data-stu-id="86516-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="86516-126">De bestemmer også, hvordan der beregnes vareforbrug.</span><span class="sxs-lookup"><span data-stu-id="86516-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="86516-127">Vælg **FIFO** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="86516-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="86516-128">Udvid sektionen **Administrer omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="86516-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="86516-129">Vælg rullelisten i feltet **Varegruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="86516-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="86516-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="86516-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="86516-131">Varegrupper anvendes til at styre lagerbeholdningen ved at opdele lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="86516-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="86516-132">Vælg **CarAudio** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="86516-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="86516-133">Vælg **Plan** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="86516-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="86516-134">Vælg **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="86516-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="86516-135">Vælg en indstilling i feltet **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="86516-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="86516-136">Vælg **Produktion** for at angive, at standardindstillingen for denne produktmaster er at producere den.</span><span class="sxs-lookup"><span data-stu-id="86516-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="86516-137">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86516-137">Select **Save**.</span></span>
20. <span data-ttu-id="86516-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="86516-138">Close the page.</span></span>
21. <span data-ttu-id="86516-139">Luk formularen **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="86516-139">Close the **Released product details** form.</span></span>

