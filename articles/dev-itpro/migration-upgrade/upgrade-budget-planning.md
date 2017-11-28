---
title: "Opgradere budgetplanlægning"
description: "Der er væsentlige forskelle i budgetplanlægning mellem Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Finance and Operations. Nogle funktioner blev ikke opgraderet og kræver derfor omkonfiguration. I dette emne beskrives, hvad der skal konfigureres, og nye funktioner, der skal overvejes, når opgraderingen er fuldført."
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a39f516bb6d023ea18492ba3dfe721bd1127c60e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="upgrade-budget-planning"></a>Opgradere budgetplanlægning

[!include[banner](../includes/banner.md)]


Der er væsentlige forskelle i budgetplanlægning mellem Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Finance and Operations. Nogle funktioner blev ikke opgraderet og kræver derfor omkonfiguration. I dette emne beskrives, hvad der skal konfigureres, og nye funktioner, der skal overvejes, når opgraderingen er fuldført.  

Budgetplanlægning i Microsoft Dynamics 365 for Finance and Operations har mange forbedringer, der ikke var tilgængelige i Microsoft Dynamics AX 2012. I dette emne beskrives de ændringer, der skal foretages af kunder, der opgraderer. Desuden omtales de nye funktioner, der skal overvejes i opgraderingsprocessen. På grund af omfanget af ændringerne kan eventuelle eksisterende budgetplaner ikke åbnes, før de ændringer, der er beskrevet i dette emne, er foretaget. Rapporter bør dog fortsat fungere og skulle ikke kræve yderligere ændringer.

## <a name="overview-of-changes"></a>Oversigt over ændringer
Der er foretaget mange væsentlige ændringer i Budgettering til Finance and Operations. Disse ændringer er beregnet til at gøre budgetplanlægningen nemmere at konfigurere og mere genanvendelig og til at reducere opsætning og vedligeholdelse år for år. Følgende områder i AX 2012 findes ikke længere i Finance and Operations:

-   Skabeloner til budgetplan (konfiguration af budgetplanlægning)
-   Mapper til budgetplan (konfiguration af budgetplanlægning)
-   Scenariebegrænsninger (konfiguration af budgetplanlægning)
-   Skabeloner til regler og skabeloner til budgetplanlægningsstadier (budgetplanlægningsproces).
-   Matrixfelter til regnearksskabeloner
-   Guiden Microsoft Excel-skabelon til budgetplan

Nogle nye begreber kan ikke opgraderes direkte fra de tidligere funktioner. Derfor skal du omkonfigurere nogle funktioner af hensyn til disse nye begreber. I følgende afsnit beskrives de begreber, der har erstattet elementerne i den foregående liste.

### <a name="columns"></a>Søjler

Kolonner er et nyt begreb, der erstatter dele af Excel-skabelonen og også matrixfelter. Kolonner kan repræsentere en periode, måned, kvartal, år eller al tid. Tidsreferencen er dynamisk. Den peger på en relativ periode eller år med reference til budgetprocessen. F.eks. refererer kolonnen **Forrige år januar** til regnskabsperiode 1 for år -1. En kolonne er specifik for et budgetplanscenarie, f.eks. anmodning om faktiske oplysninger eller budget.

### <a name="layouts"></a>Layout

Layout er et nyt begreb, der erstatter Excel-skabelonen. Layout indeholder de kolonner, der definerer, hvilke budgetdata eller faktiske oplysninger og perioder der skal vises. Layout deles også mellem klienten og Excel-tilføjelsesprogrammet. Brugeroplevelsen, når du angiver eller får vist data i Dynamics 365 for Finance and Operations-klienten, er derfor bedre end brugeroplevelsen i AX 2012. Når indtaster data i Finance and Operations-klienten, er du ikke længere begrænset til visning og indtastning af et enkelt scenario i en posteringsvisning. I stedet kan du med en sammenlignende visning nemt få vist og angive beløb for flere perioder og konti på samme tid. Layout kan også defineres, så du kan angive og få vist valuta, kommentarer og andre valgfrie data. Med layout kan du definere, hvilke finansdimensioner og beskrivelser for dimensionen der skal vises. Layout omfatter også begrænsninger i scenariet for at definere, hvilke kolonner i en skabelon, der kan redigeres, og hvilke kolonner der skal være tilgængelige i Excel. Når du har defineret et layout, oprettes der en skabelon for det. Denne skabelon opretter den tilsvarende Excel-skabelon. Du kan derefter redigere Excel-skabelonen, hvis du vil medtage flere formler og formatering, og derefter overføre den igen. Layout tildeles derefter til hver stadieregel på siden **Budgetplanlægningsproces**. Derfor erstatter layout skabeloner, som blev tildelt og brugt på samme måde.

