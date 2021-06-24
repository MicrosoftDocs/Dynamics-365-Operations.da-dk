---
title: Angive færdigheder
description: Arbejdere og ledere kan indtaste færdigheder i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5a65f1884ea87bbf2519cc94e4c52a40ac1a91bd
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193971"
---
# <a name="enter-skills"></a><span data-ttu-id="b2d6c-103">Angive færdigheder</span><span class="sxs-lookup"><span data-stu-id="b2d6c-103">Enter skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2d6c-104">Du kan angive målfærdigheder eller reelle færdigheder for arbejdere, ansøgere eller kontakter i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-104">You can enter target skills or actual skills for workers, applicants, or contacts in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b2d6c-105">En målfærdighed er en færdighed, som en person har til hensigt at opnå.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-105">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b2d6c-106">En reel færdighed er en færdighed, som en person har i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-106">An actual skill is a skill that a person currently has.</span></span>

## <a name="create-a-workflow-to-auto-approve-skills"></a><span data-ttu-id="b2d6c-107">Oprette en arbejdsproces, der godkender færdigheder automatisk</span><span class="sxs-lookup"><span data-stu-id="b2d6c-107">Create a workflow to auto-approve skills</span></span>

<span data-ttu-id="b2d6c-108">Hvis du vil angive færdigheder uden at kræve godkendelse, skal du oprette en arbejdsproces for automatisk godkendelse af færdigheder.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-108">To enter skills without requiring approval, you must create a workflow to auto-approve skills.</span></span>

> [!NOTE]
> <span data-ttu-id="b2d6c-109">Færdigheder, der indtastes af arbejdere, kræver altid en leders godkendelse.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-109">Skills entered by workers always require manager approval.</span></span> <span data-ttu-id="b2d6c-110">Denne arbejdsproces godkender kun færdigheder automatisk, hvis de er angivet af ledere på vegne af deres arbejdere.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-110">This workflow only auto-approves skills entered by managers on behalf of their workers.</span></span>

1. <span data-ttu-id="b2d6c-111">Vælg **Links** i arbejdsområdet **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-111">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="b2d6c-112">Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-112">Under **Setup**, select **Human resources workflows**.</span></span>

3. <span data-ttu-id="b2d6c-113">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-113">Select **New**.</span></span>

