---
title: Sikkerhedsmargener
description: Dette emne beskriver, hvordan sikkerhedsmargener kan bruges sammen med tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4982e277dab826f546b0cbef8a66a379bb0f4d94
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469611"
---
# <a name="safety-margins"></a>Sikkerhedsmargener

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan sikkerhedsmargener kan bruges sammen med tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Oversigt over sikkerhedsmargener

Formålet med sikkerhedsmargener er at aktivere en opsætning, der giver en vis buffertid ud over den normale gennemløbstid. Når materialerne f.eks. skal pakkes ud eller inspiceres, efter at de er modtaget fra leverandøren, kan du ikke bare lægge den ekstra tid til indkøbets leveringstid, da denne fremgangsmåde giver den ekstra buffertid til leverandøren. I dette eksempel kan modtagelsesmargenen bruges til at sikre, at leverandøren leverer tidligere. Denne fremgangsmåde giver buffertid, så varerne kan håndteres internt.

Der er tre typer sikkerhedsmargener:

- **Bestillingsmargen** – Buffertiden for afgivelse af forsyningsordren
- **Modtagelsesmargen** – Buffertiden for håndtering af indgående forsyning
- **Afgangsmargen** – Buffertiden for ekspedition af forsendelser

I følgende illustration vises, hvordan disse sikkerhedsmargener anvendes over tid.

![Sikkerhedsmargener.](media/safety-margins-1.png)

Alle margener defineres i dage. Standardværdieb på *0* (nul) angiver, at ingen standardmargen bruges. Hvis du konfigurerer flere margener, vil de alle blive føjet til den samlede tid fra forsyningens *ordredato* til *behovsdatoen*. En opsætning har f.eks. ikke en leveringstid, og alle tre margentyper er angivet til én dag. I dette tilfælde vil der være tre dage mellem forsyningens ordredato og behovsdatoen, så hvis ordredatoen er 1. juli, vil behovsdatoen være den 4.

### <a name="receipt-margin"></a>Modtagelsesmargen

Modtagelsesmargen er sandsynligvis den mest anvendte af de tre sikkerhedsmargener. Den anvendes på *leveringsdatoen* og bagud fra *behovsdatoen*. Produkterne bør med andre ord modtages i det angivne antal dage inden for modtagelsesmargen, før de er påkrævet.

I følgende illustration fremhæves modtagelsesmargenen.

![Modtagelsesmargen.](media/safety-margins-2.png)

Modtagelsesmargenen bruges typisk som en buffer til at sikre tid nok til lagerregistrering eller andre tidskrævende processer, der ikke medtages som en del af den generelle leveringstid i systemet. I forbindelse med indkøb er det en fordel, at *leveringsdatoen* for indkøbsordren flyttes tilsvarende. Hvis du øger leveringstiden i stedet for at bruge en sikkerhedsmargen, bliver leverandøren stadig bedt om at levere i sidste øjeblik.

Bemærk, at modtagelsesmargenen ikke ændrer *behovsdatoen* for forsyningen. Derfor er modtagelsesmargenen ikke direkte synlig, når behovsdatoer for udbud og efterspørgsel sammenlignes (f.eks. på siden **Nettobehov**). Hvis modtagelsesmargenen f.eks. er angivet til fire dage, og en indkøbsordrelinje er planlagt til modtagelse den 15. i måneden, beregner behovsplanlægningen den justerede modtagelsesdato som den 19. i måneden.

Bemærk, at der ikke anvendes modtagelsesmargen, når der bruges en disponibel lagerbeholdning som forsyning. Alle disponible lagerbeholdninger antages at være til rådighed med det samme, uanset hvornår den faktisk blev modtaget.

### <a name="reorder-margin"></a>Bestillingsmargen

I følgende illustration fremhæves bestillingsmargen.

![Bestillingsmargen.](media/safety-margins-3.png)

