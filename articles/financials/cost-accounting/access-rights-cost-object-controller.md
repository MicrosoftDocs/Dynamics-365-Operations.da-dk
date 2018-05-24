---
title: Angive adgangsrettigheder for controllere til omkostningsobjekt
description: Dette emne indeholder oplysninger om adgangsrettigheder for controllere til omkostningsobjekter.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1cac3c3b724dda4ab39a65aa5221eda427767eb8
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="2d883-103">Adgangsrettigheder for en controller til et omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="2d883-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d883-104">Arbejdsområdet **Omkostningsstyring** er et centralt punkt, hvor ledere kan få vist performance for deres omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="2d883-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="2d883-105">I dette arbejdsområde kan ledere bruge omkostningsregnskabsdata, selvom de ikke er bogholdere.</span><span class="sxs-lookup"><span data-stu-id="2d883-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="2d883-106">Ledere skal af sikkerhedsmæssige årsager kun have adgang til at se de omkostningsregnskabsdata, der er relateret til de specifikke omkostningsobjekter, som de er ansvarlige for.</span><span class="sxs-lookup"><span data-stu-id="2d883-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="2d883-107">Der er fire entydige roller i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="2d883-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="2d883-108">Rollenavn</span><span class="sxs-lookup"><span data-stu-id="2d883-108">Role name</span></span>               | <span data-ttu-id="2d883-109">Licens</span><span class="sxs-lookup"><span data-stu-id="2d883-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="2d883-110">Vedligehold regnskabschef for omkostning</span><span class="sxs-lookup"><span data-stu-id="2d883-110">Cost accounting manager</span></span> | <span data-ttu-id="2d883-111">Aktivitet</span><span class="sxs-lookup"><span data-stu-id="2d883-111">Activity</span></span>     |
| <span data-ttu-id="2d883-112">Lagerbogholder</span><span class="sxs-lookup"><span data-stu-id="2d883-112">Cost accountant</span></span>         | <span data-ttu-id="2d883-113">Operations</span><span class="sxs-lookup"><span data-stu-id="2d883-113">Operations</span></span>   |
| <span data-ttu-id="2d883-114">Lagerregnskabsassistent</span><span class="sxs-lookup"><span data-stu-id="2d883-114">Cost accountant clerk</span></span>   | <span data-ttu-id="2d883-115">Operations</span><span class="sxs-lookup"><span data-stu-id="2d883-115">Operations</span></span>   |
| <span data-ttu-id="2d883-116">Controller til omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="2d883-116">Cost object controller</span></span>  | <span data-ttu-id="2d883-117">Teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="2d883-117">Team members</span></span> |

<span data-ttu-id="2d883-118">Dette emne forklarer, hvordan du tildeler rollen **Controller til omkostningsobjekt** til en leder.</span><span class="sxs-lookup"><span data-stu-id="2d883-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="2d883-119">Når rollen **Controller til omkostningsobjekt** tildeles til en leder, kan lederen udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="2d883-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="2d883-120">Få adgang til **Omkostningsstyring**-arbejdsområdet (i klienten).</span><span class="sxs-lookup"><span data-stu-id="2d883-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="2d883-121">Få detaljeadgang og adgang til at se de sider, der understøtter detaljeadgangsoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="2d883-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="2d883-122">Få adgang til **Omkostningsstyring**-arbejdsområdet (i mobilprogrammet).</span><span class="sxs-lookup"><span data-stu-id="2d883-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="2d883-123">Rollen **Controller til omkostningsobjekt** styrer ikke, hvilke omkostningsobjekter brugeren har adgang til og kan få vist data for.</span><span class="sxs-lookup"><span data-stu-id="2d883-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="2d883-124">Sikkerheden på rækkeniveau leveres via dimensionshierarkier og adgangslistehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="2d883-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="2d883-125">Tildele adgangsrettigheder</span><span class="sxs-lookup"><span data-stu-id="2d883-125">Grant access rights</span></span>
<span data-ttu-id="2d883-126">Følgende eksempel viser, hvordan et dimensionshierarki kan se ud.</span><span class="sxs-lookup"><span data-stu-id="2d883-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="2d883-127">**Detaljer om dimensionshierarki**</span><span class="sxs-lookup"><span data-stu-id="2d883-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="2d883-128">Navn på dimensionshierarki</span><span class="sxs-lookup"><span data-stu-id="2d883-128">Dimension hierarchy name</span></span> | <span data-ttu-id="2d883-129">Dimension</span><span class="sxs-lookup"><span data-stu-id="2d883-129">Dimension</span></span>    | <span data-ttu-id="2d883-130">Navn på dimensionshierarkitype</span><span class="sxs-lookup"><span data-stu-id="2d883-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="2d883-131">Adgangslistehierarki</span><span class="sxs-lookup"><span data-stu-id="2d883-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="2d883-132">Organisation</span><span class="sxs-lookup"><span data-stu-id="2d883-132">Organization</span></span>             | <span data-ttu-id="2d883-133">Bærere</span><span class="sxs-lookup"><span data-stu-id="2d883-133">Cost centers</span></span> | <span data-ttu-id="2d883-134">Klassifikationshierarki for dimension</span><span class="sxs-lookup"><span data-stu-id="2d883-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="2d883-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="2d883-135">**Yes**</span></span>               |

