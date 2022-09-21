---
title: Bufferprofil og -niveauer
description: Denne artikel indeholder oplysninger om bufferprofiler og -niveauer, der bestemmer de minimum- og maksimumlagerniveauer, der skal bevares for hvert grænsepunkt.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428138"
---
# <a name="buffer-profile-and-levels"></a>Bufferprofil og -niveauer

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Når du har identificeret dine afløbspunkter (nøglevarer, som du strategisk vil beholde på lager), skal du beslutte, hvor meget lagerbeholdning (buffer) du vil beholde for hver af dem. Denne opgave er det andet trin i DDMRP (Demand Driven Materials Resource Planning).

## <a name="buffer-levels-and-zones"></a>Bufferprofil og -niveauer

I DDMRP defineres hver lagerbuffer ved hjælp af tre værdier: minimumantal, maksimumantal og restordrepunkt. Disse værdier opretter tre differencezoner, som identificeres ved følgende farvekoder:

- **Rød zone** – Området under minimumantallet. Minimumantallet kaldes også "top of red", og din planlægningsstrategi skal udformes til at sikre, at lagerniveauer altid ligger over dette punkt.
- **Gul zone** – Området mellem minimumantallet og restordrepunktet. Restordrepunktet kaldes også "øverst på gul". Når dette punkt er nået, skal systemet bestille igen.
- **Gul zone** – Området mellem genbestillingspoint og maksimummængde. Maksimummængden kaldes også "øverst på grøn". Dette punkt er det maksimale niveau, som lageret skal genopfyldes til.

I følgende illustration vises de tre farvezoner, og hvordan de relateres til minimumantal, maksimumantal og restordrepunkt.

![DDMRP-bufferzoner og -niveauer.](media/ddmrp-buffer-levels.png "DDMRP-bufferzoner og -niveauer")

## <a name="calculating-the-buffer-zones"></a>Beregne bufferzoner

I dette afsnit forklares det, hvordan højden på hver bufferzone beregnes.

Den gule zone beregnes typisk først. Denne zone repræsenterer det antal, du forbruger fra det tidspunkt, hvor du bestiller, til ordren ankommer. Det er med andre ord det forventede forbrug under genopfyldningstiden. Det beregnes ved hjælp af følgende ligning:

- **Gul zone** = *, daglig brug (ADU)* × *afledet gennemløbstid*

Den *afkoblede gennemløbstid* repræsenterer den tid, der kræves for at producere eller modtage en vare, hvis de fejlmeldte point altid er på lager. Den er normalt meget kortere end den *akkumulerede gennemløbstid*, der traditionelt bruges til behovsplanlægning. Korrekte bufferindstillinger er nøglen til sikring af, at afkoblingspunkter altid rent faktisk findes på lager, men ikke overfyldes.

Den røde zone beregnes ved hjælp af følgende ligninger:

- **Rød base** = *ADU* × *Afledt gennemløbstid* × *Gennemløbstidsfaktor*
- **Rød sikkerhed** = *Rød base* × *Variability-faktor*
- **Rød zone** = *Rød base* + *Rød sikkerhed*

Den grønne zone beregnes som det maksimale resultat af følgende tre ligninger:

- *Min. ordreantal*
- *ADU* × *Ordrecyklus*
- *ADU* × *Afledt gennemløbstid* × *Gennemløbstidsfaktor*

## <a name="calculating-average-daily-usage"></a>Beregn gennemsnitlig daglig brug

Systemet bruger en af tre metoder til at beregne det beløb, du forbruger pr. dag:

- **Gennemsnitlig brug (tidligere)** – Denne tilgang er baseret på faktisk tidligere forbrug.
- **Gennemsnitlig brug (fremadrettet)** – Denne tilgang er baseret på planlagt fremtidigt forbrug.
- **Gennemsnitlig daglig brug (blandet)** – Denne tilgang er baseret på en vægtet miks af tidligere og budgetteret forbrug.

### <a name="average-daily-usage-past"></a>Gennemsnitlig daglig brug (tidligere)

Past ADU beregnes som et gennemsnit ved at lægge de antal sammen, der bruges hver dag i et angivet antal tidligere dage, og derefter dividere totalen med antallet af dage. I følgende illustration vises, hvordan denne fremgangsmåde fungerer, når beregningen kigger tre dage ind i fortiden.

![Gennemsnitlig daglig brug (diagram.)](media/ddmrp-adu-past.png "Gennemsnitligt dagligt forbrug (tidligere) diagram")

