--- 
title: Oprette et afskrivningsforslag
description: "Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ffc358fa7db0ae40fb39d3acdfee7783949f0e1f
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-depreciation-proposal"></a>Oprette et afskrivningsforslag

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver. Denne opgave bruger USMF-demofirmaet og rollen revisor.


## <a name="create-depreciation-proposal"></a>Opret afskrivningsforslag
1. Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.
2. Klik på rullelisten i feltet Kladdenavn for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
4. Indtast en dato i feltet Til dato.
    * Markér indstillingen Opsummer afskrivning, hvis du vil opsummere månedlige afskrivninger på én kladdelinje.  
    * Hvis Til dato-værdien f.eks. er 31. marts 2015, genereres følgende beskrivelse: "Afskrivning siden 31. januar 2015". Derefter indstilles feltet Dato på de foreslåede kladdelinjer til 31. marts 2015.  
    * Afskrivningsforslaget kan filtreres efter aktiv, aktivgruppe eller andre kriterier ved hjælp af parameteren Filter.  
    * Når du bruger Opret anskaffelses- eller afskrivningsforslag til formen anlægsaktiver, kan du foreslå afskrivning i batch. Dette anbefales til større forslag, der vil bruge flere systemressourcer. Hvis du vælger batchindstillingen, kan du stadig fuldføre andre opgaver samtidig. Når du foreslår afskrivning på denne måde, beregnes afskrivningen for værdimodeller for anlægsaktiver.  
5. Klik på Opret kladde.

## <a name="review-depreciation-entries"></a>Gennemse afskrivningsposter.
1. Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.
2. Find og vælg den ønskede post på listen.
3. Klik på Linjer.
4. Klik på Bogfør.