<span data-ttu-id="2d883-136">Du kan bruge oversigtspanelet **Brugere** i hierarkidesigneren til at indsætte et eller flere bruger-id'er på hver node.</span><span class="sxs-lookup"><span data-stu-id="2d883-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="2d883-137">Brugere</span><span class="sxs-lookup"><span data-stu-id="2d883-137">Users</span></span>            | <span data-ttu-id="2d883-138">Intervaller for dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="2d883-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="2d883-139">**Noder**</span><span class="sxs-lookup"><span data-stu-id="2d883-139">**Nodes**</span></span>                         | <span data-ttu-id="2d883-140">**Bruger-id**</span><span class="sxs-lookup"><span data-stu-id="2d883-140">**User ID**</span></span>      | <span data-ttu-id="2d883-141">**Fra dimensionsmedlem**</span><span class="sxs-lookup"><span data-stu-id="2d883-141">**From dimension member**</span></span> | <span data-ttu-id="2d883-142">**Til dimensionsmedlem**</span><span class="sxs-lookup"><span data-stu-id="2d883-142">**To dimension member**</span></span> |
| <span data-ttu-id="2d883-143">Organisation</span><span class="sxs-lookup"><span data-stu-id="2d883-143">Organization</span></span>                      | <span data-ttu-id="2d883-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="2d883-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="2d883-145">&nbsp;&nbsp;Administration</span><span class="sxs-lookup"><span data-stu-id="2d883-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="2d883-146">April</span><span class="sxs-lookup"><span data-stu-id="2d883-146">April</span></span>            |                           |                         |
| <span data-ttu-id="2d883-147">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="2d883-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="2d883-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="2d883-148">Alicia</span></span>           | <span data-ttu-id="2d883-149">CC002</span><span class="sxs-lookup"><span data-stu-id="2d883-149">CC002</span></span>                     | <span data-ttu-id="2d883-150">CC003</span><span class="sxs-lookup"><span data-stu-id="2d883-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="2d883-151">CC007</span><span class="sxs-lookup"><span data-stu-id="2d883-151">CC007</span></span>                     | <span data-ttu-id="2d883-152">CC007</span><span class="sxs-lookup"><span data-stu-id="2d883-152">CC007</span></span>                   |
| <span data-ttu-id="2d883-153">&nbsp;&nbsp;&nbsp;&nbsp;Personale</span><span class="sxs-lookup"><span data-stu-id="2d883-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="2d883-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="2d883-154">Arnie</span></span>            | <span data-ttu-id="2d883-155">CC001</span><span class="sxs-lookup"><span data-stu-id="2d883-155">CC001</span></span>                     | <span data-ttu-id="2d883-156">CC001</span><span class="sxs-lookup"><span data-stu-id="2d883-156">CC001</span></span>                   |
| <span data-ttu-id="2d883-157">&nbsp;&nbsp;Produktion</span><span class="sxs-lookup"><span data-stu-id="2d883-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="2d883-158">David</span><span class="sxs-lookup"><span data-stu-id="2d883-158">David</span></span>            |                           |                         |
| <span data-ttu-id="2d883-159">&nbsp;&nbsp;&nbsp;&nbsp;Emballage</span><span class="sxs-lookup"><span data-stu-id="2d883-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="2d883-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="2d883-160">Ellen</span></span>            | <span data-ttu-id="2d883-161">CC005</span><span class="sxs-lookup"><span data-stu-id="2d883-161">CC005</span></span>                     | <span data-ttu-id="2d883-162">CC005</span><span class="sxs-lookup"><span data-stu-id="2d883-162">CC005</span></span>                   |
| <span data-ttu-id="2d883-163">&nbsp;&nbsp;&nbsp;&nbsp;Samling</span><span class="sxs-lookup"><span data-stu-id="2d883-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="2d883-164">Chris</span><span class="sxs-lookup"><span data-stu-id="2d883-164">Chris</span></span>            | <span data-ttu-id="2d883-165">CC006</span><span class="sxs-lookup"><span data-stu-id="2d883-165">CC006</span></span>                     | <span data-ttu-id="2d883-166">CC006</span><span class="sxs-lookup"><span data-stu-id="2d883-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="2d883-167">Bogholdere skal tildeles til det øverste niveau i hierarkiet, så de kan se alle poster i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="2d883-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="2d883-168">Før adgangslistehierarkiet og de tilhørende sikkerhedsindstillinger kan anvendes, skal indstillingen **Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt** være indstillet til **Ja** under fanen **Generelt** på siden **Parametre for omkostningsregnskab** (**Omkostningsregnskab** > **Opsætning** > **Parametre**).</span><span class="sxs-lookup"><span data-stu-id="2d883-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="2d883-169">Indstillingerne for adgangslistehierarkiet bruges til at styre, hvilke data der vises i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="2d883-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="2d883-170">Arbejdsområdet **Omkostningsstyring** (i klienten):</span><span class="sxs-lookup"><span data-stu-id="2d883-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="2d883-171">Data på de sider, der bruges til detaljeadgang</span><span class="sxs-lookup"><span data-stu-id="2d883-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="2d883-172">Arbejdsområdet **Omkostningsstyring** (i mobilprogrammet):</span><span class="sxs-lookup"><span data-stu-id="2d883-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="2d883-173">Saldi i kort</span><span class="sxs-lookup"><span data-stu-id="2d883-173">Balances in cards</span></span>

