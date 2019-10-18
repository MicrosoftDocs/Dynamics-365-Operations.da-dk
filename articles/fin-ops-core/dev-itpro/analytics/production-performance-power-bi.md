---
title: Power BI-indhold til produktionsperformance
description: I dette emne beskrives, hvad der er omfattet af Power BI-indhold til produktionsperformance. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.
author: AndersGirke
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ProductionPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9e2613a9adf60699a1c20b780e1acf2afb99d37d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182870"
---
# <a name="production-performance-power-bi-content"></a>Power BI-indhold til produktionsperformance

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvad der er omfattet af Microsoft Power BI-indhold til **Produktionsperformance**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Produktionsperformance** gælder for produktionschefer eller personer i organisationen, der er ansvarlige for produktionsstyring.

Med de rapporter, der indgår, kan du bruge Power BI til at overvåge performance for fremstillingsprocesser med hensyn til rettidig udførelse, kvalitet og omkostninger. Rapporterne bruger transaktionsdata fra produktionsordrer og batchordrer og giver både en samlet oversigt over produktionstal for hele firmaet og en opdeling af performanceværdier pr. produkt og ressource.

Power BI-indholdet fremhæver organisationens evne til at fuldføre produktionen til tiden og i sin helhed. Den fremtidige performance planlægges ud fra produktionsplaner. Omfattende rapporter indeholder detaljeret indsigt i produktfejl, der er forårsaget af produktionen, og også fejlrater for ressourcer og operationer.

Med dette Power BI-indhold kan du også analysere afvigelser i produktionen. Produktionsafvigelser beregnes som forskellen mellem forkalkulerede omkostninger og realiserede omkostninger. Produktionsafvigelser beregnes, når produktionsordrer eller batchordrer når status **Afsluttet**.

