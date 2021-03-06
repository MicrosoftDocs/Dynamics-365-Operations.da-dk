---
title: Oprette en tidsplan for et sted
description: Denne procedure viser, hvordan du planlægger produktionsordrer, der endnu ikke er startet på en lokation.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 070d8441700cd0051d421ea7e2210bcb668e8c22
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820364"
---
# <a name="create-a-schedule-for-a-site"></a>Oprette en tidsplan for et sted

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du planlægger produktionsordrer, der endnu ikke er startet på en lokation.  Demodatafirmaet USMF bruges til at fuldføre denne procedure.


## <a name="identify-production-orders-that-are-not-started"></a>Identificere produktionsordrer, der ikke er startet
1. Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.
2. Brug Quick Filter til at finde poster. Du kan f.eks. filtrere på feltet Lokation med værdien '1'.
    * 1 repræsenterer en lokation i USMF. Hvis du ikke bruger USMF, kan du vælge en lokation fra din egen virksomhed.  
3. Åbn kolonnefilteret Status.
4. Anvend et filter for feltet "Status" med værdien "Planlagt" ved hjælp af filteroperatøren "er præcis".

## <a name="create-a-schedule"></a>Oprette en tidsplan
1. Markér eller fjern markeringen af alle rækker på listen.
2. Klik på Planlæg i handlingsruden.
3. Klik på Finplanlægge.
4. Vælg 'Bagud fra leveringsdato' i feltet Planlægningsvej.
5. Vælg Nej i feltet Kapacitetsbegrænsning.
6. Vælg Nej i feltet Materialebegrænsning.
7. Klik på OK.
    * Det kan tage et stykke tid.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Vise resultatet af planlagte produktionsordrer
1. Markér den valgte række på listen.
    * Du kan markere enhver række.  
2. Klik på Produktionsordre i handlingsruden.
3. Klik på Alle job.
    * På denne side kan du se listen over job. Under fanen planlægning kan du se startdatoen og slutdatoen for et job.  
4. Klik på Materialer.
    * På denne side kan du se det forkalkulerede materialeforbrug for operationer på produktionsordren og den aktuelle disponible beholdning.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]