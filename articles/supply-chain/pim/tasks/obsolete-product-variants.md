---
title: Finde forældede produktvarianter
description: Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dcd0f67bae1042cb1e81423898eacd20f921e0e2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147572"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="465bc-103">Finde forældede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="465bc-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="465bc-104">Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="465bc-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="465bc-105">Forudsætning: Du skal definere mindst én status for produktlivscyklus, der er inaktiv for planlægning, før du kan afspille denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="465bc-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="465bc-106">Køre en simulering</span><span class="sxs-lookup"><span data-stu-id="465bc-106">Run a simulation</span></span>
1. <span data-ttu-id="465bc-107">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="465bc-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="465bc-108">Indtast eller vælg en værdi i feltet Ny status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="465bc-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="465bc-109">Vælg Ja i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="465bc-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="465bc-110">Indtast et tal i feltet Udelad produkter, der er oprettet inden for det angivne antal dage.</span><span class="sxs-lookup"><span data-stu-id="465bc-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="465bc-111">Indtast et tal i feltet Udelad produkter, der er brugt i transaktioner (i antal dage).</span><span class="sxs-lookup"><span data-stu-id="465bc-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="465bc-112">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="465bc-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="465bc-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="465bc-113">Click Filter.</span></span>
8. <span data-ttu-id="465bc-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="465bc-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="465bc-115">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="465bc-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="465bc-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="465bc-116">Click OK.</span></span>
11. <span data-ttu-id="465bc-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="465bc-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="465bc-118">Det anbefales at køre en simulering i batch, hvis du forventer at søge i et stort antal produkter.</span><span class="sxs-lookup"><span data-stu-id="465bc-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="465bc-119">Du skal også kontrollere, at simuleringen ikke køres under den mest aktive arbejdstid for firmaet.</span><span class="sxs-lookup"><span data-stu-id="465bc-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="465bc-120">Gennemse simuleringsresultaterne.</span><span class="sxs-lookup"><span data-stu-id="465bc-120">Review the simulation results</span></span>
1. <span data-ttu-id="465bc-121">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="465bc-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="465bc-122">På denne side kan du få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.</span><span class="sxs-lookup"><span data-stu-id="465bc-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="465bc-123">Kør opdateringen af livscyklusstatus for forældede produkter</span><span class="sxs-lookup"><span data-stu-id="465bc-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="465bc-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="465bc-124">Close the page.</span></span>
2. <span data-ttu-id="465bc-125">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="465bc-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="465bc-126">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="465bc-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="465bc-127">Bemærk, at dit seneste valg er blevet gemt.</span><span class="sxs-lookup"><span data-stu-id="465bc-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="465bc-128">Vælg Nej i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="465bc-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="465bc-129">Udvid sektionen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="465bc-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="465bc-130">Afhængigt af hvor mange produkter og produktvarianter, der er berørt, kan du overveje at køre dette job i batch.</span><span class="sxs-lookup"><span data-stu-id="465bc-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="465bc-131">Kontroller, at du ikke kører et stort opdateringsjobbet under den mest aktive arbejdstid i firmaet.</span><span class="sxs-lookup"><span data-stu-id="465bc-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="465bc-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="465bc-132">Click OK.</span></span>
7. <span data-ttu-id="465bc-133">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="465bc-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="465bc-134">Gennemse de ændrede udgivne produkter og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="465bc-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="465bc-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="465bc-135">In the list, find and select the desired record.</span></span>

