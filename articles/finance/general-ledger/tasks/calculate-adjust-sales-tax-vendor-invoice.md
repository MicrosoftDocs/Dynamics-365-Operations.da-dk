---
title: Beregne og justere moms på en kreditorfaktura
description: Dette emne forklarer, hvordan du justerer moms på en kreditorfaktura i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139961"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Beregne og justere moms på en kreditorfaktura

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du justerer moms på en kreditorfaktura. Hvis det oprindelige kildedokument viser forskellige momsbeløb som beregnet, kan du justere beløbene, før der bogføres. Denne opgave bruger demofirmaet DEMF.

1. Gå til **Moduler > Kreditorer > Fakturaer > Fakturajournal** i navigationsruden.
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

