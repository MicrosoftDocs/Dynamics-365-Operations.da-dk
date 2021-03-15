---
title: Kontakt til part
description: Dette emne beskriver partkontaktenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 38f53d402ebe9f9f358281dd3996797a20923056
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125467"
---
# <a name="party-contact"></a>Kontakt til part

Dette emne beskriver partkontaktenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpartycontactentities

## <a name="description"></a>Betegnelse

Denne enhed beskriver kandidatens kontaktoplysninger, herunder telefon-, e-mail- og social mediekonti.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Enheds-id for partkontakt**<br>mshr_dirpartycontactentityid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydigt id til enhedsposten. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Id for den tilknyttede partpost (person). |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Lokations-id**<br>mshr_locationid<br>*Streng* | Læse/skrive<br>Påkrævet | Lokations-id for adressepost. Konfigurer i enheden mshr_logisticspostaladdresslocationcdsentity. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskrivelse af kontaktoplysningerne. |
| **Type**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype indstilling* | Læse/skrive<br>Påkrævet | Kontaktoplysningstype. |
| **Lande-/områdekode**<br>mshr_countryregioncode<br>*Streng* | Læse/skrive<br>Valgfri | Landet eller området i adressen. |
| **Locator**<br>mshr_locator<br>*Streng* | Læse/skrive<br>Valgfri | Kontaktoplysninger. Hvis typen f.eks. er **e-mail-adresse**, indeholder dette felt kandidatens e-mailadresse. |
| **Lokalnummer til Locator**<br>mshr_locatorextension<br>*Streng* | Læse/skrive<br>Valgfri | Lokalnummer til Locator. Hvis typen f.eks. er **Telefon**, vil denne egenskab indeholde lokalnummeret for telefonnummeret. |
| **Er mobil**<br>mshr_ismobile<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om telefon er et mobilnummer. |
| **Er en chatbesked**<br>mshr_isinstantmessage<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om telefon er aktiveret til chatbeskeder. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Bestemmer den primære kontaktperson for kontaktpersontypen. Der må kun være én primær post pr. kontaktpersontype. |
| **Er privat**<br>mshr_isprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Påkrævet | Angiver, om denne adresse er en privat adresse for personen. |
| **Formål**<br>mshr_purpose<br>*Streng* | Læse/skrive<br>Valgfri | Formål/rolle med kontaktoplysninger. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som primært id for enhedsposten. Kombinationen af partnummer, type, beskrivelse og locator. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]