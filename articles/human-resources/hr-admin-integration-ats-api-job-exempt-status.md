---
title: Status for jobfritagelse
description: Denne artikel beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894666"
---
# <a name="job-exempt-status"></a>Status for jobfritagelse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.

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
