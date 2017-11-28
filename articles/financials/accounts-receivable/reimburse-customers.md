---
title: Refundere kunder
description: "I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer. Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 01c9dcebe82544624c6dd0feb3672d1c5bdfe2d1
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="reimburse-customers"></a>Refundere kunder

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer. Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen. 

Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

| Forudsætning                                                            | Beskrivelse                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Angiv minimumbeløbet for refusion for den juridiske enhed.          | På siden **Debitorparametre** side i området **Generelt** i feltet **Minimumsrefusion** skal du angive det minimumbeløb, som kan refunderes i forbindelse med kunders overbetaling. |
| Valgfrit: Føj en kreditorkonto til hver kunde, der kan få refunderet beløb. | Vælg kundens kreditorkonto på siden **Kunder** på oversigtspanelet **Diverse detaljer** i feltet **Kreditorkonto**.                                           |

Når du opretter refusionsposteringer, oprettes der en kreditorfaktura for beløbet svarende til kreditsaldoen. Refusionsprocessen fjerner kreditsaldoen for debitorkontoen, og der oprettes en forfalden saldo for kreditorkontoen, der er knyttet til kunden.

1.  I Debitor skal du køre processen **Refusion**.
2.  Udfør ét af følgende trin:
    -   Hvis refusionen kun gælder bestemte kundekonti, skal du klikke på **Vælg** og angive kundekontiene i forespørgslen.
    -   Hvis refusionen gælder alle kundekonti, skal du klikke på **OK**.

    Kreditbeløbene overføres til kundernes kreditorkonti og behandles som almindelige betalinger. Hvis en kunde ikke har en kreditorkonto, oprettes der automatisk en engangskreditorkonto for kunden.
3.  Til at få vist de refusionsposter, der er oprettet, kan du bruge siden **Refusion**.
4.  I Kreditor skal du oprette en betaling for kreditorfakturaer, der er oprettet af refusionsprocessen.





