---
title: Konsolidere forsendelser, når de frigives til lagerstedet, ved hjælp af automatisk frigivelse af salgsordrer
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den automatiserede procedure til periodisk frigivelse til lagersted.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 82a95ecf196ef7c33831da7f4d03df629b17fa53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807554"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a>Konsolidere forsendelser, når de frigives til lagerstedet, ved hjælp af automatisk frigivelse af salgsordrer

[!include [banner](../includes/banner.md)]

Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den automatiserede procedure til periodisk frigivelse til lagersted. Ordrerne vil automatisk blive konsolideret til forsendelser baseret på regler, der er defineret som politikker for forsendelseskonsolidering.

I løbet af scenariet opretter du sæt af salgsordrer og frigiver hvert sæt til lagerstedet. Derefter skal du gennemse de forsendelser, der er oprettet eller opdateret under forsendelseskonsolidering, baseret på de konfigurerede politikker.

## <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Konfigurere politikker for forsendelseskonsolidering og produktfiltre

I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der. Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.

## <a name="create-the-sales-orders-for-this-scenario"></a>Oprette salgsordrer til dette scenarie

Start med at oprette en samling salgsordrer, som du kan arbejde med. Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser. Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.

Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.

### <a name="create-order-set-1"></a>Opret ordresæt 1

#### <a name="sales-order-1-1"></a>Salgsordre 1-1

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Leveringsmåde:** *Airwa-Air*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-order-1-2"></a>Salgsordre 1-2

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Leveringsmåde:** *Airwa-Air*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-order-1-3"></a>Salgsordre 1-3

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Leveringsmåde:** *10*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

1. Tilføj en anden ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*
    - **Leveringsmåde:** *Airwa-Air*

### <a name="create-order-set-2"></a>Opret ordresæt 2

#### <a name="sales-orders-2-1-and-2-2"></a>Salgsordrer 2-1 og 2-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-002*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)
    - **Antal:** *1.00*

1. Tilføj en anden ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)
    - **Antal:** *1.00*
    - **Leveringsmåde:** *Airwa-Air*

### <a name="create-order-set-3"></a>Opret ordresæt 3

#### <a name="sales-order-3-1"></a>Salgsordre 3-1

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-002*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)
    - **Antal:** *1.00*

1. Tilføj en anden ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)
    - **Antal:** *1.00*
    - **Leveringsmåde:** *Airwa-Air*

> [!NOTE]
> Denne ordre er identisk med de to ordrer, du har oprettet for ordresæt 2. Men den er angivet som sin egen ordre, fordi du frigiver den på et senere tidspunkt i dette scenarie.

### <a name="create-order-set-4"></a>Opret ordresæt 4

#### <a name="sales-order-4-1"></a>Salgsordre 4-1

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Debitorrekvisition:** *1*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

### <a name="create-order-set-5"></a>Opret ordresæt 5

#### <a name="sales-orders-5-1-and-5-2"></a>Salgsordrer 5-1 og 5-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Debitorrekvisition:** *2*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-order-5-3"></a>Salgsordre 5-3

1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Debitorrekvisition:** *1*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

### <a name="create-order-set-6"></a>Opret ordresæt 6

#### <a name="sales-orders-6-1-and-6-2"></a>Salgsordrer 6-1 og 6-2

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-003*
    - **Debitorrekvisition:** *2*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Salgsordrer 6-3 og 6-4

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-004*
    - **Debitorrekvisition:** *1*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Salgsordrer 6-5 og 6-6

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Lokation:** *6*
    - **Lagersted:** *61*
    - **Pulje:** *ShipCons*

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Salgsordrer 6-7 og 6-8

1. Opret to identiske salgsordrer, der har følgende indstillinger:

    - **Debitorkonto:** *US-007*
    - **Lokation:** *6*
    - **Lagersted:** *61*
    - **Pulje:** Lad feltet være tomt.

1. Tilføj en ordrelinje, der har følgende indstillinger:

    - **Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)
    - **Antal:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatisk frigivelse af salgsordrer til lagerstedet

