---
title: "Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose"
description: "Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose. Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72735c9e3fb4291076f0b577f45384dec319b2a7
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose

[!include[banner](../includes/banner.md)]


Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose. Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed.

Du kan udelukke afvigelser for at forbedre prognosens nøjagtighed. Denne opgave er valgfri. Her er en oversigt over processen:

1.  Klik på **Overordnet planlægning** &gt; **Opsætning** &gt; **Behovsprognose** &gt; **Fjernelse af afvigelse** for at åbne siden **Fjernelse af afvigelse**, hvor du kan bruge en forespørgsel til at vælge posteringerne, der skal udelades.
2.  Vælg det regnskab, som forespørgslen gælder for, og angiv derefter et navn og en beskrivelse. Feltet **Forespørgselsdato** angives automatisk til den aktuelle dato.
3.  Markér afkrydsningsfeltet **Aktiv** for at udelukke de transaktioner, som forespørgslen finder fra de historiske data. Denne indstilling træder i kraft, når du opretter en oprindelig prognose.
4.  På siden **Forespørgsel om fjernelse af afvigelse** kan du tilføje, fjerne og vælge de kriterier, der definerer, hvilke transaktioner der udelades, når den oprindelige prognose beregnes. Du kan f.eks. vælge en bestemt vare eller ordretransaktion, der skal udelukkes.
5.  Klik på **Vis posteringer**. Siden **Afvigelsestransaktioner** viser de transaktioner, der opfylder de kriterier, du har defineret i forespørgslen, og som skal udelukkes fra de historiske data, når behovsprognosen beregnes.

**Bemærk!** Du kan også oprette en forespørgsel, der er baseret på en eksisterende forespørgsel. Vælg den forespørgsel, der skal kopieres, og klik derefter på **Dupliker**. Feltet **Forespørgselsdato** identificerer versionen. Du kan bruge forespørgslen, som den er, eller du kan klikke på **Rediger forespørgsel** for at ændre kriterierne. Du kan eventuelt ændre navnet og beskrivelsen for den nye forespørgsel.

<a name="see-also"></a>Se også
--------

[Introduktion til behovsprognoser](introduction-demand-forecasting.md)

[Overvågning af prognosenøjagtighed](monitor-forecast-accuracy.md)



