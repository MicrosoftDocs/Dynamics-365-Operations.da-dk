---
title: Status for jobfritagelse
description: Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053845"
---
# <a name="job-exempt-status"></a>Status for jobfritagelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: cdm_jobexemptstatus

Denne fasttekst beskriver den indstilling der er angivet for statusværdier for FLSA-jobfritagelse. Dette findes i den eksisterende cdm_jobexemptstatus indstilling.

| Værdi | Mærkat | Beskrivelse |
| --- | --- | --- |
| 200000000 | Frit | Jobbet har eksempel på status på baggrund af FLSA-retningslinjer. |
| 200000001 | Ikke-eksisterende | Jobbet har eksempel på ikke-eksisterende status på baggrund af FLSA-retningslinjer. |
| 200000002 | Gælder ikke | FLSA-statusretningslinjer gælder ikke for jobbet. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]