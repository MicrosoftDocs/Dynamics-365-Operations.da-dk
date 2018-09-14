--- 
title: Oprette og redigere salgstilbud
description: Denne procedure viser, hvordan du opretter og opdaterer et salgstilbud.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="1393b-103">Oprette og redigere salgstilbud</span><span class="sxs-lookup"><span data-stu-id="1393b-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1393b-104">Denne procedure viser, hvordan du opretter og opdaterer et salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="1393b-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="1393b-105">Du kan køre procedure på dine egne data eller i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="1393b-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="1393b-106">Oprette et salgstilbud</span><span class="sxs-lookup"><span data-stu-id="1393b-106">Create a sales quotation</span></span>
1. <span data-ttu-id="1393b-107">Gå til Salg og marketing > Salgstilbud > Alle tilbud.</span><span class="sxs-lookup"><span data-stu-id="1393b-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="1393b-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="1393b-108">Click New.</span></span>
3. <span data-ttu-id="1393b-109">Vælg Kundeemne i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="1393b-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="1393b-110">Indtast eller vælg en værdi i feltet Kundeemne.</span><span class="sxs-lookup"><span data-stu-id="1393b-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="1393b-111">Udvid sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="1393b-111">Expand the General section.</span></span>
    * <span data-ttu-id="1393b-112">Typen indstilles automatisk til Salgstilbud, fordi du har valgt at oprette et tilbud fra området Salg og marketing.</span><span class="sxs-lookup"><span data-stu-id="1393b-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="1393b-113">Hvis du vil oprette et tilbud for et projekt, kan du åbne det i modulet Projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="1393b-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="1393b-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1393b-114">Click OK.</span></span>
    * <span data-ttu-id="1393b-115">Felter og handlinger på tilbudslinjerne er meget lig dem på salgsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="1393b-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="1393b-116">Som salgsordrer, kan der oprettes tilbud for en bestemt vare, eller når varenummer ikke er kendt eller ikke findes på tidspunktet for oprettelse af tilbud, kan der oprettes tilbud for en salgskategori.</span><span class="sxs-lookup"><span data-stu-id="1393b-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="1393b-117">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="1393b-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="1393b-118">Skriv en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="1393b-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="1393b-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-119">Close the page.</span></span>
10. <span data-ttu-id="1393b-120">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="1393b-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1393b-121">Hvis der er gyldige samhandelsaftaler for varen, der er valgt på linjen, kopieres gældende priser og rabatter automatisk til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="1393b-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="1393b-122">Kontroller, at feltet Enhedspris indeholder en værdi, og du kan også angive værdier for rabat, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="1393b-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="1393b-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="1393b-123">Click Save.</span></span>
12. <span data-ttu-id="1393b-124">Klik på Salgstilbud i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1393b-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="1393b-125">Klik på Totaler.</span><span class="sxs-lookup"><span data-stu-id="1393b-125">Click Totals.</span></span>
14. <span data-ttu-id="1393b-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1393b-126">Click OK.</span></span>
15. <span data-ttu-id="1393b-127">Klik på Salgstilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="1393b-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="1393b-128">Klik på Priser.</span><span class="sxs-lookup"><span data-stu-id="1393b-128">Click Prices.</span></span>
    * <span data-ttu-id="1393b-129">På siden Kør prissimulering kan du eksperimentere med at justere forventet omsætning eller rentabilitet for dit tilbud baseret på den ønskede enhedspris, rabatbeløb, rabatprocent, samlet beløb, margen eller dækningsgrad.</span><span class="sxs-lookup"><span data-stu-id="1393b-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="1393b-130">Når du er tilfreds med måltallene, anvender du forslaget på tilbudslinjen; så opdateres dens prisrelaterede felter tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="1393b-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="1393b-131">Du kan oprette så mange prissimuleringer, som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="1393b-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="1393b-132">Når du klikker på Ny, kopieres prisbetingelserne fra den aktuelle tilbudslinje til siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="1393b-133">Du kan derefter ændre værdierne i ethvert af de prisrelaterede felter til målværdierne.</span><span class="sxs-lookup"><span data-stu-id="1393b-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="1393b-134">En ændring i et af felterne udløser genberegning i alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="1393b-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="1393b-135">Produktets enhedsomkostning skal være kendt, for at systemet kan beregne salgsmargen og dækningsgrad.</span><span class="sxs-lookup"><span data-stu-id="1393b-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="1393b-136">Brug fanen Simulerede priser for at se en detaljeret visning af de oprindelige priser, foreslåede ændringer og deres indvirkning på de samlede tilbudsbeløb.</span><span class="sxs-lookup"><span data-stu-id="1393b-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="1393b-137">Som hovedregel, når der anvendes en simulering, der angiver et nyt beløb på tilbudslinjen, genberegner og angiver systemet en ny værdi i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="1393b-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="1393b-138">Hvis simuleringen er baseret på en ny margen eller en ny dækningsgrad, opdateres kun feltet Nettobeløb, og Enhedspris er tomt.</span><span class="sxs-lookup"><span data-stu-id="1393b-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="1393b-139">I begge tilfælde slettes eventuelle rabatter, der var på tilbudslinjen før simulering.</span><span class="sxs-lookup"><span data-stu-id="1393b-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="1393b-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-140">Close the page.</span></span>
