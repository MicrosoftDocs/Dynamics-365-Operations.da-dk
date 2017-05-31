---
title: "Importér historiske data til behovsprognoser"
description: "For at få nøjagtige behovsprognoser skal du have historiske behovsdata pr. vare eller varefordelingsnøgle. Dette emne forklarer, hvordan du bruger dataenheder til at importere historiske behovsdata fra alle systemer, så du har en længere historik over behovsprognosedata."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Importér historiske data til behovsprognoser

[!include[banner](../includes/banner.md)]

For at garantere for nøjagtigheden af behovsprognoser skal du have så mange historiske behovsdata pr. vare eller en varefordelingsnøgle, som du kan få. Hvis du ikke allerede har importeret historiske behovsdata, kan du bruge dataenheden **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Microsoft Dynamics 365 for Operations til at importere dem.

I arbejdsområdet **Datastyring**, kan du se en oversigt over alle felterne i enheden.

1. Åbn arbejdsområdet **Datastyring**.
2. Klik på feltet **Dataenheder**.
3. Søg i enhedslisten efter **Historisk eksternt behov**.
4. Klik på **Målfelter**. Følgende enhedsfelter er obligatoriske: websted (**DeliveringSiteId**), dato (**DemandDate**), antal (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøgle (**ProductAllocationKeyId**).

For at kunne bruge dataenheden skal du have en Microsoft Excel-fil eller kommaseparerede værdier (CSV), der indeholder de historiske behovsdata. Følgende eksempel viser, hvordan du importerer data fra en CSV-fil.

## <a name="example"></a>Eksempel

Du kan bruge følgende fil som et eksempel. Hent [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Denne fil indeholder de historiske behovsdata for vare D0001. Den indeholder kun følgende obligatoriske felter: websted, antal og behovsdatoen.

1. Vælg det firma, du vil importere de historiske behovsdata til.
2. Åbn arbejdsområdet **Datastyring**.
3. Klik på feltet **Importér**.
4. Angiv et navn til importprojektet, f.eks. **Importér historiske behov for vare D0001**.
5. I feltet **Kildedataformat** skal du vælge formatet på den fil, du importerer. Hvis du vil importere filen HistoricalDemandData i dette eksempel, skal du vælge **CSV**.
6. I feltet **Enhedsnavn** skal du vælge **Historisk eksternt behov**.
7. Gem filen på computeren, og overfør den derefter.
8. Klik på **Importér**.
9. Siden **Udførelsesoversigt** åbnes automatisk. Kontrollér de importerede data på siden.

Når du har importeret de historiske behovsdata, kan du generere en behovsprognose.

## <a name="see-also"></a>Se også

[Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)

