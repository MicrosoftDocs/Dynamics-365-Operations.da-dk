---
title: Registrerings-id'er
description: Dette emne indeholder oplysninger om opsætning og brug af registrerings-id'er.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: kfend
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: def0b35043f0a660e2a167b78cf0c65cd1e8b2fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006028"
---
# <a name="registration-ids"></a>Registrerings-id'er

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om opsætning og brug af registrerings-id'er.

Mange lande og områder har forskellig lovgivning og krav til registrering af registreringsnumre eller -id'er. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling af understøttede registreringstyper for parter i forskellige europæiske lande. Alle lande har deres krav til understøttelse af forskellige landespecifikke funktioner, der er relateret til registreringsnumre, der leveres af forskellige offentlige kontorer. Eksempler på registreringsnumre omfatter personnummer (SSN), identifikationsnummer for skat (TIN) og europæisk moms-id (EU-moms-id). Denne funktion indeholder fælles rammer for alle lande i alle områder under hensyntagen til landespecifikke krav i visse europæiske lande. I følgende afsnit beskrives den samlede strøm af oplysninger, der bruges til konfiguration og behandling af registrerings-id'er.

## <a name="registration-type-creation"></a>Konfiguration af registreringstype
Før du kan angive registrerings-id, skal du oprette momsregistreringstyper for de forskellige typer registreringsnumre, hver part er underlagt. Gå til siden **Virksomhedsadministration** &gt; **Globalt adressekartotek** &gt; **Registreringstyper** &gt; **Registreringstyper** for at oprette og administrere registreringstyper for leverandører, kunder, medarbejdere og juridiske enheder i forskellige lande.

|Felt                 |Betegnelse      |
|------------------------------|----------------------------|                                                                           
| Navn                | Navnet på registreringstypen. |                                                                           
| Betegnelse         | Beskrivelsen af registreringstypen. |
| Land/område      | Entydig identifikator af landet/området.|
| Momsmyndighed       | Den momsmyndighed, der er tilknyttet registreringstypen.|
| Begrænset til       | Den type begrænsning, der gælder for momsregistreringstypen: Ingen, Person, Organisation.|
| Formater              | Registreringstypens valideringsformat.|
| Kan blive opdateret      | Definerer, om registreringsnummeret for registreringstypen kan opdateres, efter at det er angivet.|
| Unik              | Definerer, om registreringsnummeret for registreringstypen entydigt. |
| Primært til land/område | Hvis en part er knyttet til en eller flere adresser i et bestemt land og registrerings-id'et er gyldigt for alle disse adresser, skal du angive én adresse som primær for landet. Du kan kun registrere ét id som primært. Angiver, om registreringsnummeret kun kan angives for primær for landeadresse. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Tildel en registreringstype til en registreringskategori.
Registreringskategori er landets/områdets registrerings-identifikator, der er godkendt til brug i bestemt land/område til moms, told og andre formål. Denne kategori definerer valideringsreglerne for bestemt registrerings-ID (herunder kontrolcifre osv.) og registrerings-ID for optagelse i forskellige rapporter. Brug siden **Virksomhedsadministration** &gt; **Globalt adressekartotek** &gt; **Registreringstyper** &gt; **Registreringskategorier** til at tildele registreringstypen for det pågældende land til den understøttede registreringskategori.

| Felt            | Betegnelse|
|-----------------------|----------------|
| Registreringstype     | Registreringstypen i et bestemt land/område.|
| Begrænset til         | Den type begrænsning, der gælder for momsregistreringstypen: Ingen, Person, Organisation.|
| Registreringskategori | Det entydige registrering-id, der er godkendt til brug i landet. Den fuldstændige liste over understøttede kategorier vises senere i dette emne. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Angiv registrering-id'er for poster i globalt adressekartotek

Det globale adressekartotek (GAB) indeholder konsoliderede adresseoplysninger for debitorer, kreditorer, kontakter, forretningsforbindelser og juridiske enheder. Du kan finde flere oplysninger under [Oversigt over globalt adressekartotek](../../fin-and-ops/organization-administration/overview-global-address-book.md). De partposter, der er gemt i det globale adressekartotek, kan indeholde en eller flere adresseposter. Disse adresser bruges til forskellige formål, f.eks. fakturering eller levering. Du kan konfigurere registrerings-id'er for adresseoplysninger for debitorer, kreditorer, arbejdstagere og juridiske enheder. Find den partspost (juridisk enhed, kreditor, debitor, arbejder), som du vil angive registrerings-id, og klik derefter på **Registrerings-id'er** i formularer, der er relateret til part, juridisk enhed, kreditor, debitor, arbejder for at åbne siden **Administrer adresser**. Under fanen **Momsregistrering** skal du klikke på **Tilføj** og angiv følgende oplysninger om registrerings-id'et.


