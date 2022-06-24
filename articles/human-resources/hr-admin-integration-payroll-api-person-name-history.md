---
title: Historik for personnavn
description: Denne artikel indeholder detaljer og en eksempelforespørgsel til objektet Historik for personnavn i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875765"
---
# <a name="person-name-history"></a>Historik for personnavn


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver personnavnehistorikken til Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Beskrivelse

Denne enhed indeholder oplysninger om navnehistorikken for en bestemt person.

> [!IMPORTANT] 
> Felterne **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** og **NameValidTo** er ikke længere tilgængelige på Lønmedarbejderenheden. De er fjernet for at sikre, at der kun findes én gyldighedsdato for datakilden, som understøtter denne enhed.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Fornavn**</br>mshr_firstname</br>*Streng* | Skrivebeskyttet | Fornavn. |
| **Præfiks for efternavn**</br>mshr_lastnameprefix</br>*Streng*) | Skrivebeskyttet | Præfiks for efternavn. |
| **Efternavn**</br>mshr_lastname</br>*Streng*) | Skrivebeskyttet | Efternavn. |
| **Mellemnavn**</br>mshr_middlename</br>*Streng*) | Skrivebeskyttet | Mellemnavn. |
| **Gyldig til**</br>mshr_validto</br>*Streng*) | Skrivebeskyttet | Den dato, som adressen gælder til. |
| **Partnummer**</br>mshr_partynumber</br>*Streng* | Skrivebeskyttet | Et brugerlæsbart og systemgenereret entydigt id for personen. |
| **Primært felt**</br>mshr_primaryfield</br>*Streng* | Skrivebeskyttet | Entydigt id for posten. |
| **Enheds-id for personnavnhistorik**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Systemgenereret | En systemgenereret GUID-værdi (Global Unique Identifier), der identificerer posten entydigt. |

## <a name="relations"></a>Relationer

| Værdi af egenskab | Relateret enhed | Navigationsegenskab | Samlingstype |
| --- | --- | --- | --- |
| Ikke tilgængelig | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Ikke tilgængelig | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Eksempelforespørgsel for lønmedarbejder

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Svar**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
