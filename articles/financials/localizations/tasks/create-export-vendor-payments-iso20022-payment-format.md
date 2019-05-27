---
title: Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat
description: Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570047"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.

Det er den femte procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Brug DEMF-demodata til at fuldføre dette eksempel.

## <a name="example"></a>Eksempel

1.  Gå til **Kreditor > Betalinger > Betalingskladde**.
2.  Klik på **Ny**.
3.  Indtast eller vælg en værdi i feltet **Navn**.
4.  Klik på **Linjer > Betalingsforslag > Opret betalingsforslag**.
5.  Udvid sektionen **Poster, der skal indgå**.
6.  Klik på **Filtrér**.
7.  Markér rækken til tabellen **Leverandører** og feltet **Kreditorkonto** på listen.
8.  Indtast eller vælg en værdi i feltet **Kriterier**. Du kan anvende kriterier efter eget valg for udvælgelse af kreditorposteringer, der skal betales. I dette eksempel bruges DE 001 som en kreditorkonto.
12. Klik på **OK**.
13. Klik på **OK**.
14. Klik på **Opret betalinger**.
15. Generer en ISO20022-betalingsfil.
    1.  Klik på **Generer betalinger**.
    2.  Indtast eller vælg en værdi i feltet **Betalingsmåde**.
    3.  Skriv en værdi i feltet **Filnavn**. I dette eksempel bliver den oprettede fil SEPA-kompatibel på grund af indbetalingen i EUR. ISO20022-pengeoverførsel samt andre formater for kreditorbetalinger kan også bruges til oprettelse af betalinger i andre valutaer.
    4.  Indtast eller vælg en værdi i feltet **Bankkonto**.

