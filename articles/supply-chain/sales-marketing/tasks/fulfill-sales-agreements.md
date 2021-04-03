---
title: Opfylde salgsaftaler
description: Denne procedure viser, hvordan du opfylder en salgsaftale ved at knytte salgsordrer til den.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31c86ae556789ecf04dc303ddd9510458c1f6d01
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260377"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="11008-103">Opfylde salgsaftaler</span><span class="sxs-lookup"><span data-stu-id="11008-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11008-104">Denne procedure viser, hvordan du opfylder en salgsaftale ved at knytte salgsordrer til den.</span><span class="sxs-lookup"><span data-stu-id="11008-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="11008-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="11008-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="11008-106">Kontroller, at du har en gyldig salgsaftale af typen "Produkt værdi forpligtelse", før du starter denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="11008-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="11008-107">Du kan også køre opgaveguiden "Oprette salgsaftaler".</span><span class="sxs-lookup"><span data-stu-id="11008-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="11008-108">Frigive en salgsordre fra aftalen</span><span class="sxs-lookup"><span data-stu-id="11008-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="11008-109">Gå til salg og marketing > Salgsaftaler > Salgsaftaler.</span><span class="sxs-lookup"><span data-stu-id="11008-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="11008-110">Åbn den aftale, du vil frigive ordren mode, på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="11008-111">Klik på Salgsaftale i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11008-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="11008-112">Klik på Aftræksordre.</span><span class="sxs-lookup"><span data-stu-id="11008-112">Click Release order.</span></span>
    * <span data-ttu-id="11008-113">Som teksten over på siden Opret aftræksordre påpeger, vil de oplysninger, der kræves til salgsordrelinjerne, variere afhængigt af, om aftalen er baseret på mængde eller værdi.</span><span class="sxs-lookup"><span data-stu-id="11008-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="11008-114">Aftalen i denne vejledning er af typen "Bundet produktværdi".</span><span class="sxs-lookup"><span data-stu-id="11008-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="11008-115">Det er derfor området Linjer på denne side er tomt.</span><span class="sxs-lookup"><span data-stu-id="11008-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="11008-116">Hvis tilsagnet var baseret på mængde, ville linjeoplysningerne blive kopieret fra aftalen.</span><span class="sxs-lookup"><span data-stu-id="11008-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="11008-117">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="11008-117">Click Create.</span></span>
    * <span data-ttu-id="11008-118">Meddelelsen fortæller dig, at en salgsordre er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="11008-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="11008-119">Da ordren ikke indeholder nogen linjer, skal du tilføje ordrelinjeoplysningerne for at fuldføre frigivelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="11008-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="11008-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-120">Close the page.</span></span>
7. <span data-ttu-id="11008-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-121">Close the page.</span></span>
8. <span data-ttu-id="11008-122">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="11008-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="11008-123">Find, og åbn den ordre, der blev oprettet som et resultat af ordrefrigivelsen i den forrige opgave, på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="11008-124">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="11008-124">Click Add line.</span></span>
11. <span data-ttu-id="11008-125">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="11008-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="11008-126">I feltet Varenummer skal du skrive eller vælge den vare, der er angivet på den tilknyttede salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="11008-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="11008-127">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="11008-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="11008-128">Sørg for at angive en mængde, der bringer nettobeløbet under værdien af den tilknyttede salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="11008-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="11008-129">Bemærk, at fordi salgsordren er knyttet til aftalen, anvendes den aftalte rabatprocent på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="11008-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="11008-130">Klik på Opdater linje.</span><span class="sxs-lookup"><span data-stu-id="11008-130">Click Update line.</span></span>
15. <span data-ttu-id="11008-131">Klik på Vedhæftet.</span><span class="sxs-lookup"><span data-stu-id="11008-131">Click Attached.</span></span>
    * <span data-ttu-id="11008-132">Siden Tilknyttet aftale viser id'et og vilkårene i aftalen, som linjen er frigivet fra.</span><span class="sxs-lookup"><span data-stu-id="11008-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="11008-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-133">Close the page.</span></span>
17. <span data-ttu-id="11008-134">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11008-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="11008-135">Klik på Tilknyttet salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="11008-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="11008-136">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="11008-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="11008-137">Klik på fanen Opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="11008-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="11008-138">Fanen Opfyldelse viser en oversigt over alle de salgsordrelinjer, der er knyttet til dette tilsagn, og deres opfyldelsestilstand, samt beløbet eller mængden, der endnu ikke er frigivet.</span><span class="sxs-lookup"><span data-stu-id="11008-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="11008-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-139">Close the page.</span></span>
22. <span data-ttu-id="11008-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-140">Close the page.</span></span>
23. <span data-ttu-id="11008-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="11008-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="11008-142">Anvende salgsaftale i bestillingsprocessen</span><span class="sxs-lookup"><span data-stu-id="11008-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="11008-143">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="11008-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="11008-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="11008-144">Click New.</span></span>
3. <span data-ttu-id="11008-145">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="11008-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="11008-146">Søg på listen, og vælg den kunde, der er angivet i salgsaftalen.</span><span class="sxs-lookup"><span data-stu-id="11008-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="11008-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="11008-148">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="11008-148">Expand the General section.</span></span>
7. <span data-ttu-id="11008-149">Klik på rullelisten i feltet Salgsaftale-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="11008-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="11008-150">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="11008-151">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="11008-151">Click Yes.</span></span>
10. <span data-ttu-id="11008-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="11008-152">Click OK.</span></span>
11. <span data-ttu-id="11008-153">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="11008-154">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="11008-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="11008-155">I feltet Varenummer skal du skrive eller vælge den vare, der er angivet på den tilknyttede salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="11008-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="11008-156">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="11008-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="11008-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="11008-157">Click Save.</span></span>
16. <span data-ttu-id="11008-158">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11008-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="11008-159">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="11008-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="11008-160">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="11008-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="11008-161">Vælg Ja i feltet Bogføring.</span><span class="sxs-lookup"><span data-stu-id="11008-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="11008-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="11008-162">Click OK.</span></span>
21. <span data-ttu-id="11008-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="11008-163">Click OK.</span></span>
22. <span data-ttu-id="11008-164">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="11008-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="11008-165">Klik på Tilknyttet salgsaftale.</span><span class="sxs-lookup"><span data-stu-id="11008-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="11008-166">Klik på fanen Opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="11008-166">Click the Fulfillment tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]