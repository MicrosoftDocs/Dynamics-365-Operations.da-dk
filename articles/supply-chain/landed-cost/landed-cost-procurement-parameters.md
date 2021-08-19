---
title: Indkøbs- og forsyningsparametre for Landingsomkostninger
description: Dette emne beskriver, hvordan de relevante indkøbs- og forsyningsparametre defineres, når du bruger modulet Landingsomkostninger.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d8aa7e6ebd254289df410814a08a5d0fe31239dd103cb428f0d4bc401fbfb28a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747931"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Indkøbs- og forsyningsparametre for Landingsomkostninger

[!include [banner](../../includes/banner.md)]

Siden **Indkøbs- og forsyningsparametre** indeholder nogle få indstillinger, der især er relevante, når du bruger modulet **Landingsomkostninger**. Brug dialogboksen **Opdater ordrelinjer**, der åbnes fra siden **Indkøbs- og forsyningsparametre**, til at angive, om indkøbsordrelinjer skal opdateres automatisk, når der foretages ændringer i indkøbsordrehovedet.

Gør følgende for at fuldføre konfigurationen.

1. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.
1. Vælg linket **Opdater ordrelinjer** under fanen **Generelt**.
1. I dialogboksen **Opdater ordrelinjer** vises de felter i ordrehovedet, som også kan anvende automatiske opdateringer på de tilknyttede felter på ordrelinjerne. Indstil hvert felt på listen til en af følgende værdier:

    - **Altid** – Ordrelinjerne opdateres automatisk, når ordrehovedet opdateres.
    - **Aldrig** – Ordrelinjerne opdateres aldrig, når ordrehovedet opdateres.
    - **Prompt** – Brugeren bliver bedt om at vælge, om ordrelinjerne skal opdateres.
