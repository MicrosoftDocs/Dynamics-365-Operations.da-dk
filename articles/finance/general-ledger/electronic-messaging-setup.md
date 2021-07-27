---
title: Konfigurere elektroniske meddelelser
description: Dette emne indeholder en oversigt og oplysninger om opsætning for elektroniske meddelelser (EM).
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 947170d1db132ca5a6b7caed0e47ee814b9148cc
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433770"
---
# <a name="set-up-electronic-messages"></a>Konfigurere elektroniske meddelelser

[!include [banner](../includes/banner.md)]

**Elektroniske meddelelser** kan hjælpe dig med at vedligeholde forskellige elektroniske rapporteringsprocesser for forskellige dokumenttyper. Elektroniske meddelelser der understøtter [landespecifikke rapporteringsfunktioner](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality), er i visse komplekse scenarier konfigureret på en sådan måde, at de indeholder en kombination af mange meddelelsesstatusser, statusser for meddelelseselementer, handlinger, ekstra felter og udførelsesklasser. Der findes pakker med dataenheder til import i disse scenarier. Hvis du bruger disse dataenhedspakker, skal du importere dem til en juridisk enhed ved hjælp af datastyringsværktøjet. Du kan finde flere oplysninger om, hvordan du bruger af datastyringsværktøjet, i [Datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Hvis du ikke importerer en dataenhedspakke, kan du manuelt konfigurere EM-funktionaliteten. I dette tilfælde skal du definere følgende elementer:

- [Nummerserier](#sequences)
- [Typer af meddelelseselement](#types)
- [Statusser for meddelelseselement](#item)
- [Meddelelsesstatusser](#statuses)
- [Ekstra felter](#additional)
- [Indstillinger for eksekverbar klasse](#executable)
- [Handlingerne Udfyld poster](#populate)
- [Webapplikationer](#applications)
- [Indstillinger for webtjeneste](#settings)
- [Handlinger ved meddelelsesbehandling](#actions)
- [Behandling af elektronisk meddelelse](#processing)

Nedenstående afsnit indeholder flere oplysninger om hvert af disse elementer.

## <a name="number-sequences"></a><a id="sequences"></a>Nummerserier

Konfigurer nummerserier for både meddelelser og meddelelseselementer. Nummerserierne anvendes til at generere numre for meddelelser og meddelelseselementer automatisk. De tildelte numre anvendes som unikke identifikatorer for meddelelserne og meddelelseselementerne i systemet. Du kan oprette nummerserier til elektroniske meddelelser på siden **Finans** \> **Finansopsætning** \> **Generelle Finansparametre**.

## <a name="message-item-types"></a><a id="types"></a>Typer af meddelelseselement

Meddelelseselementtyper identificerer typerne af poster, der skal bruges i elektroniske meddelelser. Du kan konfigurere meddelelseselementtyper ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelseselementtyper**.

## <a name="message-item-statuses"></a><a id="item"></a>Statusser for meddelelseselement

Meddelelseselementstatusser identificere de statusser, der gælder for meddelelseselementer i behandlingen, som du konfigurerer. Du kan konfigurere meddelelseselementtyper ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelseselementstatusser**.

Parametret **Tillad sletning** for et meddelelseselements status definerer, om du kan slette meddelelseselementer, som har denne status, på siden **Elektroniske meddelelser** eller siden **Elektronisk meddelelseselementer**.

## <a name="message-statuses"></a><a id="statuses"></a>Meddelelsesstatusser

Konfigurer de meddelelsesstatusser, der skal være tilgængelige i behandling af meddelelser. Du kan konfigurere meddelelseselementtyper ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelseselementstatusser**.

I følgende tabel beskrives felterne på siden **Meddelelsesstatusser**.

| Feltnavn          | Beskrivelse |
|---------------------|-------------|
| Meddelelsesstatus      | Indtast et unikt navn for meddelelsens status. Meddelelsesstatusser anvendes til at karakterisere en elektronisk meddelelses tilstand på ethvert tidspunkt. Det indtastede navn fremgår af siden **Elektroniske meddelelser** og en log, der er tilknyttet elektroniske meddelelser. |
| Beskrivelse         | Indtast en beskrivelse af meddelelsens status. |
| Svartype       | Vælg svartypen for meddelelsens status. Visse handlinger i en behandling kan producere mere end én svartype. Eksempelvis kan handlinger af typen **Webtjeneste** producere svartyper i form af enten **Udført korrekt** eller **Teknisk fejl** afhængigt af resultatet af kørslen. I dette tilfælde skal meddelelsesstatus for begge svartyper være defineret. Du kan finde flere oplysninger om handlingstyper og de svartyper, der er forbundet hermed, under [Handlingstyper for behandling af meddelelser](#action-types) senere i dette emne. |
| Status for meddelelseselement | Til tider skal statussen for en elektronisk meddelelse påvirke statussen for tilknyttede meddelelseselementer. Vælg i dette felt en status for et meddelelseselement for at knytte den til meddelelsens status. |
| Tillad sletning        | Marker dette afkrydsningsfelt, hvis brugerne skal kunne slette elektroniske meddelelser med denne status på siden **Elektroniske meddelelser**. |

## <a name="additional-fields"></a><a id="additional"></a>Ekstra felter

Funktionen EM giver dig mulighed for at indsamle poster fra transaktionstabeller i Microsoft Dynamics 365 Finance som meddelelsesvarer. På denne måde kan du opstille posterne til rapportering og derefter rapportere dem. I visse tilfælde er der dog ikke tilstrækkelige oplysninger i transaktionstabellerne til at kunne udfylde posterne i overensstemmelse med rapporteringskravene. Du kan oprette ekstra felter med henblik på at angive alle de oplysninger, der skal rapporteres for en post. Der kan knyttes flere felter til både meddelelser og meddelelser. Du kan konfigurere yderligere felter ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Yderligere felter**.

I følgende tabel beskrives de generelle felter på siden **Ekstra felter**.

| Felt       | Betegnelse |
|-------------|-------------|
| Feltnavn  | Angiv navnet på et ekstra felt til elektroniske meddelelser eller meddelelseselementer, der vedrører processen. Dette navn vises i brugergrænsefladen (UI), mens du arbejder med processen. Navnet kan også bruges i ER-konfigurationer, der er knyttet til processen. |
| Betegnelse | Indtast en beskrivelse af det ekstra felt. |
| Brugerredigering   | Angiv denne indstilling til **Ja**, hvis brugerne skal kunne ændre værdien for det ekstra felt fra brugergrænsefladen. |
| Tæller     | Angiv denne indstilling til **Ja**, hvis det ekstra felt skal indeholde en nummerserie i en elektronisk meddelelse. Værdien i det ekstra felt udfyldes automatisk, når der køres en handling i form af **Eksport af elektronisk rapportering**. |
| Skjulte      | Angiv denne indstilling til **Ja**, hvis det ekstra felt skal skjules i brugergrænsefladen på siden **Elektroniske meddelelser** eller siden **Elementer for elektronisk meddelelse**. |

I oversigtspanelet **Værdier** kan du foruddefinere de værdier, som et ekstra felt kan have. Disse værdier kan derefter vælges af brugerne. Derfor behøver de ikke at blive udfyldt manuelt under behandlingen. I følgende tabel beskrives felterne.

| Felt                | Betegnelse |
|----------------------|-------------|
| Feltværdi          | Indtast den feltværdi, der skal anvendes for en meddelelse eller et meddelelseselement under rapportering. |
| Beskrivelse          | Indtast en beskrivelse af feltværdien. |
| Kontotype         | Visse feltværdier kan være begrænset til bestemte kontotyper. Vælg en eller flere af følgende værdier: **Alle**, **Debitor** eller **Kreditor**. |
| Kontokode         | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, kan du yderligere begrænse brugen af feltværdien til en bestemt gruppe eller tabel. |
| Konto/gruppenummer | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, og hvis du har angivet en gruppe eller en tabel i feltet **Kontokode**, kan du angive en bestemt gruppe eller modpostering i dette felt. |
| Gyldig            | Angiv den dato, hvor værdien skal begynde at blive taget i betragtning. |
| Udløb           | Angiv den dato, hvor værdien ikke længere skal tages i betragtning. |

Kombinationer af de kriterier, der er defineret i felterne **Konto/gruppenummer**, **Kontokode**, **Gyldig** og **Udløb**, påvirker som standard ikke valget af værdier for de ekstra felter. Disse kombinationer kan dog anvendes i en udførelsesklasse til at implementere specifikke regler, som beregner værdierne for de ekstra felter.

## <a name="executable-class-settings"></a><a id="executable"></a>Indstillinger for eksekverbar klasse

En eksekverbar klasse er en X ++-metode eller en klasse, som den elektroniske meddelelsesbehandling kan kalde i forhold til en handling, hvis en form for vurdering er påkrævet for processen.

Du kan manuelt oprette en eksekverbar klasse, der skal kaldes under behandlingen, ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Indstillinger for elektronisk opsætning**. Opret en linje på siden **Indstillinger for eksekverbar klasse**, og angiv følgende felter.

| Felt                 | Betegnelse |
|-----------------------|-------------|
| Eksekverbar klasse      | Skriv det navn, der skal bruges under konfigurationen af en meddelelsesbehandling, som denne klasse kaldes i forhold til. |
| Betegnelse           | Angiv en beskrivelse af den eksekverbare klasse. |
| Navn på eksekverbar klasse | Vælg en X ++ eksekverbar klasse. |
| Udførelsesniveau       | Dette felt angives automatisk, fordi værdien er foruddefineret for den valgte eksekverbare klasse. Dette felt begrænser det niveau, som den relaterede evaluering kører på. |
| Beskrivelse af klasse     | Dette felt angives automatisk, fordi værdien er foruddefineret for den valgte eksekverbare klasse. |
| Handlingstype           | Dette felt er tilgængeligt, når funktionen til **\[EM\]-klassehandlingstype** er aktiveret i arbejdsområdet til **funktionsstyring**. Brug dette felt til at angive handlingstypen for den eksekverbare klasse. Dette felt giver mere præcis kontrol over de næste handlinger, der er tilgængelige for den elektroniske meddelelse på siden **Elektroniske meddelelser**. |

Visse udførelsesklasser kan have obligatoriske parametre, som skal defineres, før udførelsesklassen køres første gang. Hvis du vil definere disse parametre, skal du vælge **Parametre** i handlingsruden. I dialogboksen skal du indstille felter og derefter vælge **OK**. Det er vigtigt, at du vælger **OK**. I modsat fald bliver parametrene ikke gemt i databasen, og udførelsesklassen bliver ikke kaldt korrekt.

## <a name="populate-records-actions"></a><a id="populate"></a>Handlingerne Udfyld poster

Du bruger handlinger til udfyldelse af poster til at konfigurere handlinger, der tilføjer poster til tabellen Meddelelseselementer, så de kan føjes til en elektronisk meddelelse. Hvis din elektroniske meddelelse eksempelvis skal rapportere debitorfakturaer, skal du konfigurere en handling til at udfylde poster, der er kædet sammen med feltet **Datakilde** i tabellen i debitorfakturajournalen.

Du kan konfigurere handlinger til udfyldelse af poster på siden **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Udfyld poster**.. Opret en ny post for hver handling, der skal føje poster til tabellen, og angiv følgende felter.

| Felt       | Beskrivelse |
|-------------|-------------|
| Navn        | Indtast et navn for den handling, der udfylder posterne i din proces. |
| Beskrivelse | Indtast en beskrivelse af handlingen til at udfylde posterne. |

I oversigtspanelet **Opsætning af datakilder** skal du tilføje en linje for hver datakilde, der bruges til processen, og angive følgende felter.

| Felt                  | Betegnelse |
|------------------------|-------------|
| Navn                   | Angiv et navn til datakilden. |
| Typen af meddelelseselement      | Vælg den type meddelelseselement, der skal bruges, når der oprettes poster til datakilden. |
| Kontotype           | Vælg den type konto, der skal knyttes til poster fra datakilden. |
| Navn på overordnet tabel      | Vælg den tabel, der skal være en datakilde. |
| Feltet dokumentnummer  | Vælg det felt, som dokumentnummeret skal tages fra i den valgte hovedtabel. Værdien i dette felt bruges som værdien i feltet **Dokumentnummer** for meddelelseselementet. |
| Feltet Dokumentdato    | Vælg det felt, som dokumentnummeret skal tages fra i den valgte hovedtabel. Værdien i dette felt bruges som værdien i feltet **Meddelelseselementdato** for meddelelseselementet. |
| Feltet Dokumentkonto | Vælg det felt, som dokumentkontoen skal tages fra i den valgte hovedtabel. Værdien i dette felt bruges som værdien i feltet **Kontonummer** for meddelelseselementet. |
| Virksomhed                | Dette felt er tilgængeligt, når funktionen **Forespørgsler på tværs af virksomheder til udfyldning af handling af poster** er aktiveret i arbejdsområdet til **funktionsstyring**. Du kan bruge denne funktion til at konfigurere datakilder på tværs af regnskaber for aktionerne med popup-poster. Der kan hentes data fra flere regnskaber. |
| Brugerforespørgsel             | <p>Hvis du opretter en forespørgsel ved at vælge **Rediger-forespørgsel** over gitteret, og du angiver de kriterier, der skal anvendes på den valgte mastertabel, som data er udfyldt fra, markeres dette afkrydsningsfelt automatisk. I modsat fald udfyldes alle posterne af den valgte hoveddatakilde.</p><p>Når **Forespørgsler på tværs af firmaer for funktionen til at udfylde poster** er aktiveret i arbejdsområdet til **funktionsstyring**, og poster skal indsamles fra flere firmaer, skal du tilføje en linje for hver ekstra juridisk enhed, der skal medtages i rapporteringen. For hver ny linje skal du vælge **Rediger forespørgsel** og angive et relateret kriterium, der er specifikt for den juridiske enhed, som er angivet i feltet **Firma** på linjen. Når du er færdig, indeholder **opsætningsgitteret for datakilder** linjer for alle de juridiske enheder, der skal inkluderes i rapporteringen.</p> |

## <a name="web-applications"></a><a id="applications"></a>Webapplikationer

Brug webprogramindstillingerne til at konfigurere et webprogram, således at det understøtter Open Authorization (OAuth) 2,0. OAuth er den åbne standard, som gør det muligt for brugerne at tildele "sikker delegeret adgang" til programmet på deres vegne uden at dele deres legitimationsoplysninger. Du kan også komme igennem godkendelsesprocessen ved at få en godkendelseskode og et adgangstoken. Du kan konfigurere indstillinger for webprogrammer ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Webprogrammer**.

I følgende tabel beskrives felterne på siden **Webprogrammer**.

| Felt                        | Beskrivelse |
|------------------------------|-------------|
| Applikationsnavn             | Angiv et navn til webprogrammet. |
| Beskrivelse                  | Angiv en beskrivelse af webprogrammet. |
| URL-basisadresse                     | Angiv basisinternetadressen til webprogrammet. |
| URL-sti til godkendelse       | Angiv den sti, som URL-adressen, der anvendes til godkendelse, består af. |
| URL-sti til token               | Angiv den sti, som URL-adressen, der anvendes til det pågældende token, består af. |
| URL-adresse til omdirigering                 | Angiv URL-adresse til omdirigering. |
| Klient-id                    | Angiv klient-id'et for webprogrammet. |
| Klienthemmelighed                | Angiv klientens hemmelighed for webprogrammet. |
| Servertoken                 | Angiv servertokenet til webprogrammet. |
| Formattilknytning for godkendelse | Vælg det ER-format, der anvendes til at generere anmodningen om godkendelse. |
| Importér tokenmodeltilknytning   | Vælg den ER-importmodeltilknytning, der skal anvendes til at gemme adgangstokenet. |
| Tildelt interval                | Det tildelte anvendelsesområde for anmodninger til programmet. Dette felt opdateres automatisk. |
| Adgangstokenet udløber om  | Den resterende tid før adgangstokenet udløber. Dette felt opdateres automatisk. | 
| Godkend                       | Angiv webanmodningens egenskaber for **Accept**. Indtast eksempelvis **application/vnd.hmrc.1.0+json**. |
| Indholdstype                 | Angiv indholdstypen. Indtast eksempelvis **application/json**. |

Derudover er følgende knapper tilgængelige i handlingsruden på siden **Webprogrammer** med henblik på at understøtte godkendelsesprocessen:

- **Få godkendelseskode** – Påbegynd godkendelse af webprogrammet. Denne funktion bruger det ER-format, der er angivet i feltet **Tilknytning af godkendelsesformat**, til at generere en godkendelsesanmodning.
- **Hent adgangstoken** – Påbegynd processen med at få et adgangstoken.
- **Opdater adgangstoken** – Opdater et adgangstoken. Denne funktion bruger det ER-format, der er angivet i feltet **Tilknytning af importtokenmodel**, til at importere oplysninger om det modtagne adgangstoken.

Når et adgangstoken til et webprogram gemmes i systemets database i krypteret format, kan det anvendes til anmodninger til en webtjeneste. Af sikkerhedsmæssige årsager skal adgangen til adgangstokenet begrænses til de sikkerhedsroller, der skal have tilladelse til at behandle de pågældende anmodninger. Såfremt nogen uden for sikkerhedsgruppen forsøger at behandle en anmodning, modtager de en fejlmeddelelse, som oplyser, at de ikke har tilladelse til at arbejde via det valgte webprogram. For at oprette de sikkerhedsroller, der skal have adgang til et adgangstoken, skal du anvende **Sikkerhedsroller** i oversigtspanelet på siden **Webprogrammer**. Såfremt sikkerhedsrollerne ikke defineres for et webprogram, er det kun muligt for en systemadministrator at arbejde via dette webprogram.

For hver handling med det valgte webprogram gemmer oversigtspanelet **Handlingslog** oplysninger om brugeren samt datoen og tidspunktet.

Visse webtjenester kan kræve, at der medtages forskellige overskrifter i anmodningerne. Systemadministratoren kan konfigurere yderligere overskrifter og deres værdier i oversigtspanelet **Supplerende overskrifter** og derefter bruge dem under oprettelse af anmodninger.

## <a name="web-service-settings"></a><a id="settings"></a>Indstillinger for webtjeneste

Brug indstillingerne for webtjeneste til at konfigurere overførsel af direkte data til en webtjeneste. Du kan konfigurere indstillinger for webtjenester ved at gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Webtjenesteindstillinger**.

I følgende tabel beskrives felterne på siden **Indstillinger for webtjeneste**.

| Felt                          | Betegnelse |
|--------------------------------|-------------|
| Webtjeneste                    | Angiv et navn til webtjenesten. |
| Betegnelse                    | Angiv en beskrivelse af webtjenesten. |
| Internetadresse               | <p>Angiv internetadressen på webtjenesten. Hvis der er angivet et webprogram for en webtjeneste, og hvis webtjenestens internetadresse skal være den samme som den internetadresse, der er defineret for det pågældende webprogram, skal du vælge **Kopier URL-basisadresse**. Webprogrammets basis-URL-adresse kopieres derefter til dette felt.</p><p>**Advarsel:** Tredjepartstjenester eller andre tjenester, som du konfigurerer her, kræver ikke certificering og opfylder muligvis ikke Microsofts standarder for beskyttelse af personlige oplysninger. Du bør gennemse dokumentationen til beskyttelse af personlige oplysninger for hver tjeneste og arbejde sammen med de enkelte serviceudbydere for at få mere at vide om det overholdelsesniveau, tjenesten tilbyder. Du er ansvarlig for at sikre, at disse tjenester opfylder dine sikkerhedsmæssige, personlige oplysninger og juridiske standarder. Du bærer selv risikoen for brug af tjenesterne. Microsoft giver ingen andre udtrykkelige garantier eller betingelser. Det anbefales på det kraftigste, at du kun bruger tjenester, der giver sikre og autoriserede forbindelser, f.eks. HTTPS.</p> |
| Certifikat                    | Vælg et Azure Key Vault-certifikat, der tidligere er konfigureret. |
| Webapplikation                | Vælg et webprogram, der tidligere er konfigureret. |
| Svartypen – XML        | Vælg **Ja** i denne indstilling, hvis svartypen er XML. |
| Anmodningsmetode                 | Angiv metoden for anmodningen. HTTP definerer et sæt anmodningsmetoder, der angiver den handling, der skal udføres for en bestemt ressource. Anmodningsmetoden kan være **GET**, **POST** eller en anden HTTP-metode. |
| Overskrifter til anmodning                | Angiv headers til anmodninger. Et anmodningshoved er et HTTP-header, der kan bruges i en HTTP-anmodning. Den er ikke relateret til meddelelsens indhold. |
| Godkend                         | Angiv webanmodningens egenskaber for accept. |
| Kodning af accept                | Angiv værdien for kodning af accept. HTTP-headeren til acceptkodningsanmodningen annoncerer den indholdskodning, som klienten kan forstå. Denne kodning af indhold er normalt en komprimeringsalgoritme. |
| Indholdstype                   | Angiv indholdstypen. HTTP-overskriften til indholdstypeenheden angiver ressourcens medietype. |
| Fuldført svarkode       | Angiv den HTTP-statuskode, der indikerer, at anmodningen blev udført. |
| Formattilknytning for anmodingsheader | Vælg det ER-format, der anvendes til at generere overskrifter til webanmodninger. |

## <a name="message-processing-actions"></a><a id="actions"></a>Handlinger ved meddelelsesbehandling

Du skal bruge handlinger til behandling af meddelelsen til at oprette aktioner til dine processer og definere deres parametre. Du kan konfigurere handlinger til udfyldelse af poster på siden **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelsesbehandlingshandlinger**.

I følgende tabel beskrives felterne på siden **Handlinger ved meddelelsesbehandling**.

### <a name="general-fasttab"></a>Oversigtspanelet Generelt

| Felt                                     | Betegnelse |
|-------------------------------------------|-------------|
| Aktionstype                               | Vælg handlingstypen. Du kan finde oplysninger om de tilgængelige indstillinger i sektionen [Typer af handlinger til behandling af meddelelser](#action-types) senere i dette emne. |
| Formattilknytning                            | Vælg det ER-format, der skal kaldes for handlingen. Dette felt er kun tilgængeligt for handlinger af typerne **Eksport af elektronisk rapportering**, **Import af elektronisk rapportering** og **Meddelelse om eksport af elektronisk rapportering**. |
| Formattilknytning for URL-sti               | Vælg det ER-format, der skal kaldes for handlingen. Dette format anvendes til at angive stien til den URL-adresse, som bliver føjet til den basisinternetadresse, der er angivet for den valgte webserver. Dette felt er kun tilgængeligt for handlinger af typen **Webtjeneste**. |
| Typen af meddelelseselement                         | Vælg den type poster, som handlingen skal evalueres for. Dette felt er tilgængeligt for handlinger af typen **Udførelsesniveau for meddelelseselement**, **Eksport af elektronisk rapportering**, **Import af elektronisk rapportering** og **Webtjeneste** samt visse andre typer. Hvis du lader feltet stå tomt, evalueres alle de meddelelseselementtyper, som er defineret for behandlingen af meddelelser. |
| Eksekverbar klasse                          | Vælg en eksisterende klasseindstilling, der kan udføres. Dette felt er kun tilgængeligt for handlinger af typen **Udførelsesniveau for meddelelseselement** og **Udførelsesniveau for meddelelseselement**. |
| Handlingen Udfyld poster                   | Vælg en eksisterende handling med udfyld poster. Dette felt er kun tilgængeligt for handlinger af typen **Udfyld poster**. |
| Webtjeneste                               | Vælg en eksisterende webtjeneste. Dette felt er kun tilgængeligt for handlinger af typen **Webtjeneste**. |
| Filnavn                                 | Angiv navnet på den fil, som handlingen skal resultere i. Den pågældende fil kan være svaret fra webserveren eller den genererede rapport. Dette felt er kun tilgængeligt for handlinger af typen **Webtjenesten** og **Meddelelse om eksport af elektronisk rapportering**. |
| Knyt filer til kildedokumenter          | Marker dette afkrydsningsfelt for at vedhæfte genererede filer til poster i en mastertabel, der refereres til, for EM-varer. Dette felt er kun tilgængeligt for handlinger af typen **Webtjeneste** og **Eksport af elektronisk rapportering**. |
| Vedhæft filer fra outputarkiv til elementer | Marker dette afkrydsningsfelt for at udtrække separate XML-filer fra outputarkivfilen og vedhæfte dem til de tilsvarende elektronisk meddelelseselementer. Dette felt er kun tilgængeligt for handlinger af typen **Eksport af elektronisk rapportering**. |
| Antal meddelelseselementer pr. eksport        | Angiv grænsen for det antal meddelelseselementer, der skal medtages i én fil (meddelelse). Dette felt er kun tilgængeligt for handlinger af typen **Eksport af elektronisk rapportering**. |
| Brug ER-kilde                             | Marker dette afkrydsningsfelt for at bruge ER-kildeparametre til import. Ellers bruges den vedhæftede fil fra den elektroniske meddelelse. Dette felt er kun tilgængeligt for handlinger af typen **Import af elektronisk rapportering**. |
| Vis dialogboks                               | Angiv denne indstilling til **Ja**, hvis der skal vises en dialogboks til brugerne før rapporten genereres. Dette felt er kun tilgængeligt for handlinger af typen **Meddelelse om eksport af elektronisk rapportering**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Typer af handlinger til behandling af meddelelser

Følgende indstillinger er tilgængelige i feltet **Handlingstype**:

- **Opret meddelelse** – Anvend denne handlingstype for at tillade brugerne at oprette meddelelser på siden **Elektronisk meddelelse** manuelt. Der kan ikke konfigureres en førstestatus for en handling af denne type.
- **Udfyld poster** - Denne aktionstype skal allerede være konfigureret. Knyt den til en handling af typen Udfyld poster, så den kan indgå i behandlingen. Det antages, at denne handlingstype enten anvendes til den første handling i meddelelsesbehandlingen (i de tilfælde, hvor der ikke blev oprettet nogen elektronisk meddelelse på forhånd) eller til en handling, der tilføjer meddelelseselementer til en meddelelse, som tidligere blev oprettet ved hjælp af en **Opret meddelelse**-handlingstype. Som følge heraf kan der for denne type handlinger alene konfigureres en resultatstatus for meddelelseselementer. Der kan alene konfigureres en indledende status for meddelelser.
- **Udførelsesniveau for meddelelse** – Anvend denne handlingstype til at konfigurere en udførelsesklasse, der bør evalueres på meddelelsesniveauet.
- **Udførelsesniveau for meddelelseselement** – Anvend denne handlingstype til at konfigurere en udførelsesklasse, der bør evalueres på niveauet for meddelelseselementet.
- **Eksport af elektronisk rapportering** – Brug denne type til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport, på niveauet for meddelelseselementet.
- **Meddelelse om eksport af elektronisk rapportering** – Anvend denne handlingstype til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport på niveauet for meddelelsen (eksempelvis når en meddelelse ikke har nogle meddelelseselementer).
- **Import af elektronisk rapportering** – Anvend denne handlingstype til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til import.
- **Brugerbehandling på meddelelsesniveau** – Anvend denne handlingstype til handlinger, der forudsætter visse manuelle handlinger på meddelelsesniveau. For eksempel kan brugeren opdatere status for meddelelser.
- **Brugerbehandling** – Anvend denne handlingstype til handlinger, der forudsætter visse manuelle handlinger på niveauet for meddelelseselementet. For eksempel kan brugeren opdatere status for meddelelseselementer.
- **Webtjeneste** – Anvend denne handlingstype til handlinger, der skal fremsende en genereret rapport til en webtjeneste. Denne handlingstype bruges ikke til rapportering af kommunikation vedr. italienske købs- og salgsfakturaer. For handlinger af typen Webtjeneste indeholder siden **Handlinger ved meddelelsesbehandling** et oversigtspanel med **Diverse detaljer**, hvor du kan angive en bekræftelsestekst. Denne bekræftelsestekst bliver vist for brugerne, før anmodningerne til den valgte webtjeneste bliver behandlet.
- **Anmodningsbekræftelse** – Anvend denne handlingstype til at anmode om bekræftelse fra en server.

### <a name="initial-statuses-fasttab"></a>Oversigtspanelet Førstestatusser

> [!NOTE]
> Oversigtspanelet **Indledende statusser** er ikke tilgængeligt for handlinger, der har en indledende handling af typen **Opret meddelelse**.

| Felt               | Beskrivelse |
|---------------------|-------------|
| Status for meddelelseselement | Vælg den meddelelseselementsstatus, som skal den valgte handling til behandling af meddelelsen, skal evalueres for. |
| Betegnelse         | Beskrivelse af det valgte meddelelseselements status. |

### <a name="result-statuses-fasttab"></a>Oversigtspanelet Resultatstatusser

| Felt               | Betegnelse |
|---------------------|-------------|
| Meddelelsesstatus      | Vælg den meddelelsesstatus, som skal den valgte handling til behandling af meddelelsen, skal evalueres for. Dette felt er kun tilgængeligt for handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelsen. Det er eksempelvis tilgængeligt for handlinger af typen **Eksport af elektronisk rapportering** og **Import af elektronisk rapportering**, men er ikke tilgængelig for handlinger af typerne **Brugerbehandling** og **Udførelsesniveau for meddelelseselement**. |
| Betegnelse         | Beskrivelse af den valgte meddelelses status. |
| Svartype       | Svartypen for den valgte meddelelses status. |
| Status for meddelelseselement | Vælg den resultatstatus, som skal være tilgængelig, efter at den valgte handling til behandling af meddelelsen er evalueret. Dette felt er kun tilgængeligt for handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelseselementet. Det er f.eks. ikke tilgængeligt for handlinger af typen **Brugerbehandling** og **Udførelsesniveau for meddelelseselement**. I forbindelse med handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelsen, viser dette felt den meddelelseselementstatus, der er angivet for den valgte meddelelsesstatus. |

Følgende tabel viser de resultatstatusser, der skal konfigureres for de forskellige handlingstyper og svartyper.

| Handlingstype/svartype for elektroniske meddelelser | Udført korrekt | Business-fejl | Teknisk fejl | Brugerdefineret  | Annullering |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Opret meddelelse                               | X                     |                |                 |              |        |
| Eksport af elektronisk rapportering                  | X                     |                |                 |              |        |
| Import af elektronisk rapportering                  |                       |                |                 |              |        |
| Webtjeneste                                  | X                     |                | X               |              |        |
| Brugerbehandling                              |                       |                |                 |              |        |
| Udførelsesniveau for meddelelse                      |                       |                |                 |              |        |
| Udfyld poster                             |                       |                |                 |              |        |
| Udførelsesniveau for meddelelseselement                 |                       |                |                 |              |        |
| Anmodningsbekræftelse                         | X                     | X              | X               |              |        |
| Meddelelse om eksport af elektronisk rapportering          | X                     |                |                 |              |        |
| Behandling af bruger på meddelelsesniveau                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Behandling af elektronisk meddelelse

Elektronisk meddelelsesbehandling er et grundlæggende begreb i forbindelse med EM-funktionen. Det samler handlinger, der skal evalueres for den elektroniske meddelelse. Handlingerne kan tilknyttes via førstestatus og resultatstatus. Du kan også starte handlinger af typen **Brugerbehandling** særskilt. Hvis du vil konfigurere behandling af elektroniske meddelelser, skal du gå til **Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Elektronisk meddelelsesbehandling**.

I oversigtspanelet **Handling** kan du føje foruddefinerede handlinger til behandling. Du kan angive, hvorvidt en handling skal køres separat, eller om den kan påbegyndes af behandlingen. For at præcisere at en handling i behandling alene kan påbegyndes af en bruger, skal du angive **Ja** i feltet **Kør separat** for den pågældende handling. Såfremt en handling skal påbegyndes i forbindelse med behandlingen af meddelelser eller meddelelseselementer med en status, der er defineret som den indledende status for en handling, skal feltet **Kør separat** angives til **Nej**. Handlinger af typen **Brugerhandling** skal altid køres separat.

Adskillige handlinger skal til tider samles i én serie, selv om den første handling er konfigureret til at køre separat. En bruger skal f.eks. initialisere generering af rapporter. Eksempelvis når en bruger skal påbegynde rapportgenerering, men umiddelbart efter rapportens dannelse skal sende den til en webtjeneste, og webtjenestens svar skal afspejles i systemet. Du kan i denne situation oprette en uadskillelig sekvens for de handlinger, som altid skal køres sammen. Vælg **Uadskillelige sekvenser** ovenover gitteret i oversigtspanelet for **Handling**, og opret en sekvens. Vælg dernæst sekvensen i feltet **Uadskillelig sekvens** for alle de handlinger, der skal køres sammen. I dette tilfælde kan feltet **Kør separat** angives til **Ja** for den første handling i sekvensen, men til **Nej** for alle de øvrige handlinger.

Handlinger for eksport af **Elektronisk rapportering** og **eksport af elektronisk rapportering for meddelelser** kører et ER-format, der indeholder inputparametre. Hvis behandlingen af den elektroniske meddelelse inkluderer aktioner af en af disse typer, skal du angive værdierne for inputparametrene, før du kan oprette rapporter. På denne måde kan systemet bruge et batchjob til at oprette rapporten. Du kan vælge **Parametre** over gitteret for at angive parametre for den valgte aktionstype (**Elektronisk rapporteringseksport** eller **Elektronisk rapporteringseksportmeddelelse**). Marker afkrydsningsfeltet **Brug parametre** for den handling, der skal køres med de angivne parametre i et batchjob.

Brug oversigtspanelet **Ekstra felter i meddelelseselement** for at tilføje flere foruddefinerede felter, der vedrører meddelelseselementer. Du skal tilføje flere felter for hver type meddelelseselement, der vedrører felterne. Du kan angive en standardværdi, som tildeles det ekstra felt under behandlingen.

Brug oversigtspanelet **Yderligere meddelelsesfelter** for at tilføje flere foruddefinerede felter, der vedrører meddelelser. Du kan angive en standardværdi, som tildeles det ekstra felt under behandlingen.

Brug oversigtspanelet **Sikkerhedsroller** for at konfigurere de sikkerhedsroller, der er foruddefineret i systemet til bestemte behandling. Brugere, der har en bestemt rolle, ser kun behandling, der er defineret for den pågældende rolle.

Brug oversigtspanelet **Batch** for at konfigurere behandlingen, så den kan bruges i en batchordning. Det anbefales, at du opretter et batchjob til behandlingen direkte på siden **Elektroniske meddelelser** eller **Elementer for elektronisk meddelelse**, når du vælger **Kør behandling** i handlingsruden for at starte behandlingen.
