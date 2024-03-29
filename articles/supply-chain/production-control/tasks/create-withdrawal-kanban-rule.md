---
title: Oprette en kanban-regel for udbetaling
description: Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba30e9d09e9eeb0cd7428aafc1195d6b7e7caaa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574467"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Oprette en kanban-regel for udbetaling

[!include [banner](../../includes/banner.md)]

Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder genopfyldning af et nyt eller ændret materiale.


## <a name="create-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til kanban-regler.
2. Klik på Ny.
3. Vælg 'Udtræk' i feltet Type.
    * Udtrækstypen bruges til kanban-regler i forbindelse med overførsel af materiale eller varer.  
4. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Vælg ReplenishSpeakerComponents.   Denne aktivitet er indstillet til at flytte komponenter fra lagersted 11, lokation 11 til lagersted 12, lokation 12.  
5. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg M0007.  
6. Angiv et tal i feltet Leveringstid.
    * For eksempel 60.  
7. Indtast eller vælg en værdi i feltet Måleenhed.
    * For eksempel Minutter.  

## <a name="set-quantities-for-kanban"></a>Indstille mængder for kanban
1. Angiv Standardmængde til "5".
    * Dette er det antal, der skal overføres for hver kanban.  
2. Indtast '2' i feltet Fast kanban-mængde.
    * Dette er antallet af kanbans, der skal være aktive. I dette tilfælde overfører to kanbans fem hver.  
3. Angiv "1" i feltet Minimum for påmindelsesgrænse.
    * Bruges til at holde styr på det mindste antal fulde kanbans, der skal være på destinationen. Den bruges f.eks. på oversigten over kanban-mængde.  
4. Angiv "2" i feltet Maksimum for påmindelsesgrænse.
    * Bruges til at holde styr på det maksimale antal fulde kanbans, der må være på destinationen. Den bruges f.eks. på oversigten over kanban-mængde.  

## <a name="create-kanbans"></a>Opret kanbans
1. Klik på Gem.
    * Kanban-reglen skal gemmes, før du kan oprette kanbans.  
2. Klik på Tilføj.
    * Bemærk, at der ikke er nogen aktive kanbans, fordi er det foreslåede 'Antal nye kanbans' er 2, hvilket svarer til 'Fast kanban-mængde'.  
3. Klik på Opret.
    * Dette opretter to kanbans.  
    * Bemærk, at der blev oprettet to kanbans for hver fem for denne udtræks-kanban-regel.  Dette er det sidste trin i denne procedure.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]