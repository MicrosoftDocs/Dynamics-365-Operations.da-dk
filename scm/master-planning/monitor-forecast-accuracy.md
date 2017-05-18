---
title: "Overvåge prognosenøjagtighed"
description: "I denne artikel beskrives de typer af prognosenøjagtighed, som Microsoft Dynamics 365 for Operations beregner, og forklarer, hvordan du kan få vist nøjagtighedsværdierne."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7e470e05d9acb1e7417d0d77655be99e94d15e1d
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Overvåge prognosenøjagtighed

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de typer af prognosenøjagtighed, som Microsoft Dynamics 365 for Operations beregner, og forklarer, hvordan du kan få vist nøjagtighedsværdierne.

Dynamics 365 for Operations beregner følgende typer prognosenøjagtighed:

-   Historiske prognosenøjagtighed ved at sammenligne den historiske prognose, som Varedisponering bruger, med den historiske efterspørgsel. For at få vist værdierne (både de absolutte værdier og procentvise værdier) for historisk prognosenøjagtighed skal du klikke på **Vis nøjagtighed** på siden **Detaljer om behovsprognose**.
-   Den anslåede nøjagtighed af den prognosemodel, der bruges til at generere forudsigelserne. Du kan få vist en procentangivelse for nøjagtighed under **Modeldetaljer – MAPE** på siden **Detaljer om behovsanalyse**. 

**Bemærk!** Hvis du bruger Dynamics 365 for Operations-tjenesten til behovsprognose med Microsoft Azure Machine Learning, baseres beregningen af nøjagtigheden af den interne model på testdatasæt. Hvis du vil angive størrelsen på testdatasættet, skal du indstille parameteren **TEST\_SET\_SIZE\_PERCENT** på siden **Parametre til behovsprognoser**. Hvis du f.eks. indstiller værdien til **20**, bruges de sidste 20 procent af de historiske data til at beregne nøjagtigheden af den interne model.


<a name="see-also"></a>Se også
--------

[Godkende den justerede prognose](authorize-adjusted-forecast.md)

[Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose](remove-historical-outliers-calculating-demand-forecast.md)