### <a name="budget-planning-processes"></a>Budgetplanlægningsprocesser

Budgetplanlægningsprocesser er næsten som i AX 2012. Den væsentligste ændring er en erstatning af skabeloner med layout. Hvis nogen processer tidligere blev afsluttet i AX 2012, opdateres processerne til status igangværende, så der kan udføres ændringer. Du skal tildele layout og for hver stadieregel bestemme, hvilke scenarier og tidsperioder der skal vises, når planen åbnes i klienten. De forskellige layout bestemmer også, hvilken Excel-skabelon der skal åbnes uden for Dynamics 365 for Finance and Operations, så du kan få vist budgettet. **Standardkontostruktur** er et nyt obligatorisk felt til budgetplanlægningsprocessen. For hver budgetplanlægningsproces skal du tildele den primære kontostruktur, der skal bruges til budgettering.

### <a name="attachments"></a>Vedhæftede filer

I AX 2012 blev berettigelsesdokumenter gemt i en mappe til vedhæftede filer. Ingen tidligere berettigelsesdokumenter opgraderes. Berettigelsesdokumenter gemmes nu i databasen. Hvis disse oplysninger skal gemmes i den opgraderede version, kan du sende berettigelsesdokumenter for hver enkelt plan som en vedhæftet fil ved hjælp af knappen **Berettigelse** i handlingsruden. I AX 2012 blev Excel-regneark for hver budgetplan oprettet ud fra skabelonen. I Finance and Operations åbner alle planer en kopi af layoutet. Men ingen ændringer af Excel-filen gemmes. Alle formler eller supplerende oplysninger, der blev brugt på pr. plan-basis, skal tilføjes via kommentarer, et berettigelsesdokument eller anden supplerende proces.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Konfiguration af et miljø, der er opgraderet fra AX 2012
Følgende eksempel bruger en opgraderet budgetproces fra AX 2012 demo-data til at hjælpe dig med at bestemme, hvordan du konfigurerer det opgraderede system. Der er oprettet standardkonfigurationsdata for kolonner til opgraderingen. Du kan opdatere eller slette disse standarddata, hvis de ikke opfylder dine konfigurationskrav. **Bemærk!** Der er nye obligatoriske felter, der ikke angivet i systemet. Hvis du går i stå på en side, f.eks. siden **Budgetplanlægningskonfiguration** og ikke kan navigere væk, kan du lukke browseren og derefter åbne den igen på en anden side for at angive oplysninger i den rigtige rækkefølge. Der er obligatoriske felter, som endnu ikke er angivet. Derfor kan der opstå problemer, indtil alt er konfigureret, og alle obligatoriske felter er angivet. I dette emne forklares, hvordan du angiver disse felter efter behov. Her er nogle af disse obligatoriske felter:

-   Siden **Budgetplanlægningsproces**: Feltet **Standardkontostruktur**
-   Siden **Budgetplanlægningsproces**: Feltet **Layout** i oversigtspanelet **Stadieregler og layouts for budgetplanlægning**

### <a name="define-columns-and-layouts"></a>Definere kolonner og layout

