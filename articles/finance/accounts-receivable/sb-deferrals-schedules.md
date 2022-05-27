---
title: Udskydelsesplaner i indtægts- og udgiftsudskydelser
description: Dette emne beskriver udskydelsesplaner i indtægts- og udgiftsudskydelser.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685971"
---
# <a name="deferral-schedules"></a>Udskydelsesplaner

Når en transaktion er bogført, kan der oprettes udskydelsesplaner.

Du kan bruge siden **Alle udskydelsesplaner** eller **Aktive udskydelsesplaner** til at gennemse detaljerne om en udskydelsesplan. De oplysninger, der vises, afhænger af typen af udskydelsesplan (lineær eller hændelsesbaseret) og transaktionstypen. Den omfatter linjer i udskydelsesplanen og de samlede beløb for udskydelsesplanen. Du kan bruge siden til at redigere udskydelsesplaner.

## <a name="recognize-revenue"></a>Registrer indtægt

> [!NOTE]
> - Start i trin 1 for at registrere indtægten for én udskydelsesplan.
> - Start i trin 2 for at registrere indtægten for flere planer.

1. Vælg de linjer, du vil registrere, i gitteret **Planlæg linjer** på siden **Alle udskydelsesplaner**, og vælg derefter **Registrer**.
2. På siden **Føringsbehandling** skal du indstille feltet **Registreringshandling** til **Opret registreringskladde**.
3. Vælg skæringsdatoen i feltet **Skæringsdato**. Behandlingen medtager kun linjer, hvor slutdatoen er tidligere end eller samme som den valgte skæringsdato.
4. Vælg **Filter**, og tilføj datafiltre, så listen kun viser det ønskede postinterval.
5. Vælg **Vis eksempel** for at få vist linjerne.
6. Vælg de linjer på listen over linjer, du ikke vil behandle, og vælg derefter **Fjern**.
7. Vælg, om du vil opsummere registreringskladdeposten.
8. I sektionen **Transaktionsdato** kan du tilsidesætte transaktionsdatoen med en bestemt dato for behandling af transaktionen. Transaktionsdatoen kan angives for lukkede perioder.
9. Hvis du vil udføre behandlingen som en del af et batch, skal du vælge **Batch**. Angiv parametrene for batchen i dialogboksen **Batchbehandling**, og vælg derefter **OK** for at vende tilbage til siden **Føringsbehandling**. Indtægtsføringen behandles senere, når batchen behandles.
10. Vælg **Behandling**. Hvis du ikke har føjet transaktionen til en batch, behandles alle linjer med det samme. Ellers behandles linjerne, når batchen behandles.

## <a name="modify-a-schedule"></a>Redigere en plan

Følg disse trin for at redigere en udskydelsesplan.

1. På siden **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Regnskab \> Rediger tidsplan**.
2. Rediger de indstillinger, du vil ændre, på siden **Rediger tidsplan**. Afhængigt af udskydelsesplanen kan du ikke redigere alle indstillinger.
3. Vælg **Eksempel** for at få vist ændringerne af udskydelsesplanen.
4. Vælg **OK**.

### <a name="straight-line-deferral-schedules"></a>Lineære udskydelsesplaner

Hvis udskydelsesplanen ikke har registrerede eller eksternt bogførte linjer, kan du redigere hele udskydelsesplanen, herunder startdatoen.

Hvis udskydelsesplanen har registrerede eller eksternt bogførte linjer, og du redigerer udskydelsesplanen, vil den resulterende funktionsmåde for udskydelsesplanen være afhængig af genberegningsdatoen og udskydelsens slutdato for registrerede linjer. Den første periode, der ikke er registreret, bestemmer som standard slutdatoen.

Hvis du vil bruge datoen for registreringen, skal du vælge en af følgende værdier i feltet **Start af plan**: 
- **Indhentet** – Beløbet, efter at alle registrerede linjer er genberegnet.
- **Tilbageførsel** – Alle linjer efter genberegningsdatoen tilbageføres med brug af det angivne kladdenavn og den angivne bogføringsdato. Beløbet efter genberegningsdatoen genberegnes derefter.

