---
title: Orlovssaldo
description: Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Orlovssaldo i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a16da91a7e0d63a0951804861a51bf3835829f6c
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314353"
---
# <a name="leave-balance"></a>Orlovssaldo

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Orlovssaldo til Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt angiver orlovssaldoen pr. orlovstype for en given medarbejder.

Fysisk navn: mshr_essleavebalanceentities.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Medarbejderens entydige personalenummer. |
| **Aktuel saldo**</br>mshr_balanceavailable</br>*Decimal* | Skrivebeskyttet | Medarbejderens aktuelle saldo. |
| **Type**</br>mshr_balanceavailable</br>*Streng* | Skrivebeskyttet | Orlovstype-id. |
| **Periodiseringssats**</br>mshr_accrualratedescription</br> | Skrivebeskyttet | Periodiseringssatsen. |
| **Sidst overførte beløb**</br>mshr_lastcarryforwardamount</br>*Decimal* | Skrivebeskyttet | Beløbet for sidste overførsel. |
| **Taget dette år**</br>mshr_takenthisyear</br>*Decimal* | Skrivebeskyttet | Beløbet for orlov, der er taget i år. |
| **Total dette år**</br>mshr_totalthisyear</br>*Decimal* | Skrivebeskyttet | Totalbeløbet for dette år. |
| **Dataområde-id**</br>mshr_dataareaid_id</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Primært felt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenereret | |
| **Orlovstype-id**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Skrivebeskyttet</br>Fremmed nøgle:mshr_essleavetypeentityid of mshr_essleavetypeentity entity  | Orlovstype-id |
| **Objektet Orlovssaldo**</br>mshr_essleavebalanceentityid</br>*GUID* | Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer saldoen. |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
