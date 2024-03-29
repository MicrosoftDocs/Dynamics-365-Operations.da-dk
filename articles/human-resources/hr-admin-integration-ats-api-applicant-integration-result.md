---
title: Resultat af ansøgerintegration
description: Denne artikel beskriver den indstilling for integrationsresultat for ansøger, der er angivet for Dynamics 365 Human Resources.
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702222"
---
# <a name="applicant-integration-result"></a>Resultat af ansøgerintegration


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver den indstilling for integrationsresultat for ansøger, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmapplicantintegrationresult

Denne optælling angiver status for en kandidatpost.

| Værdi | Mærkat | Beskrivelse |
| --- | --- | --- |
| 200000000 | Ikke behandlet | Kandidaten er stadig under behandling. |
| 200000001 | Ansat | Kandidaten er ansat. |
| 200000002 | Ikke ansat | Der blev truffet beslutning om ikke at ansætte kandidaten. |
| 200000003 | Afvist | Kandidaten blev ikke udvalgt til overvejelse. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
