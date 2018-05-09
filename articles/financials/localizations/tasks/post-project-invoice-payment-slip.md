--- 
title: "Bogføre en projektfaktura med et indbetalingskort (Danmark)"
description: "Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 209ebbe8952d6df2729a558c1d54d85ca7c46684
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="post-a-project-invoice-with-a-payment-slip-denmark"></a><span data-ttu-id="ba7d9-103">Bogføre en projektfaktura med et indbetalingskort (Danmark)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-103">Post a project invoice with a payment slip (Denmark)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba7d9-104">Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-104">You can post a free text invoice with a payment slip attachment in a specified format.</span></span> <span data-ttu-id="ba7d9-105">Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-105">The payment slip is printed with the creditor identification number and invoice number to identify the payment.</span></span>

<span data-ttu-id="ba7d9-106">Før du kan udføre denne procedure, skal du først oprette et indbetalingskortformat og oprette indbetalingskort til kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-106">Before you can complete this procedure, you must first set up a payment slip format and set up payment slips for customer invoices.</span></span> 



<span data-ttu-id="ba7d9-107">Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-107">This functionality is available for legal entities whose primary address is in Denmark.</span></span> 

<span data-ttu-id="ba7d9-108">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-108">This procedure was created using the demo data company DEMF.</span></span>

1. <span data-ttu-id="ba7d9-109">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="ba7d9-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ba7d9-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ba7d9-112">Vis eller skjul sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-112">Expand or collapse the Invoice and delivery section.</span></span>
5. <span data-ttu-id="ba7d9-113">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-113">Click Edit.</span></span>
6. <span data-ttu-id="ba7d9-114">I feltet På en projektfaktura skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-114">In the On a project invoice field, select an option.</span></span>
    * <span data-ttu-id="ba7d9-115">o Ingen – Udskriv ikke et indbetalingskort.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-115">o None – Do not print a payment slip.</span></span> <span data-ttu-id="ba7d9-116">Vælg denne indstilling, hvis indbetalingsbeløbet er i en anden valuta end danske kroner (DKK).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-116">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="ba7d9-117">o FIK 751 – Udskriv et FIK 751-indbetalingskort, hvis du har tænkt dig at skrive betalingsbeløbet og forfaldsdatoen på indbetalingskortet i hånden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-117">o   FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="ba7d9-118">o FIK 752 – Udskriv et FIK 752-indbetalingskort, hvis du har tænkt dig at bruge et computergenereret indbetalingskort, hvor betalingsbeløb og forfaldsdato er fortrykt.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-118">o    FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>     
7. <span data-ttu-id="ba7d9-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-119">Click Save.</span></span>
8. <span data-ttu-id="ba7d9-120">Klik på fanen TabPageGrid.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-120">Click the TabPageGrid tab.</span></span>
9. <span data-ttu-id="ba7d9-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-121">Close the page.</span></span>
10. <span data-ttu-id="ba7d9-122">Gå til Projektstyring og regnskab > Projekter > Projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-122">Go to Project management and accounting > Projects > Project contracts.</span></span>
11. <span data-ttu-id="ba7d9-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-123">Click New.</span></span>
12. <span data-ttu-id="ba7d9-124">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="ba7d9-125">Klik på rullelisten i feltet Finansieringskilde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-125">In the Funding source field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ba7d9-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-126">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="ba7d9-127">Klik på rullelisten i feltet Salgsvaluta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-127">In the Sales currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="ba7d9-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-128">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ba7d9-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-129">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ba7d9-130">Klik på rullelisten i feltet Salgsvaluta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-130">In the Sales currency field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ba7d9-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ba7d9-132">Indbetalingskortet kan kun udskrives for en projektfaktura med valutaen danske kroner (DKK).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-132">The payment slip can be printed only for a project invoice with the currency Danish kroner (DKK).</span></span>  
20. <span data-ttu-id="ba7d9-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-133">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="ba7d9-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-134">Click OK.</span></span>
22. <span data-ttu-id="ba7d9-135">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-135">Click Save.</span></span>
23. <span data-ttu-id="ba7d9-136">Gå til Projektstyring og regnskab > Projekter > Alle projekter.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-136">Go to Project management and accounting > Projects > All projects.</span></span>
24. <span data-ttu-id="ba7d9-137">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-137">Click New.</span></span>
25. <span data-ttu-id="ba7d9-138">Vælg en indstilling i feltet Projekttype.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-138">In the Project type field, select an option.</span></span>
26. <span data-ttu-id="ba7d9-139">Skriv en værdi i feltet Projektnavn.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-139">In the Project name field, type a value.</span></span>
27. <span data-ttu-id="ba7d9-140">Klik på rullelisten i feltet Projektgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-140">In the Project group field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="ba7d9-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-141">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="ba7d9-142">Klik på rullelisten i feltet Projektkontrakt-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-142">In the Project contract ID field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="ba7d9-143">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-143">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="ba7d9-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-144">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="ba7d9-145">Klik på Opret projekt.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-145">Click Create project.</span></span>
33. <span data-ttu-id="ba7d9-146">Klik på Projekt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-146">On the Action Pane, click Project.</span></span>
34. <span data-ttu-id="ba7d9-147">Klik på Projektstadie.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-147">Click Project stage.</span></span>
35. <span data-ttu-id="ba7d9-148">Klik på Under behandling.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-148">Click In process.</span></span>
36. <span data-ttu-id="ba7d9-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-149">Click OK.</span></span>
37. <span data-ttu-id="ba7d9-150">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-150">Click Save.</span></span>
38. <span data-ttu-id="ba7d9-151">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-151">On the Action Pane, click Manage.</span></span>
39. <span data-ttu-id="ba7d9-152">Klik på Acontotransaktioner.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-152">Click On-account transactions.</span></span>
40. <span data-ttu-id="ba7d9-153">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-153">Click New.</span></span>
41. <span data-ttu-id="ba7d9-154">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-154">In the list, mark the selected row.</span></span>
42. <span data-ttu-id="ba7d9-155">Angiv et tal i feltet Salgspris.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-155">In the Sales price field, enter a number.</span></span>
43. <span data-ttu-id="ba7d9-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-156">Click Save.</span></span>
44. <span data-ttu-id="ba7d9-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-157">Close the page.</span></span>
45. <span data-ttu-id="ba7d9-158">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-158">On the Action Pane, click Manage.</span></span>
46. <span data-ttu-id="ba7d9-159">Klik på Projektfakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-159">Click Project invoice proposals.</span></span>
47. <span data-ttu-id="ba7d9-160">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-160">Click New.</span></span>
48. <span data-ttu-id="ba7d9-161">Klik på Fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-161">Click Invoice proposal.</span></span>
49. <span data-ttu-id="ba7d9-162">Klik på rullelisten i feltet Projekt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-162">In the Project field, click the drop-down button to open the lookup.</span></span>
50. <span data-ttu-id="ba7d9-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-163">Close the page.</span></span>
51. <span data-ttu-id="ba7d9-164">Klik på rullelisten i feltet Projektkontrakt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-164">In the Project contract field, click the drop-down button to open the lookup.</span></span>
52. <span data-ttu-id="ba7d9-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-165">In the list, find and select the desired record.</span></span>
53. <span data-ttu-id="ba7d9-166">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-166">In the list, click the link in the selected row.</span></span>
54. <span data-ttu-id="ba7d9-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-167">Click OK.</span></span>
55. <span data-ttu-id="ba7d9-168">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-168">Click Post.</span></span>
56. <span data-ttu-id="ba7d9-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-169">Click OK.</span></span>
57. <span data-ttu-id="ba7d9-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-170">Click OK.</span></span>


