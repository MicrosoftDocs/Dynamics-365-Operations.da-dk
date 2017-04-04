---
title: "Skærm forecast præcision"
description: "I denne artikel beskrives typerne budgetterede nøjagtighed, at Microsoft Dynamics 365 for operationer beregnes, og forklarer, hvordan du kan få vist de korrekte værdier."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Skærm forecast præcision

I denne artikel beskrives typerne budgetterede nøjagtighed, at Microsoft Dynamics 365 for operationer beregnes, og forklarer, hvordan du kan få vist de korrekte værdier.

Dynamics 365 for operationer beregnes følgende typer budgetterede nøjagtighed:

-   Historiske prognosenøjagtighed ved at sammenligne den historiske prognose, som Varedisponering bruger, med den historiske efterspørgsel. For at få vist værdierne (både de absolutte værdier og procentvise værdier) for historisk prognosenøjagtighed skal du klikke på **Vis nøjagtighed** på siden **Detaljer om behovsprognose**.
-   Den anslåede nøjagtighed af den prognosemodel, der bruges til at generere forudsigelserne. Du kan få vist en procentangivelse for nøjagtighed under **Modeldetaljer – MAPE** på siden **Detaljer om behovsanalyse**. 

**Bemærk:** Hvis du bruger Dynamics-365 for operationer efterspørgsel, prognoser Microsoft Azure Machine Learning service, beregning af den interne model nøjagtighed er baseret på test-datasæt. For at angive størrelsen af test-datasæt, angive den **TEST\_angive\_størrelse\_%** parameter på den **efterspørgsel, prognoser parametre** side. Hvis du f.eks. indstiller værdien til **20**, bruges de sidste 20 procent af de historiske data til at beregne nøjagtigheden af den interne model.


<a name="see-also"></a>Se også
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


