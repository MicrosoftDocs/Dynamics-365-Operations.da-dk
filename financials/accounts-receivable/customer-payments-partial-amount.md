---
title: "Debitorbetalinger af et delvist beløb"
description: "Kunder vil nogle gange indbetale et beløb, der er mindre end beløbet på en faktura. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 7025072cd29aac4ceb13b5594c3e321350777cf1
ms.lasthandoff: 03/31/2017


---

# <a name="customer-payments-for-a-partial-amount"></a>Debitorbetalinger af et delvist beløb

Kunder vil nogle gange indbetale et beløb, der er mindre end beløbet på en faktura. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen.

<a name="partial-payment-with-no-discount"></a>Delvis betaling uden rabat
--------------------------------

Kunder kan eventuelt foretage en delvis betaling, hvis ikke har nok kontanter til at betale fakturaen i sin helhed, eller hvis der er en tvist om en vare på fakturaen. I denne situation kan fakturaen delvist udlignes med betalingen. Fakturaen forbliver åben og viser en saldo.

## <a name="discount-amounts"></a>Rabatbeløb
Du kan tilbyde kunderne en kasserabat, hvis de betaler en faktura før forfaldsdatoen. Du kan f.eks. en oprette en faktura på 100,00, der specificerer en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage. Forfaldsdatoen er 30 dage. Hvis du modtager en betaling på 98,00 inden for 10 dage, indtaster du betalingen på 98,00. Derefter, når fakturaen er markeret til udligning, medtages kasserabatten automatisk.

## <a name="partial-payments-with-cash-discounts"></a>Delvise betalinger med kasserabatter
Når kunder foretager en delvis betaling, har de måske til hensigt at foretage en yderligere delbetaling, så fakturaen udlignes helt. For at tage en kasserabat for en delbetaling, skal du angive den ** beregne kasserabatter for delbetalinger ** indstilling til **Ja** på den **Accounts receivable parameters** side. 

Du tilbyder f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du modtager en betaling på 49,00 inden for 10 dage, skal du angive en kredit på 49,00 i en betalingskladde. Når du udligner den delvise betaling på siden **Udlign posteringer**, vises **1,00** i feltet **Kasserabatbeløb, der skal medtages**. Rabatbeløbet bogføres på en kasserabatkonto. 

> [!NOTE] 
> Hvis du indtaster en delbetaling, og lader det fulde fakturabeløb i den **udligningsbeløbet** felt, den **kasserabatbeløbet at tage** beregnes automatisk, når du bogfører posteringer.

## <a name="credit-notes-with-discounts"></a>Kreditnotaer med rabat
Hvis kunder returnerer nogle af varerne på en faktura, kan du eventuelt udstede en kreditnota. Hvis en kasserabat blev medtaget på den oprindelige faktura, bør kreditnotaen til kunden være netto for kasserabatten, kunden fik. Hvis indstillingen **Beregn kasserabatter for kreditnotaer** er angivet til **Ja** på siden **Debitorparametre**, beregnes rabatten automatisk for kreditnotaen. 

Du tilbød f.eks. betalingsbetingelser, der specificerer en rabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. En faktura på 100,00 er bogført, og kunden fik en kasserabat. Hvis kunden returnerer varerne, og du udsteder en kreditnota, kan du indtaste kreditnotaen på -100.00. Når du ser en kreditnota på siden **Udlign åbne posteringer**, vises** 98,00** i feltet **Beløb, der skal udlignes**, og **-2.00** vises i feltet **Kasserabatbeløb**. Rabatbeløbet bogføres på en kasserabatkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetaling/underbetalingsbeløb
Når kunderne foretager en betaling, kan der være et meget lille beløb, der skal stadig udlignes. Du fakturerer f.eks. kunden for 1.000,00, og kunden betaler 999,90. Hvis det resterende beløb er mindre end det beløb, der er angiver for over- eller underbetalinger på siden** Debitorparametre**, bogføres differencen automatisk på en overbetalings/underbetalingsfinanskonto.

## <a name="full-settlement"></a>Fuld udligning
Kunder kan foretage en delvis betaling, hvor det resterende beløb ikke betales, men er større end det underbetalingsbeløb,, der er angivet på den **konto Kreditorparametre** side. Hvis du vil markere fakturaen som fuldt udlignet, kan du bruge den **fuld udligning** indstilling på den **udligner transaktion** side. (Du kan aktivere funktionen Fuld udligning ved hjælp af en konfigurationsnøgle.) En faktura er f.eks. bogført en faktura på 1.000,00, og kunden foretager en betaling på 990,00. Du har aftalt, at kunden ikke har til at betale de resterende 10,00. Når du har markeret fakturaen til udligning, du kan også markere Vælg **fuld udligning**. Fakturaen vil derefter blive betragtet som fuldt udlignet. Differencen på 10,00 bogføres på en kasserabatkonto som et ekstra kasserabatbeløb.

