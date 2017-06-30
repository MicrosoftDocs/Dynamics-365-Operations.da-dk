---
title: Godkende en justeret prognose
description: "Det er ikke alle prognosedata, der skal godkendes med det samme. I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for. Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 324f7385e8064eedcf35f0f07bb3b2ef6474f410
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Godkende en justeret prognose

[!include[banner](../includes/banner.md)]


Det er ikke alle prognosedata, der skal godkendes med det samme. I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for. Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller.

Det er ikke alle prognosedata, der skal godkendes med det samme. Du kan angive start- og slutdatoerne for den periode, som prognosen er godkendt for. Denne funktion gør det muligt at fryse bestemte filsæt. 

De start- og slutdatoer, du angiver, skal svare til start- og slutdatoerne for det filsæt, som budgettet oprettes i. Systemet opretholder denne begrænsning og justerer automatisk datoer, hvis regulering er påkrævet. 

Under fanen **Detaljer** på siden **Godkendelse** kan du få vist detaljer om den prognose, der blev oprettet for nylig. 

Du kan vælge firmaerne og de prognosemodeller for at godkende den prognose, der skal bruges. Dette gitter omfatter som standard alle de firmaer, som behovsprognosen er oprettet for. For hver virksomhed bliver den prognosemodel, der svarer til den aktuelle prognoseplan, der er konfigureret i parametre for varedisponering, udfyldt på forhånd. Du kan dog ændre denne prognosemodel til en prognosemodel, der hører til det pågældende firma. Hvis der er genereret nogen behovsprognosedata for et valgt firma, modtager du en advarsel under import. 

Det er meget vigtigt, at du forstår, hvordan afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget** fungerer. Hvis du har foretaget manuelle justeringer i den statistiske budgetgrundlag, godkendes de justerede værdier til brug, også selvom dette afkrydsningsfelt er markeret. Disse ændringerne kasseres dog efter godkendelsen. Næste gang der oprettes en prognose, er prognosen er derfor kun en statistisk prognose og har ingen manuelle tilsidesættelser, også selvom **Overfør manuelle justeringer til behovsprognosen** er markeret. Derfor kan du overveje afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget**, der er en mekanisme, der gør det muligt at bevare eller slette alle manuelle ændringer.

<a name="see-also"></a>Se også
--------

[Foretage manuelle reguleringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)

[Overvågning af prognosenøjagtighed](monitor-forecast-accuracy.md)




