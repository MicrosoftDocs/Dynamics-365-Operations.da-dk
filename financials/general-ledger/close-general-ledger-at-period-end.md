---
title: Lukke Finans ved periodeafslutning
description: "Dette emne beskriver de opgaver, der udføres typisk, når du udfører en lukke periode til Finans."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a7b72dfa98758b14d303d09890bd46729b1cdbe9
ms.lasthandoff: 03/31/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Lukke Finans ved periodeafslutning

Dette emne beskriver de opgaver, der udføres typisk, når du udfører en lukke periode til Finans. 

I Finans kan du afslutte lukningsprocedurer for en periode eller et år. Lukningsprocesser forberede systemet på en ny periode. For at forberede systemet til et nyt år, skal du køre processen år end tæt. Hver organisation har forskellige processer og trin, der udføres i slutningen af en periode. Her er nogle valgfrie trin for slutter:

-   Udfør alle opgaverne for alle andre moduler, som f.eks. Debitor, Kreditor og Lager.
-   Kontroller, at alle kladder bogføres.
-   Kør værdiregulering af udenlandsk valuta for at generere eventuelle ikke-realiserede tab eller gevinster.
-   Udlign posteringer for hver finanskonti.
-   Behandl alle nødvendige fordelinger.
-   Bogfør manuelt justeringer for periodeafslutningen.
-   Journaliser posteringer, og gennemse rapporten **Finanskladde**.
-   Konsolider ved hjælp af et koncernselskab eller økonomisk rapportering.
-   Generér regnskaber for periodeafslutningen ved hjælp af Økonomirapportering.
-   Angiv finansperioder til **På hold**, så der sker yderligere bogføring. Du kan også begrænse en periode til en bestemt brugergruppe, mens der pågår aktiviteter i periodeafslutningen, for at have bedre kontrol. Det er ikke en god ide at indstille perioder til **permanent lukket**, fordi du ikke kan genåbne en periode, der er blevet lukket.

Den finansielle periode Luk arbejdsområde kan bruges til at organisere og holde styr på de opgaver, der kræves til forskellige Periodeslutning processer. Henviser til den [økonomiske periode Luk arbejdsområde](financial-period-close-workspace.md) og [årets slutning tæt](Year-end-close.md) emner for at få yderligere oplysninger. 




