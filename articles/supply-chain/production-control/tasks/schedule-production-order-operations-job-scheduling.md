---
title: Planlægge en produktionsordre med grov- og finplanlægning
description: Denne procedure drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562132"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Planlægge en produktionsordre med grov- og finplanlægning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning. Der oprettes ingen job med grovplanlægning, kun job med finplanlægning. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne procedure er beregnet til produktionslederen, produktionsplanlæggeren eller den produktionstilsynsførende, der arbejder i et dedikeret produktionsmiljø.


## <a name="create-a-production-order"></a>Oprette en produktionsordre
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
2. Klik på Ny produktionsordre.
3. Indtast eller vælg en værdi i feltet Varenummer.
    * Vælg varenummer D0001.  
4. Klik på Opret.

## <a name="schedule-operations-for-the-production-order"></a>Grovplanlægge for en produktionsordre.
1. Markér den valgte række på listen.
    * Vælg den produktionsordre, du lige har oprettet. Det skal være øverst på listen.      
2. Klik på Planlæg i handlingsruden.
3. Klik på Grovplanlægge.
4. Vælg 'Fremad fra planlægningsdato' i feltet Planlægningsvej.
5. Angiv en dato i feltet Planlægningsdato.
    * Vælg en dato i fremtiden, for eksempel i dag plus en uge. Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.  
6. Klik på OK.
7. Markér den valgte række på listen.
    * Bemærk, at status ændres til Planlagt.  
8. Klik op linket i den valgte række på listen.
9. Klik på Alle job.
    * Bemærk, at der ikke oprettes nogen job til grovplanlægning.  
10. Luk siden.

## <a name="schedule-jobs-for-the-production-order"></a>Finplanlægge for en produktionsordre.
1. Klik på Planlæg i handlingsruden.
2. Klik på Finplanlægge.
3. Vælg 'Fremad fra planlægningsdato' i feltet Planlægningsvej.
4. Angiv en dato i feltet Planlægningsdato.
    * Vælg en dato i fremtiden, for eksempel i dag plus en uge. Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.  
5. Klik på OK.
6. Klik på Produktionsordre i handlingsruden.
7. Klik på Alle job.
    * Bemærk, at der baseret på den aktive rute oprettes fem jo med finplanlægning.  

