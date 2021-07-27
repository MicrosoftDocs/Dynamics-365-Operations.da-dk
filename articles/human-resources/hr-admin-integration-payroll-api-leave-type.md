---
title: Orlovstype
description: Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Orlovstype i Dynamics 365 Human Resources.
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
ms.openlocfilehash: a99d53805efd7ee2001217ea3154d46b5d5e66cd
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314349"
---
# <a name="leave-type"></a>Orlovstype

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Orlovstype til Dynamics 365 Human Resources.

### <a name="description"></a>Betegnelse

Dette objekt viser oplysninger for en given orlovstype.

Fysisk navn: mshr_essleavetypeentity.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Orlovstype-id**</br>mshr_leavetypeid</br>*Streng* | Skrivebeskyttet | Orlovstype-id. |
| **Beskrivelse**</br>mshr_description</br>*Streng* | Skrivebeskyttet | En beskrivelse af orlovstypen. |
| **Kategori**</br>mshr_category</br>*Grupperet indstilling for mshr_LeaveTypeCategory* | Skrivebeskyttet | Orlovstypekategori. |
| **Årsagskode skal angives**</br>mshr_isreasoncoderequired</br>*Grupperet indstilling for mshr_NoYes* | Skrivebeskyttet | Definerer, om der kræves en årsagskode for orlovstypen. |
| **Orlovsenhed**</br>mshr_leaveamountunit</br>*Grupperet indstilling for mshr_LeaveAmountUnit* | Skrivebeskyttet | Enheden for denne orlovstype. |
| **Aktivér halv dag**</br>mshr_enablehalfdaydefinition</br>*Grupperet indstilling for mshr_NoYes* | Definerer, om en halv dag er aktiveret for orlovstypen. |
| **Dataområde-id**</br>mshr_dataareaid_id</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Orlovstypeenhed**</br>mshr_essleavetypeentityid</br>*GUID* | Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer orlovstypen. |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Svar**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
