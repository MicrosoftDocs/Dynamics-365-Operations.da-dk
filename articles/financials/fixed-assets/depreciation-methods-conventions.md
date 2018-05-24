---
title: Afskrivningsmetoder og -principper
description: "Denne artikel indeholder en oversigt over afskrivningsprincipper og afskrivningsmetoder, der understøttes af Microsoft Dynamics 365 for Finance and Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f545b0a9abbd7c797afead67917cf80f4cbe0dae
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="68691-103">Afskrivningsmetoder og -principper</span><span class="sxs-lookup"><span data-stu-id="68691-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68691-104">Denne artikel indeholder en oversigt over afskrivningsprincipper og afskrivningsmetoder, der understøttes af Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68691-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="68691-105">Du kan vælge mellem forskellige afskrivningsmetoder og -principper.</span><span class="sxs-lookup"><span data-stu-id="68691-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="68691-106">Formålet med metoderne er at fordele den værdi af et anlægsaktiv, der kan afskrives, på flere regnskabsperioder.</span><span class="sxs-lookup"><span data-stu-id="68691-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="68691-107">Den værdi af et anlægsaktiv, der kan afskrives, er anskaffelsesprisen minus en eventuel scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="68691-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="68691-108">Hvis du bruger afskrivningsprincipper, og du ændrer den seneste startdato for afskrivning på et aktiv, så der springes nogle afskrivninger over, kan afskrivningen for det sidste år blive større eller mindre end forventet.</span><span class="sxs-lookup"><span data-stu-id="68691-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="68691-109">Afskrivningen reguleres med det antal afskrivningsperioder, der påvirkes af ændringen af den seneste startdato for afskrivning.</span><span class="sxs-lookup"><span data-stu-id="68691-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="68691-110">Hvis du f.eks. bruger afskrivningsprincippet Halvår over tre år, afskrives der normalt over 3½ år.</span><span class="sxs-lookup"><span data-stu-id="68691-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="68691-111">Hvis du ændrer den seneste startdato for afskrivning i løbet af de 3½ år, flytter det sidste afskrivningsår uden for det antal perioder, der påvirkes.</span><span class="sxs-lookup"><span data-stu-id="68691-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="68691-112">Hvis du flytter datoen tre måneder, er der ni måneder, hvor der kan afskrives i det sidste år, hvor det normalt ellers ville være seks måneder.</span><span class="sxs-lookup"><span data-stu-id="68691-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="68691-113">Du kan vælge mellem følgende afskrivningsprincipper.</span><span class="sxs-lookup"><span data-stu-id="68691-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="68691-114">Halvår</span><span class="sxs-lookup"><span data-stu-id="68691-114">Half year</span></span>
-   <span data-ttu-id="68691-115">Hel måned</span><span class="sxs-lookup"><span data-stu-id="68691-115">Full month</span></span>
-   <span data-ttu-id="68691-116">Midt i kvartal</span><span class="sxs-lookup"><span data-stu-id="68691-116">Mid quarter</span></span>
-   <span data-ttu-id="68691-117">Midt i måned (d. 1. i måneden)</span><span class="sxs-lookup"><span data-stu-id="68691-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="68691-118">Midt i måned (d. 15. i måneden)</span><span class="sxs-lookup"><span data-stu-id="68691-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="68691-119">Halvår (årsstart)</span><span class="sxs-lookup"><span data-stu-id="68691-119">Half year (start of year)</span></span>
-   <span data-ttu-id="68691-120">Halvår (næste år)</span><span class="sxs-lookup"><span data-stu-id="68691-120">Half year (next year)</span></span>

<span data-ttu-id="68691-121">Du kan vælge mellem følgende afskrivningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="68691-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="68691-122">Lineær afskrivning over servicelevetiden</span><span class="sxs-lookup"><span data-stu-id="68691-122">Straight line service life</span></span>
-   <span data-ttu-id="68691-123">Saldoværdi</span><span class="sxs-lookup"><span data-stu-id="68691-123">Reducing balance</span></span>
-   <span data-ttu-id="68691-124">Manuelt</span><span class="sxs-lookup"><span data-stu-id="68691-124">Manual</span></span>
-   <span data-ttu-id="68691-125">Faktor</span><span class="sxs-lookup"><span data-stu-id="68691-125">Factor</span></span>
-   <span data-ttu-id="68691-126">Forbrug</span><span class="sxs-lookup"><span data-stu-id="68691-126">Consumption</span></span>
-   <span data-ttu-id="68691-127">Lineær afskrivning for den resterende levetid</span><span class="sxs-lookup"><span data-stu-id="68691-127">Straight line life remaining</span></span>
-   <span data-ttu-id="68691-128">200 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="68691-128">200% reducing balance</span></span>
-   <span data-ttu-id="68691-129">175 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="68691-129">175% reducing balance</span></span>
-   <span data-ttu-id="68691-130">150 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="68691-130">150% reducing balance</span></span>
-   <span data-ttu-id="68691-131">125 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="68691-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="68691-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="68691-132">Additional resources</span></span>
--------

[<span data-ttu-id="68691-133">Afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="68691-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="68691-134">Lineær afskrivning for levetiden</span><span class="sxs-lookup"><span data-stu-id="68691-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="68691-135">Saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="68691-136">Manuel afskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="68691-137">Faktorafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="68691-138">Forbrugsafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="68691-139">Lineær afskrivning for den resterende levetid</span><span class="sxs-lookup"><span data-stu-id="68691-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="68691-140">125 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="68691-141">150 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="68691-142">175 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="68691-143">200 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="68691-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




