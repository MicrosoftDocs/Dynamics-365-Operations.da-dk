---
title: Status for rekrutteringsanmodning
description: Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067095"
---
# <a name="recruiting-request-status"></a>Status for rekrutteringsanmodning


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequeststatus

Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.

| Værdi | Mærkat | Beskrivelse |
| --- | --- | --- |
| 200000000 | Udkast | Anmodningen er kladde og klar til aktiv rekruttering. |
| 200000001 | Til gennemsyn | Anmodningen er sendt og dirigeres til godkendelse via arbejdsflow. Kun tilgængelig, når arbejdsflow er aktiveret. |
| 200000002 | Udestående | Anmodningen afventer en arbejdsflowhandling. Kun tilgængelig, når arbejdsflow er aktiveret. |
| 200000003 | Annulleret | Anmodningen blev annulleret. Kun tilgængelig, når arbejdsflow er aktiveret. |
| 200000004 | Afvist | Anmodningen er ikke godkendt. Kun tilgængelig, når arbejdsflow er aktiveret. |
| 200000005 | Aktive | Alle arbejdsflow er fuldført og godkendt, og anmodningen er klar til aktiv rekruttering. |
| 200000006 | Lukkede | Rekrutteringsanmodningen er lukket. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
