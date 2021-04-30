---
title: Adgangsrettigheder for controllere til omkostningsobjekt
description: Dette emne indeholder oplysninger om adgangsrettigheder for controllere til omkostningsobjekter.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897618"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="fb20b-103">Adgangsrettigheder for controllere til omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="fb20b-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb20b-104">Arbejdsområdet **Omkostningsstyring** er et centralt punkt, hvor ledere kan få vist performance for deres omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="fb20b-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="fb20b-105">I dette arbejdsområde kan ledere bruge omkostningsregnskabsdata, selvom de ikke er bogholdere.</span><span class="sxs-lookup"><span data-stu-id="fb20b-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="fb20b-106">Ledere skal af sikkerhedsmæssige årsager kun have adgang til at se de omkostningsregnskabsdata, der er relateret til de specifikke omkostningsobjekter, som de er ansvarlige for.</span><span class="sxs-lookup"><span data-stu-id="fb20b-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="fb20b-107">Der er fire entydige roller i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="fb20b-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="fb20b-108">Rollenavn</span><span class="sxs-lookup"><span data-stu-id="fb20b-108">Role name</span></span>               | <span data-ttu-id="fb20b-109">Licens</span><span class="sxs-lookup"><span data-stu-id="fb20b-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="fb20b-110">Vedligehold regnskabschef for omkostning</span><span class="sxs-lookup"><span data-stu-id="fb20b-110">Cost accounting manager</span></span> | <span data-ttu-id="fb20b-111">Aktivitet</span><span class="sxs-lookup"><span data-stu-id="fb20b-111">Activity</span></span>     |
| <span data-ttu-id="fb20b-112">Lagerbogholder</span><span class="sxs-lookup"><span data-stu-id="fb20b-112">Cost accountant</span></span>         | <span data-ttu-id="fb20b-113">Operations</span><span class="sxs-lookup"><span data-stu-id="fb20b-113">Operations</span></span>   |
| <span data-ttu-id="fb20b-114">Lagerregnskabsassistent</span><span class="sxs-lookup"><span data-stu-id="fb20b-114">Cost accountant clerk</span></span>   | <span data-ttu-id="fb20b-115">Operations</span><span class="sxs-lookup"><span data-stu-id="fb20b-115">Operations</span></span>   |
| <span data-ttu-id="fb20b-116">Controller til omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="fb20b-116">Cost object controller</span></span>  | <span data-ttu-id="fb20b-117">Teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="fb20b-117">Team members</span></span> |

<span data-ttu-id="fb20b-118">Dette emne forklarer, hvordan du tildeler rollen **Controller til omkostningsobjekt** til en leder.</span><span class="sxs-lookup"><span data-stu-id="fb20b-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="fb20b-119">Når rollen **Controller til omkostningsobjekt** tildeles til en leder, kan lederen udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="fb20b-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="fb20b-120">Få adgang til **Omkostningsstyring**-arbejdsområdet (i klienten).</span><span class="sxs-lookup"><span data-stu-id="fb20b-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="fb20b-121">Få detaljeadgang og adgang til at se de sider, der understøtter detaljeadgangsoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="fb20b-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="fb20b-122">Få adgang til **Omkostningsstyring**-arbejdsområdet (i mobilprogrammet).</span><span class="sxs-lookup"><span data-stu-id="fb20b-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="fb20b-123">Rollen **Controller til omkostningsobjekt** styrer ikke, hvilke omkostningsobjekter brugeren har adgang til og kan få vist data for.</span><span class="sxs-lookup"><span data-stu-id="fb20b-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="fb20b-124">Sikkerheden på rækkeniveau leveres via dimensionshierarkier og adgangslistehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fb20b-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="fb20b-125">Tildele adgangsrettigheder</span><span class="sxs-lookup"><span data-stu-id="fb20b-125">Grant access rights</span></span>
<span data-ttu-id="fb20b-126">Følgende eksempel viser, hvordan et dimensionshierarki kan se ud.</span><span class="sxs-lookup"><span data-stu-id="fb20b-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="fb20b-127">**Detaljer om dimensionshierarki**</span><span class="sxs-lookup"><span data-stu-id="fb20b-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="fb20b-128">Navn på dimensionshierarki</span><span class="sxs-lookup"><span data-stu-id="fb20b-128">Dimension hierarchy name</span></span> | <span data-ttu-id="fb20b-129">Dimension</span><span class="sxs-lookup"><span data-stu-id="fb20b-129">Dimension</span></span>    | <span data-ttu-id="fb20b-130">Navn på dimensionshierarkitype</span><span class="sxs-lookup"><span data-stu-id="fb20b-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="fb20b-131">Adgangslistehierarki</span><span class="sxs-lookup"><span data-stu-id="fb20b-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="fb20b-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="fb20b-132">Organization</span></span>             | <span data-ttu-id="fb20b-133">Bærere</span><span class="sxs-lookup"><span data-stu-id="fb20b-133">Cost centers</span></span> | <span data-ttu-id="fb20b-134">Klassifikationshierarki for dimension</span><span class="sxs-lookup"><span data-stu-id="fb20b-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="fb20b-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="fb20b-135">**Yes**</span></span>               |

