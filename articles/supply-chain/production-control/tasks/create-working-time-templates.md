--- 
title: Oprette skabeloner til arbejdstid
description: Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-working-time-templates"></a>Oprette skabeloner til arbejdstid

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum. Denne procedure viser, hvordan du definerer en arbejdstidsskabelon ved hjælp af planlægningsegenskaber for arbejdstider til kategorisering af arbejdstidsintervaller. Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.

1. Gå til alle arbejdsområder > Styring af ressourcelivscyklus.
2. Klik på Arbejdstidsskabeloner.

## <a name="create-working-time-template"></a>Oprette arbejdstidsskabelon
1. Klik på Ny.
2. Indtast en værdi i feltet Arbejdstidsskabelon.
3. Skriv en værdi i feltet Navn.
4. Udvid afsnittet Mandag.
5. Klik på Tilføj.
6. Angiv et klokkeslæt i feltet Fra.
    * Angiv det tidspunkt, hvor arbejdet begynder om morgenen.  
7. Angiv et klokkeslæt i feltet Til.
    * Angiv det tidspunkt, hvor arbejdere har frokostpause.  
8. Klik på Tilføj.
9. Angiv et klokkeslæt i feltet Fra.
    * Angiv det tidspunkt, hvor arbejdet genoptages efter frokost.  
10. Angiv et klokkeslæt i feltet Til.
    * Angiv, hvornår arbejdsdagen er slut.  

## <a name="replicate-working-times-to-all-week-days"></a>Replikere arbejdstider til alle ugedage
1. Klik på Kopier dag.
    * Kopier arbejdstidsdefinitionerne fra mandag til tirsdag.  
2. Klik på OK.
3. Klik på Kopier dag.
    * Kopier arbejdstidsdefinitionerne fra mandag til onsdag.  
4. Vælg en indstilling i feltet Til ugedag.
5. Klik på OK.
6. Klik på Kopier dag.
    * Kopier arbejdstidsdefinitionerne fra mandag til torsdag.  
7. Vælg en indstilling i feltet Til ugedag.
8. Klik på OK.
9. Klik på Kopier dag.
    * Kopier arbejdstidsdefinitionerne fra mandag til fredag.  
10. Vælg en indstilling i feltet Til ugedag.
11. Klik på OK.

## <a name="define-time-slots-for-special-operations"></a>Definere tidsrubrikker for særlige operationer
1. Udvid afsnittet Fredag.
2. Find og vælg den ønskede post på listen.
3. Indtast eller vælg en værdi i feltet Egenskab.
4. Find og vælg den ønskede post på listen.
5. Indtast eller vælg en værdi i feltet Egenskab.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Markér dage i weekend som lukket for afhentning
1. Udvid afsnittet Lørdag.
2. Vælg Ja i feltet Lukket for afhentning.
3. Udvid afsnittet Søndag.
4. Vælg Ja i feltet Lukket for afhentning.


