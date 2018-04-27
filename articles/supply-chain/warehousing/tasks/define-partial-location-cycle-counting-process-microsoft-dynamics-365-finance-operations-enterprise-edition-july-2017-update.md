--- 
title: "Definere delvis cyklusoptællingsproces for lokalitet"
description: "Når du bruger cyklusoptællingsplaner til at oprette optællingsarbejde, kan du lede de faktiske optællingsoperationer ved at anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på lokationen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
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
ms.openlocfilehash: 030f0f75d64c97f1109f36c9fd38283c2d1fa7b0
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="define-partial-location-cycle-counting-process"></a>Definere delvis cyklusoptællingsproces for lokalitet 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Når du bruger cyklusoptællingsplaner til at oprette optællingsarbejde, kan du lede de faktiske optællingsoperationer ved at anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på lokationen. Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, hjælpe med at forhindre konsolideringsfejl og spare tid. En lagerchef udfører typisk opsætningsopgaver. Du kan gennemgå denne procedure i USMF-demodatafirmaet eller i dine egne data.


## <a name="create-a-cycle-counting-work-template"></a>Oprette en arbejdsskabelon til cyklusoptælling
1. Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.
2. Vælg Cyklusoptælling i feltet Arbejdsordretype.
3. Klik på Ny.
4. Indtast et tal i feltet Sekvensnummer.
    * Sorteringsrækkefølgen er fra det mindste tal til det største tal. Værdien skal være større end 0 (nul).  
5. Markér den valgte række på listen.
6. Indtast en værdi i feltet Arbejdsskabelon.
7. Skriv en værdi i feltet Beskrivelse af arbejdsskabelon.
8. Indtast eller vælg en værdi i feltet Arbejdspulje-id.
9. Angiv et tal i feltet Arbejdsprioritet.
10. Klik på Gem.
11. Klik på Ny.
12. Markér den valgte række på listen.
13. Vælg Optælling i feltet Arbejdstype.
14. Indtast eller vælg en værdi i feltet Arbejdsklasse-id.
15. Klik på Gem.
16. Klik på Arbejdslinjeskift.
17. Klik på Ny.
18. Indtast et tal i feltet Sekvensnummer.
    * Sorteringsrækkefølgen er fra det mindste tal til det største tal. Værdien skal være større end 0 (nul).  
19. Klik på Gem.
20. Luk siden.
21. Luk siden.

## <a name="create-a-cycle-counting-plan"></a>Oprette en cyklusoptællingsplan
1. Gå til Lagerstedsstyring > Opsætning > Cyklusoptælling > Cyklusoptællingsplaner.
2. Klik på Ny.
3. Skriv en værdi i feltet Id for cyklusoptællingsplan.
4. Indtast en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Maks. antal cyklusoptællinger.
6. Indtast eller vælg en værdi i feltet Arbejdsskabelon.
7. Klik på Ny.
8. Indtast et tal i feltet Sekvensnummer.
    * Sorteringsrækkefølgen er fra det mindste tal til det største tal. Værdien skal være større end 0 (nul).  
9. Skriv en værdi i feltet Beskrivelse.
10. Klik på Gem.
11. Klik på Definer produktforespørgsel.
12. Markér den valgte række på listen.
13. Indtast eller vælg en værdi i feltet Kriterier.
14. Klik på OK.
15. Luk siden.


