---
title: EUR-00011 Generere EU-listesystemrapporten
description: Denne procedure fører dig gennem oprettelse af EU-salgslisterapporten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fcafa2beca5d998b2556ba73e9f3cc2bdd314ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564426"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="2665b-103">EUR-00011 Generere EU-listesystemrapporten</span><span class="sxs-lookup"><span data-stu-id="2665b-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2665b-104">Denne procedure fører dig gennem oprettelse af EU-salgslisterapporten.</span><span class="sxs-lookup"><span data-stu-id="2665b-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="2665b-105">Dette omfatter overførsel af samhandelstransaktioner inden for Fællesskabet til EU-listesystemet og procestiden for rapporten.</span><span class="sxs-lookup"><span data-stu-id="2665b-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="2665b-106">Denne procedure omfatter også oprettelse af en EU-samhandelstransaktion til demonstrationsformål.</span><span class="sxs-lookup"><span data-stu-id="2665b-106">This  procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="2665b-107">Du kan finde flere oplysninger om rapportering i EU-listesystemet, herunder de nødvendige forudsætninger, i Dynamics 365 for Finance and Operations Hjælp.</span><span class="sxs-lookup"><span data-stu-id="2665b-107">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="2665b-108">Denne procedure gælder for alle europæiske lande.</span><span class="sxs-lookup"><span data-stu-id="2665b-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="2665b-109">Proceduren er oprettet i demodatafirmaet DEMF, og dermed bruges Tyskland som et eksempel på indenlandsk land/område.</span><span class="sxs-lookup"><span data-stu-id="2665b-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="2665b-110">Proceduren bruger også Portugal som et eksempel EU-land/område.</span><span class="sxs-lookup"><span data-stu-id="2665b-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="2665b-111">Før du kan fuldføre denne procedure, skal du konfigurere rapportering i EU-listesystem.</span><span class="sxs-lookup"><span data-stu-id="2665b-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="2665b-112">Denne procedure er kun beregnet til bogholdere.</span><span class="sxs-lookup"><span data-stu-id="2665b-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="2665b-113">Oprette en EU-salgstransaktion til demonstrationsformål</span><span class="sxs-lookup"><span data-stu-id="2665b-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="2665b-114">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="2665b-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2665b-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2665b-115">Click New.</span></span>
3. <span data-ttu-id="2665b-116">Skriv "PRT-001" i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="2665b-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="2665b-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-117">Click OK.</span></span>
5. <span data-ttu-id="2665b-118">Skriv 'D0001' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="2665b-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="2665b-119">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="2665b-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="2665b-120">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="2665b-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="2665b-121">Skriv Fuld i feltet Varemomsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2665b-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="2665b-122">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="2665b-122">Click Add line.</span></span>
10. <span data-ttu-id="2665b-123">Skriv 'D0003' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="2665b-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="2665b-124">Skriv Rød i feltet Varemomsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2665b-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="2665b-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2665b-125">Click Save.</span></span>
13. <span data-ttu-id="2665b-126">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2665b-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="2665b-127">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="2665b-127">Click Invoice.</span></span>
15. <span data-ttu-id="2665b-128">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="2665b-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="2665b-129">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="2665b-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="2665b-130">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2665b-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="2665b-131">I feltet Fakturadato skal du indstille datoen til "01-11-2016".</span><span class="sxs-lookup"><span data-stu-id="2665b-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="2665b-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-132">Click OK.</span></span>
20. <span data-ttu-id="2665b-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="2665b-134">Overføre EU-samhandelstransaktioner til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="2665b-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="2665b-135">Gå til Skat > Erklæringer > Udenrigshandel > EU-listesystemet.</span><span class="sxs-lookup"><span data-stu-id="2665b-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="2665b-136">Klik på Overførsel.</span><span class="sxs-lookup"><span data-stu-id="2665b-136">Click Transfer.</span></span>
3. <span data-ttu-id="2665b-137">Vælg Ja i feltet Vare for at overføre vareposteringer.</span><span class="sxs-lookup"><span data-stu-id="2665b-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="2665b-138">Vælg Ja i feltet Ydelse for at overføre ydelsesposteringer.</span><span class="sxs-lookup"><span data-stu-id="2665b-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="2665b-139">Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, du vil overføre.</span><span class="sxs-lookup"><span data-stu-id="2665b-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="2665b-140">Klik på Overførsel.</span><span class="sxs-lookup"><span data-stu-id="2665b-140">Click Transfer.</span></span>
    * <span data-ttu-id="2665b-141">Kontroller, at salgstransaktionen inden for Fællesskabet er blevet overført til EU-listesystemet.</span><span class="sxs-lookup"><span data-stu-id="2665b-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="2665b-142">Generere rapport for EU-listesystem</span><span class="sxs-lookup"><span data-stu-id="2665b-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="2665b-143">Klik på Rapportering.</span><span class="sxs-lookup"><span data-stu-id="2665b-143">Click Reporting.</span></span>
