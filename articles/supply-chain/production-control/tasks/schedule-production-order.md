---
title: Planlægge en produktionsordre
description: Denne procedure viser, hvordan du planlægger en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fa0f0f38dcb93aff9b3a1d8130fba0a0c836b3b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981100"
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