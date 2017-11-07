---
title: Salgs- og rentabilitetsperformance i Power BI-indhold
description: "I dette emne beskrives, hvad der er omfattet af Power BI-indhold til Salgs og rentabilitetsperformance. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97c8f3d57ba1accb8d940c7edd3ddcac2146968b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Salgs- og rentabilitetsperformance i Power BI-indhold

[!include[banner](../includes/banner.md)]

I dette emne beskrives, hvad der er omfattet af Microsoft Power BI-indhold til **Salgs og rentabilitetsperformance**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indhold til **Salgs- og rentabilitetsperformance** blev oprettet, så salgschefer kan overvåge salgsmetrikker for indtægt, bruttooverskud og overskudsgrad. Det bruger salgstransaktionsdata og indeholder både en samlet oversigt over alle firmaets salgstal og en opdeling af salgsperformance for kunder og produkter.

Rapporter fremhæver ændringer i indtægter og overskudsvækst over tid. Derfor kan de bruges til at give ledere besked om positive og negative tendenser for individuelle kunder og produkter. Derudover sammenligner diagrammer indtægter og rentabilitet over forskellige produktkategorier og kundegrupper med hinanden. Derfor kan kategorier og regionale ledere identificere tabere og vindere. Endelig afbilder en omfattende rapport en individuel kundes indtægt i forhold til overskudsgrad. Derfor har kontoadministratorer et databaseret fundament, hvor de kan tilpasse deres salgs- og marketingbestræbelser efter hver kundes profil. 

Med indholdet af **Salgs- og rentabilitetsperformance** har salgschefer mulighed for at analysere performance på følgende måder:

-   Omsætning, år til dato (efter kundegruppe og individuelle kunder, salgskategorier og individuelle produkter og geografiske områder)
-   Omsætningsændring, år for år (efter kunderegioner og salgskategorier)

Rentabiliteten kan analyseres på disse måder:

-   Bruttoavance og overskudsgrad (efter kundegrupper og produktsalgskategorier)
-   Bruttoavanceændring, år for år
-   Kunderentabilitet (efter omsætning i forhold til bruttoavance)

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vises Power BI-indholdet af **Salgs- og rentabilitetsperformance** på siden **Salgs- og rentabilitetsperformance** (**Salg og marketing** > **Forespørgsler og rapporter** > **Performanceanalyse for salg** > **Salgs- og rentabilitetsperformance**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indhold
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

## <a name="extending-the-power-bi-content"></a>Udvidelse af Power BI-indhold
Når du bruger de indholdspakker, der er tilgængelige i Microsoft Dynamics Lifecycle Services (LCS), kan du levere fremragende analyser til personer, der ikke logger på Microsoft Dynamics 365. Du kan redigere disse indholdspakker, så de omfatter andre rapporter eller grafik, og derefter udgive indholdspakkerne på din Power BI.com-lejer med henblik på analyse.

Du kan finde Power BI-indhold til **Salgs- og rentabilitetsperformance** i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Sørg for at downloade **Salgs og rentabilitetsperformance**-indholdet, der gælder for den version af Dynamics 365, du bruger.

> [!NOTE]
> Hvis du bruger Microsoft Dynamics 365 for Operations version 1611, er KB 4011327 en forudsætning for dette Power BI-indhold. Når du logger på LCS, kan du få adgang til KB på https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende data bruges til at udfylde rapporten i Power BI-indholdet til **Salgs og rentabilitetsperformance**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md). 

De samlede målinger i denne indholdspakke er et undersæt af de samlede målinger, der var tilgængelige i salgskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager i blogindlægget [Power BI-integration med enhedslager i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). 

Følgende samlede nøglemålinger for enheden Fakturalinjer bruges som grundlag for indholdet.

| Enhed        | Samlede nøglemålinger                   | Datakilden til Dynamics 365                    | Felt                                        | Betegnelse                                   |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|----------------------------------------------|
| Fakturalinjer | Indtægter                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Beløbet i regnskabsvalutaen.            |
|               | Vareforbrug                           | InventTrans                                     | SUM (CostAmountPosted + CostAmountAdjustment) | Summen af kostbeløbet og reguleringen.    |
|               | Provisionslinjebeløb – regnskabsvaluta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisionsbeløbet i regnskabsvalutaen. |

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

