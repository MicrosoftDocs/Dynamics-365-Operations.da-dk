---
title: Autoriser ordreforslag
description: Dette emne indeholder en forklaring på, hvordan du kan autorisere ordreforslag. Når ordreforslag autoriseres, bliver de til faktiske indkøbsordrer, overførelsesordrer eller produktionsordrer.
author: t-benebo
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f3ee656b97e0337b6e3e78f0acb2300d7d85dc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468462"
---
# <a name="firm-planned-orders"></a>Autoriser ordreforslag

[!include [banner](../../includes/banner.md)]

Ordreforslag skal være *autoriserede* (dvs. frigivet) som en del af varedisponeringsprocessen. Når ordreforslag autoriseres, bliver de til faktiske indkøbsordrer, overførelsesordrer eller produktionsordrer. Disse ordrer kaldes også *frigivne ordrer* eller *åbne ordrer*.

Der findes tre metoder til autorisation af ordreforslag:

- **Manuelt autorisation** – Vælg bestemte ordreforslag på en liste, og start derefter processen manuelt.
- **Automatisk autorisation** – Definer en tidsgrænse for standardautorisation for disponeringsgrupper, individuelle varer og kombinationer af varer og behovsplaner. Under kørsler af behovsplanlægning bliver ordreforslag derefter automatisk spærret, hvis ordredatoen ligger inden for den angivne tidsgrænse for autorisation.
- **Forespørgselsbaseret autorisation** – Definer en forespørgsel for at vælge ordreforslag ud fra deres egenskaber. Du kan oprette et batchjob, så du kan køre forespørgslen og autorisere tilsvarende ordrer regelmæssigt.

I dette emne beskrives de enkelte metoder nærmere.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Aktivere de funktioner, der er beskrevet i dette emne

De fleste funktioner for ordreforslag er tilgængelige i alle standardinstallationer af Microsoft Dynamics 365 Supply Chain Management, som anvender Planlægningsoptimering. Nogle få af de funktioner, der beskrives i dette emne, skal dog være aktiveret i Funktionsstyring, før du kan bruge dem.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Aktivere eller deaktivere parallel autorisation af ordreforslag

Parallel autorisation gør det muligt at gennemføre autorisationsprocessen hurtigere ved at parallelisere den over flere tråde. Denne metode kan være nyttig, når mange ordreforslag skal autoriseres. Hvis du vil bruge denne funktion, skal funktionen *Parallel autorisation af ordreforslag* være slået til for systemet. Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan du slå denne funktion til eller fra ved at gå til arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og søge efter funktionen *Parallel autorisation af ordreforslag*.

### <a name="enable-planned-order-firming-with-filtering"></a>Aktivere autorisation af ordreforslag med filtrering

Med autorisation af ordreforslag med filtrering kan du definere logiske kriterier for valg af, hvilke ordreforslag der skal autoriseres. Du kan også få vist, hvilke ordreforslag der er valgt, køre processen i baggrunden og/eller planlægge den som et batchjob.

Fra og med Supply Chain Management version 10.0.25 er denne funktion som standard aktiveret. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter funktionen *Autorisation af ordreforslag med filtrering* i arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="enable-auto-firming-for-planning-optimization"></a>Aktivere automatisk autorisation for Planlægningsoptimering

Med automatisk autorisation kan du autorisere ordreforslag som en del af varedisponeringsprocessen inden for tidsgrænsen for autorisation. Automatisk autorisation understøttes altid i det planlægningsprogram, der er indbygget Supply Chain Management. Hvis du også vil bruge Planlægningsoptimering, skal du aktivere funktionen.

