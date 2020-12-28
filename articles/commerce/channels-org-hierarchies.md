---
title: Konfigurere organisationshierarkier
description: I dette emne beskrives, hvordan du kan konfigurere organisationshierarkier i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411041"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="3a070-103">Konfigurere organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3a070-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3a070-104">I dette emne beskrives, hvordan du kan konfigurere organisationshierarkier i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3a070-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3a070-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="3a070-105">Overview</span></span>

<span data-ttu-id="3a070-106">Før du opretter kanaler, skal du sikre, at du har konfigureret dine organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="3a070-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="3a070-107">Du kan bruge organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="3a070-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="3a070-108">Du kan f.eks. oprette et hierarki til skattemæssig, juridisk eller lovpligtig rapportering.</span><span class="sxs-lookup"><span data-stu-id="3a070-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="3a070-109">Derefter kan du oprette et andet hierarki for at afrapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til interne afrapportering.</span><span class="sxs-lookup"><span data-stu-id="3a070-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="3a070-110">Før du opretter et organisationshierarki, skal du oprette organisationer.</span><span class="sxs-lookup"><span data-stu-id="3a070-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="3a070-111">Du kan få flere oplysninger i [Oprette juridiske enheder](channels-legal-entities.md) eller [Oprette driftsenheder](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="3a070-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="3a070-112">Du kan finde flere oplysninger i følgende emner.</span><span class="sxs-lookup"><span data-stu-id="3a070-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="3a070-113">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3a070-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="3a070-114">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a070-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="3a070-115">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a070-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="3a070-116">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a070-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="3a070-117">Benyt følgende fremgangsmåde for at oprette et organisationshierarki for en kanal.</span><span class="sxs-lookup"><span data-stu-id="3a070-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3a070-118">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="3a070-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="3a070-119">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3a070-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3a070-120">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3a070-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="3a070-121">Vælg **Tildel formål** i sektionen **Formål**.</span><span class="sxs-lookup"><span data-stu-id="3a070-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="3a070-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3a070-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="3a070-123">Vælg det formål, du vil tildele til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3a070-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="3a070-124">Vælg **Tilføj** i sektionen **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="3a070-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="3a070-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3a070-125">In the list, mark the selected row.</span></span> <span data-ttu-id="3a070-126">Find det hierarki, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="3a070-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="3a070-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a070-127">Select **OK**.</span></span>

<span data-ttu-id="3a070-128">Følgende billede viser et eksempel på et organisationshierarki, der er oprettet for række af fiktive "Adventure Works"-butikker.</span><span class="sxs-lookup"><span data-stu-id="3a070-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Eksempel på organisationshierarki](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="3a070-130">Føje organisationer til et hierarki</span><span class="sxs-lookup"><span data-stu-id="3a070-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="3a070-131">Følg disse trin for at føje organisationer til et hierarki.</span><span class="sxs-lookup"><span data-stu-id="3a070-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3a070-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3a070-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="3a070-133">Vælg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3a070-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="3a070-134">Gå til handlingsruden, og vælg **Vis**.</span><span class="sxs-lookup"><span data-stu-id="3a070-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="3a070-135">Tilføj organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="3a070-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="3a070-136">Hvis du vil tilføje en organisation skal du vælge **Rediger** og derefter vælge **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="3a070-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="3a070-137">Når du er færdig med at foretage ændringer, kan du gemme en kladde og udgive ændringerne.</span><span class="sxs-lookup"><span data-stu-id="3a070-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="3a070-138">Følgende billede viser en juridisk enhed, der er føjet til hierarkiroden, med fire bærere, som er tilføjet for kanalerne "Mall", "Udgang", "Online" og "Callcenter".</span><span class="sxs-lookup"><span data-stu-id="3a070-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="3a070-139">Der kan føjes forskellige detailvarer, callcentre og onlinekanaler til hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="3a070-139">Various retail, call center and online channels can then be added to each.</span></span>

![Eksempel på hierarkidesigner](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="3a070-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3a070-141">Additional resources</span></span>

[<span data-ttu-id="3a070-142">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3a070-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3a070-143">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a070-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3a070-144">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="3a070-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="3a070-145">Oprette driftsenheder</span><span class="sxs-lookup"><span data-stu-id="3a070-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3a070-146">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="3a070-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3a070-147">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="3a070-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
