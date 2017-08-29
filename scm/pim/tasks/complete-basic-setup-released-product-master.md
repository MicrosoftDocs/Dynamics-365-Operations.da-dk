--- 
title: "Fuldføre grundlæggende konfiguration af en frigivet produktmaster"
description: "Denne fremgangsmåde viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 1c7c499b3df92fee5010c731e331e711ea0d1883
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Fuldføre grundlæggende konfiguration af en frigivet produktmaster

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.

Dette er den tredje procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Find og vælg den ønskede post på listen.
    * Vælg produktmasteren, der er frigivet i den anden procedure. Denne produktmaster er oprettet med teknologien Dimensionsbaseret konfiguration.  
3. Klik på Produkt i handlingsruden.
4. Klik på Dimensionsgrupper for at åbne dialogboksen.
5. Klik på rullelisten i feltet Lagringsdimensionsgruppe for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
    * Lagringsdimensionsgruppen bestemmer, hvilke lagringsdimensioner, der bruges til transaktion af produktet. Vælg Sted til denne procedure.  
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Sporingsdimensionsgruppe for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
    * Sporingsdimensionsgruppen bestemmer, hvilke sporingsdimensioner der bruges til transaktion af produktet. Vælg Ingen til denne procedure.  
10. Klik op linket i den valgte række på listen.
11. Klik på OK.
12. Klik op linket i den valgte række på listen.
13. Klik på Rediger.
    * Åbn formularen Frigivne produktdetaljer for at fortsætte opsætningsopgaven.  
14. Klik på rullelisten i feltet Varemodelgruppe for at åbne opslaget.
15. Find og vælg den ønskede post på listen.
    * Varemodelgrupper indeholder indstillinger, der bestemmer, hvordan varerne kontrolleres og håndteres i forbindelse med indgående varer og vareafgange. De bestemmer også, hvordan der beregnes vareforbrug. Vælg FIFO til denne procedure.  
16. Klik op linket i den valgte række på listen.
17. Vis eller skjul sektionen Administrer omkostninger.
18. Klik på rullelisten i feltet Varegruppe for at åbne opslaget.
19. Find og vælg den ønskede post på listen.
    * Varegrupper anvendes til at styre lagerbeholdningen ved at opdele lagervarer i grupper. Vælg CarAudio til denne procedure.  
20. Klik op linket i den valgte række på listen.
21. Klik på Plan i handlingsruden.
22. Klik på Standardindstillinger for ordre.
23. Vælg en indstilling i feltet Standardordretype.
    * Vælg Produktion for at angive, at standardindstillingen for denne produktmaster er at producere den.  
24. Luk siden.
25. Luk formularen Frigivne produktdetaljer.