Hvis der bruges en skabelon, ignoreres de perioder, der er sprunget over, og skabelonen bruges kun til at beregne slutdatoen.

### <a name="event-based-deferral-schedules"></a>Hændelsesbaserede udskydelsesplaner

Du kan redigere alle ikke-registrerede linjer for en hændelsesbaseret udskydelsesplan.

Hvis udskydelsesplanen har registrerede eller eksternt bogførte linjer, kan du ikke redigere skabelonen og fordelingstypen for udskydelsesplanen. Når du redigerer en eksisterende udskydelsesplan, kan du ikke ændre værdien i feltet **Opret separate hændelser pr. enhed**.

Hvis en linje er registreret eller bogført eksternt, markeres afkrydsningsfeltet **Ført**.

## <a name="modify-a-deferral-or-recognition-account"></a>Redigere en udskydelses- eller føringskonto

Hvis du vil redigere udskydelses- eller føringskontoen til en udskydelsesplan, skal du følge disse trin.

1. På siden **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Regnskab \> Rediger konto**.
2. På siden **Rediger konto** skal du vælge den konto, du vil ændre (udskydelse, kortsigtet eller føring).
3. Vælg den nye konto i feltet **Ny konto**.
4. Vælg, om ændringer af kontoen skal oprette reguleringskladdeposter.
5. Hvis du angiver indstillingen til **Ja** i forrige trin, skal du vælge kladdenavnet i feltet **Kladdenavn** og angive transaktionsdatoen i feltet **Transaktionsdato**.
6. Vælg **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Sætte en udskydelsesplan på hold

Følg disse trin for at sætte en udskydelsesplan på hold.

1. På siden **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Hold \> Sæt på hold**.
2. På siden **Sæt på hold** kan du vælge, om du vil overføre saldoen fra udskydelseskontoen eller på hold-kontoen.
3. Hvis du har valgt at overføre saldoen, skal du vælge kladdenavnet i feltet **Kladdenavn** og vælge på hold-kontoen i feltet **På hold-konto** og angive transaktionsdatoen i feltet **Transaktionsdato**.
4. Vælg **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Fjerne et hold fra en udskydelsesplan

Hvis du vil fjerne en udskydelsesplan fra hold, skal du følge disse trin.

1. På listen **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Hold \> Fjern på hold**.
2. I feltet **Kladdenavn** skal du vælge kladdenavnet.
3. Angiv transaktionsdatoen i feltet **Transaktionsdato**.
4. Vælg **OK**.

## <a name="cancel-unrecognized-amounts"></a>Annuller ukendte beløb

> [!NOTE]
> Alle linjer, der allerede er blevet registreret eller bogført eksternt, udelades fra denne proces.

Følg disse trin for at annullere ikke-registrerede beløb på en udskydelsesplan.

1. På siden **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Annuller \> Ikke-registrerede beløb**.
2. Vælg på siden **Annuller ikke-registreret beløb**, om du vil oprette annulleringsposter.
3. Hvis du har valgt at oprette annulleringsposter, skal du vælge kladdenavnet i feltet **Kladdenavn**, vælge annulleringskontoen i feltet **Annulleringskonto** og angive transaktionsdatoen i feltet **Transaktionsdato**.
4. Vælg **OK**.

## <a name="cancel-a-completed-schedule"></a>Annullere en fuldført plan

Brug siden **Alle udskydelsesplaner** til at tilbageføre eventuelle registrerede eller eksternt bogførte beløb og annullere udskydelsesplanen for at forhindre yderligere registrering.

Følg disse trin for at annullere en hel udskydelsesplan.

1. På siden **Alle udskydelsesplaner** skal du vælge udskydelsesplanen og derefter vælge **Annuller \> Fuldført tidsplan**.
2. Vælg på siden **Annuller fuldført tidsplan**, om du vil oprette annulleringsposter.
3. Hvis du har valgt at oprette annulleringsposter, skal du vælge kladdenavnet i feltet **Kladdenavn**, vælge kontoen i feltet **Annulleringskonto** og angive transaktionsdatoen i feltet **Transaktionsdato**.
4. Vælg **OK**.

