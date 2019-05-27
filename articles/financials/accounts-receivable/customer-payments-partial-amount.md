---
title: Debitorbetalinger af et delvist beløb
description: Kunder vil nogle gange indbetale et beløb, der er mindre end beløbet på en faktura. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymEntry
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 510fda7bf35e459e0da5595b083e041bb708c873
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556313"
---
# <a name="customer-payments-for-a-partial-amount"></a>Debitorbetalinger af et delvist beløb

[!include [banner](../includes/banner.md)]

Kunder vil nogle gange indbetale et beløb, der er mindre end beløbet på en faktura. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation. De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen.

<a name="partial-payment-with-no-discount"></a>Delvis betaling uden rabat
--------------------------------

Kunder kan eventuelt foretage en delvis betaling, hvis ikke har nok kontanter til at betale fakturaen i sin helhed, eller hvis der er en tvist om en vare på fakturaen. I denne situation kan fakturaen delvist udlignes med betalingen. Fakturaen forbliver åben og viser en saldo.

## <a name="discount-amounts"></a>Rabatbeløb
Du kan tilbyde kunderne en kasserabat, hvis de betaler en faktura før forfaldsdatoen. Du kan f.eks. en oprette en faktura på 100,00, der specificerer en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage. Forfaldsdatoen er 30 dage. Hvis du modtager en betaling på 98,00 inden for 10 dage, indtaster du betalingen på 98,00. Derefter, når fakturaen er markeret til udligning, medtages kasserabatten automatisk.

## <a name="partial-payments-with-cash-discounts"></a>Delvise betalinger med kasserabatter
Når kunder foretager en delvis betaling, har de måske til hensigt at foretage en yderligere delbetaling, så fakturaen udlignes helt. For at medtage en kasserabat for en delbetaling skal du angive indstillingen **Beregn kasserabatter for delvise betalinger** til **Ja** på siden **Debitorparametre**. 

Du tilbyder f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. Der er bogført en faktura på 100,00. Hvis du modtager en betaling på 49,00 inden for 10 dage, skal du angive en kredit på 49,00 i en betalingskladde. Når du udligner den delvise betaling på siden **Udlign posteringer**, vises **1,00** i feltet **Kasserabatbeløb, der skal medtages**. Rabatbeløbet bogføres på en kasserabatkonto. 

> [!NOTE] 
> Hvis du indtaster en delvis betaling og lader det fulde fakturabeløb stå i feltet **Beløb, der skal udlignes** beregnes feltet **Kasserabatbeløb, der skal medtages** automatisk, når posteringerne bogføres.

## <a name="credit-notes-with-discounts"></a>Kreditnotaer med rabat
Hvis kunder returnerer nogle af varerne på en faktura, kan du eventuelt udstede en kreditnota. Hvis en kasserabat blev medtaget på den oprindelige faktura, bør kreditnotaen til kunden være netto for kasserabatten, kunden fik. Hvis indstillingen **Beregn kasserabatter for kreditnotaer** er angivet til **Ja** på siden **Debitorparametre**, beregnes rabatten automatisk for kreditnotaen. 

Du tilbød f.eks. betalingsbetingelser, der specificerer en rabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt. En faktura på 100,00 er bogført, og kunden fik en kasserabat. Hvis kunden returnerer varerne, og du udsteder en kreditnota, kan du indtaste kreditnotaen på -100.00. Når du ser en kreditnota på siden **Udlign åbne posteringer**, vises **98,00** i feltet **Beløb, der skal udlignes**, og **-2.00** vises i feltet **Kasserabatbeløb**. Rabatbeløbet bogføres på en kasserabatkonto.

## <a name="overpaymentunderpayment-amounts"></a>Overbetaling/underbetalingsbeløb
Når kunderne foretager en betaling, kan der være et meget lille beløb, der skal stadig udlignes. Du fakturerer f.eks. kunden for 1.000,00, og kunden betaler 999,90. Hvis det resterende beløb er mindre end det beløb, der er angiver for over- eller underbetalinger på siden **Debitorparametre**, bogføres differencen automatisk på en overbetalings/underbetalingsfinanskonto.

## <a name="full-settlement"></a>Fuld udligning
Kunder kan foretage en delvis betaling, hvor det resterende beløb ikke betales, men er større end det underbetalingsbeløb,, der er angivet på siden **konto Kreditorparametre**. Hvis du vil markere fakturaen som fuldt udlignet, kan du bruge indstillingen **Fuld udligning** på siden **Udlign transaktioner**. (Du kan aktivere funktionen Fuld udligning ved hjælp af en konfigurationsnøgle.) En faktura er f.eks. bogført en faktura på 1.000,00, og kunden foretager en betaling på 990,00. Du har aftalt, at kunden ikke skal betale de resterende 10,00. Når du har markeret fakturaen til udligning, du kan også markere **Fuld udligning**. Fakturaen vil derefter blive betragtet som fuldt udlignet. Differencen på 10,00 bogføres på en kasserabatkonto som et ekstra kasserabatbeløb.


Du kan finde flere oplysninger i [Deponere debitorbetalinger](tasks/deposit-customer-payments.md).
