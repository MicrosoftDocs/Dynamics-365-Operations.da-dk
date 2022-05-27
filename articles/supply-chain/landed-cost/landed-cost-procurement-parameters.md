---
title: Indkøbs- og forsyningsparametre for Landingsomkostninger
description: Dette emne beskriver, hvordan de relevante indkøbs- og forsyningsparametre defineres, når du bruger modulet Landingsomkostninger.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6e0ceb84423d7adc9c37da1b0b35a486627c0ce3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690408"
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
