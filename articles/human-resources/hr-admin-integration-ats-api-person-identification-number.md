---
title: Personidentifikationsnummer
description: Dette emne beskriver enheden til personidentifikationsnummer for Dynamics 365 Human Resources.
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
ms.openlocfilehash: ef33e3922ca676b1312a3d60ae07aa2fe2828056
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055166"
---
# <a name="person-identification-number"></a>Personidentifikationsnummer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver enheden til personidentifikationsnummer for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Beskrivelse

Denne enhed beskriver kandidatens identifikationsnumre. Det giver API-forbrugeren mulighed for at skrive identifikationsnumre, som f.eks. personnumre eller pasnumre, til kandidatposten. Identifikationsnumrene findes på arbejderposten, men ikke i kandidatposten. Et integrationsprogram kan skrive værdierne til Human Resource-databasen, men tallene kan ikke ses i Human Resource, før kandidatens arbejderpost er oprettet.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id for personidentifikationsnummer**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Entydigt primært id for personidentifikationsnummerpost. |
| **Posttype**<br>mshr_entrytype<br>*Streng* | Læse/skrive<br>Valgfri | Fri værdi, der skal referere til posttypen for identifikationsnummeret. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelsen af identifikationsnummeret. |
| **Udløbsdato**<br>mshr_expirationdate<br>*Datetime* | Læse/skrive<br>Valgfri | Den dato, hvor identifikationsnummeret eller det tilknyttede dokument udløber. |
| **Er primær**<br>mshr_isprimary<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Definerer, om identifikationsnummeret er den primære post for personen for denne identifikationstype. |
| **Identifikationsnummer**<br>mshr_identificationnumber<br>*Streng* | Læse/skrive<br>Påkrævet | Identifikationsnummeret. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Id for part (person), der ejer identifikationsnummer. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid af mshr_dirpersonentity-enhed | Det entydig id for parten (person). |
| **Identifikationstype-id**<br>mshr_identificationtypeid<br>*Streng* | Læse/skrive<br>Påkrævet | Typens identifikationsnummer. |
| **Værdi Identifikationstype-id**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmidentificationtypeentityid of mshr_hcmidentificationtypeentity entity | Systemgenereret entydigt id til identifikationstype. |
| **Udstedende agentur-id**<br>mshr_issuingagencyid<br>*Streng* | Læse/skrive<br>Valgfri | Den myndighed eller organisation, der har udstedt identifikationsnummeret. |
| **Værdi for udstedende agentur-id**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmissuingagencyentityid of mshr_hcmissuingagencyentity entity | Systemgenereret entydigt id til identifikationsnummer for type for udstedende agentur . |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som id for enhedsposten. Kombination af partnummer, identifikatoinstype-id og identifikationsnummer. |
| **Udstedelsesdato**<br>mshr_issuedate<br>*Dato* | Læse/skrive<br>Valgfri | Den dato, hvor identifikationsnummeret blev udstedt. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]