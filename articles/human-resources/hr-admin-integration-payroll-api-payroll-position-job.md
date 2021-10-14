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
ms.openlocfilehash: c0b70411e6535b22d698545438dcb0b16935e731
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559577"
---
# <a name="payroll-position-job"></a>Lønstillingsjob

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Lønstillingsjob for Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt angiver relationen mellem stilling og et job for en given plan med fast løn.

Fysisk navn: mshr_payrollpositionjobentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Stillings-id**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | Stillingens id. |
| **Gyldig fra**</br>mshr_validto</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Den dato, som stilling og jobrelationen er gyldig fra. |
| **Gyldig til**</br>mshr_validto</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Den dato, som stillingen og jobrelationen er gyldig til. |
| **Job ID**</br>mshr_jobid</br>*Streng* | Skrivebeskyttet | Jobbets id. |
| **Primært felt**</br>mshr_primaryfield</br>*Streng* | Systemgenereret | Primært felt. |
| **Lønstillingsjobbets enheds-id**</br>mshr_payrollpositionjobentityid</br>*Guid* | Systemgenereret. | En systemgenereret GUID-værdi (Global Unique Identifier), der identificerer jobbet entydigt. |

## <a name="relations"></a>Relationer

| Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Ikke tilgængelig |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Svar**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
