---
title: Behandle afhentninger af kundeordre i POS
description: Dette emne forklarer den funktionalitet, der er tilgængelig i POS-programmet til behandling af afhentninger af kundeordrer.
author: Hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 598b155e1aa71cc7a23d1003331900604fb3de515381fd9c9987ed39bd9cbd2a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741056"
---
# <a name="process-customer-order-pickups-in-pos"></a>Behandle afhentninger af kundeordre i POS

[!include [banner](includes/banner.md)]

Når der oprettes en [kundeordre](customer-orders-overview.md) til afhentning af en butik, kan butiksbrugeren bruge POS-programmet til at starte afhentning af lageret. POS kører den endelige betalingsregistrering efter behov. Derefter fuldføres lageret og den økonomiske bogføring for de antal, der afhentes.

Hvis du er butiksbruger, kan du udføre afhentningen ved enten at bruge handlingen **Tilbagekald ordre** eller handlingen **Ordreopfyldning** i POS. Hvis du vil gøre **Afhent**-operationen tilgængelig, skal du først følge et af disse trin:

- Hvis du vil bruge handlingen **Tilbagekaldsordre**, skal du søge efter og vælge den ordre, der skal afhentes.
- Hvis du vil bruge operationen til **ordreopfyldning**, skal du søge efter og vælge en eller flere ordrelinjer.

Hvis den eller de valgte ordrelinjer ikke er konfigureret til afhentning i den pågældende butik, eller hvis ordren allerede er fuldt afhentet, vil operationen **Afhent** ikke være tilgængelig.

![Afhentningsoperation.](media/pickupoperation.png)

I Microsoft Dynamics 365 Commerce-version 10.0.17 og senere kan den **forbedrede brugeroplevelse af behandling af afhentningsordrer i POS** være aktiveret via Funktionsstyring i Commerce Headquarters. Hvis denne funktion er deaktiveret, kan brugerne ikke vælge afhentningsantal. Det samlede antal, der blev bestilt for linjen, er som standard det antal, der skal afhentes. Denne erfaring kan være problematisk, da brugerne glemmer at vælge nogle varer til afhentning, når de udfører afhentning via ordreopfyldning.

Den **forbedrede brugeroplevelse ved behandling af afhentningsordrer i POS** giver brugerne mere kontrol over valget af produkter, der skal afhentes, og antallet af de produkter, der skal afhentes. Brugerne behøver ikke at markere hver linje i salgsordren på ordreopfyldningssiden, før de vælger **Afhent**. Alle de varer, der kan afhentes, vises. Brugere kan angive flere linjer til afhentning, selvom der kun er valgt én produktlinje.

Når funktionen **Forbedring af brugeroplevelsen for behandling af afhentningsordre i POS** er aktiveret, og du vælger operationen **Afhent**, vises dialogboksen **Afhent**. Her kan du vælge de varer og antal, der skal afhentes. Som standard anses alle bestilte antal, der har lager i en afhentet eller pakket tilstand, for at være berettiget til afhentning. Dette antal angives som standard som afhentningsantallet. Du kan ændre det antal, der blev angivet, hvis antallet ikke er 0 (nul) og ikke overstiger det samlede åbne antal (dvs. ikke-faktureret) for den valgte linje.

![Dialogboksen Afhent.](media/pickupselect.png)

Når du har valgt de antal, der skal afhentes, og derefter vælger **Afhent**, vises posteringssiden. Hvis funktionen [omni-kanalbetalinger](omni-channel-payments.md) er aktiveret, og der er en fil med forhåndsgodkendte kreditkortbetalinger, skal du anvende betalingen.

På transaktionssiden beregner systemet de beløb, der er forfaldne, ved at beregne det samlede skyldige beløb for de valgte afhentningsvarer og derefter trække eventuelle tidligere anvendte indbetalinger eller godkendte kreditkortbetalinger fra. Du skal behandle betalingen for at fuldføre afhentningstransaktionen. Hvis [skærmlayout](pos-screen-layouts.md) for posteringssiden er konfigureret, så det omfatter operationen **Afslutning af postering**, og der ikke er noget forfaldent beløb, kan du fuldføre transaktionen uden at vælge en betalingsmåde. Hvis du ikke kan vælge **Afslut betaling**, kan du vælge **$0,00 forfaldent beløb** i ruden **Totaler** for at afslutte transaktionen uden at skulle vælge en betalingsmåde.

![Transaktionsside for en afhentningstransaktion for en kundeordre.](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Ændre afhentningslinjer eller -antal

Hvis du skal ændre afhentningsantallet, når du har valgt de varer, der skal afhentes, kan du vælge **Angiv antal**. Du kan ikke angive afhentningsantallet til **0** (nul) eller øge det til en værdi, der overstiger det ikke-fakturerede antal, der rester for den bestilte linje. Hvis du vil fjerne en afhentningslinje fra transaktionskurven, skal du vælge **Afmeld transaktion**. Den aktuelle postering stoppes, og bevægelsen til **Afhent**-operationen genstartes.

Hvis funktionen **Forbedring af brugeroplevelsen for behandling af afhentningsordre i POS** er aktiveret, kan organisationer tilføje en knap til handlingen **ændring af afhentningslinjer** til skærmlayoutet for posteringssiden. Når du har oprettet afhentningstransaktionsvognen på kasse og vælger varer, kan du vælge **Skift afhentningslinjer**, hvis du skal ændre afhentningsvarerne, men ikke ønsker at annullere hele transaktionen. I dialogboksen **Skift afhentningslinjer**, der vises, kan du ændre afhentningsvarerne og -mængderne. Transaktionsvognen opdateres derefter, så den afspejler dine ændringer.

![Dialogboksen Skift afhentningsvarer.](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]