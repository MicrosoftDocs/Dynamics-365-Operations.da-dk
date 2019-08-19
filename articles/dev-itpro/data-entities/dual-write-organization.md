---
title: Organisationshierarki i Common Data Service
description: I dette emne beskrives integrationen af organisationsdata mellem Finance and Operations og Common Data Service.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789168"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="36d8e-103">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="36d8e-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="36d8e-104">Da Microsoft Dynamics 365 for Finance and Operations er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="36d8e-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="36d8e-105">Virksomheders økonomi og drift kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="36d8e-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="36d8e-106">Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="36d8e-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="36d8e-107">Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36d8e-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="36d8e-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="36d8e-108">Data flow</span></span>

<span data-ttu-id="36d8e-109">En virksomheds økosystem, der består af Finance and Operations og Common Data Service, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="36d8e-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="36d8e-110">Dette organisationshierarki er baseret på Finance and Operations, men det er eksponeret i Common Data Service til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="36d8e-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="36d8e-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36d8e-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="36d8e-113">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="36d8e-113">Templates</span></span>

<span data-ttu-id="36d8e-114">Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36d8e-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="36d8e-115">Formål med internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="36d8e-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="36d8e-116">Denne skabelon giver envejs synkronisering af enheden Formål med organisationshierarkier fra Finance and Operations til Dynamics 365 for Customer engagement.</span><span class="sxs-lookup"><span data-stu-id="36d8e-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="36d8e-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-117">Source field</span></span> | <span data-ttu-id="36d8e-118">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-118">Map type</span></span> | <span data-ttu-id="36d8e-119">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-119">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="36d8e-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="36d8e-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="36d8e-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="36d8e-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="36d8e-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="36d8e-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="36d8e-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="36d8e-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="36d8e-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="36d8e-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="36d8e-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="36d8e-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="36d8e-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="36d8e-127">msdyn\_immutable</span></span>
<span data-ttu-id="36d8e-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="36d8e-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="36d8e-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="36d8e-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="36d8e-130">Type af internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="36d8e-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="36d8e-131">Denne skabelon giver envejs synkronisering af enheden Type af organisationshierarki fra Finance and Operations til Customer engagement.</span><span class="sxs-lookup"><span data-stu-id="36d8e-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="36d8e-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-132">Source field</span></span> | <span data-ttu-id="36d8e-133">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-133">Map type</span></span> | <span data-ttu-id="36d8e-134">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-134">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="36d8e-135">NAME</span></span> | \> | <span data-ttu-id="36d8e-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="36d8e-137">Internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="36d8e-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="36d8e-138">Denne skabelon giver envejs synkronisering af enheden Publiceret organisationshierarki fra Finance and Operations til Customer engagement.</span><span class="sxs-lookup"><span data-stu-id="36d8e-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="36d8e-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-139">Source field</span></span> | <span data-ttu-id="36d8e-140">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-140">Map type</span></span> | <span data-ttu-id="36d8e-141">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-141">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="36d8e-142">VALIDTO</span></span> | \> | <span data-ttu-id="36d8e-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="36d8e-143">msdyn\_validto</span></span>
<span data-ttu-id="36d8e-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="36d8e-144">VALIDFROM</span></span> | \> | <span data-ttu-id="36d8e-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="36d8e-145">msdyn\_validfrom</span></span>
<span data-ttu-id="36d8e-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="36d8e-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="36d8e-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="36d8e-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="36d8e-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="36d8e-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="36d8e-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="36d8e-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="36d8e-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="36d8e-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="36d8e-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="36d8e-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="36d8e-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="36d8e-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="36d8e-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="36d8e-158">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="36d8e-158">Internal Organization</span></span>

<span data-ttu-id="36d8e-159">Interne organisationsoplysninger i Common Data Service kommer fra to Finance and Operations-enheder, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="36d8e-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="36d8e-160">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="36d8e-160">Operating unit</span></span>

<span data-ttu-id="36d8e-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-161">Source field</span></span> | <span data-ttu-id="36d8e-162">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-162">Map type</span></span> | <span data-ttu-id="36d8e-163">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-163">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="36d8e-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="36d8e-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="36d8e-165">msdyn\_languageid</span></span>
<span data-ttu-id="36d8e-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="36d8e-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="36d8e-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="36d8e-167">msdyn\_namealias</span></span>
<span data-ttu-id="36d8e-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="36d8e-168">NAME</span></span> | \> | <span data-ttu-id="36d8e-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-169">msdyn\_name</span></span>
<span data-ttu-id="36d8e-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="36d8e-171">msdyn\_partynumber</span></span>
<span data-ttu-id="36d8e-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="36d8e-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="36d8e-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="36d8e-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="36d8e-174">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="36d8e-174">Legal entity</span></span>

<span data-ttu-id="36d8e-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-175">Source field</span></span> | <span data-ttu-id="36d8e-176">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-176">Map type</span></span> | <span data-ttu-id="36d8e-177">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-177">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="36d8e-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="36d8e-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="36d8e-179">msdyn\_namealias</span></span>
<span data-ttu-id="36d8e-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="36d8e-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="36d8e-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="36d8e-181">msdyn\_languageid</span></span>
<span data-ttu-id="36d8e-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="36d8e-182">NAME</span></span> | \> | <span data-ttu-id="36d8e-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-183">msdyn\_name</span></span>
<span data-ttu-id="36d8e-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="36d8e-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="36d8e-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="36d8e-185">msdyn\_partynumber</span></span>
<span data-ttu-id="36d8e-186">ingen</span><span class="sxs-lookup"><span data-stu-id="36d8e-186">none</span></span> | \>\> | <span data-ttu-id="36d8e-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="36d8e-187">msdyn\_type</span></span>
<span data-ttu-id="36d8e-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="36d8e-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="36d8e-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="36d8e-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="36d8e-190">Regnskab</span><span class="sxs-lookup"><span data-stu-id="36d8e-190">Company</span></span>

<span data-ttu-id="36d8e-191">Giver tovejs synkronisering af oplysninger om juridisk enhed (firma) mellem Finance and Operations og Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="36d8e-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="36d8e-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-192">Source field</span></span> | <span data-ttu-id="36d8e-193">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="36d8e-193">Map type</span></span> | <span data-ttu-id="36d8e-194">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="36d8e-194">Destination field</span></span>
---|---|---
<span data-ttu-id="36d8e-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="36d8e-195">NAME</span></span> | = | <span data-ttu-id="36d8e-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="36d8e-196">cdm\_name</span></span>
<span data-ttu-id="36d8e-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="36d8e-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="36d8e-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="36d8e-198">cdm\_companycode</span></span>
