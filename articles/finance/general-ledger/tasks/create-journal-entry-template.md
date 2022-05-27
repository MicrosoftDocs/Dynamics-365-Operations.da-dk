---
title: Oprette en kladdepostering ved hjælp af en skabelon
description: Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05cb878b570c45a2f7358ad60e6e01c7af17dc90
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716475"
---
# <a name="create-a-journal-entry-using-template"></a>Oprette en kladdepostering ved hjælp af en skabelon

[!include [banner](../../includes/banner.md)]

Bogførte kladdebilag kan gemmes som bilagsskabeloner og anvendes i et nyt kladdebilag. Denne procedure bruger demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.
2. Klik på **Ny** i **handlingsruden**. Denne procedure starter med at oprette og bogføre et kladdebilag, men alle tidligere bogførte kladdebilag kan gemmes som en skabelon.  
3. Klik på rullelisten i feltet **Navn** for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på **Linjer**.
7. Skriv en værdi i feltet **Kontotype**.
8. Indtast en værdi i feltet **Beskrivelse**.
9. Skriv en værdi i feltet **Debet**.
10. Klik på **Ny**.
11. Skriv en værdi i feltet **Kontotype**.
12. Indtast en værdi i feltet **Beskrivelse**.
13. Skriv en værdi i feltet **Debet**.
14. Klik på **Ny**.
14. I feltet **Konto** skal du angive de ønskede værdier.
15. Indtast en værdi i feltet **Beskrivelse**.
16. Angiv en værdi i feltet **Kredit** for at afstemme bilaget.
17. Klik på **Bogfør** i **handlingsruden**.
18. Klik på **Funktioner**.
19. Klik på **Gem bilagsskabelon**.
20. Denne procedure forudsætter en **Procentskabelon**-type. Klik på OK.
    - Procent: Beløbene i bilaget konverteres til procentfaktorer, som betyder, at alle beløb kan anvendes, når skabelonen Bilag er valgt.
    - Beløb: De faktiske beløb gemmes og anvendes.  
21. Klik på **Finanskladder**.
22. Klik på **Ny**.
23. Klik på rullelisten i feltet **Navn** for at åbne opslaget.
24. Klik op linket i den valgte række på listen.
25. Klik på **Linjer**.
26. Klik på **Funktioner**.
27. Klik på **Vælg bilagsskabelon**.
28. Find den skabelon, du oprettede tidligere. Klik på **OK**. Du skal muligvis klikke på **Forrige trin** og derefter vælge den rigtige skabelon, hvis der findes en anden skabelon.  
29. Angiv beløbet, der skal anvendes til bilaget, i feltet **Beløb**. Feltet **Beløb** vises kun, hvis bilagsskabelon er af typen Procent.  
30. Klik på **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
