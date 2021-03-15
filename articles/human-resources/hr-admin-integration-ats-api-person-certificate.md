---
title: Personcertifikat
description: Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125347"
---
# <a name="person-certificate"></a>Personcertifikat

Dette emne beskriver personcertifikatenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersoncertificateentity

## <a name="description"></a>Betegnelse

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

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Enheds-id for personcertifikat**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet | Systemgenereret entydig identifikation af enhedsposten for personcertifikat. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Part-id (person) for kandidaten. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Certifikattype-id**<br>mshr_certificatetypeid<br>*Streng* | Læse/skrive<br>Påkrævet |  Id for den certifikattype, der er defineret i Human Resources. |
| **Værdi for certifikattype-id**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity | Systemgenereret entydig identifikation af certifikattypen i den tilknyttede enhed. |
| **Startdato**<br>mshr_startdate<br>*Datetime* | Læse/skrive<br>Påkrævet | Den dato, hvor certifikatet blev udstedt. |
| **Slutdato**<br>mshr_enddate<br>*Datetime* | Læse/skrive<br>Valgfri | Den dato, hvor certifikatet udløber. |
| **Notater**<br>mshr_notes<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet |  Felt, der bruges som id for enhedsposten. Kombination af partnummer, certifikattype-id og startdato. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]