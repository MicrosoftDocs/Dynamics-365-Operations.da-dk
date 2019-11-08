---
title: Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje
description: Dette emne beskriver, hvordan du kan bruge indgangsbogen til at oprette fakturaer.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7d72c1d98100d1313109e8b5e55df02e2163174
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189355"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver, hvordan du kan bruge indgangsbogen til at oprette fakturaer. Brug derefter fakturapuljen til at afstemme fakturaen med en indkøbsordre, og færdiggør udgiften på siden med kreditorfakturaer.


## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre
1. I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Indkøbsordrer**.
2. Vælg **Ny** for at oprette en ny indkøbsordre.
3. I feltet **Kreditorkonto** skal du vælge en kreditor på rullelisten. Vælg for eksempel kreditor **1001**.
4. Vælg **OK**.
5. Vælg servicevarenummeret på rullelisten i feltet **Varenummer**. Vælg for eksempel **S0001**. Nettobeløbet er 75,00.  Det er det beløb, som vi forventer på fakturaen.  
6. Vælg **Køb** i handlingsruden.
7. Vælg **Bekræft**.

## <a name="create-and-post-and-invoice"></a>Oprette og bogføre fakturaen
1. Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Indgangsbog**.
2. Vælg **Ny**.
3. Åbn opslaget for at vælge navnet på den indgangsbog, du vil bruge.
4. Vælg navnet på den indgangsbog, du vil bruge.
5. Vælg **Linjer** for at åbne bogen og angive udgiftslinjer.
6. Vælg en kreditor i opslaget. Vælg for eksempel kreditor **1001**.
7. Angiv fakturanummeret i feltet **Faktura**.
8. Indtast en værdi i feltet **Beskrivelse**.
9. Angiv et tal i feltet **Kredit**.
10. Åbn rullelisten i feltet **Indkøbsordre** for at vælge den indkøbsordre, du oprettede tidligere.
11. Fremhæv en godkender på rullelisten i feltet **Godkendt af**, og klik på **Vælg** for at vælge den pågældende godkender.
12. Vælg **Bogfør**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Åbne en faktura fra puljen og tilpasse den til en indkøbsordre for at fuldføre fakturaprocessen
1. Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Fakturapulje**.
2. Vælg **Indkøbsordre** for at oprette en kreditorfaktura ud fra fakturaen i puljen.
3. Vælg den faktura, du vil gennemse.
4. Vælg **Opdater status for sammenholdelse** for at fuldføre sammenholdelsen.
5. Vælg **Indstillinger** i handlingsruden.
6. Vælg **Skift visning**.
7. Vælg **Gittervisning**.
8. Vælg **Bogfør**.
9. Luk formularen.
10. Gå i navigationsruden til **Moduler > Kreditor > Kreditorer > Kreditorer**.
11. Vælg den kreditor, der stod i indkøbsordren. Vælg for eksempel kreditor **1001**.
12. Vælg **Kreditor** i handlingsruden.
13. Vælg **Transaktioner**.
14. Vælg den faktura, du oprettede. Periodiseringen af indgangsbogen blev tilbageført og bogført på den relevante udgiftskonto.  