Bestillingsmargen lægges til før varens leveringstid for alle ordreforslag under behovsplanlægning. Derfor sikrer den, at der er mere tid til at afgive en forsyningsordre. Denne margen bruges typisk som en buffer til at sikre tid nok til godkendelsesprocesser eller andre interne processer, der er nødvendige i forbindelse med oprettelsen af forsyningsordrer. Bestillingsmargenen sættes mellem forsyningens *ordredato* og *startdato*.

### <a name="issue-margin"></a>Afgangsmargen

I følgende illustration fremhæves afgangsmargen.

![Afgangsmargen.](media/safety-margins-4.png)

Afgangsmargenen trækkes fra behovsdatoen ved varedisponering. Det er med til at sikre, at du har tid til at reagere på og afsende indgående behovsordrer. Denne margen bruges typisk som en buffer til at sikre tid til forsendelse og relaterede udgående lagerprocesser.

Bemærk, at de relaterede udbud og efterspørgselskrav ikke stemmer overens, når der anvendes en afgangsmargen. De afviger i stedet med afgangsmargenen, fordi afgangsmargenen tilføjes mellem forsyningens *behovsdato* og efterspørgslens *behovsdato*.

## <a name="set-up-safety-margins"></a>Angive sikkerhedsmargener

### <a name="turn-on-safety-margins-in-feature-management"></a>Slå sikkerhedsmargener til i Funktionsstyring

Før du kan bruge denne funktion sammen med Planlægningsoptimering, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** _Varedisponering_
- **Funktionsnavn:** _Margener for planlægningsoptimering_

### <a name="define-safety-margins"></a>Definere sikkerhedsmargener

Sikkerhedsmargener har en fleksibel opsætning. De kan angives for både *disponeringsgruppe* og *behovsplan*. Det er vigtigt, at du forstår, at margenerne lægges sammen oven på hinanden. En modtagelsesmargen på to dage i disponeringsgruppen og tre dage på behovsplanen vil f.eks. give en faktisk modtagelsesmargen på fem dage.

Muligheden for at angive margen på behovsplanen kan være nyttig, når du vil simulere længere leveringstider eller usikkerhed for en bestemt plan, men uden at påvirke den daglige planlægning.

#### <a name="coverage-group-safety-margins"></a>Sikkerhedsmargener for disponeringsgruppe

Hvis du vil anvende en sikkerhedsmargen på en disponeringsgruppe, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Disponeringsgrupper**.
1. Vælg den ønskede disponeringsgruppe i listeruden.
1. I sektionen **Sikkerhedsmargener i dage** i oversigtspanel **Andet** skal du bruge følgende felter til at angive de nødvendige sikkerhedsmargener (i dage):

    - Modtagelsesmargen lagt til behovsdato
    - Afgangsmargen trukket fra behovsdato
    - Bestillingsmargen tilføjet til varens leveringstid

#### <a name="master-plan-safety-margins"></a>Sikkerhedsmargener for behovsplan

Hvis du vil anvende en sikkerhedsmargen på en behovsplan, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg den ønskede behovsplan i listeruden.
1. I oversigtspanelet **Sikkerhedsmargener i dage** skal du bruge følgende felter til at angive de nødvendige sikkerhedsmargener (i dage):

    - Modtagelsesmargen lagt til behovsdato
    - Afgangsmargen trukket fra behovsdato
    - Bestillingsmargen tilføjet til varens leveringstid

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Angive, om beregninger er baseret på kalenderdage eller arbejdsdage

Du kan angive alle sikkerhedsmargener, så de beregnes på basis af enten kalenderdage eller arbejdsdage.

1. Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**.
1. Under fanen **Generelt** skal du i afsnittet **Sikkerhedsmargener i dage** angive indstillingen **Arbejdsdage** til *Ja* for at beregne margener baseret på arbejdsdage. Angiv indstillingen til *Nej* for at beregne margener baseret på kalenderdage.