## <a name="reverse-transactions"></a>Tilbagefør posteringer

> [!NOTE]
> - Start i trin 1 for at tilbageføre indtægtsføringen for én udskydelsesplan.
> - Start i trin 2 for at tilbageføre indtægtsføringen for flere udskydelsesplaner.

1. Vælg de linjer, du ikke længere vil registrere, i gitteret **Planlæg linjer** på siden **Alle udskydelsesplaner**, og vælg derefter **Tilbagefør**.
2. På siden **Føringsbehandling** skal du indstille feltet **Registreringshandling** til **Tilbagefør registreringskladde**.
3. Vælg skæringsdatoen i feltet **Skæringsdato**. Behandlingen medtager kun linjer, hvor slutdatoen er tidligere end eller samme som den angivne skæringsdato.
4. Vælg **Filter**, og tilføj datafiltre, så listen kun viser det ønskede postinterval.
5. Vælg **Vis eksempel** for at få vist linjerne.
6. Vælg de linjer på listen over linjer, du ikke vil behandle, og vælg derefter **Fjern**.
7. Felterne **Navn** og **Beskrivelse** opdateres automatisk med standardkladdenavn og -beskrivelse. Du kan ændre værdierne efter behov. Du kan også vælge, om du vil opsummere registreringskladdeposten.
8. I sektionen **Transaktionsdato** kan du tilsidesætte transaktionsdatoen med en bestemt dato for behandling af transaktionen. Transaktionsdatoen kan angives for lukkede perioder.
9. Hvis du vil udføre behandlingen som en del af et batch, skal du vælge **Batch**. Angiv parametrene for batchen i dialogboksen **Batchbehandling**, og vælg derefter **OK** for at vende tilbage til siden **Føringsbehandling**. Tilbageførslen af indtægtsføringen behandles senere, når batchen behandles.
10. Vælg **OK**. Hvis du ikke har føjet transaktionen til en batch, behandles alle linjer med det samme. Ellers behandles linjerne, når batchen behandles.

## <a name="apply-or-unapply-a-credit-note"></a>Anvende eller annullere brugen af en kreditnota

Følg disse trin for at anvende en kreditnota.

> [!NOTE]
> Når du opretter en kreditnota fra siden **Udskydelse af salgsordretransaktion** og angiver indstillingen **Juster eksisterende plan** til **Ja**, anvendes kreditnotaen automatisk i planen, når kreditnotaen bogføres.

1. Vælg udskydelsesplanen på siden **Alle udskydelsesplaner**.
2. Vælg en linje på listen **Kreditreguleringer**, og vælg derefter **Anvend**.
3. På siden **Anvend kreditnota (udskydelser)** skal du angive genberegningsdatoen i feltet **Genberegningsdato** og slutdatoen i feltet **Slutdato**.
4. Vælg den **Salgsordre**, der har kreditnotaer, på **Overskrift**-listen.
5. Vælg linjen på listen **Linjer**.
6. Vælg **OK**.
7. Vælg **Ja**.

> [!NOTE]
> Hvis du vil anvende en kreditnota på flere individuelle varer fra forskellige fakturaer, skal du gentage disse trin.

Følg disse trin for at holde op med at anvende en kreditnota.

1. Vælg udskydelsesplanen på siden **Alle udskydelsesplaner**.
2. Vælg fakturaen på listen **Kreditreguleringer**, og vælg derefter **Anvend ikke**.
3. Vælg **Ja**.

## <a name="fields"></a>Felter

Siden **Alle udskydelsesplaner** indeholder følgende felter.

