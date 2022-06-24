---
title: Screeningfrekvensen genereres fra
description: Denne artikel beskriver den screeningfrekvens, der genereres fra indstilling til Dynamics 365 Human Resources.
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
ms.openlocfilehash: 846a35a2e8ca39ed9479601d99c8c515328d8ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879302"
---
# <a name="screening-frequency-generate-from"></a>Screeningfrekvensen genereres fra


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver den screeningfrekvens, der genereres fra indstilling til Dynamics 365 Human Resources.

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
