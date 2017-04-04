---
title: Cost management Power BI indhold
description: "Dette emne beskriver, hvad der skal medtages i omkostningsstyring strøm BI-indhold. Det forklares, hvordan du få adgang til strøm BI-rapporter og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Cost management Power BI indhold

Dette emne beskriver, hvad der skal medtages i omkostningsstyring strøm BI-indhold. Det forklares, hvordan du få adgang til strøm BI-rapporter og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indholdet.

# <a name="overview"></a>Overblik

Den **Cost management** Microsoft Power BI-indhold er beregnet til lageret revisorer eller personer i organisationen, der er ansvarlig for lageret. Den **Cost management** Power BI indhold giver ledelsesmæssig indsigt i lager og igangværende arbejde igangværende (arbejder IGVA) lager og hvordan kostprisen flyder gennem dem efter kategori over tid. Oplysningerne kan også bruges som et yderligere supplement til regnskabet.

## <a name="key-measures"></a>Vigtigste foranstaltninger

+ Startsaldo
+ Slutsaldo
+ Netto ændring
+ Bevægelse i %
+ Aldersfordeling

## <a name="key-performance-indicators"></a>Nøgletal
+ Lageromsætning
+ Lagernøjagtighed

Den primære datakilde for CostAggregatedCostStatementEntryEntity er CostStatementCache tabellen. Denne tabel administreres af datasæt cache-framework. Tabellen opdateres hver 24 timer som standard, men du kan aktivere manuelle opdateringer i data-cache-konfigurationen. Du kan derefter foretage en manuel opdatering i den **Cost management** eller **omkostninger analyse** arbejdsområde. Når du har kørt opdateringen af CostStatementCache, skal du opdatere OData-forbindelse på Power BI.com til at få vist opdaterede data på webstedet. Afvigelse (indkøb, produktion) foranstaltningerne i denne strøm BI indhold gælder kun for varer, der er vurderet ved lager standardkostpris. Produktion-afvigelsen beregnes som forskellen mellem aktive omkostninger og realiserede omkostninger. Produktion-afvigelsen beregnes, når produktionsordren har status som **afsluttet**. Finde flere oplysninger om typer af afvigelse i produktion, og hvordan hver type beregnes [om analyse af afvigelser for en afsluttet produktionsordre](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Adgang til strøm BI-indhold
Den **Cost management** Power BI indhold er tilgængeligt fra PowerBI.com. Finde flere oplysninger om, hvordan du opretter forbindelse og indlæse din Microsoft Dynamics-365 for operationer data [Access strøm BI indhold fra PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål, som er inkluderet i indholdet strøm BI
Indholdet omfatter et sæt rapportsider. Hver side består af en række mål, som er visualized som diagrammer, fliser og tabeller. Følgende tabel indeholder en oversigt over de visuelle effekter i den **Cost management** Power BI-indhold.

| Rapportside | Diagrammer | Titler |
|---|---|---|
|Samlet lager (standard af den aktuelle periode) |Nøjagtighed |Lageret foranstaltninger:<br>Lager, slutsaldo<br>Bevægelsen i lageret<br>Lagerbeholdning bevægelsen %<br>|
| |Lageromsætning | |
| |Lageret slutsaldoen ved ressourcegruppe | |
| |Lagerbeholdning bevægelsen af kategori navn niveau 1- og kategori navn niveau 2| |
| |Købsafvigelser pr. ressourcegruppe og kategori navn niveau 3 | |
|Lager pr. websted (standard af den aktuelle periode) |Lageret slutsaldoen ved navn på websted og ressourcegruppe | |
| |Slå lager ved navn på websted og ressourcegruppe | |
| |Lageret slutsaldo af group by- og ressource | |
|Lager pr. ressourcegruppe (standard af den aktuelle periode) |Lageret foranstaltninger | |
| |Lageret nøjagtigheden af mængden af ressourcegruppe | |
| |Slå lager af mængden af ressourcegruppe | |
|Lager YOY (standard indeværende år i forhold til tidligere år) |Lageret foranstaltninger | |
| |Lager-KPI'er:<br>Lageromsætning<br>Lagernøjagtighed | |
| |Lageret slutsaldo efter år og ressource | |
| |Købsafvigelser pr. år og kategori navn niveau 3 | |
|Lager, aldersfordelt (standard i indeværende år) |Lager aldersfordelt efter kvartal og ressource | |
| |Lager aldersfordelt efter kvartal og websted navn | |
|Samlet IGVA (standard af den aktuelle periode) |Ændre via net af kategori navn niveau 1- og kategori navn niveau 2 |Igangværende arbejde via foranstaltninger:<br>Slutsaldoen for igangværende arbejde<br>VIA bevægelse<br>VIA bevægelse %<br> |
| |Produktionsafvigelser pr. ressourcegruppe og kategori navn niveau 3 | |
| |VIA bevægelse af ressourcegruppe | |
|VIA webstedet (standard af den aktuelle periode) |Igangværende arbejde via foranstaltninger | |
| |Ændre via net af webstedets navn og kategori navn niveau 2 | |
| |Afvigelser i produktion af webstedets navn og kategori navn niveau 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde siderne af rapporten i den **Cost management** Power BI-indhold. Disse data er repræsenteret som samlede målinger, der er nødvendige i butikken enhed, som er en Microsoft SQL-database, der er optimeret til analytics. Yderligere oplysninger finder du [oversigt over strøm BI integration med store enhed](power-bi-integration-entity-store.md). Følgende nøgle samlede målinger bruges som grundlag for indholdet.

| Enhed            | Samlede Kontrolmålepunkt | Datakilden til Dynamics 365 til operationer | Felt             | Betegnelse                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Sætningen poster | Netto ændring                | CostAggregatedCostStatementEntryEntity      | SUM (\[beløb\])   | Beløbet i regnskabsvalutaen |
| Sætningen poster | Antallet af bevægelse       | CostAggregatedCostStatementEntryEntity      | SUM (\[antal\]) |                                   |

Følgende tabel viser, hvor vigtige målinger af samlede bruges til at oprette flere beregnede målpunkter i det indhold dataset.

| Målepunkt                                 | Beregning af foranstaltningen                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Startsaldo                       | \[Slutsaldo\]-\[bevægelse\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Startantal balance              | \[Resterende antal balance\]-\[bevægelse, antal\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Slutsaldo                          | BEREGN (SUM (\[beløb\]), FILTER (ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navn\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskabskalendere'\[dato\]&lt;= MAX ('Regnskabskalendere'\[dato\])))                                                                                                                                                                                           |
| Afslutning saldo antal                 | BEREGN (SUM (\[antal\]), FILTER (ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navn\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskabskalendere'\[dato\]&lt;= MAX ('Regnskabskalendere'\[dato\])))                                                                                                                                                                                         |
| Lager, startsaldo             | BEREGN (\[startsaldo\], 'Sætning poster'\[sætningstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                      |
| Lager, slutsaldo                | BEREGN (\[slutsaldo\], 'Sætning poster'\[sætningstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                         |
| Bevægelsen i lageret                    | BEREGN (\[bevægelse\], 'Sætning poster'\[sætningstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                             |
| Lagerantal bevægelse           | BEREGN (\[bevægelse, antal\], 'Sætning poster'\[sætningstype\] = "Lager")                                                                                                                                                                                                                                                                                                                                                                                    |
| Lagerbeholdning bevægelsen %                  | IF (\[oversigt slutsaldoen\] = 0, 0, \[lager, bevægelse\] / \[lager slutsaldoen\])                                                                                                                                                                                                                                                                                                                                                                           |
| Slå lager efter beløb                | Hvis (OR (\[lager gennemsnitlig saldo\]&lt;= 0, \[lager solgt eller forbrugt problemer\]&gt;= 0), 0 ABS (\[lager solgt eller forbrugt problemer\]) /\[lager gennemsnitlig saldo\])                                                                                                                                                                                                                                                                                                  |
| Gennemsnitlig lageropgørelsen               | (\[Oversigt slutsaldoen\] + \[lager startsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lager, der er solgt eller forbrugt problemer       | \[Solgt lager\] + \[lager forbrugt materialeomkostninger\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Lageret forbrugt materialeomkostninger        | BEREGN (\[lager, bevægelse\], 'Sætning poster'\[kategorinavn - niveau 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Solgt lager                          | BEREGN (\[lager, bevægelse\], 'Sætning poster'\[kategorinavn - niveau 2\_\] = "Solgt")                                                                                                                                                                                                                                                                                                                                                                             |
| Nøjagtigheden af lageret med beløb            | IF (\[lager slutsaldoen\]&lt;= 0, hvis (eller (\[lager optalt beløb\]&lt;&gt; 0, \[lager slutsaldoen\]&lt; 0), 0, 1), MAX (0, (\[lager slutsaldoen\] -ABS (\[lager optalt beløb\])) /\[lager slutsaldoen\]))                                                                                                                                                                                                                              |
| Optalt beløb lager                | BEREGN (\[lager, bevægelse\], 'Sætning poster'\[kategorinavn - niveau 3\_\] = "Optælling")                                                                                                                                                                                                                                                                                                                                                                         |
| Aldersfordelt lager                         | Hvis (ISBLANK (max ('Regnskabskalendere'\[dato\])), blank(), MAX (0, MIN (\[lager, aldersfordelt tilgange antal\], \[lager, aldersfordelt saldo slutantallet\] - \[lager aldersfordelt tilgange antal fremover\]))) \*\[lager gennemsnitlige enhedsomkostning\]                                                                                                                                                                                                                                |
| Lager, aldersfordelt tilgange antal       | Hvis (\[minDate\] = \[minDateAllSelected\], BEREGN (\[lagerbeholdning bevægelsen antal\], 'Sætning poster'\[antal\]&gt; 0, FILTER (ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navn\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskabskalendere'\[dato\]&lt;= MAX ('Regnskabskalendere'\[dato\]))), BEREGN (\[lagerbeholdning bevægelsen antal\], 'Sætning poster'\[antal\]&gt; 0)) |
| Lager aldersfordelt resterende saldo antal | \[Resterende saldo antal lager\] + BEREGN (\[lagerbeholdning bevægelsen antal\], FILTER (ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navn\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskabskalendere'\[dato\]&gt; max ('Regnskabskalendere'\[dato\])))                                                                                                                                 |
| Aldersfordelt lagertilgange i fremtiden  | BEREGN (\[lager, bevægelse\], 'Sætning poster'\[beløb\]&gt; 0, FILTER (ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]), 'Regnskabskalendere'\[dato\]&gt; MAX ('Regnskabskalendere'\[dato\])))                                                                                                                                             |
| Avg lagerkostprisen                 | BEREGN (\[lager slutsaldoen\] / \[lager slutantallet balance\], ALLEXCEPT ('Regnskabskalendere', 'Regnskabskalendere'\[LedgerRecId\], 'objekter'\[ID\], 'objekter'\[navnet\], 'Finans'\[valuta\], 'Finans'\[beskrivelse\], 'Finans'\[navn\]))                                                                                                                                                                                                                 |
| Produktionsafvigelser                      | BEREGN (SUM (\[beløb\]), 'Sætning poster'\[kategorinavn - niveau 2\_\] = "Procured", 'Sætning poster'\[opgørelsestypen\] = "Afvigelse")                                                                                                                                                                                                                                                                                                                              |
| VIA startsaldo                   | BEREGN (\[startsaldo\], 'Sætning poster'\[sætningstype\] = "Igangværende arbejde")                                                                                                                                                                                                                                                                                                                                                                                            |
| Slutsaldoen for igangværende arbejde                      | BEREGN (\[slutsaldo\], 'Sætning poster'\[sætningstype\] = "Igangværende arbejde")                                                                                                                                                                                                                                                                                                                                                                                               |
| VIA bevægelse                          | BEREGN (\[bevægelse\], 'Sætning poster'\[sætningstype\] = "Igangværende arbejde")                                                                                                                                                                                                                                                                                                                                                                                                   |
| VIA bevægelse %                        | IF (\[via slutsaldo\] = 0, 0, \[via bevægelse\] / \[via slutsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Afvigelser i produktion                    | BEREGN (SUM (\[beløb\]), 'Sætning poster'\[kategorinavn - niveau 2\_\] = "ManufacturedCost", 'Sætning poster'\[opgørelsestypen\] = "Afvigelse")                                                                                                                                                                                                                                                                                                                      |
| Kategorinavnet - niveau 1                 | Skifte (\[kategorinavn - niveau 1\_\], "Ingen", "Ingen", "NetSourcing", "Net forsyning", "NetUsage", "Net forbrug", "NetConversionCost", "Net konvertering omkostninger", "NetCostOfGoodsManufactured", "Net fremstillede varer", "BeginningBalance", "Startsaldo")                                                                                                                                                                                                         |
| Kategorinavnet - niveau 2                 | Skifte (\[kategorinavn - niveau 2\_\], "Ingen", "Ingen", "Procured", "Procured", "Disposed", "Disposed", "Overført", "Overført", "Solgt", "Solgt", "ConsumedMaterialsCost", "Forbrugt materialeomkostninger", "ConsumedManufacturingCost", "Forbrugt på enkeltniveau", "ConsumedOutsourcingCost", "Forbrugt outsourcing omkostninger", "ConsumedIndirectCost", "Forbrugt indirekte omkostninger", "ManufacturedCost", "Produceret omkostninger", "Afvigelser", "Afvigelser")                            |
| Kategorinavnet - niveau 3                 | Skifte (\[kategorinavn - niveau 3\_\], "Ingen", "Ingen", "Optælling", "Ingen", "ProductionPriceVariance", "Produktion pris", "QuantityVariance", "Antal", "SubstitutionVariance", "Erstatning", "ScrapVariance", "Spild", "LotSizeVariance", "lotstørrelse", "RevaluationVariance", "Værdiregulering", "PurchasePriceVariance", "Indkøbspris", "CostChangeVariance", "Kostprisen", "RoundingVariance", "Afvigelse i afrunding")                                                   |

Følgende vigtige dimensioner bruges som filtre i udsnit af de samlede mål for at opnå større granularitet og giver større analytiske indsigt.

| Enhed           | Eksempler på attributter                       |
|------------------|----------------------------------------------|
| Enheder         | ID, navn                                     |
| Regnskabskalendere | Kalender, måned, periode, kvartal, år       |
| KPI-mål        | Lageret nøjagtighed mål lager slå mål |
| Finans          | Valuta, navn, beskrivelse                  |
| Steder            | ID, navn, land, by                      |

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



