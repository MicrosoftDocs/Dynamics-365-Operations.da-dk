---
title: Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den samme last, som derefter konsolideres automatisk i forsendelser.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 58a1f6237e37815dd0b4ae3d7a0d46157db5a808
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831332"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a>Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning

[!include [banner](../includes/banner.md)]

Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den samme last, som derefter konsolideres automatisk i forsendelser.

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

1. Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.

#### <a name="sales-order-1-2"></a>Salgsordre 1-2

1. Opret salgsordre, der har følgende indstillinger:

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

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Brug panelet for lastplanlægning til at oprette laster og frigive dem til lagerstedet

Udfør følgende trin for at oprette en last for hvert ordresæt, du har oprettet i dette scenarie, og frigiv det derefter til lagerstedet.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Under fanen **Salgslinjer** kan du finde og vælge alle salgsordrelinjer fra et af de ordresæt, du har oprettet for dette scenario.
1. I handlingsruden kan du under fanen **Udbud og efterspørgsel** vælge **Føj \> Til ny last** for at føje de valgte ordrelinjer til en ny last.
1. I dialogboksen **Tildeling af lastskabelon** skal du i feltet **Lastskabelon-id** vælge en lastskabelon, f.eks. *Standardlastskabelon*.
1. Vælg **OK** for at lukke dialogboksen. 
1. I sektionen **Laster** skal du vælge og finde den last, du lige har oprettet.
1. Vælg **Frigiv \> Frigiv til lagersted** for at frigive den valgte last til lagerstedet.
1. Gentag denne procedure for de øvrige tre ordresæt, du har oprettet for dette scenarie.

## <a name="verify-the-shipments"></a>Kontrollér forsendelserne

I følgende procedure kan du kontrollere de forsendelser, der er oprettet eller opdateret som resultat af forsendelseskonsolidering. Brug den til at gennemgå de ordresæt, du har oprettet for dette scenario, og gennemse derefter de underafsnit, der følger efter, for at sikre, at du har opnået de forventede resultater.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg den nødvendige forsendelse.
1. Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.

### <a name="release-order-set-1-in-one-load"></a>Frigiv ordresæt 1 i en last

Der skal være oprettet to forsendelser:

- Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.
- Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.

### <a name="release-order-set-2-in-one-load"></a>Frigiv ordresæt 2 i en last

Der skal være oprettet tre forsendelser:

- Den første forsendelse indeholder de *brændfarlige* varer.
- Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.

### <a name="release-order-set-3-in-one-load"></a>Frigiv ordresæt 3 i en last

Der skal være oprettet to forsendelser:

- Den første forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *1*.
- Den anden forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *2*.

### <a name="release-order-set-4-in-one-load"></a>Frigiv ordresæt 4 i en last

Der skal være oprettet fire forsendelser:

- Linjer fra to ordrer på kundekonto *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra to ordrer på kundekonto *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 4-5 og 4-6 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.
- Linjer fra salgsordrer 4-7 og 4-8 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md)
- [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]