---
title: Planlægning med negative disponible lagerantal
description: I dette emne beskrives, hvordan negative lagerbeholdninger håndteres, når du bruger planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983460"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Planlægning med negative disponible lagerantal

[!include [banner](../../includes/banner.md)]

Hvis systemet viser et negativt samlet disponibelt lagerantal, behandler planlægningsmotoren antallet som 0 (nul) for at undgå overforsyning. Funktionen fungerer på følgende måde:

1. Planlægningsoptimeringsfunktionen aggregerer de disponible antal i det laveste niveau af disponeringsdimensioner. (Hvis f.eks. *sted* ikke er en disponeringsdimension, aggregerer planlægningsoptimering antallet på *lagersteds*-niveau.)
1. Hvis det samlede disponible antal på det laveste niveau af disponeringsdimensionen er negativt, antager systemet, at den disponible mængde er 0 (nul).

> [!IMPORTANT]
> Planlægningssystemet kan være så præcist som inputdata. Hvis inputdataene er unøjagtige, vil negative poster i den disponible beholdning angive, at lageroplysningerne i Microsoft Dynamics 365 Supply Chain Management ikke er synkroniseret med den virkelige verden. Derfor vil planlægningsresultatet være fejlbehæftet. Hvis du vil have et præcist planlægningsresultat, skal du minimere antallet af poster, der viser et negativt antal.

## <a name="example-1"></a>Eksempel 1

Lagersted 13 er konfigureret på følgende måde:

- **Dækningskode:** Min./Maks.
- **Minimum:** 15 stk.
- **Maksimum:** 25 stk.

Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:

- **Sted 1, lagersted 13, sted 1** : 20 stk.
- **Sted 1 lagersted 13, sted 2:** &minus;8 stk.

Den samlede disponible beholdning for lagersted 13 er derfor 12 stk. (= 20 stk. &minus; 8 stk.).

I dette tilfælde bruger planlægningsprogrammet et samlet disponibelt antal på 12 stk. til lagersted 13.

Resultatet er en planlagt ordre på 13 stk. (= 25 stk. &minus; 12 stk.) til påfyldning af lagersted 13 fra 12 stk. til 25 stk.

## <a name="example-2"></a>Eksempel 2

Lagersted 13 er konfigureret på følgende måde:

- **Dækningskode:** Min./Maks.
- **Minimum:** 15 stk.
- **Maksimum:** 25 stk.

Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:

- **Sted 1, lagersted 13, sted 1** : 4 stk.
- **Sted 1 lagersted 13, sted 2:** &minus;8 stk.

Den samlede disponible beholdning for lagersted 13 er derfor &minus;4 stk. (= 4 stk. &minus; 8 stk.). Den er med andre ord mindre end 0 (nul).

I dette tilfælde antager planlægningsprogrammet, at den disponible beholdning for lagersted 13 er 0 stk. I stedet for &minus;4 stk.

Resultatet er en planlagt ordre på 25 stk. (= 25 stk. &minus; 0 stk.) til påfyldning af lagersted 13 fra 0 stk. til 25 stk.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Kom i gang med planlægningsoptimering](get-started.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
