---
title: Status for rekrutteringsanmodning
description: Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464640"
---
# <a name="recruiting-request-status"></a>Status for rekrutteringsanmodning

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