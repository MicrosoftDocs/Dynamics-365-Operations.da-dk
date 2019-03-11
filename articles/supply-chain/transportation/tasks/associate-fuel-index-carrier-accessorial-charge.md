---
title: Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr
description: Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae0aa90cfd673704bcd8e19f795499283ff01d44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "349785"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Tilknytte et brændstofindeks med en fragtmand som tillægsgebyr

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser, hvordan du opretter en tilbehørstildeling, tillægsgebyr for fragtmand, tillægsmaster for brændstoftillæg og knytter en fragtmands brændstofindeks til en fragtmand. Du skal have oprettet en fragtmands brændstofindeks, før du kører denne guide. Du kan bruge guiden "Konfigurer brændstofindeks for en fragtmand" for at gøre dette. Disse konfigurationsopgaver udføres typisk af en logistikchef. De demodata, der bruges til at oprette denne procedure, er USMF.


## <a name="create-an-accessorial-master"></a>Opret en tillægsmaster
1. Gå til Transportstyring > Opsætning > Klassificering > Tilbehørsmastere.
2. Klik på Ny.
3. Skriv en værdi i feltet Tilbehørsmaster.
4. Skriv en værdi i feltet Navn.
5. Klik på Gem.

## <a name="create-a-carrier-accessorial-charge"></a>Opret et tillægsgebyr for fragtmand
1. Gå til Transportstyring > Opsætning > Klassificering > Fragtmands tillægsgebyrer.
2. Klik på Ny.
3. Indtast en værdi i feltet Id for fragtmandstilbehør.
4. Klik på rullelisten i feltet Fragtmand for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
    * I dette eksempel skal du vælge lastbilsfragtmand.  
6. Klik op linket i den valgte række på listen.
7. Klik på rullelisten i feltet Fragttjeneste for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
9. Klik på rullelisten i feltet Tilbehørsmaster for at åbne opslaget.
10. Find og vælg den ønskede post på listen.
    * I dette eksempel skal du vælge den nyoprettede Tilbehørsmaster.  
11. Klik på Gem.

## <a name="create-an-accessorial-assignment"></a>Opret en tilbehørstildeling
1. Klik Tildelinger af tillæg.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Slå udvidelsen af Sektionen Kriterier til/fra.
    * I kriterierne kan du vælge altid at anvende brændstoftillægget, eller for dette eksempel vælge, at det kun gælder inden for en bestemt region.  
5. Skriv en værdi i feltet Postnummer fra.
6. Skriv en værdi i feltet Postnummer til.
7. Slå udvidelsen af sektionen Beregning til/fra.
    * I beregningssektionen kan du angive, hvordan brændstoftillægget beregnes. Denne beregning afhænger af den Tillægsenhed, som du har valgt som basis for beregningen.  
8. Vælg "Brændstoftillæg" i feltet Gebyrtype for tillæg.
9. Vælg en "Kilometertal" i feltet Tillægsenhed.
10. Klik på rullelisten i feltet Område for at åbne opslaget.
11. Klik op linket i den valgte række på listen.
12. Klik på Gem.

## <a name="update-the-carrier-rating-profile"></a>Opdater fragtmandens vurderingsprofil
1. Gå til Transportstyring > Opsætning > Fragtmænd > Fragtmænd.
2. Find og vælg den ønskede post på listen.
3. Slå udvidelsen af sektionen Vurderingsprofiler til/fra.
4. Klik på Rediger.
5. Klik på rullelisten i feltet Brændstofindeks for fragt for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
7. Klik på Gem.

