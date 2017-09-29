--- 
title: "Arrangere produktionsjob i forløb til procesproduktion"
description: "Denne procedure bruger malingsprodukter som et eksempel til at vise, hvordan du sorterer ordreforslag i overensstemmelse med prioriteten af farve og pakkestørrelse."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f37b561188cf9c6d90c25e395ba30aa979136590
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Arrangere produktionsjob i forløb til procesproduktion

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure bruger malingsprodukter som et eksempel til at vise, hvordan du sorterer ordreforslag i overensstemmelse med prioriteten af farve og pakkestørrelse. Det demodatafirma, der bruges til at oprette denne procedure, er USPI. Denne procedure er beregnet til produktionsplanlæggeren.


## <a name="run-master-planning-for-uspi"></a>Køre varedisponering for USPI
1. Gå til Varedisponering > Varedisponering > Kørsel > Varedisponering.
2. Klik på rullelisten i feltet Behovsplan for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Vælg MasterPlan.  
4. Klik på OK.
    * Dermed startes Varedisponering, herunder afviklingsrækkefølgen. Denne proces kan tage nogle få minutter.  

## <a name="view-planned-orders-for-the-paint-products"></a>Få vist ordreforslag for malingsprodukter
1. Gå til Varedisponering > Varedisponering > Ordreforslag.
2. Udvid faktaboksen Vareoplysninger.
3. Udvid faktaboksen Planoplysninger.
4. Klik på rullelisten i feltet Plan for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
    * Vælg MasterPlan.  
6. Klik op linket i den valgte række på listen.
7. Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P300'.
    * Lås op for at rulle til højre for at få vist bestillingsdato og leveringsdato. Bemærk, at disse varer har en ordredato for I dag, og leveringsdatoerne for ordreforslagene er ikke sorteret efter prioritet for farve og pakkestørrelse, som vist i produktnavnet. Du kan placere markøren over et varenummer for at få vist produktets navn og prioritet.  

## <a name="sequence-planned-orders-for-paint"></a>Sortere ordreforslag for malingsprodukter
1. Luk siden.
2. Gå til Varedisponering > Varedisponering > Sorterede ordreforslag.
3. Udvid faktaboksen Vareoplysninger.
4. Udvid faktaboksen Planoplysninger.
    * Bemærk: Her kan du se, at Start dato/klokkeslæt for ordreforslagene sorteres efter farve og pakkestørrelse i et tidsgruppeperiode på 28 dage. Disse perioder er defineret af et tal i feltet Kampagne. Formlen for sortering af ordreforslag fungerer som den typiske formular for ordreforslag, og produktionsplanlæggeren kan autorisere ordreforslagene her.  
5. Markér alle rækker.
6. Klik på Acceptér.
    * Dette vil opdatere ordreforslagene med den valgte rækkefølge for håndtering ved hjælp af Udsæt eller Fremskynd.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Kontrollere rækkefølgen af ordreforslag
1. Luk siden.
2. Gå til Varedisponering > Varedisponering > Ordreforslag.
3. Udvid faktaboksen Vareoplysninger.
4. Udvid faktaboksen Planoplysninger.
5. Klik på rullelisten i feltet Plan for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
    * Vælg MasterPlan.  
7. Klik op linket i den valgte række på listen.
8. Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P300'.
    * Bemærk, at ordrerne nu sorteres efter prioritet for farve og størrelse, og ordreforslagene begynder på den tidligste ordredato og leveringsdato. Validere kolonnen Ordredato eller Startdato i faktaboksen Planoplysninger.  