- <span data-ttu-id="2d883-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="2d883-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="2d883-175">Data, der vises i Power BI visualiseringer</span><span class="sxs-lookup"><span data-stu-id="2d883-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="2d883-176">Data Power BI-visualiseringer, der er integreret i Microsoft Dynamics 365 for Finance and Operations-klienten</span><span class="sxs-lookup"><span data-stu-id="2d883-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="2d883-177">Før adgangslistehierarkiet kan påvirke dataene i Power BI, skal adgangslistehierarkiet og sikkerhed på rækkeniveau i Power BI kombineres.</span><span class="sxs-lookup"><span data-stu-id="2d883-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="2d883-178">Du kan finde flere oplysninger i [Konfigurere sikkerhed for indholdspakke til omkostningsregnskab](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="2d883-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="2d883-179">I dette emne beskrives de forudsætninger, der skal være opfyldt, før du kan bruge arbejdsområdet **Omkostningsstyring**.</span><span class="sxs-lookup"><span data-stu-id="2d883-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="2d883-180">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2d883-180">Additional resources</span></span>

- [<span data-ttu-id="2d883-181">Arbejdsområde for omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="2d883-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="2d883-182">Dimensionshierarki</span><span class="sxs-lookup"><span data-stu-id="2d883-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="2d883-183">Konfigurere sikkerhed for indholdspakke til omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="2d883-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