| Felter | Beskrivelse |
|--------|-------------|
| **Overskrift** | |
| **Tidsplan** | |
| Fordelingstype | Fordelingstypen til hændelsesbaserede udskydelser: **Procent** eller **Beløb**. |
| Dato for genklassificering | <p>Den seneste dato, hvor den kortsigtede genklassificering for en udskydelsesplan blev behandlet. Denne dato opdateres, hver gang der bruges **Kortsigtet genklassificering af hændelse** for udskydelsesplaner.</p>Dette felt er kun tilgængeligt, når der bruges rullende perioder eller kortsigtet udskydelsesmetode for fastlagt år. |
| **Konto** | |
| Udskydelseskonto | Den konto, der bruges til udskydelsesbeløbet. |
| Føringskonto | Den konto, der bruges til føringsbeløbet. |
| Føringstype | Føringstypen. |
| Distributionstype | Distributionstypen. |
| **Transaktion** | |
| Oprettelseskilde | Den kilde, som transaktionen blev oprettet fra. |
| Transaktionstype | Transaktionstypen. |
| Salgsordre | Salgsordrenummeret. |
| Faktura | Fakturanummeret. |
| Vare | Varenummeret. |
| **Faktureringsplan** | |
| Faktureringsplannummer | Nummeret på den tilsvarende faktureringsplan. |
| Faktureringslinjestatus | Status for den tilsvarende varelinje i faktureringsplanen. |
| Eksterne referencer | Oplysninger om eksterne referencer fra faktureringsplanen: **Eksternt** og **Linjenummer**. |
| I alt | <p>Totalbeløb for udskydelsesplanen:</p><ul><li>**Langfristet** – Summen af langfristede udskudte beløb. Denne værdi er kun tilgængelig, når feltet **Kortsigtet udskydelsesmetode** er angivet til **Ingen** på siden **Udskydelsesparametre for indtægt og udgift**, eller det kortfristede beløb er større end 0 (nul).</li><li>**Kortfristet** – Summen af kortfristede udskudte beløb. Denne værdi er kun tilgængelig, når feltet **Kortsigtet udskydelsesmetode** er angivet til **Ingen** på siden **Udskydelsesparametre for indtægt og udgift**, eller det kortfristede beløb er større end 0 (nul).</li><li>**Ikke-ført** – Summen af ikke-førte beløb for alle linjer.</li><li>**Talon** – Summen af eksternt bogførte beløb for alle linjer.</li><li>**Ført** – Summen af førte beløb for alle linjer.</li><li>**Eksternt bogført og ført** – Summen af eksternt bogførte og førte beløb for alle linjer.</li><li>**Samlet beløb** – Summen af beløb for alle linjer.</li></ul> |
| **Tidsplanlinjer** | |
| Linje | Linjesekvensnummeret. |
| Startdato for udskydelse | Udskydelsesplanens startdato. |
| Slutdato for udskydelse | Udskydelsesplanens slutdato. |
| Antal | Udskydelsesbeløbet. |
| Eksternt bogført | En værdi, der angiver, om linjen er eksternt bogført. |
| Ført | En værdi, der angiver, om linjen er ført. |
| Kladdebatchnummer | Det batchnummer, som beløbet blev ført i. |
| Hændelsesbeskrivelse | En beskrivelse af hændelsen. Dette felt er kun tilgængeligt for hændelsesbaserede udskydelsesplaner. |
| **Kreditreguleringer** | |
| Faktura | <p>Fakturanummeret.</p><p>Værdien angiver fakturaen for den kreditnotaregulering, der allerede er anvendt på udskydelsesplanen.</p> |
| Anvendt beløb | Det kreditreguleringsbeløb, der allerede er anvendt på udskydelsesplanen. |
| Anvendt dato | Den dato, hvor kreditreguleringen blev anvendt. |
| **Regulering** | Reguleringsværdierne vises kun, hvis der er behandlet en kreditnota for udskydelsesplanen. Hvis der ikke er behandlet en kreditnota, skjules disse værdier. |
| Reguleringsbeløb | Det samlede reguleringsbeløb, der beregnes som *Oprindeligt beløb* – *Planbeløb*. |
| Oprindelig slutdato | Udskydelsesplanens oprindelige slutdato. |
| Oprindeligt tidsplanbeløb | Den oprindelige udskydelsesplans total. |
