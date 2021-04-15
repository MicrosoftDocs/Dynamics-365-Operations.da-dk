---
title: Resultat af ansøgerintegration
description: Dette emne beskriver den indstilling for integrationsresultat for ansøger, der er angivet for Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467547"
---
# <a name="applicant-integration-result"></a>Resultat af ansøgerintegration

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver den indstilling for integrationsresultat for ansøger, der er angivet for Dynamics 365 Human Resources.

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