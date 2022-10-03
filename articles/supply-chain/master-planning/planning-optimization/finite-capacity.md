---
title: Tidsplan og planlægning af kapacitetsbegrænsning
description: Når du planlægger kapacitetsbegrænsning og tidsplaner, kan du bedre forstå, hvor meget arbejde der kan produceres i en bestemt periode, når der tages højde for begrænsninger på forskellige ressourcer.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c5eebe9ef6258b43daa7c7007ee28b0278fe5b09
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573131"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Tidsplan og planlægning af kapacitetsbegrænsning

[!include [banner](../../includes/banner.md)]

Kapacitetsbegrænsning er en metode, der gør det nemmere at forstå, hvor meget arbejde der kan produceres i en bestemt periode, når der tages højde for begrænsninger på forskellige ressourcer. Formålet med planlægning af kapacitetsbegrænsning er at sikre, at arbejdet fortsætter i et jævnt og effektivt tempo i hele anlægget.

Hvis der planlægges kapacitetsbegrænsning, oprettes der en mere realistisk tidsplan for produktionsprocesserne, end den ubegrænsede indlæsningsmetode opretter. Hvis der ikke er tilstrækkelig kapacitet på ressourcerne, rykkes leveringsdatoen, og jobbet planlægges, når der er tilstrækkelig kapacitet.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Understøttelse af planlægningsoptimering til kapacitetsbegrænsning

Planlægning af kapacitetsbegrænsning og tidsplaner fungerer næsten på samme måde, uanset om du bruger Planlægningsoptimering eller det indbyggede planlægningsprogram. Planlægningsoptimering bruger dog ikke parameteren **Flaskehalshorisont**. Når du bruger planlægningsoptimering, planlægges flaskehalsressourcer altid med brug af samme tidshorisont som ikke-flaskehalsressourcer (som angivet i tidshorisonten for kapacitetsbegrænsning).

## <a name="set-up-finite-capacity-functionality"></a>Konfigurere funktionalitet af kapacitetsbegrænsning

Hvis du vil bruge funktionen til kapacitetsbegrænsning, skal du aktivere kapacitetsplanlægning globalt, og du skal aktivere kapacitetsbegrænsning både for den behovsplan, hvor den skal bruges, og for hver ressource, hvor den anvendes. Ved planer og ressourcer, hvor kapacitetsbegrænsning er aktiveret, vil planlægning af produktionsordreforslag tage kapacitet, der allerede er reserveret, med i betragtning. Produktionsordreforslag planlægges bagud fra behovsdatoen. Hvis kapaciteten ikke kan opfylde den optimale tidsplan, vil systemet forsøge at kræve indgående komponenter på en tidligere dato. Hvis kapaciteten kan ændres, efterhånden som kravene ændres (f.eks. når du arbejder med skiftehold), skal du ikke bruge funktionen til kapacitetsbegrænsning, fordi de beregnede behandlingstider ikke er korrekte. Planlægningen tager kun højde for kapacitet, der allerede er reserveret til ressourcer, hvor kapacitetsbegrænsning er aktiveret. Hvis du aktiverer kapacitetsbegrænsning for en ressource, kan du redigere tidshorisonten for kapacitetsbegrænsning.

### <a name="activate-master-planning-parameters"></a>Aktivere varedisponeringsparametre

Hvis du vil bruge funktionen til kapacitetsbegrænsning, skal du aktivere kapacitetsplanlægning på siden **Varedisponeringsparametre**.

1. Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**.
1. Angiv indstillingen **Produktion** til **Ja** i sektionen **Kapacitetsplanlægning** under fanen *Ordreforslag*.

### <a name="activate-a-master-plan"></a>Aktivere en behovsplan

Du skal aktivere planlægning af kapacitetsbegrænsning og tidsplan for hver behovsplan, hvor den skal bruges.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en behovsplan, der skal konfigureres til at bruge kapacitetsbegrænsning ved planlægning, i listeruden.
1. Angiv indstillingen **Kapacitetsbegrænsning** til **Ja** i sektionen **Produktionsordreforslag** i oversigtspanelet *Generelt*.
1. Gentag trin 2 og 3 for hver ekstra behovsplan, du vil konfigurere.

### <a name="activate-resources"></a>Aktivere ressourcer

Du skal aktivere planlægning af kapacitetsbegrænsning og tidsplan for hver ressource, hvor den skal bruges.

1. Gå til **Produktionsstyring \> Opsætning \> Ressourcer \> Ressourcer**.
1. Vælg en ressource, der skal konfigureres til at bruge kapacitetsbegrænsning ved planlægning, i listeruden.
1. I sektionen **Kapacitet** i oversigtspanelet **Operation** skal du vælge *Ja* for indstillingen **Forsinket momsberegning**.
1. Gentag trin 2 og 3 for hver ekstra ressource, du vil konfigurere.

## <a name="examples"></a>Eksempler

Dette afsnit indeholder følgende eksempler, der viser, hvordan du kan arbejde med både ubegrænset og begrænset kapacitet under planlægning:

- Eksempel 1 – Planlægning af ubegrænset kapacitet
- Eksempel 2 – Planlægning af kapacitetsbegrænsning med en tidshorisont på én dag
- Eksempel 3 – Planlægning af kapacitetsbegrænsning med en tidshorisont på to dage

### <a name="preconditions"></a>Betingelser

I alle tre eksempler antages forudsætningerne, der er beskrevet i dette afsnit.

Produktet *Produkt1* har en rute, der indeholder følgende operationer.

| Operationsnr. | Operationsbetegnelse | Ressource        | Procestid | Procesantal | Næste |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Svejsning        | Svejsebånd    | 1        | 2            | 20   |
| 20            | Montering     | Monterebånd | 1        | 4            |      |

