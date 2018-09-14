--- 
title: "Initialisere lagerbeholdninger på lagerstedet"
description: "Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4bfa40c19e34631edb68b8cff42e7f72eb9ce2ad
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="9ce70-103">Initialisere lagerbeholdninger på lagerstedet</span><span class="sxs-lookup"><span data-stu-id="9ce70-103">Initialize stock levels in the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ce70-104">Denne procedure viser, hvordan du får den disponible lagerbeholdning opdateret manuelt ved hjælp af en lagerbevægelseskladden.</span><span class="sxs-lookup"><span data-stu-id="9ce70-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="9ce70-105">(Det er også muligt at opdatere den disponible lagerbeholdning ved at importere posteringer i dataenheder). Du kan køre denne guide i demodatafirmaet USMF, hvor alle de nødvendige komponenter som kladdenavn, vareopsætning, posteringsprofiler og konti er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="9ce70-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="9ce70-106">Guiden foreslår specifikke værdier for varen og dimensionerne, der bruges.</span><span class="sxs-lookup"><span data-stu-id="9ce70-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="9ce70-107">Hvis du vælger et andet element, skal du indtaste værdier for forskellige dimensioner.</span><span class="sxs-lookup"><span data-stu-id="9ce70-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="9ce70-108">Gå til Lagerstyring > Kladdeposteringer > Elementer > Bevægelser.</span><span class="sxs-lookup"><span data-stu-id="9ce70-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="9ce70-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9ce70-109">Click New.</span></span>
3. <span data-ttu-id="9ce70-110">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9ce70-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9ce70-111">Vælg IMov.</span><span class="sxs-lookup"><span data-stu-id="9ce70-111">Select IMov.</span></span>
    * <span data-ttu-id="9ce70-112">Det er en god ide at bruge forskellige journalnavnskabeloner for de forskellige forretningsmæssige formål.</span><span class="sxs-lookup"><span data-stu-id="9ce70-112">It’s a good practise to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="9ce70-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9ce70-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9ce70-114">I feltet Modkonto skal du angive værdien "140200".</span><span class="sxs-lookup"><span data-stu-id="9ce70-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="9ce70-115">Dette er den modkonto, der skal være standardkontoen på kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="9ce70-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="9ce70-116">Det er muligt at tilsidesætte standardindstillingerne for at tildele forskellige modkonti pr. linje.</span><span class="sxs-lookup"><span data-stu-id="9ce70-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="9ce70-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9ce70-117">Click OK.</span></span>
8. <span data-ttu-id="9ce70-118">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9ce70-118">Click New.</span></span>
9. <span data-ttu-id="9ce70-119">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9ce70-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9ce70-120">Vælg vare A0001.</span><span class="sxs-lookup"><span data-stu-id="9ce70-120">Select item A0001.</span></span>
11. <span data-ttu-id="9ce70-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9ce70-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="9ce70-122">Klik på fanen Lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="9ce70-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="9ce70-123">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9ce70-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="9ce70-124">Vælg sted 1.</span><span class="sxs-lookup"><span data-stu-id="9ce70-124">Select site 1.</span></span>
15. <span data-ttu-id="9ce70-125">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9ce70-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="9ce70-126">Vælg lagersted 13.</span><span class="sxs-lookup"><span data-stu-id="9ce70-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="9ce70-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9ce70-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9ce70-128">Klik på rullelisten i feltet Lokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9ce70-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="9ce70-129">Vælg lokalitet 13.</span><span class="sxs-lookup"><span data-stu-id="9ce70-129">Select location 13.</span></span>
20. <span data-ttu-id="9ce70-130">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="9ce70-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="9ce70-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9ce70-131">Click Save.</span></span>
22. <span data-ttu-id="9ce70-132">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="9ce70-132">Click Post.</span></span>
23. <span data-ttu-id="9ce70-133">Markér eller fjern markeringen af afkrydsningsfeltet Overfør alle posteringsfejl til en ny kladde.</span><span class="sxs-lookup"><span data-stu-id="9ce70-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="9ce70-134">Hvis du aktiverer denne indstilling, kopieres alle linjer, der ikke kan bogføres, til en ny journal.</span><span class="sxs-lookup"><span data-stu-id="9ce70-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="9ce70-135">Du kan bruge oplysningerne i logfilen til at løse problemerne og derefter bogføre linjerne igen.</span><span class="sxs-lookup"><span data-stu-id="9ce70-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="9ce70-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9ce70-136">Click OK.</span></span>
25. <span data-ttu-id="9ce70-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9ce70-137">Close the page.</span></span>
26. <span data-ttu-id="9ce70-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9ce70-138">Close the page.</span></span>


