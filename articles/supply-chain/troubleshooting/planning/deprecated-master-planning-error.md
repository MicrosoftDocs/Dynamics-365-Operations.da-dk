---
title: Du får vist en fejlmeddelelse, når du kører det indbyggede program til varedisponering
description: Når du kører det udgåede program til varedisponering, får du vist en fejlmeddelelse.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294039"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="7d699-103">Du får vist en fejlmeddelelse, når du kører det indbyggede program til varedisponering</span><span class="sxs-lookup"><span data-stu-id="7d699-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="7d699-104">Fejlkode: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="7d699-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="7d699-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7d699-105">Symptoms</span></span>

<span data-ttu-id="7d699-106">Når du kører varedisponering ved hjælp af det udgåede program til varedisponering, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="7d699-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="7d699-107">Du får vist denne fejlmeddelelse, fordi det indbyggede varedisponeringsprogram blev brugt til scenarier, der understøttes af Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="7d699-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="7d699-108">Du bør migrere til Planlægningsoptimering nu, da den aktuelt indbyggede varedisponering udfases.</span><span class="sxs-lookup"><span data-stu-id="7d699-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="7d699-109">Bemærk, at denne varedisponeringskørsel blev fuldført korrekt.</span><span class="sxs-lookup"><span data-stu-id="7d699-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="7d699-110">Hvis din migrering har en stærk afhængighed i forhold til ventende funktioner, kan du anmode om en undtagelse for fortsat at bruge det indbyggede varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="7d699-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="7d699-111">Udfyld følgende spørgeskema for at komme i gang, og hvis det er relevant, skal du anmode om en undtagelse fra migrering til Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="7d699-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="7d699-112">Spørgeskema om migrering til og undtagelse for Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="7d699-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="7d699-113">Årsag</span><span class="sxs-lookup"><span data-stu-id="7d699-113">Cause</span></span>

<span data-ttu-id="7d699-114">Hvis du kører planlægning, og du ikke bruger funktioner til produktionsstyring, bør du overveje at migrere til Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="7d699-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="7d699-115">Det indbyggede program til varedisponering udfases.</span><span class="sxs-lookup"><span data-stu-id="7d699-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="7d699-116">Så hvis du vil fortsætte med at bruge det uden at modtage fejlmeddelelsen, skal du ansøge om en undtagelse fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d699-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="7d699-117">Løsning</span><span class="sxs-lookup"><span data-stu-id="7d699-117">Resolution</span></span>

<span data-ttu-id="7d699-118">Du kan finde flere oplysninger om, hvordan du migrerer til Planlægningsoptimering, eller hvordan du ansøger om en undtagelse, så du fortsat kan bruge det udgåede indbyggede planlægningsprogram i stedet, i [Migrering til planlægningsoptimering for varedisponering](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="7d699-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
