---
title: Power BI-indhold til købsforbrugsanalyse
description: Denne artikel beskriver, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "265434"
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 3befeb2b53f6b47cb23edbf520f49f88bd978d76
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206685"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-indhold til købsforbrugsanalyse

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvad der skal medtages i Microsoft Power BI-indhold til **Købsforbrugsanalyse**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde styr på udgifter til køb. Chefer kan analysere indkøbsudgifter på følgende måder:

- Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)
- Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)

Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare. Rapporter fremhæve ændringer i købsforbruget over tid. Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter. Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper. Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
**Power BI-indholdet til Købsforbrugsanalyse** vises på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** \> **Forespørgsler og rapporter** \> **Performanceanalyse for indkøb** \> **Købs- og forbrugsanalyse**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
**Power BI-indholdet til købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker. Disse metrikker visualiseres som diagrammer, felter og tabeller. 

I nedenstående sektioner vises en oversigt over visualiseringerne.

### <a name="purchase-by-vendor-report-page"></a>Rapportsiden Indkøb efter leverandør
**Diagrammer**
- Top 10 leverandører efter indkøb (stablet liggende søjlediagram)
- Samlet indkøb pr. leverandørgruppe/land/område/navn (cirkeldiagram)
- Indkøb pr. leverandørgruppe/land/område/navn (søjlediagram)
- Gennemsnitsindkøb pr. leverandørgruppe/land/område/navn (søjlediagram)

**Felter**
- Indkøb i alt
- Indkøbsvækst år for år
- Antal leverandører i alt
- Antal aktive leverandører i alt

**Eksempel**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Rapportsiden Køb pr. produkt

**Diagrammer**
- Køb efter indkøbskategori/produktnavn (søjlediagram)
- Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)
- Top 10 produkter efter indkøb (stablet liggende søjlediagram)

**Felter**
- Antal produkter i alt</li>
- Antal aktive produkter i alt i procentdel af antal produkter i alt
- Antal produkter, der udgør for 80 % af indkøbet

**Eksempel**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Rapportsiden Indkøb efter periode
Denne side viser køb dette og sidste år, og vækst efter indkøbskategori.

**Diagrammer** 
- Indkøb pr. måned/dag (søjlediagram)
- Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)
- Vækst i indkøb i alt år for år (søjlediagram)
- Indkøbsopgørelse (matrix)

**Felter**
- Indkøbsvækst år for år
- Indkøbsvækst år for år i %

**Eksempel**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Rapportsiden Indkøb efter leverandørlokalitet

**Diagrammer**
- Indkøb efter by
- Indkøbsvækst år for år i %
- Indkøb efter land/område

**Eksempel**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Rapportsiden Købsforbrugsanalyse efter tidspunkt

**Diagrammer** 
- Indkøb indeværende år efter måned/dag (kurvediagram)
- Køb indeværende og sidste år (linje- og søjlediagram)

**Eksempel**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Rapportsiden Købsforbrugsanalyse efter leverandør

**Diagrammer** 
- Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)
- Top 10 leverandører med forøget forbrug år for år
- Top 10 leverandører med faldende forbrug år for år

**Eksempel:** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Datamodel og enheder
Følgende data bruges til at udfylde rapportsiderne i **Power BI-indholdet til Købsforbrugsanalyse**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).

De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i købskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Power BI-integration med enhedslager](power-bi-integration-entity-store.md). Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.

| Enhed        | Samlede nøglemålinger | Datakilde                                 | Felt              | Betegnelse                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fakturalinjer | Køb                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløbet i regnskabsvalutaen. |

Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.

| Målepunkt               | Kalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Køb indeværende år | Køb indeværende år = SUM('Invoice lines'\[Purchase\])                                            |
| Køb sidste år    | Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Indkøbsvækst år for år   | Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]                            |

Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.

| Enhed                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Kreditorgrupper, kreditorlande eller -områder, kreditornavn |
| Produkter               | Produktnummer, produktnavn, varegruppenavn        |
| Indkøbskategorier | Indkøbskategori, indkøbskategorinavne      |
| Juridiske enheder         | Navn på juridisk enhed                                     |
| Datoer                  | Datoer, årsforskydning                                    |

Som standard viser indholdet data for det indeværende kalenderår. Du kan dog ændre datofilteret i rapportens filterafsnit. Du kan også ændre firmafilteret.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
