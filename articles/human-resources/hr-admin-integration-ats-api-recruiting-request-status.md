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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125948"
---
# <a name="recruiting-request-status"></a>Status for rekrutteringsanmodning

Dette emne beskriver den status for rekrutteringsanmodning, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmrecruitingrequeststatus

Denne fasttekst indeholder den indstilling, der er angivet for statusværdier for en rekrutteringsanmodning.

| Værdi | Mærkat | Betegnelse |
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