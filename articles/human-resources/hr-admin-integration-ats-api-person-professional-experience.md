---
title: Persons erhvervserfaring
description: Dette emne beskriver enheden til persons erhvervserfaring for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7cb728a29ccf6c23a227e63edd6bb5226d2ffdd0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053701"
---
# <a name="person-professional-experience"></a>Persons erhvervserfaring

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver enheden til persons erhvervserfaring for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Beskrivelse

Denne enhed beskriver en kandidats erhvervserfaring eller arbejdshistorik.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id for persons erhvervserfaring**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydigt id til enhedsposten. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Entydig identifikation af kandidatens personpost. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret entydigt id til persons enhedspost. |
| **Arbejdsgiverstilling**<br>mshr_employerposition<br>*Streng* | Læse/skrive<br>Påkrævet | Kandidatens stillingsbetegnelse, når ansøgeren er under ansættelse. |
| **Arbejdsgivernavn**<br>mshr_employername<br>*Streng* | Læse/skrive<br>Påkrævet | Arbejdsgiverens navn. |
| **Arbejdsgiverlokation**<br>mshr_employerlocation<br>*Streng* | Læse/skrive<br>Valgfri | Arbejdsgiverens placering. Maks. længde: 60. Der defineres eller kræves ikke et bestemt format. |
| **Telefon**<br>mshr_phone<br>*Streng* | Læse/skrive<br>Valgfri | Arbejdsgivers telefonnummer. |
| **URL**<br>mshr_url<br>*Streng* | Læse/skrive<br>Valgfri | URL-adressen på arbejdsgiverens websted. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Læse/skrive<br>Påkrævet | Startdatoen for kandidatens ansættelse. |
| **Slutdato**<br>mshr_enddate<br>*Datetime* | Læse/skrive<br>Valgfri | Slutdatoen for kandidatens ansættelse, eller null, hvis kandidaten stadig er ansat her. |
| **Tillad kontakt til arbejdsgiver**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno indstilling* | Læse/skrive<br>Valgfri | Angiver, om kandidaten tillader kontakt til den tidligere arbejdsgiver. |
| **Notater**<br>mshr_note<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejderen eller ansættelseschefen. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Felt, der bruges som primært id for enhedsposten. Kombinationen af partnummer, startdato, arbejdsgiverstilling og arbejdsgivernavn. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]