---
title: Organisationshierarki i Dataverse
description: I dette emne beskrives integrationen af organisatoriske data mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
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
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750806"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarki i Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki. Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.

Selvom Dataverse ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt. Som en del af Dataverse-integrationen føjes organisationshierarkiets datastruktur til Dataverse.

## <a name="data-flow"></a>Dataflow

Et virksomhedsøkosystem, der består af Finance and Operations-apps og Dataverse, vil fortsat have et organisationshierarki. Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Dataverse til informations- og udvidelsesformål. I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Dataverse som envejs dataflow fra Finance and Operations-apps til Dataverse.

![Billede af arkitektur](media/dual-write-data-flow.png)

Organisationshierarkiets tabeltilknytninger er tilgængelige for envejssynkronisering af data fra Finance and Operations-apps til Dataverse.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af tabeltilknytninger for at synkronisere produkter og relaterede oplysninger.

Finance and Operations-apps | Andre Dynamics 365-apps | Beskrivende tekst
-----------------------|--------------------------------|---
Formål med organisationshierarkier | msdyn_internalorganizationhierarchypurposes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Formål med organisationshierarkier.
Type af organisationshierarki | msdyn_internalorganizationhierarchytypes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Type af organisationshierarkier.
Organisationshierarki - publiceret | msdyn_internalorganizationhierarchies | Denne skabelon giver mulighed for envejssynkronisering af tabellen Publiceret organisationshierarki.
Driftsenhed | msdyn_internalorganizations |
Juridiske enheder | msdyn_internalorganizations |
Juridiske enheder | cdm_companies | Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Intern organisation

Interne organisationsoplysninger i Dataverse kommer fra to tabeller, **driftsenhed** og **juridiske enheder**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]