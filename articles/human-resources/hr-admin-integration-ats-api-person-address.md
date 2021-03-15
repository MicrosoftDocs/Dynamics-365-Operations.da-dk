---
title: Personadresse
description: Dette emne beskriver personadressen til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9911362ff8260860864cfe24f0b60f59adb77186
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125876"
---
# <a name="person-address"></a>Personadresse

Dette emne beskriver personadressen til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonaddressentities

## <a name="description"></a>Betegnelse

Enheden indeholder listen over postadresser for kandidatposter.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personadresseenheds-id**<br>mshr_hcmpersonaddressentityid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydigt id til enhedsposten. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Id for den tilknyttede partpost (person). |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Lokations-id**<br>mshr_locationid<br>*Streng* | Læse/skrive<br>Påkrævet | Lokations-id for adressepost. Konfigurer i enheden mshr_logisticspostaladdresslocationcdsentity. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | En beskrivelse af kandidatens adresse. |
| **Roller**<br>mshr_roles<br>*Streng* | Læse/skrive<br>Påkrævet | De roller, der er tildelt denne adresse. Du kan markere mere end en rolle. Hver rolle skal adskilles med et semikolon. Gyldige værdier i enheden mshr_logisticslocationroleentity. |
| **Gade**<br>mshr_street<br>*Streng* | Læse/skrive<br>Valgfri | Gadenummer. |
| **By**<br>mshr_city<br>*Streng* | Læse/skrive<br>Valgfri | Adressens by. Konfigurer i enheden mshr_logisticsaddresscityentity. |
| **Delstat**<br>mshr_state<br>*Streng* | Læse/skrive<br>Valgfri | Staten i adressen. Konfigurer i enheden mshr_logisticsaddressstateentity. |
| **Region**<br>mshr_county<br>*Streng* | Læse/skrive<br>Valgfri | Regionen i adressen. Konfigurer i enheden mshr_logisticsaddresscountyentity. |
| **Postnummer**<br>mshr_zipcode<br>*Streng* | Læse/skrive<br>Valgfri | Postnummeret i adressen. Konfigurer i enheden mshr_logisticsaddresspostalcodeentity. |
| **Id for land/område**<br>mshr_countryregionid<br>*Streng* | Læse/skrive<br>Valgfri | Landet eller området i adressen. |
| **Id-værdi for land/område**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_logisticaddresscountryregionentityid af mshr_logisticsaddresscountryregionentity | Systemgenereret entydig identifikator for land/område til adressen. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om denne adresse er den primære adresse for personen med den definerede rolle. |
| **Er privat**<br>mshr_isprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om denne adresse er en privat adresse for personen. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som primært id for enhedsposten. Kombination af partnummer og lokalitets-id. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]