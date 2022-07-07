---
title: Udføre fakturaopdateringer til returneringer
description: Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32a108694c11a2ebd922a71d5c82691584bbb397
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014743"
---
# <a name="perform-invoice-updates-for-returns"></a>Udføre fakturaopdateringer til returneringer 

[!include [banner](../includes/banner.md)]


En returordre en form for salgsordre, der er markeret som en returneret ordre. Listesiden **Alle salgsordrer** bruges derfor til at oprette fakturaer for returordrer i stedet for formularen **Returordrer**. Denne funktion understøtter forretningsprocesserne i organisationer, der vælger at fakturere returordrer og salgsordrer samtidig og af samme person.

Da fakturaen for en returneret vare til et negativt beløb, kaldes det en kreditnota.

Når du konfigurerer fakturaopdateringen til batchafvikling, skal salgsordren af typen **Returordre** have statussen **Modtaget** for returlinjen, hvilket angiver, at ordrens følgeseddel er opdateret.

## <a name="post-an-invoice-for-a-return-order"></a>Bogføre en faktura for en returvareordre

1.  Klik på **Debitor** \> **Ordrer** \> **Alle salgsordrer**.

2.  Vælg en salgsordre, som **Returordre** vises for i feltet **Ordretype**.

3.  Klik på **Faktura** i gruppen **Generer** under fanen **Faktura** i handlingsruden.

4.  Vælg fanen **Parametre** i dialogboksen **Bogføring**.

5.  Gennemse oplysningerne i formen, og foretag de nødvendige ændringer.

6.  Klik på **OK**. Kreditnoten bogføres.

## <a name="see-also"></a>Se også

[Følgeseddelopdateringer til returneringer](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]