For hvert sæt af salgsordrer, du har oprettet tidligere, fuldfører du en procedure for automatisk frigivelse til lagerstedet. I hvert enkelt tilfælde kan du arbejde via [den procedure for frigivelse til lager](#release-procedure), der angives her.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Grundlæggende procedure for frigivelse til lager

For hvert sæt af salgsordrer, du har oprettet tidligere, skal du fuldføre de tre fremgangsmåder, der er beskrevet i følgende underafsnit.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Opdater den bølgeskabelon, der vil blive brugt under frigivelse

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Indstil feltet **Bølgeskabelontype** til *Forsendelse*.
1. Find og vælg den bølgeskabelon, der er knyttet til det lagersted, du har brugt i de ordresæt, du har oprettet for dette scenarie. Hvis du f.eks. brugte lagerstedet *24*, skal du vælge bølgeskabelonen **24 Standard for forsendelse**. Hvis du brugte lagerstedet *61*, skal du vælge bølgeskabelonen **61 Forsendelse**.
1. Vælg **Rediger** i handlingsruden.
1. Angiv indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** til *Nej*.

#### <a name="release-to-the-warehouse"></a>Frigiv til lagerstedet

1. Gå til **Lagerstedsstyring \> Frigiv til lagersted \> Automatisk frigivelse af salgsordrer**.
1. Angiv feltet **Antal til frigivelse** til *Alle*.
1. Gå til oversigtspanelet **Poster, der skal indgå**, og vælg **Filter** for at åbne forespørgselsdialogboksen.
1. Gå til fanen **Område**, og vælg **Tilføj** for at tilføje en række, der har følgende indstillinger, til gitteret:

    - **Tabel:** *Salgsordre*
    - **Afledt tabel:** *Salgsordre*
    - **Felt:** *Salgsordre*
    - **Kriterier:** Angiv en kommasepareret liste over salgsordrenumrene fra det ønskede ordresæt.

1. Vælg **OK** for at gemme forespørgslen.
1. Vælg **OK** for at starte proceduren *Automatisk frigivelse til lagersted*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Gennemse den forsendelse, der er oprettet eller opdateret

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg den nødvendige forsendelse.
1. Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.

### <a name="release-sales-orders-from-order-set-1"></a>Frigiv salgsordrer fra ordresæt 1

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 1.

Når du er færdig, burde du kunne se, at der er oprettet to forsendelser:

- Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.
- Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.

### <a name="release-sales-orders-from-order-set-2"></a>Frigiv salgsordrer fra ordresæt 2

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 2.

Når du er færdig, burde du kunne se, at der er oprettet tre forsendelser:

- Den første forsendelse indeholder *brændfarlige* varer.
- Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.

### <a name="release-sales-orders-from-order-set-3"></a>Frigiv salgsordrer fra ordresæt 3

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 3.

Når du er færdig, burde du kunne se, at følgende handlinger er sket:

- En eksisterende forsendelse (den forsendelse, der blev oprettet, da ordresæt 2 blev frigivet til lagerstedet) blev opdateret. Der er tilføjet en linje , hvor varen *brændbar* blev tilføjet.
- Der blev oprettet en ny forsendelse, som indeholder varen *Eksplosiv*.

### <a name="release-sales-orders-from-order-set-4"></a>Frigiv salgsordrer fra ordresæt 4

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 4.

Når du er færdig, burde du kunne se, at en eksisterende forsendelse (hvor feltet **Debitorrekvisition** er angivet til *1*) blev opdateret. Der blev føjet en ny linje til den.

### <a name="release-sales-orders-from-order-set-5"></a>Frigiv salgsordrer fra ordresæt 5

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 5.

Når du er færdig, burde du kunne se, at følgende handlinger er sket:

- En eksisterende forsendelse (hvor feltet **Debitorrekvisition** er angivet til *1*) blev opdateret. En linje fra salgsordren 5-3 (hvor feltet **Debitorrekvisition** er angivet til *1*) blev føjet til den.
- Der blev oprettet en ny forsendelse, hvor linjerne fra salgsordrerne 5-1 og 5-2 er grupperet i én forsendelse.

### <a name="release-sales-orders-from-order-set-6"></a>Frigiv salgsordrer fra ordresæt 6

Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 6.

Når du er færdig, burde du kunne se, at der er oprettet fire forsendelser:

- Linjer fra to ordrer på kunde *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra to ordrer på kunde *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 6-5 og 6-6 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 6-7 og 6-8 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)
- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]