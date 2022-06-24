---
title: Afstemme fragt i transportstyring
description: I denne artikel beskrives fragtafstemningsprocessen.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff29de62de12e8ca8bea0f374921a51b5819222e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844217"
---
# <a name="reconcile-freight-in-transportation-management"></a>Afstemme fragt i transportstyring

[!include [banner](../includes/banner.md)]

I denne artikel beskrives fragtafstemningsprocessen.

Fragtafstemning kan udføres manuelt, eller det kan indstilles til at ske automatisk. Hvis du vil bruge automatisk fragtafstemning, skal du angive en revisionsmaster, hvor du kan definere de kriterier, der bestemmer, hvilken fragtbreve der afstemmes automatisk.

## <a name="the-freight-reconciliation-process"></a>Fragtafstemningsprocessen

Fragtsatser beregnes af det satsprogram, der er knyttet til den relevante fragtmand. Når en belastning er bekræftet, oprettes der et fragtbrev, og fragtsatserne overføres til det. Fragtsatserne fordeles som diverse tillæg til det relevante kildedokument (indkøbsordre, salgsordre, og/eller flytteordre), afhængigt af den konfiguration, der bruges til den almindelige fakturering. Fragtafstemningsprocessen (der er også kaldes sammenholdelsesprocessen) kan begynde, så snart fragtfakturaen ankommer fra fragtmanden. Fakturaen kan modtages elektronisk eller på papir. Hvis fakturaen modtages på papir, kan du generere en elektronisk faktura ved at bruge fragtbrevet som skabelon.

[![Fragtafstemningsproces.](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Manuel afstemning

Hvis du afstemmer fragt manuelt, skal du sammenholde hver fakturalinje med fragtbrevlinjen eller -linjerne for den belastning, der skal faktureres. Du udfører afstemningen på siden **Sammenholdelse af fragtbrev og faktura**. Hvis beløbet på fakturalinjen ikke stemmer overens med beløbet i fragtbrevet, skal du vælge en afstemningsårsag for forskellen. Hvis der er flere grunde til afstemning, kan du opdele uafstemte beløb på tværs af dem. Årsagen til afstemningen bestemmer, hvordan de forskellige beløb bogføres i finansmodulet. Når afstemningen af hele fakturabeløbet er behandlet, sendes den til godkendelse, og derefter bogføres kladden. I følgende illustration vises, hvordan du opretter en fragtfaktura og udfører fragtafstemning.

[![Fragtafstemningsopgaver.](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatisk afstemning

Hvis du vil bruge automatisk afstemning, skal du angive tidsplanen for afstemningen, og de fakturaer og fragtmænd der skal bruges. Sammenholdelse af fakturalinjer og fragtbreve sker i overensstemmelse med opsætningen af revisionsmaster- og fragtbrevtypen. Når du har kørt den automatiske afstemning, skal du håndtere eventuelle fakturaer, som systemet ikke kan afstemme. Du skal derefter behandle disse fakturaer manuelt, før du kan bogføre alle fakturaer til betaling.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Afstem fragtbreve med fragtfakturaer ved hjælp af automatisk eller manuel afstemning

*Afstemning* er den proces, der bruges til at finde de fragtbreve, som svarer til hver enkelt fragtfaktura. Dette gøres ved at afstemme fakturalinjerne én efter én (manuel afstemning) eller ved at afstemme alle tilgængelige fakturaer på én gang (automatisk afstemning).

### <a name="auto-matching"></a>Automatisk afstemning

Når flere fragtfakturaer afstemmes med samme fragtbrev, fungerer processen til automatisk afstemning på følgende måde:

1. Alle fragtfakturaer, der ikke afstemmes, sorteres efter beløb med største beløb først.
1. Fragtfakturaerne afstemmes én efter én, indtil der ikke er noget positivt beløb på fragtbrevet.
1. Restbeløbet på fragtfakturaerne angives afhængigt af opsætningen af revisionsmasteren og restbeløbet på fragtfakturaerne.

### <a name="manual-matching"></a>Manuel sammenholdelse

Alle fragtbreve med positive beløb vil være tilgængelige til afstemning. På samme måde som ved automatisk afstemning kan brugeren kun afstemme fragtfakturaer med negative beløb for fragtfakturaer, der ikke er afstemt fuldt ud.

### <a name="example"></a>Eksempel

Hvis du f.eks. har et fragtbrev (FB) på 1500, og du har oprettet tre fragtfakturaer til fragtbrevet med én fakturalinje for hver faktura med følgende indstillinger:

- Oprindelig fragtbrev (FB): Beløb 1500
- Faktura 1 (Fak1): Beløb 1000
- Faktura 2 (Fak2): Beløb 600
- Faktura 3 (Fak3): Beløb -100

#### <a name="automatic-matching-result"></a>Automatisk afstemningsresultat

Automatisk afstemning udføres i følgende rækkefølge:

1. Sortér alle fragtfakturaer i faldende rækkefølge efter beløb: Fak1 -> Fak2 -> Fak3.
1. Afstem Fak1 med FB. Fak1 har 1000 afstemte, og FB har 500 som restbeløb, så statussen er angivet til *Delvist afstemt*.
1. Afstem Fak2 med FB. Fak2 har 500 afstemte, og FB har 0 som restbeløb, så statussen er angivet til *Fuldt afstemt*.
1. Da FB nu er fuldt afstemt, behandles Fak3 ikke.

#### <a name="manual-matching-result"></a>Manuelt afstemningsresultat

Ved manuel afstemning varierer resultaterne afhængigt af rækkefølgen af afstemningen, som det er illustreret i følgende eksempelsager.

##### <a name="manual-matching-case-1"></a>Manuel afstemningssag 1

Manuel afstemning for dette eksempel kan foregå på følgende måde:

1. Afstem FB med Fak1. FB har 500 som restbeløb, så statussen er angivet til *Delvist afstemt*.
1. Afstem Fak2 med FB. Fak2 har 500 afstemte, og FB har 0 som restbeløb, så statussen er angivet til *Fuldt afstemt*.
1. Når Fak3 afstemmes manuelt, vil du ikke kunne finde nogen uafstemte fragtbreve.

Denne sag er grundlæggende den samme som automatisk afstemning

##### <a name="manual-matching-case-2"></a>Manuel afstemningssag 2

Manuel afstemning for dette eksempel kan også foregå på følgende måde:

1. Afstem Fak3 med FB. Nu har FB et restbeløb på 1600, hvilket er det samme som at fratrække negative 100 oven på 1500. Både FB og Fak3 har et afstemt antal på -100.
1. Afstem Fak1 og Fak2 med FB én efter én. FB er fuldt afstemt.

Som dette eksempel viser, skal afstemningen af fragtfakturaer med negative beløb kun foregå manuelt. Derved sikres, at det altid er muligt at afstemme fragtfakturaer med negative beløb for et fragtbrev, der ikke er fuldt afstemt, da det giver dig mulighed for at styre afstemningsrækkefølgen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]