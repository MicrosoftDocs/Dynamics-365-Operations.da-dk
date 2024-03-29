---
title: Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning
description: I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd7e02a8a3bf62606c680dad91d46658775138df
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566617"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning

[!include [banner](../../includes/banner.md)]

I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted. En kanban-regel oprettes for at overføre materiale til stedet, når lagerbeholdningen falder til under 200 enheder. Ved at køre behandlingen af udligningshændelsen oprettes de nødvendige kanbans. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.


## <a name="create-a-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Klik på Ny.
3. Vælg 'Udtræk' i feltet Type.
    * Denne type bruges til at oprette kanbans til overflytning.  
4. Vælg "Hændelse" i feltet Genopfyldningsstrategi.
    * Strategien Hændelse bruges til at oprette overførslen af kanbans ud fra en hændelse. Senere i proceduren udløser du kanbans til overførsel ved hjælp af genopfyldning af lageret.  
5. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Indtast eller vælg ReplenishSpeakerComponents. Denne overførselsaktivitet har (output) lagersted og lokation 12 for modtagelsen, hvilket betyder, at materiale flyttes til lokation 12 på lagersted 12.  
6. Udvid afsnittet Detaljer.
7. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg M0007.  
8. Udvid afsnittet Hændelse.
9. Vælg "Batch" i feltet Lagergenopfyldningshændelse.
    * Der oprettes kanbans for at opfylde behovet på den relaterede lokation under behandling af udligningshændelser.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Angiv minimumantallet for varen.
1. Klik for at følge linket i feltet Produkt.
2. Klik for at følge linket i feltet Varenummer.
3. Udvid faktaboksen Produktbillede.
4. Klik på Plan i handlingsruden.
5. Klik på Varedisponering.
6. Klik på Ny.
7. Markér den valgte række på listen.
8. Indtast eller vælg en værdi i feltet Lagersted.
    * Angiv Lagersted til 12.  
9. Angiv Minimum til '200'.

## <a name="run-the-batch-event-creation-job"></a>Kør jobbet til oprettelse af batchhændelse.
1. Gå til Produktionsstyring > Periodiske opgaver > Batchafvikling for kanban-job > Udligningshændelser.
2. Klik på OK.
3. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
4. Klik op linket i den valgte række på listen.
    * Vælg den kanban-regel, du har oprettet tidligere.  
5. Udvid afsnittet Kanbans.
    * Bemærk, at der er oprettet en kanban for at overføre det nødvendige materiale til lagersted 12.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]