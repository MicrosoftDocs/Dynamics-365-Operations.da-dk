---
title: Konfigurere og behandle en udveksling på en returordre
description: Dette emne forklarer, hvordan du konfigurerer en udveksling på en returnering i Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758330"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Konfigurere og behandle en udveksling på en returordre

[!include [banner](includes/banner.md)]

I tidligere versioner af Dynamics 365 Commerce, blev returneringer ud fra kundeordrer behandlet ved hjælp af returordredokumentet i Headquarters. Returordredokumentet kan dog kun bruges til at behandle produkter, der returneres. De returnerede produkter er angivet med et negativt antal på returordrelinjer. Salg er derimod angivet med et positivt antal. Returordredokumentet understøtter dog ikke positive antal. På grund af denne begrænsning understøttede tidligere versioner af appen ikke scenarier, hvor produktudvekslinger udføres ved hjælp af returordredokumentet.

Der er imidlertid blevet tilføjet funktionalitet til understøttelse af scenarier, hvor udveksling udføres på returordrer. Commerce anvender nu salgsordredokumentet i stedet for returordredokumentet til behandling af disse typer transaktioner.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Konfigurere Commerce til at understøtte udvekslinger på returordrer

> [!NOTE]
> I Commerce version 10.0.20 og senere er en ny funktion kaldet "Samlet behandling af returneringer i POS" tilgængelig. Hvis du aktiverer denne funktion, kræves opsætningstrinnene nedenfor ikke. **Bearbejde returneringer som salgsordrer** bliver efterhånden som salgsordrer konfigureres permanent, og du ikke kan ændre dem.

Følg disse trin for at konfigurere systemet til at understøtte udvekslinger i returordrer, hvis du ikke har funktionen **Samlet returbehandling aktiveret i POS**.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre**. På oversigtspanelet **Kundeordrer** skal du angive indstillingen **Behandl returordrer som salgsordrer** til **Ja**.
2. Kør jobbet **Global konfiguration distributionsplan** (**1110**).

## <a name="make-an-exchange"></a>Foretag en udveksling.

Når systemet er konfigureret som beskrevet i den forrige sektion, vælger POS-brugeren stadig en salgsordre eller salgsfaktura for at behandle en returnering, som i tidligere versioner af appen. Men når returvarerne er føjet til indkøbsvognen, kan brugeren tilføje nye salgslinjer til indkøbsvognen.

For disse nye salgslinjer skal brugeren angive alle de attributter, der er nødvendige for at behandle en kundeordrelinje. Disse attributter omfatter leveringsmetode og opfyldelseslokation. Den betaling, der er forfalden for transaktionen, bliver en nettoværdi af returordrelinjer og salgsordrelinjer. Når betalingen udføres for transaktionen, bogføres returordren som et salgsordredokument i Headquarters, og systemet fakturerer med det samme returneringslinjerne.

For at give bedre indsigt i de forskellige beløb for indkøbsvognen er der blevet tilføjet tre nye beløbsfelter til indkøbsvognen. Du kan bruge skærmdesigneren for at gøre disse nye felter tilgængelige i POS-brugergrænsefladen (UI).

- **Anvendt depositum** – Det indbetalingsbeløb, der anvendes på en transaktion, når brugeren udfører en kundeordreafhentning. Hvis der ikke er nogen tilsidesættelse af indbetalt beløb, og et depositum på 10 procent er konfigureret, er beløbet i dette felt 90 procent af det samlede beløb for kundeordren.
- **Udførelsesbeløb** – Det samlede beløb for linjer, hvor leveringsmåden blev angivet til **Udfør**, da ordren blev oprettet eller redigeret, eller under en kundeordreudveksling. Beløbet i dette felt omfatter moms og gebyrer.
- **Returbeløb** – Det samlede beløb for linjer med negative antal under kundeordreudvekslingen. Beløbet i dette felt omfatter moms og gebyrer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
