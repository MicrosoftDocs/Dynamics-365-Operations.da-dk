--- 
title: Opret nummerserier vha. en guide
description: "Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5fe6e54b4ebcf6cd611af54e7066a3e39d0e677d
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a>Opret nummerserier vha. en guide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er. En masterdata- eller transaktionspost, der kræver et id, kaldes en reference. Før du kan oprette nye poster for en reference, skal du konfigurere en nummerserie og knytte den til referencen. Denne fremgangsmåde forklarer, hvordan du konfigurerer alle krævede nummerserier på samme tid ved hjælp af en guide. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til Virksomhedsadministration > Nummerserier > Nummerserier.
2. Klik på Generer.
3. Klik på Næste.
    * På denne side kan du redigere identifikationskoden, den laveste værdi og den højeste værdi. Du kan også angive, om nummerserien skal være fortløbende.   
    * Du skal ikke markere indstillingen Fortløbende, hvis du skal forudallokere numre til nummerserien.     Hvis du vil føje et områdesegment til en nummerseries format, skal du vælge formatet på listen og derefter klikke på Medtager område i format.     Hvis du vil fjerne et områdesegment fra en nummerseries format, skal du vælge formatet på listen og derefter klikke på Fjerner område fra format.     Hvis du vil udelukke en nummerserie fra automatisk generering, skal du vælge nummerserien på listen og derefter klikke på Slet.  
4. Klik på Næste.
5. Klik på Finish.

