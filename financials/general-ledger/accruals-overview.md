---
title: Oversigt over periodiseringer
description: I denne artikel beskrives periodiseringer, og hvordan du konfigurerer dem og opretter transaktioner.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Oversigt over periodiseringer

I denne artikel beskrives periodiseringer, og hvordan du konfigurerer dem og opretter transaktioner.

Periodiseringer bruges i periodiseringsregnskab til at registrere indtægter, der er anerkendt i den periode, der er optjent i, ikke, når betalingen er modtaget, og til at spore udgifter (omkostninger), der registreres, når de opstår, ikke når betalingen foretages.

## <a name="accrual-schemes"></a>Periodiseringsskemaer
Periodiseringsskemaer bruges til at konfigurere udskudte indtægter og omkostninger, og det samme periodiseringsskema kan bruges til både indtægter og omkostninger. Periodiseringer af finans omfordeler omkostninger eller indtægter for en kladdelinje, så omkostningerne og indtægterne genkendes i de relevante perioder. På siden **Periodiseringsskema** kan du angive de debet- og kreditkonti, der skal bruges, når der anvendes periodiseringsskemaet.

-   **Debet** – Den hovedkonto, som du definerer, erstatter debethovedkontoen på kladdebilagslinjen. Denne konto bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af Finans.
-   **Kredit** – Den hovedkonto, som du definerer, erstatter kredithovedkontoen på kladdebilagslinjen. Denne konto bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af Finans.

Når du har bestemt, hvilke konti der skal bruges, kan du angive, hvordan bilagsnummeret oprettes, når der oprettes posteringer til periodisering. Du kan også angive, hvor ofte transaktionerne forekommer, det antal gange posteringerne oprettes, og når posteringerne er bogført. Når periodiseringsskemaet er blevet oprettet, kan du bruge det i nogle af kladderne ved hjælp af funktionen til periodisering af Finans.

## <a name="ledger-accruals"></a>Periodiseringer af finans
Når du angiver en kladde, kan du klikke på **Finansperiodisering** i menuen **Funktioner**. Når du derefter vælger periodiseringsskemaet, vises basisbeløbet fra den kladde, der fordeles over perioden som fastlagt i periodiseringsskemaet. For eksempel, hvis du betaler en medarbejders forsikring for hele året i januar, og beløbet er 12.000, skal du genkende denne udgift hver måned. Du kan vælge startdatoen. Du kan også angive, om det beløb, der er hensat, er baseret på kontoen eller modkontoen. Når du har foretaget dine valg, skal du klikke på **transaktioner** til at få vist alle posteringer, der er oprettet ud fra periodiseringsskemaet. Hvis du fordeler 12.000 i forsikring udgifter over hele året, vil du se 1.000 for hver måned. Når du bogfører kladden, kan du få vist posteringerne ved hjælp af den **bilagsposteringer** undersøgelse side. Hvis du ikke kan anvendes et periodiseringsskema, (for eksempel når en salgsordrefaktura eller fakturaen for indkøbsordren er involveret), kan du kreditere det forudbetalte beløb og debitere udgiftsbeløbet. Du kan derefter vælge **Modregn**, når du anvender periodiseringsskemaet.

