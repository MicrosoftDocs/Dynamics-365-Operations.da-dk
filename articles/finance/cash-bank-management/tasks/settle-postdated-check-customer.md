---
title: Udligne en fremdateret check fra en debitor
description: Du kan udligne en fremdateret check, efter at checken er clearet af banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176984"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Udligne en fremdateret check fra en debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan udligne en fremdateret check, efter at checken er clearet af banken. Denne økonomiske bevægelse clearer også posteringen på en mellemkonto for den fremdaterede check. 

Følgende opgaver skal være fuldført, før du starter denne.

1) Oprette fremdaterede checks

2) Registrere og bogføre en fremdateret check for en debitor 



Rollen for denne opgaveguide er Kasserer.



Denne procedure bruger demofirmaet USMF.

1. Gå til Kredit og inkasso > Forespørgsler og rapporter > Betalinger > Fremdaterede debitorchecks.
2. Klik på Udlign.
3. Klik på Afregn clearingpostering.
    * Udlign debitorkontoen for checktransaktionen.  
4. Luk siden.
5. Gå til Finans > Kladdeposteringer > Finanskladder.
6. Vælg en indstilling i feltet Vis.
7. Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.
8. Find og vælg den ønskede post på listen.
9. Klik på Linjer.
10. Klik på Bilag.
11. Luk siden.
