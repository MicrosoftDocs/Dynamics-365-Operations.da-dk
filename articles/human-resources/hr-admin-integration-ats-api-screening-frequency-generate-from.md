---
title: Screeningfrekvensen genereres fra
description: I dette emne beskrives den screeningfrekvens, der genereres fra indstilling til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 238cd5da750d815c904090cc9002e3d1a5d2bcc7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464568"
---
# <a name="screening-frequency-generate-from"></a>Screeningfrekvensen genereres fra

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives den screeningfrekvens, der genereres fra indstilling til Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmfrequencygeneratefrom

Denne fasttekst udgør den indstilling, der er angivet for værdier, der bruges til at bestemme startdatoen for beregningen til den næste påkrævede screening.

| Værdi | Mærkat | Beskrivelse |
| --- | --- | --- |
| 200000000 ikke valgt | Der er ikke valgt en værdi. |
| 200000001 Dato fuldført | Beregningen udføres fra den sidste screeningdato, der er fuldført. |
| 200000002 Dato påkrævet | Beregningen udføres fra den sidste screeningdato, der er påkrævet. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]