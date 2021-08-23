---
title: Rekrutteringsanmodningsfærdighed
description: Dette emne beskriver enheden til rekrutteringsanmodningsfærdigheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9347b6f2e18c7ec12c18137846507532fc9fcc3149a3638d12c070dc848a1fc7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712115"
---
# <a name="recruiting-request-skill"></a>Rekrutteringsanmodningsfærdighed

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver enheden til rekrutteringsanmodningsfærdigheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Beskrivelse

Beskriver færdighedskrav til en RecruitingRequest.

### <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id til rekrutteringsanmodningsfærdighed**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydig identifikation af posten **Rekrutteringsanmodningsfærdighed**. |
| **Rekrutteringsanmodnings-id**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Påkrævet | Det entydige id, der kan læses af den tilknyttede rekrutteringsanmodning. |
| **Værdi for rekrutteringsanmodnings-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br> Fremmed nøgle: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity-enhed | Systemgenereret entydig id, der kan læses af den tilhørende rekrutteringsanmodning. |
| **Kompetence-id**<br>mshr_skillid<br>*Streng*<br> | Skriv én gang<br>Påkrævet | Det entydige id, der kan læses af den krævede færdighed. |
| **Kompetence-id-værdi**<br>_mshr_fk_skill_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmskillentityid of mshr_hcmskillentity-enhed | Systemgenereret entydigt id til påkrævet færdighed. |
| **Vurderingsniveau-id**<br>mshr_ratinglevelid<br>*Streng* | Skriv én gang<br>Valgfri | Den ønskede værdi på færdighedsniveau, der er valgt for jobbet, baseret på den vurderingsmodel, der er tildelt færdigheden. |
| **Vurdering for uddannelsesniveau-id**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmratinglevelentityid of mshr_hcmratinglevelentity-enhed | Systemgenereret entydigt id til niveauet. |
| **Beskrivelse af færdighed**<br>mshr_skilldescription<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Beskrivelse af færdighed. |
| **Beskrivelse af vurderingsniveau**<br>mshr_ratingleveldescription<br>*Streng* | Skrivebeskyttet<br>Valgfri | Beskrivelse af valgt færdighedsniveau. |
| **Dataområde-id**<br>mshr_dataareaid<br>*Streng* | Læse/skrive<br>Valgfri | Angiver den juridiske enhed (regnskabet). |
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Sammensætning af værdien for rekrutteringsanmodning og færdigheds-id som en anden metode, der identificerer posten entydigt. |
| **Vurderingsmodel-id**<br>mshr_ratingmodelid<br>*Streng* | Læse/skrive<br>Påkrævet | Den vurderingsmodel, der bruges til vurdering af færdigheden. |
| **Id-værdi for vurderingsmodel**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity-enhed | Systemgenereret entydig identifikation af den vurderingsmodel, der bruges til vurdering af færdigheden. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]