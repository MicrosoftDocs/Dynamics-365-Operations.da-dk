---
title: Ydeevne for momsberegning påvirker transaktioner
description: Dette emne indeholder fejlfindingsoplysninger, der vedrører momsberegningens ydeevne og indvirkning på transaktioner.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947617"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Ydeevne for momsberegning påvirker transaktioner

[!include [banner](../includes/banner.md)]

Nogle gange påvirkes en transaktion af de problemer med ydeevnen, der er i momsberegningen. Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.

## <a name="review-the-transaction-line-count"></a>Gennemse transaktionslinjeantallet

Afgør, om transaktionen indeholder et stort antal linjer (f.eks. mere end flere hundreder). Hvis det ikke er tilfældet, skal du gå videre til næste afsnit. Hvis transaktionen ikke indeholder flere hundrede linjer, skal du udskyde momsberegningen. Du kan finde flere oplysninger i [Aktivere forsinket momsberegning for kladder](enable-delayed-tax-calculation.md). 

Derefter kan du afgøre, om nogen af følgende forhold er aktuelle:

- Der er importtransaktioner fra store filer.
- Flere sessioner behandler samme momsberegning for transaktionen samtidigt.
- Transaktionen har flere linjer, og visningerne opdateres i realtid. Feltet **Beregnet momsbeløb** på siden **Finanskladde** opdateres f.eks. i realtid, når en linjes felter bliver ændret.

   [![Feltet Beregnet momsbeløb på kladdens bilagsside](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Hvis nogen af disse forhold er til stede, skal du udskyde momsberegningen.

## <a name="review-the-call-stack"></a>Gennemse kaldstakken

Gennemse kaldstakken for at finde ud af, om momsberegningen er kaldt flere gange. Hvis det ikke er tilfældet, skal du gå videre til næste afsnit. Hvis kaldstakken er kaldt flere gange, skal du benytte følgende fremgangsmåde for at reducere momsberegningstiderne.

1. Hvis kladden har taget højde for transaktionen, skal du udskyde momsberegningen. Du kan finde flere oplysninger i [Aktivere forsinket momsberegning for kladder](enable-delayed-tax-calculation.md).
2. Hvis transaktionen er en indkøbsordre, og programversionen er senere end 10.0.15, kan du udskyde momsberegningen indtil den endelige beregning ved at aktivere flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Gennemse kaldstakkens tidslinje

Gennemse kaldstakkens tidslinje for at finde ud af, om der findes følgende problemer. Hvis det er tilfældet, skal du aktivere flighting for **TaxUncommittedDoIsolateScopeFlighting** for at rette problemet.

- Transaktionen bevirker, at systemet holder op med at svare, indtil sessionen er afsluttet. Derfor kan transaktionen ikke beregne momsresultatet. I følgende illustration vises meddelelsen "Session afsluttet", som du modtager.

    [![Meddelelsen Session afsluttet](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Metoderne for **TaxUncommitted** tager længere tid end andre metoder. I følgende illustration tager metoden **TaxUncommitted::updateTaxUncommitted()** f.eks. 43.347,42 sekunder, mens andre metoder tager 0,09 sekunder.

    [![Metodevarigheder](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Tilpasning og kald af momsberegning

Når du tilpasser, må du ikke kalde momsberegningen ved metoden **insert()** eller **update()** for hver linje. Momsberegning skal kaldes på transaktionsniveau.

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger

Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
