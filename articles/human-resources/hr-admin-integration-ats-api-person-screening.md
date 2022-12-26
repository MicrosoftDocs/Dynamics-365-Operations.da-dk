---
title: Personscreening
description: Denne artikel beskriver personscreeningenheden til Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831884"
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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivende tekst |
| --- | --- | --- |
| **Notater**<br>mshr_note<br>*Streng* | Læse/skrive<br>Valgfri | Noter til brug af rekrutteringsmedarbejdere eller ansættelseschefer. |
| **Ønsket af**<br>mshr_requiredby<br>*Datetime* | Læse/skrive<br>Valgfri | Den dato, hvor screeningen skal være fuldført. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus indstilling*|Læse/skrive<br>Obligatorisk | Angiver kandidatens status for screeningen. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Læse/skrive<br>Obligatorisk | Det partnummer (person), der er tilknyttet kandidaten. |
| **Screeningstype-id**<br>mshr_screeningtypeid<br>*Streng* | Læse/skrive<br>Påkrævet<br>Fremmed nøgle: ScreeningType | Id for den screeningtype, der er defineret i Human Resources. |
| **Værdi for screeningstype-id**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity | Systemgenereret entydig identifikation for screeningstypeposten i den tilknyttede enhed. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* |  Skrivebeskyttet<br>Obligatorisk | Felt, der bruges som id for enhedsposten. |
| **Værdi for person-id**<br>_mshr_fk_person_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_dirpersonentityid of mshr_dirpersonentity | Systemgenereret id til partpost (person). |
| **Enheds-id for personscreening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret| Entydigt primært id for personscreeningpost. |
| **Fuldførelsesdato**<br>mshr_completeddate<br>*Datetime* | Læse/skrive<br>Valgfri | Datoen, hvor screeningen blev fuldført. |


## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
