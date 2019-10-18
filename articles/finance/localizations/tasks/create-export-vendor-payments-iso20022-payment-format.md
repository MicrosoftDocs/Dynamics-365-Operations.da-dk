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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185813"
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

