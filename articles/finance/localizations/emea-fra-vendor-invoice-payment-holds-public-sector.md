---
title: Betalingsspærring af kreditorfakturaer i den offentlige sektor i Frankrig
description: De almindelige processer, der vedrører betalingsspærring af kreditorfakturaer i Microsoft Dynamics 365 Finance, er suppleret for franske enheder i den offentlige sektor. I dette emne beskrives de funktioner til betalingsspærring af kreditorfakturaer, der bruges af den offentlige sektor i Frankrig.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm
audience: Application User
ms.reviewer: kfend
ms.custom: 27331
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e830ad4e58fb3552ecbb7b961504b75b6c287c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248863"
---
# <a name="vendor-invoice-payment-holds-in-the-public-sector-in-france"></a>Betalingsspærring af kreditorfakturaer i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

De almindelige processer, der vedrører betalingsspærring af kreditorfakturaer i Dynamics 365 Finance, er suppleret for franske enheder i den offentlige sektor. I dette emne beskrives de funktioner til betalingsspærring af kreditorfakturaer, der bruges af den offentlige sektor i Frankrig.

<a name="set-up-rules-for-vendor-invoice-payment-holds"></a>Konfigurere regler for betalingsspærring af kreditorfakturaer
---------------------------------------------

Regler for betalingsspærring af kreditorfakturaer er angivet i oversigtspanelet **På hold** på siden **Betalingsbetingelser**. Hver regel har tre dele:

-   En brugerrolle, som f.eks. bogholder, regnskabschef eller controller. Kun brugere, der er tildelt den angivne rolle, kan spærre eller frigive en betaling i henhold til de angivne betalingsbetingelser.
-   Minimum antal dage, der lægges til fakturabetalingens forfaldsdato, når en bruger med den valgte rolle frigiver spærringen.
-   Det maks. antal gange, som bruger med den valgte rolle kan spærre en betaling på hver faktura. **Tip**! Hvis du vil tillade ubegrænsede spærringer, skal du angive et højt tal, f.eks. 9999.

For eksempel på Net 30 betalingsbetingelsen kan du oprette to regler, én for bogholdere og én til direktører. Reglen for bogholdere føjer mindst 30 dage til fakturabetalingens forfaldsdato, hvor spærringen frigives, og tillader maksimalt 3 spærringer på en faktura. Reglen for direktører føjer mindst 15 dage til forfaldsdatoen for betaling af fakturaen, med højst 10 spærringer på en faktura.

## <a name="when-can-i-place-and-release-vendor-invoice-payment-holds"></a>Hvornår kan jeg angive og frigive betalingsspærringer for kreditorfakturaer?
Spærringer kan angives og frigives i følgende situationer:

-   Betalingsbetingelser skal konfigureres for en kreditorfaktura, eller for alle kreditorfakturaer for en bestemt kreditor, før du kan angive en spærring.
-   For at angive eller frigive en spærring skal du være tildelt en brugerrolle, hvor der er konfigureret regler for betalingsspærringer.
-   Hvis en spærring er aktiv for en kreditor, kan du ikke frigive en spærring for en faktura for den samme kreditor. Først skal du frigive spærringen for kreditoren.
-   Du kan ikke frigive en spærring, medmindre du er den bruger, der angav spærringen, eller du er tildelt til den samme brugerrolle som den bruger, der angav spærringen.
-   Du kan ikke bogføre en kreditorfaktura, hvis den har en betalingsspærring. Spærringen skal først frigives.

## <a name="where-do-i-place-and-release-vendor-invoice-payment-holds"></a>Hvor angiver og frigiver jeg betalingsspærringer for kreditorfakturaer?
### <a name="for-a-vendor"></a>For en kreditor
Angiv eller frigiv en betalingsspærring for alle fakturaer for den valgte kreditor på siden **kreditorposteringer** eller siden **Udlign posteringer**. Hvis du angiver en betalingsspærring for en kreditor, omfatter denne spærring alle eksisterende fakturaer for den pågældende kreditor. Hvis du frigiver en betalingsspærring for en kreditor, frigives denne betalingsspærring kun for de kreditorfakturaer, der ikke har individuelle betalingsspærringer. For eksempel angiver du individuelle betalingsspærringer på to forskellige kreditorfakturaer for samme kreditor. Senere angiver du en betalingsspærring for den pågældende kreditor. Hvis du senere frigiver betalingsspærringen for den pågældende kreditor, frigives de individuelle spærringer for de to kreditorfakturaer ikke.

### <a name="for-a-vendor-invoice"></a>For en kreditorfaktura

Angiv eller frigiv en betalingsspærring for en enkelt faktura på siden **Kreditorfaktura** eller siden **Udlign posteringer**.

### <a name="for-a-posted-vendor-invoice"></a>For en bogført kreditorfaktura

Angiv eller frigiv en betalingsspærring for en bogført kreditorfaktura på siden **Fakturajournal**.

### <a name="for-all-vendor-invoices-associated-with-a-purchase-order"></a>For alle kreditorfakturaer, der er tilknyttet en indkøbsordre

Angiv eller frigiv en betalingsspærring for alle kreditorfakturaer, der er tilknyttet en indkøbsordre på siden **Udlign posteringer**.

## <a name="can-i-settle-an-invoice-that-is-on-hold"></a>Kan jeg udligne en faktura, der er spærret?
Hvis du er tildelt til den samme brugerrolle som den bruger, der angav spærringen, kan du fjerne spærringen fra siden **Udlign posteringer** og udligne kreditorfakturaen. Når du angiver en betalingsspærring, vælges indstillingen **Fakturabetaling på hold** automatisk under fanen **Betaling** på siden **Udlign posteringer**. Dette forhindrer, at en kreditorfaktura kan udlignes, før spærringen er frigivet.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]