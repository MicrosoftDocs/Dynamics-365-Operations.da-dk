--- 
title: "Overvåge kørsel af en varedisponering"
description: "Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-a-master-planning-run"></a>Overvåge kørsel af en varedisponering

[!include [task guide banner](../../includes/task-guide-banner.md)]

Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang. Brug USMF-demodatafirmaet til at fuldføre denne procedure.


## <a name="run-master-planning"></a>Køre varedisponering
1. Klik på Varedisponering.
    * Det findes på standarddashboardet.  
2. Indtast eller vælg en værdi i feltet Plan.
    * Eksempel: StaticPlan  
3. Klik på Kør.
4. Vælg Ja i feltet Spor behandlingstidspunkt.
    * Hvis feltet allerede er markeret, skal du springe over dette trin.  
5. Indtast et antal i feltet Antal tråde.
6. Udvid posterne for at inkludere sektion.
7. Klik på Filtrér.
8. Markér den valgte række på listen.
    * Marker rækken, hvor feltet = Varenummer.  
9. Indtast eller vælg en værdi i feltet Kriterier.
    * Eksempel: T0001  
10. Klik på OK.
11. Klik på OK.

## <a name="monitor-the-master-planning-run"></a>Overvåge kørslen af varedisponering
1. Klik på Historik.
2. Klik på Forespørgsler.
3. Klik på Procesopgavens varighed.
4. Find og vælg den ønskede post på listen.
    * For hver vare kan du få et overblik over, hvor lang tid det tog at fuldføre hvert trin i planlægningen.  


