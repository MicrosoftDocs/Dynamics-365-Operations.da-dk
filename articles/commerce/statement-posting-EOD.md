---
title: Forbedringer til funktioner til bogføring af opgørelse
description: I dette emne beskrives de forbedringer, der er foretaget af funktionen til bogføring af opgørelsen.
author: josaw1
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7e9f41a65ca092606e79d5aaa4e3af0ec444604f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795303"
---
# <a name="improvements-to-statement-posting-functionality"></a>Forbedringer til funktioner til bogføring af opgørelse

[!include [banner](includes/banner.md)]

I dette emne beskrives det første sæt af forbedringer, der er foretaget af funktionen til bogføring af opgørelsen. Disse forbedringer er tilgængelige i Microsoft Dynamics 365 for Finance and Operations 7.3.2.

## <a name="activation"></a>Aktivering

Som standard under installationen af Finance and Operations 7.3.2 konfigureres programmet til at bruge den tidligere funktion til bogføring af opgørelser. Hvis du vil aktivere den forbedrede funktionen til bogføring af opgørelsen, skal du aktivere konfigurationsnøglen til den.

- Gå til **Systemadministration** \> **Opsætning** \> **Licenskonfiguration**, og ryd derefter afkrydsningsfeltet **Opgørelser (ældre)** under noden **Retail og Commerce**, og markér afkrydsningsfeltet **Opgørelser**.

Når den nye konfigurationsnøgle **Opgørelser** er aktiveret, bliver et nyt menupunkt, **Opgørelser**, tilgængeligt. I dette menupunkt kan du manuelt kan oprette, beregne og bogføre opgørelser. Enhver opgørelse, der medfører en fejl, når batchposteringsprocessen bruges, vil også være tilgængelig via dette menupunkt. (Når den nye konfigurationsnøgle **Opgørelser (ældre)** aktiveres, får menupunktet navnet **Åbne opgørelser**.)

Commerce indeholder følgende valideringer, der vedrører disse konfigurationsnøgler:

- Begge konfigurationsnøgler kan ikke aktiveres på samme tid.
- De samme konfigurationsnøgler skal bruges til alle de operationer, der udføres på en given opgørelse i dens livscyklus (oprette, beregne, fjerne, bogføre osv). Du kan f.eks. ikke oprette og beregne en opgørelse, mens konfigurationsnøglen **Opgørelser (ældre)** er slået til, og derefter prøve at bogføre den samme opgørelse, mens konfigurationsnøglen **Opgørelse** er slået til.

> [!NOTE]
> Det anbefales, at du bruger konfigurationsnøglen **Opgørelser** til den forbedrede funktion til bogføring af opgørelsen, medmindre der er tvingende årsager til at bruge konfigurationsnøglen **Opgørelser (ældre)** i stedet. Microsoft fortsætter med at investere i den nye og forbedrede bogføringsfunktion, og det er vigtigt, at du hurtigst muligt skifter til den for at få fordel af den. Den ældre opgørelsesbogføringsfunktion er blevet udfaset fra og med version 8.0.

## <a name="setup"></a>Konfiguration

Som en del af forbedringerne af funktionen til bogføring af opgørelser er der introduceret tre nye parametre i oversigtspanelet **Opgørelse** under fanen **Bogføring** på siden **Commerce-parametre**:

- **Deaktiver rydning af opgørelse** – Denne indstilling gælder kun for den ældre funktionen til bogføring af opgørelser. Vi anbefaler, at du vælger **Nej** i denne indstilling for at forhindre, at brugere fjerner opgørelser, der er delvist bogført. Hvis opgørelser, der er delvist bogførte, fjernes, beskadiges dataene. Du skal kun vælge **Ja** i denne indstilling under ekstraordinære omstændigheder.
- **Reservér lager under beregning** – Vi anbefaler, at du bruger batchjobbet **Bogfør lager** til lagerreservation, og at du vælger **Nej** i denne indstilling. Når denne indstilling er sat til **Nej**, forsøger den forbedrede bogføringsfunktion ikke at oprette lagerreservationsposteringer på tidspunktet for beregningen (hvis posteringerne ikke allerede er oprettet via batchjobbet **Bogfør lager**). I stedet opretter funktionen kun lagerreservationsposter på bogføringstidspunktet. Denne implementering er baseret på, at tidsvinduet mellem beregningsprocessen og bogføringsprocessen er typisk lille. Men hvis du vil reservere lager på beregningstidspunktet, kan du vælge **Ja** i denne indstilling.

    Den ældre bogføringsfunktion reserverer altid lager under opgørelsesberegningsprocessen (hvis reservationen ikke var allerede er blevet foretaget via batchjobbet **Bogfør lager**), uanset hvad der er valgt i denne indstilling.

