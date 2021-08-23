---
title: " Basispris- og samhandelsaftaler"
description: Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler.
author: josaw1
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 282cbe0cb115d6204137613f4754068b8a9a321400d24808eb67266a83d7bcc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730725"
---
# <a name="base-price-and-trade-agreements"></a> Basispris- og samhandelsaftaler

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler. Proceduren bruger USRT-demodatafirmaet.

1. Gå til **Moduler > Retail og Commerce > Styring af prissætning og rabatter > Prisgrupper > Alle prisgrupper** i **Navigationsrude**. Prisgrupper er den måde samhandelsaftaler er tildelt til bestemte kanaler. Hvis du bruger prisgrupper til at tildele samhandelsaftaler til en kanal, er det muligt at have kanalspecifikke priser.  
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Prisgrupper**.
4. Skriv en værdi i feltet **Navn**.
5. Klik på **Gem**.
6. Luk siden.
7. Gå til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker** i **Navigationsrude**.
8. Vælg "New York" på listen
9. Klik på **Butik** i handlingsruden.
10. Klik på **Prisgrupper**.
11. Klik på **Ny**.
12. Klik på rullelisten i feltet **Prisgrupper** for at åbne opslaget.
13. Find og vælg den ønskede post på listen.
14. Klik på **Gem**.
15. Luk siden.
16. Luk siden.
17. Gå til **Moduler > Retail og Commerce > Produkter og kategorier > Frigivne produkter efter kategori** i **Navigationsrude**.
18. Klik op linket i den valgte række på listen.
19. Klik på **Rediger**.
20. Udvid oversigtspanelet **Sælg**.
21. Angiv et tal i feltet **Pris**. Denne pris bruges, hvis der findes nogen relevante samhandelsaftaler.  
22. Klik på **Gem**.
23. Klik på **Sælg** i **handlingsruden**.
24. Klik på **Opret handelsaftaler**.
25. Klik på **Ny**.
26. Klik på rullelisten i feltet **Navn** for at åbne opslaget.
27. Markér **Commerce** på listen. I demodataene har kladdenavnet **Commerce** standardrelationen **Pris (salg)**. Det betyder, at alle nye linjer, der oprettes, som standard vil være salgsprissamhandelsaftaler.  
28. Klik på **Linjer** i **Handlingsrude**.
29. Vælg 'Gruppe' i feltet **Type af partkode**.
30. Klik på rullelisten i feltet **Kontovalg** for at åbne opslaget.
31. Find og vælg den ønskede post på listen. Dette fuldfører linket fra Kanal til Prisgruppe til Samhandelsaftale.  
32. Indtast en værdi i feltet **Varerelation**.
33. Indtast et tal i feltet **Beløb i valuta**.
34. Markér evt. afkrydsningsfeltet **Find næste** i oversigtspanelet **Detaljer**. Når **Find næste** er angivet til 'Ja', fortsætter prisprogrammet med at søge efter relevante samhandelsaftaler med en lavere salgspris. Når **Find næste** er indstillet til 'Nej', stopper prisprogrammet søgningen og bruger samhandelsaftalen.  
35. Klik på **Bogfør**.
36. Klik på **OK**.
37. Luk siden.
38. Klik på Sælg i **handlingsruden**.
39. Klik på **Salgspris**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]