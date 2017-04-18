---
title: "Kreditorbetalinger af et delvist beløb"
description: "Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Kreditorbetalinger af et delvist beløb

Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen. 

<a name="cash-discount-amounts"></a>Kasserabatbeløb
---------------------

En kreditor kan tilbyde dig en kasserabat, hvis du betaler en faktura før forfaldsdatoen. Du kan f.eks. en oprette en faktura på 100,00, der specificerer en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage. Forfaldsdatoen er 30 dage. Hvis et betalingsforslag bruger kasserabatten som et kriterium for at vælge en faktura, og hvis forslaget køres på eller før datoen for kasserabat, fakturaen er udvalgt til betaling, og der oprettes betalingen til 98,00. En kasserabat kan også tages en engangs betaling, der er oprettet manuelt.

## <a name="partial-payments-with-cash-discounts"></a>Delvise betalinger med kasserabatter
Når du foretager en delvis betaling, har du måske til hensigt at foretage en yderligere delbetaling, så fakturaen udlignes helt. For at tage en kasserabat for en delbetaling, skal du angive den ** beregne kasserabatter for delbetalinger ** indstilling til **Ja** på den **konto Kreditorparametre** side. 

Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du foretager en betaling på 49,00 inden for 10 dage, kan du angive en debitering på 49,00 i en betalingskladde. Når du udligner den delvise indbetaling på den **udligne åbne posteringer** side, **1.00** vises i den **kasserabatbeløbet at tage** felt. 

> [!NOTE] 
> Hvis du indtaster en delbetaling, og lader det fulde fakturabeløb i den **udligningsbeløbet** felt, den **kasserabatbeløbet at tage** beregnes automatisk, når du bogfører posteringer.

## <a name="credit-notes-with-cash-discounts"></a>Kreditnotaer med kasserabatter
Du kan evt. returnere nogle af varerne på en faktura, hvorefter du modtager en kreditnota. Hvis der tidligere er medtaget en kasserabat på en original faktura, kan du fratrække værdien af rabatten og modtage en refundering på det rigtige beløb. Hvis den ** beregne kasserabatter for kreditnotaer ** indstilling er angivet til **Ja** på den **konti Kreditorparametre** side, rabatten beregnes automatisk for kreditnotaen. 

Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du returnerer varerne, og du modtager en kreditnota, kan du indtaste kreditnotaen for det fulde beløb for den oprindelige faktura 100,00 samt 2 procent kasserabatten, der er også defineret i kreditnotaen.  Når du får vist en kreditnota på det **udligne posteringer** siden **98,00** vises i den **udligningsbeløbet** felt, og **-2.00** vises i den **kasserabatbeløbet** felt. Rabatbeløbet bogføres på en kasserabatkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetaling/underbetalingsbeløb
Du foretager eventuelt en delbetaling, hvor beløbet, der stadig skal udlignes, er meget lille. For eksempel er kreditorfakturaen for 1.000,00, og du betaler 999.90. Hvis det resterende beløb er mindre end det beløb, der er angiver for over- eller underbetalinger på siden **Kreditorparametre**, bogføres differencen automatisk på en overbetalings/underbetalingsfinanskonto.