|Felt                |Betegnelse                                                |
|---------------------|-----------------------------------------------------------|
| Registreringstype   | Registreringstypen i det valgte land/område.     |
| Registreringsnummer | Partens registrerings-ID.                                |
| Betegnelse         | Beskrivelsen af registreringsnummeret.               |
| Sektion             | Yderligere oplysninger om registreringsnummeret. |
| Udstedende organ      | Den myndighed, der har udstedt registreringsnummeret.        |
| Udstedelsesdato         | Registreringsnummerets udstedelsesdato.              |
| Gyldig           | Registreringsnummerets ikrafttrædelsesdato.           |
| Udløb          | Registreringsnummerets udløbsdato.          |

> [!NOTE]
> SE-nummeret for den juridiske enhed, kreditor, debitor kan vælges fra registrerings-id'er, der er relateret til moms-id'et og angivet for parten.

## <a name="search-for-records-by-registration-id"></a>Søge efter poster pr. registrerings-id
Søgning efter partposter, der er baseret på et registrerings-ID, er tilgængelig i formularer, der er relateret til part, juridisk enhed, kreditor, debitor og arbejder. Klik på indstillingen **Søgning efter registrerings-id** for at åbne siden **Søgekriterier for registrerings-id**. Angiv søgekriterier, og klik på **Find**. Systemet viser de valgte poster fra det globale adressekartotek og partpostens tilknyttede typer.

## <a name="supported-registration-categories"></a>Understøttede registreringskategorier
Følgende tabel viser de understøttede registreringstyper. Hvis du er fortrolig med Microsoft Dynamics AX 2012-felter til registrering af id'er, knytter denne tabel også disse felter til registreringskategorier i Dynamics 365 Finance.

| Finance-registreringskategori         |Land/område  | Dynamics AX 2012 udtryk/felt|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Moms-id                                                        | Alle lande i Den Europæiske Union (EU)|  SE-nummer (lovgivningsmæssig type MOMS-ID i AX 2012 R3)|
| Virksomheds-id (COID)                                          | Belgien Tjekkiet Estland Ungarn Letland Litauen Polen Schweiz | Virksomhedsnummer (EnterpriseNumber) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Registreringsnummer (RegNum\_W) Virksomhedskode (EnterpriseCode) Registreringsnummer (RegNum\_W) UID (lovgivningsmæssig type UID i AX 2012 R3) |
| Afdelings-id                                                     | Belgien            | Afdelingsnummer (BranchNumber)|
| Spisová značka (registreringsnummer, udstedende organ, afsnit) | Tjekkiet     | Registreringsnummer (CommercialRegisterInsetNumber) Opbevaret på handelsregister (CommercialRegister) Sektion for handelsregister(CommercialRegisterSection)|
| Toldmyndighedens debitor-id                                           | Finland | Tolddebitornummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Den Russiske Føderation| INN (lovgivningsmæssig type INN i AX 2012 R3)|
| RRC                                                           | Den Russiske Føderation| RRC (lovgivningsmæssig type RRC i AX 2012 R3)|
| OKDP                                                          | Den Russiske Føderation| OKDP (lovgivningsmæssig type OKDP i AX 2012 R3)|
| OKPO                                                          | Den Russiske Føderation| OKPO (lovgivningsmæssig type OKPO i AX 2012 R3)|
| RCOAD                                                         | Den Russiske Føderation| RCOAD (lovgivningsmæssig type RCOAD i AX 2012 R3)|
| OGRN                                                          | Den Russiske Føderation| OGRN (lovgivningsmæssig type OGRN i AX 2012 R3) |
| SNILS                                                         | Den Russiske Føderation| SNILS (lovgivningsmæssig type SNILS i AX 2012 R3)|
| CIFTS                                                         | Den Russiske Føderation| CIFTS (lovgivningsmæssig type CIFTS i AX 2012 R3)|
| Pas                                                      | Spanien             | Pas|
| Officielt identifikationsdokument                              | Spanien             | Officielt identifikationsdokument|
| Bopælscertifikat                                         | Spanien             | Bopælscertifikat|
| Andet identifikationsdokument                                 | Spanien             | Andet identifikationsdokument|
| Ingen census                                                  | Spanien             | Ikke tilgængelig i AX 2012 R3|


Du kan finde flere oplysninger om behandling af registrerings-id'er, herunder nødvendige forudsætninger, i følgende opgaveregistreringer for moms-ID i Lifecycle Services (LCS):

-   Opsætning af moms-id
-   Moms-id-registrering for kreditor
-   Parts søgning ved hjælp af moms-id




