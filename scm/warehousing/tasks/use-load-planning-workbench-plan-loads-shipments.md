--- 
title: "Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet"
description: "Denne fremgangsmåde viser, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 982c746de1329be435d9047d4057cba100475b1b
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre. Som en forudsætning skal vi skal oprette salgsordren. Denne procedure er en del af det daglige arbejde for transportkoordinatoren. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-sales-order"></a>Oprette en salgsordre
1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Vælg konto US-004.
5. Klik på OK.
6. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
7. Vælg vare A0001.
    * A0001 er aktiveret for transportstyring.  
8. Klik op linket i den valgte række på listen.
9. Angiv et tal i feltet Antal.
10. Skriv 24 i feltet Lagersted.
    * Vælg lagersted 24 i dette eksempel. Dette lagersted er aktiveret for transportstyring og avanceret lagerstedsstyring.  
11. Klik på Gem.
12. Luk siden.

## <a name="create-a-new-load"></a>Opret en ny belastning
1. Gå til Transportstyring > Planlægning > Lastplanlægningspanel.
2. Klik på fanen Salgslinjer.
    * Nu kan du opbygge belastningen for den salgsordre, som du lige har oprettet. Belastninger kan bygges baseret på udbud og efterspørgsel fra købsordrer, flytteordrer og salgsordrer.  
3. Klik på fanen Udbud og efterspørgsel i handlingsruden.
4. Klik på Til ny last.
5. Klik på rullelisten i feltet Lastskabelons-id for at åbne opslaget.
    * Lastskabelonen definerer det maksimale mål for vægt og volumen af den samlede belastning. For eksempel kan lastskabelonen repræsentere størrelsen af en container eller lastbil.  
6. Klik op linket i den valgte række på listen.
7. Klik på OK.

## <a name="rate-and-route-the-load"></a>Vurder og ruteplanlæg belastningen
1. Klik på Vurdering og ruteplanlægning.
2. Klik på Satsrutepanel.
3. Klik på Satsbutik.
4. Find og vælg den ønskede post på listen.
5. Klik på Tildel.
6. Luk siden.
7. Luk siden.


