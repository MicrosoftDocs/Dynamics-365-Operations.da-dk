--- 
title: Oprette salgsordrefakturaer
description: Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-order-invoices"></a>Oprette salgsordrefakturaer

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling. Denne procedure bruger demofirmaet USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Opret en faktura fra en salgsordre.
1. Gå til Debitor > Ordrer > Salgsordrer, der er afsendt men ikke faktureret.
2. Vælg en salgsordre på listen. 
3. Klik på Faktura i handlingsruden.
4. Klik på Faktura.
    * Bemærk, at denne salgsordre har flere tilknyttede følgesedler. Den viser kun ordet <multiple> i stedet for nummeret på følgesedlen.  
5. Udvid sektionen Parametre.
    * Bogføring skal være angivet til Ja for at bogføre fakturaen. Du kan også deaktivere bogføring og bare udskrive fakturaen. Du kan dog opnå det samme resultat ved at oprette en proformafaktura i stedet for en faktura.  
    * Denne indstilling anvendes til batchjob. Forespørgslen køres, når batchjobbet køres.    
6. Vælg "Efter" i feltet Udskriv.
7. Vælg Ja for Udskriv faktura.
    * Udskriftsstyring kan udskrive flere kopier af fakturaen og også sende fakturaen via mail som en PDF-fil.  
8. Vælg "Opsummer" i feltet Udskriv gebyrer.
9. Vælg "Saldo" i feltet Kontrollér kreditmaks.
10. Klik på Annuller.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinere ordrer i én enkelt faktura
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Find en debitor, der har flere fakturaer, der er åbne.
3. Vælg en åben salgsordre.
4. Vælg en anden salgsordre for den samme kunde.
5. Klik på Faktura i handlingsruden.
6. Klik på Faktura.
7. Udvid sektionen Parametre.
8. Vælg "Alle" i feltet Antal.
    * Bemærk, at der er vist to fakturaer oversigtsafsnittet. Nu vi flette dem til en enkelt faktura.  
9. Vælg "Fakturakonto"i samleopdateringen for feltet.
10. Klik på Arranger for at flette salgsordrerne til en enkelt faktura.
    * De to salgsordrer er nu flettet i én faktura.   
11. Klik på Annuller.
12. Klik på Ja.

## <a name="post-invoices-in-a-batch"></a>Bogføre fakturaer i et batch
1. Gå til Debitor > Fakturaer > Batchfakturering > Faktura.
2. Klik på Vælg.
3. Klik på OK.
4. Klik på Batch.
5. Klik på Ja for at aktivere batchbehandling.
6. Klik på Gentagelse.
7. Vælg Dage
8. Klik på OK.
9. Klik på OK.
10. Klik på Annuller.
11. Klik på Ja.


