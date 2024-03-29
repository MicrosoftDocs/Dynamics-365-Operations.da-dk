---
title: Oprette og tildele politik for omkostningsfunktionalitet til en omkostningskontrolenhed
description: Omkostningsfunktionalitet er klassificeringen af omkostninger som enten faste eller variable.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735136"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Oprette og tildele politik for omkostningsfunktionalitet til en omkostningskontrolenhed

[!include [banner](../../includes/banner.md)]

Omkostningsfunktionalitet er klassificeringen af omkostninger som enten faste eller variable. En politik og de tilsvarende regler skal tildeles til en omkostningskontrolenhed, hvis politikken skal træde i kraft. Du kan bruge denne procedure til at oprette en politik og derefter tildele politikken til en omkostningskontrolenhed.


## <a name="create-a-cost-behavior-hierarchy"></a>Oprette et hierarki for omkostningsfunktionalitet
1. Gå til **Omkostningsregnskab > Dimensioner > Dimensionshierarkier**.
2. Klik på **Ny**.
3. Klik på **Opret**.
4. Skriv 'Hierarki for omkostningsfunktionalitet' i feltet **Navn på dimensionshierarki**.
5. Indtast eller vælg en værdi i feltet **Dimension**.
    * Vælg Omkostningselementer.  
6. Klik på **Gem**.
7. Klik på **Vis hierarki**.
8. Klik på **Ny**.
9. Angiv en værdi i feltet **Nodenavn**.
    * Skriv Fast omkostning.  
10. Vælg 'Hierarki for omkostningsfunktionalitet' i træet.
11. Klik på **Ny**.
12. Angiv en værdi i feltet **Nodenavn**.
    * Angiv Variabel omkostning.  
13. Klik på **Gem**.
14. Vælg 'Hierarki for omkostningsfunktionalitet\Fast omkostning' i træet.
15. Klik på **Ny**.
16. Markér den valgte række på listen.
17. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.  
18. Indtast eller vælg en værdi i feltet **Til dimensionsmedlem**.
    * Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.  
19. Vælg 'Hierarki for omkostningsfunktionalitet\Variabel omkostning' i træet.
20. Klik på **Ny**.
21. Markér den valgte række på listen.
22. Indtast eller vælg en værdi i feltet **Fra dimensionsmedlem**.
    * Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.  
23. Indtast eller vælg en værdi i feltet **Til dimensionsmedlem**.
    * Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.  
24. Klik på **Gem**.

## <a name="create-the-policy-and-rules"></a>Oprette politikken og reglerne
1. Gå til **Omkostningsregnskab > Politikker > Politikker for funktionalitet af omkostning**.
2. Klik på **Ny**.
3. Angiv en værdi i feltet **Navn på politik**.
4. Indtast eller vælg en værdi i feltet **Dimensionshierarki for omkostningselement**.
    * Vælg det politikhierarki, du netop har oprettet.  
5. Indtast eller vælg en værdi i feltet **Dimensionshierarki for omkostningsobjekt**.
    * Vælg organisation.  
6. Klik på **Gem**.
7. Klik på **Ny**.
8. Markér den valgte række på listen.
9. Indtast eller vælg en værdi i feltet **Dimensionshierarkinode for omkostningselement**.
    * Udvid hierarkiet ved at vælge Variabel omkostning.  
10. Indtast eller vælg en værdi i feltet **Dimensionshierarkinode for omkostningsobjekt**.
    * Som standard er den variable procentdel 100 %.  
11. Klik på **Politiktildelinger for omkostningskontrolenhed**.
12. Klik på **Ny**.
13. Markér den valgte række på listen.
14. Indtast en dato i feltet **Gyldig fra regnskabsdato**.
    * Reglerne er datorelaterede, og en bruger eller systemet kan lade en regel udløbe, hvis der oprettes en nyere version.  
15. Indtast eller vælg en værdi i feltet **Omkostningskontrolenhed**.
16. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
