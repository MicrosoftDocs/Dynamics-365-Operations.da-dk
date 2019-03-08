---
title: Definere kreditorbetalingsbetalinger
description: Konfigurer betalingsbetingelserne kreditorfakturaer.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "358548"
---
# <a name="define-vendor-payment-terms"></a>Definere kreditorbetalingsbetalinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Konfigurer betalingsbetingelserne kreditorfakturaer. Denne opgave bruger demofirmaet USMF.

1. Gå til Kreditor > Betalingsopsætning > Betalingsbetingelse.
2. Klik på Ny.
    * Siden Betalingsbetingelser bruges til at definere, hvordan forfaldsdatoen beregnes. Den bruges ikke til at definere, hvordan kasserabatdatoen beregnes.  
3. Indtast en værdi i feltet Betalingsbetingelse.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv et tal i feltet Dage.
    * Det tal, der angives her, skal bruges til at føje til forfaldsdatoen eller til slutningen af den periode, der er identificeret i betalingsmetoden. Hvis du for eksempel vælger Netto, føjes tallet til forfaldsdatoen. Hvis du vælger Aktuel måned, føjes tallet til den sidste dag i den aktuelle måned til beregning af forfaldsdatoen.  
6. Klik på Gem.
7. Luk siden.
8. Gå til Kreditor > Betalingsopsætning > Kasserabatter.
9. Klik på Ny.
10. Angiv et id i feltet Kasserabat.
11. Skriv en værdi i feltet Beskrivelse.
12. Hvis leverandøren tilbyder niveauinddelt rabat, skal du vælge den næste kasserabat, når den aktuelle er udløbet.
13. Luk siden.
14. Angiv et tal i feltet Dage.
    * Det antal, der er angivet i feltet Dage, skal bruges til at beregne dato for kasserabat ud fra den indstilling, der blev valgt i feltet Netto/Løbende. Hvis der blev valgt Netto, føjes antallet til fakturadatoen for at fastlægge kasserabatdatoen. Hvis der blev valgt Løbende, føjes antallet til slutningen af den aktuelle måned for at fastlægge kasserabatdatoen.  
15. Angiv procenten af kasserabatten i feltet Rabat. 
16. Angiv den hovedkonto, som kasserabatten bogføres til for debitorfakturaer.
17. Angiv den hovedkonto, som kasserabatten bogføres til for kreditorfakturaer.
    * Hvis "Rabatmodkonti" er indstillet til Brug hovedkonto til kreditorrabatter, bruges hovedkontoen.  Hvis indstillingen er angivet til Konti på fakturalinjerne, bogføres kasserabatten til aktiv/udgiftskonti på fakturalinjerne.  
18. Klik på Gem.

