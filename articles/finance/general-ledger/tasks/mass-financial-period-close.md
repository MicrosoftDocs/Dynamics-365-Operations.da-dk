---
title: Masseafslutning af regnskabsperiode
description: Dette emne viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144976"
---
# <a name="mass-financial-period-close"></a>Masseafslutning af regnskabsperiode

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen. Desuden viser opgaven, hvordan du kan begrænse bogføring for en brugergruppe til bestemte moduler.

1. Gå til **Moduler > Finans > Luk periode > Finanskalendere** i navigationsruden. Bemærk, at listen over juridiske enheder, der vises, afhænger af den regnskabskalender, der er valgt på siden. Kun juridiske enheder, der bruger den valgte regnskabskalender, vises.
2. Vælg **Rediger**.
3. Vælg den periode, du vil ændre status for.
4. Vælg de juridiske enheder, du vil opdatere status for. Du kan hurtigt markere alle de juridiske enheder ved at markere afkrydsningsfeltet i øverste venstre side af gitteret.  
5. Vælg **Opdater modul adgang** for at definere bogføringsadgang til et bestemt modul. Modulstatus kan også opdateres én efter én ved at redigere poster i gitteret. Knappen er nyttig, når du hurtigt vil opdatere flere poster for juridiske enheder.  
6. I modulet **Program** skal du vælge det modul, du vil opdatere status for. Klik på **Vælg**.
7. På niveauet **Adgang** skal du markere **Alle**, **Ingen** eller en bestemt brugergruppe. Klik på **Vælg**. Alle angiver, at alle brugere med Rediger-adgang til modulet kan bogføre, hvis perioden er åben. Ingen angiver, at ingen brugere kan bogføre til modulet, hvis perioden er åben. En bestemt brugergruppe angiver, at kun brugere i gruppen kan bogføre til modulet, hvis perioden er åben.  
8. Vælg **Opdater**.
9. Vælg en anden periode, du vil opdatere status for.
10. Vælg de juridiske enheder, du vil opdatere periodestatus for.
11. Vælg **Opdater periodestatus**, og angiv status til **På hold**, **Åben** eller **Permanent lukket**. **Åben** angiver, at der kan bogføres til perioden, hvis brugeren har adgang. **På hold** betyder, at der ikke kan bogføres på perioden, men perioden kan genåbnes. **Permanent lukket** betyder, at perioden er lukket og ikke kan åbnes. Reguleringer kan ikke bogføres. Det anbefales ikke at indstille en periode til **Permanent lukket**, før alle reguleringer og revisioner er afsluttet.  
12. Vælg **Opdater**.