- **Deaktivering af optælling er påkrævet** – Når denne indstilling er sat til **Ja**, fortsætter bogføringsprocessen for en opgørelse, selvom forskellen mellem det optalte beløb og transaktionsbeløbet i opgørelsen er uden for grænsen, der er defineret i oversigtspanelet **Opgørelse** for butikker.

Derudover er følgende parametre introduceret i oversigtspanelet **Batchbehandling** under fanen **Bogføring** på siden **Commerce-parametre**: 

- **Det maksimale antal parallelle opgørelsesbogføringer** – Dette felt definerer antallet af batchopgaver, der skal bruges til at bogføre flere opgørelser. 
- **Maks. antal tråde til ordrebehandling pr. opgørelse** – Dette felt repræsenterer det maksimale antal tråde, der bruges af batchjobbet for opgørelsesbogføringen til at oprette og fakturere salgsordrer for en enkelt opgørelse. Det samlede antal tråde, der bruges af bogføringsprocessen for opgørelser, beregnes på basis af værdien i denne parameter ganget med værdien i parameteren **Det maksimale antal parallelle opgørelsesbogføringer**. Hvis værdien af denne parameter er for høj, kan det have en negativ indvirkning på ydeevnen for opgørelsesprocessen.
- **Maks. antal posteringslinjer, der er inkluderet i aggregeringen** – Dette felt definerer antallet af posteringslinjer, som skal medtages i en enkelt aggregeret transaktion, før der oprettes en ny. Aggregerede posteringer oprettes på basis af forskellige aggregeringskriterier, f.eks. debitor, forretningsdato eller økonomiske dimensioner. Det er vigtigt at bemærke, at linjerne fra en enkelt transaktion ikke bliver opdelt på tværs af forskellige aggregerede transaktioner. Det betyder, at der er mulighed for, at antallet af linjer i en aggregeret transaktion er lidt højere eller lavere baseret på faktorer som antallet af specifikke produkter.
- **Maksimale antal tråde til at validere butikstransaktioner** – Dette felt definerer antallet af tråde, der skal bruges til validering af transaktioner. Validering af transaktioner er et påkrævet trin, der skal udføres, før transaktionerne kan trækkes ind i opgørelserne. Desuden skal du også definere et **gavekortprodukt** på oversigtspanelet **Gavekort** under fanen **Bogføring** på siden **Commerce-parametre**. Det skal defineres, selvom gavekort ikke bruges af organisationen.

> [!NOTE]
> Alle indstillinger og parametre, der er relateret til bogføring af opgørelsen, og som er defineret i butikker og på siden **Commerce-parametre**, gælder for funktionen til forbedret bogføring af opgørelser.

## <a name="processing"></a>Afvikling

Opgørelser kan beregnes og bogføres i batches ved hjælp af menupunkterne i **Beregn opgørelser i batch** og **Bogfør opgørelser i batch**. Alternativt kan opgørelser beregnes og bogføres manuelt ved hjælp af menupunktet **Opgørelser**, som funktionen til forbedret opgørelsesbogføring indeholder.

Processen og fremgangsmåden til beregning og bogføring af opgørelser i et batch er den samme, som de var i den ældre bogføringsfunktion. Dog er der sket betydelige forbedringer i kerne-backend-behandlingen af opgørelser. Disse forbedringer gør det mere fleksibel og giver bedre indsigt i tilstands- og fejloplysninger. Brugerne kan derfor fokusere på hovedårsagen til fejl og derefter fortsætte bogføringsprocessen uden at forårsage beskadigelse af data og uden, at det kræver datarettelser.

I følgende afsnit beskrives nogle af de vigtigste forbedringer af opgørelsesbogføringsfunktionen, som findes i brugergrænsefladen for opgørelser og bogførte opgørelser.

### <a name="status-details"></a>Statusoplysninger

