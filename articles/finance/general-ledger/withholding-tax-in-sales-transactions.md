---
title: A-skat i salgstransaktioner
description: I dette emne kan du se, hvordan du undgår at beregne A-skat for udvalgte kunder. For kunder, der angiver A-skat i deres betalinger til dig, kan du tildele standardgruppen for A-skat.
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
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060716"
---
# <a name="withholding-tax-in-sales-transactions"></a>A-skat i salgstransaktioner

I dette emne kan du se, hvordan du undgår at beregne A-skat for udvalgte kunder. For kunder, der angiver A-skat i deres betalinger til dig, kan du tildele standardgruppen for **A-skattegruppe** på siden **Kunder**. 

1. Gå til **Navigationsrude > Moduler > Debitor > Kunder > Alle kunder**.

2. Klik på den pågældende debitorkonto, og klik på **Rediger**.

3. Angiv **Ja** i feltet **Beregn A-skat** på fanen **Faktura og levering**.

   > [!NOTE] 
   > A-skat beregnes ikke, hvis **Beregn A-skat** ikke er aktiveret for denne kunde i leverandør i masterdata.

4. Vælg en A-skattegruppe i **A-skattegruppen**.

5. Klik på **Gem**.

For varer/tjenester, der er ansvarlige for A-skat, kan du tildele standardgruppen for **Varer i A-skattegruppe** i **Frigivne produkter**.

1. Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.

2. Klik på det pågældende elementnummer og klik på **Rediger**.

3. Klik på **Beregn A-skat** på fanen **Sælg**.

   > [!NOTE] 
   > A-skat beregnes ikke, hvis **Beregn A-skat** ikke er angivet til **Ja** for denne vare under fanen **Sælg** på siden **Frigivet produkt**.

4. Vælg et element i A-skattegruppe på listen **Element i A-skattegruppe**.

5. Klik på **Gem**.

A-skattegrupper og A-skattegrupper for varer kan tildeles ved hjælp af siden **Salgsordre**. 

Standardgruppen for A-skat og A-skattegruppen for varer bruges som standardposter på salgsordrelinjer, når du opretter en ny salgsordre.

A-skat beregnes og bogføres sammen med **Debitorbetalingskladde**. Du kan manuelt justere den relevante kode for A-skat og det faktiske beløb for A-skat under fanen **A-skat** på siden **Afregn posteringer**.

Beløbet for den beregnede A-skat trækkes fra kundebetalingen og bogføres på kontoen for **A-skatteforskydning** i et relateret bilag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]