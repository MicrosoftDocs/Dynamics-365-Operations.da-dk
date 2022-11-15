---
title: Intern planlægning
description: Denne artikel beskriver den interne planlægning og forklarer, hvordan du konfigurerer intern planlægning i Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3d1c82aa3810b37b06b9d9157e73588fc1727348
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740026"
---
# <a name="intercompany-planning"></a>Intern planlægning

[!include [banner](../../includes/banner.md)]

I nogle organisationer afhænger logistikdriften af andre juridiske enheder (firmaer) i organisationen. Denne drift håndteres ved hjælp af interne salg og indkøb, fordi hver juridiske enhed har en separat kontoplan.

Denne artikel beskriver den interne planlægning og forklarer, hvordan du konfigurerer intern planlægning i Microsoft Dynamics 365 Supply Chain Management.

Denne artikel anvender følgende vigtige interne begreber:

- **Upstream** – En relativ reference i en firma- eller forsyningskæde. Den angiver bevægelse i retning af råvareleverandøren.
- **Downstream** – En relativ reference i en firma- eller forsyningskæde. Den angiver bevægelse i retning af kunden.
- **Planlagt intern efterspørgsel** – Planlagt behov for et produkt i et firma, baseret på den planlagte efterspørgsel efter produktet fra et downstream-firma.

I varedisponering kan en plan i et firma omfatte planlagt intern efterspørgsel, der er relateret til ordreforslag fra en plan i et andet firma. Denne funktion er nyttig, fordi den giver fuld synlighed over ordreforslag på tværs af firmaer. Det sikrer også, at alle påkrævede planlagte forsyningsordrer oprettes, men uden at kræve, at ordreforslag autoriseres for den interne efterspørgsel.

Hvis du kører varedisponering fra en behovsplan, der omfatter planlagt downstream-behov, vil indkøbsordreforslag fra de relaterede interne leverandører blive medtaget i planen som et behov.

## <a name="required-setup"></a>Nødvendig opsætning

Hvis du vil bruge intern planlægning, skal du forberede systemet på følgende måde:

1. De relevante produkter skal frigives i alle relevante firmaer. Yderligere oplysninger finder du i [Konfigurere og bruge intern handel i Dynamics 365 Supply Chain Management](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Downstream-behov skal være dækket af indkøb fra en leverandør, der har en intern relation til upstream-firmaet, og relevante standardlagerdimensioner (lokation og lagersted) på kunden. Yderligere oplysninger finder du i [Konfigurere og bruge intern handel i Dynamics 365 Supply Chain Management](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Behovsplanen i upstream-firmaet skal indeholde planlagt downstream-efterspørgsel, og det relevante firma og behovsplanen skal være angivet i de downstream-planerne.

## <a name="include-planned-downstream-demand"></a>Inkluder planlagt downstream-efterspørgsel

Hvis du vil konfigurere din behovsplan, så den omfatter planlagt downstream-efterspørgsel, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg eller opret en behovsplan.
1. I oversigtspanelet **Intern planlægning** skal du indstille følgende felter:

    - **Medtag planlagt downstream-efterspørgsel** – Angiv denne indstilling til *Ja* for at aktivere intern planlægning for behovsplanen.
    - **Downstream-planer** – Hvis du angiver indstillingen **Medtag planlagt downstream-efterspørgsel** til *Ja*, skal du bruge værktøjslinjen og gitteret til at tilføje de ønskede behovsplaner fra andre firmaer.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Udligne på tværs af firmaer ved hjælp af udligning på flere niveauer

I udligninger på flere niveauer kan du få vist udligning på tværs af firmaer for at se den første kilde til efterspørgslen, der er dækket af en forsyning.

Benyt følgende fremgangsmåde for at få vist oplysninger om udligning på flere niveauer.

1. Gå til **Varedisponering \> Varedisponering \> Ordreforslag**.
1. Vælg eller åbn et ordreforslag.
1. Vælg **Udligning på flere niveauer** i gruppen **Krav** under fanen **Vis** i handlingsruden.

### <a name="intercompany-example-that-involves-two-companies"></a>Internt eksempel, der involverer to firmaer

I dette eksempel oprettes der et produktionsordreforslag i USMF-firmaet, der dækker en salgsordrer i DEMF-firmaet. I USMF er den direkte efterspørgsel en planlagt intern efterspørgsel. For at få dette behov vist i USMF, køres varedisponering først i DEMF og derefter i USMF.

I følgende illustration vises, hvordan dette eksempel kan se ud på siden **Udligning på flere niveauer** for den planlagte produktionsordre.

![Internt eksempel, der involverer to firmaer.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Internt eksempel, der involverer tre firmaer

I dette eksempel oprettes der et indkøbsordreforslag i USMF-firmaet, der dækker en salgsordrer i FRRT-firmaet. I firmaerne DEMF og USMF er den direkte efterspørgsel en planlagt intern efterspørgsel. For at få dette behov vist i USMF, køres varedisponering først i FRRT , derefter i DEMF og til sidst i USMF.

I følgende illustration vises, hvordan dette eksempel kan se ud på siden **Udligning på flere niveauer** for den planlagte produktionsordre.

![Internt eksempel, der involverer tre firmaer.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
