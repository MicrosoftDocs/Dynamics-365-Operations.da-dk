---
title: Opret afskrivningsforslag
description: Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "361285"
---
# <a name="create-depreciation-proposal"></a>Opret afskrivningsforslag

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