I ovenstående illustration, hvis i dag er om morgenen den 11. juni, er ADU for de foregående tre dage (8., 9. og 10. juni) er 21.

- **ADU (tidligere)** = (29 + 11 + 23) ÷ 3 = 21

Der tages højde for følgende posteringer ved beregning af gennemsnitlig daglig brug:

- Transaktioner, der reducerer antallet af varer (i tabellen `inventtrans`, hvor antallet er mindre end nul)
- Transaktioner med status *I bestilling*, *Reserveret bestilt*, *Reserveret fysisk*, *Plukket*, *Fratrukket* eller *Solgt*
- Posteringer, der er dateret inden for den valgte periode bagud (den gennemsnitlige brug tidligere periode)
- Andre transaktioner end lagerstedsarbejde, karantæne, salgstilbud eller kontoudtog (`WHSWork`, `WHSQuarantine`, `SalesQuotation` eller `Statement`)
- Andre posteringer end overførselskladder, der findes inden for samme disponeringsdimension

### <a name="average-daily-usage-forward"></a>Beregn gennemsnitlig daglig brug (fremadrettet)

I forbindelse med et nyt produkt har du muligvis ikke tidligere brugsdata. Derfor kan du i stedet bruge det forventede ADU, fremadrettet (f.eks. baseret på budgetteret efterspørgsel). I følgende illustration vises, hvordan denne fremgangsmåde fungerer, når beregningen kigger tre dage ind i fortiden (herunder i dag).

![Beregn gennemsnitlig daglig brugsdiagram (fremadrettet).](media/ddmrp-adu-forward.png "Gennemsnitlig dagligt forbrug (fremadrettet) diagram")

I ovenstående illustration, hvis i dag er om morgenen den 11. juni, er ADU for de næste tre dage (11., 12. og 13. juni) er 21.66.

- **ADU (fremadrettet)** = (18 + 18 + 29) ÷ 3 = 21.66

Der tages højde for følgende posteringer ved (fremadrettet) beregning af gennemsnitlig daglig brug:

- Budgetposter for den vare, hvor budgettet er valgt i behovsplanen
- Posteringer, der er dateret inden for den valgte periode fremadrettet (den gennemsnitlige brug tidligere periode)

### <a name="average-daily-usage-blended"></a>Gennemsnitlig daglig brug (blandet)

Den blandede ADU kombinerer den gennemsnitlige tidligere brug og den gennemsnitlige fremtidige brug som vist i følgende illustration.

![Gennemsnitlig daglig brugsdiagram (blandet).](media/ddmrp-adu-blended.png "Gennemsnitlig dagligt forbrug (blandet) diagram")

I ovenstående illustration, hvis i dag er om morgenen den 11. juni, er blandet ADU for de foregående og næste tre dage (8. - 13.) er 21.33.

- **ADU-blandet** = (*ADU tidligere* + *ADU fremadrettet*) ÷ 2<br>= (21 + 21.66) ÷ 2<br>= 21.33

## <a name="buffer-calculation-factors"></a>Bufferberegningsfaktorer

For hver vare kan du definere to faktorer for at justere, hvor store de røde og grønne zoner skal være. På denne måde kan du udligne den forventede gennemløbstid og efterspørgselsvariation.

![Faktorer til gennemløbstid og variation.](media/ddmrp-zone-factors.png "Faktorer til gennemløbstid og variation")

Den første faktor er *leveringstidsfaktoren*. Værdien er en decimalværdi fra 0 til 1. Jo længere gennemløbstiden er, jo lavere skal værdien være. Demand Driven Institute anbefaler følgende områder:

- **Lang gennemløbstid:** 0.20–0.40
- **Mellemstor gennemløbstid:** 0,41-0,60
- **Kort gennemløbstid:** 0,61-1,00

Den anden faktor er *variationsfaktoren*. Værdien er en decimalværdi fra 0 til 1. Jo højere efterspørgselsvariationen er, jo lavere skal værdien være. Demand Driven Institute anbefaler følgende områder:

- **Lav variability:** 0,20-0,40
- **Medium variability:** 0,41-0,60
- **Høj variability:** 0,61-1,00

## <a name="buffer-calculation-examples"></a>Eksempler på bufferberegninger

I dette eksempel fortsættes det produktionseksempel, der findes i [Lagerplacering](ddmrp-inventory-positioning.md). I dette eksempel valgte du de afkoblingspunkter, der reducerede gennemløbstiden fra 21 dage til fem dage som vist i følgende illustration.

