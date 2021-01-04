---
title: Udligningsoversigt
description: Dette emne indeholder generelle oplysninger om udligningsprocessen. Det beskriver, hvilke posteringstyper der kan udlignes, samt timingen og processen for at udligne dem. Det beskriver også resultaterne af udligningsprocessen.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 650b0ef0123cf9acf42c2e7460693b555897744f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441547"
---
# <a name="settlement-overview"></a>Udligningsoversigt

[!include [banner](../includes/banner.md)]

Dette emne indeholder generelle oplysninger om udligningsprocessen. Det beskriver, hvilke posteringstyper der kan udlignes, samt timingen og processen for at udligne dem. Det beskriver også resultaterne af udligningsprocessen.

I udligningsprocessen udlignes posteringerne på et enkelt dokument med transaktionerne i et andet dokument for at øge eller reducere saldoen for hvert dokument. En betaling kan f.eks. udlignes med en faktura. Forskellige posteringstyper kan udlignes, på forskellige tidspunkter, og via forskellige metoder. Udligningsprocessen kan også generere nye posteringer.

## <a name="what-transactions-can-be-settled"></a>Hvilke posteringer kan udlignes

I Kreditor og Debitor kan udligning forekomme mellem de posteringstyper, der påvirker kreditorsaldoen eller debitorsaldoen. Disse posteringstyper kan omfatte fakturaer, betalinger, kreditnotaer og gebyrer. Alle posteringstyper kan udlignes med en anden transaktionstype. Du kan f.eks. udligne en betaling med en faktura, en kreditnota med en faktura, en faktura med en anden faktura og betaling med en anden betaling.

Du kan udligne betalinger med en postering i samme juridiske enhed eller i en anden juridisk enhed. I organisationer, der anvender en centraliseret betalingsmodel, kan [centraliserede betalinger](set-up-centralized-payments.md) hjælpe med at strømline betalingsprocessen.

## <a name="when-to-settle-transactions"></a>Hvornår posteringer skal udlignes

Posteringer kan udlignes, når der angives betalinger. Når du f.eks. foretager en betaling til en kreditor, vælger du typisk, hvilke fakturaer der skal betales. Når du vælger fakturaer, markerer du dem til udligning mod betalingen. Når Debitor-medarbejdere registrerer kundebetalinger, kan de markere de relevante fakturaer til udligning baseret på de oplysninger, der er inkluderet i hver enkelt debitors betaling. Du kan bruge **Udlign transaktioner** til at markere posteringer til udligning. Du kan åbne denne side fra enhver ikke-bogført faktura eller betaling. Når transaktionen bogføres, bogføres udligningen også. 

Posteringer kan også udlignes, efter de er bogført. Du kan angive og bogføre en debitorbetaling uden at udligne den med en faktura. Du kan evt. sikre dig, at betalingen udlignes med den korrekte faktura, før du posterer udligningen. Siden **Udlign transaktioner** kan åbnes fra siden **Alle kunder** eller **Alle leverandører** eller fra siden **Transaktioner** for en debitor eller kreditor.

Du kan også tilbageføre bogførte forudbetalinger for en faktura ved at markere betalingen for udligning med en købsordre eller salgsordre. I dette tilfælde har betalingen fortsat en åben saldo, men den kan ikke udlignes mod en anden faktura. Betalingen udlignes automatisk mod den faktura, der oprettes ud fra indkøbsordren eller salgsordren.

## <a name="how-to-settle-transactions"></a>Hvordan posteringer skal udlignes

Posteringer kan udlignes manuelt, automatisk eller via en kombination af de to metoder. Valget af en udligningsmetode afhænger af dine forretningsprocesser. På siderne **Kreditorparametre** og **Debitorparametre** kan du konfigurere udligningsprocessen, så den er justeret i forhold til disse forretningsprocesser.

Du kan oprette kreditorbetalinger og direkte debitorbetalinger for kunder ved hjælp af et betalingsforslag. Et betalingsforslag bruges til at vælge fakturaer, der skal betales. Betalingsforslaget startes manuelt, og derefter markerer systemet automatisk de valgte fakturaer til udligning, når betalingerne oprettes.

Hvis betalingerne oprettes manuelt, kan du bruge siden **Udlign transaktioner** til at vælge fakturaer til udligning. Du kan manuelt vælge fakturaerne, eller du kan bruge indstillingen **Markér efter prioritet**, så fakturaer automatisk markeres til udligning. Indstillingen **Markér efter prioritet** er kun tilgængelig for Debitor. Du kan aktivere denne indstilling på fanen **Udligningsprioritet** på siden **Debitorparametre**.

Hvis en betalingsmedarbejder indtaster en betaling, men ikke udligner betalingen, før den er bogført, kan betalingen udlignes automatisk. Du kan slå automatisk udligning til på siderne **Debitorparametre** og **Kreditorparametre**. Automatisk udligning udligner kun posteringer i den samme juridiske enhed. Den udligner ikke posteringer på tværs af flere juridiske enheder.

Når du bruger automatisk udligning, kan du bruge den foruddefinerede udligningsprioritet, eller du kan definere dine egen udligningsprioritet på siden **Debitorparametre**. Denne funktionalitet er kun tilgængelig for Debitor.

## <a name="results-of-settlement"></a>Resultater af udligning

Når posteringer udlignes, øges eller mindskes den udestående saldo for hver postering efter behov. Normalt, når en faktura og betaling udlignes, opdateres status og saldoen for hver transaktion efter følgende regler:

- Hvis betalingsbeløbet er større end fakturabeløbet, reduceres fakturasaldoen til 0,00, og fakturaen lukkes. Betalingen forbliver åben, og saldoen er forskellen mellem betalingsbeløbet og fakturabeløbet.
- Hvis betalingsbeløbet er mindre end fakturabeløbet, reduceres betalingssaldoen til 0,00, og betalingen lukkes. Fakturaen forbliver åben, og saldoen er forskellen mellem fakturabeløbet og betalingsbeløbet.
- Hvis betalingsbeløbet er lig med fakturabeløbet, lukkes både betalingen og fakturaen, og saldoen for begge er reduceret til 0,00.

Hvis [betalingsbeløbet er mindre end fakturabeløbet](../accounts-payable/vendor-payments-partial-amount.md) på grund af en kasserabat, afskrivning eller underbetaling, lukkes fakturaen og betalingen måske alligevel, afhængigt af, hvordan udligninger er konfigureret på siderne **Kreditorparametre** og **Debitorparametre**.

Udligninger kan også generere posteringer. Udligning af en faktura og betaling kan for eksempel medføre en kasserabat, realiseret gevinst eller tab, momsreguleringer, afskrivninger eller øredifferencer.

## <a name="identifying-marked-transactions-during-settlement"></a>Identificere markerede posteringer under udligning

Når du forsøger at udligne en postering, kan du bemærke et symbol, der angiver, at posteringen er markeret et andet sted. I dette tilfælde kan du vælge posteringen på siden **Udlign posteringer** og derefter vælge **Forespørgsel \> Udligning** i udligningsvinduet. Visningen for denne forespørgsel viser kladder, salgsordrer, fakturaer, betalingsforslag og debitorlokationer, der muligvis blokerer posteringen i at blive udlignet. Hvis du vil løse dette problem, kan du vælge linket for at gå direkte fra forespørgslen til den blokerede lokation. Du kan derefter opdatere dokumentet med de justeringer, der er nødvendige for at udligne den. Du kan også bruge indikatoren **Markeret** til at identificere andre dokumenter, der er inkluderet på samme blokeringslokation.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Udlign rest](settle-remainder.md)
