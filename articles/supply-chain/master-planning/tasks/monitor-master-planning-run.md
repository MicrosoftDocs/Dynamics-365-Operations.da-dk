---
title: Overvåge kørsel af en varedisponering
description: Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845107"
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