Du kan gøre denne funktion tilgængelig i systemet ved at gå til [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Automatisk autorisation for Planlægningsoptimering*. (Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret.)

## <a name="manually-firm-planned-orders"></a>Autorisere ordreforslag manuelt

Hvis du vil autorisere ordreforslag manuelt, kan du finde og vælge de ordreforslag, du vil autorisere og derefter starte autorisationsprocessen manuelt.

1. [Åbn siden for listen over ordreforslag](approved-planned-order.md#view-planned-orders).
1. Brug feltet **Filter**, **Plan** og kolonneoverskrifterne til at filtrere og sortere listen, så du kan finde de ønskede ordreforslag.
1. Markér afkrydsningsfeltet for hvert ordreforslag, du vil autorisere. Hvis du vil autorisere alle de ordreforslag, der aktuelt vises på siden (baseret på de filtre, du har anvendt), skal du springe dette trin over.
1. Vælg en af følgende knapper i handlingsruden:

    - **Autoriser** – Autoriser kun de valgte ordreforslag.
    - **Autoriser alle** – Autoriserr alle de ordreforslag, der aktuelt vises på siden (baseret på de filtre, du har anvendt), uanset hvilke afkrydsningsfelter der er markerede. Denne indstilling kan være nyttig, hvis du autoriserer mange ordreforslag.

1. Angiv følgende felter i dialogboksen **Autorisation** i oversigtspanelet **Parametre**. (I mange af disse felter tages standardværdierne fra Fanen **Standardopdatering** på siden **Parametre for varedisponering**.)

    - **Opdater markering** – Vælg den politik for lagermarkering, der skal bruges ved autorisation af ordreforslag.
    - **Stop autorisation, hvis der opstår en fejl** – Angiv denne indstilling til *Ja*, hvis du ikke længere vil autorisere alle valgte ordreforlag, hvis der opstår en fejl i et af dem. Denne indstilling skal være angivet til *Nej*, hvis indstillingen **Paralleliser autorisation** er angivet til *Ja*.
    - **Paralleliser autorisation** – Denne indstilling er kun tilgængelig, hvis funktionen [*Parallel autorisation af ordreforslag*](#enable-features) er aktiveret i systemet, og hvis du har valgt to eller flere ordreforslag til autorisation. Angiv det til *Ja*, hvis du vil køre autorisationsprocesserne parallelt. Parallel autorisation kan være med til at forbedre ydeevnen.
    - **Antal tråde** – Denne indstilling er kun tilgængelig, hvis funktionen [*Parallel autorisation af ordreforslag*](#enable-features) er aktiveret i systemet, og hvis du har angivet **Paralleliser autorisation** til *Ja*. Angiv det antal tråde, der skal bruges til parallelisering af autorisationsprocessen. Du kan få flere oplysninger om, hvordan du bruger denne indstilling i varedisponeringen, i [Forbedre ydeevne for varedisponering](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > En værdi på *0* (nul) for feltet **Antal tråde** øger kørselstiden for varedisponeringen. Det anbefales derfor, at du altid angiver dette felt til en værdi, der er mere end 0.

    - **Grupper efter leverandør** – Angiv denne indstilling til *Ja*, hvis du vil gruppere indkøbsordreforslag og oprette én indkøbsordre pr. leverandør under autorisationen. Du kan også oprette én indkøbsordre, der har én linje for hvert ordreforslag.
    - **Gruppér efter købergruppe** – Angiv denne indstilling til *Ja*, hvis du vil gruppere indkøbsordreforslag og oprette én indkøbsordre, som kombinerer leverandør- og købergruppen. Hvis du vil bruge denne indstilling, skal du også angive indstillingen **Gruppér efter leverandør** til *Ja*.
    - **Gruppér efter købsaftale** – Angiv denne indstilling til *Ja* for at gruppere indkøbsordreforslag, der har samme leverandør som eksisterende købsaftaler og oprette én indkøbsordre pr. købsaftale. Denne indstilling aktiveres automatisk, når **Gruppér efter leverandør** aktiveres. Hvis du vil bruge **Gruppér efter købsaftale**, skal **Søg efter købsaftaler** angives til *Ja* på siden **Varedisponeringsparametre**.
    - **Gruppér efter periode** (i sektionen **Indkøbsordrer**) – Vælg den periode, som indkøbsordreforslag skal grupperes efter. Hvis du vil bruge denne indstilling, skal du også vælge indstillingen **Gruppér efter leverandør**.
    - **Gruppér efter periode** (i sektionen **Overførsler**) – Vælg den periode, som overførselsordreforslag skal grupperes efter. Ordrerne grupperes ud fra værdierne for **Fra lagersted** og **Til lagersted**.

    > [!NOTE]
    > Hver af indstillingerne "Gruppér efter" bevirker, at systemet konverterer hvert ordreforslag til en linje i den enkelte indkøbsordre, der er resultatet af gruppering.

    ![Oversigtpanelet Parametre i dialogboksen Autorisation.](./media/manual-firming.png "Oversigtpanelet Parametre i dialogboksen Autorisation")

1. På oversigtspanelet **Kør i baggrunden** skal du konfigurere jobbet, så det kører i batchtilstand. Det giver dog ikke mening at konfigurere en tilbagevendende plan, når du udfører manuel autorisation. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management. Ved manuel autorisation behandler batchjobbet dog kun de aktuelt valgte ordreforslag. De ordrer, som opfylder filtrene, men anvendes på siden i øjeblikket, behandles ikke.
1. Vælg **OK** for at anvende dine indstillinger og generere de autoriserede ordrer.

## <a name="auto-firm-planned-orders"></a>Autorisere ordreforslag automatisk

Ved automatisk autorisation kan du autorisere ordreforslag som del af varedisponeringsprocessen. Du kan definere en tidsgrænse for autorisationen af disponeringsgrupper, individuelle varer og kombinationer af varer og behovsplaner. Under kørsler af behovsplanlægning bliver ordreforslag derefter automatisk spærret, hvis ordredatoen ligger inden for den angivne tidsgrænse for autorisation. Ordreforslag, der genereres via Planlægningsoptimering, og den indbyggede varedisponeringssoperation håndterer ordredatoen (dvs. startdatoen) forskelligt.

> [!NOTE]
> Automatisk autorisation af indkøbsordreforslag kan kun forekomme for varer, der er knyttet til en leverandør.
> 
> Afledte ordrer (dvs. indkøbsordrer for underleverandører), som er autoriserede, har statussen *Til gennemsyn*, hvis sporing af ændringer er aktiveret.

> [!IMPORTANT]
> Inden den funktion, der beskrives i dette afsnit, kan bruges sammen med Planlægningsoptimering, skal funktionen [*Automatisk autorisation for Planlægningsoptimering*](#enable-features) være aktiveret i systemet som beskrevet i starten af dette emne. Automatisk autorisation kan altid bruges med det indbyggede varedisponeringsprogram.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatisk autorisation med Planlægningsoptimering vs. det indbyggede planlægningsprogram

Både Planlægningsoptimering og det indgbyggede planlægningsprogram kan bruges til automatisk autorisation af ordreforslag. Der er dog nogle vigtige forskelle. I Planlægningsoptimering bruges ordredatoen (dvs. startdatoen) til at bestemme, hvilke ordreforslag der skal autoriseres, mens det indbyggede planlægningsprogram bruger behovsdatoen (dvs. slutdatoen). I følgende tabel vises en oversigt over forskellene.

| Funktion | Planlægningsoptimering | Indbygget planlægningsprogram |
|---|---|---|
| **Datobasis** | Automatisk autorisation er baseret på ordredatoen (startdato). | Automatisk autorisation er baseret på behovsdatoen (slutdatoen). |
| **Leveringstid** | Da ordredatoen (startdato) udløser en autorisation, behøver du ikke at overveje leveringstiden som en del af autorisations tidshorisonten. | For at sikre, at ordrer autoriseres rettidigt, skal tidsgrænsen for autorisation være længere end leveringstiden. |
| **Ordrer i den aktuelle uge** | Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal tidsgrænsen for autorisation være én uge. | Hvis du vil autorisere alle ordrer, der skal starte i løbet af den aktuelle uge, skal tidsgrænsen for autorisation ære leveringstiden plus én uge. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Konfigurere automatisk autorisation og tidsgitter for autorisation

Du kan aktivere automatisk autorisation ved at tildele en tidsgrænse for automatisk autorisation til den relevante disponeringsopsætning som beskrevet senere i dette afsnit. Hvis automatisk autorisation ikke er aktiveret for en disponeringsopsætning, eller hvis planlægningen startes fra en bestemt side, f.eks. **Nettobehov** for et frigivet produkt, springes processen for automatisk autorisation over.

Grupperings- og afmærkningsindstillinger for automatisk autorisation henter værdierne fra fanen **Standardopdatering** på siden **Parametre for varedisponering**.

Tidsgrænsen for automatisk autorisation defineres af det antal dage, du angiver for den relevante disponeringsopsætning. Du kan aktivere automatisk autorisation og styre tidsgrænsen på følgende måder:

- Hvis du vil definere en standardtidsgrænse for autorisation for en disponeringsgruppe, skal du gå til **Varedisponering \> Opsætning \> Disponering \> Disponeringsgrupper** og vælge en disponeringsgruppe. Derefter skal du angive antallet af dage i oversigtspanelet **Andet** i feltet **Automatisk autorisationstidshorisont (dage)**.
- Hvis du vil overskrive den tidsgrænse for autorisation, der er defineret for disponeringsgruppen for en bestemt vare, skal du gå til **Administration af produktoplysninger \> Frigivne produkter**. Vælg **Plan** i handlingsruden, og vælg derefter **Varedisponering**. I fanen **Generelt** skal du vælge **Tilsidesæt tidsgrænse** og angive antallet af dage i feltet **Tidsgræsen for automatisk autorisation (dage)**.
- Hvis du vil overskrive den tidsgrænse for autorisation, der er defineret for disponeringsgruppen og varedisponeringen for en bestemt behovsplan, skal du gå til **Varedisponering \> Opsætning \> Behovsplaner** og vælge en behovsplan. Derefter skal du i oversigtspanelet **Tidsgrænse i dage** angive indstillingen **Autorisation** til *Ja* og angive antallet af dage.

Hvis du angiver alle de tidligere nævnte tidsgrænser til *0* (nul), deaktiveres automatisk autorisation helt for de relevante disponerede varer.

## <a name="firm-planned-orders-by-using-a-query"></a>Autorisere ordreforslag ved hjælp af en forespørgsel

Med forespørgselsbaseret autorisation kan du planlægge autorisation ud fra kriterier, der er defineret på forhånd. I modsætning til automatisk autorisation giver forespørgselsbaseret autorisation mulighed for automatisk autorering af forskellige undersæt af ordrer på forskellige tidspunkter. Du kan desuden bruge manuelle eller automatiske operationer til at autorisere forskellige typer ordreforslag. Du kan også få vist, hvilke autoriserede ordrer der er valgt ud fra dine indstillinger. Du kan derfor bekræfte, at valget opfylder dine forventninger.

Du kan kombinere automatisk autorisation med forespørgselsbaseret autorisation. Et forespørgselsbaseret autorisationsjob har f.eks. en fremskrevet tidsgrænse, der er længere end tidsgrænsent for en tilsvarende konfiguration af automatisk auto-autorisation af varedisponering. Derfor behandler det forespørgselsbaserede autorisationsjob ordreforslag, inden den automatiske autorisation startes. Du kan bruge denne funktion til at planlægge ordrer for bestemte leverandører på en anden måde end ordrer på lignende produkter fra andre leverandører.

> [!IMPORTANT]
> Inden den funktion, der beskrives i dette afsnit, kan bruges sammen med funktionen [*Autorisation af ordreforslag med filtrering*](#enable-features), skal den aktiveres i systemet som beskrevet i starten af dette emne.

Hvis du vil autorisere et ordreforslag ved hjælp af den forespørgselsbaserede autorisationsproces, skal du benytte følgende fremgangsmåde.

1. Gå til **Varedisponering \> Varedisponering \> Kør \> Autorisation af ordreforslag**.
1. Angiv de grundlæggende indstillinger for behandling, afmærkning og gruppering i dialogboksen **Autorisation af ordreforslag** i oversigtpanelet **Parametre**. Disse indstillinger fungerer på samme måde som i dialogboksen **Autorisation**. (Se forrige afsnit for at få en beskrivelse). Derefter skal du i sektionen **Plan** angive følgende felter, der er entydige for dialogboksen **Autorisation af ordreforslag**:

    - **Plan** – Vælg den behovsplan, der skal anvendes ved autorisation af de ordreforslag, der findes i denne forespørgsel.
    - **Dage fremad for autorisations tidsgrænse** – Vælg, hvor lang tid fremad de forskellige krav og andre forhold skal beregnes i varedisponeringen.
    - **Dage bagud for autorisations tidsgrænse** – Vælg, hvor langt tilbage de forskellige krav og andre forhold skal beregnes i varedisponeringen.

    ![Oversigtpanelet Parametre i dialogboksen Autorisation af ordreforslag.](./media/planned-order-firming-main-1.png "Oversigtpanelet Parametre i dialogboksen Autorisation af ordreforslag")

1. Hvis du vil angive, hvilke poster der skal medtages i ordren, skal du vælge knappen **Filter** i oversigtspanelet **Poster, der skal indgå**. Der vises en standarddialogboks for forespørgsler, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Supply Chain Management. Felterne her er skrivebeskyttede og viser værdier, der er relateret til forespørgslen.

    ![Oversigtpanelet Poster, der skal indgå i dialogboksen Autorisation af ordreforslag.](./media/planned-order-firming-main-2.png "Oversigtpanelet Poster, der skal indgå i dialogboksen Autorisation af ordreforslag")

1. Vælg **Forhåndsvisning** for at få vist indholdet af den autoriserede ordre, baseret på dine nuværende indstillinger. Listen over ordreforslag, som vil blive autoriseret, vises som en meddelelse. Du kan derefter justere indstillingerne efter behov, indtil forhåndsvisningen viser den ønskede autoriserede ordre.

    ![Eksempel på forhåndsvisning af autoriseret ordre.](./media/planned-order-firming-preview.png "Eksempel på forhåndsvisning af autoriseret ordre")

    > [!WARNING]
    > Denne funktion autoriserer alle ordreforslag, der opfylder filterkriterierne. Ukritisk autorisation af ordreforslag kan det medføre, at der oprettes uønskede indkøbs-, flytte- og produktionsordrer. Før du fortsætter, skal du altid bruge knappen **Forhåndsvisning** til at validere de poster, der vil blive medtaget.

1. På oversigtspanelet **Kør i baggrunden** skal du konfigurere jobbet, så det kører i batchtilstand, og/eller konfigurere en tilbagevendende tidsplan. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK** for at anvende dine indstillinger og generere de autoriserede ordrer.

## <a name="track-firmed-orders"></a>Spore autoriserede ordrer

Hvis du vil spore et ordreforslag, der er blevet autoriseret, skal du benytte følgende fremgangsmåde.

1. [Åbn siden for listen over ordreforslag](approved-planned-order.md#view-planned-orders).
1. Åbn eller vælg det ordreforslag, som du vil spore.
1. Vælg **Autorisationshistorik** under fanen **Vis** i gruppen **Vis** i handlingsruden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
