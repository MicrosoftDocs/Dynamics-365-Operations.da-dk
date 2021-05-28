---
title: Lønarbejderadresse
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Lønarbejderadresse i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020699"
---
# <a name="payroll-worker-address"></a>Lønarbejderadresse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Lønarbejderadresse i Dynamics 365 Human Resources.

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **By**<br>mshr_city<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Byen, der er defineret for adressen.   |
| **Personalenummer**<br>mshr_personnelnumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Medarbejderens entydige personalenummer.  |
| **Land og område**<br>mshr_countryregionid<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Det land og område, der er defineret til adressen  |
| **Gyldig fra**<br>mshr_postaladdressvalidfrom<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Den dato, som adressen gælder fra. |
| **Arbejdsadresse**<br>mshr_isworkedinaddressbr>*Int32* | Skrivebeskyttet<br>Påkrævet | Angiver, om adressen er der, hvor medarbejderen arbejder. |
| **Region**<br>mshr_county<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Regionen, der er defineret for adressen.  |
| **Lønarbejderadresse-id**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Påkrævet<br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer adressen.  |
| **Primært felt**<br>mshr_primaryfield<br>*Streng* | Skrivebeskyttet<br>Påkrævet |  |
| **Gade**<br>mshr_street<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Gaden, der er defineret for adressen. |
| **Gyldig til**<br>mshr_postaladdressvalidto<br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet <br>Påkrævet | Den dato, som adressen gælder til.  |
| **Lokations-id**<br>mshr_locationidbr>*Streng* | Skrivebeskyttet <br>Påkrævet | Adressens id.  |
| **Postnummer**<br>mshr_zipcode<br>*Streng* | Skrivebeskyttet <br>Påkrævet |Det identifikationsnummer, der er defineret for medarbejderen.  |
| **Bopælsadresse**<br>mshr_islivedinaddressbr>*Streng* | Skrivebeskyttet<br>Påkrævet | Angiver, om adressen er der, hvor medarbejderen bor. |
| **Stat**<br>mshr_state<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Delstaten, der er defineret for adressen.  |

## <a name="example-query"></a>Eksempelforespørgsel

**Anmodning**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