Arbejderne i firmaet arbejder i ét skiftehold i otte timer (8.00 til 16:00).

Der er planlagt produktionsordre på *24 stk.* af *Produkt1*. Den har behovsdatoen *I dag + 3 dage*.

På grund af planlægningen indlæses ressourcerne på følgende måde:

- **Svejsebånd:** Denne ressource lastes fra *I dag kl. 8:00* til *I dag + 1 kl. 12:00*.
- **Monterebånd:** Denne ressource lastes fra *I dag + 1 kl. 12:00* til *I dag + 2 kl. 10:00*.

I følgende illustration vises det Gantt-diagram, der er resultatet (vælg det for at få større visning).

[![Gantt-diagram, der viser forudsætninger.](media/finite-examples-conditions-small.png "Gantt-diagram, der viser forudsætninger")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Eksempel 1 – Planlægning af ubegrænset kapacitet

Dette eksempel viser planlægningsresultaterne, når du bruger ubegrænset kapacitetsplanlægning i stedet for kapacitetsbegrænsning.

Behovsplanen har følgende relevante indstilling, hvilket deaktiverer kapacitetsbegrænsning under planlægningen:

- **Kapacitetsbegrænsning:** *Nej*

Indstillingen **Kapacitetsbegrænsning** er også angivet til *Nej* for begge relevante ressourcer for at deaktivere planlægning af kapacitetsbegrænsning for dem:

- Svejsebånd
- Monterebånd

Du tilføjer nu en ny salgsordre på *8 stk.* af *Produkt1* og kører planen. Som følge heraf indlæser systemet svejsebåndet fra *I dag kl. 8:00* til *I dag kl. 12:00*. Når operationerne på svejsebåndet er fuldført, indlæses monterebåndet fra *I dag kl. 12:00* til *I dag kl. 14:00*.

I følgende illustration vises det Gantt-diagram, der er resultatet (vælg det for at få større visning).

[![Gantt-diagram med et eksempel på ubegrænset kapacitetsplanlægning.](media/finite-examples-example1-small.png "Gantt-diagram med et eksempel på ubegrænset kapacitetsplanlægning")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Eksempel 2 – Planlægning af kapacitetsbegrænsning med en tidshorisont på én dag

Dette eksempel viser planlægningsresultaterne, når du bruger begrænset kapacitetsplanlægning og en tidshorisont på én dag.

Behovsplanen har følgende relevante indstillinger, hvilket aktiverer kapacitetsbegrænsning og angiver en tidshorisont for planen:

- **Kapacitetsbegrænsning:** *Ja*
- **Tidshorisont for kapacitetsbegrænsning:** *1*

Indstillingen **Kapacitetsbegrænsning** er også angivet til *Ja* for begge relevante ressourcer for at aktivere planlægning af kapacitetsbegrænsning for dem:

- Svejsebånd
- Monterebånd

Du tilføjer nu en ny salgsordre på *8 stk.* af *Produkt1* og kører planen. Som følge heraf indlæser systemet svejsebåndet fra *I dag + 1 kl. 8:00* til *I dag + 1 kl. 12:00*. Når operationerne på svejsebåndet er fuldført, indlæses monterebåndet fra *I dag +1 kl. 12:00* til *I dag + 1 kl. 14:00*. Systemet tager kun højde for kapacitetsbegrænsning én dag.

I følgende illustration vises det Gantt-diagram, der er resultatet (vælg det for at få større visning).

[![Gantt-diagram, der viser planlægning af kapacitetsbegrænsning med en tidshorisont på én dag.](media/finite-examples-example2-small.png "Gantt-diagram, der viser planlægning af kapacitetsbegrænsning med en tidshorisont på én dag")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Eksempel 3 – Planlægning af kapacitetsbegrænsning med en tidshorisont på to dage

Dette eksempel viser planlægningsresultaterne, når du bruger begrænset kapacitetsplanlægning og en tidshorisont på to dage.

Behovsplanen har følgende relevante indstillinger, hvilket aktiverer kapacitetsbegrænsning og angiver en tidshorisont for planen:

- **Kapacitetsbegrænsning:** *Ja*
- **Tidshorisont for kapacitetsbegrænsning:** *2*

Indstillingen **Kapacitetsbegrænsning** er også angivet til *Ja* for begge relevante ressourcer for at aktivere planlægning af kapacitetsbegrænsning for dem:

- Svejsebånd
- Monterebånd

Du tilføjer nu en ny salgsordre på *8 stk.* af *Produkt1* og kører planen. Som følge heraf indlæser systemet svejsebåndet fra *I dag + 1 kl. 12:00* til *I dag + 1 kl. 16:00*. Når operationerne på svejsebåndet er fuldført, indlæses monterebåndet fra *I dag +2 kl. 8:00* til *I dag + 2 kl. 10:00*. Systemet tager kun højde for kapacitetsbegrænsning i to dage.

I følgende illustration vises det Gantt-diagram, der er resultatet (vælg det for at få større visning).

[![Gantt-diagram, der viser planlægning af kapacitetsbegrænsning med en tidshorisont på to dage.](media/finite-examples-example3-small.png "Gantt-diagram, der viser planlægning af kapacitetsbegrænsning med en tidshorisont på to dage")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Du skal altid angive tidshorisonten for kapacitetsbegrænsning efter behov, så den passer til din virksomhed. De eksempler, der vises i denne artikel, illustrerer kun funktionaliteten. I praksis er en enkelt dags tidshorisont sandsynligvis for kort til de fleste producenter, der bruger planlægning af kapacitetsbegrænsning.
