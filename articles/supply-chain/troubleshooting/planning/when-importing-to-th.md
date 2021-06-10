---
title: Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer
description: Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049458"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Du bliver bedt om at gemme indstillinger for varedisponering, selvom du ikke har foretaget nogen ændringer

KB-nummer: 4615588

## <a name="symptoms"></a>Symptomer

I nogle scenarier kan du få vist følgende meddelelse, når du åbner siden **Varedisponering**, efter du har importeret varer via objektet *Varedisponering V2*:

> Vil du gemme dine ændringer, før der lukkes?

Du modtager denne meddelelse, selvom du ikke har foretaget nogen ændringer.

## <a name="resolution"></a>Løsning

Siden **Varedisponering** indeholder kompleks standardlogik, der kan medføre, at meddelelsen vises, når der for nylig er foretaget direkte ændringer i databasen, f.eks. via import af objekt. `AREGENERALSETTINGSOVERRIDDEN`-objektfeltet er f.eks. angivet til *Nej*, men du kan importere en fil, der indeholder nye eller ændrede værdier for felter, f.eks. `PRODUCTCOVERAGEGROUPID` og/eller `VENDORACCOUNTNUMBER`. Da `AREGENERALSETTINGSOVERRIDDEN`-feltet er angivet til *Nej*, fjernes værdierne i dette tilfælde automatisk fra felterne, når du åbner siden **Varedisponering** første gang efter importen. Hvis du gemmer ændringerne, som meddelelsesfeltet beder om, gemmes de i databasen. Ellers modtager du den samme meddelelse, næste gang du åbner siden.

Hvis du vil forhindre denne funktionsmåde, men også medtage værdier for felter, f.eks. `PRODUCTCOVERAGEGROUPID` via import af objekter, skal du angive `AREGENERALSETTINGSOVERRIDDEN` til *Ja*, når du importerer.
