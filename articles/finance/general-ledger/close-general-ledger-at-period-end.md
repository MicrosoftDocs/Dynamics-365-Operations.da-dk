---
title: Lukke Finans ved periodeafslutning
description: I dette emne beskrives de opgaver, der typisk udføres, når du udfører en lukning af periode til Finans.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eca533ed1621ec3507d8510f75842c0f0165275
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186733"
---
# <a name="close-the-general-ledger-at-period-end"></a>Lukke Finans ved periodeafslutning

[!include [banner](../includes/banner.md)]

I dette emne beskrives de opgaver, der typisk udføres, når du udfører en lukning af periode til Finans. 

I Finans kan du afslutte lukningsprocedurer for en periode eller et år. Lukningsprocesser forberede systemet på en ny periode. Når du skal forberede systemet på et nyt år, skal du køre årsafslutningsprocessen. Hver organisation har forskellige processer og trin, der udføres ved periodens udløb. Her er nogle valgfrie trin for periodeudløb:

-   Udfør alle opgaverne for alle andre moduler, som f.eks. Debitor, Kreditor og Lager.
-   Kontroller, at alle kladder bogføres.
-   Kør værdiregulering af udenlandsk valuta for at generere eventuelle ikke-realiserede tab eller gevinster.
-   Udlign posteringer for hver finanskonti.
-   Behandl alle nødvendige fordelinger.
-   Bogfør manuelt justeringer for periodeafslutningen.
-   Journaliser posteringer, og gennemse rapporten **Finanskladde**.
-   Konsolider ved hjælp af et koncernselskab eller økonomisk rapportering.
-   Generér regnskaber for periodeafslutningen ved hjælp af Økonomirapportering.
-   Angiv finansperioder til **På hold**, så der sker yderligere bogføring. Du kan også begrænse en periode til en bestemt brugergruppe, mens der pågår aktiviteter i periodeafslutningen, for at have bedre kontrol. Det er ikke en god ide at indstille perioder til **Permanent lukket**, fordi du ikke kan genåbne en periode, der er blevet lukket.

Den arbejdsområdet Afslutning på regnskabsperiode kan bruges til at organisere og spore de opgaver, der kræves til forskellige periodeafslutningsprocesser. 


Du kan finde flere oplysninger i følgende emner:
- [Arbejdsområde til afslutning på regnskabsperiode](financial-period-close-workspace.md) 
- [Årsafslutning](Year-end-close.md)  
- [Masseafslutning af regnskabsperiode](tasks/mass-financial-period-close.md)



