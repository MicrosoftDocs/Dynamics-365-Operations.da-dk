---
title: Oprette aktivitetsrelation - Efterfølgende
description: Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cee0c75de1fee24cfb6df018de62ece102c96cc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579202"
---
# <a name="create-activity-relation---successor"></a>Oprette aktivitetsrelation - Efterfølgende

[!include [banner](../../includes/banner.md)]

Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer. Denne optagelse viser, hvordan du opretter en aktivitetsrelation.

Forudsætninger:

- Et produktionsflow og en version i kladdetilstand. 

- To aktiviteter, der følger efter hinanden i produktionsflowet, er oprettet, men ikke relateret.


## <a name="find-the-production-flow-version"></a>Find produktionsflowversionen 
1. Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Markér den valgte række på listen.
5. Vælg en kladdeversion på listen.
    * Aktivitetsrelationer kan føjes til både kladdeversioner eller aktive versioner af et produktionsflow.  

## <a name="open-the-activity-overview"></a>Åbn den aktivitetsoversigten
1. Klik på Aktiviteter.
    * Bemærk, at formularen viser alle aktiviteter i produktionsflowet, der er allokeret til versionen af de produktionsflow, du arbejder i.  

## <a name="add-a-successor"></a>Tilføj en efterfølgende aktivitet
1. Klik på Tilføj efterfølgende aktivitet.
2. Klik på rullelisten i feltet Aktivitet for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Markér afkrydsningsfeltet Begrænsning.
6. Skriv et tal i feltet Begrænsningsværdi.
    * Begrænsningstiden er den tid, der skal planlægges mellem den planlagte afslutning af den foregående aktivitet (forfaldsdato og tid) og det planlagte starttidspunkt for den efterfølgende aktivitet.  
7. Angiv en værdi i feltet Enheder.
8. Angiv et tal i feltet Procestidsforhold.
    * Hvis begge aktiviteter kører i den samme takt, skal procestidsforholdet være 1. Hvis den foregående opgave kører med dobbelt hastighed af den efterfølgende, skal forholdet være 2.   Procestidsforholdene bruges til at beregne de enkelte procestider for produktionsflowaktiviteterne.  
9. Klik på OK.
10. Luk siden.
11. Klik på fanen GridPanel.
12. Luk siden.
13. Opdater siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]