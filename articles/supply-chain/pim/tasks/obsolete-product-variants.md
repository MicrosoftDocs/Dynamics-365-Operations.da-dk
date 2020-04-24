---
title: Finde forældede produktvarianter
description: Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aea9c785ce57bf498007d3127edbd270b1c31a52
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203474"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="9dc05-103">Finde forældede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="9dc05-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dc05-104">Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="9dc05-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="9dc05-105">Forudsætning: Du skal definere mindst én status for produktlivscyklus, der er inaktiv for planlægning, før du kan afspille denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="9dc05-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="9dc05-106">Køre en simulering</span><span class="sxs-lookup"><span data-stu-id="9dc05-106">Run a simulation</span></span>
1. <span data-ttu-id="9dc05-107">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="9dc05-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="9dc05-108">Indtast eller vælg en værdi i feltet Ny status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="9dc05-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="9dc05-109">Vælg Ja i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="9dc05-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="9dc05-110">Indtast et tal i feltet Udelad produkter, der er oprettet inden for det angivne antal dage.</span><span class="sxs-lookup"><span data-stu-id="9dc05-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="9dc05-111">Indtast et tal i feltet Udelad produkter, der er brugt i transaktioner (i antal dage).</span><span class="sxs-lookup"><span data-stu-id="9dc05-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="9dc05-112">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="9dc05-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9dc05-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="9dc05-113">Click Filter.</span></span>
8. <span data-ttu-id="9dc05-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9dc05-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9dc05-115">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="9dc05-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="9dc05-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9dc05-116">Click OK.</span></span>
11. <span data-ttu-id="9dc05-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9dc05-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc05-118">Det anbefales at køre en simulering i batch, hvis du forventer at søge i et stort antal produkter.</span><span class="sxs-lookup"><span data-stu-id="9dc05-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="9dc05-119">Du skal også kontrollere, at simuleringen ikke køres under den mest aktive arbejdstid for firmaet.</span><span class="sxs-lookup"><span data-stu-id="9dc05-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="9dc05-120">Gennemse simuleringsresultaterne.</span><span class="sxs-lookup"><span data-stu-id="9dc05-120">Review the simulation results</span></span>
1. <span data-ttu-id="9dc05-121">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="9dc05-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="9dc05-122">På denne side kan du få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.</span><span class="sxs-lookup"><span data-stu-id="9dc05-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="9dc05-123">Kør opdateringen af livscyklusstatus for forældede produkter</span><span class="sxs-lookup"><span data-stu-id="9dc05-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="9dc05-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9dc05-124">Close the page.</span></span>
2. <span data-ttu-id="9dc05-125">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="9dc05-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="9dc05-126">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="9dc05-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc05-127">Bemærk, at dit seneste valg er blevet gemt.</span><span class="sxs-lookup"><span data-stu-id="9dc05-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="9dc05-128">Vælg Nej i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="9dc05-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="9dc05-129">Udvid sektionen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="9dc05-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc05-130">Afhængigt af hvor mange produkter og produktvarianter, der er berørt, kan du overveje at køre dette job i batch.</span><span class="sxs-lookup"><span data-stu-id="9dc05-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="9dc05-131">Kontroller, at du ikke kører et stort opdateringsjobbet under den mest aktive arbejdstid i firmaet.</span><span class="sxs-lookup"><span data-stu-id="9dc05-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="9dc05-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9dc05-132">Click OK.</span></span>
7. <span data-ttu-id="9dc05-133">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="9dc05-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc05-134">Gennemse de ændrede udgivne produkter og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="9dc05-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="9dc05-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9dc05-135">In the list, find and select the desired record.</span></span>

