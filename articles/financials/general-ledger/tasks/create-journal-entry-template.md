--- 
title: "Oprette en kladdepostering ved hjælp af en skabelon"
description: "Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-journal-entry-using-template"></a>Oprette en kladdepostering ved hjælp af en skabelon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag. Denne procedure bruger demofirmaet USMF.

1. Finans > Kladdeposteringer > Finanskladder. Klik på Ny.
    * Denne procedure starter med at oprette og bogføre et kladdebilag, men alle tidligere bogførte kladdebilag kan gemmes som en skabelon.  
2. Klik på rullelisten i feltet Navn for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på Linjer.
6. Angiv en konto for kontotypen.
7. Skriv en værdi i feltet Beskrivelse.
8. Indtast et beløb i feltet Debet.
9. Klik på Ny.
10. Angiv en anden konto for kontotypen.
11. Skriv en værdi i feltet Beskrivelse.
12. Indtast et beløb i feltet Debet.
13. Klik på Ny.
14. I feltet Konto skal du specificere de ønskede værdier.
15. Indtast en værdi i feltet Beskrivelse.
16. Angiv et beløb i feltet Kredit for at afstemme bilaget.
17. Klik på Bogfør.
18. Klik på Funktioner.
19. Klik på Gem bilagsskabelon.
20. Denne procedure forudsætter en procentskabelontype. Klik på OK.
    * • Procent: Beløbene i bilaget konverteres til procentfaktorer, som betyder, at alle beløb kan anvendes, når skabelonen Bilag er valgt.  • Beløb: De faktiske beløb gemmes og anvendes.  
21. Klik på Finanskladder.
22. Klik på Ny.
23. Klik på rullelisten i feltet Navn for at åbne opslaget.
24. Klik op linket i den valgte række på listen.
25. Klik på Linjer.
26. Klik på Funktioner.
27. Klik på Vælg bilagsskabelon.
28. Find den skabelon, du oprettede tidligere. Klik på OK.
    * Du skal muligvis klikke på trinnet Forrige og derefter vælge den rigtige skabelon, hvis der findes en anden skabelon.  
29. Angiv beløbet, der skal anvendes til bilaget, i feltet Beløb.
    * Beløbsfeltet vises kun, hvis bilagsskabelon er af typen Procent.  
30. Klik på OK.


