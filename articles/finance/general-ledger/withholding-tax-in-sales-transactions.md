---
title: A-skat i salgstransaktioner
description: I dette emne kan du se, hvordan du undgår at beregne A-skat for udvalgte kunder. For kunder, der angiver A-skat i deres betalinger til dig, kan du tildele standardgruppen for A-skat.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b221fc04ef82f148846fc0c282f6c8601f0eb4759d99a8dee02256cc0d42417f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747077"
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