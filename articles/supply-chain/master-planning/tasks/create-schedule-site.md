--- 
title: Oprette en tidsplan for et sted
description: "Denne procedure viser, hvordan du planlægger produktionsordrer, der endnu ikke er startet på en lokation."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a611cb773919284b2bbe55395a7ec2b947d5c0b4
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-schedule-for-a-site"></a>Oprette en tidsplan for et sted

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

