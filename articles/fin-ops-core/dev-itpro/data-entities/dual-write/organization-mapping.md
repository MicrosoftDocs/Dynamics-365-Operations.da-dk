---
title: Organisationshierarki i Dataverse
description: I dette emne beskrives integrationen af organisationsdata mellem Finans og drift-apps og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9174612743c68595d12dd223f0932ace1857c0fb
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358358"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarki i Dataverse

[!include [banner](../../includes/banner.md)]



Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki. Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.

Selvom Dataverse ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt. Som en del af Dataverse-integrationen føjes organisationshierarkiets datastruktur til Dataverse.

## <a name="data-flow"></a>Dataflow

En virksomhedsøkosystem, der består af Finans og drift-apps og Dataverse, vil fortsat have et organisationshierarki. Dette organisationshierarki er baseret på Finans og drift-apps, men det vises i Dataverse til informations- og udvidelsesformål. I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Dataverse som envejs dataflow fra Finans og drift-apps til Dataverse.

![Billede af arkitektur.](media/dual-write-data-flow.png)

Organisationshierarkiets tabeltilknytninger er tilgængelige for envejs synkronisering af data fra Finans- og driftsapps til Dataverse.

## <a name="templates"></a>Skabeloner

En organisation er en grupper personer, der arbejder sammen for at udføre en forretningsproces eller nå et mål. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af. Du kan definere følgende typer interne organisationer: juridiske enheder, driftsenheder og team. Som det fremgår af tabellen nedenfor, oprettes der en samling tabeltilknytninger til synkronisering af juridiske enheder, driftsenheder og relaterede oplysninger om organisationshierarki.

Finans og drift-apps | Kundeengagementapps     | Beskrivelse
-----------------------|--------------------------------|---
[Juridiske enheder](mapping-reference.md#102) | cdm_companies | 
[Juridiske enheder](mapping-reference.md#142) | msdyn_internalorganizations |
[Driftsenhed](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisationshierarki - publiceret](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Denne skabelon giver mulighed for envejssynkronisering af tabellen Publiceret organisationshierarki.
[Formål med organisationshierarkier](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Formål med organisationshierarkier.
[Type af organisationshierarki](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Type af organisationshierarkier.

## <a name="internal-organization"></a>Intern organisation

Interne organisationsoplysninger i Dataverse kommer fra to tabeller, **Driftsenhed** og **Juridiske enheder**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
