---
title: Screeningstyper
description: Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126164"
---
# <a name="screening-types"></a>Screeningstyper

Dette emne beskriver enheden Screeningtyper til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmscreeningtypeentity

## <a name="description"></a>Betegnelse

Denne enhed beskriver de screeningtyper, firmaet har konfigureret for præ-ansættelse og igangværende medarbejder-screeningprocesser.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Enheds-id for screeningstype**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Entydigt primært id for screeningtypepost. |
| **Screeningstype-id**<br>mshr_screeningtypeid<br>*Streng* | Læse/skrive<br>Påkrævet | Brugerdefineret entydig id for screeningtype. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskrivelsen af screeningtypen. |
| **Frekvensenhed**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit-indstilling* | Læse/skrive<br>Påkrævet | Beskriver, hvor ofte screeningen skal fuldføres for den tildelte person. |
| **Generér fra**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom-indstilling* | Læse/skrive<br>Påkrævet | Hvis værdien for Frekvens er en anden værdi end "Kun én gang", bestemmer Værdien GenerateFrom den dato, den næste screeninghændelse skal beregnes fra. |
| **Frekvensinterval**<br>mshr_frequencyinterval<br>*Heltal* | Læse/skrive<br>Påkrævet | Hvis frekvensværdien har en anden værdi end "Kun én gang", skal du definere et interval for tidsenhederne mellem hver enkelt screeninghændelse. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]