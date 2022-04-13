---
title: Forudbetalinger fra debitorer
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og behandle forudbetalinger fra kunder (også kaldet kundeindbetalinger).
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ba462dc2b5fe326db14dfb3c92f986478d31791
ms.sourcegitcommit: 3cb1f49a02e4a849fc34ffeb81fe507f0608b35e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/22/2022
ms.locfileid: "8464870"
---
# <a name="customer-prepayments"></a>Forudbetalinger fra debitorer

[!include [banner](../includes/banner.md)]

Forudbetalinger fra debitorer bruges, når du modtager en betaling fra en debitor, uden at der er en faktura, som betalingen kan udlignes mod. Disse typer betalinger kaldes også debitorindbetalinger.

Processen til opsætning og arbejde med forudbetalinger fra kunder består af følgende grundlæggende trin.

1. Opret en debitorposteringsprofil til forudbetalinger.
2. Angiv parameteren **Posteringsprofil med kladdebilag for forudbetaling**.
3. Opret en debitorbetalingskladde, og marker afkrydsningsfeltet **Kladdebilag for forudbetaling** på hver linje.
4. Bogfør debitorbetalingskladde.
5. Når en faktura er genereret, skal du udligne forudbetalingen på den ved hjælp af siden **Udlign åbne posteringer**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Oprette en debitorposteringsprofil til forudbetalinger

Når du accepterer forudbetalinger eller indbetalinger fra kunderne, inden varer eller tjenester leveres, eller før der findes en faktura i systemet, vil du typisk registrere kontanterne som et passiv i stedet for et aktiv i din kontoplan. Kravene til registrering af disse beløb i finansmodulet kan dog være forskellige, afhængigt af dit land eller område. Derfor skal du sørge for at kontakte en revisor vedrørende eventuelle lokale regler, der er gældende.

Generelt er processen til oprettelse af en posteringsprofil, der kan bruges til forudbetalinger, den samme som processen til oprettelse af andre posteringsprofiler. Den primære forskel er den hovedkonto, du vælger i feltet **Samlekonto**. Du kan finde flere oplysninger i [Debitorposteringsprofiler](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Definere parametre for debitorforudbetalinger

Der er to hovedparametre for debitorer, som du skal overveje, når du konfigurerer systemet til debitorforudbetalinger. Følg disse trin for at konfigurere parametrene.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
2. Valgfrit: Vælg **Ja** i **Moms for kladdebilag for forudbetalinger** i oversigtspanelet **Betaling** under fanen **Finans og moms**.
3. Vælg den debitorposteringsprofil, der skal bruges til bogføring af forudbetalinger, i feltet **Posteringsprofil med kladdebilag for forudbetaling**.
4. Luk siden.

## <a name="create-customer-prepayment-vouchers"></a>Oprette forudbetalingsbilag for debitorer

Når du opretter debitorbetalingskladden, skal du for hver forudbetaling vælge **Ja** i indstillingen **Kladdebilag for forudbetaling** på siden **Debitorbetalingskladde**. Følg disse trin for at oprette en debitorforudbetaling.

1. Gå til **Debitor \> Betalinger \> Debitorbetalingskladde**.
2. Vælg **Ny** for at oprette en kladde.
3. I feltet **Navn** skal du vælge det kladdenavn, der skal bruges.

    > [!IMPORTANT]
    > Hvis du valgte **Ja** i indstillingen **Moms for kladdebilag for forudbetalinger** i den foregående procedure, skal du vælge et kladdenavn, hvor parameteren **Beløb er inklusive moms** er valgt. 

4. Valgfrit: Angiv en detaljeret beskrivelse i feltet **Beskrivelse**.
5. Vælg **Linjer**.
6. Hvis der ikke findes en tom linje, skal du vælge **Ny** for at oprette en linje.
7. Angiv den dato, hvor forudbetalingen skal bogføres, i feltet **Dato**.
8. Vælg kunden for forudbetalingen i feltet **Konto**.
9. Valgfrit: Angiv en detaljeret beskrivelse af transaktionen i feltet **Beskrivelse**.
10. Angiv forudbetalingsbeløbet i feltet **Kredit**.
11. Vælg den konto, som betalingen skal modregnes mod, i feltet **Modkonto**. Vælg f.eks. den bank- eller hovedkonto, betalingen skal bogføres på.
12. Vælg kundens betalingsmåde i feltet **Betalingsmåde**.
13. Vælg **Ja** i indstillingen **Kladdebilag for forudbetaling** under fanen **Betaling**.
14. Gentag trin 7 til 13 for hver ekstra forudbetaling, der skal bogføres.
15. Vælg **Bogfør** for at afslutte kladden.

## <a name="settle-prepayments-with-invoices"></a>Udligne forudbetalinger med fakturaer

Du kan bruge arbejdsområdet **Debitorbetalinger** til nemt at finde og udligne betalinger, der ikke er fuldt udlignet.

1. Vælg feltet **Debitorbetalinger** på dashboardet **Start**.
2. Søg efter og vælg den betaling, der skal udlignes, under fanen **Betalinger, der ikke er udlignet** i sektionen **Debitorposter**.
3. Vælg **Udlign posteringer**.
4. Marker afkrydsningsfeltet **Marker** for fakturaen og den betaling, der skal udlignes.
5. Vælg **Bogfør**.

Du kan finde flere oplysninger om, hvordan du udligner åbne posteringer, i [Udligningsoversigt](/dynamics365/finance/cash-bank-management/settlement-overview).
