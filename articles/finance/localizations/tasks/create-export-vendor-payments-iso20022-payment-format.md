---
title: Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat
description: Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac84055586eff678ea489b35198b1c2dfab13658
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856461"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat

[!include [banner](../../includes/banner.md)]

Denne artikel beskriver, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel.

Det er den femte procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Brug DEMF-demodata til at fuldføre dette eksempel.

## <a name="example"></a>Eksempel

1.    Gå til **Kreditor > Betalinger > Betalingskladde**.
2.    Klik på **Ny**.
3.    Indtast eller vælg en værdi i feltet **Navn**.
4.    Klik på **Linjer > Betalingsforslag > Opret betalingsforslag**.
5.    Udvid sektionen **Poster, der skal indgå**.
6.    Klik på **Filtrér**.
7.    Markér rækken til tabellen **Leverandører** og feltet **Kreditorkonto** på listen.
8.    Indtast eller vælg en værdi i feltet **Kriterier**. Du kan anvende kriterier efter eget valg for udvælgelse af kreditorposteringer, der skal betales. I dette eksempel bruges DE 001 som en kreditorkonto.
12.    Klik på **OK**.
13.    Klik på **OK**.
14.    Klik på **Opret betalinger**.
15. Generer en ISO20022-betalingsfil.
    1.    Klik på **Generer betalinger**.
    2.    Indtast eller vælg en værdi i feltet **Betalingsmåde**.
    3.    Skriv en værdi i feltet **Filnavn**. I dette eksempel bliver den oprettede fil SEPA-kompatibel på grund af indbetalingen i EUR. ISO20022-pengeoverførsel samt andre formater for kreditorbetalinger kan også bruges til oprettelse af betalinger i andre valutaer.
    4.    Indtast eller vælg en værdi i feltet **Bankkonto**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]