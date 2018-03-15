---
title: Power BI-indhold til omkostningsstyring
description: I dette emne beskrives, hvad der skal medtages i Power BI-indhold til omkostningsstyring.
author: YuyuScheller
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7b5c4428c8610a7b2d4cf1a28287ba2bb1f9c2ea
ms.openlocfilehash: 6739d769c3f7876f67d80554743458b0abd5aae5
ms.contentlocale: da-dk
ms.lasthandoff: 02/06/2018

---

# <a name="cost-management-power-bi-content"></a>Power BI-indhold til omkostningsstyring

[!include[banner](../includes/banner.md)]

> [!Note]
> Denne indholdspakke er blevet udfaset, som beskrevet i [Power BI-indholdspakker, der er publiceret på PowerBI.com](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom).


I dette emne beskrives, hvad der skal medtages i Power BI-indhold til omkostningsstyring. 

Microsoft Power BI-indhold til **Omkostningsstyring** er beregnet til lagerregnskabsmedarbejdere eller personer i organisationen, der er ansvarlige for lageret. Power BI-indholdet til **Omkostningsstyring** giver ledelsesmæssig indsigt i lager og lager for igangværende forarbejdning (IGVF), og hvordan kostprisen flyder gennem dem efter kategori over tid. Oplysningerne kan også bruges som et detaljeret supplement til regnskabet.

## <a name="key-measures"></a>Nøgletal

+ Startsaldo
+ Slutsaldo
+ Netto ændring
+ Netto ændring i %
+ Aldersfordeling

## <a name="key-performance-indicators"></a>Nøgletal
+ Lageromsætning
+ Lagernøjagtighed

Den primære datakilde for CostAggregatedCostStatementEntryEntity er CostStatementCache-tabellen. Denne tabel administreres af datasættes cachestruktur. Tabellen opdateres med 24 timers mellemrum som standard, men du kan aktivere manuelle opdateringer i datacachekonfigurationen. Du kan derefter foretage en manuel opdatering i **Omkostningsstyring** eller **Omkostningsanalyse** arbejdsområdet. Efter kørslen af opdateringen af CostStatementCache skal du opdatere OData-forbindelsen på Power BI.com for at få vist opdaterede data på webstedet. Afvigelsesmålingerne (indkøb, produktion) i dette Power BI-indhold gælder kun for varer, der er vurderet med lagermetoden for standardomkostninger. Produktionsafvigelsen beregnes som forskellen mellem aktive omkostninger og realiserede omkostninger. Produktionsafvigelsen beregnes, når produktionsordren har status **Afsluttet**. Du kan finde flere oplysninger om typer af produktionsafvigelse, og hvordan hver type beregnes, under [Om analyse af afvigelser for en afsluttet produktionsordre](https://technet.microsoft.com/en-us/library/gg242850.aspx).


## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indhold
Indholdet omfatter et sæt rapportsider. Hver side består af en række mål, som er visualiseret som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i Power BI-indholdet til **Omkostningsstyring**.

| Rapportside | Diagrammer | Titler |
|---|---|---|
|Samlet lager (standard efter aktuel periode) |Nøjagtighed |Lagermålinger:<br>Lagerslutsaldo<br>Lagernettoændring<br>Lagernettoændring i %<br>|
| |Lageromsætning | |
| |Lagerslutsaldo efter ressourcegruppe | |
| |Lagernettoændring efter kategorinavn på niveau 1 og kategorinavn på niveau 2| |
| |Købsafvigelser pr. ressourcegruppe og kategorinavn på niveau 3 | |
|Lager efter sted (standard efter aktuel periode) |Lagerslutsaldo efter navn på sted og ressourcegruppe | |
| |Lageromsætning efter navn på sted og ressourcegruppe | |
| |Lagerslutsaldo efter by og ressourcegruppe | |
|Lager efter ressourcegruppe (standard efter aktuel periode) |Lagermålinger | |
| |Lagernøjagtighed efter mængde efter ressourcegruppe | |
| |Lageromsætning efter mængde efter ressourcegruppe | |
|Lager år for år (standard indeværende år i forhold til tidligere år) |Lagermålinger | |
| |Lager-KPI'er:<br>Lageromsætning<br>Lagernøjagtighed | |
| |Lagerslutsaldo efter år og ressourcegruppe | |
| |Købsafvigelser pr. år og kategorinavn på niveau 3 | |
|Aldersfordelt lager (standard efter indeværende år) |Aldersfordelt lager efter kvartal og ressourcegruppe | |
| |Aldersfordelt lager efter kvartal og navn på sted | |
|Samlet IGVF (standard efter aktuel periode) |IGVF-nettoændring efter kategorinavn på niveau 1 og kategorinavn på niveau 2 |IGVF-målinger for igangværende forarbejdning:<br>IGVF-slutsaldo<br>IGVF-nettoændring<br>IGVF-nettoændring i %<br> |
| |Produktionsafvigelser pr. ressourcegruppe og kategorinavn på niveau 3 | |
| |IGVF-nettoændring efter ressourcegruppe | |
|IGVF efter sted (standard efter aktuel periode) |IGVF-målinger for igangværende forarbejdning | |
| |IGVF-nettoændring efter navn sted og kategorinavn på niveau 2 | |
| |Produktionsafvigelser pr. navn på sted og kategorinavn på niveau 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Finance and Operations-data bruges til at udfylde rapportsiderne i Power BI-indhold til **Omkostningsstyring**. Disse data repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL-database, der er optimeret til analyse. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md). Følgende samlede nøglemålinger bruges som grundlag for indholdet.