Der er indført en ny tilstandsmodel i opgørelsesbogføringsrutinen på tværs af beregning og bogføring.

I følgende tabel beskrives de forskellige tilstande og deres rækkefølge under beregningsprocessen.

| Tilstandsrækkefølge | Status      | Betegnelse |
|-------------|------------|-------------|
| 1           | Igangsat    | Opgørelsen er oprettet og er klar til at blive beregnet. |
| 2           | Afmærket     | De posteringer, der er relevante for opgørelsen, identificeres baseret på parameterindstillingerne i opgørelsen, og de er markeret med opgørelses-id'et. |
| 3           | Beregnet | Opgørelseslinjerne beregnes og vises. |

I følgende tabel beskrives de forskellige tilstande og deres rækkefølge under bogføringsprocessen.

| Tilstandsrækkefølge | Status                   | Betegnelse |
|-------------|-------------------------|-------------|
| 1           | Markeret                 | Der udføres flere valideringer, der er relateret til parametre (f.eks. dispositionsgebyret) og til opgørelsen og opgørelseslinjerne (f.eks. forskellen mellem det optalte beløb og transaktionsbeløbet). |
| 2           | Aggregeret              | Salgstransaktioner for navngivne og unavngivne kunder aggregeres baseret på konfigurationen. Hver aggregeret transaktion konverteres til sidst til en salgsordre. |
| 3           | Kundeordre oprettet  | Baseret på den aggregerede transaktion oprettes der salgsordrer i systemet. |
| 4           | Kundeordre faktureret | Salgsordrer faktureres. |
| 5           | Bogførte rabatter        | Periodiske rabatkladder bogføres ud fra konfigurationen. |
| 6           | Bogført indtægt/udgift   | Indtægts-/ udgiftstransaktioner bogføres som bilag. |
| 7           | Tilknyttede bilag         | Betalingskladder oprettes og sammenkædes med den tilsvarende faktura. |
| 8           | Bogførte betalinger         | Betalingskladder bogførtes. |
| 9           | Bogførte gavekort       | Gavekorttransaktioner bogføres som bilag. |
| 10          | Opslået                  | Opgørelsen markeres som bogført. |

Hver tilstand i de foregående tabeller er af natur uafhængig, og der opbygges en hierarkisk afhængighed mellem tilstandene. Denne afhængighed løber fra top til bund. Hvis der opstår fejl i systemet, mens det behandler en tilstand, vender status for tilstanden tilbage til den foregående tilstand. Alle efterfølgende forsøg, der foretages af processen, fortsætter fra den tilstand, der mislykkedes, og flytter fortsat fremad i processen. Denne metode har følgende fordele:

- Brugeren har fuldstændig synlighed i den tilstand, hvor fejlen opstod.
- Beskadigelse af data undgås. Der var f.eks. forekomster i den ældre funktion til bogføring af opgørelser, hvor nogle af slagordrerne blev faktureret, mens andre forblev åbne. Der var også forekomster, hvor nogle betalingskladder ikke havde en tilhørende faktura at udligne, fordi der opstod en fejl i fakturabogføringen.
- Brugere kan se den aktuelle tilstand for en opgørelse ved hjælp af knappen **Statusoplysninger** i gruppen **Detaljer om udførelse** i opgørelsen. Siden med statusdetaljer består af tre sektioner:

    - Den første sektion viser den aktuelle status for opgørelsen sammen med fejlkoden og en detaljeret fejlmeddelelse, hvis der opstod en fejl.
    - Den anden sektion viser beregningsprocessens forskellige tilstande. Visuelle tegn angiver tilstande, der er blevet udført, tilstande, der ikke kunne køres på grund af fejl, og tilstande, der endnu ikke er udført.
    - Den tredje sektion viser bogføringsprocessens forskellige tilstande. Visuelle tegn angiver tilstande, der er blevet udført, tilstande, der ikke kunne køres på grund af fejl, og tilstande, der endnu ikke er udført.

Hovedet i den anden og tredje sektion viser derudover den samlede status for den relevante proces.

### <a name="event-logs"></a>Hændelseslogge

