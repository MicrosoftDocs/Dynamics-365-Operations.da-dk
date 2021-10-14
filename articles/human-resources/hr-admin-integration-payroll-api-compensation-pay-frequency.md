---
title: Kompensation - lønfrekvens
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Kompensation - lønfrekvens i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b864d0db8ff1b380749b6099fa74a40045932b67
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559635"
---
# <a name="compensation-pay-frequency"></a>Kompensation - lønfrekvens

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Kompensation - lønfrekvens i Dynamics 365 Human Resources.

Fysisk navn: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Beskrivelse

Denne enhed indeholder oplysninger om lønsatskonverteringen for en given kompensationslønfrekvens.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Årlig lønsatskonvertering**</br>mshr_annualconversionfactor</br>*Decimal* | Skrivebeskyttet | Den årlige omregningsfaktor for betalingsfrekvensen. |
| **Beskrivelse**</br>mshr_description</br>*Streng* | Skrivebeskyttet | Beskrivelsen af konverteringsfaktoren. |
| **Lønsatskonvertering pr. time**</br>mshr_hourlyconversionfactor</br>*Decimal* | Skrivebeskyttet | Omregningsfaktor pr. time for betalingsfrekvensen. |
| **Lønsatskonvertering pr. måned**</br>mshr_monthlyconversionfactor</br>*Decimal* | Skrivebeskyttet | Den månedlige omregningsfaktor for betalingsfrekvensen. |
| **Konvertering af lønsats**</br>mshr_payrateconversion</br>*Streng* | Skrivebeskyttet | En entydig streng, der identificerer omregningssatsen. |
| **Termin**</br>mshr_period</br>*periodeindstillingssæt* | Skrivebeskyttet | Hovedperioden for den angivne lønsatskonvertering. |
| **Lønsatskonvertering pr. uge**</br>mshr_weeklyconversionfactor</br>*Decimal* | Skrivebeskyttet | Omregningsfaktor pr. uge for betalingsfrekvensen. |
| **Dataområde-id**</br>mshr_dataareaid</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Objekt-id for Kompensation - lønfrekvens**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Systemgenereret | En systemgenereret GUID-værdi (Global Unique Identifier), der identificerer posten entydigt. |

## <a name="example-query-for-payroll-employee"></a>Eksempelforespørgsel for lønmedarbejder

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Svar**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
