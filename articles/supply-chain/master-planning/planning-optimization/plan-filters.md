---
title: Anvend filtre på en plan
description: I dette emne beskrives det, hvordan du kan anvende filtre på en plan, når funktionen Planlægningsoptimering anvendes.
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9d1431cc8db6fb28d1f1ec73ee07dd15e78f82e8
ms.sourcegitcommit: 65f4b8a751670a7fe9ef4cb8b218213f792d57a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945413"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a>Anvend filtre på en plan

Når funktionen Planlægningsoptimering bruges, kan du anvende et filter på en plan. **Planfilteret** anvendes altid under en varedisponeringskørsel. Et **Planfilter** er nyttigt, når du vil begrænse en plan til en bestemt varegruppe og sikre dig, at ingen andre varer medtages som en del af den afsluttende varedisponering.

Hvis der anvendes et **Planfilter**, og der også anvendes et kørselsfilter under varedisponeringskørslen, er det kun sammenfaldet mellem de to filtre, der medtages i planlægningskørslen.

Du kan få adgang til **Planfiltret** fra **Behovsplaner**, når der bruges Planlægningsoptimering.

## <a name="example-scenario"></a>Eksempelscenario

Der oprettes et planfilter, der omfatter varer A, B og C. Varedisponering kører derefter i samme plan, men der anvendes forskellige kørselsfiltre:

- **Kørselsfilter, der indeholder vare D:** Der er ikke planlagt nogen varer, fordi der ikke er noget sammenfald mellem planfilteret og kørselsfilteret.
- **Kørselsfilter, der omfatter vare A og D:** Kun vare A indgår i planlægningskørslen, fordi vare D ikke indgår i planfilteret.
- **Kørselsfilter, der omfatter vare B:** Kun vare B indgår i planlægningskørslen, og det forrige planlagte out for vare A bibeholdes.
- **Kørselsfilter, der omfatter alle varer (tomt filter):** Varerne A, B og C medtages i planlægningskørslen, og den forrige output for planlægning for vare A og B overskrives.

> [!NOTE]
> Du bør undgå at angive et planfilter på den plan, der er valgt som **Aktuel dynamisk behovsplan** på siden **Varedisponeringsparametre**. Ellers vil funktionaliteten for den dynamiske behovsplan begrænses til de filtrerede elementer. Hvis nettobehovet f.eks. opdateres for en vare, der ikke er en del af planfilteret, vil der ikke blive genereret et resultat.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Oversigt over Planlægningsoptimering](planning-optimization-overview.md)

[Introduktion til Planlægningsoptimering](get-started.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
