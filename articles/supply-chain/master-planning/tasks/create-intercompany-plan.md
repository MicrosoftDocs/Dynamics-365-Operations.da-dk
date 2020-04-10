---
title: Oprette en intern plan
description: Denne fremgangsmåde viser, hvordan du opretter en intern plan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a321f7e781f1ae93d8a69ee45a0e6e8e6eeb1e8d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150326"
---
# <a name="create-an-intercompany-plan"></a>Oprette en intern plan

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en intern plan. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Konfigurer en intern planlægningsgruppe 
1. Gå i **navigationsruden** til **Moduler > Varedisponering > Konfiguration > Interne planlægningsgrupper**. 
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien '10'.
3. Markér den valgte række på listen.
4. Klik på **Slet**. Dette trin skal udføres for at afkorte kørslen af den interne varedisponering.   Intern planlægning kører varedisponering i alle virksomheder i en planlægningsgruppe med start fra den laveste planlægningsrækkefølge.  
5. Klik på **Ja**.
6. Luk siden.

## <a name="create-an-intercompany-plan"></a>Oprette en intern plan
1. Gå i **navigationsruden** til **Moduler > Varedisponering > Arbejdsområder > Varedisponering**.
2. Klik på **Intern varedisponering**.  
3. Klik på rullelisten i feltet **Intern planlægningsgruppe** for at åbne opslaget.
4. Klik op linket i den valgte række på listen. Vælg intern planlægningsgruppe 10.  
5. Skriv '2' i feltet **Antal gentagelser af intern planlægning**. Den interne planlægningsgruppe 10 har to medlemmer. Hvis du vil overføre forsinkelserne fra kildefirmaet (USMF) til kundefirmaet (DEMF), skal du køre internt i begge firmaer to gange. Den første gentagelse fordeler behovet ud og identificerer forsinkelser i kildefirmaet (USMF). Den anden gentagelse overfører forsinkelserne fra USMF til DEMF.  
6. Vælg 'Genopbygning' i feltet **Første gentagelse**.
7. Vælg 'Genopbygning' i feltet **Efterfølgende gentagelser**.
8. Indtast et antal i feltet **Antal tråde**. Dette repræsenterer antallet af parallelle tråde, der bruges til planlægning.  
9. Klik på **OK**.

## <a name="view-the-result-of-the-plan"></a>Se resultatet af planen
1. Klik på rullelisten i feltet **Plan** for at åbne opslaget.
2. Klik op linket i den valgte række på listen. Klik på linket for StaticPlan. Du skal være i firmaet USMF.  
3. Klik på **Ordreforslag**.

