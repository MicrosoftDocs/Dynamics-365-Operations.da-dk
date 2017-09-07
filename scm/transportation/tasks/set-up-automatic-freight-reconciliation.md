--- 
title: Konfigurere automatisk fragtafstemning
description: Denne procedure viser, hvordan du konfigurerer data til automatisk fragtafstemning.
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
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
ms.openlocfilehash: 61b795d52d4d2586db7f42a976790ee8608e179b
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Konfigurere automatisk fragtafstemning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du konfigurerer data til automatisk fragtafstemning. Det udføres typisk af en lagerchef. Du kan bruge denne procedure i USMF-demodatafirmaet.


## <a name="set-up-the-freight-bill-type"></a>Konfigurer fragtbrevstypen
1. Gå til Transportstyring > Konfiguration > Afstemning af fragt > Fragtbrevstype.
    * Typen af fragtbrev definerer, hvordan fragtbreve og fragtfakturaer skal sammenholdes.  
2. Klik på Ny.
3. Skriv en værdi i feltet Fragtbrevstype.
4. I programassembly'en skal du skrive 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.
    * Dette er kodebiblioteket for programmet til sammenligning af transportstyring.  
5. I programklassen skal du skrive 'Microsoft.Dynamics.Ax.Tms.dll'.
    * Dette er klassen for programmet til sammenligning af transportstyring.  
6. Klik på Ny.
7. Vælg den værdi, der skal svare til fragtbrevet og fragtfakturaen, i feltet Beskrivelse.  
8. Vælg 'Ja' i feltet Kræver afstemning.
    * Hvis du angiver feltet til Ja, betyder det, at værdien i feltet Beskrivelse skal svare til både fragtbrevet og fragtfakturaen. Hvis du angiver det til Nej, må feltet være tomt for en af disse.  
9. Klik på Gem.

## <a name="set-up-the-freight-bill-type-assignment"></a>Konfigurer tildelingen af fragtbrevstype
1. Luk siden.
2. Gå til Transportstyring > Konfiguration > Afstemning af fragt > Tildelinger af fragtbrevstype.
    * Tildelingen af typen af fragtbrev bruges til at angive, hvilken type fragtbrev der bruges til en bestemt fragtmand.   
3. Klik på Ny.
4. Indtast eller vælg en værdi i feltet Tilstand.
5. Indtast eller vælg en værdi i feltet Fragtmand.
6. Vælg typen fragtbrev, du oprettede tidligere, i feltet Fragtbrevstype.
7. Luk siden.

## <a name="set-up-the-audit-master"></a>Konfigurer overvågningsmasteren
1. Gå til Transportstyring > Konfiguration > Afstemning af fragt > Revisionsmaster.
    * I revisionsmasteren defineres tolerancegrænserne for automatisk fragtafstemning. Den angiver, hvor meget pengebeløbene i fragtbrevet og i fragtfakturaen kan variere og stadig tillade, at afstemningen finder sted. Den definerer også, hvordan du håndterer uoverensstemmelser.  
2. Klik på Ny.
3. Skriv en værdi i feltet Revisionsmaster.
4. Vælg samme fragtmand som tidligere i feltet Fragtmand.
5. Vælg typen fragtbrev, du oprettede tidligere, i feltet Fragtbrevstype.
6. Udvid afsnittet Tolerance.
7. Skriv et tal i feltet Min. toleranceniveau.
8. Skriv et tal i feltet Maks. toleranceniveau.
9. Udvid afsnittet Resultat.
10. Indtast eller vælg en værdi i feltet Årsagskode for overbetaling.
    * Hvis pengebeløbene afviger i fragtbrevet og fragtfakturaen, angiver årsagskoderne for overbetaling eller underbetaling de konti, som forskellen skal registreres på, så længe forskellen ligger inden for toleranceniveauerne.  
11. Indtast eller vælg en værdi i feltet Årsagskode for underbetaling.
12. Luk siden.