En opgørelse, gennemgår forskellige handlinger (for eksempel Opret, Beregn, Fjern og Bogfør), og flere forekomster af den samme handling kan kaldes under opgørelsens livscyklus. F.eks. efter en opgørelse er oprettet og beregnet, kan en bruger fjerne opgørelsen og beregne den igen. Knappen **Hændelseslogge** i gruppen **Detaljer om udførelse** i opgørelsen indeholder et fuldstændigt revisionsspor for de forskellige handlinger, der blev kaldt i en opgørelse, sammen med oplysninger om, hvornår disse handlinger blev kaldt.

### <a name="aggregated-transactions"></a>Aggregerede transaktioner

Under bogføringsprocessen aggregeres salgsposteringerne baseret på konfigurationen. Disse aggregerede transaktioner gemmes i systemet og bruges til at oprette salgsordrer. Hver aggregerede transaktion opretter én tilsvarende salgsordre i systemet. Du kan se de aggregerede tilstande ved hjælp af knappen **Aggregerede transaktioner** i gruppen **Detaljer om udførelse** i opgørelsen.

Fanen **Oplysninger om salgsordre** i en aggregeret transaktion indeholder følgende oplysninger:

- **Post-id** – Id'et for den aggregerede transaktion.
- **Opgørelsesnummer** – Den opgørelse, som den aggregerede transaktion tilhører.
- **Dato** – Den dato, hvor den aggregerede transaktion blev oprettet.
- **Salgs-id** – Når der oprettes en salgsordre fra den aggregerede transaktion, er dette salgsordre-id'et. Hvis dette felt er tomt, er den tilsvarende salgsordre ikke blevet oprettet.
- **Antal aggregerede linjer** – Det samlede antal linjer til den aggregerede transaktion og salgsordre.
- **Status** – Den sidste status for den aggregerede transaktion.
- **Faktura-id** – Når salgsordren for den aggregerede transaktion er faktureret, er dette salgsfaktura-id'et. Hvis dette felt er tomt, er fakturaen for salgsordren ikke blevet bogført.

Fanen **Transaktionsdetaljer** i en aggregeret transaktion viser alle transaktioner, der er trukket ind i den aggregerede transaktion. De aggregerede linjer i den aggregerede transaktion viser alle de poster, der er aggregeret fra transaktionerne. De aggregerede linjer viser også oplysninger om f.eks. vare, variant, antal, pris, nettobeløb, enhed og lagersted. Grundlæggende svarer hver aggregerede linje til én salgsordrelinje.

Fra siden **Aggregerede transaktioner** kan du hente XML-filen til en bestemt aggregeret transaktion ved hjælp af knappen **Eksportér salgsordre-XML**. Du kan bruge XML-filen til fejlfinding af problemer, der vedrører oprettelse af salgsordrer og bogføring. Hent XML-filen, overfør den til et testmiljø, og foretag fejlfinding af problemet i testmiljøet. Funktionen til hentning af XML-filen til aggregerede transaktioner er ikke tilgængelig for opgørelser, der er bogført.

Den aggregerede transaktionsvisning giver følgende fordele:

- Brugeren har indsigt i de aggregerede transaktioner, der mislykkedes under oprettelse af salgsordren, og de salgsordrer, der mislykkedes under faktureringen.
- Brugeren har indsigt i, hvordan transaktioner bliver aggregeret.
- Brugeren har et fuldstændigt revisionsspor, fra transaktioner til salgsordrer til salgsfakturaer. Dette revisionsspor var ikke tilgængeligt i den ældre funktionen til bogføring af opgørelser.
- Den aggregerede XML-fil gør det nemmere at identificere problemer under oprettelse af salgsordrer og fakturering.

### <a name="journal-vouchers"></a>Kladdebilag

Knappen **Kladdebilag** i gruppen **Detaljer om udførelse** i opgørelsen viser alle de forskellige bilagsposteringer, der er oprettet for en opgørelse, og som vedrører rabatter, indtægts- eller udgiftskonti, gavekort osv.

I øjeblikket vises disse data kun for bogførte opgørelser.

### <a name="payment-journals"></a>Betalingskladder

Knappen **Betalingskladder** i gruppen **Detaljer om udførelse** i opgørelsen viser alle de forskellige betalingskladder, der er oprettet for en opgørelse.

I øjeblikket vises disse data kun for bogførte opgørelser.

## <a name="other-improvements"></a>Andre forbedringer

Der er foretaget andre backend-forbedringer, som brugerne kan se, af funktionen til bogføring af opgørelsen. Her er nogle eksempler:

