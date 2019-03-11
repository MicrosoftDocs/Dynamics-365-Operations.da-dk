---
title: Power BI-indhold til omkostningsstyring
description: I dette emne beskrives, hvad der skal medtages i Power BI-indhold til omkostningsstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f67b1c901267bdf79c94e4f4c698c8731c515bb4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327797"
---
# <a name="cost-management-power-bi-content"></a>Power BI-indhold til omkostningsstyring

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overblik

Microsoft Power BI-indholdet til **Omkostningsstyring** er beregnet til lagerbogholdere eller enkeltpersoner i organisationen, som er ansvarlige for eller interesserede i status for lageret eller det igangværende arbejde (IGVA), eller som er ansvarlig for eller interesseret i at analysere afvigelser i standardomkostningerne.

> [!NOTE]
> Det Power BI-indhold til **Omkostningsstyring**, som beskrives i dette emne, gælder for Dynamics 365 for Finance and Operations 8.0.
> 
> Power BI-indholdspakken til **Omkostningsstyring**, som er tilgængelig på AppSource-webstedet, er blevet udfaset. Du kan finde flere oplysninger om denne udfasning i [Power BI-indholdspakkerne, der er tilgængelig på AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Dette Power BI-indhold giver et kategoriseret format, som gør det lettere at overvåge performance for lagerbeholdninger og visualisere, hvordan omkostninger "flyder" gennem dem. Du kan få ledelsesmæssig indsigt, f.eks. omsætningshastigheden, antallet af dage, hvor varen er på lager, nøjagtighed og "ABC-klassifikation" på dit foretrukne samlede niveau (firma, vare, varegruppe eller sted). De oplysninger, der er gjort tilgængelige, kan også bruges som et detaljeret supplement til regnskabet.

Power BI-indholdet er baseret på den samlede måling for **CostObjectStatementCacheMonthly**, som har tabellen **CostObjectStatementCache** som primær datakilde. Denne tabel administreres af datasættes cachestruktur. Tabellen opdateres med 24 timers mellemrum som standard, men du kan ændre opdateringshyppigheden og aktivere manuelle opdateringer i konfigurationen af datasætcachen. Manuelle opdateringer kan køres enten i arbejdsområdet **Omkostningsstyring** eller **Omkostningsanalyse**.

Efter hver opdatering af tabellen **CostObjectStatementCache**, skal den samlede måling for **CostObjectStatementCacheMonthly** opdateres, før dataene Power BI-visualiseringerne opdateres.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet

Power BI-indholdet til **Omkostningsstyring** vises i arbejdsområderne **Omkostningsstyring** og **Omkostningsanalyse**.

Arbejdsområdet **Omkostningsstyring** indeholder følgende faner:

- **Oversigt** – Denne fane viser programdata.
- **Lagerregnskabsstatus** – Denne fane viser Power BI-indhold.
- **Produktionsregnskabsstatus** – Denne fane viser Power BI-indhold.

Arbejdsområdet **Omkostningsanalyse** indeholder følgende faner:

- **Oversigt** – Denne fane viser programdata.
- **Lagerregnskabsanalyse** – Denne fane viser Power BI-indhold.
- **Produktionsregnskabsanalyse** – Denne fane viser Power BI-indhold.
- **Analyse af standardomkostningsafvigelse** – Denne fane viser Power BI-indhold.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Rapportsider, der er inkluderet i Power BI-indholdet

Power BI-indholdet til **Omkostningsstyring** omfatter en række rapportsider, der indeholder et sæt nøgletal. Disse metrikker visualiseres som diagrammer, felter og tabeller. 

I nedenstående tabeller vises en oversigt over visualiseringerne i Power BI-indholdet til **Omkostningsstyring**.

### <a name="inventory-accounting-status"></a>Lagerregnskabsstatus

| Rapportside                               | Visualisering                                   |
|-------------------------------------------|-------------------------------------------------|
| Lageroversigt                        | Startsaldo                               |
|                                           | Netto ændring                                      |
|                                           | Nettoændring i %                                    |
|                                           | Slutsaldo                                  |
|                                           | Lagernøjagtighed                              |
|                                           | Lageromsætningshastighed                        |
|                                           | Dage for disponibel beholdning                          |
|                                           | Aktivt produkt i periode                        |
|                                           | Aktive omkostningsobjekter i periode                   |
|                                           | Saldo pr. varegruppe                           |
|                                           | Saldo pr. sted                                 |
|                                           | Kontoudtog pr. kategori                           |
|                                           | Nettoændring pr. kvartal                           |
| Lageroversigt pr. sted og varegruppe | Lagernøjagtighed pr. sted                      |
|                                           | Lageromsætningshastighed pr. sted                |
|                                           | Lagerslutsaldo pr. sted                |
|                                           | Lagernøjagtighed pr. varegruppe                |
|                                           | Lageromsætningshastighed pr. varegruppe          |
|                                           | Lagerslutsaldo pr. sted og varegruppe |
| Lageropgørelse                       | Lageropgørelse                             |
| Lageropgørelse pr. sted               | Lageropgørelse pr. sted                     |
| Lageropgørelse pr. produkthierarki  | Lageropgørelse                             |
| Lageropgørelse pr. produkthierarki  | Lageropgørelse pr. sted                     |

### <a name="manufacturing-accounting-status"></a>Produktionsregnskabsstatus

| Rapportside                | Visualisering                       |
|----------------------------|-------------------------------------|
| ÅTD for IGVF-oversigt           | Startsaldo                   |
|                            | Netto ændring                          |
|                            | Nettoændring i %                        |
|                            | Slutsaldo                      |
|                            | Omsætningshastighed for IGVF                  |
|                            | Dage for IGVF-beholdning                    |
|                            | Aktivt omkostningsobjekt i periode        |
|                            | Nettoændring pr. ressourcegruppe        |
|                            | Saldo pr. sted                     |
|                            | Kontoudtog pr. kategori               |
|                            | Nettoændring pr. kvartal               |
| IGVA-beregning              | Startsaldo                   |
|                            | Slutsaldo                      |
|                            | IGVF-kontoudtog pr. kategori           |
| IGVF-kontoudtog pr. sted      | Startsaldo                   |
|                            | Slutsaldo                      |
|                            | IGVF-kontoudtog pr. kategori og sted  |
| IGVF-kontoudtog pr. hierarki | Startsaldo                   |
|                            | Slutsaldo                      |
|                            | IGVF-kontoudtog pr. kategorihierarki |

### <a name="inventory-accounting-analysis"></a>Lagerregnskabsanalyse

| Rapportside        | Visualisering                                                                |
|--------------------|------------------------------------------------------------------------------|
| Lagerdetaljer  | 10 vigtigste ressourcer pr. slutsaldo                                           |
|                    | 10 vigtigste ressourcer pr. stigning i nettoændring                                      |
|                    | 10 vigtigste ressourcer pr. reduktion i nettoændring                                      |
|                    | 10 vigtigste ressourcer pr. lagers omsætningshastighed                                 |
|                    | Ressourcer pr. lav omsætningshastighed og slutsaldo over grænseværdi for lager |
|                    | 10 vigtigste ressourcer pr. lav nøjagtighed                                             |
| ABC-klassifikation | Lagerslutsaldo                                                     |
|                    | Forbrugt materiale                                                            |
|                    | Solgt (vareforbrug)                                                                  |
| Lagertendenser   | Lagerslutsaldo                                                     |
|                    | Lagernettoændring                                                         |
|                    | Lageromsætningshastighed                                                     |
|                    | Lagernøjagtighed                                                           |

### <a name="manufacturing-accounting-analysis"></a>Produktionsregnskabsanalyse

| Rapportside | Visualisering      |
|-------------|--------------------|
| IGVF-tendenser  | IGVF-slutsaldo |
|             | IGVF-nettoændring     |
|             | Omsætningshastighed for IGVF |

### <a name="std-cost-variance-analysis"></a>Analyse af standardomkostningsafvigelse

| Rapportside                             | Visualisering                                        |
|-----------------------------------------|------------------------------------------------------|
| ÅTD for afvigelse i købspris (standardomkostning) | Saldo for indkøb                                     |
|                                         | Afvigelse i købspris                              |
|                                         | Afvigelsesgrad for købspris                        |
|                                         | Afvigelse pr. varegruppe                               |
|                                         | Afvigelse pr. sted                                     |
|                                         | Købspris pr. kvartal                            |
|                                         | Købspris pr. kvartal og varegruppe             |
|                                         | 10 vigtigste ressourcer pr. negativt købsprisforhold |
|                                         | 10 vigtigste ressourcer pr. positivt købsprisforhold   |
| ÅTD for produktionsafvigelse (standardomkostning)     | Produktionsomkostning                                    |
|                                         | Produktionsomkostningsafvigelse                                  |
|                                         | Produktionsafvigelsesforhold                            |
|                                         | Afvigelse pr. varegruppe                               |
|                                         | Afvigelse pr. sted                                     |
|                                         | Produktionsafvigelse pr. kvartal                       |
|                                         | Produktionsafvigelse pr. kvartal og afvigelsestype     |
|                                         | 10 vigtigste ressourcer pr. negativ produktionsafvigelse  |
|                                         | 10 vigtigste ressourcer pr. positiv produktionsafvigelse    |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Data fra Microsoft Dynamics 365 for Finance and Operations bruges til at udfylde rapportsider i Power BI-indhold til **Omkostningsstyring**. Disse data repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL Server-database, der er optimeret til analyse. Du kan finde flere oplysninger under [Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

De vigtigste samlede målinger for følgende objekter bruges som grundlag af Power BI-indholdet.

| Objekt                          | Samlede nøglemålinger | Datakilde til Finance and Operations | Felt               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Beløb                     | CostObjectStatementCache               | Beløb              |
| CostObjectStatementCacheMonthly | Kvantitet                   | CostObjectStatementCache               | Antal                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Tabellen nedenfor viser de beregnede målinger i Power BI-indholdet.

| Målepunkt                            | Udregning |
|------------------------------------|-------------|
| Startsaldo                  | Startsaldo = \[Slutsaldo\]-\[Nettoændring\] |
| Antal for startsaldo             | Antal for startsaldo = \[Antal for slutsaldo\]-\[Antal for nettoændring\] |
| Slutsaldo                     | Slutsaldo = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))) |
| Antal for slutsaldo                | Antal for slutsaldo = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))) |
| Netto ændring                         | Nettoændring = SUM(\[AMOUNT\]) |
| Antal for nettoændring                    | Antal for nettoændring = SUM(\[QTY\]) |
| Lageromsætningshastighed pr. beløb | Lageromsætningshastighed pr. beløb = if(OR(\[Gennemsnitlig saldo for lager\] \<= 0, \[Lagerafgange, salg eller forbrug\] \>= 0), 0, ABS(\[Lagerafgange, salg eller forbrug\])/\[Gennemsnitlig saldo for lager\]) |
| Gennemsnitlig saldo for lager          | Gennemsnitlig saldo for lager = ((\[Slutsaldo\] + \[Startsaldo\]) / 2) |
| Dage for disponibel beholdning             | Dage for disponibel beholdning = 365 / CostObjectStatementEntries\[Lageromsætningshastighed pr. beløb\] |
| Lagernøjagtighed                 | Lagernøjagtighed pr. beløb = IF(\[Slutsaldo\] \<= 0, IF(OR(\[Lager, optalt beløb\] \<\> 0, \[Slutsaldo\] \< 0), 0, 1), MAX(0, (\[Slutsaldo\] - ABS\[Lager, optalt beløb\]))/\[Slutsaldo\])) |

Følgende nøgledimensioner bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.


| Enhed                                                  | Eksempler på attributter                          |
|---------------------------------------------------------|-------------------------------------------------|
| Produkter                                                | Produktnummer, Produktnavn, Enhed, Varegrupper |
| Kategorihierarkier (tildelt rollen Omkostningsstyring) | Kategorihierarki, Kategoriniveau              |
| Juridiske enheder                                          | Navne på juridisk enhed                              |
| Regnskabskalendere                                        | Regnskabskalender, År, Kvartal, Periode, Måned   |
| Sted                                                    | Id, Navn, Adresse, Stat, Land               |
