---
title: Personuddannelse
description: Dette emne beskriver personuddannelsesenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: cfa05fe6816c6b24034f8f015bf6e42d665ef1dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466490"
---
# <a name="person-education"></a>Personuddannelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver personuddannelsesenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersoneducationentity

## <a name="description"></a>Beskrivelse

Denne enhed indeholder uddannelseshistorikken for den person, der er kandidat. Uddannelsen er knyttet til personens post, hvilket gør det muligt, at uddannelsen kan knyttes til andre roller, der er oprettet for personen, ud over kandidatposten (arbejder, kontrahent mm.).

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id for personuddannelse**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydigt id til persons uddannelsesenhedspost. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Entydig identifikation af kandidatens personpost (person). |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Det systemgenererede entydige id for kandidatens partpost (person). |
| **Krediteringsbase**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis indstilling* | Læse/skrive<br>Valgfri | Krediteringsgrundlaget for uddannelsesgraden. |
| **Kreditering afsluttet**<br>mshr_creditscompleted<br>*Decimal* | Læse/skrive<br>Valgfri | Antallet af krediteringer, der er fuldført for uddannelsen. |
| **Optjente krediteringer**<br>mshr_creditsearned<br>*Decimal* | Læse/skrive<br>Valgfri | Antallet af optjente krediteringer for uddannelsesposten for en igangværende uddannelse. |
| **Påkrævede krediteringer**<br>mshr_creditsneeded<br>*Decimal* | Læse/skrive<br>Valgfri | Det antal krediteringer, der kræves af en igangværende uddannelse. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Valgfri | En beskrivelse af kandidatens karakter. |
| **Uddannelsesniveau-id**<br>mshr_educationlevelid<br>*Streng* | Læse/skrive<br>Valgfri | Id for uddannelsesniveauet. | 
| **Værdi for uddannelsesniveau-id**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmeducationdegreeentityid af mshr_hcmeducationdegreeentity enhed | Systemgenereret entydigt id til posten til uddannelseskarakter. Dette id angiver, hvilken karakter og uddannelsesniveau der er defineret for organisationen. |
| **Id for uddannelsesdisciplin**<br>mshr_educationdisciplineid<br>*Streng* | Læse/skrive<br>Påkrævet<br>Fremmed nøgle: EducationDiscipline | Id for uddannelsesdisciplin. |
| **Id for uddannelsesdisciplinværdi**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity | Systemgenereret entydigt id for uddannelsesdisciplinens uddannelsespost. |
| **Sekundært**<br>mshr_secondaryemphasis<br>*Streng* | Læse/skrive<br>Valgfri | Den sekundære vægtning af det optjente niveau. |
| **Uddannelsesinstitution-id**<br>mshr_educationinstitutionid<br>*Streng* | Læse/skrive<br>Valgfri | Id for uddannelsesstedet. |
| **Værdi for uddannelsesinstitution-id**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Skrivebeskyttet<br>Valgfri<br>Fremmed nøgle: mshr_hcmeducationinstitutionentityid of mshr_hcmeducationinstitutionentity | Systemgenereret id for uddannelsesstedet. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Læse/skrive<br>Valgfri | Startdatoen for uddannelsen for den optjente uddannelseskarakter. |
| **Slutdato**<br>mshr_enddate<br>*Datetime* | Læse/skrive<br>Påkrævet | Den dato, hvor legitimationsoplysningerne blev udstedt. |
| **Varighed**<br>mshr_duration<br>*Decimal* | Læse/skrive<br>Valgfri | Uddannelsespostens varighed. |
| **Enhed for varighed**<br>mshr_durationunit<br>*mshr_periodunit indstilling* | Læse/skrive<br>Valgfri | Den tidsenhed, der er knyttet til uddannelsespostens varighed. |
| **Karaktergennemsnit**<br>mshr_gradepointaverage<br>*Decimal* | Læse/skrive<br>Valgfri | Det opnåede karaktergennemsnit for uddannelsen. |
| **Karakterskala**<br>mshr_gradescale<br>*Streng* | Læse/skrive<br>Valgfri | Det anvendte karaktergennemsnit for uddannelsen. |
| **Notater**<br>mshr_notes<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejderen eller ansættelseschefen. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som andet id for enhedsposten. Kombination af partnummer, uddannelses-id, uddannelsesinstitution-id og uddannelsesniveau-id. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]