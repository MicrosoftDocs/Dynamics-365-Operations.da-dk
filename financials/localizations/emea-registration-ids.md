---
title: Registrerings-id&quot;er
description: "Dette emne indeholder oplysninger om opsætning og brug af registrering id&quot;er."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Registrerings-id'er

Dette emne indeholder oplysninger om opsætning og brug af registrering id'er.

Mange lande og områder har forskellig lovgivning og krav til registrering af registreringsnumre eller -id'er. Dette emne indeholder en oversigt over de nødvendige indstillinger og behandling af understøttede registreringstyper for parter i forskellige europæiske lande. Alle lande har deres krav til understøttelse af forskellige landespecifikke funktioner, der er relateret til registreringsnumre, der leveres af forskellige tilstand kontorer. Eksempler på registreringsnumre omfatter personnummer (SSN), identifikationsnummer for skat (TIN) og europæiske moms-id (EU-moms-ID). Denne funktion indeholder fælles rammer for alle lande i alle regioner under hensyntagen til konto landespecifikke krav i visse lande. I følgende afsnit beskrives den samlede strøm af oplysninger, der bruges til oprettelse og behandling af registrering id'er.

## <a name="registration-type-creation"></a>Registrering af typen oprettelse
Før du kan angive registrerings-ID, skal du angive registreringstyper for de forskellige typer registreringsnumre, hver part er underlagt. Gå til **virksomhedsadministration**&gt;**globale adressekartotek**&gt;**registreringstyper**&gt;**registreringstyper** til at oprette og administrere registreringstyper for leverandører, kunder, medarbejdere og juridiske enheder i forskellige lande.

|Felt                 |Betegnelse      |
|------------------------------|----------------------------|                                                                           
| Navn                | Navnet på registreringstypen. |                                                                           
| Betegnelse         | Beskrivelse af registreringstypen. |
| Land/område      | Entydig identifier af land/området.|
| Momsmyndighed       | Den skattemyndighed, der er knyttet til registreringstypen.|
| Begrænset til       | Typen begrænsning, der gælder for momsregistreringstypen: ingen Person, organisation.|
| Formater              | Formatet for registreringstypen validering.|
| Kan blive opdateret      | Angiver, om registreringsnummeret for registreringstypen kan opdateres, når den er angivet.|
| Unik              | Angiver, om registreringsnummeret for registreringstypen er entydigt. |
| Primært til land/område | Hvis en part er knyttet til en eller flere adresser i land og registrerings-ID er gyldig for alle disse adresser, skal du angive en adresse som primær for landet. Du kan kun registrere én-ID som primær. Angiver, om CVR-nummeret kan angives kun for primær adresse i land. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Tildele en registrering til en registrering-kategori
Registrering af kategori er land registrering id, der er godkendt til brug af navnlig land for skat, told og andre formål. Denne kategori definerer valideringsreglerne af særlige registrerings-ID (herunder kontrolcifre osv.) og registrerings-ID for optagelse i forskellige rapporter. Brug siden **virksomhedsadministration**&gt;**globale adressekartotek**&gt;**registreringstyper**&gt;**registrering kategorier** skal tildeles understøttede registrering kategori registreringstype for det pågældende land.

| Felt            | Betegnelse|
|-----------------------|----------------|
| Registreringstype     | Registreringen Skriv navnlig land.|
| Begrænset til         | Typen begrænsning gælder for momsregistreringstypen: ingen Person, organisation.|
| Registreringskategori | Hver enkel entydig registrering-id, der er godkendt til brug i landet. Den komplette liste af understøttede i AX7.1 kategorier er under. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Angiv registrering id'er for globale adressekartoteksposter
Det globale adressekartotek (GAB) i Microsoft Dynamics 365 for operationer indeholder konsoliderede adresseoplysninger for debitorer, kreditorer, kontaktpersoner, forretningsforbindelser og juridiske enheder. Yderligere oplysninger finder [oversigt over globalt adressekartotek](/dynamics365/operations/organization-administration/overview-global-address-book). De partposter, der er gemt i det globale adressekartotek kan indeholde en eller flere adresseposter. Disse adresser bruges til forskellige formål, f.eks. fakturering eller levering. Du kan konfigurere registrering id'er for adresseoplysninger for debitorer, kreditorer, arbejdstagere og juridiske enheder. Find part (juridisk enhed, kreditor, debitor, medarbejder) post, du vil angive register-ID, og klik derefter på **registrering-id'er** i formularer, der er relateret til part, juridisk enhed, kreditor, debitor, arbejder for at åbne den **Administrer adresser** side. På den **skat registrering**, og klik på **Tilføj**, og Angiv følgende oplysninger om CVR-ID.

