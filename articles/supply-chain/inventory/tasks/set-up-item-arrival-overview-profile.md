---
title: Konfigurere en oversigtsprofil for varemodtagelse
description: Denne opgave fokuserer på oprettelse af en profil for modtagelsesoversigt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "338009"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="6a92e-103">Konfigurere en oversigtsprofil for varemodtagelse</span><span class="sxs-lookup"><span data-stu-id="6a92e-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a92e-104">Denne opgave fokuserer på oprettelse af en profil for modtagelsesoversigt.</span><span class="sxs-lookup"><span data-stu-id="6a92e-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="6a92e-105">Profilen for modtagelsesoversigt er en samling af regler, der anvendes, når siden Modtagelsesoversigt åbnes af en bruger.</span><span class="sxs-lookup"><span data-stu-id="6a92e-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="6a92e-106">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="6a92e-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="6a92e-107">Denne procedure vil typisk blive udført af en modtagende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="6a92e-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="6a92e-108">Gå til Lagerstyring > Opsætning > Distribution > Profiler for oversigt over modtagelse.</span><span class="sxs-lookup"><span data-stu-id="6a92e-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="6a92e-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6a92e-109">Click New.</span></span>
    * <span data-ttu-id="6a92e-110">Da du næsten altid vil arbejde på samme lagersted og aflaste fulde lastbillæs, bør du oprette en profil for modtagelsesoversigt for at forenkle processen med at registrere modtagne varer.</span><span class="sxs-lookup"><span data-stu-id="6a92e-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="6a92e-111">Indtast en værdi i feltet Navn for profil for oversigt over modtagelse.</span><span class="sxs-lookup"><span data-stu-id="6a92e-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="6a92e-112">Vælg en indstilling i feltet Vis linjer.</span><span class="sxs-lookup"><span data-stu-id="6a92e-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="6a92e-113">Vælg, hvilke linjer der skal vises for tilgangene: Alle – Vis alle linjer, uanset status.</span><span class="sxs-lookup"><span data-stu-id="6a92e-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="6a92e-114">I gang – Vis linjer for tilgange, hvor statussen er Afsluttet eller Delvist.</span><span class="sxs-lookup"><span data-stu-id="6a92e-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="6a92e-115">Dette betyder, at enten det fulde antal eller et delvist antal er registreret for hver linje i en modtagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="6a92e-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="6a92e-116">Ikke færdig – Vis linjer for tilgange, hvor statussen er Ingen eller Delvist.</span><span class="sxs-lookup"><span data-stu-id="6a92e-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="6a92e-117">Dette betyder, at enten intet eller kun et delvist antal er registreret for hver linje i en modtagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="6a92e-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="6a92e-118">Udvid eller skjul sektionen Modtagelsesindstillinger.</span><span class="sxs-lookup"><span data-stu-id="6a92e-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="6a92e-119">Indtast en værdi i feltet Dage frem.</span><span class="sxs-lookup"><span data-stu-id="6a92e-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="6a92e-120">Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget inden for de næste par dage (afhængigt af det nummer, du angiver).</span><span class="sxs-lookup"><span data-stu-id="6a92e-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="6a92e-121">Indtast en værdi i feltet Dage tilbage.</span><span class="sxs-lookup"><span data-stu-id="6a92e-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="6a92e-122">Dette angiver et filter for at vise de kvitteringslinjer, der forventes at blive modtaget et antal dage før dags dato.</span><span class="sxs-lookup"><span data-stu-id="6a92e-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="6a92e-123">Indtast en værdi i feltet Lagersteder.</span><span class="sxs-lookup"><span data-stu-id="6a92e-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="6a92e-124">Filter på et eller flere lagersteder.</span><span class="sxs-lookup"><span data-stu-id="6a92e-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="6a92e-125">Vælg en værdi i feltet Leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="6a92e-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="6a92e-126">Dette angiver et filter til kun at vise modtagelseslinjerne med denne leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="6a92e-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="6a92e-127">Vælg WHS i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6a92e-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="6a92e-128">I feltet Lagersted skal du vælge et lagersted 24.</span><span class="sxs-lookup"><span data-stu-id="6a92e-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="6a92e-129">Dette er det standardlagersted, der skal bruges til registrerede modtagelseslinjer, der bruger denne profil.</span><span class="sxs-lookup"><span data-stu-id="6a92e-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="6a92e-130">Vælg Baydoor i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="6a92e-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="6a92e-131">Dette er den standardlokalitet, der skal bruges til registrerede modtagelseslinjer, som bruger denne profil.</span><span class="sxs-lookup"><span data-stu-id="6a92e-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="6a92e-132">Vis eller skjul sektionen Oplysninger om modtagelsesforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="6a92e-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="6a92e-133">Vælg lokation 2 i feltet Begræns til sted.</span><span class="sxs-lookup"><span data-stu-id="6a92e-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="6a92e-134">Dette angiver et filter til kun at vise modtagelseslinjerne med dette sted.</span><span class="sxs-lookup"><span data-stu-id="6a92e-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="6a92e-135">Angiv indstillingen Indkøbsordrer til Ja.</span><span class="sxs-lookup"><span data-stu-id="6a92e-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="6a92e-136">Vælg kvitteringslinjer fra åbne indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="6a92e-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="6a92e-137">Angiv indstillingen Flytteordrer til Ja.</span><span class="sxs-lookup"><span data-stu-id="6a92e-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="6a92e-138">Vælg kvitteringslinjer fra flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="6a92e-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="6a92e-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6a92e-139">Click Save.</span></span>
18. <span data-ttu-id="6a92e-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6a92e-140">Close the page.</span></span>

