---
title: A-skat i indkøbstransaktioner
description: For kreditorer, der skal betale A-skat, kan du tildele standardgruppen for **A-skat** på siden **Alle kreditorer**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06997e2d6b47d867e014a7d493d91015c78a5e04
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060714"
---
# <a name="withholding-tax-in-purchase-transactions"></a>A-skat i indkøbstransaktioner

For kreditorer, der skal betale A-skat, kan du tildele standardgruppen for **A-skat** på siden **Alle kreditorer**.

1. Gå til **Navigationsruden > Moduler > Kreditor > Kreditorer > Alle kreditorer**.

2. Klik på den pågældende kreditorkonto, og klik på **Rediger**.

3. Angiv **Ja** i feltet **Beregn A-skat** på fanen **Faktura og levering**.

   > [!NOTE] 
   > A-skat beregnes ikke, hvis **Beregn A-skat** ikke er aktiveret for denne leverandør i dataene.

4. Vælg en A-skattegruppe i **A-skattegruppen**.

5. Klik på **Gem**.

For varer/tjenester, der er ansvarlige for A-skat, kan du tildele standardgruppen for **Varer i A-skattegruppe** i **Frigivne produkter**.

1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.

2. Klik på det pågældende elementnummer og klik på **Rediger**.

3. Klik på **Beregn A-skat** på fanen **Køb**.

   > [!NOTE] 
   > A-skat beregnes ikke, hvis **Beregn A-skat** ikke er angivet til **Ja** for denne vare under fanen **Indkøb** på siden **Frigivet produkt**.

4. Vælg et element i A-skattegruppe på listen **Element i A-skattegruppe**.

5. Klik på **Gem**.

A-skattegrupper og A-skattegrupper for varer kan tildeles på sider: 

- **Indkøbsordre**
- **Kreditorfaktura**
- **Fakturajournal**

Standardgruppen for A-skattegruppe og A-skattegruppen for varer overføres til linjerne, når der oprettes **Indkøbsordrer** og/eller **Ventende kreditorfakturaer**. I forbindelse med **Kreditorfakturakladde** kan du skifte til **Beregn A-skat** og vælge **Element i A-skattegruppe** på fanen **Generelt** i kladden.

Det midlertidige beløb for A-skat er tilgængeligt i feltet **Reguleret A-skat** på fanen **Totaler** på siden **Indkøbsordre**.

![A-skat medtages på indkøbsordren](media/withholding-tax-adjusted.png)

A-skat beregnes på **leverandørbetalingskladde**. Du kan manuelt justere de relevante koder for A-skat og de faktiske beløb for A-skat under fanen **A-skat** på siden **Afregn posteringer**.

![A-skat kan reguleres manuelt på siden Udlign posteringer](media/withholding-tax-vendor-payment-tab.png)

Beløbet for den afledte A-skat trækkes fra kreditorbetalingen og bogføres på kontoen for **A-skattekonto** i et relateret bilag.

![A-skattekonto, der viser et relateret bilag](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]