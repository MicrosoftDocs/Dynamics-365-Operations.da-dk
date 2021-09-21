---
title: Opfyldning af sikkerhedslager for varer
description: I dette emne beskrives opfyldning af sikkerhedslageret, og hvordan du kan konfigurere antallet af varer på sikkerhedslageret.
author: thethehelga
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-oldolg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 28f902c589cd80f1c34dc2758232548309db9aca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474622"
---
# <a name="safety-stock-fulfillment-for-items"></a>Opfyldning af sikkerhedslager for varer

[!include [banner](../includes/banner.md)]

Et sikkerhedslager er en ekstra beholdning af en vare, der opbevares på lageret, for at reducere risikoen for, at varen bliver udsolgt fra lageret. Sikkerhedslageret bruges som et bufferlager i tilfælde af indgående salgsordrer, hvor leverandøren ikke er i stand til at levere de ekstra varer, der kræves for at overholde kundens ønskede afsendelsesdato. Når sikkerhedslageret bruges til at opfylde en salgsordre, reduceres sikkerhedslageret. Du kan bruge Varedisponering til automatisk at føre lageret tilbage til niveauet for sikkerhedsbeholdningen.

## <a name="set-up-safety-stock-levels-for-items"></a>Konfigurere niveauer for sikkerhedslagerbeholdninger af varer

Sikkerhedslageret konfigureres som en del af varedisponeringen på siden **Varedisponering** under **Frigivne produkter \> Plan \> Dækning**.

I feltet **Minimum** skal du angive det niveau for sikkerhedslagerbeholdningen, som du vil opretholde for varen. Værdien er udtrykt i lagerenheder. Hvis du ikke udfylder feltet, er standardværdien nul. Dette felt er tilgængeligt, når du vælger **Periode**, **Behov** eller **Min./Maks.** i oversigten **Disponeringskode**. Niveaugrænsen for sikkerhedslagerbeholdningen gælder for den disponible beholdning, hvilket betyder, at reservationer og mærkning kan udløse genopfyldningen af sikkerhedslageret, før det fysiske antal er reduceret til under det angivne minimumsniveau.

> [!NOTE]
> Du skal definere alle andre disponerede dimensioner, før du kan definere feltet **Minimum**. Dette forhindrer, at der bruges en ugyldig post under varedisponering. Denne situation kan f.eks. opstå, hvis en dimensionsgruppe udvides med en ekstra disponeret dimension, der endnu ikke er defineret minimum- og maksimumlagermængder for.

Du kan bruge minimumnøgler til at tage højde for sæsonbetingede forskelle i efterspørgsel. Du kan f.eks. sænke minimumlagerniveauet for en vare uden for sæsonen og øge niveauet trinvist i de andre måneder. Du kan oprette en minimumsnøgle ved at gå til **Varedisponering \> Opsætning \> Dækning \> Minimums-/maksimumnøgler**. Du kan angive minimumsnøglen for at justere niveauet for sikkerhedslagerbeholdningen ud fra sæsonudsving i feltet **Minimumsnøgle** på siden **Varedisponering**.

## <a name="example-minimum-key"></a>Eksempel: Minimumsnøgle

Følgende procedure er et eksempel på, hvordan du definerer en minimumsnøgle, der viser, hvordan sæsonbetinget efterspørgsel øges i sommer- og sommermånederne.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Minimums-/maksimumnøgler**.
1. Vælg **Ny** for at oprette en Minimums-/maksimumnøgle.
1. Angiv et id for nøglen i feltet **Minimums-/maksimumnøgle**. Angiv et navn til nøglen i feltet **Navn**.
1. Angiv indstillingen **Brug ikrafttrædelsesdatoen** til *Ja*, og lad feltet **Ikrafttrædelsesdato** være tomt, så nøglen er gyldig fra den første dag i det indeværende år.

    > [!NOTE]
    > Kombinationen af indstillingerne for **Brug ikrafttrædelsesdato** og **ikrafttrædelsesdato** definerer den dato, som nøglen gælder fra.
    >
    > - Når indstillingen **Brug ikrafttrædelsesdato** er angivet til *Nej*, er nøglen gyldig fra dags dato eller systemdatoen.
    > - Når indstillingen for **Brug ikrafttrædelsesdato** er indstillet til *Ja*, er nøglen gyldig fra den dato, der er defineret i feltet **Ikrafttrædelsesdato**.

