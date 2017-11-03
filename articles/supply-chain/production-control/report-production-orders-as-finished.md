---
title: "Færdigmelde produktionsordrer"
description: "Færdigmelding er et produktionsstadie. På dette stadie færdigmeldes et produkt og flyttes fra produktionsordren til lageret."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 80a882e51332d87835bdfb41a1bb1fcda2471f02
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="69eae-104">Færdigmelde produktionsordrer</span><span class="sxs-lookup"><span data-stu-id="69eae-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="69eae-105">Færdigmelding er et produktionsstadie.</span><span class="sxs-lookup"><span data-stu-id="69eae-105">Report as finished is a production stage.</span></span> <span data-ttu-id="69eae-106">På dette stadie færdigmeldes et produkt og flyttes fra produktionsordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="69eae-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="69eae-107">Når en mængde af de færdige varer færdigmeldes på en produktionsordre, opdateres den som disponibel i lagret.</span><span class="sxs-lookup"><span data-stu-id="69eae-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="69eae-108">Delmængder af den oprindeligt planlagte ordremængde kan færdigmeldes.</span><span class="sxs-lookup"><span data-stu-id="69eae-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="69eae-109">Det er også muligt at indberette fejlmængder med en tilknyttet årsag til fejlen, når mængder færdigmeldes.</span><span class="sxs-lookup"><span data-stu-id="69eae-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="69eae-110">Når produktionsordren når fasen Færdigmeldt, angives det, at ingen yderligere mængder færdigmeldes på produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="69eae-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="69eae-111">Følgende egenskaber er også knyttet til processen **Færdigmelding**:</span><span class="sxs-lookup"><span data-stu-id="69eae-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="69eae-112">Det er muligt at konfigurere forbrug af råvarer og tid, der er proportional med den rapporterede mængde (baglænstræk)</span><span class="sxs-lookup"><span data-stu-id="69eae-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="69eae-113">Lægge på lager-arbejde kan oprettes for varer, der er aktiveret for lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="69eae-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="69eae-114">Den planlagte eller standardkostværdi for de færdige varer kan konfigureres til at blive rapporteret til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="69eae-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="69eae-115">En kvalitetsordre kan oprettes for den rapporterede mængde baseret på konfigurationen af en kvalitetstilknytning.</span><span class="sxs-lookup"><span data-stu-id="69eae-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="69eae-116">Mængden, der er rapporteret til outputplaceringen.</span><span class="sxs-lookup"><span data-stu-id="69eae-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="69eae-117">Lagerstedsarbejde genereres derefter for at flytte mængden fra outputplaceringen til den endelige destination, der er defineret af lokalitetsdirektivet for lægge på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="69eae-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="69eae-118">En kvalitetsordre kan oprettes, når en produktionsordre meldes færdig, hvis der er oprettet en kvalitetstilknytning.</span><span class="sxs-lookup"><span data-stu-id="69eae-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="69eae-119">Konfigurer en produktionsordre, der skal færdigmeldes</span><span class="sxs-lookup"><span data-stu-id="69eae-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="69eae-120">Du kan konfigurere en produktionsordres status til **Færdigmelding** gennem den almindelige funktion til opdatering af produktionsordrer, gennem rute- eller jobkortkladder eller ved hjælp af kladden **Færdigmelding**.</span><span class="sxs-lookup"><span data-stu-id="69eae-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="69eae-121">Du kan også opdatere fasen til **Færdigmelding** via siderne jobkortterminal og jobkortenhed, når du rapporterer på det sidste job i produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="69eae-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="69eae-122">Endelig kan du aktivere indstillingen **Færdigmelding** som en proces for lagerstedets håndholdte enhedsløsning.</span><span class="sxs-lookup"><span data-stu-id="69eae-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




