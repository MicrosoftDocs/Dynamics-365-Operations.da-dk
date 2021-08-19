---
title: Produktet er på hold for transaktioner
description: Når du har autoriseret ordreforslag, modtager du en fejlmeddelelse om, at en vare er på hold for transaktioner.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752604"
---
# <a name="product-is-on-hold-for-transactions"></a>Produktet er på hold for transaktioner

Fejlkode: SYS13295

## <a name="symptoms"></a>Symptomer

Når du autoriserer ordreforslag, får du vist følgende fejlmeddelelse:

> Varen %1 er spærret for bevægelser i %2.

## <a name="cause"></a>Årsag

Når spærrede varer beskrives, bruger systemet begreberne *spærret*, *stoppet* og *på hold* som synonymer. Denne fejl betyder, at varen er angivet som **Stoppet** i standardordreindstillingerne.

Hvis en vare er spærret, og du føjer den til en indkøbsordre- eller salgsordrelinje, får du vist en advarsel. Når en vare er spærret, kan lagertransaktioner med relation til indkøbsordre- eller salgsordrelinjen ikke ændres, når du for eksempel bogfører en følgeseddel eller en faktura. Du kan spærre en købt vare og samtidigt sælge varen. I så fald er afkrydsningsfelt **Stoppet** markeret på en indkøbsordre, men varen er ikke spærret på lageret eller på en salgsordre.

Her er nogle af de betingelser, der kan medføre, at et varenummer spærres, så varen ikke kan sælges:

- Varen stadig er under udvikling eller i produktion. Du ønsker derfor ikke, at den sælges eller reserveres.
- Du har modtaget mange fejlbehæftede varer, og fejlene skal rettes, før varen kan sælges.

I den slags tilfælde kan du spærre varen, indtil problemerne er løst.

Hvis en vare er spærret, og du opretter en returordrelinje, modtager du en meddelelse. Du kan ikke spærre en vareserie eller et vareparti. Hvis dele af en vare skal spærres, kan du gøre det ved at flytte lagerbeholdning eller spærre hele beholdningen af varen i den pågældende periode.

## <a name="resolution"></a>Løsning

- Åbn siden **Standardindstillinger for ordre** for varen, og fjern markeringen i afkrydsningsfeltet **Stoppet**.
