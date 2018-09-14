--- 
title: Konfigurere vareomfordeling for kort plukning
description: "Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: bf56a0811c4793ee2e3eaf78c8696c3c29e984c3
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="18881-103">Konfigurere vareomfordeling for kort plukning</span><span class="sxs-lookup"><span data-stu-id="18881-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18881-104">Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til.</span><span class="sxs-lookup"><span data-stu-id="18881-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="18881-105">Det er muligt at bruge en automatisk omfordelingsproces, som bruger lokalitetsbestemmelser til at hente varerne, hvis de er tilgængelige på en anden lokalitet.</span><span class="sxs-lookup"><span data-stu-id="18881-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="18881-106">Når manuel omfordeling bruges, vises der også en liste over lokaliteter med det disponible på mobilenheden, så lagermedarbejderen kan vælge, hvilken lokalitet lageret skal bruges fra.</span><span class="sxs-lookup"><span data-stu-id="18881-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="18881-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="18881-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="18881-108">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="18881-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="18881-109">Konfigurer arbejdsundtagelser</span><span class="sxs-lookup"><span data-stu-id="18881-109">Set up work exceptions</span></span>
1. <span data-ttu-id="18881-110">Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsundtagelser.</span><span class="sxs-lookup"><span data-stu-id="18881-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="18881-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="18881-111">Click New.</span></span>
    * <span data-ttu-id="18881-112">Det er muligt at definere flere undtagelser for arbejde med forskellige politikker for omfordeling af varer for at give lagermedarbejderen mulighed for at vælge én baseret på behov i den leverance, som de behandler.</span><span class="sxs-lookup"><span data-stu-id="18881-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="18881-113">Indtast en værdi i feltet Kode for arbejdsundtagelse.</span><span class="sxs-lookup"><span data-stu-id="18881-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="18881-114">Giv undtagelsen for arbejde en titel for at angive, hvad den skal bruges til.</span><span class="sxs-lookup"><span data-stu-id="18881-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="18881-115">Det kan f.eks. være Vejledning til korte pluk.</span><span class="sxs-lookup"><span data-stu-id="18881-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="18881-116">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="18881-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="18881-117">Vælg "Kort pluk" i feltet Undtagelsestype.</span><span class="sxs-lookup"><span data-stu-id="18881-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="18881-118">Marker afkrydsningsfeltet Reguler lager.</span><span class="sxs-lookup"><span data-stu-id="18881-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="18881-119">Denne indstilling betyder, at lageret automatisk reguleres til 0 på den placering, hvor der er udført korte pluk.</span><span class="sxs-lookup"><span data-stu-id="18881-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="18881-120">Indtast eller vælg en værdi i feltet Standardkode for reguleringstype.</span><span class="sxs-lookup"><span data-stu-id="18881-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="18881-121">I USMF kan du for eksempel vælge 'Fjern Res Adj Out'.</span><span class="sxs-lookup"><span data-stu-id="18881-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="18881-122">Vælg 'Manuelt' i feltet Vareomfordeling.</span><span class="sxs-lookup"><span data-stu-id="18881-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="18881-123">Hvis du vælger Manuel eller Automatisk og manuel, skal lagermedarbejderen have mulighed for at bruge manuel omfordeling.</span><span class="sxs-lookup"><span data-stu-id="18881-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="18881-124">Konfigurer en arbejder til at bruge manuel vareomfordeling</span><span class="sxs-lookup"><span data-stu-id="18881-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="18881-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18881-125">Close the page.</span></span>
2. <span data-ttu-id="18881-126">Gå til Lokationsstyring > Konfiguration > Arbejder.</span><span class="sxs-lookup"><span data-stu-id="18881-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="18881-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="18881-127">Click Edit.</span></span>
4. <span data-ttu-id="18881-128">Vælg arbejder 24 på listen.</span><span class="sxs-lookup"><span data-stu-id="18881-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="18881-129">Udvid afsnittet Arbejde.</span><span class="sxs-lookup"><span data-stu-id="18881-129">Expand the Work section.</span></span>
6. <span data-ttu-id="18881-130">Vælg Ja i feltet Tillad manuel vareomfordeling.</span><span class="sxs-lookup"><span data-stu-id="18881-130">Select Yes in the Allow manual item reallocation field.</span></span>