![Eksempel på afkoblet gennemløbstid.](media/ddmrp-bom-decoupled-lead-time-example.png "Eksempel på afkoblet gennemløbstid")

Antag for dette eksempel, at ADU er beregnet som 23 styk, og som vist i foregående illustration er den forsinkede gennemløbstid fem dage. Når du bruger disse værdier, kan du beregne den gul zone ved at bruge følgende ligning:

- **Gul zone** = *ADU* × *Afskærmet gennemløbstid* = 115

![Eksempel på beregning af gul zone.](media/ddmrp-example-calc-yellow.png "Eksempel på beregning af gul zone")

Beregningen af den røde zone svarer til den gul zoneberegning, men den har tastatur til variation og gennemløbstid. I dette eksempel kan du antage, at du har set en mellemstor gennemløbstid (faktor = 0,50) og høj efterspørgselsvariation (faktor = 0,8). Hvis du bruger disse værdier sammen med komponenterne fra den gul zoneligning, kan du beregne den røde zone ved at bruge følgende ligninger:

- **Rød base** = *ADU* × *Afledt gennemløbstid* × *Gennemløbstidsfaktor* = 57.5
- **Rød sikkerhed** = *Rød base* × *Variability-faktor* = 46
- **Rød zone** = *Rød base* + *Rød sikkerhed* = 103.5

Systemet vil runde den røde zone op til 104 styk (ea), fordi styk tælles i hele numre.

![Eksempel på beregning af rød zone.](media/ddmrp-example-calc-red.png "Eksempel på beregning af rød zone")

Beregningen af den grønne zone inkluderer også komponenterne fra den gul zoneligning, men det giver mulighed for en minimumsordrestørrelse, ordrecyklus og gennemløbstidsfaktor. I dette eksempel kan du antage, at der ikke er nogen ordrecyklus (derfor er der ingen tidsbegrænsninger for, hvor ofte du bestiller), og minimumsordreantallet er 10 styk. Den grønne zone beregnes som det maksimale resultat af følgende tre ligninger:

- *Minimalt ordreantal* = 10
- *ADU* × *Ordrecyklus* = 0
- *ADU* × *Afledt gennemløbstid* × *Gennemløbstidsfaktor* = 57.5

Systemet vil runde den grønne zone op til 58 styk (ea), fordi styk tælles i hele numre.

![Eksempel på beregning af grøn zone.](media/ddmrp-example-calc-green.png "Eksempel på beregning af grøn zone")

I følgende illustration opsummeres disse zoneberegningsresultater ved hjælp af den tragtgrafik, der ofte bruges i DDMRP.

![Opsummering af zoneberegningsresultater.](media/ddmrp-example-calc-summary.png "Opsummering af zoneberegningsresultater")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynamiske reguleringer

Du kan bruge dynamiske justeringer til at anvende en *reguleringsfaktor for efterspørgsel* i perioder med høj eller lav efterspørgsel. Denne faktor multipliceres ADU i alle beregninger for den valgte periode. Bufferzonerne ændres derefter efter tur. Denne faktor anvendes normalt, når du har genereret de første bufferværdier, så du kan finjustere dem over tid og på baggrund af ændrede betingelser. Denne opgave er det tredje trin i DDMRP.

Der kan f.eks. være større efterspørgsel efter et produkt fra august, når folk går på ferie. Derfor forventes salget at være højere. I dette tilfælde kan du ændre værdien for **efterspørgselsreguleringsfaktoren** for produktet til *1,5* for alle uger i august.

På denne måde kan du beregne bufferværdier over tid og derefter justere dem ud fra mere end blot de oplysninger, systemet har. I en komplet DDMRP-implementering kan du beregne nye bufferværdier hver dag via et batchjob og automatisk acceptere værdierne. Du skal derefter køre planlægningen som et batchjob og gennemse ordreforslagene hver dag for at opfylde bufferne.

## <a name="implement-buffers-in-supply-chain-management"></a>Implementer buffere i Supply Chain Management

I dette afsnit beskrives, hvordan du implementerer bufferzonestrategien i Microsoft Dynamics 365 Supply Chain Management. Det antages, at du allerede har udført de analyser og beregninger, der er skitseret i første halvdel af denne artikel.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Opret buffers for en vare til udfyldningspunkt

