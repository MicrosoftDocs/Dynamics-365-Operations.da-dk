---
title: Udligne en fremdateret check for en kreditor
description: Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9564bf0ded6acbd05c7953798ea02959babbdfd
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726288"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Udligne en fremdateret check for en kreditor

[!include [banner](../../includes/banner.md)]

Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken. 

Gennemfør følgende procedurer, før du starter denne.

1) Oprette fremdaterede checks

2) Registrere og bogføre en fremdateret check for en kreditor



Rollen for denne procedure er Kasserer. Denne procedure bruger demofirmaet USMF.

1. Gå til Kreditor > Betalinger > Fremdaterede kreditorchecks.
2. Klik på Udlign.
3. Klik på Afregn clearingpostering.
    * Udlign kreditorkontoen for checktransaktionen.  
4. Luk siden.
5. Gå til Finans > Kladdeposteringer > Finanskladder.
6. Vælg "Alle" i feltet Vis.
7. Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.
8. Markér den valgte række på listen.
9. Klik på Linjer.
10. Klik på Bilag.
11. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
