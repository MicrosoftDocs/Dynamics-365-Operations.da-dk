---
title: Plan for variabel løn
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Plan for variabel løn i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2f057fb0f492efd08674b3bbeef9f3fec3d7be0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068453"
---
# <a name="payroll-variable-compensation-plan"></a>Plan for variabel løn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Plan for variabel løn for Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt angiver den plan for variabel løn, der er tildelt for en medarbejders givne stilling.

Fysisk navn: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Medarbejderens entydige personalenummer.  |
| **Bonusdato**</br>mshr_awarddate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Dato for bonussen. |
| **Bonustype**</br>mshr_awardtype</br>*[Grupperet indstilling for mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Skrivebeskyttet | Den type bonus, der er defineret til den valgte variable lønstruktur. |
| **Valuta**</br>mshr_unitcurrencycode</br>*Streng* | Skrivebeskyttet |Den valuta, der er defineret for Plan for variabel løn.   |
| **Id for plan for fast løn**</br>mshr_fixedplanid</br>*Streng* | Skrivebeskyttet | Den struktur for fast løn, der bruges som udgangspunkt for beregningen af bonussen. |
| **Enhedsværdi**</br>mshr_awardamount</br>*Decimal* | Skrivebeskyttet | Værdien for enheden |
| **Procestype**</br>mshr_processtype</br>*[Grupperet indstilling for mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Skrivebeskyttet | Procestypen. |
| **Type af variabel kompensationsplan**</br>Streng</br>*mshr_typeid* | Skrivebeskyttet | Typen af variabel lønstruktur. |
| **Id for variabel kompensationsplan**</br>Streng</br>*mshr_planid* | Skrivebeskyttet | Id'et for den variable lønstruktur. |
| **Antal enheder**</br>Decimal</br>*mshr_numberofunits* | Skrivebeskyttet | Angiv antallet af enheder for bonus. |
| **Primært felt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenereret. | |
| **Objektet Plan for variabel løn**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer lønplanen. |

## <a name="relations"></a>Relationer 

|Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
