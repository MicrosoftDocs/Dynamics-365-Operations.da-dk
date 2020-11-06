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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000728"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="26c9d-103">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="26c9d-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26c9d-104">Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="26c9d-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="26c9d-105">Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="26c9d-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="26c9d-106">Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="26c9d-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="26c9d-107">Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="26c9d-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="26c9d-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="26c9d-108">Data flow</span></span>

<span data-ttu-id="26c9d-109">Et virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="26c9d-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="26c9d-110">Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="26c9d-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="26c9d-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="26c9d-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

<span data-ttu-id="26c9d-113">Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="26c9d-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="26c9d-114">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="26c9d-114">Templates</span></span>

<span data-ttu-id="26c9d-115">Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="26c9d-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="26c9d-116">Som følgende tabel viser, oprettes der en samling af enhedstilknytninger for at synkronisere produkter og relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="26c9d-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="26c9d-117">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="26c9d-117">Finance and Operations apps</span></span> | <span data-ttu-id="26c9d-118">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="26c9d-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="26c9d-119">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="26c9d-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="26c9d-120">Formål med organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="26c9d-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="26c9d-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="26c9d-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="26c9d-122">Denne skabelon giver mulighed for envejssynkronisering af enheden Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="26c9d-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="26c9d-123">Type af organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="26c9d-123">Organization hierarchy type</span></span> | <span data-ttu-id="26c9d-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="26c9d-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="26c9d-125">Denne skabelon giver mulighed for envejssynkronisering af enhedstypen Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="26c9d-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="26c9d-126">Organisationshierarki - publiceret</span><span class="sxs-lookup"><span data-stu-id="26c9d-126">Organization hierarchy - published</span></span> | <span data-ttu-id="26c9d-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="26c9d-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="26c9d-128">Denne skabelon giver mulighed for envejssynkronisering af enheden Publiceret Organisationshierarki Formål.</span><span class="sxs-lookup"><span data-stu-id="26c9d-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="26c9d-129">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="26c9d-129">Operating unit</span></span> | <span data-ttu-id="26c9d-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="26c9d-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="26c9d-131">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="26c9d-131">Legal entities</span></span> | <span data-ttu-id="26c9d-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="26c9d-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="26c9d-133">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="26c9d-133">Legal entities</span></span> | <span data-ttu-id="26c9d-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="26c9d-134">cdm_companies</span></span> | <span data-ttu-id="26c9d-135">Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).</span><span class="sxs-lookup"><span data-stu-id="26c9d-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="26c9d-136">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="26c9d-136">Internal Organization</span></span>

<span data-ttu-id="26c9d-137">Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="26c9d-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
