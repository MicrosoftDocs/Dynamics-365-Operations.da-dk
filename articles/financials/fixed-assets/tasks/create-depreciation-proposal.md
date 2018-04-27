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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-depreciation-proposal"></a>Oprette et afskrivningsforslag

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


