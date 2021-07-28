---
title: Gennemgå status for et eksperiment
description: I dette emne forklares, hvad status et eksperiment har i livscyklussen for eksperimenteren i Dynamics 365 Commerce.
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
ms.openlocfilehash: bb9d0e96f8bbdb49408b232eb0405a22d6f478bb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349202"
---
# <a name="review-the-status-of-an-experiment"></a>Gennemgå status for et eksperiment
Der er mange trin involveret i opsætning og kørsel af et eksperiment i Dynamics 365 Commerce. Du kan finde flere oplysninger om livscyklussen for eksperimenteren under [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md).

Hvis du vil vide, hvor et eksperiment er i livscyklussen, skal du vælge **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren. Der vises en liste over eksperimenter med status for hvert eksperiment i både Commerce og den tredjepartstjeneste, der bruges til at aktivere oprettelse af eksperimenter, tildele variationer og analysere data.

I kolonnen **Commerce-status** kan følgende værdier vises. 
- **Kladde** - Eksperimentet er knyttet til en side eller et fragment i Commerce og er ved at blive redigeret.
- **Publiceret** - Eksperimentvariationerne er klar til at blive vist på dit websted. Hvis eksperimentet kører i tredjepartstjenesten, vil brugere af webstedet se en variant af siden eller fragmentet, der er valgt af tredjepartstjenesten.
- **Ikke-publiceret** - Eksperimentet er ikke længere tilgængeligt på dit websted. Hvis eksperimentet kører i tredjepartstjenesten, vil brugere af webstedet kun se standardversionen af siden eller fragmentet.
- **Fuldført** - Eksperimentet er færdigafviklet, og en variation blev hævet til live for alle brugere af webstedet.

På samme måde kan følgende værdier vises i kolonnen **tredjepartsstatus** for at angive, hvilken status eksperimenter har i tredjepartstjenesten.
- **Kladde** - Eksperimentet er konfigureret i tredjepartstjenesten, men er ikke blevet startet.
- **Kører** - Eksperimentet blev startet i tredjepartstjenesten og indsamler data.
- **Afbrudt midlertidigt** - Eksperimentet er midlertidigt afbrudt og indsamler ikke data. Du skal fortsætte eksperimentet for at indsamle data igen.
- **Arkiveret** - Eksperimentet er færdigafviklet og er blevet katalogiseret i tredjepartstjenesten til fremtidig brug.

I nedenstående diagram vises begge sæt statusser, og hvordan de er relateret til hinanden.

[ ![Eksperimenterens statusser.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]