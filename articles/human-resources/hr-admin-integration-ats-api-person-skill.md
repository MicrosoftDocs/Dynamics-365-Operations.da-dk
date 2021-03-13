---
title: Personkompetence
description: Dette emne beskriver personkompetenceenheden til Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b6bcbbd1203f4e9e80f6c5264cf4d5ea7d0970fc
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126092"
---
# <a name="person-skill"></a>Personkompetence

Dette emne beskriver personkompetenceenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonskillentity

## <a name="description"></a>Betegnelse

Denne enhed beskriver en kandidats færdigheder.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personkompetenceenheds-id**<br>mshr_hcmpersonskillentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydigt id til enhedsposten. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet |   Id for den tilknyttede partpost (person). |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Godkender**<br>mshr_certifier<br>*Streng* | Læse/skrive<br>Valgfri | Personalenummeret på den arbejder, der har godkendt denne færdighed. |
| **Værdi for godkender-id**<br>_mshr_fk_certifier_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmworkerentityid of mshr_hcmworkerentity | Systemgenereret entydig identifikation af arbejderposten for den arbejder, der har certificeret færdigheden. |
| **Kompetence-id**<br>mshr_skillid<br>*Streng* | Læse/skrive<br>Påkrævet | Id for den kompetence, der er defineret i Human Resources. |
| **Kompetence-id-værdi**<br>_mshr_fk_skill_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmskillentityid of mshr_hcmskillentity | Det systemgenererede id for denne valgte kompetence. |
| **Års erfaring**<br>mshr_yearsofexperience<br>*Decimal* | Læse/skrive<br>Valgfri | Kandidatens erfaring har denne færdighed. |
| **Vurderings-id**<br>mshr_ratingid<br>*Streng* | Læse/skrive<br>Påkrævet | Vurderingsskalatypen. For denne enhed er værdien **Færdigheder**. |
| **Niveautype**<br>mshr_leveltype<br>*mshr_hrmskillleveltype indstilling* | Læse/skrive<br>Påkrævet | En type kategorisering for det niveau, der er tildelt færdigheden. |
| **Niveau-id**<br>mshr_levelid<br>*Streng* | Læse/skrive<br>Påkrævet | Id for det vurderingsniveau, som kandidaten har for denne færdighed. |
| **Vurdering for uddannelsesniveau-id**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity | Det systemgenererede id for vurderingsniveau. |
| **Niveaudato**<br>mshr_leveldate<br>*Datetime* | Læse/skrive<br>Påkrævet | Den dato, hvor kandidaten blev vurderet med færdigheden. |
| **Vurderingsniveau-eksaminator**<br>mshr_ratinglevelexaminer<br>*Streng* | Læse/skrive<br>Valgfri | Personalenummeret på den arbejder, der har vurderet kandidaten. |
| **Værdi for eksaminator-id vurderingsniveau**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmworkerentityid of mshr_hcmworkerentity | Det systemgenererede id for den arbejder, der undersøgt kandidatens færdighedsniveau. |
| **Bekræftet**<br>mshr_verified<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om den vurderede færdighed er blevet bekræftet. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som id for enhedsposten. Kombination af partnummer, niveautype, værdigheds-id og niveaudato. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

