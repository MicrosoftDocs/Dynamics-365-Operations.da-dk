---
title: Lønoplysninger for stillinger
description: Denne artikel indeholder detaljer og en eksempelforespørgsel til stillingsenhedens lønoplysninger i Dynamics 365 Human Resources.
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
ms.openlocfilehash: ac36b0386312e1631528b8ab5976db2cb3924caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904124"
---
# <a name="payroll-position"></a>Lønstilling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver objektet Lønstilling i Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollpositionentity.

### <a name="description"></a>Betegnelse

Dette objekt viser stillingsrelaterede oplysninger for en given medarbejder.

Fysisk navn: mshr_payrollpositionentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Stillings-id**</br>mshr_positionid</br>*Streng* | Skrivebeskyttet | Stillingens id. |
| **Betalingscyklus-id**</br>mshr_paycycleid</br>*Streng* | Skrivebeskyttet | Den løncyklus, der er defineret på stillingen. |
| **Normaltimer på årsbasis**</br>annualregularhours</br>*Decimal* | Skrivebeskyttet | Årlige regelmæssige timer, der er defineret på stillingen. |
| **Betalt af juridisk enhed**</br>paidbylegalentity</br>*Streng* | Skrivebeskyttet | Den juridiske enhed, der er defineret på den stilling, der er ansvarlig for udstedelse af betaling. |
| **Gyldig til**</br>validto</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Den dato, hvor stillingsoplysningerne er gyldige til. |
| **Gyldig fra**</br>validfrom</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Den dato, hvor stillingsoplysningerne er gyldige fra. |
| **Primært felt**</br>mshr_primaryfield</br>*Streng* | Systemgenereret | Primært felt. |
| **Enheds-id til lønoplysninger for stillinger**</br>payrollpositiondetailsentityid</br>*Guid* | Påkrævet</br>Systemgenereret. | En systemgenereret GUID-værdi (Global Unique Identifier), der identificerer positionen entydigt. |

## <a name="relations"></a>Relationer

| Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Ikke tilgængelig |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Ikke tilgængelig |

## <a name="example-query"></a>Eksempelforespørgsel

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

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
