---
title: Fejlfinde planlægningsoptimering
description: Denne artikel beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med planlægningsoptimering.
author: t-benebo
ms.date: 05/07/2020
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
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739723"
---
# <a name="troubleshoot-planning-optimization"></a>Fejlfinde planlægningsoptimering 

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med planlægningsoptimering.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Installationen af tilføjelsesprogrammet Planlægningsoptimering blev ikke fuldført

Planlægningsoptimering er et LCS (Lifecycle Services) med høj tilgængelighed på niveau 2 eller højere (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere. Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke.

**Rettelse** : Annuller installationen, og brug et miljø med høj tilgængelighed, niveau 2 eller højere (ikke et Onebox-miljø).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Planlægning af batchjob mislykkes, når planlægningsoptimering er aktiveret.

Når du aktiverer Planlægningsoptimering, deaktiveres det udfasede varedisponeringsprogram automatisk. Varedisponeringsbatchjob, der blev oprettet til det udfasede varedisponeringsprogram, mislykkes, hvis de udløses, når Planlægningsoptimering er aktiveret. Der vises muligvis en fejlmeddelelse, f.eks. *Denne handling har udløst varedisponering, der ikke understøttes, når Planlægningsoptimering er aktiveret*.

**Rettelse** : Annuller alle varedisponeringsbatchjob, der blev oprettet for det udfasede varedisponeringsprogram.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Resultater fra Planlægningsoptimering adskiller sig fra tidligere resultater.

Planlægningsoptimering adskiller sig fra det udfasede varedisponeringsprogram på visse områder. Dette kan også skyldes ventende funktioner.

**Rettelse**: Kør analyse af tilpasning af planlægningsoptimering, og analysér derefter resultaterne, mens der henvises til den relaterede dokumentation for at forstå virkningen. Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Kan ikke aktivere Planlægningsoptimering

**Forbindelsesstatussen** skal være **tilsluttet**, før du kan angive **Brug planlægningsoptimering** til **Ja**. Du kan finde flere oplysninger under [Kom i gang med Planlægningsoptimering](get-started.md).

**Rettelse** : Kontroller, at tilføjelsesprogrammet Planlægningsoptimering blev installeret korrekt.

## <a name="error-message-is-shown-during-ctp"></a>Der vises en fejlmeddelelse under CTP

Hvis du prøver at køre ledningsevne (LE) fra en salgsordre, når Planlægningsoptimering er aktiveret, får du vist følgende fejlmeddelelse: *Denne handling har udløst varedisponering, der ikke understøttes, når Planlægningsoptimering er aktiveret*.

Dette er knyttet til en ventende funktion, der er planlagt som en del af understøttelsen af produktionsordrer.

**Rettelse:** Undgå LE-beregninger, når Planlægningsoptimering er aktiveret, indtil der er en tilgængelig LE-understøttelse.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Start her med varedisponering](get-started.md)
- [Analyse af tilpasning af planlægningsoptimering](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]