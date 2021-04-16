---
title: Initialisere lagerbeholdninger på lagerstedet
description: Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0746b799c701c569f0ae5c657ac3302ab6626287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823475"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="291c0-103">Initialisere lagerbeholdninger på lagerstedet</span><span class="sxs-lookup"><span data-stu-id="291c0-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="291c0-104">Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden.</span><span class="sxs-lookup"><span data-stu-id="291c0-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="291c0-105">(Det er også muligt at opdatere den disponible lagerbeholdning ved at importere posteringer i dataenheder). Du kan køre denne guide i demodatafirmaet USMF, hvor alle de nødvendige komponenter som kladdenavn, vareopsætning, posteringsprofiler og konti er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="291c0-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="291c0-106">Guiden foreslår specifikke værdier for varen og dimensionerne, der bruges.</span><span class="sxs-lookup"><span data-stu-id="291c0-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="291c0-107">Hvis du vælger et andet element, skal du indtaste værdier for forskellige dimensioner.</span><span class="sxs-lookup"><span data-stu-id="291c0-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="291c0-108">Gå til Lagerstyring > Kladdeposteringer > Elementer > Bevægelser.</span><span class="sxs-lookup"><span data-stu-id="291c0-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="291c0-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="291c0-109">Click New.</span></span>
3. <span data-ttu-id="291c0-110">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="291c0-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="291c0-111">Vælg IMov.</span><span class="sxs-lookup"><span data-stu-id="291c0-111">Select IMov.</span></span>
    * <span data-ttu-id="291c0-112">Det er en god ide at bruge forskellige journalnavnskabeloner for de forskellige forretningsmæssige formål.</span><span class="sxs-lookup"><span data-stu-id="291c0-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="291c0-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="291c0-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="291c0-114">I feltet Modkonto skal du angive værdien "140200".</span><span class="sxs-lookup"><span data-stu-id="291c0-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="291c0-115">Dette er den modkonto, der skal være standardkontoen på kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="291c0-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="291c0-116">Det er muligt at tilsidesætte standardindstillingerne for at tildele forskellige modkonti pr. linje.</span><span class="sxs-lookup"><span data-stu-id="291c0-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="291c0-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="291c0-117">Click OK.</span></span>
8. <span data-ttu-id="291c0-118">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="291c0-118">Click New.</span></span>
9. <span data-ttu-id="291c0-119">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="291c0-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="291c0-120">Vælg vare A0001.</span><span class="sxs-lookup"><span data-stu-id="291c0-120">Select item A0001.</span></span>
11. <span data-ttu-id="291c0-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="291c0-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="291c0-122">Klik på fanen Lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="291c0-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="291c0-123">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="291c0-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="291c0-124">Vælg sted 1.</span><span class="sxs-lookup"><span data-stu-id="291c0-124">Select site 1.</span></span>
15. <span data-ttu-id="291c0-125">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="291c0-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="291c0-126">Vælg lagersted 13.</span><span class="sxs-lookup"><span data-stu-id="291c0-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="291c0-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="291c0-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="291c0-128">Klik på rullelisten i feltet Lokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="291c0-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="291c0-129">Vælg lokalitet 13.</span><span class="sxs-lookup"><span data-stu-id="291c0-129">Select location 13.</span></span>
20. <span data-ttu-id="291c0-130">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="291c0-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="291c0-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="291c0-131">Click Save.</span></span>
22. <span data-ttu-id="291c0-132">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="291c0-132">Click Post.</span></span>
23. <span data-ttu-id="291c0-133">Markér eller fjern markeringen af afkrydsningsfeltet Overfør alle posteringsfejl til en ny kladde.</span><span class="sxs-lookup"><span data-stu-id="291c0-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="291c0-134">Hvis du aktiverer denne indstilling, kopieres alle linjer, der ikke kan bogføres, til en ny journal.</span><span class="sxs-lookup"><span data-stu-id="291c0-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="291c0-135">Du kan bruge oplysningerne i logfilen til at løse problemerne og derefter bogføre linjerne igen.</span><span class="sxs-lookup"><span data-stu-id="291c0-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="291c0-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="291c0-136">Click OK.</span></span>
25. <span data-ttu-id="291c0-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="291c0-137">Close the page.</span></span>
26. <span data-ttu-id="291c0-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="291c0-138">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]