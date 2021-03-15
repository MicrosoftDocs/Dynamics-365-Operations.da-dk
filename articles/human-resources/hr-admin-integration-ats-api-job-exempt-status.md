---
title: Status for jobfritagelse
description: Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125563"
---
# <a name="job-exempt-status"></a>Status for jobfritagelse

Dette emne beskriver den indstilling for status for jobfritagelse, der er angivet for Dynamics 365 Human Resources.

Fysisk navn: cdm_jobexemptstatus

Denne fasttekst beskriver den indstilling der er angivet for statusværdier for FLSA-jobfritagelse. Dette findes i den eksisterende cdm_jobexemptstatus indstilling.

| Værdi | Mærkat | Betegnelse |
| --- | --- | --- |
| 200000000 | Frit | Jobbet har eksempel på status på baggrund af FLSA-retningslinjer. |
| 200000001 | Ikke-eksisterende | Jobbet har eksempel på ikke-eksisterende status på baggrund af FLSA-retningslinjer. |
| 200000002 | Gælder ikke | FLSA-statusretningslinjer gælder ikke for jobbet. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til anmodning om rekruttering](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]