En kalender kan f.eks. være åben fra mandag til fredag og være lukket lørdag og søndag. Hvis der er en modtagelsesmargen på én dag, opretter en behovsdato på en mandag en leveringsdato på den forrige fredag, fordi lørdag og søndag ikke er arbejdsdage.

Den kalender, der bruges til at bestemme arbejdsdage, afhænger af opsætningen og forsyningstypen. Den kan styres af kalenderne i disponeringsgruppen, lagerstedet og leverandøren.

> [!NOTE]
> Hvis *lagerstedet* ikke indgår i disponeringsdimensionen (dvs. planlægningen kun er baseret på *lokationen*), bruges lagerstedskalenderen ikke.

Systemet kan håndtere en opsætning, hvor der er defineret en eller flere kalendere. I følgende underafsnit beskrives de mulige kombinationer, der kan bruges til at kontrollere resultatet.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalender, der bruges til varigheden

De definerede kalendere styrer den faktiske samlede leveringstid i kalenderdage fra forsyningsordredatoen til behovsdatoen. Følgende kalenderprioritering bruges:

- **Leveringstid for indkøb** – Det er kun disponeringsgruppekalenderen, der tages i betragtning.
- **Modtagelsesmargen** – Der bruges en disponeringsgruppekalender, hvis den er defineret. Ellers bruges lagerstedskalenderen.
- **Afgangsmargen** – Der bruges en disponeringsgruppekalender, hvis den er defineret. Ellers bruges lagerstedskalenderen.
- **Ordremargen** – Det er kun disponeringsgruppekalenderen, der tages i betragtning.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalender, der bruges til slutdatoen

Følgende regler bruges til at bestemme, om planlægningsprogrammet kan bruge en bestemt dato for en given datotype:

- **Modtagelsesdato for indkøb** – Leverandørkalenderen bruges, hvis den er defineret. Ellers bruges disponeringsgruppekalenderen, hvis den er defineret. Hvis ingen af disse kalendere er defineret, bruges lagerstedskalenderen.
- **Modtagelsesdato for flytteordre** – Der bruges en disponeringsgruppekalender, hvis den er defineret. Ellers bruges lagerstedskalenderen.
- **Modtagelsesdato for produktion** – Der bruges en disponeringsgruppekalender, hvis den er defineret. Ellers bruges lagerstedskalenderen.
- **Åbningsdag for behovsafgang** – Der bruges en lagerstedskalender, hvis den er defineret. Ellers bruges disponeringsgruppekalenderen.
- **Åbningsdag for ordre** – En kombination (skæringspunkt) af disponeringsgruppekalenderen og leverandørkalenderen bruges. Begge kalendere skal være åbne for at kunne bruge datoen. Hvis kun en af disse kalendere er defineret, bruges kalenderen alene.

#### <a name="calendar-setup-overview-matrix"></a>Oversigtsmatrix for kalenderopsætning

I følgende illustration vises en matrix, der opsummerer, hvilke kalendere der anvendes, når der beregnes sikkerhedsmargener. (Vælg billedet for at åbne en version af det med høj opløsning). Følgende forkortelser og farver bruges til at angive, hvor de enkelte typer kalendere er specificeret:

- **Disponeringsgruppe (CG):** grøn
- **Lagersted (WH):** gul
- **Leverandør (V):** blå

[![Oversigtsmatrix for kalenderopsætning.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Beregning af forsinkelser

Alle tre typer sikkerhedsmargener medtages, når systemet bestemmer, om en ordre er forsinket.

En vare har f.eks. en leveringstid på én dag og en modtagelsesmargen på tre dage. En salgsordre for denne vare angives som påkrævet i dag. I dette tilfælde beregnes forsinkelsen som *leveringstid* + *modtagelsesmargen* = fire dage. Hvis dags dato f.eks. er 14. august, skaber de fire dages forsinkelse en levering den 18. august. Følgende illustration viser dette eksempel.

![Eksempelberegning af forsinkelse.](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Start her med planlægningsoptimering](get-started.md)

[Analyse af tilpasning af planlægningsoptimering](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]