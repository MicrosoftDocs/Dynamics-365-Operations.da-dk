---
title: Procesautomatisering
description: Dette emne indeholder oplysninger om, hvordan procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508179"
---
# <a name="process-automation"></a>Procesautomatisering

[!include[banner](../includes/banner.md)]

Procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren. Den opdaterede kalendervisning af det planlagte arbejde giver slutbrugere mulighed for at få vist og reagere på planlagt og afsluttet arbejde.

## <a name="administration"></a>Administration

Den centrale administrationsside for alle procesautomatiseringer findes i modulet Systemadministration under menuen **Konfiguration** . På denne side vises en liste over alle automatiserede processer (serier), der er oprettet i systemet. Du kan også tilføje nye procesautomatiseringer direkte fra denne side. Når en serie er konfigureret, kan du administrere hver serie på denne liste. Du kan vælge at redigere hele serien, slette den, få vist alle forekomster i en listevisning eller deaktivere serien, hvis du midlertidigt vil stoppe det planlagte arbejde i en tidsperiode. 

## <a name="calendar-view"></a>Kalendervisning 
En af de vigtigste fordele ved procesautomatisering er muligheden for at se det planlagte arbejde i en simpel kalendervisning.  Du kan bruge denne visning til at få vist arbejde for en uge ad gangen. Du kan se denne visning i højre side af siden **Procesautomatisering**. Den vil blive udfyldt med det planlagte arbejde for den valgte serie. 

[![Kalender for procesautomatisering](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Forekomster ændres
Hver forekomst kan redigeres uden at påvirke andre forekomster, der er defineret af den serie, der har oprettet dem. Forekomster af planlagt arbejde kan redigeres i kalendervisningen ved at vælge knappen **Vis/Rediger** og vælge **Forekomst**. Dette giver dig adgang til alle de indstillinger, der oprindeligt blev vist i guiden til konfiguration af serie, og giver mulighed for at foretage en engangsændring for den valgte forekomst. En forekomst af planlagt arbejde kan også slås fra ved at vælge knappen **Deaktiver** i kalendervisningen. 

## <a name="developer-documentation"></a>Udviklerdokumentation 
Dokumentationen til udviklere skrives i øjeblikket for at give udviklere mulighed for at udvide procesautomatiseringsstrukturen. Denne dokumentation indeholder oplysninger om, hvordan du kan oprette brugerdefinerede processer, som du skal køre på den batchserver, der er planlagt med guiden til procesautomatisering, og som automatisk vises i kalendervisningen.
