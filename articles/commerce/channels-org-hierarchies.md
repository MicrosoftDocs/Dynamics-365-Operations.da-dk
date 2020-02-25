---
title: Konfigurer organisationshierarkier
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
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002329"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="c35ea-103">Konfigurer organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="c35ea-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c35ea-104">I dette emne beskrives, hvordan du kan konfigurere organisationshierarkier i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c35ea-104">This topic descibes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c35ea-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="c35ea-105">Overview</span></span>

<span data-ttu-id="c35ea-106">Før du opretter kanaler, skal du sikre, at du har konfigureret dine organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="c35ea-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="c35ea-107">Du kan bruge organisationshierarkier for at få vist og rapportere om forskellige perspektiver i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="c35ea-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="c35ea-108">Du kan f.eks. oprette et hierarki til skattemæssig, juridisk eller lovpligtig rapportering.</span><span class="sxs-lookup"><span data-stu-id="c35ea-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="c35ea-109">Derefter kan du oprette et andet hierarki for at afrapportere økonomiske oplysninger, der ikke er juridisk påkrævet, men bruges til interne afrapportering.</span><span class="sxs-lookup"><span data-stu-id="c35ea-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="c35ea-110">Før du opretter et organisationshierarki, skal du oprette organisationer.</span><span class="sxs-lookup"><span data-stu-id="c35ea-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="c35ea-111">Du kan få flere oplysninger i [Oprette juridiske enheder](channels-legal-entities.md) eller [Oprette driftsenheder](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c35ea-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="c35ea-112">Du kan finde flere oplysninger i følgende emner.</span><span class="sxs-lookup"><span data-stu-id="c35ea-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="c35ea-113">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="c35ea-113">Organizations and organizational hierarchies overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [<span data-ttu-id="c35ea-114">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="c35ea-114">Plan your organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c35ea-115">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="c35ea-115">Create an organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="c35ea-116">Oprette et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="c35ea-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="c35ea-117">Benyt følgende fremgangsmåde for at oprette et organisationshierarki for en kanal.</span><span class="sxs-lookup"><span data-stu-id="c35ea-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c35ea-118">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c35ea-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="c35ea-119">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c35ea-120">Angiv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c35ea-121">Vælg **Tildel formål** i sektionen **Formål**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="c35ea-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c35ea-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="c35ea-123">Vælg det formål, du vil tildele til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c35ea-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="c35ea-124">Vælg **Tilføj** i sektionen **Tildelte hierarkier**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="c35ea-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c35ea-125">In the list, mark the selected row.</span></span> <span data-ttu-id="c35ea-126">Find det hierarki, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="c35ea-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="c35ea-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-127">Select **OK**.</span></span>

<span data-ttu-id="c35ea-128">Følgende billede viser et eksempel på et organisationshierarki, der er oprettet for række af fiktive "Adventure Works"-butikker.</span><span class="sxs-lookup"><span data-stu-id="c35ea-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Eksempel på organisationshierarki](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="c35ea-130">Føje organisationer til et hierarki</span><span class="sxs-lookup"><span data-stu-id="c35ea-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="c35ea-131">Følg disse trin for at føje organisationer til et hierarki.</span><span class="sxs-lookup"><span data-stu-id="c35ea-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c35ea-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c35ea-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="c35ea-133">Vælg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c35ea-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="c35ea-134">Gå til handlingsruden, og vælg **Vis**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="c35ea-135">Tilføj organisationer efter behov.</span><span class="sxs-lookup"><span data-stu-id="c35ea-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="c35ea-136">Hvis du vil tilføje en organisation skal du vælge **Rediger** og derefter vælge **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="c35ea-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="c35ea-137">Når du er færdig med at foretage ændringer, kan du gemme en kladde og udgive ændringerne.</span><span class="sxs-lookup"><span data-stu-id="c35ea-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="c35ea-138">Følgende billede viser en juridisk enhed, der er føjet til hierarkiroden, med fire bærere, som er tilføjet for kanalerne "Mall", "Udgang", "Online" og "Callcenter".</span><span class="sxs-lookup"><span data-stu-id="c35ea-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="c35ea-139">Der kan føjes forskellige detailvarer, callcentre og onlinekanaler til hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="c35ea-139">Various retail, call center and online channels can then be added to each.</span></span>

![Eksempel på hierarkidesigner](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="c35ea-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c35ea-141">Additional resources</span></span>

[<span data-ttu-id="c35ea-142">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="c35ea-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c35ea-143">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="c35ea-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c35ea-144">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="c35ea-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c35ea-145">Oprette driftsenheder</span><span class="sxs-lookup"><span data-stu-id="c35ea-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c35ea-146">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="c35ea-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c35ea-147">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="c35ea-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
