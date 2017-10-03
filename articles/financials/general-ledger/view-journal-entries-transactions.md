---
title: "Få vist kladdeposteringer og transaktioner"
description: "I denne artikel beskrives de forskellige måder, du kan få vist kladdeposter og transaktioner."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 91cf395f2245f85cb244c7532ea77a63da98fcd7
ms.contentlocale: da-dk
ms.lasthandoff: 08/01/2017

---

# <a name="view-journal-entries-and-transactions"></a>Få vist kladdeposteringer og transaktioner

[!include[banner](../includes/banner.md)]


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
-   **Udskrift af kladden** – i denne rapport vises resultatet af en bogført kladde. Du kan køre rapporten efter kladdebatchnummer eller kladdetypen eller tilføje flere felter.
-   **Bogførte posteringer efter kladde** – Denne rapport viser de transaktioner, der er bogført i en kladde grupperet efter bilag.
-   **Posteringsliste pr. dato** – Denne rapport viser alle posteringer efter dato sammen med kladdenummer, bilag og finanskonto. Den viser også transaktionerne i transaktions-, regnskabs- og rapporteringsvalutaer.
-   **Transaktionsoprindelse** – Denne transaktionsrapport viser kontoen efter kladde og efter transaktions-, regnskabs- og rapporteringsvaluta. Den viser også hver linje i kladden, der blev brugt som en forskydning.


##<a name="see-also"></a>Se også
- [Kontosaldi i Finans](general-ledger-account-balances.md) 
- [Sporing af regnskabskilde](..\accounts-payable\accounting-source-explorer.md)
- [Økonomirapportering](financial-reporting-getting-started.md)
- [Se kladdeposteringer](tasks/view-journal-entries-or-transactions.md)




