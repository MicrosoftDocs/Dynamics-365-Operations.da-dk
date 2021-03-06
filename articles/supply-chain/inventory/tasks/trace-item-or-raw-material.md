---
title: Spore en vare eller råmateriale
description: Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges.
author: sherry-zheng
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46e46d75ecab3ec2e94372aecfd2c29783756446
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102849"
---
# <a name="trace-an-item-or-raw-material"></a>Spore en vare eller råmateriale

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges. Med denne procedure kan du identificere en vare, spore den tilbage til kilden og derefter spore den fremad gennem produktionen og salget af det færdige produkt. Processen kan bruges til at undersøge de kunder og de salgsordrer, der berøres, m.m. Proceduren bruger demodatafirmaet USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Spore et element bagud ved hjælp af et kendt batchnummer
1. Gå i **Navigationsrude** til **Moduler > Lagerstyring > Forespørgsler og rapporter > Sporingsdimensioner > Varesporing**.
2. I feltet **Varenummer** skal du vælge "P9100".
3. Klik op linket i den valgte række på listen.
4. Vælg "Bagud" i feltet **Retning**.
5. Vælg "as-12-344-01" i feltet **Batchnummer**.
6. Klik op linket i den valgte række på listen.
7. Klik på **OK**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identificere en vare, spore den fremad og foretage en analyse

Den øverste node i træet repræsenterer det disponible antal af den valgte vare og batch. Du skal udvide noderne i træet for at finde den vare, som den fremadrettede sporing skal udføres for.   
1. I træet skal du udvide de noder, der er beskrevet nedenfor og derefter vælge den sidste node.
    
    Udvid: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7,00 gal \P9100 ● Plukket ● Salgsordre 000072 ● 12/22/2015 ● -1 keg ● -4,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 \P9100 ● Produktion B-000050 ● 12/9/2015● 7 keg ● 27,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 ● Samprodukter: P9101', og vælg derefter denne node.     
2. I træet skal du udvide den node, der er beskrevet nedenfor og derefter vælge denne node.
    
    Start fra den node, du lige har valgt, udvid ' M9103 ● Produktionslinje B-000050 ● 12/9/2015 ●-160,00 lb ● Størrelse=70, Farve=OK, Sted=1, Lagersted=10, Batchnummer=App01', og vælg derefter denne node.  
3. Klik på **Spor fra node**.
4. Klik på **Fremad**.
5. Klik på **Sporing** i **Handlingsrude**.
    
    Der er flere vektoriseringsindstillinger, der indeholder oplysninger om de debitorer, der er påvirket af den vare, du sporer, og de salgsordrer, der relaterer til den vare, der er eller ikke er leveret.   
6. Klik på **Debitorer**.
7. Luk siden.
8. Klik på **Sporing** i **Handlingsrude**.
9. Klik på **Afsendte salgsordrer**.
10. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]