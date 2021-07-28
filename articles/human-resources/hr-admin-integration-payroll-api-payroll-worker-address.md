---
title: Lønarbejderadresse
description: Dette emne indeholder detaljer og en eksempelforespørgsel til enheden Lønarbejderadresse i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ff65a0518232275f7c5d0b4a70d04f77e4936c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314107"
---
# <a name="payroll-worker-address"></a>Lønarbejderadresse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver objektet Lønarbejderadresse for Dynamics 365 Human Resources.

Fysisk navn: mshr_payrollworkeraddressentity.

### <a name="description"></a>Betegnelse

Denne enhed angiver bopælsplaceringen for løn og arbejdsplaceringen for løn for en bestemt medarbejder.

## <a name="properties"></a>Egenskaber

| Egenskab</br>**Fysisk navn**</br>**_Type_** | Anvendelse | Betegnelse |
| --- | --- | --- |
| **By**</br>mshr_city</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Byen, der er defineret for adressen.   |
| **Personalenummer**</br>mshr_personnelnumber</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Medarbejderens entydige personalenummer.  |
| **Land og område**</br>mshr_countryregionid</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Det land og område, der er defineret til adressen.  |
| **Gyldig fra**</br>mshr_postaladdressvalidfrom</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet </br>Påkrævet | Den dato, som adressen gælder fra. |
| **Arbejdsadresse** </br> mshr_isworkedinaddressbr </br>*[Grupperet indstilling for mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet</br>Påkrævet | Angiver, om adressen er der, hvor medarbejderen arbejder. |
| **Region**</br>mshr_county</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Regionen, der er defineret for adressen.  |
| **Lønarbejderadresse-id**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Påkrævet</br>Systemgenereret | Systemgenereret GUID-værdi, der entydigt identificerer adressen.  |
| **Primært felt**</br>mshr_primaryfield</br>*Streng* | Skrivebeskyttet</br>Påkrævet |  |
| **Gade**</br>mshr_street</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Gaden, der er defineret for adressen. |
| **Gyldig til**</br>mshr_postaladdressvalidto</br>*Dato- og klokkeslætsforskydning* | Skrivebeskyttet </br>Påkrævet | Den dato, som adressen gælder til.  |
| **Lokations-id**</br>mshr_locationidbr>*Streng* | Skrivebeskyttet <br>Påkrævet | Adressens id.  |
| **Postnummer**</br>mshr_zipcode<br>*Streng* | Skrivebeskyttet <br>Påkrævet |Det identifikationsnummer, der er defineret for medarbejderen.  |
| **Bopælsadresse**</br>mshr_islivedinaddressbr </br> *[Grupperet indstilling for mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Skrivebeskyttet</br>Påkrævet | Angiver, om adressen er der, hvor medarbejderen bor. |
| **Stat**</br>mshr_state</br>*Streng* | Skrivebeskyttet</br>Påkrævet | Delstaten, der er defineret for adressen.  |

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

## <a name="see-also"></a>Se også

[Introduktion til lønintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
