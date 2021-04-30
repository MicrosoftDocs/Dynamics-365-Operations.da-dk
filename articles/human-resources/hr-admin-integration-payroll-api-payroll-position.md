---
title: Lønoplysninger for stillinger
description: Dette emne indeholder detaljer og en eksempelforespørgsel til stillingsenhedens lønoplysninger i Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881948"
---
# <a name="payroll-position"></a>Lønstilling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder detaljer og en eksempelforespørgsel til stillingsenhedens lønoplysninger i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Normaltimer på årsbasis**<br>annualregularhours<br>*Decimal* | Skrivebeskyttet<br>Påkrævet | Årlige regelmæssige timer, der er defineret på stillingen.  |
| **Enheds-id til lønoplysninger for stillinger**<br>payrollpositiondetailsentityid<br>*Guid* | Påkrævet<br>Systemgenereret. | Systemgenereret GUID-værdi, der entydigt identificerer stillingen.  |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Påkrævet<br>Systemgenereret |  |
| **Stillingsjob-id-værdi**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_PayrollPositionJobEntity for mshr_payrollpositionjobentity |Id for det job, der er tilknyttet stillingen.|
| **Id-værdi til plan for fast løn**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmed nøgle: mshr_FixedCompPlan_id for mshr_payrollfixedcompensationplanentity  | Id for planen for fast løn, der er tilknyttet stillingen. |
| **Betalingscyklus-id**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Den løncyklus, der er defineret på stillingen. |
| **Betalt af juridisk enhed**<br>paidbylegalentity<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Den juridiske enhed, der er defineret på den stilling, der er ansvarlig for udstedelse af betaling. |
| **Stillings-id**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Stillingens id. |
| **Gyldig til**<br>validto<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet |Den dato, hvor stillingsoplysningerne er gyldige fra.  |
| **Gyldig fra**<br>validfrom<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet |Den dato, hvor stillingsoplysningerne er gyldige til.  |

**Forespørgsel**

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Svar**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
