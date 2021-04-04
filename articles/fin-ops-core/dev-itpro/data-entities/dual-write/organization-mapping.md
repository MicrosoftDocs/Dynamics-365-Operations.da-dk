---
title: Organisationshierarki i Dataverse
description: I dette emne beskrives integrationen af organisatoriske data mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f265d49a87383e2abf129b8d1d67567fc4b9e0de
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559573"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="3ab58-103">Organisationshierarki i Dataverse</span><span class="sxs-lookup"><span data-stu-id="3ab58-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3ab58-104">Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3ab58-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="3ab58-105">Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3ab58-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="3ab58-106">Selvom Dataverse ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt.</span><span class="sxs-lookup"><span data-stu-id="3ab58-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="3ab58-107">Som en del af Dataverse-integrationen føjes organisationshierarkiets datastruktur til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3ab58-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="3ab58-108">Dataflow</span><span class="sxs-lookup"><span data-stu-id="3ab58-108">Data flow</span></span>

<span data-ttu-id="3ab58-109">Et virksomhedsøkosystem, der består af Finance and Operations-apps og Dataverse, vil fortsat have et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3ab58-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="3ab58-110">Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Dataverse til informations- og udvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="3ab58-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="3ab58-111">I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Dataverse som envejs dataflow fra Finance and Operations-apps til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3ab58-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Billede af arkitektur](media/dual-write-data-flow.png)

<span data-ttu-id="3ab58-113">Organisationshierarkiets tabeltilknytninger er tilgængelige for envejssynkronisering af data fra Finance and Operations-apps til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3ab58-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="3ab58-114">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="3ab58-114">Templates</span></span>

<span data-ttu-id="3ab58-115">Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="3ab58-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="3ab58-116">Som følgende tabel viser, oprettes der en samling af tabeltilknytninger for at synkronisere produkter og relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="3ab58-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="3ab58-117">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="3ab58-117">Finance and Operations apps</span></span> | <span data-ttu-id="3ab58-118">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="3ab58-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="3ab58-119">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="3ab58-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="3ab58-120">Formål med organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="3ab58-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="3ab58-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="3ab58-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="3ab58-122">Denne skabelon giver mulighed for envejssynkronisering af tabellen Formål med organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="3ab58-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="3ab58-123">Type af organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3ab58-123">Organization hierarchy type</span></span> | <span data-ttu-id="3ab58-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="3ab58-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="3ab58-125">Denne skabelon giver mulighed for envejssynkronisering af tabellen Type af organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="3ab58-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="3ab58-126">Organisationshierarki - publiceret</span><span class="sxs-lookup"><span data-stu-id="3ab58-126">Organization hierarchy - published</span></span> | <span data-ttu-id="3ab58-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="3ab58-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="3ab58-128">Denne skabelon giver mulighed for envejssynkronisering af tabellen Publiceret organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3ab58-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="3ab58-129">Driftsenhed</span><span class="sxs-lookup"><span data-stu-id="3ab58-129">Operating unit</span></span> | <span data-ttu-id="3ab58-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="3ab58-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="3ab58-131">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="3ab58-131">Legal entities</span></span> | <span data-ttu-id="3ab58-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="3ab58-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="3ab58-133">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="3ab58-133">Legal entities</span></span> | <span data-ttu-id="3ab58-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="3ab58-134">cdm_companies</span></span> | <span data-ttu-id="3ab58-135">Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).</span><span class="sxs-lookup"><span data-stu-id="3ab58-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="3ab58-136">Intern organisation</span><span class="sxs-lookup"><span data-stu-id="3ab58-136">Internal Organization</span></span>

<span data-ttu-id="3ab58-137">Interne organisationsoplysninger i Dataverse kommer fra to tabeller, **driftsenhed** og **juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="3ab58-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]