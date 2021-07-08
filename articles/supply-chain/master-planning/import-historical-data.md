---
title: Importér historiske data til behovsprognoser
description: For at få nøjagtige behovsprognoser skal du have historiske behovsdata pr. vare eller varefordelingsnøgle. Dette emne forklarer, hvordan du bruger dataenheder til at importere historiske behovsdata fra alle systemer, så du har en længere historik over behovsprognosedata.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301644"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Importér historiske data til behovsprognoser

[!include [banner](../includes/banner.md)]

For at garantere for nøjagtigheden af behovsprognoser skal du have så mange historiske behovsdata pr. vare eller en varefordelingsnøgle, som du kan få. Hvis du ikke allerede har importeret historiske behovsdata, kan du bruge dataenheden **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til at importere dem.

I arbejdsområdet **Datastyring**, kan du se en oversigt over alle felterne i enheden.

1. Åbn arbejdsområdet **Datastyring**.
2. Vælg feltet **Dataenheder**.
3. Søg i enhedslisten efter **Historisk eksternt behov**.
4. Vælg **Målfelter**. Følgende enhedsfelter er obligatoriske: websted (**DeliveringSiteId**), dato (**DemandDate**), antal (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøgle (**ProductAllocationKeyId**).

For at kunne bruge dataenheden skal du have en Microsoft Excel-fil eller kommaseparerede værdier (CSV), der indeholder de historiske behovsdata. Følgende eksempel viser, hvordan du importerer data fra en CSV-fil.

Yderligere oplysninger om, hvordan du importerer data, herunder hvordan du rydder data efter en import, finder du i [Oversigt over dataimport- og -eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og relaterede emner.

Se også [Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]