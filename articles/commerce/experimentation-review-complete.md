---
title: Hæve en variation og fuldføre et eksperiment
description: Denne artikel beskriver, hvordan du kan hæve en vellykket variation og fuldføre et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942731"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Hæve en variation og fuldføre et eksperiment

Denne artikel beskriver, hvordan du kan hæve den variation, der giver de bedste resultater i dit eksperiment, og hvordan du fuldfører eksperimentet. I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate artikler.

[ ![Eksperimenteringens brugerrejse - vurdere og fuldføre.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Når du har [kørt dit eksperiment](experimentation-run-monitor.md) og har indsamlet tilstrækkelige data til at finde ud af, hvilken variation du vil bruge på dit live websted, skal du hæve variationen og afslutte eksperimentet.

## <a name="promote-a-variation"></a>Hæve en variation
Brug de data og den analyse, der er knyttet til eksperimentet, i tredjepartstjenesten for at afgøre, hvilken variation der har givet de bedste resultater. Du kan derefter hæve den ved at erstatte det aktuelle indhold på det live websted med den vindende variation, så den er tilgængelig for alle brugere af dit websted.

Benyt følgende fremgangsmåde for at hæve den bedste variation: 

1. Vælg **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren, og vælg derefter eksperimentet.
1. Vælg **Fuldfør eksperiment** på kommandolinjen.
1. Vælg **Gennemse eksperimentdataene** i dialogmenuen **Fuldfør eksperimentet**. Tredjepartstjenesten åbner, hvor du kan validere målepunkterne og bestemme, hvilken variation der er udført bedst.
1. Vælg den bedste variation i dialogboksen **Fuldfør eksperimentet**, og vælg derefter **Næste**.
1. Åbn tredjepartstjenesten, og stop eksperimentet.
1. Vælg **Fuldfør** i webstedsgeneratoren for at overskrive den oprindelige aktive side og publicere den vindende variation, så den er tilgængelig for alle brugere på dit websted. 

> [!NOTE]
> Hvis du vælger at beholde den aktuelle live side og ikke vil publicere en variation, skal du vælge **Publicer den oprindelige side igen**.

## <a name="delete-your-experiment"></a>Slette dit eksperiment
Selvom det ikke er påkrævet, at du sletter et fuldført arbejdsområde i Commerce, kan du vælge at slette det for at spare plads eller rydde op i arbejdsområdet. 

Udfør følgende trin for at slette et fuldført eksperiment i Commerce-webstedsgenerator.

1. Vælg **Eksperimenter** i venstre navigationsrude, og vælg derefter eksperimentet. 
    > [!NOTE]
    > Hvis eksperimentet stadig er aktivt, skal du stoppe eksperimentet på tredjepartstjenesten, inden du fortsætter.
1. Vælg **Annuller publicering** på kommandolinjen for at fjerne variationsindholdet fra det live websted.
1. Vælg **Slet** for at slette eksperimentet.

## <a name="previous-step"></a>Forrige trin
[Køre og overvåge et eksperiment](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
