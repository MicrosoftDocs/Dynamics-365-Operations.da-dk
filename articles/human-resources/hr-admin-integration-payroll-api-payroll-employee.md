---
title: Medarbejders løn
description: Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Lønmedarbejder i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 672db002ddf8d12aaab5b97241390c036ad7ab5c
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538848"
---
# <a name="payroll-employee"></a>Medarbejders løn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Medarbejders løn for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollemployeeentity.

### <a name="description"></a>Betegnelse

Dette objekt indeholder oplysninger om medarbejderen. Du skal angive [parametrene for lønintegration](hr-admin-integration-payroll-api-parameters.md), før du bruger dette objekt.

>[!IMPORTANT] 
>Felterne **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** er ikke længere tilgængelige på denne enhed. Dette sikrer, at der kun findes én ikrafttrædelsesdato for den datakilde, der understøtter denne enhed, som er **HcmEmployment** med felterne **EmploymentStartDate** og **EmploymentEndDate**.

>Disse felter vil være tilgængelige på **DirPersonNameHistoricalEntity**, som blev udgivet i Platform-opdatering 43. Der er en OData-relation fra **PayrollEmployeeEntity** til **DirPersonNameHistoricalEntity** i feltet **Person**. Enheden **DirPersonNameHistoricalEntity** kan også forespørges direkte via OData med det offentlige navn **PersonHistoricalNames**.


## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personalenummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Medarbejderens entydige personalenummer. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Påkrævet<br>Systemgenereret |  |
| **Id for juridisk enhed**<br>mshr_legalentityID<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Angiver den juridiske enhed (regnskabet). |
| **Køn**<br>mshr_gender<br>[mshr_hcmpersongender indstilling](hr-admin-integration-payroll-api-gender.md) | Skrivebeskyttet<br>Påkrævet | Medarbejderens køn. |
| **Lønmedarbejders enheds-id**<br>mshr_payrollemployeeentityid<br>*GUID* | Påkrævet<br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer medarbejderen. |
| **Startdato for ansættelse**<br>mshr_employmentstartdate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet | Startdatoen for medarbejderens ansættelse. |
| **Identifikationstype-id**<br>mshr_identificationtypeid<br>*Streng* |Skrivebeskyttet<br>Påkrævet | Den identifikationstype, der er defineret for medarbejderen. |
| **Slutdato for ansættelse**<br>mshr_employmentenddate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet |Slutdatoen for medarbejderens ansættelse.  |
| **Dataområde-id**<br>mshr_dataareaid_id<br>*GUID* | Påkrævet <br>Systemgenereret | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |
| **Gyldig til**<br>mshr_namevalidto<br>*Dato- og klokkeslætsforskydning* |  Skrivebeskyttet<br>Påkrævet | Dato, hvortil medarbejderoplysningerne er gyldige. |
| **Fødselsdato**<br>mshr_birthdate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Medarbejderens fødselsdato |
| **Identifikationsnummer til**<br>mshr_identificationnumber<br>*Streng* | Skrivebeskyttet <br>Påkrævet |Det identifikationsnummer, der er defineret for medarbejderen.  |

## <a name="example-query-for-payroll-employee"></a>Eksempelforespørgsel for lønmedarbejder

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
