---
title: Organisationshierarki i Common Data Service
description: I dette emne beskrives integrationen af organisationsdata mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182019"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="fd28f-103">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fd28f-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="fd28f-104">Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="fd28f-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="fd28f-105">Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fd28f-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="fd28f-106">Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="fd28f-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="fd28f-107">Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fd28f-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="fd28f-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="fd28f-108">Data flow</span></span>

<span data-ttu-id="fd28f-109">En virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="fd28f-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="fd28f-110">Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="fd28f-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="fd28f-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fd28f-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="fd28f-113">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="fd28f-113">Templates</span></span>

<span data-ttu-id="fd28f-114">Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fd28f-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="fd28f-115">Formål med internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="fd28f-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="fd28f-116">Denne skabelon giver envejs synkronisering af enheden Formål med organisationshierarkier fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="fd28f-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="fd28f-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-117">Source field</span></span> | <span data-ttu-id="fd28f-118">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-118">Map type</span></span> | <span data-ttu-id="fd28f-119">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-119">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fd28f-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fd28f-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="fd28f-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="fd28f-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fd28f-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fd28f-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="fd28f-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="fd28f-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="fd28f-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="fd28f-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="fd28f-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="fd28f-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="fd28f-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="fd28f-127">msdyn\_immutable</span></span>
<span data-ttu-id="fd28f-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="fd28f-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="fd28f-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="fd28f-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="fd28f-130">Type af internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="fd28f-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="fd28f-131">Denne skabelon giver envejs synkronisering af enheden Type af organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="fd28f-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="fd28f-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-132">Source field</span></span> | <span data-ttu-id="fd28f-133">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-133">Map type</span></span> | <span data-ttu-id="fd28f-134">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-134">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="fd28f-135">NAME</span></span> | \> | <span data-ttu-id="fd28f-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="fd28f-137">Internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="fd28f-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="fd28f-138">Denne skabelon giver envejs synkronisering af enheden Publiceret organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="fd28f-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="fd28f-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-139">Source field</span></span> | <span data-ttu-id="fd28f-140">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-140">Map type</span></span> | <span data-ttu-id="fd28f-141">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-141">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="fd28f-142">VALIDTO</span></span> | \> | <span data-ttu-id="fd28f-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="fd28f-143">msdyn\_validto</span></span>
<span data-ttu-id="fd28f-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="fd28f-144">VALIDFROM</span></span> | \> | <span data-ttu-id="fd28f-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="fd28f-145">msdyn\_validfrom</span></span>
<span data-ttu-id="fd28f-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fd28f-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fd28f-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="fd28f-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="fd28f-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="fd28f-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="fd28f-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="fd28f-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="fd28f-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="fd28f-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="fd28f-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="fd28f-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fd28f-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="fd28f-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fd28f-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="fd28f-158">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="fd28f-158">Internal Organization</span></span>

<span data-ttu-id="fd28f-159">Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="fd28f-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="fd28f-160">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="fd28f-160">Operating unit</span></span>

<span data-ttu-id="fd28f-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-161">Source field</span></span> | <span data-ttu-id="fd28f-162">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-162">Map type</span></span> | <span data-ttu-id="fd28f-163">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-163">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="fd28f-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="fd28f-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="fd28f-165">msdyn\_languageid</span></span>
<span data-ttu-id="fd28f-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="fd28f-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="fd28f-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="fd28f-167">msdyn\_namealias</span></span>
<span data-ttu-id="fd28f-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="fd28f-168">NAME</span></span> | \> | <span data-ttu-id="fd28f-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-169">msdyn\_name</span></span>
<span data-ttu-id="fd28f-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fd28f-171">msdyn\_partynumber</span></span>
<span data-ttu-id="fd28f-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="fd28f-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="fd28f-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="fd28f-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="fd28f-174">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="fd28f-174">Legal entity</span></span>

<span data-ttu-id="fd28f-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-175">Source field</span></span> | <span data-ttu-id="fd28f-176">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-176">Map type</span></span> | <span data-ttu-id="fd28f-177">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-177">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="fd28f-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="fd28f-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="fd28f-179">msdyn\_namealias</span></span>
<span data-ttu-id="fd28f-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="fd28f-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="fd28f-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="fd28f-181">msdyn\_languageid</span></span>
<span data-ttu-id="fd28f-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="fd28f-182">NAME</span></span> | \> | <span data-ttu-id="fd28f-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-183">msdyn\_name</span></span>
<span data-ttu-id="fd28f-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="fd28f-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="fd28f-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="fd28f-185">msdyn\_partynumber</span></span>
<span data-ttu-id="fd28f-186">ingen</span><span class="sxs-lookup"><span data-stu-id="fd28f-186">none</span></span> | \>\> | <span data-ttu-id="fd28f-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="fd28f-187">msdyn\_type</span></span>
<span data-ttu-id="fd28f-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="fd28f-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="fd28f-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="fd28f-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="fd28f-190">Regnskab</span><span class="sxs-lookup"><span data-stu-id="fd28f-190">Company</span></span>

<span data-ttu-id="fd28f-191">Giver tovejs synkronisering af oplysninger om juridisk enhed (firma) mellem Finance and Operations og andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="fd28f-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="fd28f-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-192">Source field</span></span> | <span data-ttu-id="fd28f-193">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="fd28f-193">Map type</span></span> | <span data-ttu-id="fd28f-194">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fd28f-194">Destination field</span></span>
---|---|---
<span data-ttu-id="fd28f-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="fd28f-195">NAME</span></span> | = | <span data-ttu-id="fd28f-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="fd28f-196">cdm\_name</span></span>
<span data-ttu-id="fd28f-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="fd28f-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="fd28f-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="fd28f-198">cdm\_companycode</span></span>