1. I afsnittet **Perioder** skal du oprette 12 linjer og angive følgende værdier for dem:

    - **Ændring** – Tildel et entydigt nummer til hver linje fra 1 til 12. Dette felt angiver den trinvise ændring i den tidsenhed, der er defineret i feltet **Enhed**.
    - **Enhed** – Vælg *måneder* for hver linje.
    - **Fra dato**, **Til dato** og **Måned** – Disse felter angives automatisk på basis af indstillingerne for **ændring** og **enhed**. Månedlige perioder starter fra den første dag i det indeværende år.
    - **Faktor** – Angiv de værdier, der er beskrevet i følgende tabel. Dette felt definerer den faktor, som minimumlageret skal ganges med.

        | Linje (Ændring) | Faktor | Resultat |
        |---|---|---|
        | 1-3 | 1 | Minimumslageret er baseret på indstillingen for januar til marts på siden **Varedisponering**. |
        | 4-5 | 2 | Minimumslager ganges med faktor 2 for april og maj. |
        | 6-8 | 2.5 | Minimumslager ganges med faktor 2,5 for juni til og med august. |
        | 9-12 | 1 | Minimumslageret går tilbage til indstillingen på siden **Varedisponering** for september til og med december. |

    Indstillingerne skal nu ligne indstillingerne i følgende illustration.

    ![Minimum- eller maksimumnøgleperioder.](media/min-max-key-periods.png "Minimum- eller maksimumnøgleperioder")

> [!NOTE]
> Du kan også bruge denne guide til at oprette en minimums-/maksimumsnøgle. Vælg **guiden** for at åbne guiden **Minimums-/maksimumsnøgler** i handlingsruden på siden **Minimums- eller maksimumsnøgler**. Guiden fører dig trinvist gennem processen til oprettelse og konfiguration af minimums-/maksimumsnøglen.

Hvis disponeringskoden er *Min./Maks*, du kan også angive det maksimum-lagerantal, du vil opretholde for varen på lageret. Værdien er også udtrykt i lagerenheder. Hvis den forventede disponible beholdning falder under det minimale antal, oprettes der et ordreforslag under varedisponeringen til dækning af alle åbne behov, og den disponible lagerbeholdning føres op til det angivne maksimale antal. På samme måde som du konfigurerer minimum, skal du definere alle andre disponerede dimensioner, før du kan definere feltet **Maksimum**.

## <a name="example-minmax-coverage-code"></a>Eksempel: Min./Maks disponeringskode

Minimumantallet er 10, og maksimumantallet er 15. Den aktuelle disponible lagerbeholdning er 4. Det giver et minimalt antalsbehov på 6. Men da det maksimale antal er 15, oprettes der et ordreforslag på 11 varer ved varedisponeringen.

For varer, der følger sæsonbestemt efterspørgsel, skal du muligvis angive andre niveaumaksimumværdier. For at gøre det skal du definere **Maksimumsnøgler** ved at gå til **Varedisponering \> Opsætning \> Dækning \> Minimums/maksimumsnøgler**. Udfyld feltet **Maksimumsnøgle** på siden **Varedisponering**. Du kan få vist oplysninger om niveauet for sikkerhedslagerbeholdningerne, defineret via minimumsnøgler, under fanen **Min./Maks** på siden **Varedisponering**. Du skal sørge for, at de minimale og maksimale værdier holdes synkroniserede i en bestemt periode.

## <a name="safety-stock-fulfillment"></a>Opfyldning af sikkerhedslager

Med parameteren **Opfyld minimum** kan du vælge den dato eller den tidsperiode, hvor lagerniveauet mindst skal udgøre det antal, du har angivet i feltet **Minimum**. Dette felt er tilgængeligt, når du vælger **Periode**, **Behov** eller **Min./Maks.** i oversigten **Disponeringskode**.

Hvis **Minimumsnøgler** bruges, skal du markere afkrydsningsfeltet **Minimumsperioder** for at opfylde det minimale lagerniveau for alle perioder, der er defineret i minimumsnøglen. Hvis markeringen i afkrydsningsfeltet fjernes, opfyldes minimumlagerbeholdningen kun for den aktuelle periode.

