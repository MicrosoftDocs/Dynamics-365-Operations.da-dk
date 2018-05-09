--- 
title: "Oprette en købsaftræksordre ved oprettelse af indkøbsordren"
description: "Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2a5fde13fac7f0523c098f750d897ca5da06473b
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="61a09-103">Oprette en købsaftræksordre ved oprettelse af indkøbsordren</span><span class="sxs-lookup"><span data-stu-id="61a09-103">Create a purchase release order when creating the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61a09-104">Denne fremgangsmåde viser, hvordan du bruger en købsaftale, når du opretter en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="61a09-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="61a09-105">Købsaftalen skal anvendes, når du opretter indkøbsordren, fordi der er generelle betingelser, der skal kopieres til indkøbsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="61a09-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="61a09-106">Denne opgave vil typisk blive foretaget af en indkøber.</span><span class="sxs-lookup"><span data-stu-id="61a09-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="61a09-107">Du skal have en gyldig købsaftale med et tilsagn om produktantal for en kreditor og varer som en forudsætning for denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="61a09-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="61a09-108">Samme fremgangsmåde kan bruges, hvis du har en købsaftale med andre typer forpligtelser.</span><span class="sxs-lookup"><span data-stu-id="61a09-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="61a09-109">Du kan køre denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="61a09-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="61a09-110">Hvis du bruger USMF, kan du køre guiden "Opret en købsaftale" først for at konfigurere de nødvendige forudsætninger for denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="61a09-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="61a09-111">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="61a09-111">Create a purchase order</span></span>
1. <span data-ttu-id="61a09-112">Åbn arbejdsområdet til klargøring af indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="61a09-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="61a09-113">Klik på Ny indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="61a09-113">Click New purchase order.</span></span>
3. <span data-ttu-id="61a09-114">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="61a09-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="61a09-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="61a09-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="61a09-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="61a09-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="61a09-117">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="61a09-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="61a09-118">Klik på rullelisten i feltet Købsaftale for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="61a09-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="61a09-119">Alle aftaler, der er tilgængelige for kreditoren, er anført her.</span><span class="sxs-lookup"><span data-stu-id="61a09-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="61a09-120">Find den gældende aftale, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="61a09-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="61a09-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="61a09-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="61a09-122">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="61a09-122">Click Yes.</span></span>
10. <span data-ttu-id="61a09-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="61a09-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="61a09-124">Tilføj en linje</span><span class="sxs-lookup"><span data-stu-id="61a09-124">Add a line</span></span>
1. <span data-ttu-id="61a09-125">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="61a09-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="61a09-126">Hvis der er bestemte lager- eller lokalitetsdimensioner på tilsagnet, skal du angive de samme værdier på indkøbsordrelinjen for at gøre brug af aftalen.</span><span class="sxs-lookup"><span data-stu-id="61a09-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="61a09-127">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="61a09-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="61a09-128">Stedet er muligvis allerede udfyldt med standardværdien fra ordren eller fra kreditoren.</span><span class="sxs-lookup"><span data-stu-id="61a09-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="61a09-129">Hvis det er tilfældet, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="61a09-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="61a09-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="61a09-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="61a09-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="61a09-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="61a09-132">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="61a09-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="61a09-133">Kontrollér, at prisen er kopieret fra tilsagnet.</span><span class="sxs-lookup"><span data-stu-id="61a09-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="61a09-134">Slå tilsagnet op</span><span class="sxs-lookup"><span data-stu-id="61a09-134">Look up the commitment</span></span>
1. <span data-ttu-id="61a09-135">Klik på Opdater linje.</span><span class="sxs-lookup"><span data-stu-id="61a09-135">Click Update line.</span></span>
2. <span data-ttu-id="61a09-136">Klik på Vedhæftet.</span><span class="sxs-lookup"><span data-stu-id="61a09-136">Click Attached.</span></span>
    * <span data-ttu-id="61a09-137">Her kan du få oplysninger om for købsaftalen.</span><span class="sxs-lookup"><span data-stu-id="61a09-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="61a09-138">For eksempel kan du se prisen og om pris og rabat er fast, hvilket betyder, at hvis du ændrer pris eller rabat på indkøbsordren til en anden værdi end på forpligtelsen, systemet vil fjerne linket, så indkøbsordrelinjen ikke opfylde forpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="61a09-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="61a09-139">Du kan også se hvis Maks gennemtvinges indstilling er markeret, hvilket betyder, at antallet på forpligtelsen, der ikke kan overskrides ved at sammenlægge alle de køb, der skal opfylde forpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="61a09-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="61a09-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="61a09-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="61a09-141">Slå købsaftalen op</span><span class="sxs-lookup"><span data-stu-id="61a09-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="61a09-142">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="61a09-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="61a09-143">Klik på Indkøbsaftale.</span><span class="sxs-lookup"><span data-stu-id="61a09-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="61a09-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="61a09-144">Close the page.</span></span>
4. <span data-ttu-id="61a09-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="61a09-145">Close the page.</span></span>


