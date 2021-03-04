---
title: Gennemse og publicere et eksperiment
description: I dette emne beskrives, hvordan du gennemser og publicerer et eksperiment fra Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4411218"
---
# <a name="preview-and-publish-an-experiment"></a>Gennemse og publicere et eksperiment

Dette emne beskriver, hvordan du gennemser og publicerer dit eksperiment i Dynamics 365 Commerce, når du har [tilsluttet dit eksperiment og redigeret dine variationer](experimentation-connect-edit.md). I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate emner.

[ ![Eksperimenteringens brugerrejse - gennemse og publicere](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Gennemse dine eksperimentvariationer
Du kan gennemse dine variationer og fortsætte med at redigere dem, indtil de ser ud, som du vil have dem.

Benyt følgende fremgangsmåde for at afprøve dine eksperimentvariationer i Commerce-webstedsgenerator.

1. I rullemenuen med variationer under kommandoværktøjslinjen skal du vælge det indhold, du vil gennemse. 
1. Vælg **Forhåndsvisning** på kommandolinjen. Et eksempel på, hvordan indholdet vil se ud, når det publiceres, vises.
1. Hvis du vil se en anden variation, skal du vælge den på rullelisten Variation og vælge **Eksempel** igen.

## <a name="publish-your-experiment"></a>Publicere dit eksperiment
Hvis du ikke bruger en publiceringsgruppe til at planlægge, hvornår dit eksperiment går live, og du vil publicere det med det samme, skal du vælge **Publicer** på kommandolinjen. Alle de variationer, der hører til eksperimentet, vil blive publiceret.
    
> [!IMPORTANT]
> Hvis siden har en ikke-publiceret URL-adresse, skal du først publicere URL-adressen, ellers kan den ikke ses af brugerne på webstedet. Der er flere oplysninger i [Gemme, se og publicere en side](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Bruge publiceringsgrupper til at planlægge, hvornår dit eksperiment går live
Varianter, der er oprettet i webstedsgeneratoren, kan planlægges til publicering ved hjælp af en publiceringsgruppe. I en publiceringsgruppe kan du forbinde en side eller et fragment med dit eksperiment ved at vælge **Eksperimenter** i venstre navigationsrude. Du kan også gøre dette ved at vælge **Sider** eller **Fragmenter** og følge instruktionerne i [Tilslutte et eksperiment og redigere variationer](experimentation-connect-edit.md). Du kan finde oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).

Når du bruger publiceringsgrupper sammen med eksperimenter, er der nogle vigtige overvejelser, du skal være opmærksom på.
- Når du tilføjer en side eller et fragment, der har et eksperiment kørende, i en publiceringsgruppe, fjernes eksperimentet fra siden eller fragmentet i publiceringsgruppen.
- Eksperimenter, der er forbundet med sider på et live websted, er ikke tilgængelige for siderne i publiceringsgrupper og omvendt. På samme måde er sider, hvor eksperimenter kører på et live websted, ikke tilgængelige for andre eksperimenter i publiceringsgrupper og omvendt.
- Når du publicerer eller planlægger en publiceringsgruppe, publiceres alt indhold i publiceringsgruppen, uanset om der er et eksperiment knyttet til publiceringsgruppen.
- Da en publiceringsgruppe fortsat vil være aktiv, efter at den er publiceret til et live websted, vil eksperimenter i publiceringsgruppen også fortsætte. Derfor kan du ikke knytte andre eksperimenter til den samme side eller det samme fragment. Hvis du vil undgå denne begrænsning, skal du slette alle publiceringsgrupper med vedvarende eksperimenter. Hvis du ligeledes vil slette et eksperiment på et live websted, der også findes i en publiceringsgruppe, skal du først slette det fra publiceringsgruppen.

## <a name="previous-step"></a>Forrige trin
[Tilslutte og redigere et eksperiment](experimentation-connect-edit.md)

## <a name="next-step"></a>Næste trin
[Køre og overvåge et eksperiment](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]