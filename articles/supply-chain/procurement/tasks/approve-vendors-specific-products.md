---
title: Godkende kreditorer til specifikke produkter
description: Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383268"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="878f1-103">Godkende kreditorer til specifikke produkter</span><span class="sxs-lookup"><span data-stu-id="878f1-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="878f1-104">Denne fremgangsmåde viser, hvordan du godkender kreditorer for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="878f1-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="878f1-105">Dette gør det muligt at styre, hvilke kreditorer der kan bruges, når produktet føjes til en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="878f1-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="878f1-106">Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="878f1-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="878f1-107">Denne opgave vil typisk blive udført af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="878f1-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="878f1-108">I navigationsruden skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="878f1-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="878f1-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="878f1-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="878f1-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="878f1-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="878f1-111">Udvid oversigtspanelet **Indkøb**.</span><span class="sxs-lookup"><span data-stu-id="878f1-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="878f1-112">Hvis der ingen primær kreditor vises i feltet **Kreditor**, skal du tilføje denne kreditor som en godkendt kreditor med følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="878f1-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="878f1-113">Noter kreditornummeret ned, hvis der vises et.</span><span class="sxs-lookup"><span data-stu-id="878f1-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="878f1-114">Klik på **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="878f1-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="878f1-115">Klik på **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="878f1-115">Click **Setup**.</span></span>
7. <span data-ttu-id="878f1-116">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="878f1-116">Click **Add**.</span></span>
8. <span data-ttu-id="878f1-117">Indtast eller vælg en værdi i feltet Kreditor.</span><span class="sxs-lookup"><span data-stu-id="878f1-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="878f1-118">Vælg den godkendte kreditor.</span><span class="sxs-lookup"><span data-stu-id="878f1-118">Select the approved vendor.</span></span> <span data-ttu-id="878f1-119">Mindst én af linjerne skal vise den primære leverandør, hvis der var en i produktposten.</span><span class="sxs-lookup"><span data-stu-id="878f1-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="878f1-120">Hvis du tidligere har noteret kreditornummeret ned, kan du vælge det her.</span><span class="sxs-lookup"><span data-stu-id="878f1-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="878f1-121">Angiv en dato i feltet **Udløb**.</span><span class="sxs-lookup"><span data-stu-id="878f1-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="878f1-122">Vælg en dato, der ligger et par måneder frem.</span><span class="sxs-lookup"><span data-stu-id="878f1-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="878f1-123">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="878f1-123">Click **Add**.</span></span>
11. <span data-ttu-id="878f1-124">Indtast eller vælg en værdi i feltet **Kreditor**.</span><span class="sxs-lookup"><span data-stu-id="878f1-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="878f1-125">Angiv en dato i feltet **Udløb**.</span><span class="sxs-lookup"><span data-stu-id="878f1-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="878f1-126">Vælg en dato, der er forskellig fra den forrige udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="878f1-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="878f1-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-127">Close the page.</span></span>
14. <span data-ttu-id="878f1-128">Klik på **Godkendte kreditorer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="878f1-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="878f1-129">Angiv en dato i feltet **Udløb**.</span><span class="sxs-lookup"><span data-stu-id="878f1-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="878f1-130">Denne dato fungerer som et filter, så du kan se, hvem de godkendte leverandører er frem til en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="878f1-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="878f1-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-131">Close the page.</span></span>
17. <span data-ttu-id="878f1-132">Klik på **Gyldighedsperiode** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="878f1-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="878f1-133">Angiv en dato i feltet **Vis kreditorer, der er udløbet efter**.</span><span class="sxs-lookup"><span data-stu-id="878f1-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="878f1-134">Du kan bruge denne side til at identificere kreditorer, hvor godkendelsesstatussen udløber efter en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="878f1-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="878f1-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-135">Close the page.</span></span>
20. <span data-ttu-id="878f1-136">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="878f1-136">Click **Edit**.</span></span>
21. <span data-ttu-id="878f1-137">Vælg en indstilling i feltet **Godkendt kontrolmetode for kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="878f1-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="878f1-138">I dette felt kan du vælge politikken for, hvad der skal ske, hvis produktet er føjet til en indkøbsordrelinje, hvor kreditoren ikke er en godkendt kreditor.</span><span class="sxs-lookup"><span data-stu-id="878f1-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="878f1-139">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="878f1-139">Click **Save**.</span></span>
23. <span data-ttu-id="878f1-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-140">Close the page.</span></span>
24. <span data-ttu-id="878f1-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-141">Close the page.</span></span>
25. <span data-ttu-id="878f1-142">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Leverandør-/varerelationer > Godkendt kreditorliste efter vare**.</span><span class="sxs-lookup"><span data-stu-id="878f1-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="878f1-143">Denne side giver dig en oversigt over alle produkter og godkendte kreditorer.</span><span class="sxs-lookup"><span data-stu-id="878f1-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="878f1-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-144">Close the page.</span></span>
27. <span data-ttu-id="878f1-145">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="878f1-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="878f1-146">Du kan også starte fra en kreditor og derefter gå til listen over godkendte produkter for den pågældende kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="878f1-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="878f1-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="878f1-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="878f1-148">Klik på fanen **Indkøb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="878f1-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="878f1-149">Klik på **Godkendt kreditorliste efter kreditor**.</span><span class="sxs-lookup"><span data-stu-id="878f1-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="878f1-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-150">Close the page.</span></span>
32. <span data-ttu-id="878f1-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="878f1-151">Close the page.</span></span>

