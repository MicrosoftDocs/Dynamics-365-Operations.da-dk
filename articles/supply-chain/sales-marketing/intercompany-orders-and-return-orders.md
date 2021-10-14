---
title: Interne ordrer og returordrer
description: Dette emne forklarer interne ordrer og returordrer
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548179"
---
# <a name="intercompany-orders-and-return-orders"></a>Interne ordrer og returordrer

[!include [banner](../../includes/banner.md)]

I dette emne beskrives, hvordan interne indkøbsordrer, salgsordrer, returvareordrer, købsaftaler og salgsaftaler oprettes og opdateres.

## <a name="about-intercompany-orders"></a>Om interne ordrer

Når du opretter en intern salgsordre, opretter Microsoft Dynamics 365 Supply Chain Management automatisk en tilsvarende indkøbsordre. Når du opretter en intern indkøbsordre, oprettes der ligeledes automatisk en tilsvarende intern salgsordre.

Det gælder for toleddede ordrer (transaktioner mellem to relaterede firmaer) og for de fleste treleddede firmaer (hvor en intern transaktion startes med en salgsordre til en ekstern kunde).

## <a name="intercompany-order-example"></a>Eksempel på intern ordre

Du har to relaterede firmaer. Firma A er en salgsvirksomhed, og firma B er en distributionsvirksomhed. Der oprettes automatisk interne salgsordrer og indkøbsordrer i følgende scenarier:

- Når firma A opretter en indkøbsordre, og leverandøren er firma B, oprettes der automatisk en intern salgsordre i firma B. Den toleddede ordrekæde består af en indkøbsordre i firma A og en intern salgsordre i firma B.
- Når firma B opretter en salgsordre, og kunden er firma A, oprettes der automatisk en intern indkøbsordre i firma A. Den toleddede ordrekæde består af en salgsordre i firma B og en intern indkøbsordre i firma A.
- Når firma A først opretter en salgsordre til en ekstern kunde, kan der automatisk oprettes en indkøbsordre i firma A. Det medfører automatisk oprettelse af en intern salgsordre i firma B. Den treleddede ordrekæde består af en salgsordre og en indkøbsordre i firma A og en intern salgsordre i firma B.

## <a name="about-intercompany-return-orders"></a>Om interne returordrer

Interne varer kan returneres på samme måde, som varer normalt returneres. I forbindelse med interne varer vil den eksterne kundes returordre oprette en intern indkøbsordre. Det fører til automatisk oprettelse af en intern salgsreturordre. Du kan også returnere en intern vare uden en returordre fra en ekstern kunde.

Interne returordrer, f.eks. almindelige returordrer, startes på siden **Opret returordre** .

I Microsoft Dynamics 365 Supply Chain Management opdateres interne salgs- og købsaftaler automatisk for at afspejle en returvare. Forpligtelsen ved salg- eller købsaftalen for varen justeres automatisk for at afspejle ændringerne i mængden eller beløbet, når en vare returneres.

## <a name="intercompany-return-order-example"></a>Eksempel på intern returordre

Firma A opretter en indkøbsordre, der er knyttet til en købsaftale for en intern vare. Der oprettes automatisk en intern salgsordre i firma B, der knyttes til den tilsvarende salgsaftale. Købsaftalen og salgsaftalen er relateret som interne aftaler.

Firma A returnerer den interne vare til firma B. Firma B opretter en returordre for varen, og der oprettes automatisk en købsreturvareordre i firma A. De forpligtelser, der er knyttet til de oprindelige ordrer i både købsaftalen og salgsaftalen justeres automatisk for at afspejle ændringen i mængde eller beløb.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