|Felt                |Betegnelse                                                |
|---------------------|-----------------------------------------------------------|
| Registreringstype   | Registreringstypen det valgte land/område.     |
| Registreringsnummer | Registrering af part-ID.                                |
| Betegnelse         | Beskrivelse af CVR-nummer.               |
| Sektion             | Yderligere oplysninger om CVR-nummer. |
| Udstedende organ      | Den myndighed, der har udstedt et registreringsnummer.        |
| Udstedelsesdato         | Den dato, der udstedte registreringsnummeret.              |
| Gyldig           | Ikrafttrædelsesdatoen for CVR-nummeret.           |
| Udløb          | Udløbsdatoen for et registreringsnummer.          |

> [!NOTE]
> Moms-nummer for den juridiske enhed, kreditor, debitor kan vælges fra registreringen id'er vedrører moms-ID og angivet for parten.

## <a name="search-for-records-by-registration-id"></a>Søge efter poster af registrerings-ID
Søg efter partposter, der er baseret på et registrerings-ID er tilgængeligt på formularer, der er relateret til part, juridisk enhed, kreditor, debitor og arbejder. Klik på **registrerings-ID Søg** at åbne den **søgekriterier registrerings-ID** side. Angiv søgekriterier, og klik på **finde**. Systemet viser de valgte poster fra det globale adressekartotek og de tilknyttede typer partpost.

## <a name="supported-registration-categories"></a>Understøttede registrering kategorier
Følgende tabel viser de understøttede registrering i Dynamics 365 for operationer. Hvis du er fortrolig med Microsoft Dynamics AX 2012-felter til registrering af id'er, knytter denne tabel også disse felter til Dynamics-365 for operationer registrering kategorier.

| Dynamics 365 for registrering af operationer kategori         |Land/område  | Dynamics AX 2012 betegnelse/felt|
|---------------------------------------------------------------|---------------------|---------------------------------|
| Moms-id                                                        | Alle lande i den Europæiske Union (EU)|  Se-nummer (lovgivningsmæssige type SKATTE-ID i AX 2012 R3)|
| Virksomheds-id (COID)                                          | Belgien, Tjekkiet Estland Ungarn Letland Litauen Polen Schweiz | Enterprise-nummer (EnterpriseNumber) registreringsnummer (RegNum\_W) registreringsnummer (RegNum\_W) registreringsnummer (RegNum\_W) registreringsnummer (RegNum\_W) registreringsnummer for Enterprise-kode (EnterpriseCode) (RegNum\_W) UID (lovgivningsmæssige type UID i AX 2012 R3) |
| Afdelings-id                                                     | Belgien            | Afdelingsnummer (BranchNumber)|
| Spisová značka (registreringsnummer udstedt af agenturet, afsnit) | Tjekkiet     | Cellejustering tal (CommercialRegisterInsetNumber) Kept på kommercielle registrere (CommercialRegister)-sektion i handelsregister (CommercialRegisterSection)|
| Toldmyndighedens debitor-id                                           | Finland | Toldmyndighederne kundenummer (CustomsCustomerNumber\_FI)|
| INN                                                           | Den Russiske Føderation| INN (lovgivningsmæssige type INN i AX 2012 R3)|
| RRC                                                           | Den Russiske Føderation| RRC (lovgivningsmæssige type RRC i AX 2012 R3)|
| OKDP                                                          | Den Russiske Føderation| OKDP (lovgivningsmæssige type OKDP i AX 2012 R3)|
| OKPO                                                          | Den Russiske Føderation| OKPO (lovgivningsmæssige type OKPO i AX 2012 R3)|
| RCOAD                                                         | Den Russiske Føderation| RCOAD (lovgivningsmæssige type RCOAD i AX 2012 R3)|
| OGRN                                                          | Den Russiske Føderation| OGRN (lovgivningsmæssige type OGRN i AX 2012 R3) |
| SNILS                                                         | Den Russiske Føderation| SNILS (lovgivningsmæssige type SNILS i AX 2012 R3)|
| CIFTS                                                         | Den Russiske Føderation| CIFTS (lovgivningsmæssige type CIFTS i AX 2012 R3)|

Se følgende opgave optagelserne moms-ID i livscyklus Services (LCS) for yderligere oplysninger om registrering id'er behandling, herunder nødvendige forudsætninger:

-   Opsætning af moms-id
-   MOMS-id-registrering af kreditor
-    Parts søgning ved hjælp af moms-id



