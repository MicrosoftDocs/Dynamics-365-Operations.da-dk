---
title: Certifikattype
description: Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054686"
---
# <a name="certificate-type"></a>Certifikattype

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver certifikatstypeenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmcertificatetypeentity

## <a name="description"></a>Beskrivelse

Denne enhed definerer listen over typer af professionelle certifikater, der er defineret i Human Resources. Enheden er ikke specifik for en juridisk enhed (firma).

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Enheds-id for certifikattype**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet 
Systemgenereret | Entydig primær identifikation af certifikattype. |
| **Certifikattype**<br>mshr_certificatetype<br>*Streng* | Læse/skrive<br>Påkrævet | Entydig brugerlæsbar identifikation af certifikattype. |
| **Beskrivelse**<br>mshr_description<br>*Streng* | Læse/skrive<br>Påkrævet | Beskrivelse af certifikattype. |
| **Fornyelse påkrævet**<br>mshr_requirerenewal<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Angiver, om certifikatet skal fornys. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]