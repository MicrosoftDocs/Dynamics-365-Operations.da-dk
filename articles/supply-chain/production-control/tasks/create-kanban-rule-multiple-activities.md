---
title: Oprette en kanban-regel for flere aktiviteter
description: Denne fremgangsmåde viser, hvordan du kan oprette en kanban-regel, der omfatter flere aktiviteter fra et produktionsflow.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b52e33c34a2fd151765833c68eab9091b22405cc
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147014"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Oprette en kanban-regel for flere aktiviteter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du kan oprette en kanban-regel, der omfatter flere aktiviteter fra et produktionsflow. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.


## <a name="create-a-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Klik på Ny.
3. Vælg 'Planlagt' i feltet Genopfyldningsstrategi.
4. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Vælg SpeakerAssemblyAndPolish.  
5. Markér afkrydsningsfeltet Flere aktiviteter.
    * Formålet er at inkludere mere end én aktivitet i kanban-reglen. Du kan vælge en sti i produktionsflowet, når du vælger den sidste planaktivitet.  
6. Angiv eller vælg en værdi i feltet Sidste planaktivitet.
    * Vælg SpeakerTestAndPackaging. Når du vælger værdien, åbnes en side automatisk. Vælg kanban-flowet SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Klik på OK.  
7. Udvid afsnittet Detaljer.
8. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg vare L0006.  

## <a name="create-kanban-and-view-jobs"></a>Opret kanban, og se job
1. Udvid afsnittet Kanbans.
2. Klik på Tilføj.
3. Skriv "1" i feltet Antal nye kanbans.
    * Dette opretter én kanban.  
4. Angiv Produktmængde til "3".
    * Kanban skal behandle 3 produkter.  
5. Angiv en dato og et klokkeslæt i feltet Forfaldsdato/-klokkeslæt.
    * Du kan angive I dag.  
6. Klik på Opret.
7. Klik på Detaljer.
    * Bemærk, at den pågældende kanban har to procesjob fra produktionsflowet. Det første er SpeakerAssemblyAndPolish, og det andet er SpeakerTestAndPackaging.  
    * Dette er det sidste trin!  

