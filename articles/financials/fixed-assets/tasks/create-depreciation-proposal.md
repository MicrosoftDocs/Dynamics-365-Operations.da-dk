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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839995"
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

