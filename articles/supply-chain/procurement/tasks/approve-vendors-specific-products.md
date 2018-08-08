--- 
title: Godkende kreditorer til specifikke produkter
description: "Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7b4d9ff2b9831e78acae2090a8d2ad9e1178ae7a
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="9af3d-103">Godkende kreditorer til specifikke produkter</span><span class="sxs-lookup"><span data-stu-id="9af3d-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9af3d-104">Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="9af3d-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="9af3d-105">Dette gør det muligt at styre, hvilke kreditorer der kan bruges, når produktet føjes til en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="9af3d-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="9af3d-106">Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="9af3d-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="9af3d-107">Denne opgave vil typisk blive udført af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="9af3d-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="9af3d-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="9af3d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9af3d-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9af3d-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9af3d-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9af3d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9af3d-111">Udvid sektionen Indkøb.</span><span class="sxs-lookup"><span data-stu-id="9af3d-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="9af3d-112">Hvis der ingen primær kreditor vises i feltet Kreditor, skal du tilføje denne kreditor som en godkendt kreditor med følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="9af3d-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="9af3d-113">Noter kreditornummeret ned, hvis der vises et.</span><span class="sxs-lookup"><span data-stu-id="9af3d-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="9af3d-114">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="9af3d-115">Klik på Opsætning.</span><span class="sxs-lookup"><span data-stu-id="9af3d-115">Click Setup.</span></span>
7. <span data-ttu-id="9af3d-116">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9af3d-116">Click Add.</span></span>
8. <span data-ttu-id="9af3d-117">Indtast eller vælg en værdi i feltet Kreditor.</span><span class="sxs-lookup"><span data-stu-id="9af3d-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="9af3d-118">Vælg den godkendte kreditor.</span><span class="sxs-lookup"><span data-stu-id="9af3d-118">Select the approved vendor.</span></span> <span data-ttu-id="9af3d-119">Mindst én af linjerne skal vise den primære leverandør, hvis der var en i produktposten.</span><span class="sxs-lookup"><span data-stu-id="9af3d-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="9af3d-120">Hvis du tidligere har noteret kreditornummeret ned, kan du vælge det her.</span><span class="sxs-lookup"><span data-stu-id="9af3d-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="9af3d-121">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="9af3d-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9af3d-122">Vælg en dato, der ligger et par måneder frem.</span><span class="sxs-lookup"><span data-stu-id="9af3d-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="9af3d-123">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9af3d-123">Click Add.</span></span>
11. <span data-ttu-id="9af3d-124">Indtast eller vælg en værdi i feltet Kreditor.</span><span class="sxs-lookup"><span data-stu-id="9af3d-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="9af3d-125">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="9af3d-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9af3d-126">Vælg en dato, der er forskellig fra den forrige udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="9af3d-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="9af3d-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-127">Close the page.</span></span>
14. <span data-ttu-id="9af3d-128">Klik på Godkendte kreditorer.</span><span class="sxs-lookup"><span data-stu-id="9af3d-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="9af3d-129">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="9af3d-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9af3d-130">Denne dato fungerer som et filter, så du kan se, hvem de godkendte leverandører er frem til en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="9af3d-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="9af3d-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-131">Close the page.</span></span>
17. <span data-ttu-id="9af3d-132">Klik på Gyldighedsperiode.</span><span class="sxs-lookup"><span data-stu-id="9af3d-132">Click Effective period.</span></span>
18. <span data-ttu-id="9af3d-133">Angiv en dato i feltet Vis kreditorer, der er udløbet efter.</span><span class="sxs-lookup"><span data-stu-id="9af3d-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="9af3d-134">Du kan bruge denne side til at identificere kreditorer, hvor godkendelsesstatussen udløber efter en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="9af3d-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="9af3d-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-135">Close the page.</span></span>
20. <span data-ttu-id="9af3d-136">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="9af3d-136">Click Edit.</span></span>
21. <span data-ttu-id="9af3d-137">Vælg en indstilling i metodefeltet Godkendt kontrolmetode for kreditorer.</span><span class="sxs-lookup"><span data-stu-id="9af3d-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="9af3d-138">I dette felt kan du vælge politikken for, hvad der skal ske, hvis produktet er føjet til en indkøbsordrelinje, hvor kreditoren ikke er en godkendt kreditor.</span><span class="sxs-lookup"><span data-stu-id="9af3d-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="9af3d-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9af3d-139">Click Save.</span></span>
23. <span data-ttu-id="9af3d-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-140">Close the page.</span></span>
24. <span data-ttu-id="9af3d-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-141">Close the page.</span></span>
25. <span data-ttu-id="9af3d-142">Gå til Indkøb og forsyning > Kreditorer > Kreditor/varerelationer > Godkendt kreditorliste efter vare.</span><span class="sxs-lookup"><span data-stu-id="9af3d-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="9af3d-143">Denne side giver dig en oversigt over alle produkter og godkendte kreditorer.</span><span class="sxs-lookup"><span data-stu-id="9af3d-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="9af3d-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-144">Close the page.</span></span>
27. <span data-ttu-id="9af3d-145">Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="9af3d-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="9af3d-146">Du kan også starte fra en kreditor og derefter gå til listen over godkendte produkter for den pågældende kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="9af3d-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="9af3d-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9af3d-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="9af3d-148">Klik på fanen Indkøb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="9af3d-149">Klik på Godkendt kreditorliste efter kreditor.</span><span class="sxs-lookup"><span data-stu-id="9af3d-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="9af3d-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-150">Close the page.</span></span>
32. <span data-ttu-id="9af3d-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9af3d-151">Close the page.</span></span>