<span data-ttu-id="fb20b-136">Du kan bruge oversigtspanelet **Brugere** i hierarkidesigneren til at indsætte et eller flere bruger-id'er på hver node.</span><span class="sxs-lookup"><span data-stu-id="fb20b-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="fb20b-137">Noder</span><span class="sxs-lookup"><span data-stu-id="fb20b-137">Nodes</span></span>                 | <span data-ttu-id="fb20b-138">Brugere</span><span class="sxs-lookup"><span data-stu-id="fb20b-138">Users</span></span>            | <span data-ttu-id="fb20b-139">Fra dimensionsmedlem</span><span class="sxs-lookup"><span data-stu-id="fb20b-139">From dimension member</span></span>     |   <span data-ttu-id="fb20b-140">Til dimensionsmedlem</span><span class="sxs-lookup"><span data-stu-id="fb20b-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="fb20b-141">Organisation</span><span class="sxs-lookup"><span data-stu-id="fb20b-141">Organization</span></span>                      | <span data-ttu-id="fb20b-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="fb20b-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="fb20b-143">&nbsp;&nbsp;Administration</span><span class="sxs-lookup"><span data-stu-id="fb20b-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="fb20b-144">April</span><span class="sxs-lookup"><span data-stu-id="fb20b-144">April</span></span>            |                           |                         |
| <span data-ttu-id="fb20b-145">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="fb20b-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="fb20b-146">Alicia</span><span class="sxs-lookup"><span data-stu-id="fb20b-146">Alicia</span></span>           | <span data-ttu-id="fb20b-147">CC002</span><span class="sxs-lookup"><span data-stu-id="fb20b-147">CC002</span></span>                     | <span data-ttu-id="fb20b-148">CC003</span><span class="sxs-lookup"><span data-stu-id="fb20b-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="fb20b-149">CC007</span><span class="sxs-lookup"><span data-stu-id="fb20b-149">CC007</span></span>                     | <span data-ttu-id="fb20b-150">CC007</span><span class="sxs-lookup"><span data-stu-id="fb20b-150">CC007</span></span>                   |
| <span data-ttu-id="fb20b-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="fb20b-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="fb20b-152">Arnie</span><span class="sxs-lookup"><span data-stu-id="fb20b-152">Arnie</span></span>            | <span data-ttu-id="fb20b-153">CC001</span><span class="sxs-lookup"><span data-stu-id="fb20b-153">CC001</span></span>                     | <span data-ttu-id="fb20b-154">CC001</span><span class="sxs-lookup"><span data-stu-id="fb20b-154">CC001</span></span>                   |
| <span data-ttu-id="fb20b-155">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="fb20b-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="fb20b-156">David</span><span class="sxs-lookup"><span data-stu-id="fb20b-156">David</span></span>            |                           |                         |
| <span data-ttu-id="fb20b-157">&nbsp;&nbsp;&nbsp;&nbsp;Emballage</span><span class="sxs-lookup"><span data-stu-id="fb20b-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="fb20b-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="fb20b-158">Ellen</span></span>            | <span data-ttu-id="fb20b-159">CC005</span><span class="sxs-lookup"><span data-stu-id="fb20b-159">CC005</span></span>                     | <span data-ttu-id="fb20b-160">CC005</span><span class="sxs-lookup"><span data-stu-id="fb20b-160">CC005</span></span>                   |
| <span data-ttu-id="fb20b-161">&nbsp;&nbsp;&nbsp;&nbsp;Samling</span><span class="sxs-lookup"><span data-stu-id="fb20b-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="fb20b-162">Chris</span><span class="sxs-lookup"><span data-stu-id="fb20b-162">Chris</span></span>            | <span data-ttu-id="fb20b-163">CC006</span><span class="sxs-lookup"><span data-stu-id="fb20b-163">CC006</span></span>                     | <span data-ttu-id="fb20b-164">CC006</span><span class="sxs-lookup"><span data-stu-id="fb20b-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="fb20b-165">Bogholdere skal tildeles til det øverste niveau i hierarkiet, så de kan se alle poster i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="fb20b-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="fb20b-166">Før adgangslistehierarkiet og de tilhørende sikkerhedsindstillinger kan anvendes, skal indstillingen **Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt** være indstillet til **Ja** under fanen **Generelt** på siden **Parametre for omkostningsregnskab** (**Omkostningsregnskab** > **Opsætning** > **Parametre**).</span><span class="sxs-lookup"><span data-stu-id="fb20b-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="fb20b-167">Indstillingerne for adgangslistehierarkiet bruges til at styre, hvilke data der vises i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="fb20b-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="fb20b-168">Arbejdsområdet **Omkostningsstyring** (i klienten):</span><span class="sxs-lookup"><span data-stu-id="fb20b-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="fb20b-169">Data på de sider, der bruges til detaljeadgang</span><span class="sxs-lookup"><span data-stu-id="fb20b-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="fb20b-170">Arbejdsområdet **Omkostningsstyring** (i mobilprogrammet):</span><span class="sxs-lookup"><span data-stu-id="fb20b-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="fb20b-171">Saldi i kort</span><span class="sxs-lookup"><span data-stu-id="fb20b-171">Balances in cards</span></span>

