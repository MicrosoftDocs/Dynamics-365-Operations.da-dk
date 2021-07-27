---
title: Anmodning om orlov
description: Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Orlovsanmodning i Dynamics 365 Human Resources.
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
ms.openlocfilehash: b7f5744265dd106f11e6ffe7334873e697a7ea13
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314345"
---
# <a name="leave-request"></a>Anmodning om orlov

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Orlovsanmodning til Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt viser oplysninger for en orlovsanmodning.

Fysisk navn: mshr_essleaverequestentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Anmodnings-id**</br>mshr_requestid</br>*Streng* | Skrivebeskyttet | Anmodnings-id'et. |
| **Orlovstype-id**</br>mshr_leavetypeid</br>*Streng* | Skrivebeskyttet | Orlovstype-id. |
| **Dato**</br>mshr_leavedate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Datoen for orlovsanmodningen. |
| **Beløb**</br>mshr_amount</br>*Decimal* | Skrivebeskyttet | Beløbet for orlovsanmodningen. |
| **Halvdagstype**</br>mshr_halfdaydefinition</br>*Grupperet indstilling for mshr_LeaveHalfDayDefinition* | Skrivebeskyttet | Typen af halvdagsorlov. |
| **Kommentar**</br>mshr_comment</br>*Streng* | Skrivebeskyttet | Kommentar til anmodningen. |
| **Status**</br>mshr_status</br>*Grupperet indstilling for mshr_status* | Skrivebeskyttet | Status for anmodningen. |
| **Dato**</br>mshr_requestdate</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Datoen for anmodningen. |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet | Medarbejderens entydige personalenummer. |
| **Årsagskode-id**</br>mshr_reasoncodeid</br>*Streng* | Skrivebeskyttet | Årsagskode-id'et. |
| **Dataområde-id**</br>mshr_dataareaid</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Primært felt**</br>mshr_primaryfield</br>*GUID* | Skrivebeskyttet</br>Systemgenereret | |
| **Orlovstypeenhed**</br>mshr_essleaverequestentityid</br>*GUID* | Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer orlovsanmodningen. |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
