---
title: Kreditorbetalinger af et delvist beløb
description: Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deb150e35a80cc4c49f46dfc55822625db83cbda
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715372"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Kreditorbetalinger af et delvist beløb

[!include [banner](../includes/banner.md)]

Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen. 

## <a name="cash-discount-amounts"></a>Kasserabatbeløb

En kreditor kan tilbyde dig en kasserabat, hvis du betaler en faktura før forfaldsdatoen. Du kan f.eks. en oprette en faktura på 100,00, der specificerer en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage. Forfaldsdatoen er 30 dage. Hvis et betalingsforslag bruger kasserabatten som et kriterium for at vælge en faktura, og hvis forslaget køres på eller før datoen for kasserabat, udvælges fakturaen til betaling, og der oprettes betalingen af 98,00. En kasserabat kan også tages fra en engangsbetaling, der er oprettet manuelt.

## <a name="partial-payments-with-cash-discounts"></a>Delvise betalinger med kasserabatter
Når du foretager en delvis betaling, har du måske til hensigt at foretage en yderligere delbetaling, så fakturaen udlignes helt. For at medtage en kasserabat for en delbetaling skal du angive indstillingen **Beregn kasserabatter for delvise betalinger** til **Ja** på siden **Kreditorparametre**. 

Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du foretager en betaling på 49,00 inden for 10 dage, angiver du en debitering på 49,00 i en betalingskladde. Når du udligner den delvise betaling på siden **Udlign åbne posteringer**, vises **1,00** i feltet **Kasserabatbeløb, der skal medtages**. 

> [!NOTE] 
> Hvis du indtaster en delvis betaling og lader det fulde fakturabeløb stå i feltet **Beløb, der skal udlignes** beregnes feltet **Kasserabatbeløb, der skal medtages** automatisk, når posteringerne bogføres.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnotaer med kasserabatter
Du kan evt. returnere nogle af varerne på en faktura, hvorefter du modtager en kreditnota. Hvis der tidligere er medtaget en kasserabat på en original faktura, kan du fratrække værdien af rabatten og modtage en refundering på det rigtige beløb. Hvis indstillingen **Beregn kasserabatter for kreditnotaer** er angivet til **Ja** på siden **Kreditorparametre**, beregnes rabatten automatisk for kreditnotaen. 

Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du returnerer varerne, og du modtager en kreditnota, kan du indtaste kreditnotaen for det fulde beløb for den oprindelige faktura 100,00 sammen med de 2 procent kasserabat, der er også defineret i kreditnotaen.  Når du ser en kreditnota på siden **Udlign transaktioner**, vises **98,00** i feltet **Beløb, der skal udlignes**, og **-2,00** vises i feltet **Kasserabatbeløb**. Rabatbeløbet bogføres på en kasserabatkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetaling/underbetalingsbeløb
Du foretager eventuelt en delbetaling, hvor beløbet, der stadig skal udlignes, er meget lille. For eksempel er kreditorfakturaen for 1.000,00, og du betaler 999.90. Hvis det resterende beløb er mindre end det beløb, der er angiver for over- eller underbetalinger på siden **Kreditorparametre**, bogføres differencen automatisk på en overbetalings/underbetalingsfinanskonto.


Du kan finde flere oplysninger i [Oversigt over kreditorbetalinger](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
