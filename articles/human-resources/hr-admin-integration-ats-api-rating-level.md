---
title: Rangeringsniveau
description: Dette emne beskriver vurderingsniveauenheden for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054830"
---
# <a name="rating-level"></a>Rangeringsniveau

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver vurderingsniveauenheden for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmratinglevelentity

## <a name="description"></a>Beskrivelse

Denne enhed giver de tilgængelige vurderingsniveauer for færdigheder. Vurderingsniveauer gælder på tværs af alle juridiske enheder.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Vurdering for enheds-id**<br>mshr_hcmratinglevelentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Systemgenereret entydigt id til niveauet. |
| **Vurderingsniveau-id**<br>mshr_ratinglevelid<br>*Streng* | Læse/skrive<br>Påkrævet | Brugerlæsbar entydig identifikation af niveau. |
| **Vurderingsmodel-id**<br>mshr_ratingmodelid<br>*Streng* | Læse/skrive<br>Påkrævet | Den vurderingsmodel, som vurderingsniveauet tilhører. |
| **Vurderingsmodel for enheds-id**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity | Det systemgenererede id for den vurderingsmodel, som vurderingsniveauet tilhører. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskrivelsen af vurderingsniveauet. |
| **Faktor**<br>mshr_factor<br>*Heltal* | Læse/skrive<br>Påkrævet | Faktoren for vurderingsniveauet. Når du sammenligner varer med et andet antal vurderingsniveauer, anvendes faktoren til at normalisere resultaterne. Værdien skal være et heltal mellem 0 og 9. |
| **Bemærk!**<br>mshr_note<br>*Streng* | Læse/skrive<br>Valgfri | Eventuelle notater, der er tilknyttet vurderingsniveauet. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som id for enhedsposten. Kombination af vurderingsniveau-id og vurderingsmodel-id. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]