Power BI-indholdet til **Produktionsperformance** omfatter data, der stammer fra produktionsordrer og batchordrer. Rapporterne omfatter ikke data, der er relateret til kanban-produktioner.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Power BI-indholdet **Produktionsperformance** vises på siden **Produktionsperformance** (**Produktionsstyring** \> **Forespørgsler og rapporter** \> **Performanceanalyse for produktion** \> **Produktionsperformance**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet

Power BI-indholdet til **Produktionsperformance** omfatter et sæt rapportsider. Hver side består af en række mål, som er visualiseret som diagrammer, felter og tabeller.

I nedenstående tabel vises en oversigt over de visualiseringer, der indgår.

| Rapportside                                | Diagrammer | Felter |
|--------------------------------------------|--------|-------|
| Produktionsperformance                     | <ul><li>Antal produktionslinjer efter dato</li><li>Antal produktioner pr. produkt og varegruppe</li><li>Antal planlagte produktioner efter dato</li><li>Nederste 10 produkter efter til tiden og i sin helhed</li></ul> | <ul><li>Samlede ordrer</li><li>Til tiden og i sin helhed i %</li><li>Ufuldstændig i %</li><li>For tidlig i %</li><li>For sent i %</li></ul> |
| Fejl efter produkt                         | <ul><li>Fejlrate (ppm) efter dato</li><li>Fejlrate (ppm) efter produkt og varegruppe</li><li>Antal produceret pr. dato</li><li>Produkter i top 10 efter effektivitetsrate</li></ul> | <ul><li>Fejlrate (ppm)</li><li>Fejlbehæftet mængde</li><li>Samlet antal</li></ul> |
| Fejltendenser efter produkt                   | Fejlrate (ppm) efter produceret antal | Fejlrate (ppm) |
| Fejl pr. ressource                        | <ul><li>Fejlrate (ppm) pr. dato</li><li>Fejlrate (ppm) efter ressource og sted</li><li>Fejlrate (ppm) pr. operation</li><li>Ressourcer i top 10 efter fejlrate</li></ul> | Fejlbehæftet mængde |
| Fejltendenser efter ressource                  | Fejlrate (ppm) efter behandlet antal | |
| Produktionsafvigelser for efterkalkulering af jobordre | <ul><li>Produktionsafvigelse efter dato og omkostningsgruppetype</li><li>Produktionsafvigelse efter sted og omkostningsgruppetype</li><li>Varer i top 10 med negativ produktionsafvigelse</li><li>Top 10 over negativ produktionsafvigelse efter ressource</li></ul> | <ul><li>Realiseret omkostning</li><li>Produktionsomkostningsafvigelse</li><li>Produktionsomkostningsafvigelse i %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende data bruges til rapportsiderne i Power BI-indholdet til **Produktionsperformance**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger om enhedslageret under [Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

Følgende tabel viser de samlede nøglemålinger, der bruges som grundlag af Power BI-indholdet.

| Enhed                   | Samlede nøglemålinger  | Datakilde til Finance and Operations-apps | Felt              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Følgende tabel viser, hvor de samlede nøglemålinger bruges til at oprette flere beregnede målepunkter i indholdets datasæt.

| Målepunkt                  | Sådan beregnes målepunktet |
|--------------------------|-------------------------------|
| Produktionsomkostningsafvigelse i %   | SUM('Produktionsomkostningsafvigelse'\[[produktionsomkostningsafvigelse\]]) / SUM('Produktionsomkostningsafvigelse'\[forkalkuleret omkostning\]) |
| Alle ordreforslag       | COUNTROWS('Produktionsordreforslag') |
| For tidlig                    | COUNTROWS(FILTER('Produktionsordreforslag', 'Produktionsordreforslag'\[Planlagt slutdato\] \< 'Produktionsordreforslag'\[Behovsdato\])) |
| Forsinket                     | COUNTROWS(FILTER('Produktionsordreforslag', 'Produktionsordreforslag'\[Planlagt slutdato\] \> 'Produktionsordreforslag'\[Behovsdato\])) |
| Til tiden                  | COUNTROWS(FILTER('Produktionsordreforslag', 'Produktionsordreforslag'\[Planlagt slutdato\] = 'Produktionsordreforslag'\[Behovsdato\])) |
| Til tiden i %                | IF ('Produktionsordreforslag'\[Til tiden\] \<\> 0, 'Produktionsordreforslag'\[Til tiden\], IF ('Produktionsordreforslag'\[Alle ordreforslag\] \<\> 0, 0, BLANK()) ) / 'Produktionsordreforslag'\[Alle ordreforslag\] |
| Afsluttede                | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er færdigmeldt\] = TRUE)) |
| Fejlrate (ppm)     | IF('Produktionsordre'\[Samlet antal\] = 0, BLANK(), (SUM('Produktionsordre'\[Fejlbehæftet mængde\]) / 'Produktionsordre'\[Samlet antal\]) \* 1000000) |
| Forsinket produktionsgrad  | 'Produktionsordre'\[For sent \#\] / 'Produktionsordre'\[Fuldført\] |
| For tidlig og i sin helhed          | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er i sin helhed\] = TRUE && 'Produktionsordre'\[Er for tidlig\] = TRUE)) |
| For tidlig \#                 | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er for tidlig\] = TRUE)) |
| For tidlig i %                  | IFERROR( IF('Produktionsordre'\[For tidlig \#\] \<\> 0, 'Produktionsordre'\[For tidlig \#\], IF('Produktionsordre'\[Samlede ordrer\] = 0, BLANK(), 0)) / 'Produktionsordre'\[Samlede ordrer\], BLANK()) |
| Ikke fuldført               | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er i sin helhed\] = FALSE && 'Produktionsordre'\[Er færdigmeldt\] = TRUE)) |
| Ufuldstændig i %             | IFERROR( IF('Produktionsordre'\[Ufuldstændig\] \<\> 0, 'Produktionsordre'\[Ufuldstændig\], IF('Produktionsordre'\[Samlede ordrer\] = 0, BLANK(), 0)) / 'Produktionsordre'\[Samlede ordrer\], BLANK()) |
| Er forsinket               | 'Produktionsordre'\[Er færdigmeldt\] = TRUE && 'Produktionsordre'\[Værdi for Forsinket\] = 1 |
| Er for tidlig                 | 'Produktionsordre'\[Er færdigmeldt\] = TRUE && 'Produktionsordre'\[Dages forsinkelse\] \< 0 |
| Er i sin helhed               | 'Produktionsordre'\[Antal gode\] \>= 'Produktionsordre'\[Planlagt antal\] |
| Er færdigmeldt                | 'Produktionsordre'\[produktionsstatusværdi\] = 5 \|\| 'Produktionsordre'\[produktionsstatusværdi\] = 7 |
| For sent og i sin helhed           | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er i sin helhed\] = TRUE && 'Produktionsordre'\[Er forsinket\] = TRUE)) |
| For sent \#                  | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er forsinket\] = TRUE)) |
| For sent i %                   | IFERROR( IF('Produktionsordre'\[For sent \#\] \<\> 0, 'Produktionsordre'\[For sent \#\], IF('Produktionsordre'\[Samlede ordrer\] = 0, BLANK(), 0)) / 'Produktionsordre'\[Samlede ordrer\], BLANK()) |
| Til tiden og i sin helhed        | COUNTROWS(FILTER('Produktionsordre', 'Produktionsordre'\[Er i sin helhed\] = TRUE && 'Produktionsordre'\[Er forsinket\] = FALSE && 'Produktionsordre'\[Er for tidlig\] = FALSE)) |
| Til tiden og i sin helhed i %      | IFERROR( IF('Produktionsordre'\[Til tiden og i sin helhed\] \<\> 0, 'Produktionsordre'\[Til tiden og i sin helhed\], IF('Produktionsordre'\[Fuldført\] = 0, BLANK(), 0)) / 'Produktionsordre'\[Fuldført\], BLANK()) |
| Samlede ordrer             | COUNTROWS('Produktionsordre') |
| Samlet antal           | SUM('Produktionsordre'\[Antal gode\]) + SUM('Produktionsordre'\[Fejlbehæftet mængde\]) |
| Fejlrate (ppm)        | IF('Ruteposteringer'\[Behandlet antal\] = 0, BLANK(), (SUM('Ruteposteringer'\[Fejlbehæftet mængde\]) / 'Ruteposteringer\[Behandlet antal\]) \* 1000000) |
| Fejlgrad blandet (ppm) | IF('Ruteposteringer'\[Samlet antal blandet\] = 0, BLANK(), (SUM('Ruteposteringer'\[Fejlbehæftet mængde\]) / 'Ruteposteringer\[Samlet antal blandet\]) \* 1000000) |
| Behandlet antal       | SUM('Ruteposteringer'\[Antal gode\]) + SUM('Ruteposteringer'\[Fejlbehæftet mængde\]) |
| Samlet antal blandet     | SUM('Produktionsordre'\[Antal gode\]) + SUM('Ruteposteringer'\[Fejlbehæftet mængde\]) |

Følgende tabel viser de nøgledimensioner, der bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.

| Enhed                    | Eksempler på attributter                                        |
|---------------------------|---------------------------------------------------------------|
| Færdigmeldingsdato | Forskydning af fuldførelsesdato (færdigmeldt), måned og år                 |
| Slutdato                | Forskydning af månedsafslutning og måned                                  |
| Behovsdato          | Forskydning af behovsdato for måned og behovsdato            |
| Dato for rutepostering    | Forskydning af ruteposteringsmåned og dato                       |
| Steder                     | Sted-id, navn på sted, stat og by                          |
| Enheder                  | Id og navn                                                   |
| Ressourcer                 | Ressource-id, ressourcenavn, ressourcetype og ressourcegruppe |
| Produkter                  | Produktnummer, produktnavn, vare-id og varegruppe         |
