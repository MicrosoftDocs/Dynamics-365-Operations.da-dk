---
title: Opfyldning af sikkerhedslager for varer
description: I dette emne beskrives opfyldning af sikkerhedslageret, og hvordan du kan konfigurere antallet af varer på sikkerhedslageret.
author: roxanadiaconu
manager: tfehr
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 7a1721b3206f8a3df010f26dc31e3ac4e5e0878b
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887010"
---
# <a name="safety-stock-fulfillment-for-items"></a>Opfyldning af sikkerhedslager for varer

[!include [banner](../includes/banner.md)]

Et sikkerhedslager er en ekstra beholdning af en vare, der opbevares på lageret, for at reducere risikoen for, at varen bliver udsolgt fra lageret. Sikkerhedslageret bruges som et bufferlager i tilfælde af indgående salgsordrer, hvor leverandøren ikke er i stand til at levere de ekstra varer, der kræves for at overholde kundens ønskede afsendelsesdato. Når sikkerhedslageret bruges til at opfylde en salgsordre, reduceres sikkerhedslageret. Du kan bruge Varedisponering til automatisk at føre lageret tilbage til niveauet for sikkerhedsbeholdningen.    

## <a name="set-up-safety-stock-levels-for-items"></a>Konfigurere niveauer for sikkerhedslagerbeholdninger af varer

Sikkerhedslageret konfigureres som en del af varedisponeringen på siden **Varedisponering** under **Frigivne produkter** > **Plan** > **Disponering**.

I feltet **Minimum** skal du angive det niveau for sikkerhedslagerbeholdningen, som du vil opretholde for varen. Værdien er udtrykt i lagerenheder. Hvis du ikke udfylder feltet, er standardværdien nul. Dette felt er tilgængeligt, når du vælger **Periode**, **Behov** eller **Min./Maks.** i oversigten **Disponeringskode**. Niveaugrænsen for sikkerhedslagerbeholdningen gælder for den disponible beholdning, hvilket betyder, at reservationer og mærkning kan udløse genopfyldningen af sikkerhedslageret, før det fysiske antal er reduceret til under det angivne minimumsniveau.

> [!NOTE]
> Du skal definere alle andre disponerede dimensioner, før du kan definere feltet **Minimum**. Dette forhindrer, at der bruges en ugyldig post under varedisponering. Denne situation kan f.eks. opstå, hvis en dimensionsgruppe udvides med en ekstra disponeret dimension, der endnu ikke er defineret minimum- og maksimumlagermængder for.

Du kan bruge minimumnøgler til at tage højde for sæsonbetingede forskelle i efterspørgsel. Du kan f.eks. sænke minimumlagerniveauet for en vare uden for sæsonen og øge niveauet trinvist i de andre måneder. Du kan oprette en minimumsnøgle ved at gå til **Varedisponering** > **Opsætning** > **Disponering** > **Minimums/maksimumsnøgler**. Du kan angive minimumsnøglen for at justere niveauet for sikkerhedslagerbeholdningen ud fra sæsonudsving i feltet **Minimumsnøgle** på siden **Varedisponering**. 

## <a name="example-minimum-key"></a>Eksempel: Minimumsnøgle
Hvis du vil angive en minimumsnøgle, der står for øget sæsonbetinget efterspørgsel i forårs- og sommermånederne, skal du gå til **Varedisponering** > **Opsætning** > **Disponering** > **Minimums-/maksimumnøgler** og følge disse trin.

1. Opret 12 linjer, og tildel et nummer fra 1 til 12 til linjerne i feltet **Rediger**.
2. Vælg **Måneder** i feltet **Enhed**.
3. I feltet **Faktor** skal du angive de værdier, der er beskrevet i følgende tabel.

|Kurve|Angiv denne værdi|Resultat|
|---|---|---|
|1-3|1|Minimumslageret er baseret på indstillingen for januar til marts på siden **Varedisponering**.|
|4-5|2|Minimumslager ganges med faktor 2 for april og maj.|
|6-8|2,5|Minimumslager ganges med faktor 2,5 for juni til og med august.|
|9-12|1|Minimumslageret går tilbage til indstillingen på siden **Varedisponering** for september til og med december.|

