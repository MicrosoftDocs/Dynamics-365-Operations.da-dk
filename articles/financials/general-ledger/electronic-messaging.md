---
title: Elektroniske meddelelser
description: Dette emne indeholder oversigts- og konfigurationsoplysninger for elektroniske meddelelser i Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 232398a6c4193d0074881e26fff361deb9784bf2
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="electronic-messaging"></a>Elektroniske meddelelser

[!include [banner](../includes/banner.md)]

Dette emne indeholder oversigts- og konfigurationsoplysninger for elektroniske meddelelser i Microsoft Dynamics 365 for Finance and Operations.

Offentlige myndigheder og lovgivende forsamlinger i forskellige lande og områder i hele verden har for nylig implementeret krav til rapportering for virksomheder, der er registreret i disse lande eller områder. Formålet med kravene er at gøre det muligt at få data fra disse virksomheder i elektronisk format direkte fra de systemer, hvor de er blevet bogført, gemt og behandlet.

Den elektroniske meddelelsesfunktion i Finance and Operations understøtter forskellige elektroniske kommunikationsprocesser mellem Finance and Operations, og de systemer, som offentlige myndigheder tilbyder til rapportering, afsendelse og modtagelse af officielle oplysninger.

Den elektroniske meddelelsesfunktion er integreret i modulet **Elektronisk rapportering** (Electronic Reporting – ER). Derfor kan du konfigurere ER-formater til elektroniske meddelelser. Du kan finde flere oplysninger under [Elektronisk rapportering (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektroniske meddelelser er baseret på følgende enheder:

- **Elektronisk meddelelse** – En rapport eller erklæring, der skal rapporteres og/eller overføres internt. Et eksempel er en rapport, der sendes til et skattekontor.
- **Elektroniske meddelelseselementer** – Poster, der skal medtages i den meddelelse, der rapporteres.
- **Behandling af elektronisk meddelelse** – En kæde af handlinger, enten tilknyttede eller ikke-tilknyttede, der skal køres for at indsamle de nødvendige data, generere rapporter, gemme data i Microsoft Azure Blob-lageret, sende rapporter uden for systemet, modtage svar, der ikke kommer fra systemet, og opdatere databasen ud fra de oplysninger, der er modtaget.

I følgende illustration vises en række data til elektroniske meddelelser.

![Dataflow for elektroniske meddelelser](media/electronic-messaging-data-flow.png)

Den elektroniske meddelelsesfunktion understøtter følgende scenarier:

- Manuel oprettelse af meddelelser og generering af rapporter, der er baseret på tilknyttede ER-formater til eksport af forskellige typer: Microsoft Excel, XML, JSON (JavaScript Object Notation), PDF, tekst og Microsoft Word.
- Automatisk oprettelse og behandling af meddelelser, der er baseret på oplysninger, der blev anmodet om og tilsendt fra en myndighed via et tilknyttet ER-format til import.
- Indsamling og behandling af oplysninger fra en datakilde (Finance and Operations-tabel) som meddelelseselementer.
- Lagring af flere oplysninger og evaluering af forskellige værdier ved at kalde specifikt definerede eksekverbare klasser i forhold til meddelelser eller meddelelseselementer.
- Aggregering af oplysninger, der er indsamlet i meddelelseselementer, opdeling af disse oplysninger efter meddelelse og generering af rapporter, der er i tilknyttede ER-eksportformater.
- Afsendelse af rapporter, der er oprettet til en webtjeneste ved hjælp af sikkerhedsoplysninger, der er gemt i Azure Key Vault.
- Få svar fra en webtjeneste, fortolke svaret og opdatere data i Finance and Operations efter behov.
- Lagring og gennemgang de rapporter, der genereres.
- Lagring og gennemgang af alle logoplysninger, der er knyttet til handlinger, der køres for en meddelelse eller et meddelelseselement.
- Styring af behandlingen via forskellige meddelelsesstatusser og meddelelseselementstatusser.

## <a name="set-up-electronic-messaging"></a>Konfigurere elektroniske meddelelser

Elektroniske meddelelser kan hjælpe dig med at vedligeholde forskellige elektroniske rapporteringsprocesser for forskellige dokumenttyper. Elektroniske meddelelser er i visse komplekse scenarier konfigureret til at have en kombination af mange meddelelsesstatusser, meddelelseselementstatusser, handlinger, yderligere felter og eksekverbar klasser. Der findes pakker med dataenheder til import i disse scenarier. Hvis du bruger disse dataenhedspakker, skal du importere dem til en juridisk enhed ved hjælp af datastyringsværktøjet. Du kan finde flere oplysninger om, hvordan du bruger af datastyringsværktøjet, i [Datastyring](../../dev-itpro/data-entities/data-entities-data-packages.md).

Hvis du ikke importerer en dataenhedspakke, kan du manuelt konfigurere den elektroniske meddelelsesfunktion. I dette tilfælde skal du definere følgende elementer: 

- [Nummerserier](#number-sequences)
- [Meddelelseselementtyper og -statusser](#message-item-types-and-statuses)
- [Meddelelsesstatusser](#message-statuses)
- [Ekstra felter](#additional-fields)
- [Indstillinger for eksekverbar klasse](#executable-class-settings)
- [Handlingerne Udfyld poster](#populate-records-actions)
- [Indstillinger for webtjeneste](#web-service-settings)
- [Handlinger ved meddelelsesbehandling](#message-processing-actions)
- [Behandling af elektronisk meddelelse](#electronic-message-processing)

Nedenstående afsnit indeholder flere oplysninger om hvert af disse elementer.

### <a name="number-sequences"></a>Nummerserier

Konfigurer nummerserier for både meddelelser og meddelelseselementer. Nummerserierne bruges til automatisk nummerering af meddelelserne og meddelelseselementerne, og de numre, der tildeles, bruges som entydige id'er for meddelelserne og meddelelseselementerne i systemet. Du kan oprette nummerserier til elektroniske meddelelser på siden **Finansparametre** (**Finans** \> **Opsætning Finans** \> **Finansparametre**).

### <a name="message-item-types-and-statuses"></a>Meddelelseselementtyper og -statusser

Meddelelseselementtyper identificerer typerne af poster, der skal bruges i elektroniske meddelelser. Du kan konfigurere meddelelseselementtyper på siden **Typer af meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Typer af meddelelseselement**).

Meddelelseselementstatusser identificere de statusser, der gælder for meddelelseselementer i behandlingen, som du konfigurerer. Du kan konfigurere meddelelseselementtyper på siden **Statusser for meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Statusser for meddelelseselement**).

### <a name="message-statuses"></a>Meddelelsesstatusser

Konfigurer de meddelelsesstatusser, der skal være tilgængelige i behandling af meddelelser. Du kan konfigurere meddelelsesstatusser på siden **Meddelelsesstatusser** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Meddelelsesstatusser**).

### <a name="additional-fields"></a>Ekstra felter

Med den elektroniske meddelelsesfunktion kan du udfylde poster fra en posteringstabel. På denne måde kan du opstille posterne til rapportering og derefter rapportere dem. Nogle gange er der ikke tilstrækkelige oplysninger i posteringstabellen til at rapportere en post i overensstemmelse med rapporteringskravene. Du kan angive alle de oplysninger, der skal rapporteres for en post, ved at oprette flere felter. Der kan knyttes flere felter til både meddelelser og meddelelser. Du kan oprette flere felter på siden **Ekstra felter** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Ekstra felter**).

I følgende tabel beskrives felterne på siden **Ekstra felter**.

| Felt                | Betegnelse |
|----------------------|-------------|
| Feltnavn           | Angiv navnet på en ekstra attribut for meddelelseselementer, der vedrører processen. Dette navn vises i brugergrænsefladen, mens du arbejder med processen. Det kan også bruges i ER-konfigurationer, der er knyttet til processen. |
| Betegnelse          | Angiv en beskrivelse på den ekstra attribut for meddelelseselementer, der vedrører processen. |
| Feltværdi          | Angiv den værdi i feltet, der skal bruges i forhold til et meddelelseselement under rapportering. |
| Beskrivelse af felt    | Angiv en beskrivelse af feltet, der skal bruges i forhold til et meddelelseselement under rapportering. |
| Kontotype         | Nogle ekstra feltværdier kan være begrænset til bestemte kontotyper. Vælg en eller flere af følgende værdier: **Alle**, **Debitor** eller **Kreditor**. |
| Kontokode         | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, kan du yderligere begrænse brugen af feltværdier til en bestemt gruppe eller tabel. |
| Konto/gruppenummer | Hvis du har valgt **Debitor** eller **Kreditor** i feltet **Kontotype**, og hvis du har angivet en gruppe eller en tabel i feltet **Kontokode**, kan du angive en bestemt gruppe eller modpostering i dette felt. |
| Gyldig            | Angiv den dato, hvor værdien skal begynde at blive taget i betragtning. |
| Udløb           | Angiv den dato, hvor værdien ikke længere skal tages i betragtning. |

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

### <a name="populate-records-actions"></a>Handlingerne Udfyld poster

Du bruger handlinger til udfyldelse af poster til at konfigurere handlinger, der tilføjer poster til tabellen Meddelelseselementer, så de kan føjes til en elektronisk meddelelse. Hvis for eksempel den elektroniske meddelelse skal rapportere debitorfakturaer, skal du konfigurere en **Udfyld poster**-handling, der er kædet sammen i tabellen **Debitorfakturajournal** (i feltet **Datakilde**). Du kan konfigurere handlinger til udfyldelse af poster på siden **Handlingen Udfyld poster** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Handlingen Udfyld poster**). Opret en ny post for hver handling, der skal føje poster til tabellen, og angiv følgende felter.

| Felt       | Betegnelse                                                               |
|-------------|---------------------------------------------------------------------------|
| Navn        | Angiv et navn til den handling, der udfylder poster i processen.       |
| Betegnelse | Angiv en beskrivelse af den handling, der udfylder poster i processen. |

I oversigtspanelet **Opsætning af datakilder** skal du tilføje en linje for hver datakilde, der bruges til processen, og angive følgende felter.

| Felt                  | Betegnelse |
|------------------------|-------------|
| Navn                   | Angiv et navn til datakilden. |
| Typen af meddelelseselement      | Vælg den type meddelelseselement, der skal bruges, når der oprettes poster til datakilden. |
| Kontotype           | Vælg den type konto, der skal knyttes til poster fra datakilden. |
| Navn på overordnet tabel      | Vælg den tabel i Finance and Operations, der skal være en datakilde. |
| Feltet dokumentnummer  | Vælg det felt, som dokumentnummeret skal tages fra i den valgte tabel. |
| Feltet Dokumentdato    | Vælg det felt, som dokumentets dato skal tages fra i den valgte tabel. |
| Feltet Dokumentkonto | Vælg det felt, som dokumentkontoen skal tages fra i den valgte tabel. |
| Brugerforespørgsel             | Hvis dette afkrydsningsfelt er markeret, kan du oprette en forespørgsel ved at vælge **Rediger forespørgsel** over gitteret. Ellers udfyldes alle posterne fra datakilden. |

### <a name="web-service-settings"></a>Indstillinger for webtjeneste

Du kan bruge indstillingerne for webtjeneste til at konfigurere overførsel af direkte data til en webtjeneste. Du kan konfigurere indstillinger for webtjenesten på siden **Indstillinger for webtjeneste** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Indstillinger for webtjeneste**) .

I følgende tabel beskrives felterne på siden **Indstillinger for webtjeneste**.

| Felt                   | Betegnelse |
|-------------------------|-------------|
| Webtjeneste             | Angiv et navn til webtjenesten. |
| Betegnelse             | Angiv en beskrivelse af webtjenesten. |
| Internetadresse        | Angiv internetadressen på webtjenesten. |
| Certifikat             | Vælg et Key Vault-certifikat, der tidligere er konfigureret. |
| Svartypen – XML | Vælg **Ja** i denne indstilling, hvis svartypen er XML. |
| Anmodningsmetode          | Angiv metoden for anmodningen. HTTP definerer et sæt anmodningsmetoder, der angiver den handling, der skal udføres for en bestemt ressource. Metoden kan være **GET**, **POST** eller en anden HTTP-metode. |
| Headers til anmodninger         | Angiv headers til anmodninger. En anmodningsheader er en HTTP-header, der kan bruges i en HTTP-anmodning, og som ikke er relateret til indholdet af meddelelsen. |
| Kodning af accept         | Angiv kodning af accept. HTTP-headeren til acceptkodningsanmodningen annoncerer den indholdskodning, som klienten kan forstå. Denne kodning af indhold er normalt en komprimeringsalgoritme. |
| Indholdstype            | Angiv indholdstypen. Headeren til Content-Type-enheden angiver medietypen for ressourcen. |

### <a name="message-processing-actions"></a>Handlinger ved meddelelsesbehandling

Du skal bruge handlinger til behandling af meddelelsen til at oprette aktioner til dine processer og definere deres parametre. Du kan konfigurere handlinger til behandling af meddelelsen på siden **Statusser for meddelelseselement** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Handlinger ved meddelelsesbehandling**).

I følgende tabel beskrives felterne på siden **Handlinger ved meddelelsesbehandling**.

#### <a name="general-fasttab"></a>Oversigtspanelet Generelt

| Felt                   | Betegnelse |
|-------------------------|-------------|
| Aktionstype             | Vælg handlingstypen. Du kan finde oplysninger om de tilgængelige indstillinger i sektionen [Typer af handlinger til behandling af meddelelser](#message-processing-action-types). |
| Formattilknytning          | Vælg det ER-format, der skal kaldes for handlingen. Dette felt er kun tilgængeligt for handlinger af typerne **Eksport af elektronisk rapportering**, **Import af elektronisk rapportering** og **Meddelelse om eksport af elektronisk rapportering**. |
| Typen af meddelelseselement       | Vælg den type poster, som handlingen skal evalueres for. Dette felt er tilgængeligt for handlinger af typerne **Udførelsesniveau for meddelelseselement**, **Eksport af elektronisk rapportering** og **Import af elektronisk rapportering** og også visse andre typer. Hvis du lader feltet stå tomt, evalueres alle de meddelelseselementtyper, som er defineret for behandlingen af meddelelser. |
| Eksekverbar klasse        | Vælg de eksekverbare klasseindstillinger, der tidligere blev oprettet. Dette felt er kun tilgængeligt for handlinger af typen **Udførelsesniveau for meddelelseselement** og **Udførelsesniveau for meddelelseselement**. |
| Handlingen Udfyld poster | Vælg en Udfyld poster-handling, der tidligere blev oprettet. Dette felt er kun tilgængeligt for handlinger af typen **Udfyld poster**. |

##### <a name="message-processing-action-types"></a>Typer af handlinger til behandling af meddelelser

Følgende indstillinger er tilgængelige i feltet **Handlingstype**:

- **Udfyld poster** – En **Udfyld posterne**-handling skal være konfigureret tidligere. Knyt den til en handling af typen **Udfyld poster**, så den kan indgå i behandlingen. Det forudsættes, at denne handlingstype bruges til den første handling i behandling af meddelelser. Derfor er det kun en resultatstatus, der kan konfigureres for en handling af denne type. Der kan ikke oprettes en førstestatus.
- **Opret meddelelse** – Brug denne type, hvis brugerne manuelt skal kunne oprette meddelelser på siden **Elektronisk meddelelse**. Der kan ikke konfigureres en førstestatus for en handling af denne type.
- **Udførelsesniveau for meddelelse** – Brug denne type til at konfigurere en eksekverbar klasse, der skal evalueres på niveauet for meddelelsen.
- **Udførelsesniveau for meddelelseselement** – Brug denne type til at konfigurere en eksekverbar klasse, der skal evalueres på niveauet for meddelelseselementet.
- **Eksport af elektronisk rapportering** – Brug denne type til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport, på niveauet for meddelelseselementet.
- **Meddelelse om eksport af elektronisk rapportering** – Brug denne type til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til eksport, på niveauet for meddelelsen (for eksempel, når en meddelelse ikke har nogen meddelelseselementer).
- **Import af elektronisk rapportering** – Brug denne type til handlinger, der skal generere en rapport, som er baseret på en ER-konfiguration til import.
- **Behandling af bruger på meddelelsesniveau** – Brug denne type til handlinger, der forudsætter visse handlinger, der udføres manuelt af brugeren. For eksempel kan brugeren opdatere status for meddelelser.
- **Brugerbehandling** – Brug denne type til handlinger, der forudsætter handling, der udføres manuelt af brugeren. For eksempel kan brugeren opdatere status for meddelelseselementer.
- **Webtjeneste** – Brug denne type til handlinger, der skal overføre en rapport, der er genereret, til en webtjeneste. Denne handlingstype bruges ikke til rapportering af kommunikation vedr. italienske købs- og salgsfakturaer.
- **Anmodningsbekræftelse** – Brug denne type til at anmode om bekræftelse fra en server.

#### <a name="initial-statuses-fasttab"></a>Oversigtspanelet Førstestatusser

> [!NOTE]
> Oversigtspanelet **Første statusser** er ikke tilgængeligt for handlinger, der har første-typen **Udfyld poster** eller **Opret meddelelse**.

| Felt               | Betegnelse                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Status for meddelelseselement | Vælg den meddelelseselementsstatus, som skal den valgte handling til behandling af meddelelsen, skal evalueres for. |
| Betegnelse         | Beskrivelse af det valgte meddelelseselements status.                                                  |

#### <a name="result-statuses-fasttab"></a>Oversigtspanelet Resultatstatusser

| Felt               | Betegnelse |
|---------------------|-------------|
| Meddelelsesstatus      | Vælg den meddelelsesstatus, som skal den valgte handling til behandling af meddelelsen, skal evalueres for. Dette felt er kun tilgængeligt for handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelsen. F.eks. er det tilgængeligt for handlinger af typerne **Eksport af elektronisk rapportering** og **Import af elektronisk rapportering**. Det er ikke tilgængeligt for handlinger af typen **Brugerbehandling** og **Udførelsesniveau for meddelelseselement**. |
| Betegnelse         | Beskrivelse af den valgte meddelelses status. |
| Svartype       | Svartypen for den valgte meddelelses status. |
| Status for meddelelseselement | Vælg den resultatstatus, som skal være tilgængelig, efter at den valgte handling til behandling af meddelelsen er evalueret. Dette felt er kun tilgængeligt for handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelseselementet. Det er f.eks. ikke tilgængeligt for handlinger af typen **Brugerbehandling** og **Udførelsesniveau for meddelelseselement**. I forbindelse med handlinger til behandling af meddelelser, der evalueres på niveauet for meddelelsen, viser dette felt den meddelelseselementstatus, der er angivet for den valgte meddelelsesstatus. |

### <a name="electronic-message-processing"></a>Behandling af elektronisk meddelelse

Elektronisk meddelelsesbehandling er et grundlæggende begreb i forbindelse med den elektroniske meddelelsesfunktion. Det samler handlinger, der skal evalueres for den elektroniske meddelelse. Handlingerne kan tilknyttes via førstestatus og resultatstatus. Du kan også starte handlinger af typen **Brugerbehandling** særskilt. På siden **Behandling af elektronisk meddelelse** (**Moms** \> **Konfiguration** \> **Elektroniske meddelelser** \> **Behandling af elektronisk meddelelse**), kan du også vælge flere felter, der skal understøttes under behandlingen.

I oversigtspanelet **Handling** kan du føje foruddefinerede handlinger til behandling. Du kan angive, om en handling skal foretages separat, eller om den kan påbegyndes af behandlingen. (Brugerhandlinger skal køres separat).

I oversigtspanelet **Ekstra felter i meddelelseselement** kan du tilføje flere foruddefinerede felter, der vedrører meddelelseselementer. Du skal tilføje flere felter for hver type meddelelseselement, der vedrører felterne.

I oversigtspanelet **Yderligere meddelelsesfelter** kan du tilføje flere foruddefinerede felter, der vedrører meddelelser.

I oversigtspanelet **Sikkerhedsroller** kan du konfigurere de sikkerhedsroller, der er foruddefineret i systemet til bestemte behandling. Brugere, der har en bestemt rolle, ser kun behandling, der er defineret for den pågældende rolle.

I oversigtspanelet **Batch** kan du konfigurere behandlingen, så den kan bruges i en batchordning.

## <a name="work-with-electronic-messages-functionality"></a>Arbejde med elektroniske meddelelsesfunktioner

Hvis du arbejder på meddelelsesniveau, er siden **Elektroniske meddelelser** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elektroniske meddelelser**) mest nyttig. Hvis du arbejder på dataindsamlingsniveau (meddelelseselement), er siden **Elementer i elektronisk meddelelse** (**Moms** \> **Forespørgsler og rapporter** \> **Elektroniske meddelelser** \> **Elementer i elektronisk meddelelse**) mest nyttig.

### <a name="electronic-messages"></a>Elektroniske meddelelser

Siden **Elektroniske meddelelser** viser den behandling, der er tilgængelige for dig, afhængigt af din rolle. Sikkerhedsroller knyttes til behandlingen under konfigurationen af behandlingen. For hver behandling, der er tilgængelige for dig, viser siden elektroniske meddelelser og oplysninger, der er knyttet til dem.

I oversigtspanelet **Meddelelser** vises elektroniske meddelelser for den valgte behandling. Afhængigt af status for den valgte meddelelse og foruddefinerede behandling kan du køre bestemte handlinger ved at vælge knapperne over gitteret:

- **Ny** – Denne knap er knyttet til handlinger af typen **Opret meddelelse**.
- **Slet** – Denne knap er tilgængelig, hvis afkrydsningsfeltet **Tillad sletning** er markeret for den aktuelle status for den valgte meddelelse.
- **Generér rapport** – Denne knap er knyttet til handlinger af typen **Meddelelse om eksport af elektronisk rapportering**.
- **Send rapport** – Denne knap er knyttet til handlinger af typen **Webtjeneste**.
- **Opdater status** – Denne knap er knyttet til handlinger af typen **Behandling af bruger på meddelelsesniveau**.
- **Meddelelseselementer** – Åbn siden **Elementer i elektronisk meddelelse**.

I oversigtspanelet **Handlingslog** vises oplysninger om de handlinger, der er udført for den valgte meddelelse.

I oversigtspanelet **Yderligere meddelelsesfelter** vises de ekstra felter, der er defineret for meddelelser i opsætningen af behandlingen. Værdierne i disse ekstra felter vises også.

I oversigtspanelet **Meddelelseselementer** vises alle de meddelelseselementer, der vedrører den valgte meddelelse.

Du kan gennemse alle vedhæftede filer for den valgte meddelelse. Disse vedhæftede filer er rapporter, der allerede er oprettet og modtaget. Vælg den meddelelse, du vil gennemse vedhæftede filer i, og vælg derefter knappen **Vedhæftet fil** i handlingsruden.

![Knappen Vedhæftet fil](media/attachment-icon.png)

Siden **Vedhæftede filer** viser alle vedhæftede filer, der er relateret til meddelelsen. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

![Knappen Åbn](media/open-button.png)

For at få vist en vedhæftet fil, der er knyttet til en bestemt handling, der tidligere blev kørt for en meddelelse, skal du vælge meddelelsen på siden **Elektroniske meddelelser** og derefter vælge handlingen i oversigtspanelet **Handlingslog**. Vælg derefter knappen **Vedhæftet fil** i handlingsruden.

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
<td>Kontonummeret for en kunde eller leverandør (eller en anden feltværdi, afhængigt af det felt, der er defineret i handlingen <strong>Udfyld poster</strong>). Dette felt kan kun udfyldes automatisk, når en faktura føjes til tabellen Meddelelseselementer.</td>
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
<td>De næste handlinger, der kan startes med den aktuelle status for meddelelseselementet.</td>
</tr>
</tbody>
</table>

Fanen **Ekstra felter** viser de ekstra felter for det valgte meddelelseselement og deres værdier.

#### <a name="run-processing"></a>Kør behandling

Vælg **Kør behandling** i handlingsruden for at køre behandlingen af meddelelseselementer. For at køre en bestemt handling skal du i dialogboksen **Kør behandling** vælge **Ja** i indstillingen **Vælg handling** og derefter vælge en handling. For at køre hele behandlingen skal du lade indstillingen **Vælg handling** være angivet til **Nej**.

#### <a name="generate-report"></a>Generér rapport

Vælg **Generér rapport** i handlingsruden for at generere en rapport. Denne knap er knyttet til handlinger af typen **Eksport af elektronisk rapportering**.

#### <a name="update-status"></a>Opdater status

Vælg **Opdater status** i handlingsruden for at opdatere status for en eller flere meddelelseselementer. I dialogboksen **Opdater status** skal du bruge oversigtspanelet **Poster, der skal indgå** til at vælge meddelelseselementer til opdatering. Sørg for, at du definerer udvælgelseskriterierne korrekt, fordi meddelelseselementers status opdateres i overensstemmelse med disse kriterier, førstestatus for den valgte handling og den **Ny status**-værdi, du angiver. Når en statusopdatering er fuldført, er det vanskeligt at bestemme, hvilke elementer der lige er blevet opdateret. Derfor vil det være vanskeligt at tilbageføre statusopdateringer.

#### <a name="electronic-messages"></a>Elektroniske meddelelser

Vælg **Elektronisk meddelelse** i handlingsruden for at gennemse en elektronisk meddelelse, der er relateret til det valgte meddelelseselement.

Du kan også gennemse de filer, der svarer til meddelelseselementet. Vælg feltet **Meddelelse** i meddelelseselementet, eller vælg **Elektronisk meddelelse** i handlingsruden. På siden **Elektronisk meddelelse** skal du vælge den meddelelse, du vil gennemse en rapport for, og derefter vælge knappen **Vedhæftet fil** i handlingsruden.

![Knappen Vedhæftet fil](media/attachment-icon.png)

Siden **Vedhæftede filer** viser alle vedhæftede filer, der er relateret til meddelelsen. For at få vist en fil skal du vælge den på listen til venstre og derefter vælge **Åbn** i handlingsruden.

![Knappen Åbn](media/open-button.png)

#### <a name="original-document"></a>Originaldokument

Vælg **Originaldokument** i handlingsruden for at åbne det oprindelige dokument for det valgte meddelelseselement.

## <a name="example"></a>Eksempel

Når du har oprettet ER-formatet, knyttet det til datakilder og fuldført det, kan du køre det ved hjælp af arbejdsområdet **Elektronisk rapportering**. Der genereres en rapport, som du kan gemme lokalt.

Du kan styre følgende aspekter af rapporteringsprocessen ved at konfigurere behandlingen af elektroniske meddelelser:

- Log oplysninger om, hvem der oprettede rapporten.
- Log, hvornår rapporten blev oprettet.
- Gem de rapporter, der blev oprettet for tidligere perioder.

Dette afsnit indeholder et eksempel, der viser, hvordan du kan oprette den elektroniske meddelelsesfunktionen for at opbygge en rapporteringsproces.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Opret og kør behandling for at kalde et simpelt ER-eksportformat for at oprette en Excel-rapport

Dette afsnit indeholder et eksempel, der viser, hvordan du kan oprette elektroniske meddelelser for at generere en rapport, der er baseret på et ER-eksportformat til Excel. For at følge dette eksempel skal ER Excel-eksportformatet allerede være oprettet, knyttes til datakilder og fuldført. En nummerserie skal i forvejen være konfigureret til elektroniske meddelelser.

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
    - I oversigtspanelet **Resultatstatusser** skal du i feltet **Meddelelsesstatus** vælge **Forberedt** eller (og) **Ny**. I feltet **Svartype** skal du angive **Udført korrekt**.

#### <a name="electronic-message-processing"></a>Behandling af elektronisk meddelelse

I dette eksempel skal alle handlingerne være konfigureret, så de kører separat. Det antages, at hver handling initialiseres af brugeren.

1. Gå til **Moms \> Konfiguration \> Elektroniske meddelelser \> Behandling af elektronisk meddelelse**.
2. Føj en post til din behandling, og tilføj alle tidligere definerede handlinger og et ekstra felt.
3. Valgfrit: I oversigtspanelet **Sikkerhedsroller** skal du definere sikkerhedsroller, så behandlingen begrænser adgangen til bestemt rapportering.
4. Gå til **Moms \> Forespørgsler og rapporter \> Elektroniske meddelelser \> Elektroniske meddelelser**.
5. Vælg **Ny** for at oprette en meddelelse. På dette tidspunkt kan du tilføje datoer og en beskrivelse. Du kan også opdatere værdien af det ekstra felt efter behov.

    ![Oprette en elektronisk meddelelse](media/create-electronic-message.png)

Gitteret i oversigtspanelet **Handlingslog** udfyldes automatisk med en log over alle handlinger, der udføres på meddelelsen.

Du kan nu enten slette eller opdatere meddelelsesstatus. For at opdatere meddelelsesstatussen skal du vælge **Opdater status** og derefter i feltet **Ny status** vælge **Forberedt**. Vælg derefter **OK**.

![Opdatere meddelelsens status](media/update-status.png)

Meddelelsesstatussen opdateres til **Forberedt**, og du kan nu generere rapporten ved at vælge **Generér rapport**. Rapporten oprettes, og meddelelsesstatus og handlingsloggen opdateres. For at få vist den genererede rapport skal du vælge knappen **Vedhæftet fil** i handlingsruden.

