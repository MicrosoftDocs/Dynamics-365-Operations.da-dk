---
title: Udføre fakturaopdateringer til returneringer
description: Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d3b884d1ed11d2f79e968a5a099860486ef600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810648"
---
# <a name="perform-invoice-updates-for-returns"></a>Udføre fakturaopdateringer til returneringer 

[!include [banner](../includes/banner.md)]


En returordre en form for salgsordre, der er markeret som en returneret ordre. Listesiden **Alle salgsordrer** bruges derfor til at oprette fakturaer for returordrer i stedet for formularen **Returordrer**. Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person.

Da fakturaen for en returneret vare til et negativt beløb, kaldes det en kreditnota.

Når du konfigurerer fakturaopdateringen til batchafvikling, skal salgsordren af typen **Returordre** have statussen **Modtaget** for returlinjen, hvilket angiver, at ordrens følgeseddel er opdateret.

## <a name="post-an-invoice-for-a-return-order"></a>Bogføre en faktura for en returvareordre

1.  Klik på **Debitor** \> **Almindelige** \> **Salgsordrer** \> **Alle salgsordrer**.

2.  Vælg en salgsordre, som **Returordre** vises for i feltet **Ordretype**.

3.  Klik på **Faktura** i gruppen **Generer** under fanen **Faktura** i handlingsruden.

4.  Vælg fanen **Parametre** i dialogboksen **Bogføring**.

5.  Gennemse oplysningerne i formen, og foretag de nødvendige ændringer.

6.  Klik på **OK**. Kreditnoten bogføres.

## <a name="see-also"></a>Se også

[Følgeseddelopdateringer til returneringer](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]