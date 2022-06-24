---
title: Konsolidere forsendelser manuelt ved hjælp af siden Konsolider forsendelser
description: Denne artikel viser et scenarie, hvor der frigives flere ordrer til lagerstedet og derefter konsolideres senere ved hjælp af siden Konsolider forsendelser.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d24542a126d64621525f62e694bbc7174b474810
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897336"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Konsolidere forsendelser manuelt ved hjælp af siden Konsolider forsendelser

[!include [banner](../includes/banner.md)]

Denne artikel viser et scenarie, hvor der frigives flere ordrer til lagerstedet og derefter konsolideres senere ved hjælp af siden **Konsolider forsendelser**.

## <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Scenariet i denne artikel indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Konfigurere politikker for forsendelseskonsolidering og produktfiltre

I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der. Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.

## <a name="create-the-sales-orders-for-this-scenario"></a>Oprette salgsordrer til dette scenarie

Start med at oprette en samling salgsordrer, som du kan arbejde med. Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser. Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.

Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.

### <a name="create-sales-orders-1-and-2"></a>Oprette salgsordre 1 og 2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Pulje:** *ShipCons*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

### <a name="create-sales-orders-3-and-4"></a>Oprette salgsordre 3 og 4

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Pulje:** Lad feltet være tomt.

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

## <a name="release-the-orders-to-the-warehouse"></a>Frigive ordrerne til lagerstedet

Udfør følgende trin for at frigive hver salgsordre, du har oprettet i dette scenarie, til lagerstedet.

1. Gå til **Debitor \> Ordrer \> Alle salgsordrer**.
1. Find og vælg den salgsordre, der skal frigives.
1. I handlingsruden skal du på fanen **Lagersted** vælge **Handlinger \> Frigiv til lagersted** for at at frigive den valgte salgsordre.
1. Gentag denne procedure for hver anden salgsordre, du har oprettet for dette scenarie.

## <a name="consolidate-shipments"></a>Konsolider forsendelser

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg en forsendelse, der blev oprettet, da salgsordre 1 blev frigivet på lagerstedet. (Dens felt **Politik for forsendelseskonsolidering** skal angives til *Ordrepulje*.)
1. I handlingsruden skal du på fanen **Forsendelser** vælge **Forsendelser \> Konsolider forsendelser**.
1. Kontrollér de forsendelser, der foreslås til konsolidering. Der bør kun foreslås én forsendelse, der har samme politik, til konsolidering.
1. Luk siden **Forsendelseskonsolidering**.
1. Find og vælg en forsendelse, der blev oprettet, da salgsordre 3 blev frigivet på lagerstedet. (Dens felt **Politik for forsendelseskonsolidering** skal angives til *Standard*.)
1. I handlingsruden skal du på fanen **Forsendelser** vælge **Forsendelser \> Konsolider forsendelser**.
1. Kontrollér, at ingen forsendelser er blevet foreslået til konsolidering.
1. Vælg **Vis filtre**.
1. I ruden **Filtre** skal du du fjerne filtret **Ordrenummer** og derefter vælge **Anvend**.
1. Kontrollér de forsendelser, der foreslås til konsolidering. Der bør kun foreslås én forsendelse, der har samme politik, til konsolidering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)
- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]