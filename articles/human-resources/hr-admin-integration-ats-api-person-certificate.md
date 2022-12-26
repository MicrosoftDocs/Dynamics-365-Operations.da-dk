---
title: Personcertifikat
description: Denne artikel beskriver personcertifikatenheden til Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887311"
---
# <a name="person-certificate"></a>Personcertifikat


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver personcertifikatenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersoncertificateentity

## <a name="description"></a>Beskrivelse

Denne enhed beskriver en kandidats faglige certifikater.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivende tekst |
| --- | --- | --- |
| **Certifikattype-id**<br>mshr_certificatetypeid<br>*Streng* | Læse/skrive<br>Påkrævet |  Id for den certifikattype, der er defineret i Human Resources. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Læse/skrive<br>Obligatorisk | Den dato, hvor certifikatet blev udstedt. |
| **Slutdato**<br>mshr_enddate<br>*Datetime* | Læse/skrive<br>Valgfri | Den dato, hvor certifikatet udløber. |
| **Notater**<br>mshr_notes<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Obligatorisk | Part-id (person) for kandidaten. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Obligatorisk |  Felt, der bruges som id for enhedsposten. Kombination af partnummer, certifikattype-id og startdato. |
| **Værdi for certifikattype-id**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity | Systemgenereret entydig identifikation af certifikattypen i den tilknyttede enhed. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Enheds-id for personcertifikat**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydig identifikation af enhedsposten for personcertifikat. |




## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
