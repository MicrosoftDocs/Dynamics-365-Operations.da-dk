---
title: Power BI-indhold til Salgs og rentabilitetsperformance
description: Denne artikel beskriver, hvad der er omfattet af Power BI-indhold til Salgs og rentabilitetsperformance.
author: ShylaThompson
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8433250efad467e92aeaa851f0b60c3c1eced99c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898676"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Power BI-indhold til Salgs og rentabilitetsperformance

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvad der er omfattet af **Salgs og rentabilitetsperformance** i Microsoft Power BI-indhold. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indhold til **Salgs- og rentabilitetsperformance** blev oprettet, så salgschefer kan overvåge salgsmetrikker for indtægt, bruttooverskud og overskudsgrad. Det bruger salgstransaktionsdata og indeholder både en samlet oversigt over alle firmaets salgstal og en opdeling af salgsperformance for kunder og produkter.

Rapporter fremhæver ændringer i indtægter og overskudsvækst over tid. Derfor kan de bruges til at give ledere besked om positive og negative tendenser for individuelle kunder og produkter. Derudover sammenligner diagrammer indtægter og rentabilitet over forskellige produktkategorier og kundegrupper med hinanden. Derfor kan kategorier og regionale ledere identificere tabere og vindere. Endelig afbilder en omfattende rapport en individuel kundes indtægt i forhold til overskudsgrad. Derfor har kontoadministratorer et databaseret fundament, hvor de kan tilpasse deres salgs- og marketingbestræbelser efter hver kundes profil.

Med indholdet af **Salgs- og rentabilitetsperformance** har salgschefer mulighed for at analysere performance på følgende måder:

- Omsætning, år til dato (efter kundegruppe og individuelle kunder, salgskategorier og individuelle produkter og geografiske områder)
- Omsætningsændring, år for år (efter kunderegioner og salgskategorier)

Rentabiliteten kan analyseres på disse måder:

- Bruttoavance og overskudsgrad (efter kundegrupper og produktsalgskategorier)
- Bruttoavanceændring, år for år
- Kunderentabilitet (efter omsætning i forhold til bruttoavance)

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Power BI-indholdet **Salgs og rentabilitetsperformance** vises på siden **Salgs og rentabilitetsperformance** (**Salg og marketing** \> **Forespørgsler og rapporter** \> **Performanceanalyse for salg** \> **Salgs og rentabilitetsperformance**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
Power BI-indholdet til **Salgs- og rentabilitetsperformance** omfatter en rapport, der består af et sæt nøgletal. Disse metrikker visualiseres som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i indholdet.

| Rapportside            | Diagrammer                                     | Felter                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Omsætning efter kunde    | Top 10-kunder efter omsætning                | Samlet omsætning                                           |
|                        | Samlet omsætning efter kundegruppe            | Stigning år for år i omsætning                                      |
|                        | Gennemsnitlig kundeomsætning efter kundegruppe | Bruttoavance                                            |
|                        | Omsætning og bruttoavance efter kundegruppe   |                                                         |
| Omsætning efter produkt     | Omsætning og bruttoavance efter salgskategori   | I alt \# produkter                                    |
|                        | Top 10-produkter efter omsætning                 | Antal aktive produkter i alt og procentdel af antal produkter i alt |
|                        | Omsætning i alt efter salgskategori            | Antal produkter, der udgør for 80 % af omsætningen           |
| Omsætning pr. periode\*    | Omsætning pr. måned                           | Stigning år for år i omsætning                                      |
|                        | Efterfølgende omsætningsafvigelse år for år             | Stigning i % år for år i omsætning                                    |
|                        | Afvigelse i salg i alt efter kundeområde    |                                                         |
| Omsætning efter lokalitet    | Omsætning efter by                      |                                                         |
|                        | Stigning i % år for år i omsætning                       |                                                         |
|                        | Omsætning pr. område                    |                                                         |
| Kunderentabilitet | Bruttoavance i forhold til omsætning, efter kunde   | Bruttofortjeneste, dækningsbidrag, stigning i omsætningen år for år          |
| Rentabilitetsanalyse | Omsætning og bruttoavance pr. måned          |                                                         |
|                        | Top 15-kunder efter bruttoavance           |                                                         |
|                        | Bruttoavance pr. måned, år for år                 |                                                         |

\* Omsætning dette og sidste år, og vækst efter salgskategori.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende data bruges til at udfylde rapporten i Power BI-indholdet til **Salgs og rentabilitetsperformance**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).

De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i salgskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager i blogindlægget [Power BI-integration med enhedslager i Dynamics](/archive/blogs/dynamicsaxbi/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update).

Følgende samlede nøglemålinger for enheden Fakturalinjer bruges som grundlag for indholdet.

| Enhed        | Samlede nøglemålinger                   | Datakilden til Dynamics 365 | Felt                                        | Betegnelse                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Fakturalinjer | Indtægter                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Beløbet i regnskabsvalutaen.            |
|               | Vareforbrug                           | InventTrans                  | SUM (CostAmountPosted + CostAmountAdjustment) | Summen af kostbeløbet og reguleringen.    |
|               | Provisionslinjebeløb – regnskabsvaluta | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Provisionsbeløbet i regnskabsvalutaen. |

Nedenstående tabel viser de samlede nøglemålinger af enheden Fakturalinjer, der bruges til at oprette flere beregnede målepunkter i indholdspakkens datasæt.

| Målepunkt           | Kalkulation                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Bruttoavance      | SUM(Omsætning – vareforbrug – provision – moms (inkluderet i debitorfakturalinjebeløb))          |
| Bruttoavance      | SUM(Bruttoavance/(Omsætning - moms (inkluderet i debitorfakturalinjebeløb)))             |
| Omsætning sidste år | Omsætning sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |

Følgende nøgledimensioner i salgskuben bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.

| Enhed           | Eksempler på attributter                               |
|------------------|------------------------------------------------------|
| Kunder        | Debitorgrupper, kundeområder, adresse, branche |
| Produkter         | Produktnummer, produktnavn, varegruppenavn       |
| Salgskategorier | Navne på salgskategorier                                 |
| Juridiske enheder   | Navne på juridisk enhed                                   |
| Datoer            | Datoer                                                |

Som standard viser indholdet data for det indeværende kalenderår. Du kan dog ændre datofilteret i rapportens filterafsnit. Du kan også ændre firmafilteret.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]