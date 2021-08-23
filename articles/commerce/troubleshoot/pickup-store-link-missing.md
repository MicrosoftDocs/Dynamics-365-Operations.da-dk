---
title: Afhentningsindstillingen vises ikke på sider med oplysninger om indkøbsvogn eller produkt
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når indstillingen for afhentning i butikken ikke vises på siden med indkøbsvognen eller produktdetaljer.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 836f767caae8e32c156a1c13d1e2864a4d3cdd92e7a11814a2585c9e907575dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733815"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>"Afhentningsindstillingen" vises ikke på sider med oplysninger om indkøbsvogn eller produkt

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når indstillingen for afhentning i butikken ikke vises på siden med indkøbsvognen eller produktdetaljer.

## <a name="description"></a>Betegnelse

Knappen **Afhent** vises ikke på sider med oplysninger om indkøbsvogn eller produkt.

I følgende illustration vises et eksempel på en side, der indeholder knappen **Afhent**.

![Knappen Afhent.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Løsning

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Aktivere BOPIS-filtypenavnet i Commerce Site Builder

Hvis du vil aktivere filtypen "køb online, hent op i butikken" (BOPIS) i Commerce site builder, skal du følge disse trin.

1. Vælge dit websted.
1. Vælg **Webstedsindstillinger**, og vælg derefter **Udvidelse**.
1. Kontroller, at indstillingen **Deaktiver BOPIS** er fjernet.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Konfigurere leveringsmåder i Commerce Headquarters

Følg disse trin for at konfigurere leveringstilstande i Commerce Headquarters.

1. Gå til **Indkøb og forsyning \> Opsætning \> Leveringstilstande**.
1. Kontroller, at der oprettet en **Kundeafhentning**, og at der er knyttet produkter og adresser til den.
1. Gå til **Retail og Commerce \> Headquarters setup \> Parametre**.
1. Vælg **Kundeordrer** i navigationsruden til venstre.
1. Sørg for, **Levering gennem afhentning** er konfigureret korrekt.

### <a name="configure-customer-orders-payments"></a>Konfigurere debitorordrebetalinger

Følg disse trin for at konfigurere kundeordrebetalinger i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Headquarters setup \> Parametre**.
1. Vælg **Kundeordrer** i navigationsruden til venstre.
1. Kontroller, at felterne **Betalingsbetingelser** og **Betalingsmetoder** på oversigtspanelet **Betalinger** er angivet korrekt.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere BOPIS](../cpe-bopis.md)

[Aktivere flere leveringsmåder for afhentning af kundeordrer](../multiple-pickup-modes.md)

[Omni-kanalers Commerce-ordrebetalinger](../dev-itpro/commerce-payments.md)

[Butiksvælgermodul](../store-selector.md)