Benyt følgende fremgangsmåde for at konfigurere bufferværdier for et afkoblingspunkt.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg en frigivet vare, der er konfigureret som et afkoblingspunkt. (Du finder flere oplysninger under [Lagerpositionering](ddmrp-inventory-positioning.md).)
1. Vælg **Plan** i handlingsruden, og vælg derefter **Varedisponering**.
1. Vælg en varedisponeringspost, der opretter et disponeringspunkt på siden **Varedisponering**. (Denne post viser navnet på en disponeringsgruppe, der er konfigureret til at oprette disponeringspunkter).
1. Vælg fanen **Generelt**.
1. Hvis du ønsker, at systemet skal genberegne bufferværdier hver dag eller hver uge baseret på salgshistorikken, budgetter og indstillinger for disponeringsgrupper, skal du benytte følgende fremgangsmåde:

    1. Angiv **bufferværdier for overtid** til *Ja*.
    1. En meddelelsesboks giver dig besked om, at dine manuelle bufferindstillinger (**Minimum**, **Genbestillingspunkt** og **Maksimum**) nulstilles, hvis du fortsætter. Vælg **Ja** for at beholde den nye indstilling.

    Hvis du foretrækker at beregne eller angive bufferindstillingerne én gang, kan du også benytte følgende fremgangsmåde:

    1. Angiv **bufferværdier for overtid** til *Nej*.
    1. Angiv felterne **Minimum**, **Genbestillingspunkt** og **Maksimum** til de bufferværdier, du har beregnet for varen, som beskrevet tidligere i denne artikel.

