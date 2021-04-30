---
title: Elektroniske meddelelser
description: Dette emne indeholder en oversigt og oplysninger om opsætning for elektroniske meddelelser i Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dd49edeb92e6a23723b1b6b6ea7800b69a81bd0f
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897594"
---
# <a name="electronic-messaging"></a>Elektroniske meddelelser

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt og oplysninger om opsætning for elektroniske meddelelser.

Offentlige myndigheder og lovgivende forsamlinger i forskellige lande og områder i hele verden har for nylig implementeret krav til rapportering for virksomheder, der er registreret i disse lande eller områder. Formålet med kravene er at gøre det muligt at få data fra disse virksomheder i elektronisk format direkte fra de systemer, hvor de er blevet bogført, gemt og behandlet.

Den elektroniske meddelelsesfunktion i Finance understøtter forskellige elektroniske kommunikationsprocesser mellem Finance og de systemer, som offentlige myndigheder tilbyder til rapportering, afsendelse og modtagelse af officielle oplysninger.

Den elektroniske meddelelsesfunktion er integreret i modulet **Elektronisk rapportering** (Electronic Reporting – ER). Derfor kan du konfigurere ER-formater til elektroniske meddelelser. Du kan finde flere oplysninger under [Elektronisk rapportering (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniske meddelelser er baseret på følgende enheder:

- **Elektronisk meddelelse** – En rapport eller erklæring, der skal rapporteres og/eller overføres internt. Et eksempel er en rapport, der sendes til et skattekontor.
- **Elektroniske meddelelseselementer** – Poster, der skal medtages i den meddelelse, der rapporteres.
- **Behandling af elektroniske meddelelser** – En kæde af handlinger, der skal køres for at indsamle de nødvendige data, generere rapporter, gemme data i Microsoft Azure Blob-lageret, sende rapporter uden for systemet, modtage svar, der ikke kommer fra systemet, og opdatere databasen på grundlag af de modtagne oplysninger. Handlingerne i kæden kan enten være forbundne eller ikke-forbundne.

I følgende illustration vises en række data til elektroniske meddelelser.

![Dataflow for elektroniske meddelelser](media/electronic-messaging-data-flow.png)

Den elektroniske meddelelsesfunktion understøtter følgende scenarier:

- Manuel oprettelse af meddelelser og generering af rapporter, der er baseret på tilknyttede ER-formater til eksport af forskellige typer: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst og Microsoft Word.
- Automatisk oprettelse og behandling af meddelelser, som er baseret på oplysninger, der blev anmodet om og modtaget fra en myndighed via et tilknyttet ER-format til import.
- Indsamling og behandling af oplysninger fra en datakilde som meddelelseselementer. Datakilden er en Finance-tabel.
- Lagring af flere oplysninger og evaluering af forskellige værdier ved at kalde specifikt definerede eksekverbare klasser i forhold til meddelelser eller meddelelseselementer.
- Aggregering af oplysninger, der er indsamlet i meddelelseselementer, opdeling af disse oplysninger efter meddelelse og generering af rapporter, der er i tilknyttede ER-eksportformater.
- Afsendelse af rapporter, som er genereret til en webtjeneste ved hjælp af sikkerhedsoplysninger, der er gemt i Azure Key Vault.
- Modtagelse af svar fra en webtjeneste, fortolkning af svaret og opdatering af data i Finance efter behov.
- Lagring og gennemgang de rapporter, der genereres.
- Lagring og gennemgang af alle logoplysninger, der er knyttet til handlinger, der køres for en meddelelse eller et meddelelseselement.
- Styring af behandlingen via forskellige meddelelsesstatusser og meddelelseselementstatusser.

## <a name="set-up-electronic-messaging"></a>Konfigurere elektroniske meddelelser

Elektroniske meddelelser kan hjælpe dig med at vedligeholde forskellige elektroniske rapporteringsprocesser for forskellige dokumenttyper. Elektroniske meddelelser er i visse komplekse scenarier konfigureret på en sådan måde, at de indeholder en kombination af mange meddelelsesstatusser, statusser for meddelelseselementer, handlinger, ekstra felter og udførelsesklasser. Der findes pakker med dataenheder til import i disse scenarier. Hvis du bruger disse dataenhedspakker, skal du importere dem til en juridisk enhed ved hjælp af datastyringsværktøjet. Du kan finde flere oplysninger om, hvordan du bruger af datastyringsværktøjet, i [Datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Hvis du ikke importerer en dataenhedspakke, kan du manuelt konfigurere den elektroniske meddelelsesfunktion. I dette tilfælde skal du definere følgende elementer:

- [Nummerserier](#number-sequences)
- [Meddelelseselementtyper og -statusser](#message-item-types-and-statuses)
- [Meddelelsesstatusser](#message-statuses)
- [Ekstra felter](#additional-fields)
- [Indstillinger for eksekverbar klasse](#executable-class-settings)
- [Handlingerne Udfyld poster](#populate-records-actions)
- [Webapplikationer](#web-applications)
- [Indstillinger for webtjeneste](#web-service-settings)
- [Handlinger ved meddelelsesbehandling](#message-processing-actions)
- [Behandling af elektronisk meddelelse](#electronic-message-processing)

Nedenstående afsnit indeholder flere oplysninger om hvert af disse elementer.

### <a name="number-sequences"></a>Nummerserier

Konfigurer nummerserier for både meddelelser og meddelelseselementer. Nummerserierne anvendes til at generere numre for meddelelser og meddelelseselementer automatisk. De tildelte numre anvendes som unikke identifikatorer for meddelelserne og meddelelseselementerne i systemet. Du kan oprette nummerserier til elektroniske meddelelser på siden **Finansparametre** (**Finans** \> **Opsætning Finans** \> **Finansparametre**).

### <a name="message-item-types-and-statuses"></a>Meddelelseselementtyper og -statusser

Meddelelseselementtyper identificerer typerne af poster, der skal bruges i elektroniske meddelelser. Du kan konfigurere meddelelseselementtyper på siden **Typer af meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Typer af meddelelseselement**).

Meddelelseselementstatusser identificere de statusser, der gælder for meddelelseselementer i behandlingen, som du konfigurerer. Du kan konfigurere meddelelseselementtyper på siden **Statusser for meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Statusser for meddelelseselement**).

Parametret **Tillad sletning** for et meddelelseselements status definerer, om brugeren kan slette meddelelseselementer, som har denne status, på siden **Elektroniske meddelelser** eller siden **Elektronisk meddelelseselementer**.

### <a name="message-statuses"></a>Meddelelsesstatusser

Konfigurer de meddelelsesstatusser, der skal være tilgængelige i behandling af meddelelser. Du kan konfigurere meddelelsesstatusser på siden **Meddelelsesstatusser** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelsesstatusser**).

I følgende tabel beskrives felterne på siden **Meddelelsesstatusser**.

| Feltnavn          | Beskrivelse |
|---------------------|-------------|
| Meddelelsesstatus      | Indtast et unikt navn for meddelelsens status. Meddelelsesstatusser anvendes til at karakterisere en elektronisk meddelelses tilstand på ethvert tidspunkt. Det indtastede navn fremgår af siden **Elektroniske meddelelser** og en log, der er tilknyttet elektroniske meddelelser. |
| Beskrivelse         | Indtast en beskrivelse af meddelelsens status. |
| Svartype       | Vælg svartypen for meddelelsens status. Visse handlinger i en behandling kan producere mere end én svartype. Eksempelvis kan handlinger af typen **Webtjeneste** producere svartyper i form af enten **Udført korrekt** eller **Teknisk fejl** afhængigt af resultatet af kørslen. I dette tilfælde skal du definere meddelelsesstatussen for begge svartyper. Du kan finde flere oplysninger om handlingstyper og de svartyper, der er forbundet hermed, under [Handlingstyper for behandling af meddelelser](#message-processing-action-types). |
| Status for meddelelseselement | Til tider skal statussen for en elektronisk meddelelse påvirke statussen for tilknyttede meddelelseselementer. Vælg i dette felt en status for et meddelelseselement for at knytte den til meddelelsens status. |
| Tillad sletning        | Marker dette afkrydsningsfelt, hvis brugerne skal kunne slette elektroniske meddelelser med denne status på siden **Elektroniske meddelelser**. |

### <a name="additional-fields"></a>Ekstra felter

Med den elektroniske meddelelsesfunktion kan du udfylde poster fra en transaktionstabel. På denne måde kan du opstille posterne til rapportering og derefter rapportere dem. I visse tilfælde er der dog ikke tilstrækkelige oplysninger i transaktionstabellerne til at kunne udfylde posterne i overensstemmelse med rapporteringskravene. Du kan oprette ekstra felter med henblik på at angive alle de oplysninger, der skal rapporteres for en post. Der kan knyttes flere felter til både meddelelser og meddelelser. Du kan oprette flere felter på siden **Ekstra felter** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Ekstra felter**).

I følgende tabel beskrives de generelle felter på siden **Ekstra felter**.

| Felt       | Beskrivelse |
|-------------|-------------|
| Feltnavn  | Angiv navnet på en ekstra attribut for meddelelseselementer, der vedrører processen. Dette navn vises i brugergrænsefladen (UI), mens du arbejder med processen. Det kan også bruges i ER-konfigurationer, der er knyttet til processen. |
| Beskrivelse | Indtast en beskrivelse af det ekstra felt. |
| Brugerredigering   | Angiv denne indstilling til **Ja**, hvis brugerne skal kunne ændre værdien for det ekstra felt fra brugergrænsefladen. |
| Tæller     | Angiv denne indstilling til **Ja**, hvis det ekstra felt skal indeholde en nummerserie i en elektronisk meddelelse. Værdien i det ekstra felt udfyldes automatisk, når der køres en handling i form af **Eksport af elektronisk rapportering**. |
| Skjulte      | Angiv denne indstilling til **Ja**, hvis det ekstra felt skal være skjult i brugergrænsefladen. |

Hvert af de ekstra felter kan have forskellige værdier for behandlingen. Du kan definere disse værdier i oversigtspanelet **Værdier**. I følgende tabel beskrives felterne.

| Felt                | Beskrivelse |
|----------------------|-------------|
| Feltværdi          | Indtast den feltværdi, der skal anvendes for en meddelelse eller et meddelelseselement under rapportering. |
| Beskrivelse          | Indtast en beskrivelse af feltværdien. |
| Kontotype         | Visse feltværdier kan være begrænset til bestemte kontotyper. Vælg en eller flere af følgende værdier: **Alle**, **Debitor** eller **Kreditor**. |
| Kontokode         | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, kan du yderligere begrænse brugen af feltværdien til en bestemt gruppe eller tabel. |
| Konto/gruppenummer | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, og hvis du har angivet en gruppe eller en tabel i feltet **Kontokode**, kan du angive en bestemt gruppe eller modpostering i dette felt. |
| Gyldig            | Angiv den dato, hvor værdien skal begynde at blive taget i betragtning. |
| Udløb           | Angiv den dato, hvor værdien ikke længere skal tages i betragtning. |

Kombinationer af de kriterier, der er defineret i felterne **Konto/gruppenummer**, **Kontokode**, **Gyldig** og **Udløb**, påvirker som standard ikke valget af værdier for de ekstra felter. Disse kombinationer kan dog anvendes i en udførelsesklasse til at implementere specifikke regler, som beregner værdierne for de ekstra felter.

### <a name="executable-class-settings"></a>Indstillinger for eksekverbar klasse

En eksekverbar klasse er en X ++-metode eller en klasse, som den elektroniske meddelelsesbehandling kan kalde i forhold til en handling, hvis en form for vurdering er påkrævet for processen.

Du kan manuelt oprette en eksekverbar klasse på siden **Indstillinger for eksekverbar klasse** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Indstillinger for eksekverbar klasse**). Opret en linje, og angiv følgende felter.

| Felt                 | Betegnelse |
|-----------------------|-------------|
| Eksekverbar klasse      | Skriv det navn, der skal bruges under konfigurationen af en meddelelsesbehandling, som denne klasse kaldes i forhold til. |
| Betegnelse           | Angiv en beskrivelse af den eksekverbare klasse. |
| Navn på eksekverbar klasse | Vælg en X ++ eksekverbar klasse. |
| Udførelsesniveau       | Dette felt angives automatisk, fordi værdien skal være foruddefineret for den valgte eksekverbare klasse. Dette felt begrænser det niveau, som den relaterede evaluering kører på. |
| Beskrivelse af klasse     | Dette felt angives automatisk, fordi værdien skal være foruddefineret for den valgte eksekverbare klasse. |

Visse udførelsesklasser kan have obligatoriske parametre, som skal defineres, før udførelsesklassen køres første gang. Du kan definere disse parametre ved at vælge **Parametre** i handlingsruden, angive felterne i den dialogboks, der vises, og derefter vælge **OK**. Det er vigtigt, at du vælger **OK**. I modsat fald bliver parametrene ikke gemt i databasen, og udførelsesklassen bliver ikke kaldt korrekt.

### <a name="populate-records-actions"></a>Handlingerne Udfyld poster

Du bruger handlinger til udfyldelse af poster til at konfigurere handlinger, der tilføjer poster til tabellen Meddelelseselementer, så de kan føjes til en elektronisk meddelelse. Hvis din elektroniske meddelelse eksempelvis skal rapportere debitorfakturaer, skal du konfigurere en handling til at udfylde poster, der er kædet sammen med feltet **Datakilde** i tabellen i debitorfakturajournalen. Du kan konfigurere handlinger til udfyldelse af poster på siden **Handlingen Udfyld poster** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Handlingen Udfyld poster**). Opret en ny post for hver handling, der skal føje poster til tabellen, og angiv følgende felter.

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
| Feltet dokumentnummer  | Vælg det felt, som dokumentnummeret skal tages fra i den valgte tabel. |
| Feltet Dokumentdato    | Vælg det felt, som dokumentets dato skal tages fra i den valgte tabel. |
| Feltet Dokumentkonto | Vælg det felt, som dokumentkontoen skal tages fra i den valgte tabel. |
| Brugerforespørgsel             | Hvis dette afkrydsningsfelt er markeret, kan du oprette en forespørgsel ved at vælge **Rediger forespørgsel** over gitteret. I modsat fald udfyldes alle posterne af den valgte datakilde. |

### <a name="web-applications"></a>Webapplikationer

Du kan anvende webprogramindstillingerne til at konfigurere et webprogram, således at det understøtter Open Authorization (OAuth) 2,0. OAuth er den åbne standard, som gør det muligt for brugerne at tildele "sikker delegeret adgang" til programmet på deres vegne uden at dele deres legitimationsoplysninger. Du kan også komme igennem godkendelsesprocessen ved at få en godkendelseskode og et adgangstoken. Du kan konfigurere indstillinger for webprogrammer på siden **Webprogrammer** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Webprogrammer**).

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
| Adgangstokenet udløber om  | Den resterende tid før adgangstokenet udløber. | 
| Godkend                       | Angiv webanmodningens egenskaber for **Accept**. Indtast eksempelvis **application/vnd.hmrc.1.0+json**. |
| Indholdstype                 | Angiv indholdstypen. Indtast eksempelvis **application/json**. |

Derudover er følgende knapper tilgængelige i handlingsruden på siden **Webprogrammer** med henblik på at understøtte godkendelsesprocessen:

- **Få godkendelseskode** – Påbegynd godkendelse af webprogrammet.
- **Hent adgangstoken** – Påbegynd processen med at få et adgangstoken.
- **Opdater adgangstoken** – Opdater et adgangstoken.

Når et adgangstoken til et webprogram gemmes i systemets database i krypteret format, kan det anvendes til anmodninger til en webtjeneste. Af sikkerhedsmæssige årsager skal adgangen til adgangstokenet begrænses til de sikkerhedsroller, der skal have tilladelse til at behandle de pågældende anmodninger. Såfremt brugere uden for sikkerhedsgruppen forsøger at behandle en anmodning, modtager de en fejlmeddelelse, som oplyser, at de ikke har tilladelse til at arbejde via det valgte webprogram. For at oprette de sikkerhedsroller, der skal have adgang til et adgangstoken, skal du anvende **Sikkerhedsroller** i oversigtspanelet på siden **Webprogrammer**. Såfremt sikkerhedsrollerne ikke defineres for et webprogram, er det kun muligt for en systemadministrator at arbejde via dette webprogram.

### <a name="web-service-settings"></a>Indstillinger for webtjeneste

Du kan bruge indstillingerne for webtjeneste til at konfigurere overførsel af direkte data til en webtjeneste. Du kan konfigurere indstillinger for webtjenesten på siden **Indstillinger for webtjeneste** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Indstillinger for webtjeneste**) .

I følgende tabel beskrives felterne på siden **Indstillinger for webtjeneste**.

| Felt                          | Betegnelse |
|--------------------------------|-------------|
| Webtjeneste                    | Angiv et navn til webtjenesten. |
| Betegnelse                    | Angiv en beskrivelse af webtjenesten. |
| Internetadresse               | Angiv internetadressen på webtjenesten. Hvis der er angivet et webprogram for en webtjeneste, og hvis webtjenestens internetadresse skal være den samme som den internetadresse, der er defineret for det pågældende webprogram, skal du vælge **Kopier URL-basisadresse** for at kopiere webprogrammets URL-basisadresse til dette felt. |
| Certifikat                    | Vælg et Key Vault-certifikat, der tidligere er konfigureret. |
| Webapplikation                | Vælg et Key Vault-certifikat, der tidligere er konfigureret. |
| Svartypen – XML        | Vælg **Ja** i denne indstilling, hvis svartypen er XML. |
| Anmodningsmetode                 | Angiv metoden for anmodningen. HTTP definerer et sæt anmodningsmetoder, der angiver den handling, der skal udføres for en bestemt ressource. Anmodningsmetoden kan være **GET**, **POST** eller en anden HTTP-metode. |
| Overskrifter til anmodning                | Angiv headers til anmodninger. En anmodningsheader er en HTTP-header, der kan bruges i en HTTP-anmodning, og som ikke er relateret til indholdet af meddelelsen. |
| Godkend                         | Angiv webanmodningens egenskaber for **Accept**. |
| Kodning af accept                | Angiv værdien for **Kodning af accept**. HTTP-headeren til acceptkodningsanmodningen annoncerer den indholdskodning, som klienten kan forstå. Denne kodning af indhold er normalt en komprimeringsalgoritme. |
| Indholdstype                   | Angiv indholdstypen. HTTP-overskriften til indholdstypeenheden angiver ressourcens medietype. |
| Fuldført svarkode       | Angiv den HTTP-statuskode, der indikerer, at anmodningen blev udført. |
| Formattilknytning for anmodingsheader | Vælg det ER-format, der anvendes til at generere overskrifter til webanmodninger. |

### <a name="message-processing-actions"></a>Handlinger ved meddelelsesbehandling

Du skal bruge handlinger til behandling af meddelelsen til at oprette aktioner til dine processer og definere deres parametre. Du kan konfigurere handlinger til behandling af meddelelsen på siden **Statusser for meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Handlinger ved meddelelsesbehandling**).

I følgende tabel beskrives felterne på siden **Handlinger ved meddelelsesbehandling**.

#### <a name="general-fasttab"></a>Oversigtspanelet Generelt

| Felt                       | Betegnelse |
|-----------------------------|-------------|
| Aktionstype                 | Vælg handlingstypen. Du kan finde oplysninger om de tilgængelige indstillinger i sektionen [Typer af handlinger til behandling af meddelelser](#message-processing-action-types). |
| Formattilknytning              | Vælg det ER-format, der skal kaldes for handlingen. Dette felt er kun tilgængeligt for handlinger af typerne **Eksport af elektronisk rapportering**, **Import af elektronisk rapportering** og **Meddelelse om eksport af elektronisk rapportering**. |
| Formattilknytning for URL-sti | Vælg det ER-format, der skal kaldes for handlingen. Dette felt er kun tilgængeligt for handlinger af typen **Webtjeneste**. Feltet anvendes til at angive stien til den URL-adresse, som bliver føjet til den basisinternetadresse, der er angivet for den valgte webserver. |
| Typen af meddelelseselement           | Vælg den type poster, som handlingen skal evalueres for. Dette felt er tilgængeligt for handlinger af typen **Udførelsesniveau for meddelelseselement**, **Eksport af elektronisk rapportering**, **Import af elektronisk rapportering** og **Webtjeneste** samt visse andre typer. Hvis du lader feltet stå tomt, evalueres alle de meddelelseselementtyper, som er defineret for behandlingen af meddelelser. |
| Eksekverbar klasse            | Vælg de eksekverbare klasseindstillinger, der tidligere blev oprettet. Dette felt er kun tilgængeligt for handlinger af typen **Udførelsesniveau for meddelelseselement** og **Udførelsesniveau for meddelelseselement**. |
| Handlingen Udfyld poster     | Vælg en Udfyld poster-handling, der tidligere blev oprettet. Dette felt er kun tilgængeligt for handlinger af typen **Udfyld poster**. |
| Webtjeneste                 | Vælg en webtjeneste, der tidligere blev oprettet. Dette felt er kun tilgængeligt for handlinger af typen **Webtjeneste**. |
| Filnavn                   | Angiv navnet på den fil, som handlingen skal resultere i. Den pågældende fil kan være svaret fra webserveren eller den genererede rapport. Dette felt er kun tilgængeligt for handlinger af typen **Webtjenesten** og **Meddelelse om eksport af elektronisk rapportering**. |
| Vis dialogboks                 | Angiv denne indstilling til **Ja**, hvis der skal vises en dialogboks til brugerne før rapporten genereres. Dette felt er kun tilgængeligt for handlinger af typen **Meddelelse om eksport af elektronisk rapportering**. |

##### <a name="message-processing-action-types"></a>Typer af handlinger til behandling af meddelelser

Følgende indstillinger er tilgængelige i feltet **Handlingstype**:

- **Opret meddelelse** – Anvend denne handlingstype for at tillade brugerne at oprette meddelelser på siden **Elektronisk meddelelse** manuelt. Der kan ikke konfigureres en førstestatus for en handling af denne type.
- **Udfyld poster** – En handling af typen **Udfyld posterne** skal være konfigureret på forhånd. Tilknyt denne handlingstype til en handling, der skal udfylde poster, for at tillade, at den pågældende handling medtages i behandlingen. Det antages, at denne handlingstype enten anvendes til den første handling i meddelelsesbehandlingen (i de tilfælde, hvor der ikke blev oprettet nogen elektronisk meddelelse på forhånd) eller til en handling, der tilføjer meddelelseselementer til en meddelelse, som tidligere blev oprettet ved hjælp af en **Opret meddelelse**-handlingstype. Som følge heraf kan der for denne type handlinger alene konfigureres en resultatstatus for meddelelseselementer. Der kan alene konfigureres en indledende status for meddelelser.
- **Udførelsesniveau for meddelelse** – Anvend denne handlingstype til at konfigurere en udførelsesklasse, der bør evalueres på meddelelsesniveauet.
- **Udførelsesniveau for meddelelseselement** – Anvend denne handlingstype til at konfigurere en udførelsesklasse, der bør evalueres på niveauet for meddelelseselementet.
- **Eksport af elektronisk rapportering** – Anvend denne handlingstype til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport på niveauet for meddelelseselementet.
- **Meddelelse om eksport af elektronisk rapportering** – Anvend denne handlingstype til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport på niveauet for meddelelsen (eksempelvis når en meddelelse ikke har nogle meddelelseselementer).
- **Import af elektronisk rapportering** – Anvend denne handlingstype til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til import.
- **Brugerbehandling på meddelelsesniveau** – Anvend denne handlingstype til handlinger, der forudsætter visse manuelle handlinger på meddelelsesniveau. For eksempel kan brugeren opdatere status for meddelelser.
- **Brugerbehandling** – Anvend denne handlingstype til handlinger, der forudsætter visse manuelle handlinger på niveauet for meddelelseselementet. For eksempel kan brugeren opdatere status for meddelelseselementer.
- **Webtjeneste** – Anvend denne handlingstype til handlinger, der skal fremsende en genereret rapport til en webtjeneste. Denne handlingstype bruges ikke til rapportering af kommunikation vedr. italienske købs- og salgsfakturaer. For handlinger af typen **Webtjeneste** indeholder siden **Handlinger ved meddelelsesbehandling** et oversigtspanel med **Diverse detaljer**, hvor du kan angive en bekræftelsestekst. Denne bekræftelsestekst bliver vist for brugerne, før anmodningerne til den valgte webtjeneste bliver behandlet.
- **Anmodningsbekræftelse** – Anvend denne handlingstype til at anmode om bekræftelse fra en server.

#### <a name="initial-statuses-fasttab"></a>Oversigtspanelet Førstestatusser

> [!NOTE]
> Oversigtspanelet **Indledende statusser** er ikke tilgængeligt for handlinger, der har en indledende handling af typen **Opret meddelelse**.

| Felt               | Beskrivelse |
|---------------------|-------------|
| Status for meddelelseselement | Vælg den meddelelseselementsstatus, som skal den valgte handling til behandling af meddelelsen, skal evalueres for. |
| Betegnelse         | Beskrivelse af det valgte meddelelseselements status. |

#### <a name="result-statuses-fasttab"></a>Oversigtspanelet Resultatstatusser

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

### <a name="electronic-message-processing"></a>Behandling af elektronisk meddelelse

Elektronisk meddelelsesbehandling er et grundlæggende begreb i forbindelse med den elektroniske meddelelsesfunktion. Det samler handlinger, der skal evalueres for den elektroniske meddelelse. Handlingerne kan tilknyttes via førstestatus og resultatstatus. Du kan også starte handlinger af typen **Brugerbehandling** særskilt. På siden **Behandling af elektronisk meddelelse** (**Moms** \> **Opsætning** \> **Elektroniske meddelelser** \> **Behandling af elektronisk meddelelse**) kan du ligeledes vælge ekstra felter, der bør understøttes i forbindelse med behandlingen på enten meddelelsesniveau eller meddelelseselementniveau.

I oversigtspanelet **Handling** kan du føje foruddefinerede handlinger til behandling. Du kan angive, hvorvidt en handling skal køres separat, eller om den kan påbegyndes af behandlingen. For at præcisere at en handling i behandling alene kan påbegyndes af en bruger, skal du angive **Ja** i feltet **Kør separat** for den pågældende handling. Såfremt en handling skal påbegyndes i forbindelse med behandlingen af meddelelser eller meddelelseselementer med en status, der er defineret som den indledende status for en handling, skal feltet **Kør separat** angives til **Nej**. Handlinger af typen **Brugerhandling** skal altid køres separat.

Adskillige handlinger skal til tider samles i én serie, selv om den første handling er konfigureret til at køre separat. Eksempelvis når en bruger skal påbegynde rapportgenerering, men umiddelbart efter rapportens dannelse skal sende den til en webtjeneste, og webtjenestens svar skal afspejles i systemet. Du kan i denne situation oprette en uadskillelig sekvens for de handlinger, som altid skal køres sammen. Vælg **Uadskillelige sekvenser** ovenover gitteret i oversigtspanelet for **Handling**, og opret en sekvens. Vælg dernæst sekvensen i feltet **Uadskillelig sekvens** for alle de handlinger, der skal køres sammen. I dette tilfælde kan feltet **Kør separat** angives til **Ja** for den første handling i sekvensen, men til **Nej** for alle de øvrige handlinger.

I oversigtspanelet **Ekstra felter i meddelelseselement** kan du tilføje flere foruddefinerede felter, der vedrører meddelelseselementer. Du skal tilføje flere felter for hver type meddelelseselement, der vedrører felterne.

I oversigtspanelet **Yderligere meddelelsesfelter** kan du tilføje flere foruddefinerede felter, der vedrører meddelelser.

I oversigtspanelet **Sikkerhedsroller** kan du konfigurere de sikkerhedsroller, der er foruddefineret i systemet til bestemte behandling. Brugere, der har en bestemt rolle, ser kun behandling, der er defineret for den pågældende rolle.

I oversigtspanelet **Batch** kan du konfigurere behandlingen, så den kan bruges i en batchordning.

## <a name="work-with-the-electronic-messages-functionality"></a>Arbejde med de elektroniske meddelelsesfunktioner

Hvis du arbejder på meddelelsesniveau, er siden **Elektroniske meddelelser** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elektroniske meddelelser**) mest nyttig. Hvis du arbejder på dataindsamlingsniveau (meddelelseselement), er siden **Elementer i elektronisk meddelelse** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elementer i elektronisk meddelelse**) mest nyttig.

### <a name="electronic-messages"></a>Elektroniske meddelelser

Siden **Elektroniske meddelelser** viser den behandling, der er tilgængelige for dig, afhængigt af din rolle. Sikkerhedsroller knyttes til behandlingen under konfigurationen af behandlingen. For hver behandling, der er tilgængelige for dig, viser siden elektroniske meddelelser og oplysninger, der er knyttet til dem.

I oversigtspanelet **Meddelelser** vises elektroniske meddelelser for den valgte behandling. Du kan, afhængigt af den valgte meddelelses status og den foruddefinerede behandling, køre visse handlinger ved at anvende knapperne over gitteret:

- **Ny** – Denne knap er knyttet til handlinger af typen **Opret meddelelse**.
- **Slet** – Denne knap er tilgængelig, hvis afkrydsningsfeltet **Tillad sletning** er markeret for den aktuelle status for den valgte meddelelse.
- **Indsaml data** – Denne knap er tilknyttet handlinger af typen **Udfyld poster**.
- **Generér rapport** – Denne knap er knyttet til handlinger af typen **Meddelelse om eksport af elektronisk rapportering**.
- **Send rapport** – Denne knap er knyttet til handlinger af typen **Webtjeneste**.
- **Importer svar** – Denne knap er tilknyttet handlinger af typen **Import af elektronisk rapportering**.
- **Opdater status** – Denne knap er knyttet til handlinger af typen **Behandling af bruger på meddelelsesniveau**.
- **Meddelelseselementer** – Åbn siden **Elementer i elektronisk meddelelse**.

I oversigtspanelet **Handlingslog** vises oplysninger om de handlinger, der er udført for den valgte meddelelse. Hvis en handling har medført en fejl, vedhæftes oplysninger om fejlen den tilknyttede linje i gitteret. For at gennemse oplysningerne om fejlen skal du markere linjen i gitteret og dernæst trykke på **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

I oversigtspanelet **Yderligere meddelelsesfelter** vises de ekstra felter, der er defineret for meddelelser i opsætningen af behandlingen. Værdierne i disse ekstra felter vises også.

I oversigtspanelet **Meddelelseselementer** vises alle de meddelelseselementer, der vedrører den valgte meddelelse. Du kan, afhængigt af det valgte meddelelseselements status, køre visse handlinger ved at anvende knapperne over gitteret:

- **Slet** – Denne knap er tilgængelig, hvis afkrydsningsfeltet **Tillad sletning** er markeret for den aktuelle status for det valgte meddelelseselement.
- **Opdater status** – Denne knap er knyttet til handlinger af typen **Brugerbehandling**.
- **Originaldokument** – Åbner en side, som viser det oprindelige dokument for det valgte meddelelseselement.

Alle de rapporter, der allerede er genereret og modtaget for en meddelelse, vedhæftes den pågældende meddelelse. For at gennemse de vedhæftede filer, der er relateret til en meddelelse, skal du vælge meddelelsen og dernæst trykke på **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

![Knappen Vedhæftet fil](media/attachment-icon.png)

Siden **Vedhæftede filer** viser alle de vedhæftede filer, der er relateret til den valgte meddelelse. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

![Knappen Åbn](media/open-button.png)

Du kan ligeledes gennemse de vedhæftede filer, der er relateret til en specifik handling, som tidligere er blevet kørt for en meddelelse. På siden **Elektroniske meddelelser** skal du vælge meddelelsen i oversigtspanelet **Meddelelser**, handlingen i oversigtspanelet **Handlingslog** og dernæst vælge knappen **Vedhæft fil** i øverste højre hjørne af siden.

Du kan også køre enten hele behandlingen eller kun en bestemt handling ved at vælge **Kør behandling** i handlingsruden.

### <a name="electronic-message-items"></a>Elementer i elektronisk meddelelse

Siden **Elementer i elektronisk meddelelse** viser alle meddelelseselementer og en log over de handlinger, der er udført for hvert meddelelseselement. Siden viser også de ekstra felter, der er defineret for meddelelseselementer, og værdierne i disse ekstra felter.

I følgende tabel beskrives felterne under fanen **Meddelelseselementer**.

<table>
<thead>
<tr>
<th>Felt</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Afvikling</td>
<td>Navnet på den behandling, der blev brugt til at oprette meddelelseselementet.</td>
</tr>
<tr>
<td>Meddelelseselement</td>
<td>Id'et for meddelelseselementet. Dette id tildeles automatisk baseret på den <strong>Meddelelseselement</strong>-nummerserie, der er defineret på siden <strong>Finansparametre</strong>.</td>
</tr>
<tr>
<td>Meddelelseselementdato</td>
<td>Den dato, hvor meddelelsen blev oprettet.</td>
</tr>
<tr>
<td>Typen af meddelelseselement</td>
<td>Meddelelseselementtypen. Flere typer meddelelseselementer kan konfigureres til samme behandling (f.eks. <strong>Indgående fakturaer</strong> og <strong>Udgående fakturaer</strong>). Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Status for meddelelseselement</td>
<td>Den faktiske status for meddelelseselementet. De tilgængelige statusser afhænger af typen af meddelelseselement. Her er nogle eksempler:
<ul>
<li><strong>Udfyldt</strong> – Der blev føjet en post til tabellen Meddelelseselement.</li>
<li><strong>Evalueret</strong> – Der blev beregnet yderligere attributter for meddelelseselementet.</li>
<li><strong>Rapporteret</strong> – Meddelelseselementet blev føjet til en rapport.</li>
<li><strong>Udelukket</strong> – Denne status kan være nyttig, hvis du udelader visse meddelelseselementer fra en rapport, før den er eksporteret.</li>
</ul>
</td>
</tr>
<tr>
<td>Overførselsdato</td>
<td>Til behandling, der automatisk sender en rapport, der er oprettet uden for systemet, på den dato, da meddelelseselementet blev sendt.</td>
</tr>
<tr>
<td>Dokumentnummer</td>
<td>Dette felt udfyldes automatisk på grundlag af opsætningen af handlingen Udfyld poster. Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Kontonummeret for en kunde eller leverandør (eller en anden feltværdi afhængigt af det felt, der er defineret i handlingen til at udfylde poster). Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
</tr>
<tr>
<td>Melding</td>
<td>Nummeret på meddelelsen. Dette nummer tildeles automatisk baseret på den <strong>Meddelelse</strong>-nummerserie, der er defineret på siden <strong>Finansparametre</strong>.</td>
</tr>
<tr>
<td>Meddelelsesstatus</td>
<td>Den faktiske status for den elektroniske meddelelse.</td>
</tr>
<tr>
<td>Næste handling</td>
<td>De næste handlinger, der kan påbegyndes for meddelelseselementets aktuelle status.</td>
</tr>
</tbody>
</table>

Fanen **Ekstra felter** viser de ekstra felter for det valgte meddelelseselement og deres værdier.

#### <a name="run-processing"></a>Kør behandling

Vælg **Kør behandling** i handlingsruden for at køre behandlingen af meddelelseselementer. For at køre en bestemt handling skal du i dialogboksen **Kør behandling** vælge **Ja** i indstillingen **Vælg handling** og derefter vælge en handling. For at køre hele behandlingen skal du lade indstillingen **Vælg handling** være angivet til **Nej**.

#### <a name="generate-report"></a>Generér rapport

Vælg **Generér rapport** i handlingsruden for at generere en rapport. Denne knap er knyttet til handlinger af typen **Eksport af elektronisk rapportering**.

#### <a name="update-status"></a>Opdater status

Vælg **Opdater status** i handlingsruden for at opdatere status for en eller flere meddelelseselementer. I dialogboksen **Opdater status** skal du bruge oversigtspanelet **Poster, der skal indgå** til at vælge de meddelelseselementer, der skal opdateres. Sørg for, at du definerer udvælgelseskriterierne korrekt, da meddelelseselementers status opdateres i henhold til disse kriterier, den indledende status for den valgte handling og **Ny status**-værdien, du angiver. Når en statusopdatering er fuldført, vil det være vanskeligt at fastslå, hvilke elementer der er blev opdateret. Det vil derfor være vanskeligt at tilbageføre statusopdateringen.

#### <a name="electronic-messages"></a>Elektroniske meddelelser

Vælg **Elektroniske meddelelser** i handlingsruden for at gennemse en elektronisk meddelelse, der er relateret til det valgte meddelelseselement.

Du kan ligeledes gennemse alle de filer, der er relateret til et specifikt meddelelseselement. Vælg feltet **Meddelelse** for meddelelseselementet, eller vælg **Elektroniske meddelelser** i handlingsruden. Dernæst skal du på siden **Elektronisk meddelelse** vælge den meddelelse, du ønsker at gennemse filer for, og efterfølgende trykke på knappen **Vedhæft fil** (symbolet med en papirklip) i øverste højre hjørne af siden.

![Knappen Vedhæftet fil](media/attachment-icon.png)

Siden **Vedhæftede filer** viser alle vedhæftede filer, der er relateret til meddelelsen. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

![Knappen Åbn](media/open-button.png)

#### <a name="original-document"></a>Originaldokument

Vælg **Originaldokument** i handlingsruden for at åbne det oprindelige dokument for det valgte meddelelseselement.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Eksempel: konfigurer og kør behandling for at kalde et simpelt ER-eksportformat med henblik på at oprette en Excel-rapport

Når du har oprettet ER-formatet, knyttet det til datakilder og fuldført det, kan du køre det ved hjælp af arbejdsområdet **Elektronisk rapportering**. Der genereres en rapport, og du får mulighed for at gemme den lokalt.

Du kan styre følgende aspekter af rapporteringsprocessen ved at konfigurere behandlingen af elektroniske meddelelser:

- Log oplysninger om, hvem der oprettede rapporten.
- Logoplysninger om, hvornår rapporten blev genereret.
- Gem de rapporter, der blev oprettet for tidligere perioder.

Dette afsnit indeholder et eksempel, der viser, hvordan du kan oprette elektroniske meddelelser for at generere en rapport, der er baseret på et ER-eksportformat til Excel. Hvis du ønsker at følge dette eksempel, skal ER-eksportformatet for Excel allerede være oprettet, knyttet til datakilderne og fuldført. Derudover skal der allerede være konfigureret en nummerserie for elektroniske meddelelser.

Når du konfigurerer behandling, er det nyttigt, hvis du først definerer de behandlingshandlinger og statusser, der skal oprettes. I følgende illustration vises, hvordan behandlingen ser ud i dette eksempel.

![Behandlingsskema](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Opret meddelelsesstatusser

1. Gå til **Moms \> Konfiguration \> Elektroniske meddelelser \> Meddelelsesstatusser**.
2. Oprette følgende meddelelsesstatusser:

    - Nyt
    - Forberedt
    - Genereret

    ![Meddelelsesstatusser](media/message-statuses.png)

3. På linjen for den **Ny** status, skal du markere afkrydsningsfeltet **Tillad sletning** for at tillade, at brugere sletter meddelelser med denne status.

#### <a name="create-additional-fields"></a>Oprette flere felter

1. Gå til **Moms \> Konfiguration \> Elektroniske meddelelser \> Ekstra felter**.
2. Tilføj et ekstra felt og de tilhørende værdier. Her er et eksempel.

    ![Ekstra felter](media/additional-fields.png)

3. Vælg **Ja** i indstillingen **Brugerredigering**, så brugerne kan redigere feltet.

#### <a name="create-message-processing-actions"></a>Oprette handlinger til meddelelsesbehandling

I dette eksempel skal du oprette følgende handlinger:

- **Opret meddelelse**
- **Opdater til Forberedt**
- **Generér rapport**
- **Opdater til første status** (valgfrit)

1. Gå til **Moms \> Konfiguration \> Elektroniske meddelelser \> Handlinger ved meddelelsesbehandling**.
2. Opret en handling, der hedder **Opret meddelelse**. I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Opret meddelelse**.
3. Opret en handling, der hedder **Opdater til Forberedt**, og indstil følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Behandling af bruger på meddelelsesniveau**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Ny**.
    - I oversigtspanelet **Resultatstatusser** skal du i feltet **Meddelelsesstatus** vælge **Forberedt**. I feltet **Svartype** skal du angive **Udført korrekt**.

4. Opret en handling, der hedder **Generér rapport**, og indstil følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Eksport af elektronisk rapportering**. I feltet **Formattilknytning** skal du vælge ER-formatet til eksport. De tilgængelige indstillinger er **Excel**, **XML**, **JSON**, **Tekst** og **Andet**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Forberedt**.
    - I oversigtspanelet **Resultatstatusser** skal du i feltet **Meddelelsesstatus** vælge **Genereret**. I feltet **Svartype** skal du angive **Udført korrekt**.

    ![Handlingen Generér rapport](media/generate-report-action.png)

5. Valgfrit: Du kan lade brugerne generere en rapport flere gange ved at oprette en **Opdater til første status**-handling og angive følgende felter:

    - I oversigtspanelet **Generelt** skal du i feltet **Handlingstype** vælge **Behandling af bruger på meddelelsesniveau**.
    - I oversigtspanelet **Første statusser** skal du i feltet **Meddelelsesstatus** vælge **Genereret**.
    - I oversigtspanelet **Resultatstatusser** skal du tilføje en separat linje for hver af de to meddelelsesstatusser (**Forberedt** og **Ny**). Angiv feltet **Svartype** til **Udført korrekt** for begge linjer.

#### <a name="electronic-message-processing"></a>Behandling af elektronisk meddelelse

I dette eksempel skal alle handlingerne være konfigureret, så de kører separat. Det antages, at brugeren påbegynder hver handling.

1. Gå til **Moms \> Konfiguration \> Elektroniske meddelelser \> Behandling af elektronisk meddelelse**.
2. Føj en post til din behandling, og tilføj alle tidligere definerede handlinger og et ekstra felt.
3. Valgfrit: i oversigtspanelet **Sikkerhedsroller** skal du definere sikkerhedsrollerne for din behandling for derved at begrænse adgangen til specifikke rapporter.
4. Gå til **Moms \> Forespørgsler og rapporter \> Elektroniske meddelelser \> Elektroniske meddelelser**.
5. Vælg **Ny** for at oprette en meddelelse. På dette tidspunkt kan du tilføje datoer og en beskrivelse. Du kan også opdatere værdien af det ekstra felt efter behov.

    ![Oprette en elektronisk meddelelse](media/create-electronic-message.png)

Gitteret i oversigtspanelet **Handlingslog** udfyldes automatisk med en log over alle handlinger, der udføres på meddelelsen.

Du kan nu enten slette eller opdatere meddelelsesstatus. Vælg **Opdater status** for at opdatere meddelelsens status. I feltet **Ny status** skal du vælge **Forberedt** og dernæst vælge **OK**.

![Opdatere meddelelsens status](media/update-status.png)

Meddelelsesstatussen opdateres til **Forberedt**, og du kan nu generere rapporten ved at vælge **Generér rapport**. Rapporten oprettes, og meddelelsesstatus og handlingsloggen opdateres. For at gennemse den genererede rapport skal du trykke på knappen **Vedhæft fil** (symbolet med papirklip) i øverste højre hjørne af siden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]