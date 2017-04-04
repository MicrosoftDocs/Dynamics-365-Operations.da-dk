---
title: "Få vist kladdeposteringer og transaktioner"
description: "I denne artikel beskrives de forskellige måder, du kan få vist kladdeposter og transaktioner."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a6848ea9c05536ac18a038b1864c9ccb9408964c
ms.lasthandoff: 03/31/2017


---

# <a name="view-journal-entries-and-transactions"></a>Få vist kladdeposteringer og transaktioner

I denne artikel beskrives de forskellige måder, du kan få vist kladdeposter og transaktioner. 

Brugere, der ønsker at få vist kladder og transaktioner, har flere måder at få adgang til dataene på. De kan drage fordel af forespørgselssider, der giver mulighed for detailudledning, eller de kan bruge forskellige rapportindstillinger i finansmodulet.

## <a name="voucher-transactions"></a>Bilagstransaktioner
**Bilagsposteringer** er en forespørgselsside, hvor du kan vælge fra forskellige tabeller og felter for at angive kriterier for den saldo eller postering, som du søger efter. Du kan for eksempel få vist alle posteringer for en bestemt dato eller en konto, eller alle transaktioner af typen **Igangværende**, der er i et bestemt posteringslag. Siden viser kladdenummer, bilag, dato og hovedkontoen som standard, men du kan tilføje flere tabeller, felter og kriterier for at indsnævre søgningen.

## <a name="audit-trail"></a>Revisionsspor
**Revisionsspor** er en forespørgselsside, der viser typer transaktioner, beskrivelser, hvem posteringerne blev oprettet af, og hvornår de blev oprettet. Fra forespørgselssiden **Revisionsspor** kan du få vist bilagsposteringer.

## <a name="financial-reports"></a>Økonomirapporter
Du kan også udforske og analysere finansposteringer ved at køre økonomiske rapporter. Da udformningen af økonomiske rapporter kan være baseret på konti, dimensioner, kontoarter eller en kombination af disse tre, kan du få vist posteringerne ved at foretage detailudledning på forskellige måder. Hvis du ønsker yderligere oplysninger til finanstransaktioner, kan du også medtage flere transaktionsegenskaber som led i rapportdesignet. Hvis du desuden vil have vist de transaktioner, der udgør en finanssaldo, kan du foretage detailudledning til kontotransaktioner, på samme måde som du kan fra listesiden **Råbalance**.

## <a name="ledger-reports"></a>Finansrapporter
Ud over de økonomiske rapporter, kan du bruge følgende finansrapporter til at få vist finanstransaktioner:

-   **Dimensionsopgørelse** – Denne rapport viser transaktioner efter dag og konto, og der er også mulighed for at få vist transaktioner efter dimension og periode.
-   **Finansposteringsliste** – Denne rapport viser transaktioner i transaktions-, regnskabs- og rapporteringsvaluta for et regnskab.
-   **Udskriv kladde** – i denne rapport vises resultatet af en bogført kladde. Du kan køre rapporten efter kladdebatchnummer eller kladdetypen eller tilføje flere felter.
-   **Bogførte posteringer efter kladde** – Denne rapport viser de transaktioner, der er bogført i en kladde grupperet efter bilag.
-   **Posteringsliste pr. dato** – Denne rapport viser alle posteringer efter dato sammen med kladdenummer, bilag og finanskonto. Den viser også transaktionerne i transaktions-, regnskabs- og rapporteringsvalutaer.
-   **Transaktionsoprindelse** – Denne transaktionsrapport viser kontoen efter kladde og efter transaktions-, regnskabs- og rapporteringsvaluta. Den viser også hver linje i kladden, der blev brugt som en forskydning.


Yderligere oplysninger finder du [finanspostbalancer](general-ledger-account-balances.md), [regnskabsmæssige kilde explorer](\financials\accounts-payable\accounting-source-explorer) og [finansiel rapportering](financial-reporting-getting-started.md)


