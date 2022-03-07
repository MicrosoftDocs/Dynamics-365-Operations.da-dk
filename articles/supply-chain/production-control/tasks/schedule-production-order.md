---
title: Planlægge en produktionsordre
description: Denne procedure viser, hvordan du planlægger en produktionsordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43d183764def1b1bea7bbe140c25e0eec0b692b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580570"
---
# <a name="schedule-a-production-order"></a>Planlægge en produktionsordre

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du planlægger en produktionsordre. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Dette er den tredje procedure ud af syv, der beskriver produktionsordrelivscyklussen.


## <a name="schedule-a-production-order"></a>Planlægge en produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
    * Vælg en produktionsordre, som har statussen Forkalkuleret.  
2. Klik på Planlæg i handlingsruden.
3. Klik på Finplanlægge.
    * Parametrene for planlægning konfigureres på denne side. Du kan konfigurere parametre for bestemte brugere eller alle brugere.  
4. Vælg "Fremad fra i dag" i feltet Planlægningsvej.
5. Angiv en dato i feltet Planlægningsdato.
6. Markér eller fjern markeringen i afkrydsningsfeltet Kapacitetsbegrænsning.
7. Markér eller fjern markeringen i afkrydsningsfeltet Materialebegrænsning.
8. Klik på OK.

## <a name="view-the-scheduling-results"></a>Vise planlægningsresultaterne
1. Klik på Produktionsordre i handlingsruden.
2. Klik på Alle job.
    * Denne side viser de planlagte opgaver, som du lige har oprettet.  
3. Udvid eller skjul sektionen Planlægning.
    * Du kan få vist den planlagte dato og klokkeslæt i oversigtspanelet Planlægning.  
4. Klik på Forespørgsler.
5. Klik på Kapacitetsbelastning.
    * Siden Kapacitetsbelastning viser den kapacitet, der er reserveret via finplanlægning, det samlede antal timer, som aktuelt er reserveret for ressourcen, og antallet af timer, der er tilgængelige til finplanlægning af ressourcen.  
6. Luk siden.
7. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]