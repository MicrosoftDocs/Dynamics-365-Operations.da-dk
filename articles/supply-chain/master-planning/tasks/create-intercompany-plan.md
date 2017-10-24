--- 
title: Oprette en intern plan
description: "Denne fremgangsmåde viser, hvordan du opretter en intern plan."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a>Oprette en intern plan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en intern plan. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Konfigurer en intern planlægningsgruppe 
1. Gå til Interne planlægningsgrupper.
    * Overordnet planlægning > Opsætning > Interne planlægningsgrupper  
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien '10'.
3. Markér den valgte række på listen.
4. Klik på Slet.
    * Dette trin skal udføres for at afkorte kørslen af den interne varedisponering.   Intern planlægning kører varedisponering i alle virksomheder i en planlægningsgruppe med start fra den laveste planlægningsrækkefølge.  
5. Klik på Ja.
6. Luk siden.

## <a name="create-an-intercompany-plan"></a>Oprette en intern plan
1. Klik på Intern varedisponering.
    * Det er i arbejdsområdet Varedisponering.  
2. Klik på rullelisten i feltet Intern planlægningsgruppe for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Vælg intern planlægningsgruppe 10.  
4. Skriv 2 i feltet Antal gentagelser af intern planlægning.
    * Den interne planlægningsgruppe 10 har to medlemmer. Hvis du vil overføre forsinkelserne fra kildefirmaet (USMF) til kundefirmaet (DEMF), skal du køre internt i begge firmaer to gange. Den første gentagelse fordeler behovet ud og identificerer forsinkelser i kildefirmaet (USMF). Den anden gentagelse overfører forsinkelserne fra USMF til DEMF.  
5. Vælg en indstilling i feltet Første gentagelse.
6. Vælg 'Genopbygning' i feltet Første gentagelse.
7. Vælg 'Genopbygning' i feltet Efterfølgende gentagelser.
8. Indtast et antal i feltet Antal tråde.
    * Dette repræsenterer antallet af parallelle tråde, der bruges til planlægning.  
9. Klik på OK.

## <a name="view-the-result-of-the-plan"></a>Se resultatet af planen
1. Klik på rullelisten i feltet Plan for at åbne opslaget.
2. Klik op linket i den valgte række på listen.
    * Klik på linket for StaticPlan. Du skal være i firmaet USMF.  
3. Klik på Ordreforslag.


