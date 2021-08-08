---
title: Organisationshierarki i Dataverse
description: I dette emne beskrives integrationen af organisatoriske data mellem Finance and Operations-apps og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1ad3bc4eef1650b927d9f6dd699f788994c7e87
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542581"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarki i Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Da Dynamics 365 Finance er et økonomisystem, er *organisation* kernekonceptet, og systemopsætningen starter med konfigurationen af et organisationshierarki. Virksomheders økonomi kan derefter spores på organisationsniveau og også på alle niveauer i organisationshierarkiet.

Selvom Dataverse ikke har konceptet med et organisationshierarki, har det et par løse begreber, f.eks. samlet salgsindtægt. Som en del af Dataverse-integrationen føjes organisationshierarkiets datastruktur til Dataverse.

## <a name="data-flow"></a>Dataflow

Et virksomhedsøkosystem, der består af Finance and Operations-apps og Dataverse, vil fortsat have et organisationshierarki. Dette organisationshierarki er baseret på Finance and Operations-apps, men det vises i Dataverse til informations- og udvidelsesformål. I følgende illustration vises de oplysninger om organisationshierarkiet, der vises i Dataverse som envejs dataflow fra Finance and Operations-apps til Dataverse.

![Billede af arkitektur.](media/dual-write-data-flow.png)

Organisationshierarkiets tabeltilknytninger er tilgængelige for envejssynkronisering af data fra Finance and Operations-apps til Dataverse.

## <a name="templates"></a>Skabeloner

Produktoplysninger indeholder alle de oplysninger, der er knyttet til produktet og dets definition, f. eks. produktdimensionerne eller sporings-og lagringsdimensionerne. Som følgende tabel viser, oprettes der en samling af tabeltilknytninger for at synkronisere produkter og relaterede oplysninger.

Finance and Operations-apps | Kundeengagementapps     | Betegnelse
-----------------------|--------------------------------|---
[Juridiske enheder](mapping-reference.md#102) | cdm_companies | Giver mulighed for tovejssynkronisering af juridiske enhedsoplysninger (firma).
[Juridiske enheder](mapping-reference.md#142) | msdyn_internalorganizations |
[Driftsenhed](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisationshierarki - publiceret](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Denne skabelon giver mulighed for envejssynkronisering af tabellen Publiceret organisationshierarki.
[Formål med organisationshierarkier](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Formål med organisationshierarkier.
[Type af organisationshierarki](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Denne skabelon giver mulighed for envejssynkronisering af tabellen Type af organisationshierarkier.

## <a name="internal-organization"></a>Intern organisation

Interne organisationsoplysninger i Dataverse kommer fra to tabeller, **Driftsenhed** og **Juridiske enheder**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
