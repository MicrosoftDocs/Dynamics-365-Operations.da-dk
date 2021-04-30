---
title: Plan for fast løn
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881953"
---
# <a name="payroll-fixed-compensation-plan"></a>Plan for fast løn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Medarbejder-id**<br>mshr_fk_employee_id_value<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Fremmednøgle: mshr_Employee_id for mshr_payrollemployeeentity enhed  | Medarbejder-id |
| **Lønsats**<br>mshr_payrate<br>*Decimal* | Skrivebeskyttet<br>Påkrævet | Lønsats, der er defineret i Plan for fast løn. |
| **Plan-id**<br>mshr_planid<br>*Streng* | Skrivebeskyttet<br>Påkrævet |Angiver lønplanen.  |
| **Gyldig fra**<br>mshr_validfrom<br>*Dato- og klokkeslætsforskydning* |  Skrivebeskyttet<br>Påkrævet |Dato, hvorfra medarbejderens faste løn er gyldig.  |
| **Enheden Plan for fast løn**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Påkrævet<br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer lønplanen. |
| **Lønfrekvens**<br>mshr_payfrequency<br>*Streng* | Skrivebeskyttet<br>Påkrævet |Hvor ofte medarbejderen bliver betalt.  |
| **Gyldig til**<br>mshr_validto<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Dato, hvortil medarbejderens faste løn er gyldig. |
| **Stillings-id**<br>mshr_positionid<br>*Streng* | Skrivebeskyttet <br>Påkrævet | Stillings-id, der er tilknyttet medarbejderen og tilmelding til Plan for fast løn. |
| **Valuta**<br>mshr_currency<br>*Streng* | Skrivebeskyttet <br>Påkrævet |Den valuta, der er defineret for Plan for fast løn   |
| **Personalenummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet |Medarbejderens entydige personalenummer.  |

**Forespørgsel**

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
