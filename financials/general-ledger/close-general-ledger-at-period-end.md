---
title: Lukke Finans ved periodeafslutning
description: "I dette emne beskrives de opgaver, der typisk udføres, når du udfører en lukning af periode til Finans."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 81d687cc16ef43442c8c1c166cc6f0d8b171e28f
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Lukke Finans ved periodeafslutning

[!include[banner](../includes/banner.md)]


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

Den arbejdsområdet Afslutning på regnskabsperiode kan bruges til at organisere og spore de opgaver, der kræves til forskellige periodeafslutningsprocesser. Du kan finde flere oplysninger i emnerne [Arbejdsområde til afslutning på regnskabsperiode](financial-period-close-workspace.md) og [Årsafslutning](Year-end-close.md). 






