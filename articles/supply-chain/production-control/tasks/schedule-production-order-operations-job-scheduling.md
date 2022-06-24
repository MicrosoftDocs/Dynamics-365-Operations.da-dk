---
title: Planlægge en produktionsordre med grov- og finplanlægning
description: Denne artikel drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d82d5439e57c02ddc9db4222a946bd15f4ed67e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903921"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Planlægge en produktionsordre med grov- og finplanlægning

[!include [banner](../../includes/banner.md)]

Denne artikel drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning. Der oprettes ingen job med grovplanlægning, kun job med finplanlægning. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne procedure er beregnet til produktionslederen, produktionsplanlæggeren eller den produktionstilsynsførende, der arbejder i et dedikeret produktionsmiljø.


## <a name="create-a-production-order"></a>Oprette en produktionsordre
1. Gå i navigationsruden til **Moduler > Produktionsstyring > Produktionsordrer > Alle produktionsordrer**.
2. Vælg **Ny produktionsordre**.
3. Indtast eller vælg en værdi i feltet **Varenummer**. Vælg varenummer **D0001**.  
4. Vælg **Opret**.

## <a name="schedule-operations-for-the-production-order"></a>Grovplanlægge for en produktionsordre.
1. Marker den række, der netop er oprettet.      
2. Vælg **Planlæg** i handlingsruden.
3. Vælg **Grovplanlægge**.
4. Vælg **Fremad fra planlægningsdato** i feltet **Planlægningsvej**.
5. Angiv en dato i feltet **Planlægningsdato**. Vælg en dato i fremtiden, for eksempel i dag plus en uge. Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.  
6. Vælg **OK**.
7. Markér den valgte række på listen. Bemærk, at status ændres til **Planlagt**. 
8. Vælg **Alle job**. Bemærk, at der ikke oprettes nogen job til grovplanlægning.  
9. Luk siden.

## <a name="schedule-jobs-for-the-production-order"></a>Finplanlægge for en produktionsordre.
1. Vælg **Planlæg** i handlingsruden.
2. Vælg **Finplanlægge**.
3. Vælg **Fremad fra planlægningsdato** i feltet **Planlægningsvej**.
4. Angiv en dato i feltet **Planlægningsdato**. Vælg en dato i fremtiden, for eksempel i dag plus en uge. Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.  
5. Vælg **OK**.
6. Vælg **Produktionsordre** i handlingsruden.
7. Vælg **Alle job**. Bemærk, at der baseret på den aktive rute oprettes fem jo med finplanlægning.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]