---
title: Udligne en fremdateret check fra en debitor
description: Du kan udligne en fremdateret check, efter at checken er clearet af banken.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780009"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Udligne en fremdateret check fra en debitor

[!include [banner](../../includes/banner.md)]

Du kan udligne en fremdateret check, efter at checken er clearet af banken. Denne økonomiske bevægelse clearer også posteringen på en mellemkonto for den fremdaterede check. 

Følgende opgaver skal være fuldført, før du starter denne.

1) Oprette fremdaterede checks

2) Registrere og bogføre en fremdateret check for en debitor 



Rollen for denne opgaveguide er Kasserer.



Denne procedure bruger demofirmaet USMF.

1. Gå til **Kredit og inkasso > Forespørgsler og rapporter > Betalinger > Fremdaterede debitorchecks**.
2. Klik på **Udlign**.
3. Klik på **Afregn clearingpostering**.
    * Udlign debitorkontoen for checktransaktionen.  
4. Luk siden.
5. Gå til **Finans > Kladdeposteringer > Finanskladder**.
6. Vælg en indstilling i feltet **Vis**.
7. Marker eller fjern markeringen i afkrydsningsfeltet **Vis kun kladder, der er oprettet af brugeren** .
8. Find og vælg den ønskede post på listen.
9. Klik på **Linjer**.
10. Klik på **Bilag**.
11. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
