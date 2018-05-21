--- 
title: Masseafslutning af regnskabsperiode
description: "Denne procedure viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 1954bfdf4807e91d275e3a1ba80f959bdf9464a8
ms.contentlocale: da-dk
ms.lasthandoff: 10/26/2017

---
# <a name="mass-financial-period-close"></a>Masseafslutning af regnskabsperiode

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen. Desuden viser opgaven, hvordan du kan begrænse bogføring for en brugergruppe til bestemte moduler.

1. Gå til Finans > Luk periode > Finanskalendere.
    * Bemærk, at listen over juridiske enheder, der vises, afhænger af den regnskabskalender, der er valgt på siden. Kun juridiske enheder, der bruger den valgte regnskabskalender, vises.  
2. Klik på Rediger.
3. Vælg den periode, du vil ændre status for.
4. Vælg de juridiske enheder, du vil opdatere status for.
    * Du kan hurtigt markere alle de juridiske enheder ved at markere afkrydsningsfeltet i øverste venstre side af gitteret.  
5. Vælg Opdater modul adgang for at definere bogføringsadgang til et bestemt modul.
    * Modulstatus kan også opdateres én efter én ved at redigere poster i gitteret. Knappen er nyttig, når du hurtigt vil opdatere flere poster for juridiske enheder.  
6. I Programmodul skal du vælge det modul, du vil opdatere status for. Klik på Vælg.
7. I Adgangsniveau skal du markere Alle, Ingen eller en bestemt brugergruppe. Klik på Vælg.
    * Alle angiver, at alle brugere med Rediger-adgang til modulet kan bogføre, hvis perioden er åben. Ingen angiver, at ingen brugere kan bogføre til modulet, hvis perioden er åben. En bestemt brugergruppe angiver, at kun brugere i gruppen kan bogføre til modulet, hvis perioden er åben.  
8. Klik på Opdater.
9. Vælg en anden periode, du vil opdatere status for.
10. Vælg de juridiske enheder, du vil opdatere periodestatus for.
11. Vælg Opdater periodestatus, og angiv status til På hold, Åben eller Permanent lukket.
    * Åben angiver, at der kan bogføres til perioden, hvis brugeren har adgang. På hold betyder, at der ikke kan bogføres på perioden, men perioden kan genåbnes. Permanent lukket betyder, at perioden er lukket og ikke kan åbnes. Reguleringer kan ikke bogføres. Det anbefales ikke at indstille en periode til Permanent lukket, før alle reguleringer og revisioner er afsluttet.  
12. Klik på Opdater.


