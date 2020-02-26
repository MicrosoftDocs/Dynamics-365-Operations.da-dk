---
title: Common Data Service-enheder
description: Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008535"
---
# <a name="common-data-service-entities"></a>Common Data Service-enheder

Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.

Du kan finde flere oplysninger om Common Data Service i [Hvad er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Følgende HR-ressourcer er tilgængelige i Common Data Service .

## <a name="benefit-entities"></a>Frynsegodeenheder

**Frekvens for frynsegodeberegning**

| **Felter**        | **Datatype** | **Krævet** | **Søgbar** |
|-------------------|---------------|--------------|----------------|
| Beskrivelse       | Text          |              | X              |
| Frekvenskontrol | Grupperet indstilling    | X            | X              |
| Kan ikke ændres      | To muligheder   |              | X              |
| Navn              | Text          | X            | X              |


**Frynsegodeberegningssats**

| **Felter**  | **Datatype** | **Krævet** | **Søgbar** |
|-------------|---------------|--------------|----------------|
| Beskrivelse | Text          |              | X              |
| Navn        | Text          | X            | X              |
| Lagtype    | Grupperet indstilling    | X            | X              |


**Oplysninger om frynsegodeberegningssats**

| **Felter**                             | **Datatype**  | **Krævet** | **Søgbar** |
|----------------------------------------|----------------|--------------|----------------|
| Oplysningsnummer på frynsegodeberegningssats | Text           | X            | X              |
| Beregningssats-id                    | Opslag         | X            | X              |
| Bidragsmetode                    | Grupperet indstilling     | X            | X              |
| Gyldig                              | Kun dato      | X            | X              |
| Arbejdsgiverbidrag                  | Decimalnummer |              | X              |
| Udløb                             | Kun dato      | X            | X              |
| Arbejders fradrag                        | Decimalnummer |              | X              |


**Frynsegodetype**

| **Felter**           | **Datatype** | **Krævet** | **Søgbar** |
|----------------------|---------------|--------------|----------------|
| Samtidig tilmelding | Grupperet indstilling    |              | X              |
| Beskrivelse          | Text          |              | X              |
| Navn                 | Text          | X            | X              |
| Lønart      | Grupperet indstilling    |              | X              |


**Frynsegodeplan**

| **Felter**                               | **Datatype**  | **Krævet** | **Søgbar** |
|------------------------------------------|----------------|--------------|----------------|
| Begrænsningsmetode for restance                      | Grupperet indstilling     |              | X              |
| Frynsegodetype                             | Opslag         | X            | X              |
| Bidragsgrænsemetode                | Grupperet indstilling     |              | X              |
| Bidragsmetode                      | Grupperet indstilling     |              | X              |
| Valuta                                 | Opslag         |              | X              |
| Fradragsprioritet                       | Heltal   |              | X              |
| Grænse for standardbidragsbeløb        | Valuta       |              | X              |
| Standardbidragsbeløb for grænse (basis) | Valuta       |              | X              |
| Periode for grænse for standardbidrag        | Grupperet indstilling     |              | X              |
| Grænse for standardfradragsbeløb           | Valuta       |              | X              |
| Standardfradragsbeløb for grænse (basis)    | Valuta       |              | X              |
| Standardperiode for fradragsgrænse           | Grupperet indstilling     |              | X              |
| Beskrivelse                              | Text           |              | X              |
| Valutakurs                            | Decimalnummer |              | X              |
| Er ekstra lønkørsel                | To muligheder    |              | X              |
| Kan indberettes via Affordable Care Act        | To muligheder    |              | X              |
| Er restance genereret                      | To muligheder    |              | X              |
| Er bruttoficering                              | To muligheder    |              | X              |
| Er primær                               | To muligheder    |              | X              |
| Navn                                     | Text           | X            | X              |
| Løneffekt                           | Grupperet indstilling     |              | X              |
| Pensionstype                          | Grupperet indstilling     |              | X              |


**Ansættelsesenhed**

| **Felter**                     | **Datatype**  | **Krævet** | **Søgbar** |
|--------------------------------|----------------|--------------|----------------|
| Justeret startdato for medarbejder     | Dato og klokkeslæt  |              | X              |
| Regnskab                        | Opslag         | X            | X              |
| Beløb i enhed for medarbejderopsigelse | Decimalnummer |              | X              |
| Enhed for medarbejderopsigelse        | Grupperet indstilling     |              | X              |
| Slutdato for ansættelse            | Dato og klokkeslæt  |              | X              |
| Ansættelsesnummer              | Text           | X            | X              |
| Startdato for ansættelse          | Dato og klokkeslæt  |              | X              |
| Sidste arbejdsdag              | Dato og klokkeslæt  |              | X              |
| Overførselsdato                | Dato og klokkeslæt  |              | X              |
| Gyldig fra                     | Dato og klokkeslæt  | X            | X              |
| Gyldig til                       | Dato og klokkeslæt  |              | X              |
| Arbejdstråd                         | Opslag         | X            | X              |
| Opsigelsesbeløb til medarbejder           | Decimalnummer |              | X              |
| Startdato for medarbejder             | Dato og klokkeslæt  |              | X              |
| Arbejdertype                    | Grupperet indstilling     | X            | X              |
| Enhed for arbejderopsigelse          | Grupperet indstilling     |              | X              |

## <a name="worker-entities"></a>Enheder for arbejder

**Etnisk oprindelse**

| **Felter**         | **Datatype** | **Krævet** | **Søgbar** |
|--------------------|---------------|--------------|----------------|
| Beskrivelse        | Text          |              | X              |
| Navn på etnisk oprindelse | Text          | X            | X              |


**Sprog**

| **Felter**    | **Datatype** | **Krævet** | **Søgbar** |
|---------------|---------------|--------------|----------------|
| Beskrivelse   | Text          |              | X              |
| Sprognavn | Text          | X            | X              |


**Veteranstatus**

| **Felter**           | **Datatype** | **Krævet** | **Søgbar** |
|----------------------|---------------|--------------|----------------|
| Beskrivelse          | Text          |              | X              |
| Er beskyttet veteran | To muligheder    |              | X              |
| Sprognavn        | Text          | X            | X              |


**Arbejdstråd**

| **Felter**                | **Datatype** | **Krævet** | **Søgbar** |
|---------------------------|---------------|--------------|----------------|
| Fødselsdato                 | Kun dato     |              | X              |
| Beskrivelse               | Text          |              | X              |
| Mailadresse 1           | E-mail         |              | X              |
| Mailadresse 2           | E-mail         |              | X              |
| Facebook-id         | Text          |              | X              |
| Fornavn                | Text          |              | X              |
| Fulde navn                 | Text          |              | X              |
| Køn                    | Grupperet indstilling    |              | X              |
| Oprettelse                | Text          |              | X              |
| Er mailkontakt tilladt  | To muligheder   |              | X              |
| Er telefonkontakt tilladt  | To muligheder   |              | X              |
| Efternavn                 | Text          |              | X              |
| LinkedIn-id         | Text          |              | X              |
| Leder                   | Opslag        |              | X              |
| Mellemnavn               | Text          |              | X              |
| Mobiltelefon              | Telefon         |              | X              |
| Office Graph-identifikator   | Text          |              | X              |
| Primær mailadresse     | E-mail         |              | X              |
| Primær telefon         | Telefon         |              | X              |
| Erhverv                | Text          |              | X              |
| Socialt netværk 1          | Grupperet indstilling    |              | X              |
| Socialt netværk 2          | Grupperet indstilling    |              | X              |
| Socialt netværk-id 1 | Text          |              | X              |
| Socialt netværk-id 2 | Text          |              | X              |
| Kildetekst                    | Grupperet indstilling    | X            | X              |
| Status                    | Grupperet indstilling    | X            | X              |
| Telefon 1               | Telefon         |              | X              |
| Telefon 2               | Telefon         |              | X              |
| Telefon 3               | Telefon         |              | X              |
| Twitter-identitet          | Text          |              | X              |
| Bruger                      | Opslag        |              | X              |
| URL-adresse for websted               | URL-adresse           |              | X              |
| Arbejdernummer             | Text          | X            | X              |
| Arbejdertype               | Grupperet indstilling    | X            | X              |
| Yomi fornavn           | Text          |              | X              |
| Yomi fulde navn            | Text          |              | X              |
| Yomi efternavn            | Text          |              | X              |
| Yomi mellemnavn          | Text          |              | X              |


**Arbejders adresse**

| **Felter**           | **Datatype**  | **Krævet** | **Søgbar** |
|----------------------|----------------|--------------|----------------|
| Gadenummer       | Text           | X            | X              |
| Adressetype         | Grupperet indstilling     | X            | X              |
| Bynavn                 | Text           |              | X              |
| Land eller område    | Text           |              | X              |
| Region               | Text           |              | X              |
| Telefax                  | Telefon          |              | X              |
| Er Foretrukne         | To muligheder    |              | X              |
| Breddegrad             | Decimalnummer |              | X              |
| Linje 1               | Text           |              | X              |
| Linje 2               | Text           |              | X              |
| Linje 3               | Text           |              | X              |
| Længdegrad            | Decimalnummer |              | X              |
| Postnummer          | Text           |              | X              |
| Postboksnummer      | Text           |              | X              |
| Forsendelsesmetodekode | Heltal   |              | X              |
| Delstat eller provins    | Text           |              | X              |
| Telefon 1          | Telefon          |              | X              |
| Telefon 2          | Telefon          |              | X              |
| Telefon 3          | Telefon          |              | X              |
| USP-zone             | Text           |              | X              |
| UTC-modkontering           | Heltal   |              | X              |
| Arbejdstråd               | Opslag         | X            | X              |


**Arbejders personlige oplysninger**

| Felter                             | Datatype    | Obligatorisk | Søgbar |
|------------------------------------|--------------|----------|------------|
| Fødeby                         | Text         |          | X          |
| Fødeland eller -område            | Grupperet indstilling   |          | X          |
| Fødselsdato                          | Kun dato    |          | X          |
| Land eller område for statsborgerskab      | Grupperet indstilling   |          | X          |
| Dato for medarbejders død                      | Kun dato    |          | X          |
| Dato for bekræftelse af handicappet veteran | Kun dato    |          | X          |
| Uddannelse                          | Text         |          | X          |
| Etnisk oprindelse                     | Opslag       |          | X          |
| Slutdato for udstationering                  | Kun dato    |          | X          |
| Startdato for udstationering                | Kun dato    |          | X          |
| Fars fødeland eller -område     | Grupperet indstilling   |          | X          |
| Køn                             | Grupperet indstilling   |          | X          |
| Er handicappet                        | To muligheder  |          | X          |
| Er handicappet veteran                | To muligheder  |          | X          |
| Gælder der regler for udstationering    | To muligheder  |          | X          |
| Er fuldtidsstuderende               | To muligheder  |          | X          |
| Ægteskabelig status                     | Grupperet indstilling   |          | X          |
| Slutdato for militærtjeneste          | Kun dato    |          | X          |
| Startdato for militærtjeneste        | Kun dato    |          | X          |
| Mors fødeland eller -område     | Grupperet indstilling   |          | X          |
| Nationalitet, land eller område      | Grupperet indstilling   |          | X          |
| Modersmål                    | Opslag       |          | X          |
| Antal personer i husstand               | Heltal |          |            |
| Veteranstatus                     | Opslag       |          | X          |
| Arbejdstråd                             | Opslag       | X        | X          |
| Arbejders personlige nummer      | Text         | X        | X          |


**Arbejders bankkonto**

| **Felter**                 | **Datatype** | **Krævet** | **Søgbar** |
|----------------------------|---------------|--------------|----------------|
| Kontoindehaver             | Text          |              | X              |
| Konto-id     | Text          |              | X              |
| Beskrivelse af adresse        | Text          |              | X              |
| Bankkontotype          | Grupperet indstilling    |              | X              |
| Bankens lokationskode         | Text          |              | X              |
| Afdelingsnavn                | Text          |              | X              |
| Afdelingsnummer              | Text          |              | X              |
| Bynavn                       | Text          |              | X              |
| Land eller område          | Text          |              | X              |
| Region                     | Text          |              | X              |
| Beskrivelse                | Text          |              | X              |
| Distriktsnavn              | Text          |              | X              |
| E-mail                      | Text          |              | X              |
| Forlængelse                  | Text          |              | X              |
| Telefax                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Linje 1                     | Text          |              | X              |
| Linje 2                     | Text          |              | X              |
| Linje 3                     | Text          |              | X              |
| Mobiltelefon               | Text          |              | X              |
| Personnavn             | Text          |              | X              |
| Postnummer                | Text          |              | X              |
| Postboksnummer            | Text          |              |                |
| Registreringsnummer             | Text          |              | X              |
| Registreringsnummertype        | Grupperet indstilling    |              | X              |
| Delstat eller provins          | Text          |              | X              |
| SWIFT-kode                 | Text          |              | X              |
| Telefon                  | Text          |              | X              |
| Telexnummer               | Text          |              | X              |
| URL-adresse for websted                | Text          |              | X              |
| Arbejdstråd                     | Opslag        | X            | X              |
| Arbejders bankkontonummer | Text          |              | X              |
| Arbejders bankkontonummer | Text          | X            | X              |

**Arbejders faste løn**

| Felter                                | Datatype      | Obligatorisk | Søgbar |
|---------------------------------------|----------------|----------|------------|
| Regnskab                               | Opslag         | X        | X          |
| Kompensationstype                     | Grupperet indstilling     |          | X          |
| Valuta                              | Opslag         |          | X          |
| Ikrafttrædelsesdato                        | Kun dato      |          | X          |
| Hændelse                                 | Opslag         | X        | X          |
| Valutakurs                         | Decimalnummer |          | X          |
| Udløbsdato                       | Kun dato      |          | X          |
| Linjenummer                           | Decimalnummer |          | X          |
| Lønfrekvens                         | Opslag         | X        | X          |
| Lønsats                              | Valuta       |          | X          |
| Lønsats (basis)                       | Valuta       |          | X          |
| Plan                                  | Opslag         | X        | X          |
| Stilling                              | Opslag         | X        | X          |
| Procestype                          | Grupperet indstilling     | X        | X          |
| Linje for opsætning af referencepunkt            | Opslag         |          | X          |
| Arbejdstråd                                | Opslag         | X        | X          |
| Arbejders faste lønnummer      | Text           | X        | X          |

**Personidentifikationsnummeret for arbejder**

| Felter                 | Datatype   | Obligatorisk | Søgbar |
|------------------------|-------------|----------|------------|
| Beskrivelse            | Text        |          | X          |
| Posttype             | Text        |          | X          |
| Udløbsdato        | Kun dato   |          | X          |
| Identifikationsnummer  | Text        | X        | X          |
| Identifikationstype    | Opslag      | X        | X          |
| Er primær             | To muligheder |          | X          |
| Udstedelsesdato             | Kun dato   |          | X          |
| Udstedende organ         | Opslag      | X        | X          |
| Arbejdstråd                 | Opslag      | X        | X          |


## <a name="position-entities"></a>Stillingsenheder

**Stilling**

| **Felter**               | **Datatype**  | **Krævet** | **Søgbar** |
|--------------------------|----------------|--------------|----------------|
| Aktivering               | Dato og klokkeslæt  |              | X              |
| Tilgængelig for tildeling | Dato og klokkeslæt  |              | X              |
| Afdeling               | Opslag         |              | X              |
| Beskrivelse              | Text           |              | X              |
| Fuldtidsækvivalent     | Decimalnummer |              | X              |
| Stilling                      | Opslag         | X            | X              |
| Stillingsnummer      | Text           | X            | X              |
| Overordnet stilling      | Opslag         |              | X              |
| Stillingstype            | Opslag         |              | X              |
| Pension               | Dato og klokkeslæt  |              | X              |
| Stilling                    | Grupperet indstilling     |              | X              |
| Gyldig fra               | Dato og klokkeslæt  | X            | X              |
| Gyldig til                 | Dato og klokkeslæt  |              | X              |


**Stillingstype**

| **Felter**         | **Datatype** | **Krævet** | **Søgbar** |
|--------------------|---------------|--------------|----------------|
| Klassifikation     | Grupperet indstilling    |              | X              |
| Beskrivelse        | Text          |              | X              |
| Navn på stillingstype | Text          | X            | X              |


**Arbejdertildeling til stilling**

| **Felter**                        | **Datatype** | **Krævet** | **Søgbar** |
|-----------------------------------|---------------|--------------|----------------|
| Stilling                      | Opslag        | X            | X              |
| Arbejdertildelingsnummer til stilling | Text          | X            | X              |
| Gyldig fra                        | Text          | X            | X              |
| Gyldig til                          |               |              | X              |
| Arbejdstråd                            |               | X            | X              |

## <a name="job-entities"></a>Jobenheder

**Stilling**

| **Felter**                   | **Datatype**  | **Krævet** | **Søgbar** |
|------------------------------|----------------|--------------|----------------|
| Tillad ubegrænsede stillinger    | To muligheder    |              | X              |
| Standardfuldtidsækvivalent | Decimalnummer |              | X              |
| Beskrivelse                  | Text           |              | X              |
| Stillingsbeskrivelse              | Text           |              | X              |
| Jobfunktion                 | Opslag         |              | X              |
| Jobtype                     | Opslag         |              | X              |
| Maksimalt antal stillinger  | Heltal   |              | X              |
| Navn                         | Text           | X            | X              |
| Stilling                        | Grupperet indstilling     |              | X              |
| Gyldig fra                   | Dato og klokkeslæt  | X            | X              |
| Gyldig til                     | Dato og klokkeslæt  |              | X              |


**Jobfunktion**

| **Felter**        | **Datatype** | **Krævet** | **Søgbar** |
|-------------------|---------------|--------------|----------------|
| Beskrivelse       | Text          | X            | X              |
| Jobfunktionsnavn | Text          | X            | X              |


**Jobtype**

| **Felter**    | **Datatype** | **Krævet** | **Søgbar** |
|---------------|---------------|--------------|----------------|
| Beskrivelse   | Text          | X            | X              |
| Momsfri status | Grupperet indstilling    | X            | X              |
| Jobtypenavn | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>Orlovs- og fraværsenheder

**Orlovstilmelding**

| **Felter**            | **Datatype** | **Krævet** | **Søgbar** |
|-----------------------|---------------|--------------|----------------|
| Grundlag for periodiseringsdato    | Kun dato     | X            | X              |
| Startdato for periodisering    | Kun dato     | X            | X              |
| Brugerdefineret dato           | Kun dato     | X            | X              |
| Er periodisering afbrudt  | To muligheder   |              | X              |
| Orlovstilmeldingsnummer | Text          | X            | X              |
| Orlovsplan            | Opslag        | X            | X              |
| Startdato            | Kun dato     | X            | X              |
| Niveaubasis            | Grupperet indstilling    | X            | X              |
| Arbejdstråd                | Opslag        | X            | X              |


**Orlovsbanktransaktion**

| **Felter**                    | **Datatype**  | **Krævet** | **Søgbar** |
|-------------------------------|----------------|--------------|----------------|
| Beløb                        | Decimalnummer | X            | X              |
| Regnskab                       | Opslag         | X            | X              |
| Banktransaktionsnummer for orlov | Text           | X            | X              |
| Orlovsplan                    | Opslag         |              | X              |
| Orlovstype                    | Opslag         | X            | X              |
| Posteringsdato              | Kun dato      | X            | X              |
| Transaktionsnummer            | Decimalnummer | X            | X              |
| Transaktionstype              | Grupperet indstilling     | X            | X              |
| Arbejdstråd                        | Opslag         | X            | X              |


**Orlovsplan**

| **Felter**        | **Datatype** | **Krævet** | **Søgbar** |
|-------------------|---------------|--------------|----------------|
| Periodiseringsfrekvens | Grupperet indstilling    | X            | X              |
| Regnskab           | Opslag        | X            | X              |
| Beskrivelse       | Text          |              | X              |
| Orlovstype        | Opslag        | X            | X              |
| Navn              | Text          | X            | X              |
| Startdato        | Kun dato     | X            | X              |


**Orlovsanmodning**

| **Felter**           | **Datatype** | **Krævet** | **Søgbar** |
|----------------------|---------------|--------------|----------------|
| Kommentar              | Text          | X            | X              |
| Regnskab              | Opslag        | X            | X              |
| Orlovsanmodningsnummer | Text          |              | X              |
| Anmodningsdato         | Dato og klokkeslæt | X            | X              |
| Status               | Grupperet indstilling    | X            | X              |
| Arbejdstråd               | Opslag        | X            | X              |


**Detaljer om orlovsanmodning**

| **Felter**                  | **Datatype**  | **Krævet** | **Søgbar** |
|-----------------------------|----------------|--------------|----------------|
| Beløb                      | Decimalnummer | X            | X              |
| Orlovsdato                  | Dato og klokkeslæt  | X            | X              |
| Orlovsanmodning               | Opslag         | X            | X              |
| Detaljenummer på orlovsanmodning | Text           | X            | X              |
| Orlovstype                  | Opslag         | X            | X              |


**Orlovstype**

| **Felter**      | **Datatype** | **Krævet** | **Søgbar** |
|-----------------|---------------|--------------|----------------|
| Regnskab         | Opslag        | X            | X              |
| Beskrivelse     | Text          |              | X              |
| Lønkode    | Opslag        |              | X              |
| Navn på orlovstype | Text          | X            | X              |


**Arbejdskalender**

| **Felter**  | **Datatype** | **Krævet** | **Søgbar** |
|-------------|---------------|--------------|----------------|
| Regnskab     | Opslag        | X            | X              |
| Beskrivelse | Text          |              | X              |
| Navn        | Text          | X            | X              |


**Arbejdskalenderdag**

| **Felter**               | **Datatype** | **Krævet** | **Søgbar** |
|--------------------------|---------------|--------------|----------------|
| Kalenderdato            | Kun dato     | X            | X              |
| Regnskab                  | Opslag        |              | X              |
| Status                   | Text          |              | X              |
| Arbejdskalender            | Opslag        | X            | X              |
| Nummer på arbejdskalenderdag | Text          | X            | X              |


**Arbejdskalenderfridag**

| **Felter**  | **Datatype** | **Krævet** | **Søgbar** |
|-------------|---------------|--------------|----------------|
| Navn        | Text          |              | X              |
| Beskrivelse | Text          | X            | X              |


**Ferielinje i arbejdskalender**

| **Felter**                        | **Datatype** | **Krævet** | **Søgbar** |
|-----------------------------------|---------------|--------------|----------------|
| Feriedato                      | Kun dato     | X            | X              |
| Navn                              | Text          |              | X              |
| Arbejdskalenderfridag             | Opslag        | X            | X              |
| Nummer på ferielinje i arbejdskalender | Text          | X            | X              |


**Tidsinterval i arbejdskalender**

| **Felter**                         | **Datatype** | **Krævet** | **Søgbar** |
|------------------------------------|---------------|--------------|----------------|
| Regnskab                            | Opslag        |              | X              |
| Sluttidspunkt                           | Heltal  |              | X              |
| Starttidspunkt                         | Heltal  |              | X              |
| Arbejdskalender                      | Opslag        | X            | X              |
| Arbejdskalenderdag                  | Opslag        | X            | X              |
| Nummer på tidsinterval i arbejdskalender | Text          | X            | X              |

## <a name="organization-entities"></a>Organisationsenheder

**Regnskab**

| **Felter**   | **Datatype** | **Krævet** | **Søgbar** |
|--------------|---------------|--------------|----------------|
| Firmakode | Text          | X            | X              |
| Navn         | Text          | X            | X              |


**Afdeling**

| **Felter**        | **Datatype** | **Krævet** | **Søgbar** |
|-------------------|---------------|--------------|----------------|
| Afdelingsnummer | Text          | X            | X              |
| Beskrivelse       | Text          |              | X              |
| Navn              | Text          | X            | X              |
| Overordnet afdeling | Opslag        |              | X              |


**Valuta**

| **Felter**         | **Datatype**  | **Krævet** | **Søgbar** |
|--------------------|----------------|--------------|----------------|
| Valutakode      | Text           | X            | X              |
| Valutanavn      | Text           | X            | X              |
| Valutapræcision | Heltal   | X            | X              |
| Valutasymbol    | Text           | X            | X              |
| Enhedsbillede       | Billede          |              |                |
| Valutakurs      | Decimalnummer | X            | X              |
| Organisation       | Opslag         | X            | X              |
| Status             | Grupperet indstilling     |              | X              |

## <a name="payroll-entities"></a>Lønenheder

**Betalingscyklus**

| **Felter**  | **Datatype** | **Krævet** | **Søgbar** |
|-------------|---------------|--------------|----------------|
| Beskrivelse | Text          | X            | X              |
| Frekvens   | Grupperet indstilling    | X            | X              |
| Navn        | Text          | X            | X              |


**Lønperiode**

| **Felter**           | **Datatype** | **Krævet** | **Søgbar** |
|----------------------|---------------|--------------|----------------|
| Standardbetalingsdato | Kun dato     |              | X              |
| Beskrivelse          | Text          |              | X              |
| Betalingscyklus            | Se          | X            | X              |
| Lønperiodenummer    | Text          | X            | X              |
| Periodens slutdato      | Kun dato     | X            | X              |
| Periodens startdato    | Kun dato     | X            | X              |
| Status               | Grupperet indstilling    |              | X              |


**Lønkode**

| **Felter**              | **Datatype** | **Krævet** | **Søgbar** |
|-------------------------|---------------|--------------|----------------|
| Beskrivelse             | Text          | X            | X              |
| Inkluder i betalingstype | Grupperet indstilling    | X            | X              |
| Er produktiv           | To muligheder   | X            | X              |
| Navn                    | Text          |              | X              |
| Mængdeenhed           | Grupperet indstilling    |              | X              |
| Spor FMLA-timer        | To muligheder   |              | X              |


**Skatteområde**

| **Felter**        | **Datatype** | **Krævet** | **Søgbar** |
|-------------------|---------------|--------------|----------------|
| Bynavn              | Text          |              | X              |
| Land eller område | Text          |              | X              |
| Region            | Text          |              | X              |
| Navn              | Text          | X            | X              |
| Delstat eller provins | Text          |              | X              |


**Frynsegoders beregningsfrekvens, lønperiode**

| **Felter**                                      | **Datatype** | **Krævet** | **Søgbar** |
|-------------------------------------------------|---------------|--------------|----------------|
| Frekvens for frynsegodeberegning                   | Opslag        | X            | X              |
| Nummer på frynsegoders beregningsfrekvens, lønperiode | Text          | X            | X              |
| Lønperiode                                      | Opslag        | X            | X              |


**Bankkontoudbetalinger**

| **Felter**                       | **Datatype**  | **Krævet** | **Søgbar** |
|----------------------------------|----------------|--------------|----------------|
| Beløb                           | Valuta       |              | X              |
| Beløb (basis)                    | Valuta       |              | X              |
| Bankkonto                     | Opslag         | X            | X              |
| Nummer på bankkontoudbetalinger | Text           | X            | X              |
| Regnskab                          | Opslag         | X            | X              |
| Valuta                         | Opslag         |              | X              |
| Valutakurs                    | Decimalnummer |              | X              |
| Er restbeløb                     | To muligheder    |              | X              |
| Prioritet                         | Heltal   |              | X              |

**Udstedende organ for personidentifikation**

| **Felter**           | **Datatype** | **Krævet** | **Søgbar** |
|----------------------|---------------|--------------|----------------|
| Beskrivelse af adresse  | Text          |              | X              |
| Adresselinje 1       | Text          |              | X              |
| Adresselinje 2       | Text          |              | X              |
| Adresselinje 3       | Text          |              | X              |
| Bynavn                 | Text          |              | X              |
| Land eller område    | Grupperet indstilling    |              | X              |
| Region               | Text          |              | X              |
| Beskrivelse          | Text          |              | X              |
| E-mail                | Text          |              | X              |
| Forlængelse            | Text          |              | X              |
| Telefax                  | Text          |              | X              |
| Navn på udstedende organ  | Text          | X            | X              |
| Mobiltelefon         | Text          |              | X              |
| Side                 | Text          |              | X              |
| Postnummer          | Text          |              | X              |
| Postboksnummer      | Text          |              | X              |
| Sms                  | Text          |              | X              |
| Delstat eller provins    | Text          |              | X              |
| Telefon            | Text          |              | X              |
| Telex                | Text          |              | X              |
| URL-adresse for websted          | Text          |              | X              |

**Personidentifikationstype for arbejder**

| **Felter**                        | **Datatype**  | **Krævet** | **Søgbar** |
|-----------------------------------|----------------|--------------|----------------|
| Tilladte værdier                    | Grupperet indstilling     |              | X              |
| Land eller område                 | Text           |              | X              |
| Beskrivelse                       | Text           |              | X              |
| Fast længde                      | Heltal   |              | X              |
| Format af identifikationsnummer      | Text           |              | X              |
| Type                              | Grupperet indstilling     |              | X              |
| Personidentifikationstype for arbejder | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Enheder for fast løn

**Kompensation - fast struktur**

| **Felter**                  | **Datatype** | **Krævet** | **Søgbar** |
|-----------------------------|---------------|--------------|----------------|
| Regnskab                     | Opslag        | X            | X              |
| Kompensationsgitter           | Opslag        |              | X              |
| Valuta                    | Opslag        | X            | X              |
| Beskrivelse                 | Text          | X            | X              |
| Ikrafttrædelsesdato              | Kun dato     | X            | X              |
| Udløbsdato             | Kun dato     | X            | X              |
| Ansættelsesregel                   | Grupperet indstilling    | X            | X              |
| Navn                        | Text          | X            | X              |
| Tolerance uden for afgrænsningerne      | Grupperet indstilling    | X            | X              |
| Lønfrekvens               | Opslag        | X            | X              |
| Anbefaling tilladt      | To muligheder   | X            | X              |
| Opsætning af referencepunktlinje  | Opslag        |              | X              |
| Type                        | Grupperet indstilling    | X            | X              |

**Kompensationsgitter**

| **Felter**                  | **Datatype** | **Krævet** | **Søgbar** |
|-----------------------------|---------------|--------------|----------------|
| Regnskab                     | Opslag        | X            | X              |
| Valuta                    | Opslag        |              | X              |
| Beskrivelse                 | Text          | X            | X              |
| Ikrafttrædelsesdato              | Kun dato     |              | X              |
| Udløbsdato             | Kun dato     |              | X              |
| Navn                        | Text          | X            | X              |
| Opsætning af referencepunkt       | Opslag        | X            | X              |
| Type                        | Grupperet indstilling    | X            | X              |

**Kompensationsniveau**

| **Felter**      | **Datatype** | **Krævet** | **Søgbar** |
|-----------------|---------------|--------------|----------------|
| Beskrivelse     | Text          |              | X              |
| Navn            | Text          | X            | X              |
| Type            | Grupperet indstilling     | X            | X              |

**Kompensation - lønfrekvens**

| **Felter**                  | **Datatype**   | **Krævet** | **Søgbar** |
|-----------------------------|-----------------|--------------|----------------|
| Årlig omregningsfaktor    | Decimalnummer  |              | X              |
| Regnskab                     | Opslag          | X            | X              |
| Beskrivelse                 | Text            |              | X              |
| Omregningsfaktor pr. time    | Decimalnummer  |              | X              |
| Månedlig omregningsfaktor   | Decimalnummer  |              | X              |
| Navn                        | Text            | X            | X              |
| Termin                      | Grupperet indstilling      |              | X              |
| Ugentlig omregningsfaktor    | Grupperet indstilling      |              | X              |


**Opsætning af kompensationsreferencepunkt**

| **Felter**          | **Datatype**   | **Krævet** | **Søgbar** |
|---------------------|-----------------|--------------|----------------|
| Regnskab             | Opslag          | X            | X              |
| Kompensationstype   | Grupperet indstilling      | X            | X              |
| Beskrivelse         | Text            | X            | X              |
| Navn                | Text            | X            | X              |

**Opsætningslinje for kompensationsreferencepunkt**

| **Felter**            | **Datatype**   | **Krævet** | **Søgbar** |
|-----------------------|-----------------|--------------|----------------|
| Regnskab               | Opslag          | X            | X              |
| Beskrivelse           | Text            | X            | X              |
| Linjenummer           | Decimalnummer  | X            | X              |
| Navn                  | Text            | X            | X              |
| Opsætning af referencepunkt | Opslag          | X            | X              |

**Kompensationsområde**

| **Felter**      | **Datatype** | **Krævet** | **Søgbar** |
|-----------------|---------------|--------------|----------------|
| Beskrivelse     | Text          | X            | X              |
| Navn            | Text          | X            | X              |

**Kompensationsstruktur**

| **Felter**                    | **Datatype**   | **Krævet** | **Søgbar** |
|-------------------------------|---------------  |--------------|----------------|
| Beløb                        | Valuta        |              | X              |
| Beløbsgrundlag                   | Valuta        |              | X              |
| Regnskab                       | Opslag          | X            | X              |
| Kompensationsstrukturnummer | Text            | X            | X              |
| Valuta                      | Opslag          |              | X              |
| Valutakurs                 | Decimalnummer  |              | X              |
| Gitter                          | Opslag          | X            | X              |
| Niveau                         | Opslag          | X            | X              |
| Referencepunkt               | Opslag          | X            | X              |
| Opsætning af referencepunktlinje    | Opslag          | X            | X              |

**Hændelse for fast løn**

| **Felter**            | **Datatype**   | **Krævet** | **Søgbar** |
|-----------------------|-----------------|--------------|----------------|
| Regnskab               | Opslag          | X            | X              |
| Beskrivelse           | Text            | X            | X              |
| Hændelsestype            | Grupperet indstilling      | X            | X              |
| Er aktiv             | To muligheder     | X            |                |
| Navn                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Enhedsrelationsmodeller

### <a name="worker"></a>Arbejdstråd
![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stilling og job
![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Frynsegoder
![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensation
![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Orlov
![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbejdskalender
![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)
