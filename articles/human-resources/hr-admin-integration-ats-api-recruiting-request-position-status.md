---
title: Status for rekrutteringsanmodningsstilling
description: Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6a63a95201583fa7b215e221a03715e56b55c11a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064885"
---
# <a name="recruiting-request-position-status"></a>Status for rekrutteringsanmodningsstilling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver status for stillingen i en rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequestpositionstatus

Denne fasttekst indeholder den indstilling, der er angivet for statusværdierne for hver enkelt stilling, en rekrutteringsanmodning i enheden RecruitingRequestPosition.

| Værdi | Mærkat | Beskrivelse |
| --- | --- | --- |
| 200000000 | Åbnet | Stillingen i rekrutteringsanmodningen er åben for rekruttering. Det betyder ikke, at der ikke aktuelt er nogen aktiv stillingstildeling for stillingen. Der kan være en medarbejder i stillingen på tidspunktet for rekruttering. Det angiver kun, at stillingen er tilgængelig for rekruttering i forbindelse med rekrutteringsanmodningen. |
| 200000001 | Besat | Der er valgt en arbejder til tildeling til stillingen. |
| 200000002 | Annulleret | Anmodningen om at rekruttere til denne stilling er annulleret. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
