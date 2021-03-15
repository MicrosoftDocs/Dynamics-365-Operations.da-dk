---
title: Oprette en kanban-regel for styklistelinjehændelse
description: Opgaven fokuserer på den konfiguration, der er nødvendig for at oprette en kanban-hændelsesregel for at sikre forsyning til produktionsstyklistelinjer i et blandet lean-miljø og et klassisk produktionsmiljø.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcef749139635b2d8858a85154ff7619c16857d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998747"
---
# <a name="create-a-bom-line-event-kanban-rule"></a>Oprette en kanban-regel for styklistelinjehændelse

[!include [banner](../../includes/banner.md)]

Opgaven fokuserer på den konfiguration, der er nødvendig for at oprette en kanban-hændelsesregel for at sikre forsyning til produktionsstyklistelinjer i et blandet lean-miljø og et klassisk produktionsmiljø. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.


## <a name="create-a-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Kanban-regler.
2. Klik på Ny.
3. Vælg 'Udtræk' i feltet Type.
    * Udtrækstypen bruges til at oprette kanbans til overflytning.  
4. Vælg "Hændelse" i feltet Genopfyldningsstrategi.
    * Strategien Hændelse er valgt for at oprette overførslen af kanbans ud fra en hændelse. Senere i opgavevejledningen vil vi udløse den ved at forkalkulere en produktionsordre.  
5. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Indtast eller vælg ReplenishSpeakerComponents. Denne overførselsaktivitet har (output) lagersted og lokation 12 for modtagelsen, hvilket betyder, at materiale flyttes til lokation 12 på lagersted 12.  
6. Udvid afsnittet Detaljer.
7. Indtast eller vælg M0001 i feltet Produkt.
8. Udvid afsnittet Hændelse.
9. Vælg 'Automatisk' i feltet Styklistehændelse.
    * Når feltet Styklistelinjehændelse er indstillet til Automatisk, oprettes der kanbans for at opfylde materialebehovet for produktionsordrens styklistelinjer.  
10. Luk siden.

## <a name="create-and-modify-a-new-production-order"></a>Oprette og redigere en ny produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
2. Klik på Ny produktionsordre.
3. Indtast eller vælg en værdi i feltet Varenummer.
    * Angiv eller vælg 'L0001'. Vi bruger vare L0001, fordi vare M0001 indgår i styklisten for vare L0001.  
4. Klik på Opret.
5. Klik på linket i rækken for L0001 på listen.
6. Klik på Stykliste.
7. Klik op linket i den valgte række på listen.
8. Klik på Rediger.
9. Vælg 'Sporet forsyning' i feltet Linjetype.
    * Sporet forsyning er valgt for at udløse oprettelse af forsyning for en kanban.  
10. Vælg Nej i feltet Ressourceforbrug.
    * Når markeringen i afkrydsningsfeltet Ressourceforbrug fjernes, kan lagerstedet ændres.  
11. Udvid sektionen Lagerdimensioner.
12. Skriv 12 i feltet Lagersted.
    * Lageret er indstillet til 12, fordi dette er lagerstedet til udlagring for udtræksaktiviteten.  
13. Skriv '12' i feltet Lokation.
    * Lokationen er indstillet til 12, fordi dette er lokationen til udlagring for udtræksaktiviteten.  
14. Luk siden.
15. Luk siden.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Forkalkulere produktionsordren og få vist den oprettede kanban
1. Klik på Forkalkulation.
    * Forkalkulation af produktionsordren udløser oprettelsen af den tilknyttede kanban for at levere varen M0001.  
2. Klik på OK.
3. Luk siden.
4. Luk siden.
5. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
6. Klik op linket i den valgte række på listen.
    * Vælg den kanban-hændelsesregel, der er oprettet for varen M0001.  
7. Udvid afsnittet Kanbans.
8. Markér den valgte række på listen.
    * Bemærk den kanban, der er oprettet for at levere M0001 til den forkalkulerede produktionsordre.  
    * Dette er det sidste trin!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]