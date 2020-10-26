---
title: Konfigurere et eksperiment
description: Dette emne beskriver, hvordan du konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930164"
---
# <a name="set-up-an-experiment"></a>Konfigurere et eksperiment

Når du [definerer en hypotese og bestemmer, hvilke succesmålepunkter du vil bruge](experimentation-identify.md), skal du konfigurere dit eksperiment i tredjepartstjenesten. I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate emner.

[ ![Eksperimenteringens brugerrejse - konfiguration](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Konfigurere dit eksperiment i tredjepartstjenesten
Nu skulle du have valgt en tredjepartstjeneste til at køre og overvåge dit eksperiment, så du kan konfigurere eksperimenteren-connectoren. Disse forudsætninger er angivet i [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md).

Følg de trin, der er nødvendige for at oprette dit eksperiment i tredjepartstjenesten. Hvis connectoren er konfigureret korrekt, vil den fuldstændige liste over de eksperimenter, du konfigurerer i tredjepartstjenesten, blive synlig i webstedsgeneratoren inden for 5 minutter.

## <a name="set-up-your-success-metrics"></a>Konfigurere succesmålepunkter
Alle eksperimenter skal bruge målepunkter til måling af variationernes effekt og for at validere hypotesen. Benyt følgende fremgangsmåde for at aktivere beregning af målepunkter i tredjepartstjenesten ved hjælp af hændelser med live telemetri fra Dynamics 365 Commerce.

1. I webstedsgeneratoren skal du vælge fanen **Sider** i venstre navigationsrude og derefter vælge den side, du vil indsamle målepunkter på. 
1. Gå til sektionen **Hændelses-id'er, der skal spores** i egenskabsruden til højre for den side eller det modul, du vil spore.
1. Vælg **Vis**. Der vises en liste over alle hændelses-id'er. Kopiér den hændelse, du vil spore, og Indsæt hændelsesnøglen på den angivne placering i tredjepartstjenesten. Hvis du skal bruge mere end én hændelse, skal du kopiere nøglerne én ad gangen. 
    - Du kan få mere at vide om, hvordan du kan få vist alle tilgængelige hændelser og attributter, herunder sidevisninger og sporing af omsætning, under [Commerce-komponenthændelser for diagnosticering og fejlfinding](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Udfør andre trin for at spore de påkrævede målepunkter i tredjepartstjenesten.

## <a name="previous-step"></a>Forrige trin
[Identificere en hypotese og fastslå målepunkter for et eksperiment](experimentation-identify.md) 


## <a name="next-step"></a>Næste trin
[Tilslutte og redigere et eksperiment](experimentation-connect-edit.md)
