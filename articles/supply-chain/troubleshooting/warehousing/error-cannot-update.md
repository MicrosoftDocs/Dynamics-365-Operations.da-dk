---
title: Der opstår en fejl, når lokationen vælges under registrering af pluklisten
description: Der opstår en fejl, når lokationen vælges under registrering af pluklisten.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026355"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Der opstår en fejl, når lokationen vælges under registrering af pluklisten

KB-nummer: 4613106

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når systemet er konfigureret til automatisk at reservere salgsordrer. Hvis du prøver at vælge lokationen for en pluklisteregistreringslinje, modtager du følgende fejlmeddelelse, når du bruger reservationsprocesser i lokationsstyring (WMS):

> Antallet kan ikke opdateres med nye dimensioner

Denne fejl kan forekomme, fordi du ikke har tilstrækkelig lagerbeholdning på en angivet lokation.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet.

Hvis du f.eks. bruger reservationsprocessen på lagerstedsniveau, anbefales det, at du bruger den manuelle reservationsproces fra pluklinjen, hvis beholdningen på en bestemt lokation ikke er tilstrækkelig, og der ikke reserveres nok på alle lagerdimensionsniveauer. Du kan derefter bruge funktionen *Reserver parti* til at fordele de lavere reservationer, f.eks. lokation, til alle tilgængelige disponible lagerbeholdninger.
