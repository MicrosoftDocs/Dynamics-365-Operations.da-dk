---
title: Frynsegodeplan for lønmedarbejder
description: Denne artikel indeholder detaljer og en eksempelforespørgsel til enheden Frynsegodeplan for lønmedarbejder i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef45855d9e60131ac065ae6e2769b71ae3f69537
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902279"
---
# <a name="payroll-worker-benefit-plan"></a>Frynsegodeplan for lønmedarbejder


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver enheden Frynsegodeplan for lønmedarbejder til Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Betegnelse

Denne enhed indeholder oplysninger om frynsegodeplanen for en bestemt arbejder.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Medarbejderens entydige personalenummer. |
| **Id for juridisk enhed**</br>mshr_legalentityID</br>*Streng* | Skrivebeskyttet | Angiver den juridiske enhed (regnskabet). |
| **Periode-id**</br>mshr_periodid</br>*Streng* | Skrivebeskyttet | Identifikatoren af perioden. |
| **Plan-id**</br>mshr_planid</br>*Streng* | Skrivebeskyttet | Identifikatoren af planen. |
| **Dækningsindstilling**</br>mshr_coverageoptionid</br>*Streng* | Skrivebeskyttet | Identifikation af dækningsindstillingen. |
| **Startdato for fradrag**</br>mshr_deductionstartdatetime</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Startdato for fradrag. |
| **Slutdato for fradrag**</br>mshr_deductionenddatetime</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Slutdato for fradrag. |
| **Status**</br>mshr_status</br>*[Grupperet indstilling af Frynsegodestatus for medarbejderplan](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Skrivebeskyttet | Status for frynsegodeplanen. |
| **Gyldig fra**</br>mshr_validfrom</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet | Det tidspunkt, hvorfra denne post er gyldig |
| **Gyldig til**</br>mshr_validto</br>*Dato- og klokkeslætsforskydning* |  Skrivebeskyttet | Det tidspunkt, hvortil denne post er gyldig |
| **Plantype-id**</br>mshr_plantypeid</br>*Streng* | Skrivebeskyttet | Identifikatoren af plantypen. |
| **Kode for plantype**</br>mshr_plantypecode</br>*[Grupperet indstilling for dækning af frynsegodeplantype](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Skrivebeskyttet | Specifikationen af plantypen. |
| **Antal lønperioder**</br>mshr_payperiod</br>*Heltal* | Skrivebeskyttet | Antallet af betalingsperioder, der angiver, hvor ofte frynsegodeudbyderen eller medarbejderne skal betales. Dette beløb bruges til at beregne medarbejderens årlige beløb for frynsegodeløn. |
| **Medarbejderbeløb**</br>mshr_amountemployee</br>*Decimal* | Skrivebeskyttet | Procentdel eller beløb for medarbejder. |
| **Arbejdsgiverbeløb**</br>mshr_amountemployer</br>*Decimal* | Skrivebeskyttet | Procentdel eller beløb for arbejdsgiver. |
| **Primært felt**</br>mshr_primaryfield</br>*Streng* | Systemgenereret | Primært felt. |
| **Værdi for arbejder-id** </br>_mshr_fk_worker_id_value</br>*GUID* | Fremmed nøgle: mshr_hcmworkerbaseentityid af mshr_hcmworkerbaseentity-enhed. | Systemgenereret entydigt id til arbejderen. |
| **Værdi af periode-id**</br> _mshr_fk_period_id_value</br>*GUID* | Fremmed nøgle: mshr_benefitperiodentityid af mshr_benefitperiodentity-enhed. | Systemgenereret entydigt id til perioden. |
| **Plan-id-værdi**</br> _mshr_fk_plan_id_value</br>*GUID* | Fremmed nøgle: mshr_benefitplanentityid af mshr_benefitplanentity-enhed. | Systemgenereret entydigt id til planen. |
| **Plantype-id-værdi**</br> _mshr_fk_plantype_id_value</br>*GUID* | Fremmed nøgle: mshr_benefitplantypeentityid af mshr_benefitplantypeentity-enhed. | Systemgenereret entydigt id til planen. |
| **Værdi for dækningsindstillings-id**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Fremmed nøgle: mshr_benefitcoverageoptionentityid af mshr_benefitcoverageoptionentity-enhed. | Systemgenereret entydigt id til planen. |
| **Værdi for lønarbejders enheds-id for frynsegodeplan**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Skrivebeskyttet </br> Systemgenereret | Systemgenereret entydigt id til posten. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Eksempelforespørgsel til lønarbejderens frynsegodeplan

**Anmodning**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Svar**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
