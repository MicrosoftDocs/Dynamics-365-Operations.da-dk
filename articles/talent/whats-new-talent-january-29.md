---
title: Nyheder eller ændringer i Dynamics 365 Talent (31. januar 2019)
description: I dette emne beskrives funktioner, der er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690046"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="7529f-103">Nyheder eller ændringer i Dynamics 365 Talent (31. januar 2019)</span><span class="sxs-lookup"><span data-stu-id="7529f-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="7529f-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="7529f-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="7529f-105">**Build 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="7529f-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="7529f-106">Ændringer af Core HR</span><span class="sxs-lookup"><span data-stu-id="7529f-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="7529f-107">Fridage, der er brugt på orlovskort, tager ikke datoer i orlovsplan i betragtning</span><span class="sxs-lookup"><span data-stu-id="7529f-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="7529f-108">For orlovsplaner, der ikke følger et kalenderår, viser kortet **Taget** nu fridage, der er anvendt i det orlovsår, der er defineret i planen.</span><span class="sxs-lookup"><span data-stu-id="7529f-108">For leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="7529f-109">Hvis en organisations orlovsår f.eks. går fra 1. juni til 30. maj, og en medarbejder har taget tre dage i december, viser kortet **Taget** 3 dage den 15. januar.</span><span class="sxs-lookup"><span data-stu-id="7529f-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken three days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="7529f-110">Periodiserede beløb, der ikke svarer til datogrundlaget for niveauet</span><span class="sxs-lookup"><span data-stu-id="7529f-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="7529f-111">Der er føjet nye indstillinger til orlov og fravær (**Personale** parametre) for at gøre det muligt for kunder at bestemme, hvornår medarbejdernes dato for Måneders tjeneste er gældende.</span><span class="sxs-lookup"><span data-stu-id="7529f-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="7529f-112">Datoen er slutningen af måneden for visse organisationer, men for andre kan det være starten af den efterfølgende måned.</span><span class="sxs-lookup"><span data-stu-id="7529f-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="7529f-113">F.eks. kan én organisation bevilge fridage fra d. 31. december, mens en anden gør det fra den 1. januar.</span><span class="sxs-lookup"><span data-stu-id="7529f-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="7529f-114">Med denne indstilling kan du vælge, hvornår bevillingen skal ske.</span><span class="sxs-lookup"><span data-stu-id="7529f-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="7529f-115">Arbejderansættelseshandlinger går i stå i "Arbejdsgang er fuldført"-tilstand</span><span class="sxs-lookup"><span data-stu-id="7529f-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="7529f-116">Der er foretaget ændringer til løsningen af et problem, hvor et lille antal arbejdsgange sluttede med statussen "Arbejdsgang er fuldført".</span><span class="sxs-lookup"><span data-stu-id="7529f-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="7529f-117">Nye arbejdsgange skal nu flyttes til tilstanden "Fuldført", når arbejdsgangen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="7529f-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="7529f-118">Arbejdsgange i en Arbejdsgang afsluttet-status, overflyttes til en fejlstatus for at tillade opdatering eller fjernelse, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="7529f-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
