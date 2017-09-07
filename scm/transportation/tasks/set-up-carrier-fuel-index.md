--- 
title: "Konfigurere et brændstofindeks for fragtmand"
description: "Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: e9491e027a9a7806d5a10c8e0c3505c05f216a91
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>Konfigurere et brændstofindeks for fragtmand

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du opretter et område for brændstofindeks, et brændstofindeks og fragtmandens brændstofindeks. Området for brændstofindeks angiver hvilket område brændstofindekset skal gælde for, og brændstofindekset angiver en brændstofpris for en bestemt tidsperiode. For at afspejle ændringer i brændstofpriser over tid kan du knytte flere brændstofindekser til en fragtmand.  Disse opgaver udføres normalt af en transportkoordinator. Du kan bruge denne procedure i USMF-demodatafirmaet eller ved at bruge dine egne data.


## <a name="create-a-fuel-index-region"></a>Opret et område for brændstofindeks
1. Gå til Transportstyring > Opsætning > Brændstofindekser > Områder for brændstofindeks.
    * Først er det nødvendigt at oprette forskellige områder, hvor du bruger og beregner forskellige brændstoftillæg.  
2. Klik på Ny.
3. Skriv en værdi i feltet Område.
4. Skriv en værdi i feltet Navn.
5. Klik på Gem.

## <a name="create-a-fuel-index"></a>Oprette et brændstofindeks
1. Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindekser.
    * Du skal angive de aktuelle priser for brændstof for de områder, du har oprettet.  
2. Klik på Ny.
3. Klik på rullelisten i feltet Område for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Angiv et tal i feltet Pris pr. gallon.
6. Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.
7. Klik på Gem.

## <a name="create-a-carrier-fuel-index"></a>Opret et Brændstofindeks for fragt
1. Gå til Transportstyring > Opsætning > Brændstofindekser > Brændstofindeks for fragt.
2. Klik på Ny.
3. Indtast en værdi i feltet Brændstofindeks for fragt.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på Ny.
6. Angiv en dato og et klokkeslæt i feltet Gældende startdato og -klokkeslæt.
7. Angiv et tal i feltet PGG fra.
    * I dette eksempel kan du angive feltet PPG fra til 1.95.  
8. Angiv et tal i feltet PGG til.
    * I dette eksempel kan du angive feltet PPG til til 2.  
9. Angiv et tal i feltet Procent.
    * I dette eksempel kan du angive procenten til 3.  
10. Klik på rullelisten i feltet Valuta for at åbne opslaget.
11. Find og vælg den ønskede post på listen.
12. Klik op linket i den valgte række på listen.
13. Klik på Gem.

