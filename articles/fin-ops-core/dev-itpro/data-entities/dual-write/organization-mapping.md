---
title: Organisationshierarki i Common Data Service
description: I dette emne beskrives integrationen af organisatoriske data mellem Finance and Operations-apps og Common Data Service.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173148"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="d2f5e-103">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d2f5e-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d2f5e-104">Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d2f5e-105">Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d2f5e-106">Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d2f5e-107">Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d2f5e-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="d2f5e-108">Data flow</span></span>

<span data-ttu-id="d2f5e-109">Et virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d2f5e-110">Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="d2f5e-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="d2f5e-113">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="d2f5e-113">Templates</span></span>

<span data-ttu-id="d2f5e-114">Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="d2f5e-115">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="d2f5e-115">Templates</span></span>

<span data-ttu-id="d2f5e-116">Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="d2f5e-117">Som følgende tabel viser, oprettes der en samling af enhedstilknytninger for at synkronisere produkter og relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="d2f5e-118">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="d2f5e-118">Finance and Operations apps</span></span> | <span data-ttu-id="d2f5e-119">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="d2f5e-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d2f5e-120">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="d2f5e-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="d2f5e-121">Formål med organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="d2f5e-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="d2f5e-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="d2f5e-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="d2f5e-123">Denne skabelon giver mulighed for envejssynkronisering af enheden Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="d2f5e-124">Type af organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="d2f5e-124">Organization hierarchy type</span></span> | <span data-ttu-id="d2f5e-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="d2f5e-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="d2f5e-126">Denne skabelon giver mulighed for envejssynkronisering af enhedstypen Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="d2f5e-127">Organisationshierarki - publiceret</span><span class="sxs-lookup"><span data-stu-id="d2f5e-127">Organization hierarchy - published</span></span> | <span data-ttu-id="d2f5e-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="d2f5e-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="d2f5e-129">Denne skabelon giver mulighed for envejssynkronisering af enheden Publiceret Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="d2f5e-130">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="d2f5e-130">Operating unit</span></span> | <span data-ttu-id="d2f5e-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d2f5e-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="d2f5e-132">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="d2f5e-132">Legal entities</span></span> | <span data-ttu-id="d2f5e-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d2f5e-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="d2f5e-134">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="d2f5e-134">Legal entities</span></span> | <span data-ttu-id="d2f5e-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="d2f5e-135">cdm_companies</span></span> | <span data-ttu-id="d2f5e-136">Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).</span><span class="sxs-lookup"><span data-stu-id="d2f5e-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="d2f5e-137">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="d2f5e-137">Internal Organization</span></span>

<span data-ttu-id="d2f5e-138">Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

