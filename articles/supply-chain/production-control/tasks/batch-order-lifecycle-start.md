---
title: Livscyklus for batchordre fra oprettelse til start
description: Denne procedure fører dig gennem den første del af livscyklussen for en batchordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579250"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Livscyklus for batchordre fra oprettelse til start

[!include [banner](../../includes/banner.md)]

Denne procedure fører dig gennem den første del af livscyklussen for en batchordre.

Fra oprettelse, forkalkulation og over planlægning af produktionsjob til den faktiske start på en batchordre.



Det demodatafirma, der bruges til at oprette denne procedure, er USMF. 



Forudsætningerne for at køre proceduren med et andet datasæt er et frigivet produkt med en aktiv version af formel og rute.


## <a name="create-a-batch-order"></a>Oprette en batchordre
1. Gå til Alle produktionsordrer.
2. Klik på Ny batchordre.
3. Indtast eller vælg en værdi i feltet Varenummer.
4. Klik på Opret.
5. Brug Quick Filter til at filtrere på feltet Produktion med værdien "b".

## <a name="view-production-formula-and-expected-co-products"></a>Få vist produktionsformel og forventede samprodukter
1. Klik på Produktionsordre i handlingsruden.
2. Klik på Formel.
3. Luk siden.
4. Klik på Ko-produkter.
5. Luk siden.

## <a name="estimate-the-batch-order"></a>Forkalkulere batchordren
1. Klik på Forkalkulation.
2. Klik på OK.
3. Klik på Administrer omkostninger i handlingsruden.
4. Klik på Vis beregningsoplysninger.
5. Luk siden.

## <a name="release-the-batch-order"></a>Frigive batchordren
1. Klik på Produktionsordre i handlingsruden.
2. Klik på Frigiv.
3. Klik på OK.

## <a name="schedule-production-jobs"></a>Planlægge produktionsjob
1. Klik på Planlæg i handlingsruden.
2. Klik på Finplanlægge.
3. Vælg Nej i feltet Kapacitetsbegrænsning.
4. Vælg Nej i feltet Materialebegrænsning.
5. Klik på OK.
6. Klik på Produktionsordre i handlingsruden.
7. Klik på Alle job.
8. Luk siden.

## <a name="start-the-batch-order"></a>Starte batchordren
1. Klik på Start.
2. Klik på fanen Generelt.
3. Vælg Nej i feltet Bogfør plukliste nu.
4. Klik på OK.
5. Klik på Vis i handlingsruden.
6. Klik på Plukliste.
7. Klik op linket i den valgte række på listen.
8. Luk siden.
9. Luk siden.
10. Klik på Rutekort.
11. Klik op linket i den valgte række på listen.
12. Luk siden.
13. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]