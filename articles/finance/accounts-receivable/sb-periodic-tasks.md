---
title: Periodiske opgaver ved fakturering af tilbagevendende kontrakter
description: Denne artikel indeholder en beskrivelse af de periodiske opgaver, der er tilgængelige ved fakturering af tilbagevendende kontrakter.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904782"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Periodiske opgaver ved fakturering af tilbagevendende kontrakter

Denne artikel indeholder en beskrivelse af de periodiske opgaver, der er tilgængelige ved fakturering af tilbagevendende kontrakter.

## <a name="generate-invoice"></a>Generér faktura

Du kan bruge siden **Generér faktura** til at oprette månedlige tilbagevendende massefakturaer ud fra de oplysninger, du har angivet på siderne **Alle faktureringsplaner** og **Vis faktureringsoplysninger**. Når en faktura oprettes, opdateres varebeskrivelsen til salgsordrebehandlingslinjen med varebeskrivelsen og start- og slutdatoerne for faktureringen for den planlægningslinje, der faktureres.

## <a name="generate-invoice-batch-processing"></a>Generér fakturabatchbehandling

Du kan bruge siden **Generér fakturabatchbehandling** til at oprette tilbagevendende fakturaer via en batchproces, der gentages. De parametre, der er tilgængelige, er de samme som parametrene på siden **Opret faktura**, men de kan gemmes i en batchproces, der kan køres flere gange.

## <a name="price-update"></a>Prisopdatering

Brug værktøjet til prisopdatering til at opdatere priserne på flere varer på flere faktureringsplaner i én handling. Priserne kan opdateres baseret på enten en angivet procent eller et angivet beløb. På listen over linjer vises kun varens aktuelle enhedspriser. Den viser ikke priserne efter prisopdateringen.

Bemærk følgende punkter om prisopdateringsværktøjet:

- Hvis salgsordren for et bestemt år allerede er oprettet (dvs. varerne er afregnet), påvirkes prisen på linjevarerne ikke.
- Prisopdateringsværktøjet kan bruges til linjevarer med status af **Aktiv** eller **Venter**. For varer, der venter, skal indstillingen **Juster tidsplan** have været angivet til **Nej**, da ventetiden blev indledt.
- Prisopdateringsværktøjet kan ikke bruges til linjevarer, der er forbrugsvarer, som bruger eskalering, milepælsfakturering eller indtægtsfordeling.

### <a name="price-update-example"></a>Eksempel på prisopdatering

Der oprettes en faktureringsplan, og der tilføjes en fornyelsesvare. Prisen pr. enhed er $750. Det første år for varen betales den 15. december 2021. Faktureringsplanen oprettes for perioden fra 1. januar til og med 31. december 2022.

Når ordren fornys , vil **Generér faktura** oprette salgsordren til år 2022. Når du har kørt prisopdateringsværktøjet, opdateres prisen fra $750 til $800.

Salgsordren og faktureringsplanen for 2022 påvirkes ikke, og enhedsprisen forbliver $750, da faktureringsplanen for 2022 allerede er afregnet. Faktureringsplanlinjen og linjedetaljerne for 2023 opdateres til $800, fordi faktureringsplanen for 2023 endnu ikke er afregnet.

### <a name="update-prices--flat-pricing-method"></a>Opdater priser – flad metode for prissætning

Når du opdaterer priser for varer, der bruger den flade prissætningsmetode, kan du angive en procent eller et beløb, som prisen skal øges med.

Benyt følgende fremgangsmåde for at køre prisopdateringsværktøjet for varer, der bruger den flade prissætningsmetode.

1. Vælg metoden **Flad** prissætning på siden **Prisopdatering**.
2. Vælg den stigningsmetode, der skal bruges til opdatering af prisen på varerne, i feltet **Stigningsmetode**.
3. Afhængigt af den valgte stigningsmetode skal du angive procentdelen i feltet **Procent** eller beløbet i feltet **Beløb**.
4. Brug knappen **Filter** til at tilføje datafiltre i oversigtspanelet **Poster, der skal medtages**.
5. Vælg **Vis eksempel** for at få vist området af poster.
6. Markér de linjer, du ikke vil behandle, og vælg derefter **Fjern**.
7. Vælg **OK**.

### <a name="update-prices--standard-pricing-method"></a>Opdater priser – standardprissætningsmetode

Hvis prisen på en vare er ændret i vareposten, kan den opdateres for alle faktureringsplanlinjer, hvis varen bruger standardprissætningsmetoden.

1. Vælg metoden **Standard** prissætning på siden **Prisopdatering**.
2. Brug knappen **Filter** til at tilføje datafiltre i oversigtspanelet **Poster, der skal medtages**.
3. Vælg **Vis eksempel** for at få vist området af poster.
4. Markér de linjer, du ikke vil behandle, og vælg derefter **Fjern**.
5. Vælg **OK**.

