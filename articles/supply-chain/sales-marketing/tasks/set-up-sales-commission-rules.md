--- 
title: Konfigurere salgsprovisionsregler
description: Denne procedure viser, hvordan du kan konfigurere og aktivere beregning og sporing af salgsprovision.
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7b2d44b8ee6751516621cbb11148c9a92bdf427a
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="c75d5-103">Konfigurere salgsprovisionsregler</span><span class="sxs-lookup"><span data-stu-id="c75d5-103">Set up sales commission rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c75d5-104">Denne procedure viser, hvordan du kan konfigurere og aktivere beregning og sporing af salgsprovision.</span><span class="sxs-lookup"><span data-stu-id="c75d5-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="c75d5-105">Proceduren viser, hvordan du kan oprette både debitor- og vareprovisionsgrupper, og hvordan du derefter sammenkæder en valgt kunde og et produkt til de respektive grupper.</span><span class="sxs-lookup"><span data-stu-id="c75d5-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="c75d5-106">Disse grupper bruges derefter i opsætningen af provisionsberegningen til at oprette en debitor-, vare- og sælgerkombination, der skal matches af en salgsordre for at berettige sælgerne til en provision.</span><span class="sxs-lookup"><span data-stu-id="c75d5-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="c75d5-107">Oprettelse af debitor- og vareprovisionsgrupper er valgfri, da beregningen af provisionen også kan udføres for en individuel debitor og/eller vare.</span><span class="sxs-lookup"><span data-stu-id="c75d5-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="c75d5-108">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c75d5-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="c75d5-109">Konfigurer provisionsgrupper og provisionssatser</span><span class="sxs-lookup"><span data-stu-id="c75d5-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="c75d5-110">Gå til Salg og marketing > Provisioner > Provisionskundegrupper.</span><span class="sxs-lookup"><span data-stu-id="c75d5-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="c75d5-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c75d5-111">Click New.</span></span>
3. <span data-ttu-id="c75d5-112">Skriv en værdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="c75d5-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c75d5-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c75d5-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c75d5-114">Click Save.</span></span>
6. <span data-ttu-id="c75d5-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c75d5-115">Close the page.</span></span>
7. <span data-ttu-id="c75d5-116">Gå til Salg og marketing > Provisioner > Varegrupper.</span><span class="sxs-lookup"><span data-stu-id="c75d5-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="c75d5-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c75d5-117">Click New.</span></span>
9. <span data-ttu-id="c75d5-118">Skriv en værdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="c75d5-119">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c75d5-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="c75d5-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c75d5-120">Close the page.</span></span>
12. <span data-ttu-id="c75d5-121">Gå til Salg og marketing > Provisioner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="c75d5-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="c75d5-122">En provisionssalgsgruppe angiver medarbejderne i sælgerroller, der er berettiget til at modtage en provision, når en kunde, der er knyttet til den relevante salgsgruppe, køber visse varer.</span><span class="sxs-lookup"><span data-stu-id="c75d5-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="c75d5-123">I USMF-demodatafirmaet, er der en salgsgruppe, der kaldes "Sælgere USA".</span><span class="sxs-lookup"><span data-stu-id="c75d5-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="c75d5-124">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c75d5-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="c75d5-125">Klik på Sælger.</span><span class="sxs-lookup"><span data-stu-id="c75d5-125">Click Sales rep.</span></span>
    * <span data-ttu-id="c75d5-126">Siden salg sælger viser en oversigt over virksomhedens sælgere, der er knyttet til en bestemt Kommissionen gruppe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="c75d5-127">Du kan tildele flere sælgere til den samme gruppe og definere deres respektive andel af den samlede provision gebyr som en procentværdi.</span><span class="sxs-lookup"><span data-stu-id="c75d5-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="c75d5-128">Den samlede provision andel på tværs af alle medarbejdere må ikke overstige 100.</span><span class="sxs-lookup"><span data-stu-id="c75d5-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="c75d5-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="c75d5-130">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="c75d5-130">Click Edit.</span></span>