Hvis disponeringskoden er **Min./Maks**, du kan også angive det **Maksimum**-lagerantal, du vil opretholde for varen på lageret. Værdien er også udtrykt i lagerenheder. Hvis den forventede disponible beholdning falder under det minimale antal, oprettes der et ordreforslag under varedisponeringen til dækning af alle åbne behov, og den disponible lagerbeholdning føres op til det angivne maksimale antal. På samme måde som du konfigurerer **Minimum**, skal du definere alle andre disponerede dimensioner, før du kan definere feltet **Maksimum**.

## <a name="example-minmax-coverage-code"></a>Eksempel: Min./Maks disponeringskode
Minimumantallet er 10, og maksimumantallet er 15. Den aktuelle disponible lagerbeholdning er 4. Det giver et minimalt antalsbehov på 6. Men da det maksimale antal er 15, oprettes der et ordreforslag på 11 varer ved varedisponeringen.

For varer, der følger sæsonbestemt efterspørgsel, skal du muligvis angive andre niveaumaksimumværdier. For at gøre det skal du definere **Maksimumsnøgler** ved at gå til **Varedisponering** > **Opsætning** > **Disponering** > **Minimums/maksimumsnøgler**. Udfyld feltet **Maksimumsnøgle** på siden **Varedisponering**. Du kan få vist oplysninger om niveauet for sikkerhedslagerbeholdningerne, defineret via minimumsnøgler, under fanen **Min./Maks** på siden **Varedisponering**. Du skal sørge for, at de minimale og maksimale værdier holdes synkroniserede i en bestemt periode.

## <a name="safety-stock-fulfillment"></a>Opfyldning af sikkerhedslager 

Med parameteren **Opfyld minimum** kan du vælge den dato eller den tidsperiode, hvor lagerniveauet mindst skal udgøre det antal, du har angivet i feltet **Minimum**. Dette felt er tilgængeligt, når du vælger **Periode**, **Behov** eller **Min./Maks.** i oversigten **Disponeringskode**.

Hvis **Minimumsnøgler** bruges, skal du markere afkrydsningsfeltet **Minimumsperioder** for at opfylde det minimale lagerniveau for alle perioder, der er defineret i minimumsnøglen. Hvis markeringen i afkrydsningsfeltet fjernes, opfyldes minimumlagerbeholdningen kun for den aktuelle periode.

Følgende eksempel viser, hvordan denne parameter fungerer, og hvad forskellen er mellem værdierne.

> [!NOTE]
> I alle illustrationer i dette emne repræsenterer x-aksen lager, y-aksen repræsenterer dage, søjlerne repræsenterer lagerniveauet, og pilene repræsenterer posteringer, f.eks. salgsordrelinjer, indkøbsordrelinjer eller ordreforslag.

