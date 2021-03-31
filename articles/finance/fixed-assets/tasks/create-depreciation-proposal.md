---
title: Oprette et afskrivningsforslag
description: Dette emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslå afskrivning for anlægsaktiver.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4852b25ef628cdef6f75f6edf550c539e344a4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227058"
---
# <a name="create-a-depreciation-proposal"></a>Oprette et afskrivningsforslag

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslå afskrivning for anlægsaktiver. Denne opgave bruger USMF-demofirmaet og rollen revisor.


## <a name="create-a-depreciation-proposal"></a>Oprette et afskrivningsforslag
1. I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag**.
2. Vælg en indstilling på rullelisten i feltet **Kladdenavn**.
3. Indtast en dato i feltet **Til dato**.

    - Vælg indstillingen **Opsummer afskrivning**, hvis du vil opsummere månedlige afskrivninger på én kladdelinje.  
    - Hvis Til dato-værdien f.eks. er 31. marts 2015, genereres følgende beskrivelse: "Afskrivning siden 31. januar 2015". Derefter indstilles feltet **Dato** på de foreslåede kladdelinjer til 31. marts 2015.  
    - Afskrivningsforslaget kan filtreres efter aktiv, aktivgruppe eller andre kriterier ved hjælp af parameteren **Filter**.  
    - Når du bruger formen **Opret anskaffelses- eller afskrivningsforslag til anlægsaktiver**, kan du foreslå afskrivning i batch. Dette anbefales til større forslag, der vil bruge flere systemressourcer. Hvis du vælger batchindstillingen, kan du stadig fuldføre andre opgaver samtidig. Når du foreslår afskrivning på denne måde, beregnes afskrivningen for værdimodeller for anlægsaktiver.  

4. Vælg **Opret kladde**.

## <a name="review-depreciation-entries"></a>Gennemse afskrivningsposter.
1. I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.
2. Find og vælg den ønskede post på listen.
3. Vælg **Linjer**.
4. Vælg **Bogfør**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]