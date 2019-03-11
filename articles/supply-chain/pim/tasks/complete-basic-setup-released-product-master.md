---
title: Fuldføre grundlæggende konfiguration af en frigivet produktmaster
description: Denne fremgangsmåde viser, hvordan du fuldfører opsætningen, der som minimum kræves, før produktmasteren kan bruges i styklisteversioner.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "354776"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Fuldføre grundlæggende konfiguration af en frigivet produktmaster

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

