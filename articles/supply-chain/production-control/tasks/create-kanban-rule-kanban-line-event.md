---
title: Oprette en kanban-regel ved hjælp af en kanban-linjehændelse
description: Denne fremgangsmåde opretter en kanban-regel ved at bruge indstillingen for kanban-linjehændelsen til at udløse træk fra en procesaktivitet.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7aaf959db0f0a136fc615f9a57ec787ef6cf2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579154"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Oprette en kanban-regel ved hjælp af en kanban-linjehændelse

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde opretter en kanban-regel ved at bruge indstillingen for kanban-linjehændelsen til at udløse træk fra en procesaktivitet. Kanban-reglen udløses af en kanban-procesaktivitet, med en mængde lig med eller større end 25 hver. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.


## <a name="create-a-kanban-rule"></a>Oprette en kanban-regel
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Klik på Ny.
3. Vælg "Hændelse" i feltet Genopfyldningsstrategi.
    * Derved genereres kanbans direkte ud fra efterspørgsel. Den bruges til at konfigurere regler, der definerer et scenario for fremstilling efter ordre.  
4. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Indtast eller vælg SpeakerAssemblyAndPolish. Den første aktivitet i en produktionskanban-regel er en procesaktivitet i produktionsflowet. Når du vælger aktiviteten, kopieres gyldighedsdatoerne for aktiviteten til gyldighedsdatoerne for kanban-reglen.  
5. Udvid afsnittet Detaljer.
6. Skriv 'L0001' i feltet Produkt.
7. Udvid afsnittet Hændelse.
8. Vælg 'Automatisk' i feltet Kanban-linjehændelse.
    * Dette genererer hændelses-kanbans efter behov.  Dette felt bruges til at konfigurere kanban-regler, der genopfylder materiale, som kræves i en downstream-procesaktivitet. Når du vælger Automatisk, oprettes der hændelses-kanbans med behovet. Denne indstilling anbefales, hvis du forventer at køre produktionen samme dag.  
9. Angiv Mindste antal hændelser "25".
    * Hændelses-kanbans genereres, når behovsmængden er lig med eller mere end dette felt. Dette er nyttigt, hvis du vil producere en ordremængde, der er mindre end dette felt på én maskine, og mere end dette felt på en anden maskine.  
10. Klik på Gem.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Opret salgsordre, og udløs kanban-kæde
1. Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Vælg debitorkontoen US-003, Forest Wholesales.  
4. Klik på OK.
5. Skriv 'L0001' i feltet Varenummer.
    * L0001 er den vare, du har oprettet kanban-reglen for.  
6. Angiv antallet til '27'.
    * Da 27 er højere end minimumantallet på 25 for kanban-reglen, udløser det en hændelses-kanban.  
7. Skriv "1" i feltet Sted.
8. Indtast eller vælg en værdi i feltet Lagersted.
    * Vælg lagersted 13.  
9. Klik på Gem.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Få vist den kanban, der er genereret af kanban-reglen
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Find og vælg den ønskede post på listen.
3. Udvid afsnittet Kanbans.
    * Bemærk, at en kanban for 27 blev oprettet for at behandle aktiviteten ud fra den oprettede kanban-regel.  
    * Dette er det sidste trin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]