---
title: Analyse af om Planlægningsoptimering passer til
description: Dette emne beskriver, hvordan du kan kontrollere den aktuelle opsætning og de nuværende data i forhold til funktionerne i funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208748"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse af om Planlægningsoptimering passer til

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Hvis du vil se, hvordan din aktuelle opsætning og data er kompatibel med funktionen Planlægningsoptimering, skal du gå til **Varedisponering** \> **Opsætning** \> **Analyse af om Planlægninsoptimering passer til** og dernæst vælge **Kør analyse**. Hvis analysen finder nogen uoverensstemmelser, vises de på samme side. (Det kan tage et par minutter at køre analysen).

> [!NOTE]
> Hvis der findes uoverensstemmelser, kan du stadig bruge Planlægningsoptimering. Resultaterne af tilpasningsanalysen viser kun de steder, hvor planlægningstjenesten ikke kan overholde din aktuelle opsætning. Det vil sige, at det vises de steder, hvor nogle processer muligvis bliver ignoreret eller ikke understøttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funktion:** Produktion
- **Afgang:** Varer med styklisteniveau, der er større end nul: 56
- **Forklaring:** Tilpasningsanalysen fandt 56 varer, der indeholder en styklisteopsætning til produktion. Da den aktuelle version af funktionen Planlægningsoptimering ikke understøtter produktion, vil Planlægningsoptimering oprette indkøbsordreforslag i stedet for produktionsordreforslag. Der vises også en advarsel om, at de berørte varer vises.

### <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funktion:** Handlinger
- **Afgang:** Disponeringsgrupper med aktiveret handlingsberegning: 6
- **Forklaring:** Tilpasningsanalysen fandt seks disponeringsgrupper, hvor handlingsberegningen er aktiveret. Da den aktuelle version af Planlægningsoptimerings ikke understøtter handlinger, vil der ikke blive genereret handlinger ved varedisponering.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Oversigt over Planlægningsoptimering](planning-optimization-overview.md)

[Introduktion til Planlægningsoptimering](get-started.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
