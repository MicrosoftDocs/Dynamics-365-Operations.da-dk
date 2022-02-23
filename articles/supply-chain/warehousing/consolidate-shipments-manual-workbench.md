---
title: Konsolidere forsendelser ved hjælp af panelet for forsendelseskonsolidering
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet, hvorefter disse senere konsolideres til forsendelser ved hjælp af panelet for forsendelseskonsolidering.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9d0a2671e18603f701d343a4150128a04c626952
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963379"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidere forsendelser ved hjælp af panelet for forsendelseskonsolidering

[!include [banner](../includes/banner.md)]

Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet, hvorefter disse senere konsolideres til forsendelser ved hjælp af panelet for forsendelseskonsolidering.

## <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Konfigurere politikker for forsendelseskonsolidering og produktfiltre

I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der. Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>Slå funktionen til manuel forsendelseskonsolidering til

Før du kan bruge funktionen *Manuel forsendelseskonsolidering*, skal du slå den til i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Manuel forsendelseskonsolidering*

Som det blev nævnt i [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md), skal du også aktivere funktionen *Konsolider forsendelse*, før du kan oprette politikker. Du skal dog allerede have fuldført dette trin.

## <a name="create-the-sales-orders-for-this-scenario"></a>Oprette salgsordrer til dette scenarie

Start med at oprette en samling salgsordrer, som du kan arbejde med. Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser. Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.

Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.

### <a name="create-order-set-1"></a>Opret ordresæt 1

#### <a name="sales-orders-1-1-and-1-2"></a>Salgsordrer 1-1 og 1-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Leveringsmåde:** *Airwa-Air*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-order-1-3"></a>Salgsordre 1-3

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Leveringsmåde:** *10*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.
1. Tilføj en anden ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*
    - **Leveringsmåde:** *Airwa-Air*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.

### <a name="create-order-set-2"></a>Opret ordresæt 2

#### <a name="sales-orders-2-1-and-2-2"></a>Salgsordrer 2-1 og 2-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-002*
    - **Leveringsmåde:** *Airwa-Air*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.
1. Tilføj en anden ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)
    - **Antal:** *1.00*
    - **Leveringsmåde:** *Airwa-Air*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.

### <a name="create-order-set-3"></a>Opret ordresæt 3

#### <a name="sales-orders-3-1-and-3-2"></a>Salgsordrer 3-1 og 3-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Debitorrekvisition:** *1*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-orders-3-3-and-3-4"></a>Salgsordrer 3-3 og 3-4

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Debitorrekvisition:** *2*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

### <a name="create-order-set-4"></a>Opret ordresæt 4

#### <a name="sales-orders-4-1-and-4-2"></a>Salgsordrer 4-1 og 4-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-003*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-orders-4-3-and-4-4"></a>Salgsordrer 4-3 og 4-4

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-004*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-orders-4-5-and-4-6"></a>Salgsordrer 4-5 og 4-6

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Lokation:** *6*
    - **Lagersted:** *61*
    - **Pulje:** *ShipCons*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-orders-4-7-and-4-8"></a>Salgsordrer 4-7 og 4-8

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Lokation:** *6*
    - **Lagersted:** *61*
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

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidere forsendelserne ved hjælp af panelet for forsendelseskonsolidering

1. Gå til **Lagerstyringssted \> Frigiv til lagersted \> Frigiv til forsendelseskonsolidering**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Gå til dialogboksen for forespørgselseditor, og vælg **Tilføj** på fanen **Område** for at tilføje en række, der har følgende indstillinger, til gitteret:

    - **Tabel:** *Salgsordrer*
    - **Felt:** *Salgsordre*
    - **Kriterier:** Angiv en kommasepareret liste over salgsordrenumrene for hvert ordresæt, du har oprettet for dette scenarie.

1. Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.
1. Vælg **Konsolider forsendelser** i handlingsruden.
1. Vælg alle forsendelserne, og vælg derefter **Konsolider** i handlingsruden.

## <a name="verify-the-shipments"></a>Kontrollér forsendelserne

I følgende procedure kan du kontrollere de forsendelser, der er oprettet eller opdateret som resultat af forsendelseskonsolidering. Brug den til at gennemgå de ordresæt, du har oprettet for dette scenario, og gennemse derefter de underafsnit, der følger efter, for at sikre, at du har opnået de forventede resultater.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg den nødvendige forsendelse.
1. Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.

### <a name="related-shipments-for-order-set-1"></a>Relaterede forsendelser for ordresæt 1

Der skal være oprettet to forsendelser:

- Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.
- Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.

### <a name="related-shipments-for-order-set-2"></a>Relaterede forsendelser for ordresæt 2

Der skal være oprettet tre forsendelser:

- Den første forsendelse indeholder *brændfarlige* varer.
- Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.

### <a name="related-shipments-for-order-set-3"></a>Relaterede forsendelser for ordresæt 3

Der skal være oprettet to forsendelser:

- Den første forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *1*.
- Den anden forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *2*.

### <a name="related-shipments-for-order-set-4"></a>Relaterede forsendelser for ordresæt 4

Der skal være oprettet fire forsendelser:

- Linjer fra to ordrer på kunde *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra to ordrer på kunde *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 4-5 og 4-6 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 4-7 og 4-8 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)
- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)