- <span data-ttu-id="fb20b-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="fb20b-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="fb20b-173">Data, der vises i Power BI-visualiseringer</span><span class="sxs-lookup"><span data-stu-id="fb20b-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="fb20b-174">Data Power BI-visualiseringer, der er integreret i Dynamics 365 Finance-klienten</span><span class="sxs-lookup"><span data-stu-id="fb20b-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="fb20b-175">Før adgangslistehierarkiet kan påvirke dataene i Power BI, skal adgangslistehierarki og sikkerhed på rækkeniveau i Power BI kombineres.</span><span class="sxs-lookup"><span data-stu-id="fb20b-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="fb20b-176">Du kan finde flere oplysninger i [Konfigurere sikkerhed for indholdspakke til omkostningsregnskab](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="fb20b-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="fb20b-177">I dette emne beskrives de forudsætninger, der skal være opfyldt, før du kan bruge arbejdsområdet **Omkostningsstyring**.</span><span class="sxs-lookup"><span data-stu-id="fb20b-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="fb20b-178">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fb20b-178">Additional resources</span></span>

- [<span data-ttu-id="fb20b-179">Arbejdsområde for omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="fb20b-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="fb20b-180">Dimensionshierarki</span><span class="sxs-lookup"><span data-stu-id="fb20b-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="fb20b-181">Konfigurere sikkerhed for indholdspakke til omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="fb20b-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
