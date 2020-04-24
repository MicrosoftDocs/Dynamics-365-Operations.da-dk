---
title: Konfigurere vareomfordeling for kort plukning
description: Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216798"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="05555-103">Konfigurere vareomfordeling for kort plukning</span><span class="sxs-lookup"><span data-stu-id="05555-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05555-104">Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til.</span><span class="sxs-lookup"><span data-stu-id="05555-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn't sufficient inventory at the location they've been directed to.</span></span> <span data-ttu-id="05555-105">Det er muligt at bruge en automatisk omfordelingsproces, som bruger lokalitetsbestemmelser til at hente varerne, hvis de er tilgængelige på en anden lokalitet.</span><span class="sxs-lookup"><span data-stu-id="05555-105">It's possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they're available at another location.</span></span> <span data-ttu-id="05555-106">Når manuel omfordeling bruges, vises der også en liste over lokaliteter med det disponible på mobilenheden, så lagermedarbejderen kan vælge, hvilken lokalitet lageret skal bruges fra.</span><span class="sxs-lookup"><span data-stu-id="05555-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="05555-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="05555-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="05555-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="05555-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="05555-109">Konfigurer arbejdsundtagelser</span><span class="sxs-lookup"><span data-stu-id="05555-109">Set up work exceptions</span></span>
1. <span data-ttu-id="05555-110">I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejde > Arbejdsundtagelser**.</span><span class="sxs-lookup"><span data-stu-id="05555-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="05555-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="05555-111">Click **New**.</span></span> <span data-ttu-id="05555-112">Det er muligt at definere flere undtagelser for arbejde med forskellige politikker for omfordeling af varer for at give lagermedarbejderen mulighed for at vælge én baseret på behov i den leverance, som de behandler.</span><span class="sxs-lookup"><span data-stu-id="05555-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="05555-113">Indtast en værdi i feltet **Kode for arbejdsundtagelse**.</span><span class="sxs-lookup"><span data-stu-id="05555-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="05555-114">Giv undtagelsen for arbejde en titel for at angive, hvad den skal bruges til.</span><span class="sxs-lookup"><span data-stu-id="05555-114">Give the work exception a title to indicate what it's used for.</span></span> <span data-ttu-id="05555-115">Det kan f.eks. være Vejledning til korte pluk.</span><span class="sxs-lookup"><span data-stu-id="05555-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="05555-116">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="05555-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="05555-117">Vælg 'Kort pluk' i typefeltet **Undtagelse**.</span><span class="sxs-lookup"><span data-stu-id="05555-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="05555-118">Marker afkrydsningsfeltet **Reguler lager**.</span><span class="sxs-lookup"><span data-stu-id="05555-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="05555-119">Denne indstilling betyder, at lageret automatisk reguleres til 0 på den placering, hvor der er udført korte pluk.</span><span class="sxs-lookup"><span data-stu-id="05555-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="05555-120">Indtast eller vælg en værdi i feltet **Standardkode for reguleringstype**.</span><span class="sxs-lookup"><span data-stu-id="05555-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="05555-121">I USMF kan du for eksempel vælge 'Fjern Res Adj Out'.</span><span class="sxs-lookup"><span data-stu-id="05555-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="05555-122">Vælg 'Manuelt' i feltet **Vareomfordeling**.</span><span class="sxs-lookup"><span data-stu-id="05555-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="05555-123">Hvis du vælger Manuel eller Automatisk og manuel, skal lagermedarbejderen have mulighed for at bruge manuel omfordeling.</span><span class="sxs-lookup"><span data-stu-id="05555-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="05555-124">Konfigurer en arbejder til at bruge manuel vareomfordeling</span><span class="sxs-lookup"><span data-stu-id="05555-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="05555-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="05555-125">Close the page.</span></span>
2. <span data-ttu-id="05555-126">I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="05555-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="05555-127">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="05555-127">Click **Edit**.</span></span>
4. <span data-ttu-id="05555-128">Vælg arbejder 24 på listen.</span><span class="sxs-lookup"><span data-stu-id="05555-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="05555-129">Udvid oversigtspanelet **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="05555-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="05555-130">Vælg 'Ja' i feltet **Tillad manuel vareomfordeling**.</span><span class="sxs-lookup"><span data-stu-id="05555-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

