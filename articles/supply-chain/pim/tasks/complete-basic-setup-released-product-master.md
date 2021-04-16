---
title: Fuldføre grundlæggende konfiguration af en frigivet produktmaster
description: Dette emne viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.
author: ShylaThompson
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c41e9e3267f72a2452eddfeb15f8f5cba79b0b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820148"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="6c969-103">Fuldføre grundlæggende konfiguration af en frigivet produktmaster</span><span class="sxs-lookup"><span data-stu-id="6c969-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c969-104">Dette emne viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="6c969-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="6c969-105">Dette er den tredje procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c969-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="6c969-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6c969-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6c969-107">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="6c969-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="6c969-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6c969-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="6c969-109">Vælg produktmasteren, der er frigivet i den anden procedure.</span><span class="sxs-lookup"><span data-stu-id="6c969-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="6c969-110">Denne produktmaster er oprettet med teknologien Dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6c969-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="6c969-111">Vælg **Produkt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6c969-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="6c969-112">Vælg **Dimensionsgrupper** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6c969-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="6c969-113">Vælg rullelisten i feltet **Lagringsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c969-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6c969-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6c969-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="6c969-115">Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner, der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="6c969-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="6c969-116">Vælg **Sted** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="6c969-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="6c969-117">Vælg rullelisten i feltet **Sporingsdimensionsgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c969-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6c969-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6c969-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="6c969-119">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="6c969-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="6c969-120">Vælg **Ingen** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="6c969-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="6c969-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c969-121">Click **OK**.</span></span>
10. <span data-ttu-id="6c969-122">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6c969-122">Click **Edit**.</span></span>
11. <span data-ttu-id="6c969-123">Vælg rullelisten i feltet **Varemodelgruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c969-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6c969-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6c969-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="6c969-125">Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med indgående varer og vareafgange.</span><span class="sxs-lookup"><span data-stu-id="6c969-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="6c969-126">De bestemmer også, hvordan der beregnes vareforbrug.</span><span class="sxs-lookup"><span data-stu-id="6c969-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="6c969-127">Vælg **FIFO** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="6c969-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="6c969-128">Udvid sektionen **Administrer omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="6c969-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="6c969-129">Vælg rullelisten i feltet **Varegruppe** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c969-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="6c969-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6c969-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="6c969-131">Varegrupper anvendes til at styre lagerbeholdningen ved at opdele lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="6c969-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="6c969-132">Vælg **CarAudio** til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="6c969-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="6c969-133">Vælg **Plan** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6c969-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="6c969-134">Vælg **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="6c969-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="6c969-135">Vælg en indstilling i feltet **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="6c969-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="6c969-136">Vælg **Produktion** for at angive, at standardindstillingen for denne produktmaster er at producere den.</span><span class="sxs-lookup"><span data-stu-id="6c969-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="6c969-137">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6c969-137">Select **Save**.</span></span>
20. <span data-ttu-id="6c969-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6c969-138">Close the page.</span></span>
21. <span data-ttu-id="6c969-139">Luk formularen **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="6c969-139">Close the **Released product details** form.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]