[![Almindeligt scenarie for opfyldning af sikkerhedslager](./media/Scenario1.png)](./media/Scenario1.png) Parameteren **Opfyld minimum** kan have følgende værdier:
### <a name="todays-date"></a>Dags dato 
Det angivne minimumantal opfyldes på den dato, hvor varedisponeringen køres. Systemet forsøger at opfylde sikkerhedslagergrænsen så hurtigt som muligt, selvom det kan være urealistisk på grund af gennemløbstiden. 
[![Krav for dags dato](./media/TodayReq.png)](./media/TodayReq.png) Ordreforslaget P1 oprettes for dags dato for at bringe lagerbeholdningen over sikkerhedslagerniveauet på denne dato. Salgsordrelinjerne S1 til S3 fortsætter med at reducere lagerbeholdningen. Ordreforslagene P2 til P4 genereres af varedisponering, så lagerniveauet føres tilbage til sikkerhedsgrænsen efter hvert salgsordrebehov.
Når disponeringskoden **Behov** bruges, oprettes der flere ordreforslag. Det er altid en god ide at bruge enten **Periode** eller **Min./Maks**-disponering for varer og materialer, som der er hyppigt behov for, for at bundte genopfyldningen. I følgende illustration vises et eksempel på disponeringskoden **Periode**.
[![Periode. Dags dato](./media/TodayPeriod.png)](./media/TodayPeriod.png) I følgende illustration vises et eksempel på disponeringskoden **Min./Maks.**.
[![MinMax. Dags dato](./media/TodayMinMax.png)](./media/TodayMinMax.png)
### <a name="todays-date--procurement-time"></a>Dags dato + fremskaffelsestid 
Det angivne minimumantal opfyldes på den dato, hvor varedisponeringen køres, plus købs- eller produktionsgennemløbstid. Dette tidsrum omfatter sikkerhedsmargener. Hvis varen er underlagt en samhandelsaftale og afkrydsningsfeltet **Søg købsprisaftaler** er markeret på siden **Varedisponeringsparametre**, tages leveringstiden fra samhandelsaftalen ikke i betragtning. Leveringstiderne hentes fra indstillingerne for varedisponeringen eller fra varen.
Denne opfyldningstilstand opretter planer med mindre forsinkelser og færre ordreforslag, uanset hvilken disponeringsgruppe der er konfigureret for varen. I følgende illustration vises resultatet af planen, hvis disponeringskoden er **Behov** eller **Periode**.  
[![Behov. Periode. Dags dato og gennemløbstid](./media/TodayPLTReq.png)](./media/TodayPLTReq.png) I følgende illustration vises resultatet af planen, hvis disponeringskoden er **Min./Maks.**.  
[![MinMax. Dags dato og gennemløbstid](./media/TodayPLTMinMax.png)](./media/TodayPLTMinMax.png)
### <a name="first-issue"></a>Første afgang 
Det angivne minimumsantal opfyldes på den dato, hvor den disponible beholdning går under det laveste niveau, som vist i følgende illustration. Selvom den disponible lagerbeholdning er lavere end minimumniveauet på den dato, hvor varedisponering køres, forsøger **Første afgang** ikke at dække den, før næste behov går ind.
I følgende illustration vises et eksempel på disponeringskoden **Behov**.
[![Planlægning af en vare med disponeringskoden **Behov** og ordreopfyldningen **Første afgang**](./media/FirstIssueReq.png)](./media/FirstIssueReq.png) I følgende illustration vises et eksempel på disponeringskoden **Periode**.
[![Planlægning af en vare med disponeringskoden **Periode** og ordreopfyldningen **Første afgang**](./media/FirstIssuePeriod.png)](./media/FirstIssuePeriod.png) I følgende illustration vises et eksempel på disponeringskoden **Min./Maks.**.
[![Planlægning af en vare med **Min/Max**-disponeringskode og **Første afgang**-ordreopfyldning](./media/FirstIssueMinMax.png)](./media/FirstIssueMinMax.png) På den dato, hvor varedisponering køres, hvis den disponible lagerbeholdning allerede er under sikkerhedslagergrænsen, udløser **Dags dato** og **Dags dato + fremskaffelsestid** genopfyldningen med det samme. **Første afgang** venter, indtil der er en anden afgangspostering, som f.eks. en salgsordre- og styklistelinjebehov for varen, og derefter udløser den genopfyldningen på datoen for denne postering. Hvis den disponible lagerbeholdning ikke er under sikkerhedslagergrænsen på den dato, hvor varedisponering køres, giver **Dags dato** og **Første afgang** nøjagtigt det samme resultat som vist i illustrationen nedenfor. 