| Enhed            | Samlede nøglemålinger | Datakilde til Finance and Operations | Felt             | Betegnelse                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Fordelingsposter | Netto ændring                | CostAggregatedCostStatementEntryEntity      | sum (\[Beløb\])   | Beløb i regnskabsvalutaen |
| Fordelingsposter | Nettoændring, antal       | CostAggregatedCostStatementEntryEntity      | sum(\[Antal\]) |                                   |

Følgende tabel viser, hvor de samlede nøglemålinger bruges til at oprette flere beregnede målepunkter i indholdets datasæt.

| Målepunkt                                 | Sådan beregnes målepunktet                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Startsaldo                       | \[Slutsaldo\]-\[Nettoændring\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Startsaldoantal              | \[Slutsaldoantal\]-\[Nettoændring, antal\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Slutsaldo                          | CALCULATE(SUM(\[Beløb\]), FILTER(ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]), 'Regnskabskalendere'\[Dato\] &lt;= MAX('Regnskabskalendere'\[Dato\])))                                                                                                                                                                                           |
| Slutsaldoantal                 | CALCULATE(SUM(\[Antal\]), FILTER(ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]), 'Regnskabskalendere'\[Dato\] &lt;= MAX('Regnskabskalendere'\[Dato\])))                                                                                                                                                                                         |
| Lagerstartsaldo             | CALCULATE(\[Startsaldo\], 'Fordelingsposter'\[Fordelingstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                      |
| Lagerslutsaldo                | CALCULATE(\[Slutsaldo\], 'Fordelingsposter'\[Fordelingstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                         |
| Lagernettoændring                    | CALCULATE(\[Nettoændring\], 'Fordelingsposter'\[Fordelingstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                             |
| Lagernettoændring i antal           | CALCULATE(\[Nettoændring, antal\], 'Fordelingsposter'\[Fordelingstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                    |
| Lagernettoændring i %                  | IF(\[Lagerslutsaldo\] = 0, 0, \[Lagernettoændring\] / \[Lagerslutsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Lageromsætning efter beløb                | if(OR (\[Gennemsnitlig saldo for lager\] &lt;= 0, \[Lagerafgange, salg eller forbrug\] &gt;= 0), 0 ABS (\[Lagerafgange, salg eller forbrug\]) /\[Gennemsnitlig saldo for lager\])                                                                                                                                                                                                                                                                                                  |
| Gennemsnitlig saldo for lager               | (\[Lagerslutsaldo\] + \[Lagerstartsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lagerafgange, salg eller forbrug       | \[Lagersalg\] + \[Forbrugt materialeomkostning for lager\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Forbrugt materialeomkostning for lager        | CALCULATE(\[Lagernettoændring\], 'Fordelingsposter'\[Kategorinavn - niveau 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Lagersalg                          | CALCULATE(\[Lagernettoændring\], 'Fordelingsposter'\[Kategorinavn - niveau 2\_\] = "Solgt")                                                                                                                                                                                                                                                                                                                                                                             |
| Lagernøjagtighed efter beløb            | IF(\[Lagerslutsaldo\] &lt;= 0, IF(OR(\[Lager, optalt beløb\] &lt;&gt; 0, \[Lagerslutsaldo\] &lt; 0), 0, 1), MAX(0, (\[Lagerslutsaldo\] - ABS(\[Lager, optalt beløb\]))/\[Lagerslutsaldo\]))                                                                                                                                                                                                                              |
| Lager, optalt beløb                | CALCULATE(\[Lagernettoændring\], 'Fordelingsposter'\[Kategorinavn - niveau 3\_\] = "Optælling")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldersfordelt lager                         | if(ISBLANK(max('Regnskabskalendere'\[Date\])), blank(), MAX(0, MIN(\[Aldersfordelt lager, antal tilgange\], \[Aldersfordelt lager, slutsaldoantal\] - \[Aldersfordelt lager, tilgange i fremtiden\]))) \* \[Lager, gennemsnitlig enhedskostpris\]                                                                                                                                                                                                                                |
| Aldersfordelt lager, antal tilgange       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Lagernettoændring i antal\], 'Fordelingsposter'\[Antal\] &gt; 0, FILTER(ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]), 'Regnskabskalendere'\[Dato\] &lt;= MAX('Regnskabskalendere'\[Dato\]))), CALCULATE(\[Lagernettoændring i antal\], 'Fordelingsposter'\[Antal\] &gt; 0)) |
| Aldersfordelt lager, slutsaldoantal | \[Aldersfordelt lager, slutsaldoantal\] + CALCULATE(\[Lagernettoændring i antal\], FILTER(ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]), 'Regnskabskalendere'\[Dato\] &gt; max('Regnskabskalendere'\[Dato\]) ))                                                                                                                                 |
| Aldersfordelt lager, tilgange i fremtiden  | CALCULATE(\[Lagernettoændring\], 'Fordelingsposter'\[Beløb\] &gt; 0, FILTER(ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]), 'Regnskabskalendere'\[Dato\] &gt; MAX('Regnskabskalendere'\[Dato\])))                                                                                                                                             |
| Lager, gennemsnitlig enhedskostpris                 | CALCULATE(\[Lagerslutsaldo\] / \[Aldersfordelt lager, slutsaldoantal\],ALLEXCEPT('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'enheder'\[ID\], 'enheder'\[Navn\], 'Finans'\[Valuta\], 'Finans'\[Beskrivelse\], 'Finans'\[Navn\]))                                                                                                                                                                                                                 |
| Købsafvigelser                      | CALCULATE(SUM(\[Beløb\]), 'Fordelingsposter'\[Kategorinavn - niveau 2\_\] = "Indkøbt", 'Fordelingsposter'\[Fordelingstype\] = "Afvigelse")                                                                                                                                                                                                                                                                                                                              |
| IGVF-startsaldo                   | CALCULATE(\[Startsaldo\], 'Fordelingsposter'\[Fordelingstype\] = "IGVF")                                                                                                                                                                                                                                                                                                                                                                                            |
| IGVF-slutsaldo                      | CALCULATE(\[Slutsaldo\], 'Fordelingsposter'\[Fordelingstype\] = "IGVF")                                                                                                                                                                                                                                                                                                                                                                                               |
| IGVF-nettoændring                          | CALCULATE(\[Nettoændring\], 'Fordelingsposter'\[Fordelingstype\] = "IGVF")                                                                                                                                                                                                                                                                                                                                                                                                   |
| IGVF-nettoændring i %                        | IF(\[IGVF-slutsaldo\] = 0, 0, \[IGVF-nettoændring\] / \[IGVF-slutsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Afvigelser i produktion                    | CALCULATE(SUM(\[Beløb\]), 'Fordelingsposter'\[Kategorinavn - niveau 2\_\] = "ManufacturedCost", 'Fordelingsposter'\[Fordelingstype\] = "Afvigelse")                                                                                                                                                                                                                                                                                                                      |
| Kategorinavn - niveau 1                 | switch(\[Kategorinavn - niveau 1\_\], "None", "Ingen", "NetSourcing", "Nettoforsyning", "NetUsage", "Nettoanvendelse", "NetConversionCost", "Nettokonverteringsomkostning", "NetCostOfGoodsManufactured", "Nettoomkostning for fremstillede varer", "BeginningBalance", "Startsaldo")                                                                                                                                                                                                         |
| Kategorinavn - niveau 2                 | switch(\[Kategorinavn - niveau 2\_\], "None", "Ingen", "Procured", "Indkøbt", "Disposed", "Kasseret", "Transferred", "Overført", "Sold", "Solgt", "ConsumedMaterialsCost", "Forbrugt materialeomkostning", "ConsumedManufacturingCost", "Forbrugt produktionsomkostning", "ConsumedOutsourcingCost", "Forbrugt outsourcingomkostning", "ConsumedIndirectCost", "Forbrugt indirekte omkostning", "ManufacturedCost", "Produktionsomkostning", "Variances", "Afvigelser")                            |
| Kategorinavn - niveau 3                 | switch(\[Kategorinavn - niveau 3\_\], "None", "Ingen", "Optælling", "Ingen", "ProductionPriceVariance", "Produktionspris", "QuantityVariance", "Antal", "SubstitutionVariance", "Erstatning", "ScrapVariance", "Spild", "LotSizeVariance", "Lotstørrelse", "RevaluationVariance", "Værdiregulering", "PurchasePriceVariance", "Købspris", "CostChangeVariance", "Ændring i kostpris", "RoundingVariance", "Afvigelse i afrunding")                                                   |

Følgende nøgledimensioner bruges som filtre til at skabe udsnit af de samlede målinger for at opnå større granularitet og give dybere analytisk indsigt.

| Enhed           | Eksempler på attributter                       |
|------------------|----------------------------------------------|
| Enheder         | Id, navn                                     |
| Regnskabskalendere | Kalender, måned, periode, kvartal, år       |
| KPI-mål        | Mål for lagernøjagtighed, mål for lageromsætning |
| Finans          | Valuta, navn, beskrivelse                  |
| Lokationer            | Id, navn, land, by                      |






