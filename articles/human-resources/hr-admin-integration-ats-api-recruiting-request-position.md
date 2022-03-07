---
title: Stilling til rekrutteringsanmodning
description: Dette emne beskriver rekrutteringsforespørgslen til stillingsenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 76c96b722c2be76d9aff999633ffd30a576a1614bdc5e4cc4a24fb17d92fe22a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758730"
---
# <a name="recruiting-request-position"></a>Stilling til rekrutteringsanmodning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver rekrutteringsforespørgslen til stillingsenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Beskrivelse

Beskriver den stilling eller stillinger, der skal besættes for en rekrutteringsanmodning. Det er valgfrit, om du vil føje en stilling til anmodningen om rekruttering. Egenskaberne for stillingen er skrivebeskyttede, da stillingsegenskaberne ikke bør være forskellige i rekrutteringsanmodningen, end de er i stillingsmasterposten. Hvis egenskaberne skal ændres, skal det ske i stillingsmasterposten, før stillingen føjes til rekrutteringsanmodningen.

### <a name="json-representation"></a>JSON-repræsentation
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Rekrutteringsanmodning til stillingsenheds-id**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet |    Systemgenereret id, der kan læses af rekrutteringsanmodningens stillingspost. |
| **Rekrutteringsanmodnings-id**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Påkrævet | Det entydige id, der kan læses af brugerens rekrutteringsanmodning. |
| **Værdi for rekrutteringsanmodnings-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity-enhed | Systemgenereret id, der kan læses af den rekrutteringsanmodning, som stillingen tildeles. |
| **Stillings-id**<br>mshr_positionid<br>*Streng* | Skriv én gang<br>Påkrævet | Det entydige id, der kan læses af stillingen. |
| **Stillings-id-værdi**<br>_mshr_fk_position_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity-enhed | Systemgenereret id for stillingen. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Stillingsbeskrivelsen. |
| **Stillingstype-id**<br>mshr_positiontypeid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Det entydige id, der kan læses af stillingstypen vedrørende denne stilling. |
| **Værdi for stillingstype-id**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmpositiontypeentityid of mshr_hcmpositiontypeentity-enhed | Systemgenereret entydige id for stillingstypen vedrørende denne stilling. |
| **Status**<br>mshr_status<br>*RecruitingRequestPositionStatus*-indstilling | Læse/skrive<br>Påkrævet | Status for stillingen for rekrutteringsanmodningen. |
| **Afdelingsnummer**<br>mshr_departmentnumber<br>*Streng* | Skrivebeskyttet<br>Valgfri<br> | Afdelingsnummeret for stillingen. |
| **Værdi for afdelings-id**<br>_mshr_fk_department_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_omdepartmententityid of mshr_omdepartmententity-enhed | Systemgenereret entydige id for afdelingen vedrørende denne stilling. |
| **Rapporterer til stillings-id**<br>mshr_reportstopositionid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Det brugerlæsbare id for den stilling, som de rekrutterede stillingsrapporter i organisationshierarkiet. |
| **Rapporterer til værdi for stillings-id**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity-enhed | Det systemgenererede id for den stilling, som de rekrutterede stillingsrapporter til. |
| **Rapporterer til personalenummer**<br>mshr_reportstopersonnelnumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Arbejder-id for den arbejder, som den ansatte ansøger skal rapporterer til. |
| **Rapporterer til værdi til arbejder-id**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmworkerbaseentityid af mshr_hcmworkerbaseentity-enhed | Systemgenereret id for den arbejder, som den ansatte ansøger skal rapporterer til. |
| **Økonomisk dimension**<br>mshr_financialdimension<br>*Streng* | Skrivebeskyttet<br>Valgfri | Den økonomiske dimension (f.eks. bærer), der er tildelt stillingen. Den økonomiske dimension tildeles hver stilling pr. juridisk enhed. Der er adgang til de ressourcer, der er defineret i dimensioner, via mshr_dimattributeomcostcenterentity-enheden. |
| **Dataområde-id**<br>mshr_dataareaid<br>*Streng* | Læse/skrive<br>Valgfri | Angiver den juridiske enhed (firmaet) for stilling til rekrutteringsanmodning. |
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden) til stilling til rekrutteringsanmodning. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Sammensætning af værdien for rekrutteringsanmodning og stillings-id som en anden metode, der identificerer posten entydigt. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]