---
title: Afskrivningsmetoder og -principper
description: Denne artikel indeholder en oversigt over afskrivningsprincipper og afskrivningsmetoder, der understøttes af Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afd771f3f2f0434aa3663a9f99512f0c31adbb78
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826924"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="af654-103">Afskrivningsmetoder og -principper</span><span class="sxs-lookup"><span data-stu-id="af654-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af654-104">Denne artikel indeholder en oversigt over understøttede afskrivningsprincipper og afskrivningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="af654-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="af654-105">Du kan vælge mellem forskellige afskrivningsmetoder og -principper.</span><span class="sxs-lookup"><span data-stu-id="af654-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="af654-106">Formålet med metoderne er at fordele den værdi af et anlægsaktiv, der kan afskrives, på flere regnskabsperioder.</span><span class="sxs-lookup"><span data-stu-id="af654-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="af654-107">Den værdi af et anlægsaktiv, der kan afskrives, er anskaffelsesprisen minus en eventuel scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="af654-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="af654-108">Hvis du bruger afskrivningsprincipper, og du ændrer den seneste startdato for afskrivning på et aktiv, så der springes nogle afskrivninger over, kan afskrivningen for det sidste år blive større eller mindre end forventet.</span><span class="sxs-lookup"><span data-stu-id="af654-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="af654-109">Afskrivningen reguleres med det antal afskrivningsperioder, der påvirkes af ændringen af den seneste startdato for afskrivning.</span><span class="sxs-lookup"><span data-stu-id="af654-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="af654-110">Hvis du f.eks. bruger afskrivningsprincippet Halvår over tre år, afskrives der normalt over 3½ år.</span><span class="sxs-lookup"><span data-stu-id="af654-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="af654-111">Hvis du ændrer den seneste startdato for afskrivning i løbet af de 3½ år, flytter det sidste afskrivningsår uden for det antal perioder, der påvirkes.</span><span class="sxs-lookup"><span data-stu-id="af654-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="af654-112">Hvis du flytter datoen tre måneder, er der ni måneder, hvor der kan afskrives i det sidste år, hvor det normalt ellers ville være seks måneder.</span><span class="sxs-lookup"><span data-stu-id="af654-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="af654-113">Du kan vælge mellem følgende afskrivningsprincipper.</span><span class="sxs-lookup"><span data-stu-id="af654-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="af654-114">Halvår</span><span class="sxs-lookup"><span data-stu-id="af654-114">Half year</span></span>
-   <span data-ttu-id="af654-115">Hel måned</span><span class="sxs-lookup"><span data-stu-id="af654-115">Full month</span></span>
-   <span data-ttu-id="af654-116">Midt i kvartal</span><span class="sxs-lookup"><span data-stu-id="af654-116">Mid quarter</span></span>
-   <span data-ttu-id="af654-117">Midt i måned (d. 1. i måneden)</span><span class="sxs-lookup"><span data-stu-id="af654-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="af654-118">Midt i måned (d. 15. i måneden)</span><span class="sxs-lookup"><span data-stu-id="af654-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="af654-119">Halvår (årsstart)</span><span class="sxs-lookup"><span data-stu-id="af654-119">Half year (start of year)</span></span>
-   <span data-ttu-id="af654-120">Halvår (næste år)</span><span class="sxs-lookup"><span data-stu-id="af654-120">Half year (next year)</span></span>

<span data-ttu-id="af654-121">Du kan vælge mellem følgende afskrivningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="af654-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="af654-122">Lineær afskrivning over servicelevetiden</span><span class="sxs-lookup"><span data-stu-id="af654-122">Straight line service life</span></span>
-   <span data-ttu-id="af654-123">Saldoværdi</span><span class="sxs-lookup"><span data-stu-id="af654-123">Reducing balance</span></span>
-   <span data-ttu-id="af654-124">Manuelt</span><span class="sxs-lookup"><span data-stu-id="af654-124">Manual</span></span>
-   <span data-ttu-id="af654-125">Faktor</span><span class="sxs-lookup"><span data-stu-id="af654-125">Factor</span></span>
-   <span data-ttu-id="af654-126">Forbrug</span><span class="sxs-lookup"><span data-stu-id="af654-126">Consumption</span></span>
-   <span data-ttu-id="af654-127">Lineær afskrivning for den resterende levetid</span><span class="sxs-lookup"><span data-stu-id="af654-127">Straight line life remaining</span></span>
-   <span data-ttu-id="af654-128">200 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="af654-128">200% reducing balance</span></span>
-   <span data-ttu-id="af654-129">175 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="af654-129">175% reducing balance</span></span>
-   <span data-ttu-id="af654-130">150 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="af654-130">150% reducing balance</span></span>
-   <span data-ttu-id="af654-131">125 % saldoværdi</span><span class="sxs-lookup"><span data-stu-id="af654-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="af654-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="af654-132">Additional resources</span></span>
--------

[<span data-ttu-id="af654-133">Afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="af654-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="af654-134">Lineær afskrivning for levetiden</span><span class="sxs-lookup"><span data-stu-id="af654-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="af654-135">Saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-135">Reduce balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="af654-136">Manuel afskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="af654-137">Faktorafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="af654-138">Forbrugsafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="af654-139">Lineær afskrivning for den resterende levetid</span><span class="sxs-lookup"><span data-stu-id="af654-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="af654-140">125 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="af654-141">150 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="af654-142">175 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="af654-143">200 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="af654-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]