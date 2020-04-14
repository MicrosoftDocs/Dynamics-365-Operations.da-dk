---
title: Definere kreditorbetalingsbetingelser
description: I dette emne forklares, hvordan du konfigurerer betalingsbetingelser for kreditorfakturaer.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143885"
---
# <a name="define-vendor-payment-terms"></a>Definere kreditorbetalingsbetingelser

[!include [banner](../../includes/banner.md)]

I dette emne forklares, hvordan du konfigurerer betalingsbetingelser for kreditorfakturaer. Denne opgave bruger demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Kreditor > Opsætning af betaling > Betalingsbetingelse**.
2. Vælg **Ny**. Siden Betalingsbetingelser bruges til at definere, hvordan forfaldsdatoen beregnes. Den bruges ikke til at definere, hvordan kasserabatdatoen beregnes.  
3. Indtast en værdi i feltet **Betalingsbetingelse**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Angiv et tal i feltet **Dage**. Det tal, der angives her, skal bruges til at føje til forfaldsdatoen eller til slutningen af den periode, der er identificeret i betalingsmetoden. Hvis du for eksempel vælger **Netto**, føjes tallet til forfaldsdatoen. Hvis du vælger **Aktuel måned**, føjes tallet til den sidste dag i den aktuelle måned til beregning af forfaldsdatoen.  
6. Vælg **Gem**.
7. Luk siden.
8. Gå til **Kreditor > Opsætning af betaling > Kasserabatter**.
9. Vælg **Ny**.
10. Angiv et id i feltet **Kasserabat**.
11. Indtast en værdi i feltet **Beskrivelse**.
12. Hvis leverandøren tilbyder niveauinddelt rabat, skal du vælge den næste kasserabat, når den aktuelle er udløbet.
13. Luk siden.
14. Angiv et tal i feltet **Dage**. Det antal, der er angivet i feltet **Dage**, skal bruges til at beregne dato for kasserabat ud fra den indstilling, der blev valgt i feltet **Netto/Løbende**. Hvis der blev valgt **Netto**, føjes antallet til fakturadatoen for at fastlægge kasserabatdatoen. Hvis der blev valgt **Aktuel måned**, føjes antallet til slutningen af den aktuelle måned for at fastlægge kasserabatdatoen.  
15. Angiv procenten af kasserabatten i feltet **Rabat**. 
16. Angiv den hovedkonto, som kasserabatten skal bogføres på for debitorfakturaer, og angiv derefter den hovedkonto, som kasserabatten skal bogføres på for kreditorfakturaer. Hvis **Rabatmodkonti** er indstillet til **Brug hovedkonto til kreditorrabatter**, bruges hovedkontoen. Hvis indstillingen er angivet til **Konti på fakturalinjerne**, bogføres kasserabatten til aktiv/udgiftskonti på fakturalinjerne.  
17. Vælg **Gem**.

