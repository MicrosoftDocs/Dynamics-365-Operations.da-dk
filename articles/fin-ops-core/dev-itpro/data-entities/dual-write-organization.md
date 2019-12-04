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
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769654"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organisationshierarki i Common Data Service

[!include [banner](../includes/banner.md)]

Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki. Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.

Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt. Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.

## <a name="data-flow"></a>Dataflow

En virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki. Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål. I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a>Skabeloner

Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af enhedstilknytninger for at synkronisere produkter og relaterede oplysninger.

Finance and Operations | Andre Dynamics 365-apps | Beskrivelse
-----------------------|--------------------------------|---
Formål med organisationshierarkier | msdyn_internalorganizationhierarchypurposes | Denne skabelon giver mulighed for envejssynkronisering af enheden Organisationshierarki Formål.
Type af organisationshierarki | msdyn_internalorganizationhierarchytypes | Denne skabelon giver mulighed for envejssynkronisering af enhedstypen Organisationshierarki Formål.
Organisationshierarki - publiceret | msdyn_internalorganizationhierarchies | Denne skabelon giver mulighed for envejssynkronisering af enheden Publiceret Organisationshierarki Formål.
Driftsenhed | msdyn_internalorganizations | 
Juridiske enheder | msdyn_internalorganizations | 
Juridiske enheder | cdm_companies | Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Intern organisation

Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]

