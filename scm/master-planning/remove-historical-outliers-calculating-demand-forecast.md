---
title: "Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose"
description: "Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose. Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose

Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose. Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed.

Du kan udelade afvigende resultater for at forbedre nøjagtigheden af prognose. Denne opgave er valgfri. Her er en oversigt over processen:

1.  Klik på **Master planning**&gt;**Setup**&gt;**efterspørgsel prognoser**&gt;**afvigende fjernelse** at åbne den **afvigende fjernelse** side, hvor du kan bruge en forespørgsel til at vælge posteringerne, der skal udelades.
2.  Vælg det regnskab, som forespørgslen gælder for, og angiv derefter et navn og en beskrivelse. Feltet **Forespørgselsdato** angives automatisk til den aktuelle dato.
3.  Markér afkrydsningsfeltet **Aktiv** for at udelukke de transaktioner, som forespørgslen finder fra de historiske data. Denne indstilling træder i kraft, når du opretter en oprindelig prognose.
4.  På siden **Forespørgsel om fjernelse af afvigelse** kan du tilføje, fjerne og vælge de kriterier, der definerer, hvilke transaktioner der udelades, når den oprindelige prognose beregnes. Du kan f.eks. vælge en bestemt vare eller ordretransaktion, der skal udelukkes.
5.  Klik på **Vis posteringer**. Siden **Afvigelsestransaktioner** viser de transaktioner, der opfylder de kriterier, du har defineret i forespørgslen, og som skal udelukkes fra de historiske data, når behovsprognosen beregnes.

**Bemærk!** Du kan også oprette en forespørgsel, der er baseret på en eksisterende forespørgsel. Vælg den forespørgsel, der skal kopieres, og klik derefter på **Dupliker**. Feltet **Forespørgselsdato** identificerer versionen. Du kan bruge forespørgslen, som den er, eller du kan klikke på **Rediger forespørgsel** for at ændre kriterierne. Du kan eventuelt ændre navnet og beskrivelsen for den nye forespørgsel.

<a name="see-also"></a>Se også
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

