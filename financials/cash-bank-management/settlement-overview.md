---
title: Udligningsoversigt
description: "Denne artikel indeholder generelle oplysninger om udligningsprocessen. Den beskriver de typer transaktioner, der kan udlignes, hvornår og hvordan transaktioner kan udlignes og resultaterne af udligningsprocessen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: ab12ef4127daf57fb0816ae1585876b50d1e81ed
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="settlement-overview"></a>Udligningsoversigt

[!include[banner](../includes/banner.md)]


Denne artikel indeholder generelle oplysninger om udligningsprocessen. Den beskriver de typer transaktioner, der kan udlignes, hvornår og hvordan transaktioner kan udlignes og resultaterne af udligningsprocessen.

I udligningsprocessen udlignes posteringerne på et enkelt dokument med transaktionerne i et andet dokument for at øge eller reducere saldoen for hvert dokument. En betaling kan f.eks. udlignes med en faktura. Forskellige posteringstyper kan udlignes, på forskellige tidspunkter, og via forskellige metoder. Udligning kan også medføre, at der oprettes nye posteringer.

## <a name="what-transactions-can-be-settled"></a>Hvilke posteringer kan udlignes
Udligning i Kreditor og Debitor kan forekomme mellem de posteringstyper, der påvirker kreditorsaldoen eller debitorsaldoen, såsom fakturaer, betalinger, kreditnotaer og gebyrer. Alle posteringstyper kan udlignes med en anden transaktionstype. Du kan f.eks. udligne en betaling med en faktura, en kreditnota med en faktura, en faktura med en faktura og betaling med betaling. Du kan udligne betalinger med en postering i samme juridiske enhed eller i en anden juridisk enhed. I organisationer, der anvender en centraliseret betalingsmodel, kan [centraliserede betalinger](set-up-centralized-payments.md) hjælpe med at strømline betalingsprocessen.

## <a name="when-to-settle-transactions"></a>Hvornår posteringer skal udlignes
Posteringer kan udlignes ved tidspunktet for betaling. Når du f.eks. foretager en betaling til en kreditor, vælger du typisk de fakturaer, der skal betales. Når du vælger fakturaer, markerer du dem til udligning mod betalingen. Når debitormedarbejdere registrerer en kundebetaling, kan de markere de relevante fakturaer til udligning baseret på de oplysninger, der er inkluderet i debitorens betaling. Siden **Udlign transaktioner** bruges til at markere transaktioner til udligning. Denne side kan åbnes fra enhver ikke-bogført faktura eller betaling. Når transaktionen bogføres, bogføres udligningen også. Posteringer kan også udlignes, efter de er bogført. Du kan angive og bogføre en debitorbetaling uden at udligne den med en faktura. Du skal måske lige undersøge, at betalingen udlignes med den korrekte faktura. Siden **Udlign transaktioner** kan åbnes fra siden **Alle kunder** eller **Alle leverandører** eller fra siden **Transaktioner** for en debitor eller kreditor. Du kan også tilbageføre bogførte forudbetalinger for en faktura ved at markere betalingen for udligning med en købsordre eller salgsordre. I dette tilfælde har betalingen fortsat en åben saldo, men den kan ikke udlignes mod en anden faktura. Betalingen udlignes automatisk mod den faktura, der oprettes ud fra indkøbsordren eller salgsordren.

## <a name="how-to-settle-transactions"></a>Hvordan posteringer skal udlignes
Posteringer kan udlignes manuelt, automatisk eller via en kombination af de to metoder. Valget af udligningsmetode afhænger af forretningsprocesser, som derefter kan implementeres i hele opsætningen af udligning i Kreditorparametre og Debitorparametre. Du kan oprette kreditorbetalinger og direkte debitorbetalinger for kunder ved hjælp af et betalingsforslag, som bruges til at vælge fakturaer, der skal betales. Betalingsforslaget startes manuelt, men Microsoft Dynamics 365 for Finance and Operations markerer derefter automatisk de valgte fakturaer til udligning, når betalingerne oprettes. Hvis betalingerne oprettes manuelt, kan du bruge siden **Udlign transaktioner** til at vælge fakturaer til udligning. Du kan manuelt vælge fakturaerne, eller du kan bruge indstillingen **Markér efter prioritet**, så fakturaer automatisk markeres til udligning. Indstillingen **Markér efter prioritet** er kun tilgængelig for Debitor. Hvis du vil aktivere denne indstilling, skal du bruge siden **Udligningsprioritet** i Debitorparametre. Hvis en betalingsmedarbejder indtaster en betaling, men ikke udligner betalingen, før han eller hun bogfører den, kan betalingen udlignes automatisk. Du kan aktivere automatisk udligning i debitorparametre og kreditorparametre. Når du bruger automatisk udligning, kan du bruge den foruddefinerede udligningsrækkefølge, eller du kan definere dine egen prioritetsrækkefølge for udligning i debitorparametre. Denne funktionalitet er kun tilgængelig for Debitor.

## <a name="results-of-settlement"></a>Resultater af udligning
Når posteringer udlignes, øges eller mindskes den udestående saldo for hver postering. I et typisk scenarie, hvor en faktura og betaling udlignes, opdateres status og saldoen for hver transaktion efter følgende regler:

-   Hvis betalingsbeløbet er større end fakturabeløbet, reduceres fakturasaldoen til 0,00, og fakturaen lukkes. Betalingen forbliver åben, og saldoen er det beløb, som betalingen overstiger fakturabeløbet med.
-   Hvis betalingsbeløbet er mindre end fakturabeløbet, reduceres betalingssaldoen til 0,00, og betalingen lukkes. Fakturaen forbliver åben, og saldoen er det beløb, som betalingen har underbetatalt fakturaen med.
-   Hvis betalingsbeløbet er lig med fakturabeløbet, lukkes både betalingen og fakturaen, og saldoen for begge er 0,00.

Hvis en [betalingen er mindre end fakturabeløbet](../accounts-payable/vendor-payments-partial-amount.md) på grund af en kasserabat, afskrivning eller underbetaling, lukkes fakturaen og betalingen måske alligevel, afhængigt af opsætningen af udligning i Kreditorparametre og Debitorparametre. Udligning kan også generere transaktioner. Udligning af en faktura og betaling kan for eksempel medføre kasserabat, realiseret gevinst eller tab, momsreguleringer, afskrivninger eller øredifferencer.




