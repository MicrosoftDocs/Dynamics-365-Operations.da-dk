---
title: Aktivere forsinket momsberegning på kladder
description: I dette emne forklares det, hvordan du kan bruge funktionen Forsinket momsberegning til at forbedre ydeevnen af momsberegninger, når antallet af kladdelinjer er meget stort.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d842b60b3cca8c29b281ab4a6a1b6c3b0bad3684
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236716"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="e1633-103">Aktivere forsinket momsberegning på kladder</span><span class="sxs-lookup"><span data-stu-id="e1633-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="e1633-104">Dette emne forklarer, hvordan du kan forsinke momsberegningen på kladder.</span><span class="sxs-lookup"><span data-stu-id="e1633-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="e1633-105">Denne facilitet hjælper med at forbedre ydeevnen af momsberegninger, når der er mange kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="e1633-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="e1633-106">Momsbeløb på kladdelinjer beregnes som standard, når momsrelaterede felter opdateres.</span><span class="sxs-lookup"><span data-stu-id="e1633-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="e1633-107">Disse felter omfatter felterne til momsgrupper og varemomsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e1633-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="e1633-108">Enhver opdatering af en kladdelinje medfører, at momsbeløb genberegnes for alle kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="e1633-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="e1633-109">Selvom denne funktionsmåde hjælper brugeren med at se momsbeløb beregnet i realtid, kan det også påvirke ydeevnen, hvis antallet af kladdelinjer er meget stort.</span><span class="sxs-lookup"><span data-stu-id="e1633-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="e1633-110">Med funktionen til forsinket beregning af moms kan du forsinke momsberegningen på kladder og dermed løse problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="e1633-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="e1633-111">Hvis denne funktion er slået til, vil momsbeløb kun blive beregnet, når brugeren vælger **Moms** eller bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="e1633-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="e1633-112">Du kan forsinke beregningen af moms på tre niveauer:</span><span class="sxs-lookup"><span data-stu-id="e1633-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="e1633-113">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="e1633-113">Legal entity</span></span>
- <span data-ttu-id="e1633-114">Kladdenavn</span><span class="sxs-lookup"><span data-stu-id="e1633-114">Journal name</span></span>
- <span data-ttu-id="e1633-115">Kladdehoved</span><span class="sxs-lookup"><span data-stu-id="e1633-115">Journal header</span></span>

<span data-ttu-id="e1633-116">Systemet giver prioriteten til indstillingen for kladdehovedet.</span><span class="sxs-lookup"><span data-stu-id="e1633-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="e1633-117">Denne indstilling hentes som standard fra kladdenavnet.</span><span class="sxs-lookup"><span data-stu-id="e1633-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="e1633-118">Indstillingen for kladdenavnet hentes som standard fra indstillingen på siden **Finansparametre**, når kladdenavnet oprettes.</span><span class="sxs-lookup"><span data-stu-id="e1633-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="e1633-119">I følgende afsnit forklares det, hvordan du aktiverer forsinket momsberegning for juridiske enheder, kladdenavne og kladdehoveder.</span><span class="sxs-lookup"><span data-stu-id="e1633-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="e1633-120">Aktivere forsinket momsberegning på juridisk enhedsniveau</span><span class="sxs-lookup"><span data-stu-id="e1633-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="e1633-121">Gå til **Finans \> Opsætning Finans \> Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="e1633-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="e1633-122">Under fanen **Moms** i oversigtspanelet **Generelt** skal du vælge **Ja** i indstillingen **Forsinket momsberegning**.</span><span class="sxs-lookup"><span data-stu-id="e1633-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Billede af finansparametre](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="e1633-124">Aktivere forsinket momsberegning på kladdenavnsniveau</span><span class="sxs-lookup"><span data-stu-id="e1633-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="e1633-125">Gå til **Finans \> Kladdeopsætning \> Kladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="e1633-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="e1633-126">I sektionen **Moms** i oversigtspanelet **Generelt** skal du vælge **Ja** i indstillingen **Forsinket momsberegning**.</span><span class="sxs-lookup"><span data-stu-id="e1633-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Billede af kladdenavne](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="e1633-128">Aktivere forsinket momsberegning på kladdehovedniveau</span><span class="sxs-lookup"><span data-stu-id="e1633-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="e1633-129">Gå til **Finans \> Kladdeposteringer \> Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="e1633-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="e1633-130">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e1633-130">Select **New**.</span></span>
3. <span data-ttu-id="e1633-131">Vælg et kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="e1633-131">Select a journal name.</span></span>
4. <span data-ttu-id="e1633-132">Under fanen **Opsætning** skal du angive indstillingen **Forsinket momsberegning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e1633-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Billede af siden Finanskladde](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]