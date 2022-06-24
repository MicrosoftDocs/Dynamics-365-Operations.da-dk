---
title: Personscreening
description: Denne artikel beskriver personscreeningenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: e9b2bbda8f8191f592462f4fbd1902e7274cf7f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907634"
---
# <a name="person-screening"></a>Personscreening


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver personscreeningenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpersonscreeningentity

## <a name="description"></a>Beskrivelse

Denne enhed beskriver de screeninger, som en kandidat har bestået eller skal bestået for ansættelsen.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id for personscreening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Entydigt primært id for personscreeningpost. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Påkrævet | Det partnummer (person), der er tilknyttet kandidaten. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Screeningstype-id**<br>mshr_screeningtypeid<br>*Streng* | Læse/skrive<br>Påkrævet<br>Fremmed nøgle: ScreeningType | Id for den screeningtype, der er defineret i Human Resources. |
| **Værdi for screeningstype-id**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity | Systemgenereret entydig identifikation for screeningstypeposten i den tilknyttede enhed. |
| **Ønsket af**<br>mshr_requiredby<br>*Datetime* | Læse/skrive<br>Valgfri | Den dato, hvor screeningen skal være fuldført. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus indstilling*<br>Læse/skrive<br>Påkrævet | Angiver kandidatens status for screeningen. |
| **Fuldførelsesdato**<br>mshr_completeddate<br>*Datetime* | Læse/skrive<br>Valgfri | Datoen, hvor screeningen blev fuldført. |
| **Notater**<br>mshr_note<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
