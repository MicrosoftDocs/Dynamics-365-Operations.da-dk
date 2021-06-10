---
title: Konfigurere færdigheder
description: Du kan spore arbejderens færdigheder i Dynamics 365 Human Resources. Du kan også angive de færdigheder, der kræves til et bestemt job.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076553"
---
# <a name="configure-skills"></a><span data-ttu-id="00447-104">Konfigurere færdigheder</span><span class="sxs-lookup"><span data-stu-id="00447-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="00447-105">Du kan spore arbejderens færdigheder i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="00447-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="00447-106">Du kan også angive de færdigheder, der kræves til et bestemt job.</span><span class="sxs-lookup"><span data-stu-id="00447-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="00447-107">Eksempler på færdigheder, du kan spore, omfatter:</span><span class="sxs-lookup"><span data-stu-id="00447-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="00447-108">Supervision – evnen til at føre tilsyn med andres arbejde.</span><span class="sxs-lookup"><span data-stu-id="00447-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="00447-109">Ledelse – evnen til at lede medarbejdere og forretningsområder.</span><span class="sxs-lookup"><span data-stu-id="00447-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="00447-110">Planlægning – evnen til at se fremad, formulere visioner og få dem gennemført.</span><span class="sxs-lookup"><span data-stu-id="00447-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="00447-111">HTML – evnen til at skrive HTML-kode.</span><span class="sxs-lookup"><span data-stu-id="00447-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="00447-112">Hvis du ikke allerede har konfigureret færdighedstyper og klassifikationsmodeller, skal du tilføje nogle, før du opretter færdigheder.</span><span class="sxs-lookup"><span data-stu-id="00447-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="00447-113">Følgende personer kan angive færdigheder for en arbejder:</span><span class="sxs-lookup"><span data-stu-id="00447-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="00447-114">Arbejdere kan indtaste færdigheder for sig selv i medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="00447-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="00447-115">Disse færdigheder kræver en leders godkendelse.</span><span class="sxs-lookup"><span data-stu-id="00447-115">These skills require manager approval.</span></span>
- <span data-ttu-id="00447-116">Ledere kan indtaste færdigheder for deres arbejdere.</span><span class="sxs-lookup"><span data-stu-id="00447-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="00447-117">Du kan oprette en arbejdsproces, der automatisk godkender disse færdigheder.</span><span class="sxs-lookup"><span data-stu-id="00447-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="00447-118">Oprette en færdighedstype</span><span class="sxs-lookup"><span data-stu-id="00447-118">Create a skill type</span></span>

<span data-ttu-id="00447-119">Færdighedstyper er kategorier, som individuelle færdigheder hører under, f.eks. Administration eller Salg.</span><span class="sxs-lookup"><span data-stu-id="00447-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="00447-120">I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.</span><span class="sxs-lookup"><span data-stu-id="00447-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="00447-121">Vælg **Kompetencetyper** under **Kompetenceopsætning**.</span><span class="sxs-lookup"><span data-stu-id="00447-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="00447-122">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00447-122">Select **New**.</span></span>

4. <span data-ttu-id="00447-123">Udfyld følgende felter:</span><span class="sxs-lookup"><span data-stu-id="00447-123">Complete the following fields:</span></span>

   - <span data-ttu-id="00447-124">**Færdighedstype**: Angiv et navn til færdighedstypen.</span><span class="sxs-lookup"><span data-stu-id="00447-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="00447-125">**Beskrivelse**: Angiv en beskrivelse af færdighedstypen.</span><span class="sxs-lookup"><span data-stu-id="00447-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="00447-126">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00447-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="00447-127">Oprette en rangeringsmodel</span><span class="sxs-lookup"><span data-stu-id="00447-127">Create a rating model</span></span>

<span data-ttu-id="00447-128">Rangeringsmodeller er en hjælp til at evaluere en persons faktiske færdighedsniveau, det niveau de skal tilsigte, eller det færdighedsniveau, der kræves til et job.</span><span class="sxs-lookup"><span data-stu-id="00447-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="00447-129">Hvert niveau i en klassifikationsmodel er tildelt en faktor.</span><span class="sxs-lookup"><span data-stu-id="00447-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="00447-130">I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.</span><span class="sxs-lookup"><span data-stu-id="00447-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="00447-131">Vælg **Rangeringsmodeller** under **Opsætning af kompetence**.</span><span class="sxs-lookup"><span data-stu-id="00447-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="00447-132">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00447-132">Select **New**.</span></span>