1.  På siden **Budgetplanlægningskonfiguration** skal du klikke på fanen **Kolonner**. Som en del af opgraderingen oprettes nye kolonner automatisk ud fra dine budgetplanlinjer. Kolonner bruger nu dynamiske datoer, hvor tid og år forskydes fra det regnskabsår, der er defineret i budgetplanlægningsprocessen. **Bemærk!** Af hensyn til ydeevnen under opgraderingen antages det, at alle budgetcyklusser repræsenterer kalenderår, ikke regnskabsår. Hvis du bruger regnskabsår, skal du foretage redigeringer for at tilknytte kolonner til deres regnskabsår korrekt. For eksempel fandtes følgende elementer i AX 2012:
    -   Budgetplanscenarier: faktiske oplysninger, grundlag, budgetanmodning, godkendt budget
    -   Budgetplanlinjerne for alle scenarier i 2017 og faktiske værdier for både 2017 og 2016

    Der oprettes følgende kolonner i Finance and Operations:
    | Kolonnenavn    | Budgetplansscenarie | Kolonnetidsperiode | Årsforskydning |
    |----------------|----------------------|--------------------|-------------|
    | Jan scenario 1 | Faktiske oplysninger              | 1                  | 0           |
    | Jan scenario 2 | Grundlag             | 1                  | 0           |
    | Jan scenario 3 | Budgetanmodning       | 1                  | 0           |
    | Jan scenario 4 | Godkendt budget      | 1                  | 0           |
    | Jan scenario 5 | Faktiske oplysninger              | 1                  | -1          |
    | Feb scenario 1 | Faktiske oplysninger              | 1                  | 0           |
    | ...            | ...                  | ...                | ...         |

    I dette eksempel er en kolonne med navnet **Jan scenario 1** oprettet for de seneste posteringsdata i budgetplanen, hvor der findes posteringer i januar. Der oprettes en tilsvarende kolonne for hvert scenario, der indeholder data. Når der findes kolonner for alle perioder i det pågældende år, oprettes der kolonner for tidligere år.
2.  Du kan ændre navnene på kolonnerne og beskrivelserne og andre detaljer, enten manuelt i klienten eller ved at benytte masseopdateringer via Excel-tilføjelsesprogrammet, der peger på kolonnedataenheden i budgetplanen. Filtre, der tidligere blev angivet for matrixfelter, angives nu i kolonnerne.
3.  Opret et layout til en ny budgetplan. Et layout peger på flere kolonner for at definere den visning, der vises i Excel og klienten. Layoutet kræver først, at du angiver en økonomisk dimension, der er indstillet til at bestemme, hvilke økonomiske dimensioner der kan angives. Når du har angivet dimensionsopsætningen, skal du klikke på **Beskrivelser** for at vælge de dimensionsbeskrivelser, der skal medtages i layoutet.
4.  I oversigtspanelet **Layoutelementer** skal du klikke på **Tilføj** for at tilføje metadata for hver række som en valuta, en kommentar eller en budgetklasse, der bestemmer indtægtsrækker i forhold til udgiftsrækker. Derefter skal du tilføje kolonner for det tidsrum og de scenarier, der gælder for denne budgetcyklus og dette -stadie. Du kan foretage disse ændringer manuelt i klienten eller via Excel-tilføjelsesprogrammet, der peger på dataenheden for layoutelementer i budgetplanen.
5.  For hvert layoutelement skal du vælge, om kolonnen skal kunne redigeres, og om kolonnen også skal vises i Excel-projektmappen for dette layout. **Bemærk!** Til vores historiske planer kan du overveje et layout, der viser 12 månedlige kolonner for alle budgetplansscenarier til denne proces.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Opdatere budgetplanlægningsprocesser, så de bruger det relevante layout for hver enkelt budgetfase

1.  På siden **Budgetplanlægningsproces** skal du vælge den proces, der skal konfigureres.
2.  Klik på **Rediger** i handlingsruden.
3.  Angiv standardkontostrukturen for denne budgetproces. **Standardkontostruktur** er et nyt obligatorisk felt, der skal angives.
4.  I oversigtspanelet **Stadieregler og layouts for budgetplanlægning** i feltet **Layout** skal du vælge et layout, der blev konfigureret tidligere, og som er egnet til dette trin.
5.  Fortsæt med at vælge det samme eller forskellige layout til forskellige stadier i budgetplanlægningen, og gem derefter ændringerne.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Yderligere funktioner, du kan overveje i budgetprocessen
### <a name="budget-planning-workspace"></a>Arbejdsområde til budgetplanlægning

