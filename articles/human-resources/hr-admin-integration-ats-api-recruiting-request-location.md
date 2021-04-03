---
title: Lokation af rekrutteringsanmodning
description: Dette emne beskriver rekrutteringsforespørgslen til lokationsenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9a3b47c76094adb6c601daf2f9583116255b0a99
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465936"
---
# <a name="recruiting-request-location"></a>Lokation af rekrutteringsanmodning

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver rekrutteringsforespørgslen til lokationsenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Beskrivelse

Listen over lokationer, der er defineret som steder, hvor de rekrutterede medarbejdere skal arbejde med ansættelser. Disse er lokationer, der er oprettet på tværs af juridiske enheder.

### <a name="json-representation"></a>JSON-repræsentation

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Lokations-id**<br>mshr_locationid<br>*Streng* | Skriv én gang<br>Påkrævet | Systemgenereret, brugerlæsbar identifikation til rekrutteringslokation. |
| **Lokation til rekrutteringsanmodning**<br>mshr_recruitingrequestlocationid<br>*Streng* | Skriv én gang<br>Påkrævet | Brugerdefineret entydig identifikation af rekrutteringslokationen. |
| **Rekrutteringsanmodning til lokationsenheds-id**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydig identifikation af rekrutteringsanmodning til lokationsposten. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskrivelse af lokationen. |
| **Id for land/område**<br>mshr_countryregionid<br>*Streng* | Skrivebeskyttet<br>Valgfri | Angiver, hvilket land eller område kandidaten er statsborger i. |
| **Id-værdi for land/område**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_logisticaddresscountryregionentityid af mshr_logisticsaddresscountryregionentity | Systemgenereret entydig identifikator for land/område til adressen. |
| **Postnummer**<br>mshr_zipcode<br>*Streng* | Skrivebeskyttet<br>Valgfri | Postnummer. |
| **Gade**<br>mshr_street<br>*Streng* | Skrivebeskyttet<br>Valgfri | Adresse-gade. |
| **By**<br>mshr_city<br>*Streng* | Skrivebeskyttet<br>Valgfri | By. |
| **Delstat**<br>mshr_state<br>*Streng* | Skrivebeskyttet<br>Valgfri | Delstat eller provins. |
| **Region**<br>mshr_county<br>*Streng* | Skrivebeskyttet<br>Valgfri | Område: |
| **Telefon**<br>mshr_telephone<br>*Streng* | Læse/skrive<br>Valgfri | Lokationens telefonnummer. |
| **E-mail**<br>mshr_email<br>*Streng* | Læse/skrive<br>Valgfri | E-mailadresse. |
| **Internetadresse**<br>mshr_internetaddress<br>*Streng* | Læse/skrive<br>Valgfri | URL-adressen til lokationswebstedet. |
| **Dataområde-id**<br>mshr_dataareaid<br>*Streng* | Læse/skrive<br>Valgfri | Angiver den juridiske enhed (regnskabet). |
| **Værdi for dataområde-id**<br>_mshr_dataareaid_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: cdm_companyid af cdm_company-enhed | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]