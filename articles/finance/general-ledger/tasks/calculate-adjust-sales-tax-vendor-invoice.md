---
title: Beregne og justere moms på en kreditorfaktura
description: Denne artikel forklarer, hvordan du justerer moms på en kreditorfaktura i Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868353"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Beregne og justere moms på en kreditorfaktura

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du justerer moms på en kreditorfaktura. Hvis det oprindelige kildedokument viser forskellige momsbeløb som beregnet, kan du justere beløbene, før der bogføres. Denne opgave bruger demofirmaet DEMF.

1. Gå til **Kreditor > Fakturaer > Fakturajournal**.
2. Vælg **Ny**.
3. Vælg en indstilling i rullemenuen i feltet **Navn** i den nye række.
4. Gå til handlingsruden, og vælg **Linjer**.
5. I feltet **Konto** skal du angive de ønskede værdier.
6. Skriv en værdi i feltet **Faktura**.
7. Angiv et tal i feltet **Kredit**.
8. I feltet **Modkonto** skal du specificere de ønskede værdier.
9. Vælg **Moms**.
10. Indtast et tal i feltet **Samlede faktiske momsbeløb**.
11. Under fanen **Regulering** kan momsbeløbene justeres pr. momskode
12. Vælg **Nulstil faktiske beløb fra til beregnede beløb**.
13. Vælg **OK**.
14. Vælg **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
