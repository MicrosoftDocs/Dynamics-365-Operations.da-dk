---
title: Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje
description: Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b4e9a52a383d4acc0bf2adc669fd88c0c0f7402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "357444"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer.  Brug derefter fakturapuljen til at afstemme fakturaen med en indkøbsordre, og færdiggør udgiften på siden med kreditorfakturaer.


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. Gå til Kreditor > Indkøbsordrer > Indkøbsordrer.
2. Klik på Ny for at oprette en indkøbsordre.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Vælg kreditoren på listen. For eksempel kreditor 1001.
5. Klik på OK.
6. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
7. Markér varenummeret for tjenester på listen. Vælg for eksempel S0001.
8. Klik på varenummeret, og vælg det.
    * Nettobeløbet er 75,00.  Det er det beløb, som vi forventer på fakturaen.  
9. Klik på Køb i handlingsruden.
10. Klik på Bekræft.

## <a name="create-and-post-and-invoice"></a>Oprette og bogføre fakturaen
1. Gå til Kreditor > Fakturaer > Indgangsbog.
2. Klik på Ny.
3. Åbn opslaget for at vælge navnet på den indgangsbog, du vil bruge.
4. Vælg navnet på den indgangsbog, du vil bruge.
5. Klik på Linjer for at åbne bogen og angive udgiftslinjer.
6. Vælg en kreditor i opslaget. Klik for eksempel på kreditor 1001.
7. Angiv fakturanummeret i feltet Faktura.
8. Indtast en værdi i feltet Beskrivelse.
9. Angiv et tal i feltet Kredit.
10. Klik på rullelisten i feltet Indkøbsordre for at åbne opslaget.
11. Vælg den indkøbsordre, du oprettede tidligere.
12. Klik på rullelisten i feltet Godkendt af for at åbne opslaget.
13. Fremhæv en godkender, og klik på Vælg for at vælge den pågældende godkender.
14. Klik på Bogfør.
15. Luk formularen.
16. Luk formularen.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Åbne en faktura fra puljen og tilpasse den til en indkøbsordre for at fuldføre fakturaprocessen
1. Gå til Kreditor > Fakturaer > Fakturapulje.
2. Klik på Indkøbsordre for at oprette en kreditorfaktura ud fra fakturaen i puljen.
3. Vælg den faktura, du vil gennemse.
4. Klik på Opdater status for sammenholdelse for at fuldføre sammenholdelsen.
5. Klik på Indstillinger i handlingsruden.
6. Klik på Skift visning.
7. Klik på Gittervisning.
8. Klik på Bogfør.
9. Luk formularen.
10. Gå til Kreditor > Kreditorer > Kreditorer.
11. Vælg den kreditor, der stod i indkøbsordren. Vælg for eksempel kreditor 1001.
12. Klik op linket i den valgte række på listen.
13. Klik på Kreditor i handlingsruden.
14. Klik på Transaktioner.
15. Vælg den faktura, du oprettede.
    * Periodiseringen af indgangsbogen blev tilbageført og bogført på den relevante udgiftskonto.  