4. <span data-ttu-id="00447-133">Udfyld følgende felter:</span><span class="sxs-lookup"><span data-stu-id="00447-133">Complete the following fields:</span></span>

   - <span data-ttu-id="00447-134">**Rangering**: Angiv et navn til rangeringsmodellen, **Færdigheder**.</span><span class="sxs-lookup"><span data-stu-id="00447-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="00447-135">**Beskrivelse**: Angiv en beskrivelse af rangeringsmodellen, f.eks. **Færdighedsrangering**.</span><span class="sxs-lookup"><span data-stu-id="00447-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="00447-136">Vælg **Ny** i sektionen **Niveauer**.</span><span class="sxs-lookup"><span data-stu-id="00447-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="00447-137">For hvert niveau, du vil tilføje, skal du udfylde følgende felter:</span><span class="sxs-lookup"><span data-stu-id="00447-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="00447-138">**Niveau**: Angiv et navn til niveauet.</span><span class="sxs-lookup"><span data-stu-id="00447-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="00447-139">**Beskrivelse**: Angiv en beskrivelse af niveauet.</span><span class="sxs-lookup"><span data-stu-id="00447-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="00447-140">**Faktor**: Angiv en faktorværdi fra 0-9.</span><span class="sxs-lookup"><span data-stu-id="00447-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="00447-141">Faktorer hjælper med at normalisere resultaterne af færdigheder, der bruger forskellige rangeringsmodeller.</span><span class="sxs-lookup"><span data-stu-id="00447-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="00447-142">Hvert niveau skal have en entydig faktor.</span><span class="sxs-lookup"><span data-stu-id="00447-142">Each level must have a unique factor.</span></span> <span data-ttu-id="00447-143">Niveauer med højere faktorværdier vægter mere i rangeringsmodellen.</span><span class="sxs-lookup"><span data-stu-id="00447-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="00447-144">Fortsæt med at tilføje niveauer efter behov.</span><span class="sxs-lookup"><span data-stu-id="00447-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="00447-145">Du kan angive op til ti niveauer for hver rangeringsmodel.</span><span class="sxs-lookup"><span data-stu-id="00447-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="00447-146">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00447-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="00447-147">Oprette en færdighed</span><span class="sxs-lookup"><span data-stu-id="00447-147">Create a skill</span></span>

<span data-ttu-id="00447-148">Før du kan tildele en færdighed eller oprette en færdighedssøgning eller en færdighedsprofil, skal du angive oplysninger om færdighederne på siden **Færdigheder**.</span><span class="sxs-lookup"><span data-stu-id="00447-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="00447-149">Du kan vælge en færdighedstype og en rangeringsmodel for hver færdighed.</span><span class="sxs-lookup"><span data-stu-id="00447-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="00447-150">I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.</span><span class="sxs-lookup"><span data-stu-id="00447-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="00447-151">Vælg **Færdigheder** under **Kompetenceopsætning**.</span><span class="sxs-lookup"><span data-stu-id="00447-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="00447-152">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00447-152">Select **New**.</span></span>

4. <span data-ttu-id="00447-153">Udfyld følgende felter:</span><span class="sxs-lookup"><span data-stu-id="00447-153">Complete the following fields:</span></span>

   - <span data-ttu-id="00447-154">**Færdighed**: Angiv et navn til færdigheden.</span><span class="sxs-lookup"><span data-stu-id="00447-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="00447-155">**Beskrivelse**: Angiv en beskrivelse af færdigheden.</span><span class="sxs-lookup"><span data-stu-id="00447-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="00447-156">**Rangering**: Vælg den rangeringsmodel, som du vil bruge til denne færdighed.</span><span class="sxs-lookup"><span data-stu-id="00447-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="00447-157">**Færdighedstype** : Vælg på listen over færdighedstyper.</span><span class="sxs-lookup"><span data-stu-id="00447-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="00447-158">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00447-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="00447-159">Se også</span><span class="sxs-lookup"><span data-stu-id="00447-159">See also</span></span>

[<span data-ttu-id="00447-160">Angive færdigheder</span><span class="sxs-lookup"><span data-stu-id="00447-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="00447-161">Tilknytte færdigheder</span><span class="sxs-lookup"><span data-stu-id="00447-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]