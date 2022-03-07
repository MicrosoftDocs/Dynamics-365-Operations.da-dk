---
title: Oprette en intern plan
description: Denne fremgangsmåde viser, hvordan du opretter en intern plan.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578266"
---
# <a name="create-an-intercompany-plan"></a>Oprette en intern plan

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du opretter en intern plan. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Konfigurer en intern planlægningsgruppe

1. Gå i **navigationsruden** til **Moduler > Varedisponering > Konfiguration > Interne planlægningsgrupper**.
2. Brug Quick Filter til at finde poster. For eksempel kan du filtrere på feltet Navn med værdien '10'.
3. Markér den valgte række på listen.
4. Vælg **Slet**. Dette trin skal udføres for at afkorte kørslen af den interne varedisponering.   Intern planlægning kører varedisponering i alle virksomheder i en planlægningsgruppe med start fra den laveste planlægningsrækkefølge.  
5. Vælg **Ja**.
6. Luk siden.

## <a name="create-an-intercompany-master-plan"></a>Oprette en intern behovsplan

1. Gå i **navigationsruden** til **Moduler > Varedisponering > Arbejdsområder > Varedisponering**.
2. Vælg **Intern varedisponering**.  
3. Vælg rullelistens knap i feltet **Intern planlægningsgruppe** for at åbne opslaget.
4. Vælg linket i den valgte række på listen. Vælg intern planlægningsgruppe 10.  
5. Skriv '2' i feltet **Antal gentagelser af intern planlægning**. Den interne planlægningsgruppe 10 har to medlemmer. Hvis du vil overføre forsinkelserne fra kildefirmaet (USMF) til kundefirmaet (DEMF), skal du køre internt i begge firmaer to gange. Den første gentagelse fordeler behovet ud og identificerer forsinkelser i kildefirmaet (USMF). Den anden gentagelse overfører forsinkelserne fra USMF til DEMF.  
6. Vælg 'Genopbygning' i feltet **Første gentagelse**.
7. Vælg 'Genopbygning' i feltet **Efterfølgende gentagelser**.
8. Indtast et antal i feltet **Antal tråde**. Dette repræsenterer antallet af parallelle tråde, der bruges til planlægning.  
9. Vælg **OK**.

## <a name="view-the-result-of-the-plan"></a>Se resultatet af planen

1. Vælg rullelistens kap i feltet **Plan** for at åbne opslaget.
2. Vælg linket i den valgte række på listen. Vælg linket for StaticPlan. Du skal være i firmaet USMF.  
3. Vælg **Ordreforslag**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]