## <a name="mass-hold-processing"></a>Massebehandling af hold

Brug siden **Massebehandling af hold** til at anvende holdindstillinger på flere faktureringsplaner på én gang.

Hvis du kun vil sætte én faktureringsplan eller faktureringsplanslinje på hold, skal du åbne siden **Alle faktureringsplaner** og vælge **Placer på hold**. Hvis du vil fjerne et hold, skal du bruge siden **Fjern hold**.

### <a name="put-billing-schedules-on-hold"></a>Sætte faktureringsplaner på hold

Følg disse trin for at sætte flere faktureringsplaner på hold.

1. Angiv feltet **Procesindstilling** til **Anvend hold** på siden **Massebehandling af hold**.
2. Vælg en årsagskode i feltet **Årsagskode**.
3. Angiv indstillingen **Juster tidsplan**:

    - **Ja** – Hvis du angiver indstillingen til **Ja**, skal du angive en hold-dato i feltet **Hold-dato**. Alle faktureringsplanlinjer efter hold-datoen fjernes.
    - **Nej** – Faktureringsplanlinjerne ændres ikke. Kun status ændres. Den opdateres til **På hold**.

4. Brug knappen **Filter** til at tilføje datafiltre i oversigtspanelet **Poster, der skal medtages**.
5. Vælg **Vis eksempel** for at få vist området af poster.
6. Markér de linjer, du ikke vil behandle, og vælg derefter **Fjern**.
7. Vælg **OK**.

Når du vender tilbage til listen over faktureringsplaner, bør du se, at status for faktureringsplanerne er ændret til **Venter**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Fjerne et hold fra flere faktureringsplaner

1. Angiv feltet **Procesindstilling** til **Fjern hold** på siden **Massebehandling af hold**.
2. Angiv en årsagskode i feltet **Årsagskode**.
3. Angiv den dato, hvor hold skal fjernes, i feltet **Fjern dato**.
4. Angiv felterne **Dato for genoptagelse** og **Udskydelsesdato** efter behov. Udskydelsesdatoen føjes til alle linjer, der kan udskydes.
5. Brug knappen **Filter** til at tilføje datafiltre i oversigtspanelet **Poster, der skal medtages**.
6. Vælg **Vis eksempel** for at få vist området af poster.
7. Markér de linjer, du ikke vil behandle, og vælg derefter **Fjern**.
8. Vælg **OK**.

> [!NOTE]
> Hvis du vil fjerne et hold, skal du angive værdien **Fjern tilsidesættelse af brugergruppe på hold** på siden **Faktureringsparametre for tilbagevendende kontrakter**.

En faktureringslinje har f.eks. startdatoen 1. februar 2022 og slutdatoen 28. februar 2022. Faktureringsbeløbet er $200. Feltet **Hold-dato** indstilles til 10. februar 2022. Februarperioden reguleres derfor for at udelade enhver dato efter den 10. februar. Den nye periode er fra 1. februar til og med 9. februar, og beløbet er $64,29 (via daglig proportionalitet). Alle faktureringsplanlinjer fra og med den 10. februar fjernes.

Hvis processen **Fjern hold** er fuldført, og feltet **Fjern dato** er angivet til 10. februar 2022, er der to faktureringsperioder. Den første periode er fra 1. februar til og med 9. februar, og beløbet er $64,29. Den anden periode er fra 10. februar til og med 28. februar, og beløbet er $135,71.

## <a name="mass-termination-processing"></a>Behandling af masseaftrædelse

Du kan bruge siden **Massefratrædelse** til at afslutte faktureringsplanlinjer, der vises i øjeblikket, ved at angive en fratrædelsesdato.

Hvis du bruger indtægts- og udgiftsudskydelser, kan du få refunderet faktureringsplaner, hvor feltet **Fratrædelsesdato** er angivet til **Juster tidsplan** på siden **Alle faktureringsplaner**.

Faktureringsplaner, der bruger funktionen til fordeling af flere varer (MEA), vises ikke på siden **Massefratrædelse**. Du kan stadig afslutte en enkelt faktureringsplan ved at bruge fratrædelsesfunktionen i faktureringsplanen.

> [!NOTE]
> De faktureringsplanlinjer, der aktuelt er inkluderet i en batch af **Generér faktura**, er ikke tilgængelige for denne proces.

