---
title: Tilknytte færdigheder
description: Du kan oprette en færdighedssøgning for at finde en kvalificeret person i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076583"
---
# <a name="map-skills"></a><span data-ttu-id="9d55b-103">Tilknytte færdigheder</span><span class="sxs-lookup"><span data-stu-id="9d55b-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9d55b-104">Du kan oprette en færdighedssøgning for at finde en kvalificeret person i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9d55b-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9d55b-105">Færdighedssøgninger søger efter returresultater for kriterier, du angiver, ved at gennemse følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="9d55b-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="9d55b-106">Færdigheder</span><span class="sxs-lookup"><span data-stu-id="9d55b-106">Skills</span></span>
- <span data-ttu-id="9d55b-107">Uddannelser</span><span class="sxs-lookup"><span data-stu-id="9d55b-107">Education</span></span>
- <span data-ttu-id="9d55b-108">Certifikater</span><span class="sxs-lookup"><span data-stu-id="9d55b-108">Certificates</span></span>
- <span data-ttu-id="9d55b-109">Stillinger</span><span class="sxs-lookup"><span data-stu-id="9d55b-109">Positions</span></span>
- <span data-ttu-id="9d55b-110">Projekterfaring</span><span class="sxs-lookup"><span data-stu-id="9d55b-110">Project experience</span></span>

<span data-ttu-id="9d55b-111">Du kan for eksempel finde personer i organisationen, der har optjent deres CPA.</span><span class="sxs-lookup"><span data-stu-id="9d55b-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="9d55b-112">Ved hjælp af kompetencesøgningsprofiler kan du finde aktuelle medarbejdere eller ansøgere med kvalifikationer, der svarer direkte til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="9d55b-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="9d55b-113">Det er kun arbejdere, ansøgere og kontaktpersoner, som du har valgt til at indgå i kompetencesøgninger, der vises på en resultatliste for færdighedssøgning eller indgår i en færdighedsprofil.</span><span class="sxs-lookup"><span data-stu-id="9d55b-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="9d55b-114">Hvis du vil medtage en person i færdighedssøgninger, skal du angive **Medtag i kompetencetilknytning** til **Ja** på de følgende sider:</span><span class="sxs-lookup"><span data-stu-id="9d55b-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="9d55b-115">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="9d55b-115">Worker</span></span><br>
> - <span data-ttu-id="9d55b-116">Medarbejder</span><span class="sxs-lookup"><span data-stu-id="9d55b-116">Employee</span></span><br>
> - <span data-ttu-id="9d55b-117">Ansøger</span><span class="sxs-lookup"><span data-stu-id="9d55b-117">Applicant</span></span><br>
> - <span data-ttu-id="9d55b-118">Kontakter</span><span class="sxs-lookup"><span data-stu-id="9d55b-118">Contacts</span></span><br>

<span data-ttu-id="9d55b-119">Hvis du vil oprette en færdighedssøgning, skal du gå til **Medarbejderudvikling > Links > Kompetencesøgning**.</span><span class="sxs-lookup"><span data-stu-id="9d55b-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="9d55b-120">Hvis du vil oprette en færdighedssøgningsprofil, skal du gå til **Medarbejderudvikling > Links > Kompetencesøgningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="9d55b-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="9d55b-121">Analyse af kompetencekløft og kompetenceprofilanalyse</span><span class="sxs-lookup"><span data-stu-id="9d55b-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="9d55b-122">Du kan oprette en færdighedsprofilanalyse for at få vist en liste over en persons kompetencer.</span><span class="sxs-lookup"><span data-stu-id="9d55b-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="9d55b-123">Du kan oprette en analyse af kompetencekløft for at sammenligne en persons færdigheder med de færdigheder, der kræves til et job.</span><span class="sxs-lookup"><span data-stu-id="9d55b-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="9d55b-124">Hvis du vil oprette en analyse af kløften, skal du gå til **Medarbejderudvikling > Links > Job til analyse af kompetencekløft - person**.</span><span class="sxs-lookup"><span data-stu-id="9d55b-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="9d55b-125">Hvis du vil oprette en analyse af en færdighedsprofil, skal du gå til **Medarbejderudvikling > Links > Analyse af kompetenceprofil**.</span><span class="sxs-lookup"><span data-stu-id="9d55b-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d55b-126">Se også</span><span class="sxs-lookup"><span data-stu-id="9d55b-126">See also</span></span>

[<span data-ttu-id="9d55b-127">Konfigurere færdigheder</span><span class="sxs-lookup"><span data-stu-id="9d55b-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="9d55b-128">Angive færdigheder</span><span class="sxs-lookup"><span data-stu-id="9d55b-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]