18. <span data-ttu-id="1393b-141">Klik på Tilbud i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1393b-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="1393b-142">Klik på Send tilbud.</span><span class="sxs-lookup"><span data-stu-id="1393b-142">Click Send quotation.</span></span>
20. <span data-ttu-id="1393b-143">Vælg Ja i feltet Udskriv tilbud.</span><span class="sxs-lookup"><span data-stu-id="1393b-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="1393b-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1393b-144">Click OK.</span></span>
    * <span data-ttu-id="1393b-145">Rapporten kan tage et minut at generere.</span><span class="sxs-lookup"><span data-stu-id="1393b-145">The report may take a minute to generate.</span></span> <span data-ttu-id="1393b-146">Luk ikke siden, før den er færdig.</span><span class="sxs-lookup"><span data-stu-id="1393b-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="1393b-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="1393b-148">Opdatere et salgstilbud</span><span class="sxs-lookup"><span data-stu-id="1393b-148">Update a sales quotation</span></span>
1. <span data-ttu-id="1393b-149">Klik på Opfølgning i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1393b-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="1393b-150">Klik på Konverter til kunde.</span><span class="sxs-lookup"><span data-stu-id="1393b-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="1393b-151">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="1393b-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="1393b-152">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="1393b-152">Click Check.</span></span>
    * <span data-ttu-id="1393b-153">Kontroller, at der vises en meddelelse om, at det kontonummer, du har skrevet, kan benyttes.</span><span class="sxs-lookup"><span data-stu-id="1393b-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="1393b-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1393b-154">Click OK.</span></span>
    * <span data-ttu-id="1393b-155">Systemet er nu oprettet en ny debitorkonto for kundeemnet i tilbuddet.</span><span class="sxs-lookup"><span data-stu-id="1393b-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="1393b-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-156">Close the page.</span></span>
7. <span data-ttu-id="1393b-157">Klik på Opfølgning i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1393b-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="1393b-158">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="1393b-158">Click Confirm.</span></span>
9. <span data-ttu-id="1393b-159">Indtast eller vælg en værdi i feltet Årsag.</span><span class="sxs-lookup"><span data-stu-id="1393b-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="1393b-160">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1393b-160">Click OK.</span></span>
11. <span data-ttu-id="1393b-161">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1393b-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="1393b-162">Klik på Salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="1393b-162">Click Sales orders.</span></span>
13. <span data-ttu-id="1393b-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1393b-163">Close the page.</span></span>


