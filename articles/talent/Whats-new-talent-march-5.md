---
title: Nyheder eller ændringer i Dynamics 365 Talent (5. marts 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 115d7cd3d71eaddce2434cb1939c503d36bccdf8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527284"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="97d2b-103">Nyheder eller ændringer i Dynamics 365 Talent (5. marts 2019)</span><span class="sxs-lookup"><span data-stu-id="97d2b-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="97d2b-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.</span><span class="sxs-lookup"><span data-stu-id="97d2b-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="97d2b-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="97d2b-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="97d2b-106">Udvide grupperede indstillinger i Attract</span><span class="sxs-lookup"><span data-stu-id="97d2b-106">Extending option sets in Attract</span></span>

<span data-ttu-id="97d2b-107">I Attract er der adskillige felter, som er grupperede indstillinger, i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="97d2b-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="97d2b-108">Der er indført nye funktioner til udvidelse af grupperede indstillinger, startende med felterne **Årsag til afvisning**, **Medarbejdertype** og **Anciennitetstype**.</span><span class="sxs-lookup"><span data-stu-id="97d2b-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97d2b-109">Funktionen til jobopslag på LinkedIn kræver brug af felterne **Medarbejdertype** og **Anciennitetstype** på siden **Jobdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="97d2b-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="97d2b-110">Standardværdierne i disse felter understøttes af LinkedIn og vises, når jobbet er opslået.</span><span class="sxs-lookup"><span data-stu-id="97d2b-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="97d2b-111">Hvis du laver jobopslag på LinkedIn, og du ændrer de eksisterende værdier for disse felter med grupperede indstillinger, bliver jobbet opslået, men LinkedIn viser ikke de brugerdefinerede værdier i **Medarbejdertype** og **Anciennitetstype**.</span><span class="sxs-lookup"><span data-stu-id="97d2b-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="97d2b-112">Ændringer i Onboarding</span><span class="sxs-lookup"><span data-stu-id="97d2b-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="97d2b-113">Privat prøveversion til Onboard-teams</span><span class="sxs-lookup"><span data-stu-id="97d2b-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="97d2b-114">Du kan nu nemt dele og samarbejde om skabeloner på tværs af hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="97d2b-115">Yderligere oplysninger finder du i [Dele de bedste fremgangsmåder på tværs af organisationen ved hjælp af Onboard-teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="97d2b-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="97d2b-116">Privat prøveversion med pladsholdere for modtagere</span><span class="sxs-lookup"><span data-stu-id="97d2b-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="97d2b-117">Du kan forbedre dine skabeloner ved at tildele aktiviteter til roller i stedet for personer.</span><span class="sxs-lookup"><span data-stu-id="97d2b-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="97d2b-118">Roller tildeles derefter til personer på tidspunktet for oprettelse af guiden.</span><span class="sxs-lookup"><span data-stu-id="97d2b-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="97d2b-119">Yderligere oplysninger finder du i [Strømline guideadministration ved at tildele aktiviteter til roller](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="97d2b-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="97d2b-120">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="97d2b-120">Changes in Core HR</span></span>
<span data-ttu-id="97d2b-121">**Build 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="97d2b-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="97d2b-122">Konfigurere arbejdsgang til automatisk at godkende eller følge arbejdsgang, når en personale- eller linjechef sender eller opdaterer anmodninger om fridage</span><span class="sxs-lookup"><span data-stu-id="97d2b-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="97d2b-123">Nye betingelser for arbejdsgange er tilføjet for at tillade, at anmodninger om fridage godkendes automatisk, hvis de sendes af en medarbejders chef eller af personaleafdelingen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="97d2b-124">Én måde at opnå denne automatiske godkendelse i en arbejdsgang er gennem aktivering af en automatisk handling under godkendelsen af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="97d2b-125">De poster, som er medtaget, omfatter:</span><span class="sxs-lookup"><span data-stu-id="97d2b-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="97d2b-126">Sendt af - Bruges til at evaluere systembruger-id'et for den bruger, der har sendt anmodningen til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="97d2b-127">Sendt på vegne af - Bruges til at vurdere, om orlovsanmodningen er sendt på vegne af den arbejder, der er knyttet til anmodningen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="97d2b-128">Sendt af Personale - Bruges til at vurdere, om den systembruger, der har sendt anmodningen til arbejdsgangen, har en Personale-rolle.</span><span class="sxs-lookup"><span data-stu-id="97d2b-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="97d2b-129">Sendt af chef – Bruges til at vurdere, om den bruger, der sendte orlovsanmodningen til arbejdsgangen, er leder af linjehierarkiet for den arbejder, der er knyttet til anmodningen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="97d2b-130">Muliggøre fast medarbejderløn for fremtidige stillingstildelinger</span><span class="sxs-lookup"><span data-stu-id="97d2b-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="97d2b-131">Det er almindeligt, at nye medarbejdere i en organisation ansættes med en fremtidig startdato.</span><span class="sxs-lookup"><span data-stu-id="97d2b-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="97d2b-132">Med denne ændring kan fast løn defineres for kommende medarbejdere med fremtidige stillingstildelinger.</span><span class="sxs-lookup"><span data-stu-id="97d2b-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="97d2b-133">Lønfelter for stillingen er tomme, når du redigerer stillingen</span><span class="sxs-lookup"><span data-stu-id="97d2b-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="97d2b-134">Med denne ændring får lønfelterne nu de aktuelle standardværdier, når der anmodes om ændringer af eksisterende stillinger.</span><span class="sxs-lookup"><span data-stu-id="97d2b-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="97d2b-135">Diverse andre fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="97d2b-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="97d2b-136">Andre mindre fejlrettelser er medtaget i denne version.</span><span class="sxs-lookup"><span data-stu-id="97d2b-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="97d2b-137">Opgrader til Common Data Service</span><span class="sxs-lookup"><span data-stu-id="97d2b-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="97d2b-138">Fristerne for at opgradere til Common Data Service nærmer sig med hastige skridt.</span><span class="sxs-lookup"><span data-stu-id="97d2b-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="97d2b-139">Log på Power Apps Administration for at finde ud af, om din database skal opgraderes.</span><span class="sxs-lookup"><span data-stu-id="97d2b-139">Sign in to the Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="97d2b-140">Du kan finde flere oplysninger om frister og de nødvendige trin for at opgradere under [Opgrader til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="97d2b-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="97d2b-141">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="97d2b-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="97d2b-142">Avanceret lønsikkerhed (fast og variabel)</span><span class="sxs-lookup"><span data-stu-id="97d2b-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="97d2b-143">I mange organisationer har chefer for løn og frynsegoder kun har adgang til bestemte lønposter, f.eks. poster, der er beregnet til ledere eller medarbejdere i bestemte områder.</span><span class="sxs-lookup"><span data-stu-id="97d2b-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="97d2b-144">Med denne ændring kan du administrere og vedligeholde lønstrukturer for forskellige medarbejdergrupper i organisationen.</span><span class="sxs-lookup"><span data-stu-id="97d2b-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="97d2b-145">faste og variable strukturer kan tildeles til sikkerhedsroller, som bestemmer adgangen til strukturerne og de medarbejderdata, der er knyttet til strukturerne, f.eks. løn- eller bonusposter.</span><span class="sxs-lookup"><span data-stu-id="97d2b-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="97d2b-146">Kun roller med den givne adgang kan behandle løn for de pågældende medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="97d2b-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="97d2b-147">Platform update 24 til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="97d2b-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="97d2b-148">Yderligere oplysninger om Platform update 24 til Finance and Operations finder du i [Nyheder eller ændringer i Finance and Operations Platform update 24 (marts 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="97d2b-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
