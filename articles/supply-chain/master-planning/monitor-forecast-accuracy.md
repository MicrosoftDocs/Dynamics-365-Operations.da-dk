---
title: Overvåge prognosenøjagtighed
description: I dette emne beskrives de typer af prognosenøjagtighed, som Dynamics 365 Supply Chain Management beregner, og det forklares, hvordan du kan få vist nøjagtighedsværdierne.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab74ba88ba9eb683107ef82bc105f5a3ed8fac08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209806"
---
# <a name="monitor-forecast-accuracy"></a>Overvåge prognosenøjagtighed

[!include [banner](../includes/banner.md)]

I dette emne beskrives de typer af prognosenøjagtighed, som Microsoft Dynamics 365 Supply Chain Management beregner, og det forklares, hvordan du kan få vist nøjagtighedsværdierne.

Supply Chain Management beregner følgende typer prognosenøjagtighed:

-   Historiske prognosenøjagtighed ved at sammenligne den historiske prognose, som Varedisponering bruger, med den historiske efterspørgsel. For at få vist værdierne (både de absolutte værdier og procentvise værdier) for historisk prognosenøjagtighed skal du klikke på **Vis nøjagtighed** på siden **Detaljer om behovsprognose**.
-   Den anslåede nøjagtighed af den prognosemodel, der bruges til at generere forudsigelserne. Du kan få vist en procentangivelse for nøjagtighed under **Modeldetaljer – MAPE** på siden **Detaljer om behovsanalyse**. 

> [!NOTE]
> Hvis du bruger Microsoft Azure Machine Learning Behovsprognosen, baseres beregningen af nøjagtigheden af den interne model på testdatasæt. Hvis du vil angive størrelsen på testdatasættet, skal du indstille parameteren **TEST\_SET\_SIZE\_PERCENT** på siden **Parametre til behovsprognoser**. Hvis du f.eks. indstiller værdien til **20**, bruges de sidste 20 procent af de historiske data til at beregne nøjagtigheden af den interne model.


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Autorisere en justeret prognose](authorize-adjusted-forecast.md)

[Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose](remove-historical-outliers-calculating-demand-forecast.md)



