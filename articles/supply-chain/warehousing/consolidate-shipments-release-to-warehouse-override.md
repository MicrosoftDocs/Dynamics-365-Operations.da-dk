---
title: Konsolidere forsendelser, når politikken for forsendelseskonsolidering tilsidesættes
description: Dette emne viser et scenarie, hvor en eller flere salgslinjer skal frigives til lageret manuelt fra siden Frigiv til lager, og den systemdefinerede politik for forsendelseskonsolidering skal tilsidesættes før frigivelsen.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8b1c8ac41fe0941c9bbfce20ce593eafe5699ef1
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675453"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Konsolidere forsendelser, når politikken for forsendelseskonsolidering tilsidesættes

[!include [banner](../includes/banner.md)]

Dette emne viser et scenarie, hvor en eller flere salgslinjer skal frigives til lageret manuelt fra siden **Frigiv til lager**, og den systemdefinerede politik for forsendelseskonsolidering skal tilsidesættes før frigivelsen. Der kræves muligvis en tilsidesættelse af politikken for forsendelseskonsolidering, hvis f.eks. en ordre, der ikke normalt konsolideres med åbne forsendelser, skal konsolideres med åbne forsendelser.

I løbet af scenariet opretter du et sæt salgsordrer og overskriver derefter standardpolitikken for konsolidering af forsendelser, før du frigiver ordrerne til lageret.

## <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Konfigurere politikker for forsendelseskonsolidering og produktfiltre

I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der. Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.

## <a name="create-the-sales-orders-for-this-scenario"></a>Oprette salgsordrer til dette scenarie

1. Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret tre identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-002*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Frigive salgsordrer fra siden Frigiv til lager

Udfør følgende trin for at tilsidesætte politikken for forsendelseskonsolidering under frigivelsen til lageret.

1. Gå til **Lagerstyringssted \> Frigiv til lager \> Frigiv til lager**.
1. Vælg den første salgsordre, du har oprettet for dette scenarie, i den øverste rude.
1. Vælg **Tilføj** for at føje linjen til frigivelsen til lageret. Bemærk, at *standardpolitikken* for konsolidering af forsendelse anvendes i den nederste rude.
1. Vælg **Vælg ny politik for forsendelseskonsolidering** i nederste rude.
1. Vælg en politik, der giver mulighed for konsolidering med andre åbne forsendelser med samme politik. Vælg f.eks politikken *Kundeordrenr.*.
1. Vælg **Frigiv til lager**.
1. Vælg den anden og tredje salgsordre, du har oprettet for dette scenarie.
1. Vælg **Tilføj** for at føje linjerne til frigivelsen til lageret. Bemærk, at *standardpolitikken* anvendes i den nederste rude.
1. Vælg den anden linje, og vælg derefter **Kundeordrenr.** i feltet *Vælg ny politik for forsendelseskonsolidering*.
1. Vælg **Frigiv til lager** for begge linjer.

## <a name="verify-the-shipments"></a>Kontrollér forsendelserne

Der skal være oprettet to forsendelser:

- Den første forsendelse indeholder to linjer og er oprettet ved hjælp af *Kundeordrenr.*-politikken for forsendelseskonsolidering.
- Den anden forsendelse indeholder én linjer og er oprettet ved hjælp af *standardpolitikken* for forsendelseskonsolidering.

Udfør følgende trin for at gennemse de forsendelser, der er oprettet.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg den nødvendige forsendelse.
1. I feltet **Politik for forsendelseskonsolidering** kan du gennemse den konsolideringspolitik, der blev brugt ved oprettelsen af forsendelsen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)
- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]