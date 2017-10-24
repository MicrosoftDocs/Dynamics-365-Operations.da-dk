--- 
title: "Oprette et indkøbskatalog"
description: "Denne vejledning viser, hvordan du opretter et indkøbskatalog."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Oprette et indkøbskatalog

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du opretter et indkøbskatalog. Denne opgave vil normalt udføres af en professionel indkøber. Du lærer også, hvordan medarbejdere kan bruge kataloget, når de opretter en indkøbsrekvisition. Før du kan oprette et katalog, skal der være et indkøbskategorihierarki i systemet. Hierarkiet arves af det nye katalog sammen med alle de produkter, der er i hierarkiet. Du kan bruge denne vejledning i demodatafirmaet USMF, hvor indkøbskategorihierarkiet er tilgængeligt, såvel som de eksempler, der bruges i trinnene i proceduren.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Kontroller, at der findes et indkøbskategorihierarki
1. Gå til Indkøb og forsyning > Indkøbskategorier.
    * Et indkøbskategorihierarki er tilgængeligt i USMF-demodatafirmaet, og produkter er føjet til kategorien Kontormaskiner/computere. Hvis du kører denne procedure som en opgaveguide, skal du låse opgaveguiden op, hvis du vil søge i kategorien. Hvis et hierarki ikke var tilgængeligt, skal du oprette det ved at klikke på Ny. Det kan du kun gøre én gang.  
2. Luk siden.

## <a name="create-a-catalog"></a>Oprette et katalog
1. Gå til Indkøb og forsyning > Kataloger > Indkøbskataloger.
2. Klik på Nyt indkøbskatalog for at åbne dialogboksen, hvor du kan slippe den.
3. Skriv en værdi i feltet Navn.
4. Klik på OK.
5. Udvid 'FIRMAS INDKØBSKATEGORIER' i træet.
6. Udvid 'KONTORMASKINER' i træet.
7. Vælg 'Computere' i træet.
    * Produkterne fra indkøbskategorien vises på listen. Hvis du vil føje et produkt til kategorien, skal du gøre det på siden Indkøbskategorihierarki eller på siden Vareoplysninger.  
    * Standardopdateringstypen bestemmer, om nye produkter, der er føjet til indkøbskategorihierarkiet, er synlige i kataloget med det samme. Hvis opdateringstypen er indstillet til Dynamisk, kan ændringer ses øjeblikkeligt. Hvis opdateringstypen er Statisk, er nye produkter kun synlige for brugere af kataloget, når kataloget er blevet udgivet igen. Publiceringshandling er tilgængelig i handlingsruden øverst på siden. Hvis produkter fjernes fra indkøbskategorihierarkiet, er ændringen straks synlig, uanset hvilken værdi der er i feltet Standardopdateringstype.  
8. Find og vælg den ønskede post på listen.
9. klik på Skjul.
10. Klik på Katalognavigation i handlingsruden.
11. Klik på Deaktiver.
12. Klik på Katalognavigation i handlingsruden.
13. Klik på Enable.
14. Klik på Aktivér katalog.
15. Luk siden.

## <a name="make-the-catalog-visible"></a>Gør kataloget synligt
1. Gå til Indkøb og forsyning > Konfiguration > Politikker > Indkøbspolitikker.
2. Vælg indkøbspolitikken USMF.
    * Du skal vælge indkøbspolitik, så den juridiske enhed, som arbejderen har knyttet til din brugerprofil, kan bestille produkter. I USMF-demodataene er administratorbrugeren knyttet til den arbejder, der hedder Julia Funderburk, og hun bestiller som standard produkter i USMF.  
3. Klik op linket i den valgte række på listen.
4. Vælg det katalog, du netop har oprettet.
5. Klik på OK.
6. Luk siden.
7. Luk siden.

## <a name="use-the-catalog"></a>Brug kataloget
1. Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Alle indkøbsrekvisitioner.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Klik på OK.
5. Klik på Tilføj produkter.
6. Find og vælg den ønskede post på listen.
    * Du kan bruge kategorihierarkiet til venstre eller filteret øverst på listen til at filtrere produkterne.  
7. Klik på Føj til linjer
8. Find og vælg den ønskede post på listen.
9. Klik på Føj til linjer
10. Klik på OK.


