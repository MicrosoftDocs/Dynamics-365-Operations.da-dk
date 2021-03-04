---
title: Oprette en politik for omkostningstotaler
description: Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441697"
---
# <a name="create-a-cost-rollup-policy"></a>Oprette en politik for omkostningstotaler

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken. De demodata, der bruges til at oprette denne procedure, er USP2.


## <a name="create-a-policy"></a>Oprette en politik
1. Gå til Omkostningsregnskab > Politikker > Politik for omkostningstotaler.
2. Klik på Ny.
3. Angiv en værdi i feltet Navn på politik.
4. Skriv en værdi i feltet Beskrivelse.
5. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.
    * Vælg Omkostningstotaler CC.  
6. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.
    * Vælg Omkostningstotaler CC.  
7. Klik på Gem.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Oprette regler for politikken for omkostningstotaler
1. Klik på Ny.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Vælg 007.  
4. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.
    * Vælg Omkostningstotaler CE.  
5. Indtast eller vælg en værdi i feltet Sekundært omkostningselement.
    * I dette eksempel skal du knytte det sekundære omkostningselement CC-007 til bæreren.  
6. Klik på Ny.
7. Markér den valgte række på listen.
8. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Vælg 008.  
9. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.
    * Vælg Omkostningstotaler CE.  
10. Indtast eller vælg en værdi i feltet Sekundært omkostningselement.
    * I dette eksempel skal du knytte det sekundære omkostningselement CC-008 til bæreren.  
11. Klik på Ny.
12. Markér den valgte række på listen.
13. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
    * Vælg 009.  
14. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.
    * Vælg Omkostningstotaler CE.  
15. Indtast eller vælg en værdi i feltet Sekundært omkostningselement.
    * I dette eksempel skal du knytte det sekundære omkostningselement CC-009 til bæreren.  
    * Fortsæt, indtil alle bærere er knyttet til de tilsvarende sekundære omkostningselementer.  
16. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]