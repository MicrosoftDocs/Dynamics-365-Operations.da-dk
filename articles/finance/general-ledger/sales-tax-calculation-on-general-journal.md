---
title: Beregning af moms på finanskladdelinjer
description: Dette emne forklarer, hvordan der beregnes moms for forskellige typer konti (kreditor, debitor, finans og projekt) på finanskladdelinjer.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 25eb8dd6965f659f0febe53a6340cb1381c5664f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204900"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Beregning af moms på finanskladdelinjer
[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan der beregnes moms for forskellige typer konti (kreditor, debitor, finans og projekt) på finanskladdelinjer.

Processen kan opdeles i tre trin:

- Fastsætte momsretningen.

- Fastsætte det momsbeløb, der skal gemmes en midlertidig momstabel.

- Fastsætte momsbeløbet og kontoen på bilaget.

## <a name="determine-the-sales-tax-direction"></a>Fastsætte momsretningen

Den måde, som momsretningen fastsættes på, afhænger af kontotypen i bilaget. Momsretningen bestemmes af kombinationen af kontotype og momskode. I følgende afsnit beskrives mulighederne mere detaljeret. 

### <a name="account-type-is-project"></a>Kontotype er Projekt

Hvis et bilag har en kladdelinje, hvor kontotypen er **Projekt**, anvender alle kladdelinjerne i bilaget samme momsretning. Følgende illustration viser reglen. Følgende punkter viser de mulige momsretninger for projektkonti.

• Hvis momskoden er importmoms, er momsretningen Importmoms.

• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.

• Hvis momskoden er ekstern moms, er momsretningen Udgående moms.

• Hvis momskoden er modtagermoms, er momsretningen Udgående moms.

Ellers bruges momsretningen Indgående moms.

I følgende diagram vises reglen grafisk.

![Muligheder for momsretning for projektkonti](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Kontotype er Kreditor

Hvis et bilag har en kladdelinje, hvor kontotypen er **Kreditor**, anvender alle kladdelinjerne i bilaget samme momsretning. Følgende punkter viser de mulige momsretninger for kreditorkonti. 

• Hvis momskoden er importmoms, er momsretningen Importmoms.

• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.

• Hvis momskoden er ekstern moms, er momsretningen Udgående moms.

• Hvis momskoden er modtagermoms, er momsretningen Udgående moms.

Ellers bruges momsretningen Indgående moms.

I følgende diagram vises reglen grafisk.

![Muligheder for momsretning for kreditorkonti](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Kontotype er Debitor

Hvis et bilag har en kladdelinje, hvor kontotypen er **Debitor**, anvender alle kladdelinjerne i bilaget samme momsretning. Følgende punkter viser de mulige momsretninger for debitorkonti.

• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.

• Hvis momskoden er ekstern moms, er momsretningen Indgående moms.

• Hvis momskoden er modtagermoms, er momsretningen Indgående moms.

Ellers bruges momsretningen Udgående moms.

I følgende diagram vises reglen grafisk.

![Muligheder for momsretning for debitorkonti](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Kontotype er Finans

I følgende illustration vises den regel, der gælder, når et bilag kun har kladdelinjer, hvor kontotypen er **Finans**. Følgende punkter viser de mulige momsretninger for finanskonti.

• Hvis momskoden er importmoms, er momsretningen Importmoms.

• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.

Ellers bruges momsretningen Indgående moms, hvis kladdebeløbet er debet (positiv). Hvis kladdebeløbet er kredit (negativt), er momsretningen Udgående moms.

I følgende diagram vises reglen grafisk.

![Muligheder for momsretning for finanskonti](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Tilsidesætte momsretningen

Du kan tilsidesætte momsretningen, når bilaget kun indeholder linjer, hvor kontotypen er **Finans**.

Gå til **Finans \> Kontoplan \> Konti \> Hovedkonti**, og vælg oversigtspanelet **Tilsidesættelser af juridisk enhed**.

## <a name="determine-the-sales-tax-amount"></a>Fastsætte momsbeløbet

I dette afsnit beskrives, hvordan momsbeløbs fortegn beregnes.

![Siden Momstransaktioner](media/sales-tax-amount-sign.jpg)

Følgende tabel indeholder den generelle regel til bestemmelse af fortegn på momsbeløb i den midlertidige momstabel.

| Kladdelinjebeløb | Momsretning  | Fortegn for momsbeløb |
|---------------------|----------------------|-----------------------|
| Positiv            | Indgående moms | Positiv              |
| Positiv            | Udgående moms    | Negativ              |
| Negativ            | Indgående moms | Negativ              |
| Negativ            | Udgående moms    | Positiv              |

Der findes en særlig regel for bilag, der kun indeholder **Projekt**- eller **Finans**-linjer, når der er valgt en momsgruppe eller varemomsgruppe på **Finans**-linjen. Denne regel styres ved at aktivere den uafhængige momsberegningsfunktion for finanskladder. Når denne funktion er deaktiveret, bruger momsbeløbet i **Finans**-linjen debet- og kreditretningen for **Projekt**-linjen. Når denne funktion er aktiveret, bruger momsbeløbet i **Finans**-linjen egen debet- og kreditretning. I følgende tabeller vises reglen for de enkelte scenarier. 

**Regel, når funktionen er slåer til**

| Kladdelinjebeløb i projekt | Momsretning  | Fortegn for momsbeløb |
|--------------------------------|----------------------|-----------------------|
| Positiv                       | Indgående moms | Positiv              |
| Negativ                       | Indgående moms | Negativ              |

**Regel, når funktionen er slåer fra**

| Kladdelinjebeløb i finans  | Momsretning  | Fortegn for momsbeløb |
|--------------------------------|----------------------|-----------------------|
| Positiv                       | Indgående moms | Positiv              |
| Negativ                       | Indgående moms | Negativ              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Fastsætte momsbeløbet og kontoen på bilaget

Når du bogfører moms, hentes hovedkontoen fra finanskonteringsgruppeprofilen. Når moms er indgående, bruger systemet den indgående momskonto, der er angivet i profilen. Når udgående moms bruger systemet den udgående momskonto, der er angivet i profilen.

I følgende tabel vises den generiske regel.

| Momsretning  | Fortegn for momsbeløb | Momskonto      | Beløb på bilag |
|----------------------|-----------------------|------------------------|-------------------|
| Indgående moms | Positiv              | Indgående momskonto | Positiv (debet)  |
| Indgående moms | Negativ              | Indgående momskonto | Negativ (kredit)  |
| Udgående moms    | Positiv              | Udgående momskonto    | Negativ (kredit)  |
| Udgående moms    | Negativ              | Udgående momskonto    | Positiv (debet)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]