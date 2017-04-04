---
title: Tillade et korrigerede budget
description: "Det er ikke alle prognosedata, der skal godkendes med det samme. I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for. Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Tillade et korrigerede budget

Det er ikke alle prognosedata, der skal godkendes med det samme. I denne artikel forklares, hvordan du kan angive den periode, som en prognose er godkendt for. Den forklarer også, hvordan du kan godkende prognosen for specifikke firmaer og prognosemodeller.

Det er ikke alle prognosedata, der skal godkendes med det samme. Du kan angive start- og slutdatoerne for den periode, som prognosen er godkendt for. Denne funktion gør det muligt at fryse bestemte filsæt. 

Start- og slutdatoer, du angiver skal svare til start- og slutdatoerne for filsæt, som budgettet oprettes i. Systemet opretholder denne begrænsning og justerer automatisk datoer, hvis justering er påkrævet. 

Under fanen **Detaljer** på siden **Godkendelse** kan du få vist detaljer om den prognose, der blev oprettet for nylig. 

Du kan vælge firmaerne og de prognosemodeller for at godkende den prognose, der skal bruges. Dette gitter omfatter som standard alle de firmaer, som behovsprognosen er oprettet for. For hver virksomhed bliver den prognosemodel, der svarer til den aktuelle prognoseplan, der er konfigureret i parametre for varedisponering, udfyldt på forhånd. Du kan dog ændre denne prognosemodel til en prognosemodel, der hører til det pågældende firma. Hvis der er genereret nogen behovsprognosedata for et valgt firma, modtager du en advarsel under import. 

Det er meget vigtigt, at du forstår, hvordan afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget ** fungerer. Hvis du har foretaget manuelle justeringer til den statistiske oprindelige budget, er de justerede værdier tilladt, selv hvis dette afkrydsningsfelt ikke er markeret. Disse ændringerne kasseres dog efter godkendelsen. Næste gang der oprettes en prognose, er prognosen er derfor kun en statistisk prognose og har ingen manuelle tilsidesættelser, også selvom **Overfør manuelle justeringer til behovsprognosen** er markeret. Derfor kan du overveje afkrydsningsfeltet **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget **, der er en mekanisme, der gør det muligt at bevare eller slette alle manuelle ændringer.

<a name="see-also"></a>Se også
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