Du kan finde flere oplysninger om de enkelte felter og processen i [Afslutte faktureringsplaner](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Massearkiveringsproces

Brug siden **Massearkivering** til at arkivere flere faktureringsplaner. Det er kun fratrådte faktureringsplaner, der kan arkiveres.

Når en faktureringsplan er arkiveret, forekommer følgende hændelser:

- Statussen ændres til **Arkiveret**.
- Faktureringsplanerne er låst permanent.
- Faktureringsplanlinjerne er ikke længere tilgængelige på forespørgselssider.

> [!NOTE]
> Arkivering af en faktureringsplan er en permanent handling, og den kan ikke tilbageføres.

Følg disse trin for at arkivere faktureringsplaner.

1. Angiv en slutdato for fakturering i feltet **Faktureringsslutdato** på siden **Massearkivering**. Hvis du vil have vist alle fratrådte faktureringsplaner, skal du lade dette felt stå tomt.
2. Hvis du vil begrænse de viste poster, skal du vælge knappen **Filter** i oversigtspanelet **Poster, der skal indgå**.
3. Vælg **Vis forhåndsversion**.
4. Markér de poster, du ikke vil arkivere, og vælg derefter **Fjern**.
5. Vælg **OK** for at arkivere posterne på siden.

## <a name="mass-stubbing-process"></a>Masserydningsproces

Brug siden **Masserydningsproces** til at markere alle valgte faktureringsplanlinjer som fakturerede (rydning) eller ikke-fakturerede (tilbageført rydning). Rydning eller tilbageført rydning er oftest de importerede faktureringsplanlægningslinjer, der tidligere er afregnet i et andet system. Ryddede faktureringsplanlinjer vises som ryddet og opretter ikke en faktura til kunden.

### <a name="stub-records"></a>Ryd poster

1. Vælg **Ryd** i feltet **Procesindstillinger** på siden **Masserydningsproces**.
2. Angiv en skæringsdato i feltet **Skæringsdato** for at angive de linjer, som processen skal gælde for. Det er kun poster, hvor faktureringsstartdatoen ligger på eller før den angivne skæringsdato, der vises.
3. Vælg **Vis forhåndsversion** for at få vist de linjer, du vil rydde.
4. Hvis du vil udelukke en linje fra processen, skal du markere den og derefter vælge **Fjern**.
5. Vælg **Behandling** for at rydde linjerne.

### <a name="reverse-stub-records"></a>Tilbageføre ryddede poster

1. Vælg **Tilbageføre rydning** i feltet **Procesindstillinger** på siden **Masserydningsproces**.
2. Angiv en skæringsdato i feltet **Skæringsdato** for at angive de linjer, som processen skal gælde for. Det er kun poster, hvor faktureringsstartdatoen ligger på eller før den angivne skæringsdato, der vises.
3. Vælg **Vis forhåndsversion** for at få vist de linjer, du vil tilbageføre rydning for.
4. Hvis du vil udelukke en linje fra processen, skal du markere den og derefter vælge **Fjern**.
5. Vælg **Behandling** for at tilbageføre ryddede linjer.

## <a name="update-completion-date-process"></a>Opdater proces til fuldførelsesdato

Brug siden **Opdater fuldførelsesdato** til at opdatere fuldførelsesdatoen for bestemte milepælselementer for flere faktureringsplaner eller brugere. Du kan også opdatere færdiggørelsesgrad for varer på milepælsskabeloner, hvor metoden **Procent færdiggjort** bruges.

1. Gå til **Behandling af milepæl** på siden **Opdater fuldførelsesdato**, og vælg **Opdater færdiggørelsesprocent**.
2. I feltet **Procentbeløb** skal du angive den samlede procentdel, der er fuldført.
3. Vælg det varenummer, der er relateret til milepælsskabelonen.
4. I oversigtspanelet **Poster, der skal medtages**, skal du vælge **Filter** for at vælge en bestemt **Slutbrugerkonto**, **Faktureringsplannummer** eller **Varenumre** som filterkriterium.
5. Vælg **OK** for at foretage ændringen. Når behandlingen er fuldført, føjes der en ny linje til milepælsfordelingen. Denne linje repræsenterer den procentdel, der er fuldført for milepælsskabelonen.

## <a name="unbilled-revenue-mass-processing"></a>Massebehandling af ikke-afregnet indtægt

Brug siden **Massebehandling af ikke-afregnet indtægt** til at oprette kladdeposten for ikke-afregnet omsætning eller kladdeposten for rydning af en eller flere valgte faktureringsplaner eller faktureringsdetaljelinjer.

- **Opret kladdepostering** – Opret ikke-fakturerede omsætningskladdeposteringer for flere faktureringsplanlinjer. Vælg knappen **Filter** i oversigtspanelet **Poster, der skal indgå**, for at udvælge posterne på listen. Listen viser kun faktureringsplanlinjer, som ikke-fakturerede omsætningskladdeposteringer ikke er oprettet for. De første kladdeposteringer oprettes. I forbindelse med udskudte varer oprettes også udskydelsesplaner.
- **Ryd kladdepostering** – Markér de faktureringsplanlinjer, som de ikke-fakturerede kladdeposteringer allerede er oprettet for. Denne indstilling bruges, hvis den ikke-fakturerede kladdepost allerede er bogført i et andet system. Den markerer den ikke-fakturerede omsætningskladde som ryddet og bogfører ikke en transaktion i finansmodulet.
- **Tilbageføre rydning af kladdepostering** – Tilbagefør rydning af kladdepostering, der er behandlet. Hvis der blev begået en fejl under behandlingen af **Ryd kladdepostering**, vil denne indstilling fjerne markeringen i afkrydsningsfeltet **Ryddet** for faktureringsplanlinjen.
- **Rydningsfakturerings detaljelinje** – Brug denne proces, når ikke-afregnet omsætning er behandlet i et eksternt system, og nogle af faktureringsdetaljerne allerede er afregnet. Denne proces sikrer, at det korrekte beløb vises på kontiene for ikke-afregnet omsætning.
- **Tilbageføre rydningsfakturerings detaljelinje** – Tilbagefør alle **Rydningsfakturerings detaljelinje**-handlinger.

Feltet **Kladdenavn** bruges til at bogføre **Opret kladdepostering** i finansmodulet.

> [!NOTE]
> Denne rydning bogfører ikke beløb i finansmodulet. Feltet **Kladdenavn** er ikke tilgængeligt for alle rydningsprocesser og tilbageførte rydningsprocesser.

### <a name="unbilled-revenue-stub-example"></a>Eksempel på ikke-afregnet rydning

Der konfigureres en faktureringsplan for ét år fra oktober 2021 til og med september 2022. Den ikke-fakturerede omsætning er allerede behandlet i et eksternt system. Ni måneder af faktureringsplanen er allerede afregnet. Beløbet for hver faktureringsperiode er $250. I begyndelsen af året vil det samlede beløb, der er bogført til ikke-bogført omsætning, blive $3.000. Efter ni måneder er $2.250 blevet afregnet, og $750 i ikke-afregnet omsætning resterer.

Hvis du vil konfigurere faktureringsplanen, hvor der kun er tre måneder tilbage af afregnet omsætning, skal du følge disse trin.

1. På siden **Vis faktureringsoplysninger** skal du oprette en faktureringsplan for perioden fra oktober 2021 til og med september 2022, varenummer S0001 og et beløb på $250 pr. måned.
2. Vælg **Opret kladdepost** for faktureringsplanen. Beløbet på $3.000 bogføres i ikke-afregnet omsætning.
3. Vælg **Rydningsfakturerings detaljelinje**, og angiv transaktionsdatoen i juni 2022 (ni måneder). Faktureringsplanlinjerne vises ikke i forhåndsversionen. De berørte linjer baseres på transaktionsdatoen.
4. Vælg **OK**.

De første ni måneder, der er afregnet, ryddes.

[![Vis rydningsfakturerings detaljelinjer.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

Beløbet på $3.000 tilbageføres fra ikke-afregnet omsætning, og $750 i ikke-afregnet omsætning, der resterer, bogføres. Hvis du vil se ikke-afregnede omsætningsposteringer, skal du vælge **Revision af ikke-faktureret omsætningskladde** under fanen **Fornyelser** på siden med linjedetaljer.

[![Revision af ikke-faktureret omsætningskladde.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Kladdeposten for den ikke-afregnede omsætning kan oprettes for enhver fornyelsesperiode, forudsat at alle faktureringsdetaljelinjer fra forrige periode er afregnet. En faktureringsplanlinje har f.eks. en månedlig faktureringsfrekvens for en 12-måneders periode fra januar til og med december 2021. Linjen indeholder tre perioder: den første periode, den anden periode (januar til og med december 2022) og en tredje periode (januar til og med december 2023). Når fakturaen er oprettet for alle faktureringsdetaljer fra de første 12 måneder i 2021, kan der oprettes kladdepost for ikke-afregnet omsætning for den anden periode.
>
> I forbindelse med udskydelsesvarer, der bruger funktionen til ikke-afregnet omsætning, behandles faktureringslinjen og rabatlinjerne. For disse varer oprettes kladdeposten for den ikke-afregnede omsætning og udskydelsesplanen for faktureringslinjen og rabatlinjen.
>
> De kladdeposteringer, der oprettes for varer, der ikke kan udskydes, og varer, der kan udskydes, bogfører en kredit på forskellige indtægtskonti.
