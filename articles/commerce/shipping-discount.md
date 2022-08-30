---
title: Forsendelsesrabat
description: Denne artikel beskriver egenskaberne for forsendelsesrabat i Microsoft Dynamics 365 Commerce og den opsætning, der kræves for at bruge dem.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346385"
---
# <a name="shipping-discount"></a>Forsendelsesrabat

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver egenskaberne for forsendelsesrabat i Microsoft Dynamics 365 Commerce og den opsætning, der kræves for at bruge dem.

Gratis eller rabatteret forsendelse er en faktor, der påvirker kundernes købsbeslutninger online. Mange detailforretninger bruger en fordel ved gratis forsendelse til at få kunderne til at øge deres indkøbsvognsstørrelse for at øge indtjeningen pr. transaktion.

Handel understøtter en forsendelsesrabatfunktionalitet, der giver detailforretningerne mulighed for at konfigurere en rabatprocent på forsendelsesgebyrer for en bestemt forsendelsesmetode, når det samlede salgsbeløb for kvalificerede varer i transaktionen opfylder bestemte kriterier. Et eksempel på et scenarie, der bruger forsendelsesrabatfunktionaliteten, er "Brug $50 eller mere til at få gratis forsendelse i løbet af natten".

## <a name="prerequisites"></a>Forudsætninger

Forsendelsesrabatfunktionaliteten understøttes af Commerce's [omnikanal-avancerede automatiske gebyr](/dynamics365/unified-operations/retail/omni-auto-charges)-funktioner. Hvis forsendelsesrabatfunktionaliteten skal fungere, skal du aktivere konfigurationen **Brug avancerede auto-gebyrkonfiguration** under fanen **Debitorordrer** på siden **Commerce-parametre** i Commerce Headquarters. Detailhandlende kan bruge funktionen til avancerede automatiske gebyrer til at konfigurere forskellige typer gebyrer, f.eks. håndtering, installation og afhændelse.

Forsendelsesrabatterne anvendes kun på forsendelsesgebyrerne. Derfor skal en detail forhandler angive, hvilke gebyrer der er forsendelsesgebyrer. Hvis du vil angive forsendelsesgebyrer i Commerce headquarters, skal du gå til **Kanalopsætning \> Gebyrer \> Gebyrkode** og angive **Forsendelsesgebyr** til **Ja** for de ønskede gebyrer.

![Angivelse af et gebyr som forsendelsesgebyr.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfiguration

Forsendelsesrabatfunktionaliteten er lagbaseret og understøtter kun beregningstypen **Procentdel** rabat. Hvis du vil konfigurere en forsendelsesrabat i Commerce headquarters, skal du gå til **Priser og rabatter \> Rabat for forsendelsestærskel**. Du kan derefter angive den leveringsmåde, som rabatten gælder for, definere en eller flere beløbsgrænser og angive rabatprocenten for hver grænse. Du kan også konfigurere en liste over kategorier eller produkter som kvalificerede varer. På den måde er det kun salgsbeløbet i forhold til disse varer i en transaktion, der tæller, når prissætningsprogrammet evaluerer, om totalen for transaktionen opfylder grænsen.

> [!NOTE]
> I modsætning til andre rabattyper opretter forsendelsesrabatten ikke rabatlinjer. Den redigerer i stedet forsendelsesgebyret direkte og tilføjer navnet på rabatten i beskrivelsen af tillægget.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
