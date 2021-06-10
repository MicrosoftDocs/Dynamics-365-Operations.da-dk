---
title: Lønstillingsjob
description: Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Lønstillingsjob i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055022"
---
# <a name="payroll-position-job"></a>Lønstillingsjob

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder detaljer og en eksempelforespørgsel til relationsobjektet Lønstillingsjob i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Job ID**<br>mshr_jobid<br>*Streng* | Skrivebeskyttet<br>Påkrævet |Jobbets id. |
| **Gyldig fra**<br>mshr_validto<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Den dato, som stilling og jobrelationen er gyldig fra. |
| **Gyldig til**<br>mshr_validto<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Den dato, som stillingen og jobrelationen er gyldig til.  |
| **Stillings-id**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Stillingens id. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Påkrævet<br>Systemgenereret |  |
| **Stillingsjob-id-værdi**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_PayrollPositionJobEntity for mshr_payrollpositionjobentity |Id for det job, der er tilknyttet stillingen.|
| **Id-værdi til plan for fast løn**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_FixedCompPlan_id for mshr_payrollfixedcompensationplanentity  | Id for planen for fast løn, der er tilknyttet stillingen. |
| **Lønstillingsjobbets enheds-id**<br>mshr_payrollpositionjobentityid<br>*Guid* | Påkrævet<br>Systemgenereret. | Systemgenereret GUID-værdi, der entydigt identificerer jobbet.  |

