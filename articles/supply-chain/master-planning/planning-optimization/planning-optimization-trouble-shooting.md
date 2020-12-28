---
title: Fejlfinde planlægningsoptimering
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424408"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="b5e47-103">Fejlfinde planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="b5e47-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5e47-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="b5e47-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="b5e47-105">Installationen af tilføjelsesprogrammet Planlægningsoptimering blev ikke fuldført</span><span class="sxs-lookup"><span data-stu-id="b5e47-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="b5e47-106">Planlægningsoptimering er et LCS (Lifecycle Services) med høj tilgængelighed på niveau 2 eller højere (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="b5e47-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="b5e47-107">Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke.</span><span class="sxs-lookup"><span data-stu-id="b5e47-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="b5e47-108">**Rettelse** : Annuller installationen, og brug et miljø med høj tilgængelighed, niveau 2 eller højere (ikke et Onebox-miljø).</span><span class="sxs-lookup"><span data-stu-id="b5e47-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="b5e47-109">Planlægning af batchjob mislykkes, når planlægningsoptimering er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b5e47-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="b5e47-110">Når du aktiverer Planlægningsoptimering, deaktiveres det indbyggede varedisponeringsprogram automatisk.</span><span class="sxs-lookup"><span data-stu-id="b5e47-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="b5e47-111">Varedisponeringsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management mislykkes, hvis de udløses, når Planlægningsoptimering er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b5e47-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="b5e47-112">Der vises muligvis en fejlmeddelelse, f.eks. *Denne handling har udløst varedisponering, der ikke understøttes, når Planlægningsoptimering er aktiveret*.</span><span class="sxs-lookup"><span data-stu-id="b5e47-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="b5e47-113">**Rettelse** : Annuller alle varedisponeringsbatchjob, der blev oprettet for det indbyggede planlægningsprogram for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b5e47-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="b5e47-114">Resultater fra Planlægningsoptimering adskiller sig fra tidligere resultater.</span><span class="sxs-lookup"><span data-stu-id="b5e47-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="b5e47-115">Planlægningsoptimering adskiller sig fra det indbyggede planlægningsprogramdesign på visse områder.</span><span class="sxs-lookup"><span data-stu-id="b5e47-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="b5e47-116">Dette kan også skyldes ventende funktioner.</span><span class="sxs-lookup"><span data-stu-id="b5e47-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="b5e47-117">**Rettelse**: Kør analyse af tilpasning af planlægningsoptimering, og analysér derefter resultaterne, mens der henvises til den relaterede dokumentation for at forstå virkningen.</span><span class="sxs-lookup"><span data-stu-id="b5e47-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="b5e47-118">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b5e47-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="b5e47-119">Varedisponering overholder ikke disponeringstidshorisonten</span><span class="sxs-lookup"><span data-stu-id="b5e47-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="b5e47-120">Dette skyldes en ventende funktion i Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="b5e47-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="b5e47-121">**Rettelse** : Indtil den ventende funktion er tilgængelig, skal du filtrere eller slette ordreforslag for at fjerne forsyningsforslag uden for disponeringstidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="b5e47-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="b5e47-122">Kan ikke aktivere Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="b5e47-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="b5e47-123">**Forbindelsesstatussen** skal være **tilsluttet**, før du kan angive **Brug planlægningsoptimering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b5e47-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="b5e47-124">Du kan finde flere oplysninger under [Kom i gang med Planlægningsoptimering](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="b5e47-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="b5e47-125">**Rettelse** : Kontroller, at tilføjelsesprogrammet Planlægningsoptimering blev installeret korrekt.</span><span class="sxs-lookup"><span data-stu-id="b5e47-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="b5e47-126">Der vises en fejlmeddelelse under CTP</span><span class="sxs-lookup"><span data-stu-id="b5e47-126">Error message is shown during CTP</span></span>

<span data-ttu-id="b5e47-127">Hvis du prøver at køre ledningsevne (LE) fra en salgsordre, når Planlægningsoptimering er aktiveret, får du vist følgende fejlmeddelelse: *Denne handling har udløst varedisponering, der ikke understøttes, når Planlægningsoptimering er aktiveret*.</span><span class="sxs-lookup"><span data-stu-id="b5e47-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="b5e47-128">Dette er knyttet til en ventende funktion, der er planlagt som en del af understøttelsen af produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="b5e47-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="b5e47-129">**Rettelse:** Undgå LE-beregninger, når Planlægningsoptimering er aktiveret, indtil der er en tilgængelig LE-understøttelse.</span><span class="sxs-lookup"><span data-stu-id="b5e47-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5e47-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b5e47-130">Additional resources</span></span>

[<span data-ttu-id="b5e47-131">Kom i gang med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="b5e47-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="b5e47-132">Analyse af tilpasning af planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="b5e47-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
