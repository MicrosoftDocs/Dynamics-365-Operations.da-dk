---
title: Person
description: Dette emne beskriver personenheden til Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a13222317ba59868686be5ce24c970d6a068f8bc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464172"
---
# <a name="person"></a>Person

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne beskriver personenheden til Dynamics 365 Human Resources.

Fysisk navn: mshr_dirpersonentity

### <a name="description"></a>Beskrivelse

Denne enhed angiver de personlige oplysninger for den person, der er kandidat.

## <a name="json-representation"></a>JSON-repræsentation

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Egenskaber

| Egenskab<br>**Fysisk navn**<br>**_Type_** | Anvendelse | Beskrivelse |
| --- | --- | --- |
| **Personenheds-id**<br>mshr_dirpersonentityid<br>*GUID* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Et systemgenereret entydigt id til enhedsposten. |
| **Partnummer**<br>mshr_partynumber<br>*Streng* | Skrivebeskyttet<br>Påkrævet<br>Systemgenereret | Et brugerlæsbart og systemgenereret entydigt id for personen.  |
| **Navn**<br>mshr_name<br>*Streng* | Skrivebeskyttet<br>Påkrævet | Feltværdien er en sammenkædning af fornavn, mellemnavn, efternavnpræfiks og efternavn i den rækkefølge, de er defineret i feltet **Visning af navnerækkefølge som**. |
| **Navnealias**<br>mshr_namealias<br>*Streng* | Læse/skrive<br>Valgfri | Der findes muligvis et navnealias for personen. |
| **Kendt som**<br>mshr_knownas<br>*Streng* | Læse/skrive<br>Valgfri | Et navn, der kan bruges til personen, hvis personen typisk kaldes et andet navn. |
| **Sprog-id**<br>mshr_languageid<br>*Streng* | Læse/skrive<br>Valgfri | Sprog-id for personens primære sprog, som defineret i ISO 639-1-format. |
| **Adressekartoteker**<br>mshr_addressbooks<br>*Streng* | Læse/skrive<br>Valgfri | Det adressekartotek, som personen kan tilknyttes. Adressekartoteker, der er oprettet for organisationen, vises i den mshr_diraddressbooksentity-enhed. |
| **Jubilæumsdag**<br>mshr_anniversaryday<br>*Int* | Læse/skrive<br>Valgfri | Dag for personens jubilæumsdato. |
| **Jubilæumsmåned**<br>mshr_anniversarymonth<br>*mshr_monthsofyear indstilling* | Læse/skrive<br>Valgfri | Måned for personens jubilæumsdato. |
| **Jubilæumsår**<br>mshr_anniversaryyear<br>*Int* | Læse/skrive<br>Valgfri | År for personens jubilæumsdato. |
| **Fødselsdato**<br>mshr_birthday<br>*Int* | Læse/skrive<br>Valgfri | Dag for personens fødselsdato. |
| **Fødselsmåned**<br>mshr_birthmonth<br>*mshr_monthsofyear indstilling* | Læse/skrive<br>Valgfri | Måned for personens fødselsdato. |
| **Fødselsår**<br>mshr_birthyear<br>*Int* | Læse/skrive<br>Valgfri | År for personens fødselsdato. |
| **Navne på børn**<br>mshr_childrennames<br>*Streng* | Læse/skrive<br>Valgfri | Streng til navnene på personens børn. Der er ingen påkrævet afgrænsning. |
| **Køn**<br>mshr_gender<br>*mshr_hcmpersongender indstilling* | Læse/skrive<br>Valgfri | Personens køn. |
| **Hobbyer**<br>mshr_hobbies<br>*Streng* | Læse/skrive<br>Valgfri | Personens hobbyer. |
| **Initialer**<br>mshr_initials<br>*Streng* | Læse/skrive<br>Valgfri | Initialer for personens navn. |
| **Ægteskabelig status**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus indstilling* | Læse/skrive<br>Valgfri | Persons ægteskabelige status. |
| **Fonetisk fornavn**<br>mshr_phoneticfirstname<br>*Streng* | Læse/skrive<br>Valgfri | Den fonetiske udtale personens fornavn. |
| **Fonetisk efternavn**<br>mshr_phoneticlastname<br>*Streng* | Læse/skrive<br>Valgfri | Den fonetiske udtale personens efternavn. |
| **Fonetisk mellemnavn**<br>mshr_phoneticmiddlename<br>*Streng* | Læse/skrive<br>Valgfri | Den fonetiske udtale personens efternavn. |
| **Personligt suffiks**<br>mshr_personalsuffix<br>*Streng* | Læse/skrive<br>Valgfri | Persons personlige suffiks. Gyldige værdier i enheden mshr_dirnameaffixentity, hvor mshr_type er Suffiks (200000001). |
| **Titulering**<br>mshr_personaltitle<br>*Streng* | Læse/skrive<br>Valgfri | En personlig titel for personen. Gyldige værdier i enheden mshr_dirnameaffixentity, hvor mshr_type er titel (200000000).
| **Erhvervsmæssigt suffiks**<br>mshr_professionalsuffix<br>*Streng* | Læse/skrive<br>Valgfri | Et erhvervsmæssigt suffiks. |
| **Erhvervsmæssig titel**<br>mshr_professionaltitle<br>*Streng* | Læse/skrive<br>Valgfri | En erhvervsmæssig titel. |
| **Fuld primær adresse**<br>mshr_fullprimaryaddress<br>*Streng* | Læse/skrive<br>Valgfri | Persons fulde primære adresse, en sammensætning af de primære adressefelter. |
| **By for adresse**<br>mshr_addresscity<br>*Streng* | Læse/skrive<br>Valgfri | Byen i persons primære adresse. Konfigurer i enheden mshr_logisticsaddresscityentity. |
| **Adresse Land Område**<br>mshr_addresscountryregionid<br>*Streng* | Læse/skrive<br>Valgfri | By/område i persons primære adresse. Gyldige værdier i enheden mshr_logisticsaddresscountryregionentity. |
| **Adresse Land Område ISO-kode**<br>mshr_addresscountryregionisocode<br>*Streng* | Læse/skrive<br>Valgfri | ISO-koden for landet til persons primære adresse. |
| **Adresse-område**<br>mshr_addresscounty<br>*Streng* | Læse/skrive<br>Valgfri | Området til persons primære adresse. Konfigurer i enheden mshr_logisticsaddresscountyentity. |
| **Adressedistrikt-navn**<br>mshr_addressdistrictname<br>*Streng* | Læse/skrive<br>Valgfri | Distriktet til persons primære adresse. Konfigurer i mshr_logisticsaddressdistrictentity-enhed. |
| **Adresse-breddegrad**<br>mshr_addresslatitude<br>*Streng* | Læse/skrive<br>Valgfri | Breddegraden til persons primære adresse. |
| **Adresselokation-id**<br>mshr_addresslocationid<br>*Streng* | Læse/skrive<br>Valgfri | Det entydige id for lokationen af personens primære adresse. Gyldige værdier i enheden mshr_logisticspostaladdresslocationcdsentity. |
| **Adresselokations-roller**<br>mshr_addresslocationroles<br>*Streng* | Læse/skrive<br>Valgfri | Lokationsrolle i persons primære adresse. Konfigurer i enheden mshr_logisticslocationrolecdsentity. |
| **Adresse-længdegrad**<br>mshr_addresslongitude<br>*Streng* |  Læse/skrive<br>Valgfri | Længdegraden til persons primære adresse. |
| **Adresse-stat**<br>mshr_addressstate<br>*Streng* | Læse/skrive<br>Valgfri | Staten til persons primære adresse. Konfigurer i enheden mshr_logisticsaddressstateentity. |
| **Adresse-gade**<br>mshr_addressstreet<br>*Streng* | Læse/skrive<br>Valgfri | Gade-adressen til persons primære adresse. |
| **Adresse gyldig fra**<br>mshr_addressvalidfrom<br>*Dato* | Læse/skrive<br>Valgfri | Den dato, som personens primære adresse er gyldig fra. |
| **Adresse gyldig til**<br>mshr_addressvalidto<br>*Dato* | Læse/skrive<br>Valgfri | Den dato, hvor personens primære adresse er gyldig til. |
| **Adresse-postnummer**<br>mshr_addresszipcode<br>*Streng* | Læse/skrive<br>Valgfri | Postnr. til persons primære adresse. Konfigurer i enheden mshr_logisticsaddresspostalcodeentity. |
| **Adresse er privat**<br>mshr_addressisprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Bestemmer, om personens primære adresse deles med andre i organisationen. |
| **Beskrivelse af adresse**<br>mshr_addressdescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til persons primære adresse. |
| **Primær kontakt e-mail**<br>mshr_primarycontactemail<br>*Streng* | Læse/skrive<br>Valgfri | Personens primære e-mailadresse. |
| **Primær kontakt e-mailbeskrivelse**<br>mshr_primarycontactemaildescription<br>*Streng* | Læse/skrive<br>Valgfri | En beskrivelse til den primære e-mail-adresse. |
| **Primær kontakt e-mail er IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Bestemmer, om den primære e-mailadresse er tilgængelig for onlinemeddelelser. |
| **Primær kontakt e-mailformål**<br>mshr_primarycontactemailpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formål med den primære e-mailadresse. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontaktfax**<br>mshr_primarycontactfax<br>*Streng* | Læse/skrive<br>Valgfri | Primært faxnummer. |
| **Primær kontakt faxbeskrivelse**<br>mshr_primarycontactfaxdescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til det primære faxnummer. |
| **Primær kontakt fax lokalnr.**<br>mshr_primarycontactfaxextension<br>*Streng* | Læse/skrive<br>Valgfri | Lokalnummeret på det primære faxnummer. |
| **Primær kontakt faxformål**<br>mshr_primarycontactfaxpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for det primære faxnummer. Konfigurer i enheden mshr_logisticslocationroleentity.
| **Primær kontakttelefon**<br>mshr_primarycontactphone<br>*Streng* | Læse/skrive<br>Valgfri | Primært telefonnummer. |
| **Primær kontakt telefonbeskrivelse**<br>mshr_primarycontactphonedescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til det primære telefonnummer. |
| **Primær kontakt telefon lokalnr.**<br>mshr_primarycontactphoneextension<br>*Streng* | Læse/skrive<br>Valgfri | Lokalnummeret på det primære telefonnummer. |
| **Primær kontakt telefon er mobil**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Angiver, om det primære telefonnr. er et mobilnummer. |
| **Primær kontakt telefonformål**<br>mshr_primarycontactphonepurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for det primære telefonnummer. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontakttelex**<br>mshr_primarycontacttelex<br>*Streng* | Læse/skrive<br>Valgfri | Primært telexnummer. |
| **Primær kontakt telexbeskrivelse**<br>mshr_primarycontacttelexdescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse for persons primære telexnummer. |
| **Primær kontakt telexformål**<br>mshr_primarycontacttelexpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet med personens primære telexnummer. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontakt-URL**<br>mshr_primarycontacturl<br>*Streng* | Læse/skrive<br>Valgfri | Den primære URL-adresse. |
| **Primær kontakt URL-beskrivelse**<br>mshr_primarycontacturldescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til persons primære URL-adresse. |
| **Primær kontakt URL-formål**<br>mshr_primarycontacturldescription<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for persons primære URL-adresse. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontakt Facebook**<br>mshr_primarycontactfacebook<br>*Streng* | Læse/skrive<br>Valgfri | Primær Facebook-konto. Identificeret af bruger-id. |
| **Primær kontakt Facebook-beskrivelse**<br>mshr_primarycontactfacebookdescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til persons primære Facebook-konto. |
| **Primær kontakt Facebook er privat**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Bestemmer, om den primære Facebook-konto er synlig for andre brugere. |
| **Primær kontakt Facebook-formål**<br>mshr_primarycontactfacebookpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for persons primære Facebook-konto. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontakt LinkedIn**<br>mshr_primarycontactlinkedin<br>*Streng* | Læse/skrive<br>Valgfri | Primær LinkedIn-konto. Identificeret af brugernavn. |
| **Primær kontakt LinkedIn-beskrivelse**<br>mshr_primarycontactlinkedindescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til persons primære LinkedIn-account. |
| **Primær kontakt LinkedIn er privat**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Bestemmer, om personens primære LinkedIn-kontooplysninger deles med andre brugere. |
| **Primær kontakt LinkedIn-formål**<br>mshr_primarycontactlinkedinpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for persons primære LinkedIn-konto. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Primær kontakt Twitter**<br>mshr_primarycontacttwitter<br>*Streng* | Læse/skrive<br>Valgfri | Personens primære Twitter-konto. Identificeret af @brugernavn. |
| **Primær kontakt Twitter-beskrivelse**<br>mshr_primarycontacttwitterdescription<br>*Streng* | Læse/skrive<br>Valgfri | Beskrivelse til persons primære Twitter-account. |
| **Primær kontakt Twitter er privat**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes indstilling* | Læse/skrive<br>Valgfri | Bestemmer, om personens primære Twitter-kontooplysninger deles med andre brugere. |
| **Primær kontakt Twitter-formål**<br>mshr_primarycontacttwitterpurpose<br>*Streng* | Læse/skrive<br>Valgfri | Formålet for persons primære Twitter-konto. Konfigurer i enheden mshr_logisticslocationroleentity. |
| **Parttype**<br>mshr_partytype<br>*Streng* | Læse/skrive<br>Valgfri | Id for persons parttype. Vil altid være **person** for ansøgerne. |
| **Navnerækkefølgen vises som**<br>mshr_namesequencedisplayas<br>*Streng* | Læse/skrive<br>Valgfri | Den rækkefølge, som personens navneegenskaber er sammenføjet fra egenskaben Navn (mshr_name). |
| **Fornavn**<br>mshr_firstname<br>*Streng* | Læse/skrive<br>Påkrævet | Persons fornavn. |
| **Mellemnavn**<br>mshr_middlename<br>*Streng* | Læse/skrive<br>Valgfri | Persons mellemnavn. |
| **Præfiks for efternavn**<br>mshr_lastnameprefix<br>*Streng* | Læse/skrive<br>Valgfri | Præfiks for persons efternavn. |
| **Efternavn**<br>mshr_lastname<br>*Streng* | Læse/skrive<br>Valgfri | Personens efternavn. |
| **Elektronisk lokations-id**<br>mshr_electroniclocationid<br>*Streng* | Læse/skrive<br>Valgfri | Id for personens elektroniske placering. |
| **Tidszone for adresse**<br>mshr_addresstimezone<br>*Int* | Læse/skrive<br>Valgfri | Tidszone for persons primære adresse. |

## <a name="see-also"></a>Se også

[Introduktion til API-integration for ansøgersporingssystem](hr-admin-integration-ats-api-introduction.md)<br>
[Eksempelforespørgsel til ansøger til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]