4. <span data-ttu-id="b2d6c-114">Vælg **Medarbejderfærdigheder** i ruden **Opret arbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-114">In the **Create workflow** pane, select **Worker skills**.</span></span>

   <span data-ttu-id="b2d6c-115">[![Vælg arbejdsprocessen Medarbejderfærdigheder](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span><span class="sxs-lookup"><span data-stu-id="b2d6c-115">[![Select Worker skills workflow](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)</span></span>

5. <span data-ttu-id="b2d6c-116">Vælg **Åbn** i dialogboksen **Åbn denne fil?**</span><span class="sxs-lookup"><span data-stu-id="b2d6c-116">In the **Open this file?** dialogue, select **Open**.</span></span> <span data-ttu-id="b2d6c-117">Indtast dine legitimationsoplysninger, når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-117">When prompted, enter your credentials.</span></span>

6. <span data-ttu-id="b2d6c-118">Vælg arbejdsgangselementet **Godkend færdigheder** i arbejdsproceseditoren, og træk det til lærredet.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-118">In the workflow editor, select the **Approve skills** workflow element and drag it onto the canvas.</span></span>

   <span data-ttu-id="b2d6c-119">[![Vælg arbejdsgangselementet Godkend færdigheder](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span><span class="sxs-lookup"><span data-stu-id="b2d6c-119">[![Select Approve skills workflow element](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)</span></span>

7. <span data-ttu-id="b2d6c-120">Knyt elementet **Start** til elementet **Godkend færdigheder 1**, og knyt derefter elementet **Godkend færdigheder 1** til elementet **Slut**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-120">Connect the **Start** element to the **Approve skills 1** element, and then connect the **Approve skills 1** element to the **End** element.</span></span> <span data-ttu-id="b2d6c-121">Du skal muligvis rulle ned for at se elementet **Slut**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-121">You might need to scroll down to see the **End** element.</span></span> <span data-ttu-id="b2d6c-122">Du kan trække det tættere på de andre elementer.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-122">You can drag it closer to the other elements.</span></span>

   <span data-ttu-id="b2d6c-123">[![Tilknyt arbejdsgangselementer](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span><span class="sxs-lookup"><span data-stu-id="b2d6c-123">[![Connect workflow elements](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)</span></span>

8. <span data-ttu-id="b2d6c-124">Dobbeltklik på arbejdsgangselementet **Godkend færdigheder 1**, og højreklik derefter på elementet **Trin 1**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-124">Double-click the **Approve skills 1** workflow element, and then right-click the **Step 1** element.</span></span> <span data-ttu-id="b2d6c-125">Højreklik på elementet **Trin 1**, og vælg derefter **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-125">Right-click the **Step 1** element, and then select **Properties**.</span></span>

9. <span data-ttu-id="b2d6c-126">Vælg **Betingelse** på navigationslinjen til venstre i vinduet **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-126">In the **Properties** window, select **Condition** on the left-hand nav bar.</span></span>

10. <span data-ttu-id="b2d6c-127">Vælg **Kør kun dette trin, når følgende betingelse er opfyldt**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-127">Select **Run this step only when the following condition is met**.</span></span>

11. <span data-ttu-id="b2d6c-128">Vælg **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-128">Select **Add condition**.</span></span> <span data-ttu-id="b2d6c-129">Vælg **Medarbejders selvbetjeningsfærdigheder** efter **Hvor**, og vælg derefter **Medarbejders selvbetjeningsfærdigheder.Person**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-129">After **Where**, select **Employee self service skills**, and then select **Employee self service skills.Person**.</span></span> <span data-ttu-id="b2d6c-130">Efter **er** skal du vælge **felt** og derefter vælge **Relation mellem bruger og person.Person**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-130">After **is**, select **field**, and then select **User to person relationship.Person**.</span></span>

    <span data-ttu-id="b2d6c-131">[![Angiv betingelse](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span><span class="sxs-lookup"><span data-stu-id="b2d6c-131">[![Specify condition](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)</span></span>

12. <span data-ttu-id="b2d6c-132">Vælg **Tildeling** på navigationslinjen til venstre.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-132">Select **Assignment** on the left-hand nav bar.</span></span>

13. <span data-ttu-id="b2d6c-133">Vælg **Hierarki** under fanen **Tildelingstype**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-133">On the **Assignment type** tab, select **Hierarchy**.</span></span>

14. <span data-ttu-id="b2d6c-134">Vælg **Ledelseshierarki** i feltet **Hierarkitype:** under fanen **Valg af hierarki**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-134">On the **Hierarchy selection** tab, in the **Hierarchy type:** field, select **Managerial hierarchy**.</span></span>

    <span data-ttu-id="b2d6c-135">[![Angiv ledelseshierarki](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span><span class="sxs-lookup"><span data-stu-id="b2d6c-135">[![Specify managerial hierarchy](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)</span></span>

15. <span data-ttu-id="b2d6c-136">Vælg **Luk**, vælg **Arbejdsproces** i brødkrummen på lærredet, og vælg derefter **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-136">Select **Close**, select **Workflow** in the canvas breadcrumb, and then select **Save and close**.</span></span>

<span data-ttu-id="b2d6c-137">Yderligere oplysninger om oprettelse af arbejdsprocesser finder du i [Oversigt over arbejdsgangssystem](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b2d6c-137">For more information about creating workflows, see [Workflow system overview](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).</span></span>

## <a name="enter-skills-for-a-worker"></a><span data-ttu-id="b2d6c-138">Angive færdigheder for en arbejder</span><span class="sxs-lookup"><span data-stu-id="b2d6c-138">Enter skills for a worker</span></span>

1. <span data-ttu-id="b2d6c-139">Vælg en arbejder.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-139">Select a worker.</span></span>

2. <span data-ttu-id="b2d6c-140">Vælg **Person** på handlingslinjen på siden **Arbejder**, og vælg derefter **Færdigheder**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-140">In the action bar of the **Worker** page, select **Person**, and then select **Skills**.</span></span>

3. <span data-ttu-id="b2d6c-141">Udfyld følgende felter for hver færdighed på siden **Færdigheder**:</span><span class="sxs-lookup"><span data-stu-id="b2d6c-141">On the **Skills** page, complete the following fields for each skill:</span></span>

   - <span data-ttu-id="b2d6c-142">**Færdighed**: Vælg en færdighed.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-142">**Skill**: Select a skill.</span></span>
   - <span data-ttu-id="b2d6c-143">**Niveautype**: Vælg **Faktisk** for en færdighed, som arbejderen allerede har, eller vælg **Mål** for en færdighed, som arbejderen arbejder hen imod.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-143">**Level type**: Select **Actual** for a skill the worker already has, or select **Target** for a skill the worker is working toward.</span></span>
   - <span data-ttu-id="b2d6c-144">**Niveau**: Vælg et niveau for arbejderens færdighed.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-144">**Level**: Select a level for the worker's skill.</span></span>
   - <span data-ttu-id="b2d6c-145">**Niveaudato**: Vælg en dato i kalenderværktøjet.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-145">**Level date**: Select a date in the calendar tool.</span></span>
   - <span data-ttu-id="b2d6c-146">**Eksaminator**: Vælg eventuelt en eksaminator på listen.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-146">**Examiner**: If appropriate, select an examiner from the list.</span></span> <span data-ttu-id="b2d6c-147">Du kan filtrere søgningen.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-147">You can filter your search.</span></span>
   - <span data-ttu-id="b2d6c-148">**Års erfaring**: Indtast års erfaring.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-148">**Years of experience**: Enter years of experience.</span></span>
   - <span data-ttu-id="b2d6c-149">**Bekræftet**: Hvis færdigheden er bekræftet, skal du markere afkrydsningsfeltet.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-149">**Verified**: If the skill is verified, check the box.</span></span>
   - <span data-ttu-id="b2d6c-150">**Bekræftet af**: Angiv navnet på den person, der har bekræftet.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-150">**Verified by**: Enter the name of the verifier.</span></span>

4. <span data-ttu-id="b2d6c-151">Når du er færdig med at indtaste færdigheder, skal du vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b2d6c-151">When you're done entering skills, select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2d6c-152">Se også</span><span class="sxs-lookup"><span data-stu-id="b2d6c-152">See also</span></span>

[<span data-ttu-id="b2d6c-153">Konfigurere færdigheder</span><span class="sxs-lookup"><span data-stu-id="b2d6c-153">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="b2d6c-154">Tilknytte færdigheder</span><span class="sxs-lookup"><span data-stu-id="b2d6c-154">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]