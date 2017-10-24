--- 
title: Oprette og tildele omkostningstildelingspolitik til en omkostningskontrolenhed
description: Du kan bruge denne procedure til at oprette og tildele en politik for omkostningsfordeling og de tilsvarende regler til en omkostningskontrolenhed.
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Oprette og tildele omkostningstildelingspolitik til en omkostningskontrolenhed

[!include[task guide banner](../../includes/task-guide-banner.md)]

Du kan bruge denne procedure til at oprette og tildele en politik for omkostningsfordeling og de tilsvarende regler til en omkostningskontrolenhed. Denne registrering bruger USP2-demodatafirmaet.


## <a name="create-a-policy"></a>Oprette en politik
1. Gå til Omkostningsregnskab > Politikker > Politikker for omkostningstildeling.
2. Klik på Ny.
3. Angiv en værdi i feltet Navn på politik.
4. Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.
    * Vælg organisation.  
5. Indtast eller vælg en værdi i feltet Statistisk dimension.
6. Klik på Gem.

## <a name="create-allocation-rules"></a>Oprette fordelingsregler
1. Klik på Ny.
2. Markér den valgte række på listen.
3. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
4. Vælg 'Total' i feltet Funktionalitet af omkostning.
5. Indtast eller vælg en værdi i feltet Fordelingsbasis.
6. Klik på Ny.
7. Markér den valgte række på listen.
8. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
9. Vælg 'Total' i feltet Funktionalitet af omkostning.
10. Indtast eller vælg en værdi i feltet Fordelingsbasis.
11. Klik på Ny.
12. Markér den valgte række på listen.
13. Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.
14. Vælg 'Total' i feltet Funktionalitet af omkostning.
15. Indtast eller vælg en værdi i feltet Fordelingsbasis.
    * Fortsæt, indtil du har oprettet alle regler.  
16. Klik på Gem.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Tildele politikken til en omkostningskontrolenhed
1. Klik på Politiktildelinger for omkostningskontrolenhed.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Indtast en dato i feltet Gyldig fra regnskabsdato.
    * Reglerne er datorelaterede. En bruger eller systemet kan lade reglerne udløbe, hvis der oprettes en nyere version.  
5. Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.
6. Klik på Gem.


