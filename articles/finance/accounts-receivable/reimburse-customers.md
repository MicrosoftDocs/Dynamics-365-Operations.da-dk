---
title: Refundere kunder
description: I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 892b089edb16ba560f588c086d37faafdf16958d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891776"
---
# <a name="reimburse-customers"></a>Refundere kunder

[!include [banner](../includes/banner.md)]

I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer. Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen. 

Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.

| Forudsætning                                                            | Beskrivelse |
|-------------------------------------------------------------------------|-------------|
| Angiv minimumbeløbet for refusion for den juridiske enhed.          | På siden **Debitorparametre** side i området **Generelt** i feltet **Minimumsrefusion** skal du angive det minimumbeløb, som kan refunderes i forbindelse med kunders overbetaling. |
| Valgfrit: Føj en kreditorkonto til hver kunde, der kan få refunderet beløb. | Vælg kundens kreditorkonto på siden **Kunder** på oversigtspanelet **Diverse detaljer** i feltet **Kreditorkonto**. |

Når du opretter refusionsposteringer, oprettes der en kreditorfaktura for beløbet svarende til kreditsaldoen. Refusionsprocessen fjerner kreditsaldoen for debitorkontoen, og der oprettes en forfalden saldo for kreditorkontoen, der er knyttet til kunden.

1. I debitor skal du køre **Refusions-** processen (**Debitor \> Periodiske opgaver \> Refusion**).
2. Hvis du vil gruppere alle posteringer, uanset finansdimensioner, skal du angive indstillingen **Opsummer debitor** til **Ja**. Hvis du kun vil gruppere posteringer med lignende finansdimensioner, skal du angive indstillingen til **Nej**.
3. Vælg **Medtag debitorer med udestående debetposteringer** for at vælge kunder, der har ikke-udlignede debetbeløb.
4. Hvis du vil refundere bestemte debitorkonti, skal du på oversigtspanelet **Poster, der skal indgå** vælge **Filter** og derefter angive debitorkontiene i forespørgslen.

    Kreditbeløbene overføres til kundernes kreditorkonti og behandles som almindelige betalinger. Hvis en kunde ikke har en kreditorkonto, oprettes der automatisk en engangskreditorkonto for kunden.

5. Hvis du vil have vist de refusionsposteringer, der er oprettet, skal du bruge rapporten **Refusion** (**Debitor \> Forespørgsler og rapporter \> Refusionsrapport**).
6. I Kreditor skal du oprette en betaling for kreditorfakturaer, der er oprettet af refusionsprocessen. Du kan finde flere oplysninger om betaling af kreditorer under [Oversigten Kreditorbetaling](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