Følgende eksempel viser, hvordan denne parameter fungerer, og hvad forskellen er mellem værdierne.

> [!NOTE]
> I alle illustrationer i dette emne repræsenterer x-aksen lager, y-aksen repræsenterer dage, søjlerne repræsenterer lagerniveauet, og pilene repræsenterer posteringer, f.eks. salgsordrelinjer, indkøbsordrelinjer eller ordreforslag.

[![Almindeligt scenarie for opfyldning af sikkerhedslager.](media/Scenario1.png)](media/Scenario1.png)

Parameteren **Opfyld minimum** kan have følgende værdier:

### <a name="todays-date"></a>Dags dato

Det angivne minimumantal opfyldes på den dato, hvor varedisponeringen køres. Systemet forsøger at opfylde sikkerhedslagergrænsen så hurtigt som muligt, selvom det kan være urealistisk på grund af gennemløbstiden.

[![Krav for dags dato.](media/TodayReq.png)](media/TodayReq.png)

Ordreforslaget P1 oprettes for dags dato for at bringe lagerbeholdningen over sikkerhedslagerniveauet på denne dato. Salgsordrelinjerne S1 til S3 fortsætter med at reducere lagerbeholdningen. Ordreforslagene P2 til P4 genereres af varedisponering, så lagerniveauet føres tilbage til sikkerhedsgrænsen efter hvert salgsordrebehov.

Når disponeringskoden **Behov** bruges, oprettes der flere ordreforslag. Det er altid en god ide at bruge enten **Periode** eller **Min./Maks**-disponering for varer og materialer, som der er hyppigt behov for, for at bundte genopfyldningen. I følgende illustration vises et eksempel på disponeringskoden **Periode**.

[![Periode. Dags dato.](media/TodayPeriod.png)](media/TodayPeriod.png)

I følgende illustration vises et eksempel på disponeringskoden **Min./Maks.**

