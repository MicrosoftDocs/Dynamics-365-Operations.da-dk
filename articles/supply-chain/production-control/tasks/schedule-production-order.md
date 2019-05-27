---
title: Planlægge en produktionsordre
description: Denne procedure viser, hvordan du planlægger en produktionsordre.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7ee023f39cc5d02b0f5b80fbb3ae3ad0c9774
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562069"
---
# <a name="schedule-a-production-order"></a>Planlægge en produktionsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

