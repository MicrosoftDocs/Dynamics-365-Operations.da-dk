---
title: Konfigurere en oversigtsprofil for varemodtagelse
description: Dette emne fokuserer på oprettelse af en modtagelsesoversigtsprofil.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55512c75445a5f3b9c1521376a20d48dd60e22c6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145519"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="22786-103">Konfigurere en oversigtsprofil for varemodtagelse</span><span class="sxs-lookup"><span data-stu-id="22786-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="22786-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="22786-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="22786-105">Dette emne fokuserer på oprettelse af en modtagelsesoversigtsprofil.</span><span class="sxs-lookup"><span data-stu-id="22786-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="22786-106">Profilen for modtagelsesoversigt er en samling af regler, der anvendes, når siden Modtagelsesoversigt åbnes af en bruger.</span><span class="sxs-lookup"><span data-stu-id="22786-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="22786-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="22786-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="22786-108">Denne procedure vil typisk blive udført af en modtagende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="22786-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="22786-109">I navigationsruden skal du gå til **Moduler > Lagerstyring > Opsætning > Distribution > Profiler for oversigt over modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="22786-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="22786-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="22786-110">Select **New**.</span></span> <span data-ttu-id="22786-111">Da du næsten altid vil arbejde på samme lagersted og aflaste fulde lastbillæs, bør du oprette en profil for modtagelsesoversigt for at forenkle processen med at registrere modtagne varer.</span><span class="sxs-lookup"><span data-stu-id="22786-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="22786-112">Indtast en værdi i feltet **Navn for profil for oversigt over modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="22786-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="22786-113">Vælg en indstilling i feltet **Vis linjer**.</span><span class="sxs-lookup"><span data-stu-id="22786-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="22786-114">Vælg, hvilke linjer der skal vises for tilgangene:</span><span class="sxs-lookup"><span data-stu-id="22786-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="22786-115">**Alle** – Vis alle linjer uanset status.</span><span class="sxs-lookup"><span data-stu-id="22786-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="22786-116">**I gang** – Vis linjer for tilgange, hvor statussen er Afsluttet eller Delvist.</span><span class="sxs-lookup"><span data-stu-id="22786-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="22786-117">Dette betyder, at enten det fulde antal eller et delvist antal er registreret for hver linje i en modtagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="22786-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="22786-118">**Ikke færdig** – Vis linjer for tilgange, hvor statussen er Ingen eller Delvist.</span><span class="sxs-lookup"><span data-stu-id="22786-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="22786-119">Dette betyder, at enten intet eller kun et delvist antal er registreret for hver linje i en modtagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="22786-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="22786-120">Udvid eller skjul sektionen **Modtagelsesindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="22786-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="22786-121">Indtast en værdi i feltet **Dage frem**.</span><span class="sxs-lookup"><span data-stu-id="22786-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="22786-122">Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget inden for de næste par dage (afhængigt af det nummer, du angiver).</span><span class="sxs-lookup"><span data-stu-id="22786-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="22786-123">Indtast en værdi i feltet **Dage tilbage**.</span><span class="sxs-lookup"><span data-stu-id="22786-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="22786-124">Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget et antal dage før dags dato.</span><span class="sxs-lookup"><span data-stu-id="22786-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="22786-125">Indtast en værdi i feltet **Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="22786-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="22786-126">Filter på et eller flere lagersteder.</span><span class="sxs-lookup"><span data-stu-id="22786-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="22786-127">Vælg en værdi i feltet **Leveringsmåde**.</span><span class="sxs-lookup"><span data-stu-id="22786-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="22786-128">Dette angiver et filter til kun at vise modtagelseslinjerne med denne leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="22786-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="22786-129">Vælg WHS i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="22786-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="22786-130">I feltet **Lagersted** skal du vælge et lagersted 24.</span><span class="sxs-lookup"><span data-stu-id="22786-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="22786-131">Dette er det standardlagersted, der skal bruges til registrerede modtagelseslinjer, der bruger denne profil.</span><span class="sxs-lookup"><span data-stu-id="22786-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="22786-132">Vælg **Baydoor** i feltet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="22786-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="22786-133">Dette er den standardlokalitet, der skal bruges til registrerede modtagelseslinjer, som bruger denne profil.</span><span class="sxs-lookup"><span data-stu-id="22786-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="22786-134">Vis eller skjul sektionen **Oplysninger om modtagelsesforespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="22786-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="22786-135">Vælg lokation 2 i feltet **Begræns til sted**.</span><span class="sxs-lookup"><span data-stu-id="22786-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="22786-136">Dette angiver et filter til kun at vise modtagelseslinjerne med dette sted.</span><span class="sxs-lookup"><span data-stu-id="22786-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="22786-137">Vælg **Ja** i indstillingen **Indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="22786-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="22786-138">Vælg kvitteringslinjer fra åbne indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="22786-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="22786-139">Vælg **Ja** i indstillingen **Flytteordrer**.</span><span class="sxs-lookup"><span data-stu-id="22786-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="22786-140">Vælg kvitteringslinjer fra flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="22786-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="22786-141">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="22786-141">Select **Save**.</span></span>
18. <span data-ttu-id="22786-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22786-142">Close the page.</span></span>

