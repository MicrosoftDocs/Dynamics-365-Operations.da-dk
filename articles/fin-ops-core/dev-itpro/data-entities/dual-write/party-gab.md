---
title: Part og globalt adressekartotek
description: I dette emne beskrives funktionen til part og globalt adressekartotek for dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 2e0d16b29a71da23acc925c09c87f0bb4776759c
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407759"
---
# <a name="party-and-global-address-book"></a>Part og globalt adressekartotek

[!include [banner](../../includes/banner.md)]



*Part* og *globalt adressekartotek* er begreber i programmer til finans og drift. En part kan være en organisation eller en person. Det er en god ide at gemme og administrere egenskaberne for en part globalt, f.eks. navn, sprog, kontakter og adresser. Når en egenskabsværdi ændres ét sted, afspejles ændringen derefter alle de steder, hvor parten er involveret.

## <a name="party"></a>Part

En part er en person eller organisation, der er involveret i en virksomhed. Når der anvendes en part som begreb, kan en person eller organisation spille mere end én rolle i en virksomhed (f.eks. arbejder, kunde, leverandør eller kontakt). Rollen er baseret på sammenhæng og formål. Her er nogle eksempler på roller fra to fiktive virksomheder, Contoso og Fabrikam:

+ **Arbejder** – En medarbejder. Et eksempel er en medarbejder hos Contoso.
+ **Leverandør** – En leverandørorganisation eller en enkeltmandsvirksomhed, der leverer varer eller tjenester til en virksomhed. Hvis Fabrikam f.eks. sælger varer til Contoso, er Fabrikam leverandør til Contoso.
+ **Kontakt** – En person, der kan kontaktes. Hvis Contoso f.eks. køber varer fra Fabrikam, kontakter medarbejdere hos Contoso kontakten hos Fabrikam.
+ **Kunde** – En kunde er en person eller virksomhed, der køber ting fra en anden virksomhed. Hvis Contoso f.eks. køber varer fra Fabrikam, er Contoso kunde hos Fabrikam.

Partmodellen bruges ofte til at repræsentere mellemstore til komplekse relationer mellem organisationer og personer, især når en part spiller mere end én rolle. Her er nogle almindelige eksempler:

+ En part kan både være kunde og leverandør. I Nordamerika sælger Fabrikam f.eks. elledninger til Contoso og køber samlede højttalere hos Contoso. I Europa sælger Fabrikam reservedele til Contoso, men køber ikke noget hos Contoso.
+ En part kan både være medarbejder og kunde. En medarbejder hos Contoso køber f.eks. elektronik fra Contoso til personlig brug.
+ Der kan være en mange til mange-relation (N:N) mellem en person og en organisation. Fabrikam leverer f.eks. serviceteknikere og ansætter en placeringskoordinator. Placeringskoordinatoren svarer til serviceteknikere, der håndterer anmodninger fra flere af Fabrikams kunder. Contoso er en af Fabrikams kunder. Når Contoso skal bruge en servicespecialist, kontakter virksomheden placeringskoordinatoren, som derefter håndterer anmodningen. Da placeringskoordinatoren håndterer anmodninger for alle kunder, er der tale om et N:N-forhold.

Følgende illustration viser datamodellen for partsmodellen:

![Datamodel for part.](media/party-gab-image1.png)

> [!TIP]
> Når du forsøger at oprette en ny kontopost, skal du bruge feltet **Part** til at søge efter posten ved hjælp af navnet. Hvis du finder posten, behøver du således kun vælge posten. Derefter udfylder systemet automatisk alle data fra parten. Du behøver ikke at angive alle krævede felter manuelt. Denne funktion er standard på siderne **Konto**, **Kontakt** og **Leverandør**.

