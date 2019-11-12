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
# <a name="organization-hierarchy-in-common-data-service"></a>Organisationshierarki i Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki. Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.

Selvom Common Data Service ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt. Som en del af Common Data Service-integrationen føjes organisationshierarkiets datastruktur til Common Data Service.

## <a name="data-flow"></a>Dataflow

En virksomhedsøkosystem, der består af Finance and Operations-apps og Common Data Service, vil fortsat have et organisationshierarki. Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Common Data Service til informations- og udvidelsesformål. I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Common Data Service som envejs dataflow fra Finance and Operations-apps til Common Data Service.

![Billede af arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a>Skabeloner

Organisationshierarkiets enhedstilknytninger er tilgængelige for envejs synkronisering af data fra Finance and Operations-apps til Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Formål med internt organisationshierarki

Denne skabelon giver envejs synkronisering af enheden Formål med organisationshierarkier fra Finance and Operations til andre Dynamics 365-apps.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Type af internt organisationshierarki

Denne skabelon giver envejs synkronisering af enheden Type af organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.

<!-- ![architecture image](media/dual-write-type.png) -->

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
NAVN | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Internt organisationshierarki

Denne skabelon giver envejs synkronisering af enheden Publiceret organisationshierarki fra Finance and Operations til andre Dynamics 365-apps.

<!-- ![architecture image](media/dual-write-organization.png) -->

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Intern organisation

Interne organisationsoplysninger i Common Data Service kommer fra to Finance and enheder, **driftsenhed** og **juridiske enheder**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Driftsenhed

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NAVN | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Juridisk enhed

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NAVN | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
ingen | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Regnskab

Giver tovejs synkronisering af oplysninger om juridisk enhed (firma) mellem Finance and Operations og andre Dynamics 365-apps.

<!-- ![architecture image](media/dual-write-company.png) -->

Kildefelt | Tilknytningstype | Destinationsfelt
---|---|---
NAVN | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
