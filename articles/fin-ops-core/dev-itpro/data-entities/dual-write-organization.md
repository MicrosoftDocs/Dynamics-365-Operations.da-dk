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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572443"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="85c85-103">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="85c85-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="85c85-104">Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="85c85-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="85c85-105">Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="85c85-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="85c85-106">Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="85c85-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="85c85-107">Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="85c85-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="85c85-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="85c85-108">Data flow</span></span>

<span data-ttu-id="85c85-109">En virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="85c85-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="85c85-110">Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="85c85-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="85c85-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="85c85-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="85c85-113">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="85c85-113">Templates</span></span>

<span data-ttu-id="85c85-114">Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="85c85-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="85c85-115">Formål med internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="85c85-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="85c85-116">Denne skabelon giver envejs synkronisering af enheden Formål med organisationshierarkier fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="85c85-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="85c85-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-117">Source field</span></span> | <span data-ttu-id="85c85-118">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-118">Map type</span></span> | <span data-ttu-id="85c85-119">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-119">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="85c85-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="85c85-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="85c85-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="85c85-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="85c85-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="85c85-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="85c85-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="85c85-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="85c85-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="85c85-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="85c85-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="85c85-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="85c85-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="85c85-127">msdyn\_immutable</span></span>
<span data-ttu-id="85c85-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="85c85-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="85c85-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="85c85-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="85c85-130">Type af internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="85c85-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="85c85-131">Denne skabelon giver envejs synkronisering af enheden Type af organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="85c85-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="85c85-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-132">Source field</span></span> | <span data-ttu-id="85c85-133">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-133">Map type</span></span> | <span data-ttu-id="85c85-134">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-134">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="85c85-135">NAME</span></span> | \> | <span data-ttu-id="85c85-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="85c85-137">Internt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="85c85-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="85c85-138">Denne skabelon giver envejs synkronisering af enheden Publiceret organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="85c85-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="85c85-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-139">Source field</span></span> | <span data-ttu-id="85c85-140">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-140">Map type</span></span> | <span data-ttu-id="85c85-141">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-141">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="85c85-142">VALIDTO</span></span> | \> | <span data-ttu-id="85c85-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="85c85-143">msdyn\_validto</span></span>
<span data-ttu-id="85c85-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="85c85-144">VALIDFROM</span></span> | \> | <span data-ttu-id="85c85-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="85c85-145">msdyn\_validfrom</span></span>
<span data-ttu-id="85c85-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="85c85-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="85c85-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="85c85-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="85c85-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="85c85-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="85c85-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="85c85-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="85c85-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="85c85-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="85c85-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="85c85-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="85c85-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="85c85-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="85c85-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="85c85-158">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="85c85-158">Internal Organization</span></span>

<span data-ttu-id="85c85-159">Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="85c85-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="85c85-160">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="85c85-160">Operating unit</span></span>

<span data-ttu-id="85c85-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-161">Source field</span></span> | <span data-ttu-id="85c85-162">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-162">Map type</span></span> | <span data-ttu-id="85c85-163">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-163">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="85c85-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="85c85-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="85c85-165">msdyn\_languageid</span></span>
<span data-ttu-id="85c85-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="85c85-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="85c85-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="85c85-167">msdyn\_namealias</span></span>
<span data-ttu-id="85c85-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="85c85-168">NAME</span></span> | \> | <span data-ttu-id="85c85-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-169">msdyn\_name</span></span>
<span data-ttu-id="85c85-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="85c85-171">msdyn\_partynumber</span></span>
<span data-ttu-id="85c85-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="85c85-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="85c85-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="85c85-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="85c85-174">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="85c85-174">Legal entity</span></span>

<span data-ttu-id="85c85-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-175">Source field</span></span> | <span data-ttu-id="85c85-176">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-176">Map type</span></span> | <span data-ttu-id="85c85-177">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-177">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="85c85-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="85c85-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="85c85-179">msdyn\_namealias</span></span>
<span data-ttu-id="85c85-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="85c85-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="85c85-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="85c85-181">msdyn\_languageid</span></span>
<span data-ttu-id="85c85-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="85c85-182">NAME</span></span> | \> | <span data-ttu-id="85c85-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-183">msdyn\_name</span></span>
<span data-ttu-id="85c85-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="85c85-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="85c85-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="85c85-185">msdyn\_partynumber</span></span>
<span data-ttu-id="85c85-186">ingen</span><span class="sxs-lookup"><span data-stu-id="85c85-186">none</span></span> | \>\> | <span data-ttu-id="85c85-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="85c85-187">msdyn\_type</span></span>
<span data-ttu-id="85c85-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="85c85-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="85c85-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="85c85-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="85c85-190">Regnskab</span><span class="sxs-lookup"><span data-stu-id="85c85-190">Company</span></span>

<span data-ttu-id="85c85-191">Giver tovejs synkronisering af oplysninger om juridisk enhed (firma) mellem Finance and Operations og andre Dynamics 365-apps.</span><span class="sxs-lookup"><span data-stu-id="85c85-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="85c85-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="85c85-192">Source field</span></span> | <span data-ttu-id="85c85-193">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="85c85-193">Map type</span></span> | <span data-ttu-id="85c85-194">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="85c85-194">Destination field</span></span>
---|---|---
<span data-ttu-id="85c85-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="85c85-195">NAME</span></span> | = | <span data-ttu-id="85c85-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="85c85-196">cdm\_name</span></span>
<span data-ttu-id="85c85-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="85c85-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="85c85-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="85c85-198">cdm\_companycode</span></span>
