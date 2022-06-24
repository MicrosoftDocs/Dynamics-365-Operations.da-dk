---
title: Certifikattype
description: Denne artikel beskriver certifikattypeenheden til Dynamics 365 Human Resources.
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
ms.openlocfilehash: bfe7f06176098a504f8d2ad1c1431a6f60fe059c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886183"
---
# <a name="certificate-type"></a>Certifikattype


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver certifikattypeenheden til Dynamics 365 Human Resources.

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