[![NotUnderLimit](./media/ReqFirstIssue.png)](./media/ReqFirstIssue.png) Hvis den disponible lagerbeholdning ikke er under sikkerhedslagergrænsen på den dato hvor varedisponering køres, giver **Dags dato + fremskaffelsestid** følgende resultat, da det udsætter opfyldningen, indtil den slutningen af leveringstiden for indkøb.
![Planlægning af en vare med **Behov**-disponeringskode og **Første afgang**-opfyldning](./media/ReqTodayLT.png)
### <a name="coverage-time-fence"></a>Tidshorisontdato
Det angivne minimumantal opfyldes inden for den periode, der er angivet i feltet **Tidshorisontdato**. Denne indstilling er nyttig, når Varedisponering ikke tillader, at den disponible beholdning bruges til faktiske ordrer, f.eks. salg eller overførsler, i et forsøg på at opretholde sikkerhedsniveauet. Dog vil denne genopfyldningstilstand ikke længere være nødvendig i en senere version, og denne indstilling vil være forældet.
## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Planlægge genopfyldningen af sikkerhedslageret for FEFO-varer (First Expired, First Out)
Lagertilgangen med den seneste udløbsdato bruges på et hvilket som helst tidspunkt som sikkerhedslager for at tillade, at faktiske behov, som f.eks. salgslinjer og styklistelinjer, bliver opfyldt i FEFO-rækkefølge.
Følgende eksempel kan give en ide om, hvordan dette fungerer.
[![FEFOScenario](./media/FEFOScenario.png)](./media/FEFOScenario.png) Når du kører planlægningen, dækker den den første salgsordre fra den eksisterende disponibel lagerbeholdning og en ekstra indkøbsordre for det resterende antal.
[![FEFO1](./media/FEFO1.png)](./media/FEFO1.png) Der oprettes et ordreforslag for at sikre, at den disponible beholdning bringes tilbage til sikkerhedsgrænsen.
[![FEFO2](./media/FEFO2.png)](./media/FEFO2.png) Når den anden salgsordre er planlagt, bruges det tidligere oprettede ordreforslag, der dækker sikkerhedslageret, til at dække dette antal. Det vil sige, at sikkerhedslageret hele tiden forandres.
[![FEFO3](./media/FEFO3.png)](./media/FEFO3.png) Til sidst oprettes et andet ordreforslag til dækning af sikkerhedslageret.
[![FEFO4](./media/FEFO4.png)](./media/FEFO4.png) Alle batches udløber i overensstemmelse hermed, og der oprettes ordreforslag for at genopfylde sikkerhedslageret, når det er udløbet.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Sådan håndteres sikkerhedslagerets begrænsning i Varedisponering

Sikkerhedslageret spores i systemet som en kravtype ligesom salgslinjer eller styklistekrav. Du kan se behovslinjen for sikkerhedslageret på siden **Nettobehov**, hvis du fjerner standardfilteret på kolonnen **Kravtype**.

Transaktionen til opfyldning af sikkerhedslagerbehovet nedprioriteres, hvis systemet registrerer, at dette giver forsinkelser i opfyldelsen af reelle behov, f.eks. salgslinjer, styklistelinjer, flyttebehov eller behovsprognoselinjer. Ellers har det samme prioritet at sørge for, at den disponible lagerbeholdning er over sikkerhedslageret som ved alle andre kravtyper. Dette sikrer, at der ikke er forsinkelser på faktiske transaktioner og hjælper med at forhindre at overgenopfyldning og for tidlig genopfyldning af sikkerhedslageret.

Sikkerhedslageropfyldning er ikke længere nedprioriteret i disponeringsfasen af varedisponeringen. Den disponible lagerbeholdning kan bruges før eventuelle andre efterspørgselsestyper. Under beregningen af forsinkelsen, vil blive føjet nye logik til at gennemgå de forsinkede salgslinjer, behov i styklistelinjer og alle andre behovstyper, for at bestemme, om de kan blive leveret til tiden, forudsat at sikkerhedslageret bruges. Hvis systemet identificerer, at det kan minimere forsinkelser ved hjælp af sikkerhedslageret, erstatter salgslinjerne eller styklistelinjerne deres første disponering med sikkerhedslageret, og systemet udløser genopfyldningen for sikkerhedslageret i stedet.

Hvis planen eller varen ikke er konfigureret til forsinket beregning, har sikkerhedslagerets begrænsning samme prioritet som alle andre efterspørgselstyper. Det betyder, at der er en reserve af disponibel lagerbeholdning og andre disponible beholdninger før andre efterspørgselstyper.