2. <span data-ttu-id="2665b-144">I feltet Rapporteringsperiode skal du vælge Månedlig.</span><span class="sxs-lookup"><span data-stu-id="2665b-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="2665b-145">I feltet Fra dato skal du indstille datoen til "01-01-2016".</span><span class="sxs-lookup"><span data-stu-id="2665b-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="2665b-146">Vælg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="2665b-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="2665b-147">Vælg Ja i feltet Generer rapport.</span><span class="sxs-lookup"><span data-stu-id="2665b-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="2665b-148">Skriv "EUSalesList" i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="2665b-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="2665b-149">Skriv "EUSalesList" i feltet Rapportfilnavn.</span><span class="sxs-lookup"><span data-stu-id="2665b-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="2665b-150">Skriv "123" i feltet Registrerings-id for EU-listesystem.</span><span class="sxs-lookup"><span data-stu-id="2665b-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="2665b-151">Dette felt er kun tilgængeligt for Tyskland.</span><span class="sxs-lookup"><span data-stu-id="2665b-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="2665b-152">Du kan også angive ekstra filtre på EU-samhandelstransaktioner, som du vil medtage i rapporten.</span><span class="sxs-lookup"><span data-stu-id="2665b-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="2665b-153">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-153">Click OK.</span></span>
    * <span data-ttu-id="2665b-154">Kontroller, at der vises pop op-vinduer, for at bekræfte, at filen og kontrolrapporten, bliver hentet.</span><span class="sxs-lookup"><span data-stu-id="2665b-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="2665b-155">Marker linjerne for EU-listesystemet som rapporteret</span><span class="sxs-lookup"><span data-stu-id="2665b-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="2665b-156">Klik på Marker.</span><span class="sxs-lookup"><span data-stu-id="2665b-156">Click Mark.</span></span>
2. <span data-ttu-id="2665b-157">Klik på Marker som rapporteret.</span><span class="sxs-lookup"><span data-stu-id="2665b-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="2665b-158">Vælg rækken for feltet Fakturadato på listen.</span><span class="sxs-lookup"><span data-stu-id="2665b-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="2665b-159">Skriv "01/01/2016..01/31/2016" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2665b-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="2665b-160">Vælg rækken for feltet Rapporteringsstatus på listen.</span><span class="sxs-lookup"><span data-stu-id="2665b-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="2665b-161">Vælg Medtages i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2665b-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="2665b-162">Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, som du vil markere som Rapporteret.</span><span class="sxs-lookup"><span data-stu-id="2665b-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="2665b-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-163">Click OK.</span></span>
8. <span data-ttu-id="2665b-164">Vælg Rapporteret i feltet Valg.</span><span class="sxs-lookup"><span data-stu-id="2665b-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="2665b-165">Marker linjerne for EU-listesystemet som lukket</span><span class="sxs-lookup"><span data-stu-id="2665b-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="2665b-166">Klik på Marker.</span><span class="sxs-lookup"><span data-stu-id="2665b-166">Click Mark.</span></span>
2. <span data-ttu-id="2665b-167">Klik på Marker som lukket.</span><span class="sxs-lookup"><span data-stu-id="2665b-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="2665b-168">Markér rækken for feltet Fakturadato på listen.</span><span class="sxs-lookup"><span data-stu-id="2665b-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="2665b-169">Skriv "01/01/2016..01/31/2016" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2665b-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="2665b-170">Markér rækken for feltet Rapporteringsstatus på listen.</span><span class="sxs-lookup"><span data-stu-id="2665b-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="2665b-171">Vælg Rapporteret i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2665b-171">In the Criteria field, select ‘Reported’.</span></span>
    * <span data-ttu-id="2665b-172">Du kan også angive ekstra filtre på samhandelstransaktioner inden for Fællesskabet, som du vil markere som Rapporteret.</span><span class="sxs-lookup"><span data-stu-id="2665b-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="2665b-173">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2665b-173">Click OK.</span></span>
8. <span data-ttu-id="2665b-174">Vælg Lukket i feltet Valg.</span><span class="sxs-lookup"><span data-stu-id="2665b-174">In the Selection field, select 'Closed'.</span></span>

