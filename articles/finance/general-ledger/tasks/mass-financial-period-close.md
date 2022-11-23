---
title: Masseafslutning af regnskabsperiode
description: Denne artikel viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen.
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779804"
---
# <a name="mass-financial-period-close"></a>Masseafslutning af regnskabsperiode

[!include [banner](../../includes/banner.md)]

Denne artikel viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen. Desuden viser opgaven, hvordan du kan begrænse bogføring for en brugergruppe til bestemte moduler.

1. Gå til **Finans > Luk periode > Finanskalendere** i navigationsruden. 

>[!NOTE]
> Listen over juridiske enheder, der vises, afhænger af den regnskabskalender, der er valgt på siden. Kun juridiske enheder, der bruger den valgte regnskabskalender, vises.

2. Vælg **Rediger**.
3. Vælg den periode, du vil ændre status for.
4. Vælg de juridiske enheder, du vil opdatere status for. Du kan hurtigt markere alle de juridiske enheder ved at markere afkrydsningsfeltet i øverste venstre side af gitteret.  
5. Vælg **Opdater modul adgang** for at definere bogføringsadgang til et bestemt modul. Modulstatus kan også opdateres én efter én ved at redigere poster i gitteret. Knappen er nyttig, når du hurtigt vil opdatere flere poster for juridiske enheder.  
6. I modulet **Program** skal du vælge det modul, du vil opdatere status for. Klik på **Vælg**.
7. På niveauet **Adgang** skal du markere **Alle**, **Ingen** eller en bestemt brugergruppe. Klik på **Vælg**.  
- **Alle** - Alle brugere med Rediger-adgang til modulet kan bogføre, hvis perioden er åben. 
- **Ingen** - Brugere kan ikke bogføre til modulet, hvis perioden er åben. En bestemt brugergruppe angiver, at kun brugere i gruppen kan bogføre til modulet, hvis perioden er åben.  
8. Vælg **Opdater**. 
9. Vælg en anden periode, du vil opdatere status for.
10. Vælg de juridiske enheder, du vil opdatere periodestatus for.
11. Vælg **Opdater periodestatus**, og angiv status til **På hold**, **Åben** eller **Permanent lukket**. **Åben** angiver, at der kan bogføres til perioden, hvis brugeren har adgang. **På hold** betyder, at der ikke kan bogføres på perioden, men perioden kan genåbnes. **Permanent lukket** betyder, at perioden er lukket og ikke kan åbnes. Reguleringer kan ikke bogføres. Det anbefales ikke at indstille en periode til **Permanent lukket**, før alle reguleringer og revisioner er afsluttet.  
12. Vælg **Opdater**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