17. <span data-ttu-id="c75d5-131">Indstil Provisionsandel til "50".</span><span class="sxs-lookup"><span data-stu-id="c75d5-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="c75d5-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c75d5-132">Click New.</span></span>
19. <span data-ttu-id="c75d5-133">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="c75d5-134">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="c75d5-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c75d5-135">For eksempel kan du filtrere på feltet Navn med værdien "Susan Burk".</span><span class="sxs-lookup"><span data-stu-id="c75d5-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="c75d5-136">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="c75d5-136">Click Select.</span></span>
22. <span data-ttu-id="c75d5-137">Indstil Provisionsandel til "50".</span><span class="sxs-lookup"><span data-stu-id="c75d5-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="c75d5-138">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c75d5-138">Click Save.</span></span>
24. <span data-ttu-id="c75d5-139">Gå til Salg og marketing > Provisioner > Provisionsberegning.</span><span class="sxs-lookup"><span data-stu-id="c75d5-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="c75d5-140">På siden Provisionsberegning kan du definere den provisionssats, medarbejderen skal modtage for en salgspostering, når den indeholder den forudindstillede kombination af kunde og produkt.</span><span class="sxs-lookup"><span data-stu-id="c75d5-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="c75d5-141">Som en del af provisionssatsopsætningen, skal du angive provisionsberegningsgrundlaget, og om det skal medtage eller udelukke rabatter.</span><span class="sxs-lookup"><span data-stu-id="c75d5-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="c75d5-142">Du kan også angive en gyldighedsperiode for, hvornår provisionssatsen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="c75d5-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="c75d5-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c75d5-143">Click New.</span></span>
26. <span data-ttu-id="c75d5-144">Vælg "Gruppe" i feltet Varekode:</span><span class="sxs-lookup"><span data-stu-id="c75d5-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="c75d5-145">Klik på rullelisten i feltet Varerelation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="c75d5-146">Find og vælg den gruppe, som du oprettede tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="c75d5-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c75d5-148">Vælg Gruppe i feltet Kundekode.</span><span class="sxs-lookup"><span data-stu-id="c75d5-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="c75d5-149">Klik på rullelisten i feltet Debitorrelation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="c75d5-150">Vælg den gruppe, som du konfigurerede tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="c75d5-151">I feltet Sælgerrelation skal du klikke på rullelisten for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="c75d5-152">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c75d5-153">Bevar indstillingen "Før linjerabat".</span><span class="sxs-lookup"><span data-stu-id="c75d5-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="c75d5-154">Bevar indstillingen "Omsætning" som grundlag for beregningen af provisionsværdien.</span><span class="sxs-lookup"><span data-stu-id="c75d5-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="c75d5-155">Angiv et tal i feltet Provisionssats i procent.</span><span class="sxs-lookup"><span data-stu-id="c75d5-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="c75d5-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c75d5-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="c75d5-157">Konfiguration af provisionskonteringer</span><span class="sxs-lookup"><span data-stu-id="c75d5-157">Setting up commission posting</span></span>
1. <span data-ttu-id="c75d5-158">Gå til Salg og marketing > Provisioner > Provisionskontering.</span><span class="sxs-lookup"><span data-stu-id="c75d5-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="c75d5-159">Provisionsgebyrer skal betales til medarbejderne og skal derfor sættes op til at sikre korrekt økonomisk bogføring på de relevante konti i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="c75d5-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="c75d5-160">Dette gøres på siden Provisionskontering.</span><span class="sxs-lookup"><span data-stu-id="c75d5-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="c75d5-161">Gennemse den opsætning, der er tilgængelig for det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="c75d5-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="c75d5-162">Normalt bogføres provisionsbeløbene på en dedikeret konto for udgifter og modposteres på en dedikeret kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="c75d5-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="c75d5-163">Hvis du ikke har konfigureret regler for provisionskonteringer, kan systemet ikke fuldføre fakturering af en salgsordre, der har berettiget provisioner.</span><span class="sxs-lookup"><span data-stu-id="c75d5-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="c75d5-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c75d5-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="c75d5-165">Tildel en provisionsgruppe til en kunde og et produkt</span><span class="sxs-lookup"><span data-stu-id="c75d5-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="c75d5-166">Gå til Salg og marketing > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="c75d5-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="c75d5-167">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c75d5-168">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c75d5-169">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="c75d5-169">Click Edit.</span></span>
5. <span data-ttu-id="c75d5-170">Udvid sektionen Salgsordrestandarder.</span><span class="sxs-lookup"><span data-stu-id="c75d5-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="c75d5-171">Klik på rullelisten i feltet Provisionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c75d5-172">Vælg den gruppe, som du oprettede tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="c75d5-173">Klik på rullelisten i feltet Salgsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c75d5-174">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c75d5-175">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c75d5-175">Click Save.</span></span>
11. <span data-ttu-id="c75d5-176">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="c75d5-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="c75d5-177">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="c75d5-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c75d5-178">Filtrer f.eks. efter feltet Varenummer med værdien "T0020".</span><span class="sxs-lookup"><span data-stu-id="c75d5-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="c75d5-179">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c75d5-180">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="c75d5-180">Click Edit.</span></span>
15. <span data-ttu-id="c75d5-181">Udvid afsnittet Sælg.</span><span class="sxs-lookup"><span data-stu-id="c75d5-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="c75d5-182">Klik på rullelisten i feltet Provisionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c75d5-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="c75d5-183">Find og vælg den provisionsgruppe, som du oprettede tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="c75d5-183">In the list, select the commission group that you created earlier.</span></span>


