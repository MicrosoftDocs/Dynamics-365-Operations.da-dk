--- 
title: " Basispris- og samhandelsaftaler"
description: "Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler."
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 81c70921718e41719470c7428c05a9f7ae77354a
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="base-price-and-trade-agreements"></a> Basispris- og samhandelsaftaler

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Detail og handel > Priser og rabatter > Prisgrupper > Alle prisgrupper.
    * Prisgrupper er den måde samhandelsaftaler er tildelt til bestemte kanaler. Hvis du bruger prisgrupper til at tildele samhandelsaftaler til en kanal, er det muligt at have kanalspecifikke priser.  
2. Klik på Ny.
3. Indtast en værdi i feltet Prisgrupper.
4. Skriv en værdi i feltet Navn.
5. Klik på Gem.
6. Luk siden.
7. Gå til Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker.
8. Vælg "New York" på listen
9. Klik på Butik i handlingsruden.
10. Klik på Prisgrupper.
11. Klik på Ny.
12. Klik på rullelisten i feltet Prisgrupper for at åbne opslaget.
13. Find og vælg den ønskede post på listen.
14. Klik på Gem.
15. Luk siden.
16. Luk siden.
17. Gå til Detail og handel > Produkter og kategorier > Frigivne produkter efter kategori.
18. Klik op linket i den valgte række på listen.
19. Klik på Rediger.
20. Slå udvidelsen af sektionen Sælg til/fra.
21. Angiv et tal i feltet Pris.
    * Denne pris bruges, hvis der findes nogen relevante samhandelsaftaler.  
22. Klik på Gem.
23. Klik på Sælg i handlingsruden.
24. Klik på Opret handelsaftaler?
25. Klik på Ny.
26. Klik på rullelisten i feltet Navn for at åbne opslaget.
27. Vælg "Detail" på listen.
    * I demodataene har kladdenavnet "Detail" standardrelationen "Pris (salg)". Det betyder, at alle nye linjer, der oprettes, som standard vil være salgsprissamhandelsaftaler.  
28. Klik på Linjer.
29. Vælg "Gruppe" i feltet Kontokode.
30. Klik på rullelisten i feltet Kontovalg for at åbne opslaget.
31. Find og vælg den ønskede post på listen.
    * Dette fuldfører linket fra Kanal til Prisgruppe til Samhandelsaftale.  
32. Indtast en værdi i feltet Varerelation.
33. Indtast et tal i feltet Beløb i valuta.
34. Markér eller fjern markeringen af afkrydsningsfeltet Find næste.
    * Når Find næste er angivet til "Ja", fortsætter prisprogrammet med at søge efter relevante samhandelsaftaler med en lavere salgspris. Når Find næste er indstillet til "Nej", stopper prisprogrammet søgningen og bruger samhandelsaftalen.  
35. Klik på Bogfør.
36. Klik på OK.
37. Luk siden.
38. Klik på Sælg i handlingsruden.
39. Klik på Salgspris.


