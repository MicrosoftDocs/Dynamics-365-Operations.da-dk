---
title: Rekrutteringsanmodningsuddannelse
description: Dette emne beskriver rekrutteringsforespørgselsenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126068"
---
# <a name="recruiting-request-education"></a>Rekrutteringsanmodningsuddannelse

Dette emne beskriver rekrutteringsforespørgselsenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Betegnelse

Beskriver uddannelseskrav til en RecruitingRequest.

### <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Uddannelsesenheds-id for rekrutteringsanmodning**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydig identifikation af enhedsposten for rekrutteringsforespørgsel. |
| **Rekrutteringsanmodnings-id**<br>mshr_recruitingrequestid<br>*Streng* | Skriv én gang<br>Påkrævet | Det entydige id, der kan læses af den relaterede rekrutteringsanmodning. |
| **Værdi for rekrutteringsanmodnings-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity | Systemgenereret entydig id, der kan læses af den relaterede rekrutteringsanmodning. |
| **Uddannelsesniveau-id**<br>mshr_educationlevelid<br>*Streng* | Skriv én gang<br>Påkrævet | Påkrævet uddannelsesniveau. |
| **Værdi for uddannelsesniveau-id**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmeducationlevelentityid of mshr_hcmeducationlevelentity | Systemgenereret entydigt id til påkrævet niveau for uddannelse. |
| **Beskrivelse af uddannelsesniveau**<br>mshr_educationleveldescription<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Beskrivelsen af det niveau, der kræves til færdigheden. |
| **Id for uddannelsesdisciplin**<br>mshr_educationdisciplinedescription<br>*Streng* | Skriv én gang<br>Påkrævet | Uddannelsesområdet. |
| **Id for uddannelsesdisciplinværdi**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity | Systemgenereret entydigt id til område for uddannelsesområde. |
| **Beskrivelse af uddannelsesområde**<br>mshr_educationdisciplinedescription<br>Streng | Skrivebeskyttet<br>Påkrævet | Beskrivelsen af uddannelsesområde. |
| **Dataområde-id**<br>mshr_dataareaid<br>*Streng* | Læse/skrive<br>Valgfri | Angiver den juridiske enhed (regnskabet).|
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Sammensætning af værdien for rekrutteringsanmodning, uddannelsesniveau-id og uddannelses-id som en anden metode, der identificerer posten entydigt. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]