Dette arbejdsområde er udviklet til både ejeren af et budget og individuelle bidragydere til budgetter. Det indeholder links til alle dokumenter i budgettet, der kræver din opmærksomhed. Der er også rapporter og nøgletal (KPI'er) til budgetprocessen. Budgetadministratoren kan definere den aktuelle budgetplanlægningsproces for alle brugere på siden **Budgetparametre**. Under fanen **Indstillinger for arbejdsområde** indeholder oversigtspanelet **Budgetplanlægning** et felt, hvor du kan vælge budgetplanlægningsprocessen.

### <a name="alternate-layouts"></a>Alternative layouts

Alternative layout er en ny funktion, hvor du kan få vist planer i forskellige layout. Et eller flere layout kan leveres som valgmuligheder. Derefter kan du se en budgetplan i et månedligt layout eller et kvartalslayout. Du definerer alternative layout i oversigtspanelet **Stadieregler og layouts for budgetplanlægning** på siden **Budgetplanlægningsproces**.

### <a name="budget-milestones"></a>Budgetmilepæle

Som en del af budgetprocessen er det vigtigt, at du forstår vigtige datoer og deadlines. Du kan nu konfigurere datoer, så de får beskrivelser. Budgetteringsbrugere får vist disse beskrivelser, når de åbner budgetter for at redigere eller få vist alt det, der er tildelt til dem.

### <a name="copy-from-budget-plan-allocation"></a>Kopiere fra budgetplanfordeling

En ny fordelingsmetode gør det muligt at fordele fra en overordnet plan til en underordnet plan uden at skulle gå via et mellemliggende niveau i hierarkiet. Denne metode er særligt nyttig for kunder, der tidligere har oprettet en økonomisk dimension for budgetfordeling og -godkendelser.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Generere budgetplaner fra nye budgetkilder

Følgende indstillinger blev tilføjet som periodiske processer. Med disse indstillinger kan du oprette en budgetplan ved at bruge eksisterende data fra et andet modul som udgangspunkt:

-   Oprette budgetplan fra behovsprognose
-   Oprette budgetplan fra forsyningsprognose
-   Oprette budgetplan fra projekt
-   Oprette budgetplan ud fra budgetregister

### <a name="more-complete-tracking-of-amounts"></a>Mere komplet sporing af beløb

I AX 2012 havde budgetplanlægning et enkelt planbeløb, der blev gemt for hver værdi. I Finance and Operations er datamodellen blevet udvidet. Der findes nu regnskabsvaluta-, transaktionsvaluta- og rapporteringsvalutabeløb for hver værdi. Under opgraderingen udfyldes disse nye kolonner automatisk for eksisterende data.

### <a name="do-not-convert-currency-in-aggregation"></a>Undlad at konvertere valuta i aggregering

Typisk, når en underordnet plan akkumuleres til et overordnet niveau, konverteres beløbene automatisk fra transaktionsvalutaen til regnskabsvalutaen for organisationen. Når du vælger **Nej** for indstillingen **Undlad at konvertere valuta i aggregering**, forbliver de akkumulerede beløb i den oprindelige valuta. Denne indstilling kan derfor give mere præcise reguleringer, der påvirkes af udsving i valutakursen.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Se tilbage fra en budgetplan til andre moduler, der har bidraget til budgettet

Budgetplaner kan oprettes ud fra efterspørgsels- eller forsyningsprognoser og andre områder. Forespørgslen Budgetplaner efter dimensionssæt har flere indstillinger, der gør det muligt at køre forespørgsler for at identificere de data, der var kilden til budgetplanen.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Overskrive eller tilføje i plan for fordelingsplaner

Hvis der er flere kilder til beløb, der skal distribueres, kan du angive, at beløbene skal kunne tilføjes. I så fald overskriver beløbene ikke eventuelle eksisterende beløb. De føjes derimod til de eksisterende beløb.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Økonomisk standarddimensionsopsætning for budgetplanlægningskonfiguration

Siden **Budgetplanlægningskonfiguration** indeholder nu et felt, hvor du kan angive den økonomiske standarddimensionsopsætning. Selvom dette felt er valgfrit, kan det være påkrævet til visse forespørgsler. Det kan også være påkrævet, hvis du vil gruppere eller filtrere rapportgrupperinger efter dimensionsopsætning.

### <a name="data-entities"></a>Dataenheder

Flere dataenheder er tilføjet for at aktivere hurtig implementering af budgetplanlægning. Enhederne gør det også muligt at foretage mange ændringer via Excel. Derfor behøver du ikke oprette ét element ad gangen via klienten. Her er en liste over de nye dataenheder:

-   Enhedsnavn
-   Budgetparametre
-   Budgetplanparametre
-   Budgetplansscenarier
-   Stadier i budgetplan
-   Stadie for budgetplanlægningsarbejdsgang
-   Fordelingsplaner for budgetplan
-   Trinfordelinger for budgetplan
-   Budgetplansprioriteter
-   Budgetplankolonner
-   Layoutelementer til budgetplan