- I aggregering indgår ikke overveje medarbejdere, terminal og skift af enheder. Da der er færre aggregeringsparametre, skal der behandles færre salgsordrelinjer.
- Forekomsten af deadlock i transaktionstabeller reduceres ved at anvende yderligere udvidelsestabeller og ved at benytte indsættelser i stedet for opdateringshandlinger i transaktionstabeller.
- Antallet af igangværende batchopgaver er parameteriseret og begrænset. Dette nummer kan derfor finjusteres specifikt til en kundes miljø. I den ældre funktionen til bogføring af opgørelser blev der oprettet et ubegrænset antal batchopgaver ad gangen. Resultatet var uhåndterlige belastninger, omkostninger og flaskehalse på batchserveren.
- Opgørelser kan effektivt sættes i kø til behandling ved at prioritere de sætninger, der har det maksimale antal transaktioner.
- Batchprocesser, f.eks. **Beregn opgørelser i batch** og **Bogfør opgørelser i batch**, køres kun i batchtilstand. I den ældre funktionen til bogføring af opgørelsen kunne brugerne vælge at køre disse batchprocesser i en interaktiv tilstand, som er en enkelttrådet handling i modsætning til batchprocesser, som er flertrådede.
- I den ældre opgørelsesbogføringsfunktion placerede en fejl ved en batchopgave hele batchjobbet i fejltilstand. I den forbedrede funktion forårsager fejl i batchopgaver ikke, at batchjobbet sættes i fejltilstand, hvis andre batchopgaver fuldføres. Du skal vurdere bogføringsstatussen for en batchkørsel, der kører ved hjælp af siden **Opgørelser**, hvor alle opgørelser, der ikke er blevet bogført på grund af fejl, vises.
- I den ældre bogføringsfunktion får den første forekomst af en opgørelsesfejl hele batchen til at mislykkes. De resterende opgørelser behandles ikke. I den forbedrede funktion fortsætter batchprocessen med at behandle alle opgørelser, selvom nogle af dem mislykkes. En fordel er, at brugerne får indblik i, nøjagtigt hvor mange opgørelser der indeholder fejl. Derfor behøver brugerne ikke at hænge fast i en uafbrudt fejlretningsløkke og kørsel af efteropgørelsesprocessen, indtil alle opgørelser er bogført.

## <a name="general-guidance-about-the-statement-posting-process"></a>Generel vejledning om processen til bogføring af opgørelsen

- Vi anbefaler, at du kører opgørelsesbogføringsprocessen i et batch, fordi batchkørsler udnytter multitrådsfunktionerne i batchstrukturen. Multi-trådning er nødvendig for at håndtere de store mængder af transaktioner, der normalt ses i bogføringer af opgørelser.
- Vi anbefaler, at du slår negativt fysisk lager til i varemodelgruppen, så du får en problemfri bogføringsoplevelse. I visse scenarier kan negative opgørelser ikke bogføres, medmindre der er negativt fysisk lager. Teoretisk set hvis der f.eks. findes kun én enhed af en vare på lager, og der har været en salgstransaktion og en returtransaktion for varen, skal transaktionen kunne bogføres, selv hvis negativt lager ikke er aktiveret. Da processen til bogføring af opgørelsen henter både salgstransaktionen og returtransaktionen i en enkelt kundeordre, er der ingen garanti for, at salgslinjen bogføres først, efterfulgt af returlinjen. Derfor kan der opstå fejl. Hvis negativt lager er aktiveret i dette scenario, påvirkes bogføringen af transaktionen ikke negativt, og systemet afspejler lageret korrekt.
- Vi anbefaler, at du bruger aggregering, mens du beregner og bogfører opgørelser. Derfor anbefales følgende indstillinger til nogle af aggregeringsparametrene:

    - Gå til **Retail og Commerce** \> **Konfiguration af hovedkontor** \> **Parametre** \> **Commerce-parametre**. Vælg derefter **Oversigt** i feltet **Detaljeringsniveau** i oversigtspanelet **Opdatering af lager** under fanen **Bogføring**.
    - Gå til **Retail og Commerce** \> **Konfiguration af hovedkontor** \> **Parametre** \> **Commerce-parametre**. Under fanen **Bogføring** i oversigtspanelet **Aggregering** skal du derefter vælge **Ja** i indstillingen **Posteringer på bilag**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]