[![Min/Maks. Dags dato.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Dags dato + fremskaffelsestid

Det angivne minimumantal opfyldes på den dato, hvor varedisponeringen køres, plus købs- eller produktionsgennemløbstid. Dette tidsrum omfatter sikkerhedsmargener. Hvis varen er underlagt en samhandelsaftale og afkrydsningsfeltet **Søg købsprisaftaler** er markeret på siden **Varedisponeringsparametre**, tages leveringstiden fra samhandelsaftalen ikke i betragtning. Leveringstiderne hentes fra indstillingerne for varedisponeringen eller fra varen.

Denne opfyldningstilstand opretter planer med mindre forsinkelser og færre ordreforslag, uanset hvilken disponeringsgruppe der er konfigureret for varen.

I følgende illustration vises resultatet af planen, hvis disponeringskoden er **Behov** eller **Periode**.

[![Behov. eller Periode. Dags dato og gennemløbstid.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

I følgende illustration vises resultatet af planen, hvis disponeringskoden er **Min./Maks.**

[![Min/Maks. Dags dato og gennemløbstid.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Første afgang

Det angivne minimumsantal opfyldes på den dato, hvor den disponible beholdning går under det laveste niveau, som vist i følgende illustration. Selvom den disponible lagerbeholdning er lavere end minimumniveauet på den dato, hvor varedisponering køres, forsøger **Første afgang** ikke at dække den, før næste behov går ind.

I følgende illustration vises et eksempel på disponeringskoden **Behov**.

[![Planlægning af en vare med Behov-disponeringskode og Første afgang-opfyldning.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

I følgende illustration vises et eksempel på disponeringskoden **Periode**.

[![Planlægning af en vare med Periode-disponeringskode og Første afgang-opfyldning.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

I følgende illustration vises et eksempel på disponeringskoden **Min./Maks.**

[![Planlægning af en vare med MinMax-disponeringskode og Første afgang-opfyldning.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

På den dato, hvor varedisponering køres, hvis den disponible lagerbeholdning allerede er under sikkerhedslagergrænsen, udløser **Dags dato** og **Dags dato + fremskaffelsestid** genopfyldningen med det samme. **Første afgang** venter, indtil der er en anden afgangspostering, som f.eks. en salgsordre- og styklistelinjebehov for varen, og derefter udløser den genopfyldningen på datoen for denne postering.

Hvis den disponible lagerbeholdning ikke er under sikkerhedslagergrænsen på den dato, hvor varedisponering køres, giver **Dags dato** og **Første afgang** nøjagtigt det samme resultat som vist i illustrationen nedenfor.

[![Ikke under grænse.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Hvis den disponible lagerbeholdning ikke er under sikkerhedslagergrænsen på den dato hvor varedisponering køres, giver **Dags dato + fremskaffelsestid** følgende resultat, da det udsætter opfyldningen, indtil den slutningen af leveringstiden for indkøb.

![Opfyldning udsat til slutningen af indkøbs leveringstiden.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Disponeringstidshorisont

Det angivne minimumantal opfyldes inden for den periode, der er angivet i feltet **Tidshorisontdato**. Denne indstilling er nyttig, når Varedisponering ikke tillader, at den disponible beholdning bruges til faktiske ordrer, f.eks. salg eller overførsler, i et forsøg på at opretholde sikkerhedsniveauet. Dog vil denne genopfyldningstilstand ikke længere være nødvendig i en senere version, og denne indstilling vil være forældet.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Planlægge genopfyldningen af sikkerhedslageret for FEFO-varer (First Expired, First Out)

Lagertilgangen med den seneste udløbsdato bruges på et hvilket som helst tidspunkt som sikkerhedslager for at tillade, at faktiske behov, som f.eks. salgslinjer og styklistelinjer, bliver opfyldt i FEFO-rækkefølge.

Følgende eksempel kan give en ide om, hvordan dette fungerer.

[![FEFO-scenarie.](media/FEFOScenario.png)](media/FEFOScenario.png)

Når du kører planlægningen, dækker den den første salgsordre fra den eksisterende disponibel lagerbeholdning og en ekstra indkøbsordre for det resterende antal.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Der oprettes et ordreforslag for at sikre, at den disponible beholdning bringes tilbage til sikkerhedsgrænsen.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Når den anden salgsordre er planlagt, bruges det tidligere oprettede ordreforslag, der dækker sikkerhedslageret, til at dække dette antal. Det vil sige, at sikkerhedslageret hele tiden forandres.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Til sidst oprettes et andet ordreforslag til dækning af sikkerhedslageret.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Alle batches udløber i overensstemmelse hermed, og der oprettes ordreforslag for at genopfylde sikkerhedslageret, når det er udløbet.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Sådan håndteres sikkerhedslagerets begrænsning i Varedisponering

Sikkerhedslageret spores i systemet som en kravtype ligesom salgslinjer eller styklistekrav. Du kan se behovslinjen for sikkerhedslageret på siden **Nettobehov**, hvis du fjerner standardfilteret på kolonnen **Kravtype**.

Transaktionen til opfyldning af sikkerhedslagerbehovet nedprioriteres, hvis systemet registrerer, at dette giver forsinkelser i opfyldelsen af reelle behov, f.eks. salgslinjer, styklistelinjer, flyttebehov eller behovsprognoselinjer. Ellers har det samme prioritet at sørge for, at den disponible lagerbeholdning er over sikkerhedslageret som ved alle andre kravtyper. Dette sikrer, at der ikke er forsinkelser på faktiske transaktioner og hjælper med at forhindre at overgenopfyldning og for tidlig genopfyldning af sikkerhedslageret.

Sikkerhedslageropfyldning er ikke længere nedprioriteret i disponeringsfasen af varedisponeringen. Den disponible lagerbeholdning kan bruges før eventuelle andre efterspørgselsestyper. Under beregningen af forsinkelsen, vil blive føjet nye logik til at gennemgå de forsinkede salgslinjer, behov i styklistelinjer og alle andre behovstyper, for at bestemme, om de kan blive leveret til tiden, forudsat at sikkerhedslageret bruges. Hvis systemet identificerer, at det kan minimere forsinkelser ved hjælp af sikkerhedslageret, erstatter salgslinjerne eller styklistelinjerne deres første disponering med sikkerhedslageret, og systemet udløser genopfyldningen for sikkerhedslageret i stedet.

Hvis planen eller varen ikke er konfigureret til forsinket beregning, har sikkerhedslagerets begrænsning samme prioritet som alle andre efterspørgselstyper. Det betyder, at der er en reserve af disponibel lagerbeholdning og andre disponible beholdninger før andre efterspørgselstyper.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
