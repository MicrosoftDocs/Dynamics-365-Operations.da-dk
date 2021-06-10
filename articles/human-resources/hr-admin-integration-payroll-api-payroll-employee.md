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
ms.openlocfilehash: 87efbf7063de373e1e0b844ff1b942cdaab4a021
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055046"
---
# <a name="payroll-employee"></a>Medarbejders løn

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder detaljer og en eksempelforespørgsel til objektet Lønmedarbejder i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **Personalenummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Medarbejderens entydige personalenummer. |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Påkrævet<br>Systemgenereret |  |
| **Efternavn**<br>mshr_lastname<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Medarbejderens efternavn. |
| **Id for juridisk enhed**<br>mshr_legalentityID<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Angiver den juridiske enhed (regnskabet). |
| **Gyldig fra**<br>mshr_namevalidfrom<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Dato, hvorfra medarbejderoplysningerne er gyldige.  |
| **Køn**<br>mshr_gender<br>*Int32* | Skrivebeskyttet<br>Påkrævet | Medarbejderens køn. |
| **Lønmedarbejders enheds-id**<br>mshr_payrollemployeeentityid<br>*GUID* | Påkrævet<br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer medarbejderen. |
| **Startdato for ansættelse**<br>mshr_employmentstartdate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet | Startdatoen for medarbejderens ansættelse. |
| **Identifikationstype-id**<br>mshr_identificationtypeid<br>*Streng* |Skrivebeskyttet<br>Påkrævet | Den identifikationstype, der er defineret for medarbejderen. |
| **Slutdato for ansættelse**<br>mshr_employmentenddate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet<br>Påkrævet |Slutdatoen for medarbejderens ansættelse.  |
| **Dataområde-id**<br>mshr_dataareaid_id<br>*GUID* | Påkrævet <br>Systemgenereret | Systemgenereret GUID-værdi, der identificerer den juridiske enhed (virksomheden). |
| **Gyldig til**<br>mshr_namevalidto<br>*Dato- og klokkeslætsforskydning* |  Skrivebeskyttet<br>Påkrævet | Dato, hvortil medarbejderoplysningerne er gyldige. |
| **Fødselsdato**<br>mshr_birthdate<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Medarbejderens fødselsdato |
| **Identifikationsnummer til**<br>mshr_identificationnumber<br>*Streng* | Skrivebeskyttet <br>Påkrævet |Det identifikationsnummer, der er defineret for medarbejderen.  |
| **Fornavn**<br>mshr_firstname<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Medarbejderens fornavn. |
| **Mellemnavn**<br>mshr_middlename<br>*Streng* | Skrivebeskyttet<br>Påkrævet |Medarbejderens mellemnavn.  |

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
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
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
