---
title: Finde forældede produktvarianter
description: Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807986"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="f24d0-103">Finde forældede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="f24d0-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f24d0-104">Denne procedure viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="f24d0-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="f24d0-105">Forudsætning: Du skal definere mindst én status for produktlivscyklus, der er inaktiv for planlægning, før du kan afspille denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="f24d0-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="f24d0-106">Køre en simulering</span><span class="sxs-lookup"><span data-stu-id="f24d0-106">Run a simulation</span></span>
1. <span data-ttu-id="f24d0-107">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="f24d0-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="f24d0-108">Indtast eller vælg en værdi i feltet Ny status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="f24d0-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="f24d0-109">Vælg Ja i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="f24d0-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="f24d0-110">Indtast et tal i feltet Udelad produkter, der er oprettet inden for det angivne antal dage.</span><span class="sxs-lookup"><span data-stu-id="f24d0-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="f24d0-111">Indtast et tal i feltet Udelad produkter, der er brugt i transaktioner (i antal dage).</span><span class="sxs-lookup"><span data-stu-id="f24d0-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="f24d0-112">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="f24d0-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="f24d0-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="f24d0-113">Click Filter.</span></span>
8. <span data-ttu-id="f24d0-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f24d0-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f24d0-115">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="f24d0-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="f24d0-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f24d0-116">Click OK.</span></span>
11. <span data-ttu-id="f24d0-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f24d0-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="f24d0-118">Det anbefales at køre en simulering i batch, hvis du forventer at søge i et stort antal produkter.</span><span class="sxs-lookup"><span data-stu-id="f24d0-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="f24d0-119">Du skal også kontrollere, at simuleringen ikke køres under den mest aktive arbejdstid for firmaet.</span><span class="sxs-lookup"><span data-stu-id="f24d0-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="f24d0-120">Gennemse simuleringsresultaterne.</span><span class="sxs-lookup"><span data-stu-id="f24d0-120">Review the simulation results</span></span>
1. <span data-ttu-id="f24d0-121">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="f24d0-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="f24d0-122">På denne side kan du få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.</span><span class="sxs-lookup"><span data-stu-id="f24d0-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="f24d0-123">Kør opdateringen af livscyklusstatus for forældede produkter</span><span class="sxs-lookup"><span data-stu-id="f24d0-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="f24d0-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f24d0-124">Close the page.</span></span>
2. <span data-ttu-id="f24d0-125">Gå til Administration af produktoplysninger > Periodiske opgaver > Skift livscyklusstatus for forældede produkter.</span><span class="sxs-lookup"><span data-stu-id="f24d0-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="f24d0-126">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="f24d0-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="f24d0-127">Bemærk, at dit seneste valg er blevet gemt.</span><span class="sxs-lookup"><span data-stu-id="f24d0-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="f24d0-128">Vælg Nej i feltet Kør en simulering uden at opdatere produktdata.</span><span class="sxs-lookup"><span data-stu-id="f24d0-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="f24d0-129">Udvid sektionen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="f24d0-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="f24d0-130">Afhængigt af hvor mange produkter og produktvarianter, der er berørt, kan du overveje at køre dette job i batch.</span><span class="sxs-lookup"><span data-stu-id="f24d0-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="f24d0-131">Kontroller, at du ikke kører et stort opdateringsjobbet under den mest aktive arbejdstid i firmaet.</span><span class="sxs-lookup"><span data-stu-id="f24d0-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="f24d0-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f24d0-132">Click OK.</span></span>
7. <span data-ttu-id="f24d0-133">Gå til Administration af produktoplysninger > Forespørgsler og rapporter > Vedligeholdelsesoversigt over status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="f24d0-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="f24d0-134">Gennemse de ændrede udgivne produkter og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="f24d0-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="f24d0-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f24d0-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]