--- 
title: "Fuldføre grundlæggende konfiguration af en frigivet produktmaster"
description: "Denne fremgangsmåde viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8e08fbd53657bcf31a12166cf06b614ce3e3f131
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="83950-103">Fuldføre grundlæggende konfiguration af en frigivet produktmaster</span><span class="sxs-lookup"><span data-stu-id="83950-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83950-104">Denne fremgangsmåde viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="83950-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="83950-105">Dette er den tredje procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="83950-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="83950-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="83950-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="83950-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="83950-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="83950-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="83950-109">Vælg produktmasteren, der er frigivet i den anden procedure.</span><span class="sxs-lookup"><span data-stu-id="83950-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="83950-110">Denne produktmaster er oprettet med teknologien Dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="83950-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="83950-111">Klik på Produkt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="83950-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="83950-112">Klik på Dimensionsgrupper for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="83950-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="83950-113">Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="83950-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="83950-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="83950-115">Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner, der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="83950-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="83950-116">Vælg Sted til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="83950-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="83950-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="83950-118">Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="83950-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="83950-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="83950-120">Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner der bruges til transaktion af produktet.</span><span class="sxs-lookup"><span data-stu-id="83950-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="83950-121">Vælg Ingen til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="83950-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="83950-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="83950-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="83950-123">Click OK.</span></span>
12. <span data-ttu-id="83950-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="83950-125">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="83950-125">Click Edit.</span></span>
    * <span data-ttu-id="83950-126">Åbn formularen Frigivne produktdetaljer for at fortsætte opsætningsopgaven.</span><span class="sxs-lookup"><span data-stu-id="83950-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="83950-127">Klik på rullelisten i feltet Varemodelgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="83950-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="83950-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="83950-129">Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med indgående varer og vareafgange.</span><span class="sxs-lookup"><span data-stu-id="83950-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="83950-130">De bestemmer også, hvordan der beregnes vareforbrug.</span><span class="sxs-lookup"><span data-stu-id="83950-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="83950-131">Vælg FIFO til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="83950-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="83950-132">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="83950-133">Vis eller skjul sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="83950-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="83950-134">Klik på rullelisten i feltet Varegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="83950-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="83950-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="83950-136">Varegrupper anvendes til at styre lagerbeholdningen ved at opdele lagervarer i grupper.</span><span class="sxs-lookup"><span data-stu-id="83950-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="83950-137">Vælg CarAudio til denne procedure.</span><span class="sxs-lookup"><span data-stu-id="83950-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="83950-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83950-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="83950-139">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="83950-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="83950-140">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="83950-140">Click Default order settings.</span></span>
23. <span data-ttu-id="83950-141">Vælg en indstilling i feltet Standardordretype.</span><span class="sxs-lookup"><span data-stu-id="83950-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="83950-142">Vælg Produktion for at angive, at standardindstillingen for denne produktmaster er at producere den.</span><span class="sxs-lookup"><span data-stu-id="83950-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="83950-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="83950-143">Close the page.</span></span>
25. <span data-ttu-id="83950-144">Luk formularen Frigivne produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="83950-144">Close the Released product details form.</span></span>