1. Angiv følgende felter for at afslutte opsætningen af DDMRP-beregninger for varen:

    - **Ordrecyklus** – Angiv det antal dage, der skal gå mellem indkøbsordrerne for varen. Angiv værdien til *0* (nul), hvis der ikke findes ordrebegrænsninger. Dette felt har indflydelse på den maksimale antalsbuffer, som det tidligere er beskrevet i denne artikel.
    - **Gennemsnitlig daglig brug** – Du kan vælge at angive en estimeret ADU for varen. Dette felt er udelukkende til orientering. Normalt beregnes værdien automatisk som en del af bufferberegningerne.
    - **Ordretærskel** – Angiv det minimale antal daglige salg af varen, der opfylder betingelserne for at være salg (usædvanligt stor efterspørgsel). Systemet bruger dette felt til at øge antallet af ordreforslag i perioder med stor efterspørgsel. Du kan finde flere oplysninger under [Efterspørgselsbaseret planlægning](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Beregn eller angiv afkoblede gennemløbstider

For varer, hvor du vælger at tillade, at systemet [beregner bufferzoner](#set-up-buffers) automatisk, skal du følge disse trin for at beregne eller angive de forkerte gennemløbstider for en lagervare.

1. Åbn **varedisponeringssiden** for din disponeringspunktvare. (Du kan finde flere oplysninger i [Oprette buffere for en vare til udfyldningspunkt](#set-up-buffers).)
1. Vælg en varedisponeringspost, der opretter et disponeringspunkt.
1. Vælg fanen **Bufferværdier**.
1. Hvis der ikke er vist tidsperioder i gitteret, skal du vælge **Tilføj tidsperioder** under fanen **Bufferværdier** i handlingsruden. Systemet udfylder gitteret med rækker for hver daglig eller ugentlig tidsperiode, afhængigt af om feltet **Min., maks. og re-ordrepunktsperiode** for [disponeringsgruppen](ddmrp-inventory-positioning.md) er angivet til *Daglig* eller *Ugentlig*. Systemet tilføjer nok rækker til at nå den tidsgrænse, der er angivet for den disponeringsgruppe, som er knyttet til varen.
1. Vælg den tidsperiode, hvor du vil beregne den mislykkede gennemløbstid. (Normalt er denne tidsperiode den periode, der omfatter dags dato).
1. Vælg **Beregn gennemløbstid** under fanen **Bufferværdier** i handlingsruden.
1. Angiv følgende felter i dialogboksen **Beregn afkoblet gennemløbstid**:

    - **Stykliste** – Vælg den stykliste, som du vil køre beregningen på.
    - **Dato** – Vælg den dato, som du vil køre beregningen på. Sættet af tilgængelige styklister filtreres, så det kun er de styklister, der er aktive for den valgte dato, der vises.
    - **Mængde** – Angiv det mængde, der skal køres beregning for. Sættet af tilgængelige styklister filtreres, så det kun er de styklister, der anvendes til den angivne mængde, der vises.

1. Vælg **OK** for at køre beregningen, og luk dialogboksen **Beregn afkoblet gennemløbstid**. Den **afkoblet gennemløbstid**-kolonne for den valgte tidsperiode viser nu den beregnede værdi.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Beregn eller angiv gennemsnitlig daglig brug

For varer, hvor du vælger at tillade, at systemet [beregner bufferzoner automatisk](#set-up-buffers), skal du følge disse trin for at beregne eller angive ADU afkoblingstider.

1. Åbn **varedisponeringssiden** for din disponeringspunktvare. (Du kan finde flere oplysninger i [Oprette buffere for en vare til udfyldningspunkt](#set-up-buffers).)
1. Vælg en varedisponeringspost, der opretter et disponeringspunkt.
1. Vælg fanen **Bufferværdier**.
1. Hvis der ikke er vist tidsperioder i gitteret, skal du vælge **Tilføj tidsperioder** under fanen **Bufferværdier** i handlingsruden. Systemet udfylder gitteret med rækker for hver daglig eller ugentlig tidsperiode, afhængigt af om feltet **Min., maks. og re-ordrepunktsperiode** for [disponeringsgruppen](ddmrp-inventory-positioning.md) er angivet til *Daglig* eller *Ugentlig*. Standardværdierne for felterne **Gennemløbstidsfaktor** og **Variability-faktor** tages desuden fra dækningsgruppen. Du kan redigere disse værdier for hver række efter behov.
1. Vælg en tidsperiode, hvor du vil beregne ADU.
1. Vælg **Beregn gennemsnitlig dagligt forbrug** under fanen **Bufferværdier** i handlingsruden. Systemet forsøger at indsamle data, der er påkrævet til beregningen af ADU, som defineret for [dækningsgruppen](ddmrp-inventory-positioning.md).
1. Udfør ét af følgende trin:

    - Hvis de påkrævede data er tilgængelige, føjes beregningsresultaterne til kolonnen **Gennemsnitligt dagligt forbrug**. I dette tilfælde kræves der ingen handling.
    - Hvis de påkrævede data ikke er tilgængelige, tilføjes der ingen værdier automatisk. I dette tilfælde skal du angive forkalkuleret værdi manuelt for hver række, hvor du planlægger at beregne bufferværdier.

### <a name="calculate-and-apply-buffer-values"></a>Beregn og anvend bufferværdier

For varer, hvor du vælger at tillade, at systemet [beregner bufferzoner automatisk](#set-up-buffers),kan du manuelt udløse beregningerne for bufferværdier ifølge disse trin.

1. For det relevante afkoblingselement skal du [konfigurere bufferberegningen](#set-up-buffers), [beregne eller angive afkoblingsleveringstider](#calc-lead-time) og [beregne eller angive det gennemsnitlige daglige forbrug](#calc-adu) for alle relevante tidsperioder, som beskrevet tidligere i denne artikel.
1. Åbn **varedisponeringssiden** for din disponeringspunktvare.
1. Vælg fanen **Bufferværdier**, der allerede skal vise en liste over tidsperioder.
1. Vælg en tidsperiode, hvor du vil beregne bufferværdier. (Normalt vil denne tidsperiode være den periode, der omfatter i dag). Den række, du vælger, skal allerede have værdier, der ikke er nul, i kolonnerne **Gennemsnitligt dagligt forbrug** og **Afkoblet gennemløbstid**.
1. Rediger feltet **Efterspørgselsreguleringsfaktor** for en eller flere rækker efter behov. Systemet anvender denne faktor på værdien for **daglig gennemsnitsbrug** i alle bufferberegninger, hvor denne værdi bruges. Du kan bruge denne faktor til at justere den måde, som efterspørgslen varierer efter dato (f.eks. på ferier eller sæsonvarer).
1. Under fanen **Bufferværdier** i handlingsruden skal du vælge **Beregn min., maks. og restordreantal**. Systemet beregner og udfylder gitteret for **beregnet min.**, **beregnet restordrepunkt** og **beregnede maks. kolonner** i gitteret på **varedisponeringssiden**.
1. Når du er færdig med at gennemse de beregnede værdier, skal du anvende dem. Ellers har de ingen virkning. Når du anvender en beregning for en eller flere rækker, kopieres værdier fra felterne henholdsvis **Beregnet min.**, **Beregnet genbestilling** og **Beregnet maks.** til henholdsvis kolonnerne **Min**, **Genbestillingspunkt** og **Maks**-kolonner. I handlingsruden skal du vælge en af følgende knapper under fanen **Bufferværdier** i gruppen **Udfør handling**:

    - **Accepter alle beregninger** – Anvend alle beregnede værdier i gitteret.
    - **Accepter beregninger for udvalgte rækker** – Anvend kun beregnede værdier for de valgte rækker.
    - **Kassér alle beregninger** – Slet alle beregnede værdier for minimumantal, maksimumantal og genordrepunkter i gitteret.
    - **Kassér alle beregninger for valgte rækker** – Slet alle beregnede værdier for minimumantal, maksimumantal og genordrepunkter i for valgte rækker.

### <a name="schedule-automatic-buffer-value-calculations"></a>Planlæg automatiske bufferværdiberegninger

Når du har konfigureret indstillingerne for DDMRP fuldstændigt og bekræftet, at de fungerer som forventet, vil du sandsynligvis oprette et batchjob, der periodisk skal genberegnes ADU og relaterede bufferværdier baseret på faktiske forbrugsdata og/eller opdaterede prognoser. Denne procedure gælder kun for varer, hvor du vælger at tillade, at systemet [automatisk beregner bufferzonerne](#set-up-buffers).

Benyt følgende fremgangsmåde for at planlægge automatiske beregning af bufferværdier.

1. Gå til **Varedisponering \> Varedisponering \> DDMRP \> Beregning af bufferværdier**.
1. Angiv følgende felter i dialogboksen **Beregn bufferværdier**:

    - **Beregn gennemsnitlig daglig brug** – Angiv denne indstilling til *Ja* for at genberegne ADU-varer, hver gang jobbet køres. Angiv det til *Nej* for at springe denne beregning over. Normalt skal du angive denne indstilling til *Ja*.
    - **Beregn afkoblet gennemløbstid** – Angiv denne indstilling til *Ja* for at genberegne de afledede gennemløbstider, hver gang jobbet køres. Angiv det til *Nej* for at springe denne beregning over. Normalt skal du angive denne indstilling til *Ja*.
    - **Beregn bufferværdier** – Angiv denne indstilling til *Ja*, hvis du vil genberegne bufferværdier, hver gang jobbet køres. Angiv det til *Nej* for at springe denne beregning over. Normalt skal du angive denne indstilling til *Ja*.
    - **Accepter beregning for min., maks. og restordrepunkt** – Angiv denne indstilling til *ja*, hvis du automatisk vil godkende og anvende de genberegnede bufferværdier, hver gang jobbet køres. Angiv det til *Nej*, hvis de genberegnede værdier ikke skal kunne anvendes. I dette tilfælde træder de genberegnede værdier ikke i kraft, medmindre de anvendes manuelt senere fra hvert produkts **varedisponeringsside**. Normalt skal du angive denne indstilling til *Ja*.
    - **Behovsplan** – Vælg en behovsplan, der omfatter de varer, der påvirkes af beregningen. Beregningen gælder for alle varerne i planfilteret, hvilket yderligere begrænses af **filterindstillingerne** i denne dialogboks.

1. Hvis du vil begrænse, hvilke poster der skal medtages i batchjobbet, skal du vælge **Filter** i oversigtspanelet **Poster, der skal medtages** for at åbne dialogboksen **Forespørgsel**. Denne dialogboks fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. I oversigtspanelet **Kør i baggrunden** skal du angive, hvordan, hvornår og hvor ofte de valgte beregninger skal udføres for de valgte varer. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK** for at tilføje det nye job til udførelse i batchkøen.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Gennemgå og genberegne gennemløbstider for alle varer

Følg disse trin for at gennemse og genberegne alle de leveringstider, der er tilgængelige i din juridiske enhed (regnskabet).

1. Gå til **Varedisponering \> Varedisponering \> DDMRP \> Afkoblet gennemløbstid**.
1. Gennemse og filtrer listen efter behov for at finde de oplysninger, du leder efter, på siden **Afkoblet gennemløbstid**. Hvis du vil have vist flere oplysninger om en vare, skal du vælge dens tilknytning i kolonnen **Varenummer**.
1. Hvis du vil genberegne den afledede gennemløbstid for alle varer, skal du markere varen og derefter vælge **Beregn afkoblet gennemløbstid** i handlingsruden. Dialogboksen **Beregn afkoblet gennemløbstid** vises. Denne dialogboks fungerer på samme måde, som den gør, når du [beregner afkoblede gennemløbstider](#calc-lead-time) for samme vare på siden **Varedisponering**.
