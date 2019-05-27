---
title: Spore en vare eller råmateriale
description: Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges.
author: pjacobse
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 897a777b3f4ce05fe995aa98a72feb99d82837ef
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561288"
---
# <a name="trace-an-item-or-raw-material"></a>Spore en vare eller råmateriale

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges. Med denne procedure kan du identificere en vare, spore den tilbage til kilden og derefter spore den fremad gennem produktionen og salget af det færdige produkt. Processen kan bruges til at undersøge de kunder og de salgsordrer, der berøres, m.m. Proceduren bruger demodatafirmaet USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Spore et element bagud ved hjælp af et kendt batchnummer
1. Gå til Lagerstyring > Forespørgsler og rapporter > Sporingsdimensioner > Varesporing.
2. I feltet Varenummer skal du vælge P9100.
3. Klik op linket i den valgte række på listen.
4. Vælg 'Bagud' i feltet Retning.
5. Vælg as-12-344-01' i feltet Batchnummer.
6. Klik op linket i den valgte række på listen.
7. Klik på OK.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identificere en vare, spore den fremad og foretage en analyse
    * Den øverste node i træet repræsenterer det disponible antal af den valgte vare og batch. Du skal udvide noderne i træet for at finde den vare, som den fremadrettede sporing skal udføres for.   
1. I træet skal du udvide de noder, der er beskrevet nedenfor og derefter vælge den sidste node.
    * Udvid: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7,00 gal \P9100 ● Plukket ● Salgsordre 000072 ● 12/22/2015 ● -1 keg ● -4,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 \P9100 ● Produktion B-000050 ● 12/9/2015● 7 keg ● 27,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 ● Samprodukter: P9101', og vælg derefter denne node.     
2. I træet skal du udvide den node, der er beskrevet nedenfor og derefter vælge denne node.
    * Start fra den node, du lige har valgt, udvid ' M9103 ● Produktionslinje B-000050 ● 12/9/2015 ●-160,00 lb ● Størrelse=70, Farve=OK, Sted=1, Lagersted=10, Batchnummer=App01', og vælg derefter denne node.  
3. Klik på Spor fra node.
4. Klik på Fremad.
5. Klik på Sporing i handlingsruden.
    * Der er flere vektoriseringsindstillinger, der indeholder oplysninger om de debitorer, der er påvirket af den vare, du sporer, og de salgsordrer, der relaterer til den vare, der er eller ikke er leveret.   
6. Klik på Debitorer.
7. Luk siden.
8. Klik på Sporing i handlingsruden.
9. Klik på Afsendte salgsordrer.
10. Luk siden.