Dobbeltskrivning understøtter ikke alle partroller i programmer til finans og drift. Du kan få vist en komplet liste over partroller i [Oversigten over globalt adressekartotek](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globalt adressekartotek

Det globale adressekartotek er et bibliotek med postadresser og elektroniske adresser på de organisationer og personer, der af del af en virksomhed.

Det globale adressekartotek kan gemme og håndtere alle de postadresser og elektroniske adresser, der er behov for. Fabrikam kan f.eks. have benzintanke på 50 steder. Alle steder har forskellige postadresser, mailadresser og telefonnumre. Alle køb fra virksomheden faktureres til den primære benzintank, men leveres direkte til den benzintank, der har anmodet om købet. Det globale adressekartotek gemmer hovedbenzintanken som faktureringsadresse for Fabrikam og gemmer hver enkelt benzintanks leveringsadresse. Adresserne kan gemmes på én gang og derefter hentes, når de kræves i forbindelse med tilbud og ordrer.

Afhængigt af konteksten kan en person eller organisation have mere end én rolle, og den samme postadresse og elektroniske adresse kan bruges til alle roller i virksomheden. I dette tilfælde skal en adresseændring for den ene rolle vises for alle de andre roller. Det globale adressekartotek gemmer og håndterer adresser globalt.

I følgende illustration vises datamodellen for det globale adressekartotek.

![Datamodel for det globale adressekartotek.](media/party-gab-image2.png)

## <a name="contact"></a>Kontaktperson

I kundeengagementsapps er en kontakt en person. Men tabellen **Kontakt** er dog blevet overfyldt med oplysninger om en person, en portalbruger, en B2C-kunde eller en leverandør. Repræsentationen er implicit, og du kan ikke se forskel uden at undersøge de relaterede transaktioner. Tabellen **Kontakt** er begrænset til at have en 1:1-relation til tabellen **Konto**. Som en del af modellen for part og globalt adressekartotek introducerer dobbeltskrivning eksplicitte egenskaber til klassifikation, og muliggør N:N-relationer mellem en kontakt, der er en person eller en organisation (enhed af typen **Konto** eller **Leverandør**).

Der findes to typer **Kontakt**-rækker:

+ **Stribet kontakt** – En række af typen **Kontakt**, hvor feltet **Virksomhed** har en obligatorisk værdi.
+ **Ikke-stribet kontakt** – En række af typen **Kontakt**, hvor feltet **Virksomhed** er tomt.

I tabellen **Kontakt** kan du gemme følgende typer rækker.

| Rækketype | Betegnelse |
|----------|-------------|
| En person, der er en kunde (f.eks. en salgbar kontakt eller B2C-kunde) | En stribet kontaktpost, hvor feltet **Virksomhed** ikke er tomt, og feltet **Er kunde** er angivet til **Ja**. |
| En person, der er leverandør (f.eks. en enkeltmandsvirksomhed, der er leverandør) | En stribet kontaktpost, hvor feltet **Virksomhed** ikke er tomt, og feltet **Er leverandør** er angivet til **Ja**. |
| En person, der både er kunde og leverandør | En stribet kontaktpost, hvor feltet **Virksomhed** ikke er tomt, feltet **Er kunde** er angivet til **Ja**, og feltet **Er leverandør** er angivet til **Ja**. En person kan både være producent af ét produkt og en forbruger af et andet produkt. Både programmer til finans og drift og dobbeltskrivning understøtter denne relation. |
| En person, der er kontaktperson for en organisation, men ikke er kunde eller leverandør | En ikke-stribet kontaktpost, hvor feltet **Virksomhed** er tomt, feltet **Er kunde** er angivet til **Nej**, og feltet **Er leverandør** er angivet til **Nej**. |

## <a name="contact-for-party-table"></a>Tabellen Kontakt for part

Tabellen **Kontakt for part** gemmer og håndterer N:N-relationer mellem rækker af typen **Konto** og **Kontakt**. Den kan filtrere stribede rækker af typen **Kontakt** fra ikke-stribede rækker og kun knytte de ikke-stribede rækker af typen **Kontakt** til rækker for **Konto** eller **Leverandør**.

Natasha Jones og Miguel Reyes er f.eks. dyrlæger, som arbejder for farme i deres lokalområder. Natasha betjener Seattle-området, og Miguel betjener Kent-området. I kundeengagementsappen er bondegårde angivet som kunder, og dyrlægerne er angivet som kontaktpersoner. En enkelt **Kontakt**-post for Natasha er tilknyttet alle de farme, som Natasha arbejder med. På samme måde er en enkelt post for **Kontakt** for Miguel tilknyttet alle de bondegårde, som Miguel arbejder med.

Disse relationer gemmes i tabellen **Kontakt for part**. Du kan finde oplysninger om standardsiderne for **Konto**, **Kontakt** og **Leverandør**:

+ På siden **Konto** kan du bruge fanen **Tilknyttede kontakter** til at knytte en eller flere kontakter til rækken **Konto**. På denne måde kan du tildele kontaktpersoner til en organisation. Derefter kan du vælge én kontakt som primær kontakt for kontoen. Hvis du bruger siden **Hurtig oprettelse**, kan du kun vælge en kontaktperson. Denne funktion er på samme måde, når du bruger siden **Leverandør**, og posttypen er **Organisation**.
+ Når rækken er en debitor, en kreditor eller begge (en stribet kontaktperson), kan du bruge fanen **Tilknyttede kontakter** til at tilknytte en eller flere kontakter på siden **Kontakt**. På denne måde kan du tildele kontaktpersoner til en B2C-kunde eller -leverandør. Derefter kan du vælge én kontakt som primær kontakt. Hvis du bruger siden **Hurtig oprettelse**, kan du kun vælge en kontaktperson.
+ Når rækken er en kontaktperson (en ikke-stribet kontaktperson), kan du bruge fanen **Tilknyttede organisationer** til at tilknytte en eller flere kunder eller leverandører på siden **Kontakt**. På denne måde kan du tildele kunder eller leverandører til den underliggende kontaktperson. Kunden eller leverandøren kan være en organisation, en person eller begge dele. Du kan kun vælge én værdi blandt de fire felter ad gangen:

    + Hvis du vælger en værdi i feltet **Part-id**, tildeles den underliggende kontakt alle rollerne for den valgte part.
    + Hvis du vælger en værdi i feltet **Tilknyttet kontakt**, vælger du den stribede kontakt af typen **Person**.
    + Hvis du vælger en værdi i feltet **Tilknyttet konto** eller **Tilknyttet kreditor**, vælger du en organisation.

    ![Fanen Tilknyttede organisationer på siden Kontakt.](media/party-gab-image3.png)

    Uanset dit valg oprettes tilknytningen på partniveau gælder for alle partens roller og gemmes i enheden **Kontakt for part**.

> [!NOTE]
> Det viste navn på tabellen **Kontakt for part** i kundeengagementsapps er **Kontakt for kunde/leverandør**.

Når du åbner en række af typen **Kontakt**, hvor både feltet **Er kunde** og **Er leverandør** er angivet til **Nej**, vises fanen **Tilknyttede organisationer**. Du kan bruge denne fane til at knytte en eller flere debitor- eller kreditororganisationer til kontakten.

Når du åbner en række af typen **Kontakt**, hvor enten feltet **Er kunde** eller **Er leverandør** er angivet til **Ja**, vises fanen **Tilknyttede kontakter**. Du kan bruge denne fane til at knytte en eller flere kontakter.

## <a name="postal-addresses"></a>Postadresser

Der er indført en ny fane med navnet **Adresser** på siderne **Konto**, **Kontakt** og **Leverandør**. Denne fane understøtter flere postadresser ved hjælp af et gitter som vist i følgende illustration.

![Gitter for postadresser.](media/party-gab-image4.png)

Gitteret indeholder følgende kolonner:

+ **Postadresseroller** – Formålet med postadressen.
+ **Er primær** – En værdi, der angiver, om adressen er den primære adresse.
+ **Adressenummer** – Nummer i rækken af adresser.

Du kan bruge knappen **Ny adresse** over gitteret til at oprette så mange postadresser, du vil.

Felterne **Adresse 1** og **Adresse 2** under fanen **Oversigt** på siden **Konto** svarer adresser for henholdsvis **Levering** og **Faktura**.

![Fanen Oversigt for postadresser.](media/party-gab-image5.png)

Felterne **Adresse 1**, **Adresse 2** og **Adresse 3** under fanen **Oversigt** på siden **Kontakt** svarer henholdsvis til adresserne for **Virksomhed**, **Levering** og **Faktura**.

## <a name="electronic-addresses"></a>Elektroniske adresser

Der er indført en ny fane med navnet **Elektroniske adresser** på siderne **Konto**, **Kontakt** og **Leverandør**. Denne fane understøtter flere elektroniske adresser ved hjælp af et gitter som vist i følgende illustration.

![Gitter for elektroniske adresser.](media/party-gab-image6.png)

Gitteret indeholder følgende kolonner:

+ **Type** – Typen af elektronisk adresse.
+ **Er primær** – En værdi, der angiver, om adressen er den primære adresse.
+ **Formål** – Formålet med den elektroniske adresse.

Du kan bruge knappen **Ny elektronisk adresse** over gitteret til at oprette så mange adresser, du vil.

Elektroniske adresser er kun tilgængelige i dette gitter. I fremtidige versioner fjernes alle felter med postadresser og elektroniske adresser fra andre faner, f.eks. fanerne **Oversigt** og **Detaljer**. De kontaktoplysninger, der vises under fanen **Detaljer**, er skrivebeskyttede kopier af den primære elektroniske adresse, f.eks. primær telefon, primær email, primær telefon, primær fax og primært Twitter-id. Under kvalificeringsprocessen for potentielle kunder kan du både angive et firmatelefonnummer og et mobiltelefonnummer. Firmatelefonnummeret betragtes som den primære telefon, hvis **IsNøgle=No**, og mobiltelefonnummeret betragtes som den sekundære telefon, hvis **IsMobile=Yes**.

> [!TIP]
> Brug fanerne **Adresser** og **Elektroniske adresser** i formularerne **Konto** og **Kontakt** til at administrere postadresser og elektroniske adresser. Derved sikres det, at adressedata synkroniseres med programmer til finans og drift.

## <a name="setup"></a>Konfiguration

1. Åbn Customer Engagement-appmiljøet.

2. Installer den seneste version af (2.2.2.60 eller senere) af [Orkestreringsløsning til dobbeltskrivningsapplikation](https://aka.ms/dual-write-app).

3. Installer [Løsninger til dobbeltskrivningspart og globalt adressekartotek](https://aka.ms/dual-write-gab).

4. Åbn Finans og drift-appen. Gå til modulet Dataadministration, og vælg fanen Dobbeltskrivning. Siden med administration af dobbeltskrivning åbnes.

5. Anvend begge løsninger, der er installeret i trin 2 og 3, ved hjælp af funktionen [Anvend løsning](link-your-environment.md).

6. Stop følgende tilknytninger, da de ikke kræves længere. Kør i stedet `Contacts V2 (msdyn_contactforparties)`-tilknytningen.

    + CDS Kontakter V2 og kontakter (refererer til kundekontakter)
    + CDS Kontakter V2 og kontakter (refererer til leverandørkontakter)

7. Følgende enhedstilknytninger opdateres for partfunktioner, så den seneste version skal anvendes på disse tilknytninger.

    Map | Opdater til denne version | Ændringer
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.5 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Customers V3 (accounts)` | 1.0.0.5 |Fjernede `PartyNumber` og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadresse og elektroniske kontaktadresser.
    `Customer V3 (contacts)` | 1.0.0.5 | Fjernede `PartyNumber` og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadresse og elektroniske kontaktadresser.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | Fjernede `PartyNumber` og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadresse og elektroniske kontaktadresser.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | Erstattede kontaktpersonen med reference til `ContactforParty`.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | Erstattede kontaktpersonen med reference til `ContactforParty`.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | Erstattede kontaktpersonen med reference til `ContactforParty`.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.1 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Complimentary Closings ( msdyn_compliemntaryclosings)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Dette er en ny tilknytning., der er tilføjet som del af denne version.

8. Før du kører ovenstående tilknytninger, skal du opdatere integrationsnøglerne manuelt som beskrevet i følgende trin. Vælg derefter **Gem**.

    | Map | Nøgler |
    |-----|------|
    | Konto |  accountnumber [Kontonummer]<br>msdyn_company.cdm_companycode [Virksomhed (Virksomhedskode)] |
    | Kontaktperson | msdyn_contactpersonid [Kontonummer/Kontaktperson-id]<br>msdyn_company.cdm_companycode [Virksomhed (Virksomhedskode)] |
    | Kontakt for debitor/kreditor | msdyn_contactforpartynumber [Kontakt for partnummer]<br>msdyn_associatedcompanyid.cdm_companycode [Tilknyttet virksomhed (Virksomhedskode)] |
    | Leverandør | msdyn_vendoraccountnumber [Kreditors kontonummer]<br>msdyn_company.cdm_companycode [Virksomhed (Virksomhedskode)]|

9. I Dataverse er tegngrænsen i reglerne for detektion af dubletter øget fra 450 til 700 tegn. Med denne grænse kan du føje en eller flere nøgler til reglerne for detektion af dubletter. Udvid reglen for detektion af dubletter for tabellen **Konti** ved at angive følgende felter.

    | Felt | Værdi |
    |-------|-------|
    | Navn | Konti med samme kontonavn. |
    | Betegnelse | Detekterer kontoposter med samme værdi i attributten Kontonavn. |
    | Basisposttype | Konto |
    | Tilsvarende posttype | Konto |
    | Kontonavn (felt) | Nøjagtigt match |
    | Virksomhed (felt) | Nøjagtigt match |
    | Relationstype (felt) | Nøjagtigt match |
    | Part-id (felt) | Nøjagtigt match |
    | Vælg (felt) | (tom) |

    ![Dubletregel for konti.](media/duplicate-rule-1.PNG)

10. Udvid reglen for detektion af dubletter for tabellen **Kontakter** ved at angive følgende felter.

    | Felt | Værdi |
    |-------|-------|
    | Navn | Kontaktpersoner med samme fornavn og efternavn. |
    | Betegnelse | Registrerer kontaktposter med samme værdier i felterne Fornavn og Efternavn. |
    | Basisposttype | Kontaktperson |
    | Tilsvarende posttype | Kontaktperson |
    | Fornavn (felt) | Nøjagtigt match |
    | Efternavn (felt) | Nøjagtigt match |
    | Virksomhed (felt) | Nøjagtigt match |
    | Part-id (felt) | Nøjagtigt match |
    | Vælg (felt) | (tom) |

    ![Dubletregel for kontakter.](media/duplicate-rule-2.PNG)

11. Hvis du er en eksisterende bruger af dobbeltskrivning, skal du følge instruktionerne i [Opgrader til model for part og globalt adressekartotek](upgrade-party-gab.md) og opgradere dine data. **Fortsæt ikke til trin 12 uden at fuldføre dette trin.** Hvis du er ny bruger af dobbeltskrivning, skal du gå til trin 12.

12. Hvis du er en eksisterende bruger af dobbeltskrivning, skal du fuldføre trin 11, og derefter kan du køre tilknytningerne i følgende rækkefølge. Hvis du er en ny kunde med dobbeltskrivning, kan du fortsætte direkte. Hvis du får vist en fejlmeddelelse om, at "Projektvalidering mislykkedes. Manglende destinationsfelt...", skal du åbne tilknytningen og vælge **Opdater tabeller** og derefter køre tilknytningen.

    Program til finans og drift | Customer Engagement-app  
    ----------------------------|------------------------
    [CDS-parter](mapping-reference.md#220) | msdyn_parties
    [Lokaliteter for CDS-postadresse](mapping-reference.md#234) | msdyn_postaladdresscollections
    [Oversigt over CDS-postadresse V2](mapping-reference.md#235) | msdyn_postaladdresses
    [Lokaliteter for CDS-parts postadresse](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Partkontakter V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Debitorer V3](mapping-reference.md#101) | konti
    [Debitorer V3](mapping-reference.md#116) | kontakter
    [Kreditorer V2](mapping-reference.md#202) | msdyn_vendors
    [Titler på kontaktpersoner](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Afsluttende hilsner](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Tiltaleformer](mapping-reference.md#228) | msdyn_salutations
    [Beslutningstagerrolle](mapping-reference.md#224) | msdyn_decisionmakingroles
    [Ansættelsesjobfunktioner](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Loyalitetsniveauer](mapping-reference.md#226) | msdyn_loyaltylevels
    [Personlige tegntyper](mapping-reference.md#227) | msdyn_personalcharactertypes
    [Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS-salgstilbudshoved](mapping-reference.md#215) | pristilbud
    [CDS-salgsordrehoveder](mapping-reference.md#217) | salesorders
    [Salgsfakturahoveder V2](mapping-reference.md#118) | fakturaer

> [!NOTE]
> Tilknytningen `CDS Contacts V2 (contacts)` er den tilknytning, du standsede i trin 1. Når du forsøger at køre andre tilknytninger, vises disse to tilknytninger muligvis på listen over afhængige. Du skal ikke køre disse tilknytninger.
>
> Hvis løsningen for part og globalt adressekartotek er installeret, skal du deaktivere plug-in med navnet `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead`. Hvis du fjerner løsningen for part og globalt adressekartotek, skal du genaktivere plug-in.
>
> Feltet `msdyn_*partynumber` (et enkelt linjetekstfelt), der er inkluderet i tabellerne **Konto**, **Kontakt** og **Leverandør**, bør ikke bruges fremover. Etiketnavnet har præfikset **(Frarådet)** for at specificere det. Brug i stedet feltet **msdyn_partyid**. Feltet er et opslag i tabellen **msdyn_party**.

> Tabelnavn | Gammelt felt | Nyt felt
> --------|-------|--------
> Konto | `msdyn_partynumber` | `msdyn_partyid`
> Kontaktperson | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Skabeloner

En samling af tabeltilknytninger arbejder sammen under interaktion med part og globalt adressekartotek, som vist i følgende tabel.

| Program til finans og drift | Customer Engagement-app | Beskrivelse |
|----------------------------|-------------------------|-------------|
| [Titler på kontaktpersoner](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Debitorer V3](mapping-reference.md#101) | konti |
| [Debitorer V3](mapping-reference.md#116) | kontakter |
| [CDS-parter](mapping-reference.md#220) | msdyn\_parties |
| [Lokaliteter for CDS-parts postadresse](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [Oversigt over CDS-postadresse V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [Lokaliteter for CDS-postadresse](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS-salgstilbudshoved](mapping-reference.md#215) | pristilbud |
| [CDS-salgsordrehoveder](mapping-reference.md#217) | salesorders |
| [Afsluttende hilsner](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [Kontakter V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Beslutningstagerrolle](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [Ansættelsesjobfunktioner](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Loyalitetsniveauer](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Partkontakter V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Personlige tegntyper](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Salgsfakturahoveder V2](mapping-reference.md#118) | fakturaer |
| [Tiltaleformer](mapping-reference.md#228) | msdyn\_salutations |
| [Kreditorer V2](mapping-reference.md#202) | msdyn\_vendors |

Du kan finde flere oplysninger i [referencen til tilknytning af dobbeltskrivning](mapping-reference.md).

## <a name="known-issues-and-limitations"></a>Kendte problemer og begrænsninger

+ Når du opretter en kunde sammen med adressen og gemmer den, synkroniseres adressen muligvis ikke med tabellen **Adresse** i programmer til finans og drift. Det skyldes et problem med rækkefølge på platformen for dobbeltskrivning. En løsning er først at oprette kunden og derefter gemme. Tilføj derefter adressen.
+ Når en kundepost har en primær adresse i et apps, og du opretter en ny kontakt for den pågældende kunde, arver kontaktposten en primær adresse fra den tilknyttede kundepost i programmer til finans og drift. Det sker også for leverandørkontakten. Dataverse understøtter ikke denne funktionsmåde i øjeblikket. Hvis dobbeltskrivning er aktiveret, synkroniseres en kundes kontakter, der er nedarvet med en primær adresse fra programmet til finans og drift, med Dataverse sammen med adressen.
+ Elektroniske adresser, der er angivet under fanen for elektroniske adresser i formularerne **Konto**, **Kontakt** og **Leverandør** kommer fra tabellen `msdyn_partyelectronicaddress`. Disse oplysninger føres ikke til tilknyttede transaktioner som f.eks. salgsordre, tilbud og indkøbsordre. Vi planlægger at løse dette problem trinvist i næste versioner. De eksisterende data i de elektroniske adressefelter på kontoen og kontaktposterne vil fortsat fungere for transaktioner som f.eks. salgsordre, tilbud og indkøbsordre.
+ I programmer til finans og drift kan du oprette en kontaktpost fra formularen **Tilføj kontakt**. Når du forsøger at oprette en ny kontakt fra formularen **Vis kontakt**, mislykkes handlingen. Dette er et kendt problem.

    ![Kendt problem med Tilføj kontakt.](media/party-gab-contact-issue.png)

+ **Første synkronisering** understøtter ikke tidsfelterne **Tilgængelig fra** og **Tilgængelig til** i **ContactForParty**, da DIXF konverterer værdien til en streng i stedet for et heltal. Konverteringen udløser fejlen `Cannot convert the literal '<say 08:00:00>’ to the expected type edm.int32`.
+ Når en postadresse bruges af mere end én årsag, f.eks. adresse til virksomheds kommunikation og fakturering, skal den vises som `Business;Invoice` som vist på følgende billede. Hvis du tilføjer et mellemrum mellem værdierne, vises en fejl.

    ![Kendt problem med adresse.](media/party-gab-address-issue.png)

+ Du kan ikke angive en fremdateret postadresse ved hjælp af et program til finans og drift med dobbeltskrivning, da Dataverse ikke understøtter datogyldighed. Hvis du angiver en fremdateret postadresse ved hjælp af et program til finans og drift, synkroniseres den fuldstændigt med Dataverse, og du vil straks kunne se adressen på brugergrænsefladen. Opdateringer af denne post resulterer i en fejl, da posten er fremdateret og ikke aktuel i programmer til finans og drift.
