---
title: Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed
description: Regler for omkostningsfordeling bruges til at fordele omkostninger, der er optalt i økonomisk sammenhæng på en kollektiv bærer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976181"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed

[!include [banner](../../includes/banner.md)]

Regler for omkostningsfordeling bruges til at fordele omkostninger, der er optalt i økonomisk sammenhæng på en kollektiv bærer. Bogholderen sikrer, at omkostningerne fordeles til bærerne baseret på den valgte fordelingsbasis. En politik og de tilsvarende regler tildeles til en enhed til en omkostningskontrolenhed. Denne opgaveguide bruger et eksempel til at vise, hvordan du opretter en politik for fordeling af omkostninger og de tilsvarende regler.


## <a name="create-a-policy"></a>Oprette en politik
1. Gå til Omkostningsregnskab > Politikker > Politikker for omkostningsfordeling.
2. Klik på Ny.
3. Angiv en værdi i feltet Navn på politik.
4. Skriv en værdi i feltet Beskrivelse.
5. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.
    * Vælg organisation.  
6. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.
    * Vælg CDS P/L.  
7. Indtast eller vælg en værdi i feltet Statistisk dimension.
    * Vælg Statistiske elementer.  
8. Klik på Gem.

## <a name="create-rules-for-the-policy"></a>Oprette regler for politikken
1. Klik på Ny.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Udvid hierarkiet ved at vælge 094.  
4. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.
    * Vælge Andre driftsudgifter, og vælg derefter 605110 Rengøring.  
5. Vælg en indstilling i feltet Funktionalitet af omkostning.
    * Vælg Fast omkostning.  
6. Indtast eller vælg en værdi i feltet Fordelingsbasis.
7. Klik på Ny.
8. Markér den valgte række på listen.
9. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Udvid hierarkiet ved at vælge 094.  
10. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.
    * Vælge Andre driftsudgifter, og vælg derefter 605150 Leje.  
11. Vælg en indstilling i feltet Funktionalitet af omkostning.
    * Vælg Fast omkostning.  
12. Indtast eller vælg en værdi i feltet Fordelingsbasis.
13. Klik på Gem.

## <a name="assign-rules-to-a-cost-control-unit"></a>Tildele regler til en omkostningskontrolenhed
1. Klik på Politiktildelinger for omkostningskontrolenhed.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Indtast en dato i feltet Gyldig fra regnskabsdato.
    * Vælg den 1. september i det regnskabsår, der gælder.  
5. Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.
6. Klik på Gem.

