---
title: Køre og overvåge et eksperiment
description: Denne artikel beskriver, hvordan du kører og overvåger et eksperiment i en tredjepartstjeneste. Det beskrives også, hvordan du foretager ændringer i variationer, efter at du har startet eksperimentet.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909577"
---
# <a name="run-and-monitor-an-experiment"></a>Køre og overvåge et eksperiment

Denne artikel beskriver, hvordan du kører og overvåger dit eksperiment i en tredjepartsapp og eventuelt ændrer variationer. Før du udfører trinnene i denne artikel, skal du først [publicere](experimentation-preview-publish.md) dit eksperimenter i Commerce. 

I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate artikler.

[ ![Eksperimenteringens brugerrejse - køre og overvåge.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Når du har publiceret dine variationer, skal du udføre alle de nødvendige trin i Commerce for at køre dit eksperiment. Det næste trin er afgørende for, hvilken variation der skal vises for hver enkelt bruger, når de anmoder om en side. Tredjepartstjenesten foretager denne beslutning, men først skal du aktivere eksperimentet i tjenesten. Da trinnene til aktivering af et eksperiment varierer fra tjeneste til tjeneste, skal du følge vejledningen til i din tjeneste eller fra udbyderen. Hvis eksperimentet ikke er aktiveret, kan brugere kun se standardversionen af siden (der vises ingen variationer).

Du skal holde eksperimentet kørende længe nok til at indsamle data til gyldige statistiske resultater. Brug tredjepartstjenesten til at overvåge de eksperimentrelaterede data og analyser, mens eksperimentet kører.

## <a name="adjust-your-variations"></a>Justere variationerne
Hvis du af en eller anden grund har brug for at ændre dine variationer, skal du følge trinnene nedenfor.

> [!IMPORTANT]
> Hvis du foretager ændringer i et aktivt eksperiment i Commerce eller tredjepartstjenesten, kan resultaterne blive betydeligt påvirket. Du bør overveje at lade eksperimentet køre færdigt og derefter oprette et nyt eksperimenter med større ændringer.

1. Vælg **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren, og vælg derefter eksperimentet. 
1. Vælg den variation, du vil opdatere, i rullemenuen.
1. Foretag de nødvendige ændringer, og gennemse og publicer variationerne. Du kan finde flere oplysninger i [Gennemse og publicere et eksperiment](experimentation-preview-publish.md).
1. Gå til tredjepartstjenesten for at foretage eventuelle ændringer af eksperimentets opsætning.
    
## <a name="previous-step"></a>Forrige trin
[Gennemse og publicere et eksperiment](experimentation-preview-publish.md)

## <a name="next-step"></a>Næste trin
[Hæve en variation og fuldføre et eksperiment](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]