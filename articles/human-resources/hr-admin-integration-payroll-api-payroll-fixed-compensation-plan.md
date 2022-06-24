---
title: Plan for fast løn
description: Denne artikel indeholder detaljer og en eksempelforespørgsel til enheden Plan for fast løn i Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909840"
---
# <a name="payroll-fixed-compensation-plan"></a>Plan for fast løn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver objektet Plan for fast løn for Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt angiver den plan for fast løn, der er tildelt for en medarbejders givne stilling.

Fysisk navn: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Plan-id**</br>mshr_planid</br>*Streng* | Skrivebeskyttet | Angiver lønplanen.  |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Medarbejderens entydige personalenummer. |
| **Lønsats**</br>mshr_payrate</br>*Decimal* | Skrivebeskyttet | Lønsats, der er defineret i Plan for fast løn. |
| **Stillings-id**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | Stillings-id, der er tilknyttet medarbejderen og tilmelding til Plan for fast løn. |
| **Gyldig fra**</br>mshr_validfrom</br>*Dato- og klokkeslætsforskydning* |  Skrivebeskyttet | Dato, hvorfra medarbejderens faste løn er gyldig.  |
| **Gyldig til**</br>mshr_validto</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Dato, hvortil medarbejderens faste løn er gyldig. |
| **Lønfrekvens**</br>mshr_payfrequency</br>*Streng* | Skrivebeskyttet | Id'et for [kompensationslønfrekvensen](hr-admin-integration-payroll-api-compensation-pay-frequency.md) for den givne lønsats. |
| **Valuta**</br>mshr_currency</br>*Streng* | Skrivebeskyttet | Den valuta, der er defineret for Plan for fast løn. |
| **Enheden Plan for fast løn**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer lønplanen. |

## <a name="relations"></a>Relationer

|Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Eksempelforespørgsel

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

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
