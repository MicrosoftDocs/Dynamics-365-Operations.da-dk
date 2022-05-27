---
title: Pakningsstrategier for containere
description: I dette emne beskrives forskellene mellem pakningsstrategier for containere, og det indeholder eksempler.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab34cee7fd495ec26f6b20da2aa43895f49f677c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676377"
---
# <a name="container-packing-strategies"></a>Pakningsstrategier for containere

[!include [banner](../includes/banner.md)]

En *pakningsstrategi for containere* er en strategi, som du kan bruge til at definere varefordelinger på tværs af containere. I dette emne forklares forskellene mellem strategierne *Pak i alle åbne containere* og *Pak kun i aktuel container*.

- **Pak i alle åbne containere** – Systemet skal kontrollere alle åbne containere, der allerede er oprettet under containeriseringscyklussen, for at sikre, at varen kan være i en af dem. Under pakning kontrollerer systemet hver vare for at finde ud af, om den kan være i en af de tidligere oprettede containere. Hvis varen ikke kan være i en eksisterende container, opretter systemet en ny container og fortsætter, indtil det er færdig med at pakke hele ordren.

    *N* bestilte varer kræver for eksempel containerisering. Hver gang systemet behandler en vare, der ikke kan være i en eksisterende container, vil den i det tilfælde foretage i alt (\[(*n* - 1) × (*n* + 1)\] ÷ 2) kontroller for at vurdere, om varen kan være i de eksisterende containere.

- **Pak kun i aktuel container** – Systemet skal kun kontrollere den senest oprettede container for at sikre, at varen kan være i den. Under pakning kontrollerer systemet hver vare for at finde ud af, om den kan være i den senest oprettede container. Hvis varen ikke kan være i den pågældende container, opretter systemet en ny container og fortsætter, indtil det er færdig med at pakke hele ordren.

    *N* bestilte varer kræver for eksempel containerisering. I værste tilfælde vil systemet foretage i alt (*n* - 1) kontroller for at evaluere, om varen kan være i containerne.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Eksempel på flowet for pakningsstrategier for containere

Du skal konfigurere følgende varer for containerisering.

| Post | Fysiske dimensioner (bredde × dybde × højde) | Tykkelse |
|---|---|---|
| HDMI-kabel 6' | 1 × 1 × 1 | 1 |
| HDMI-kabel 12' | 2 × 1 × 1 | 1 |
| HDMI-kabel 18' | 3 × 1 × 1 | 2 |

Du skal også konfigurere følgende kasse, som skal bruges til pakning.

| Container | Fysiske dimensioner (længde × bredde × højde) | Tykkelse | Mængde |
|---|---|---|---|
| Mellemstor kasse | 6 × 3 × 2 | 10 | 100 |

Endelig skal du konfigurere en ordre med følgende produkter og antal.

| Salgsordrelinje | Mængde |
|---|---|
| HDMI-kabel 12' | 9 |
| HDMI-kabel 18' | 8 |
| HDMI-kabel 6' | 13 |

I følgende tabel opsummeres, hvordan containerisering fungerer, når du bruger strategien *Pak i alle åbne containere*, og når du kun bruger strategien *Pak kun i aktuel container*.

| Pak i alle åbne containere | Pak i aktuel container |
|---|---|
| <p>HDMI-kabel 12':</p><ol><li>Opret en ny container, CONT0001.</li><li>Anbring 9 ea i container CONT0001.</li></ol> | <p>HDMI-kabel 12':</p><ol><li>Opret en ny container, CONT0001.</li><li>Anbring 9 ea i container CONT0001.</li></ol> |
| <p>HDMI-kabel 18':</p><ol><li>Kontrollér, om varen kan være i container CONT0001.</li><li>Opret en ny container, CONT0002.</li><li>Anbring 5 ea i container CONT0002.</li><li>Opret en ny container, CONT0003.</li><li>Anbring 3 ea i container CONT0003.</li></ol> | <p>HDMI-kabel 18':</p><ol><li>Kontrollér, om varen kan være i container CONT0001.</li><li>Opret en ny container, CONT0002.</li><li>Anbring 5 ea i container CONT0002.</li><li>Opret en ny container, CONT0003.</li><li>Anbring 3 ea i container CONT0003.</li></ol> |
| <p>HDMI-kabel 6':</p><ol><li>Kontrollér, om varen kan være i container CONT0001.</li><li>Anbring 1 ea i container CONT0001.</li><li>Kontrollér, om varen kan være i container CONT0002.</li><li>Kontrollér, om varen kan være i container CONT0003.</li><li>Anbring 4 ea i container CONT0003.</li><li>Opret en ny container, CONT0004.</li><li>Anbring 8 ea i container CONT0004.</li></ol> | <p>HDMI-kabel 6':</p><ol><li>Kontrollér, om varen kan være i container CONT0003.</li><li>Anbring 4 ea i container CONT0003.</li><li>Opret en ny container, CONT0004.</li><li>Anbring 9 ea i container CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Eksempelscenario: Pak enkelte ordrer pr. container

I dette afsnit kan du se et scenarie, hvor systemet er konfigureret til at samle flere ordrer i én forsendelse. Der udføres derfor containerisering fra salgsordren for at sikre, at alle ordrer, der indeholder flere produkter, pakkes i sin egen container.

Denne funktionalitet giver dig mulighed for at håndtere scenarier, hvor du kun skal pakke én salgsordre i hver container, så distributionscenteret kan udføre cross-docking af fulde containere mellem detailforretninger. Ud over detailscenarierne (ordre pr. detailbutik og forsendelse til et distributionscenter til cross-docking) bruges denne teknik også ofte i lean forsyningskæder (salgsordre pr. just-in-time-produktionslinje).

Dette scenario viser, hvordan du kan reducere antallet af containere, der evalueres under pakning, ved hjælp af strategien *Pak kun i aktuel container* for containerisering.

### <a name="prerequisites"></a>Forudsætninger

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Aktivere funktionen Konsolider forsendelser i systemet

I dette scenario bruges funktionen *Konsolider forsendelser*. Hvis funktionen ikke allerede er tilgængelig i systemet, skal du aktivere den ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Dette scenarie indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.

### <a name="inspect-or-create-container-types"></a>Undersøge eller oprette containertyper

Benyt følgende fremgangsmåde for at undersøge containertyper eller oprette nye containertyper, hvis det er nødvendigt.

1. Gå til **Lagerstedsstyring** \> **Konfiguration** \> **Containere** \> **Containertyper**.
1. Kontrollér, at hver af følgende containertyper er tilgængelig i dine demodata. Rediger eller opret containertyper efter behov.

    - Containertype 1:

        - **Containertypekode:** *Kasse-Stor*
        - **Beskrivelse:** *Stor kasse*
        - **Maksimal nettovægt:** *100*
        - **Mængde:** *400*
        - **Længde:** *4*
        - **Bredde:** *10*
        - **Højde:** *10*

    - Containertype 2:

        - **Containertypekode:** *Kasse-Mellem*
        - **Beskrivelse:** *Mellemstor kasse*
        - **Maksimal nettovægt:** *50*
        - **Mængde:** *200*
        - **Længde:** *2*
        - **Bredde:** *10*
        - **Højde:** *10*

    - Containertype 3:

        - **Containertypekode:** *Kasse-Lille*
        - **Beskrivelse:** *Lille kasse*
        - **Maksimal nettovægt:** *20*
        - **Mængde:** *100*
        - **Længde:** *1*
        - **Bredde:** *10*
        - **Højde:** *10*

### <a name="inspect-or-create-container-groups"></a>Undersøge eller oprette containergrupper

Benyt følgende fremgangsmåde for at undersøge containergrupper eller oprette nye containergrupper, hvis det er nødvendigt.

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containergrupper**.
1. Kontrollér, at følgende containergrupper er tilgængelige i dine demodata. Hvis den ikke er tilgængelig, skal du vælge **Ny** for at oprette den.

    - **Containergruppe-id:** *Kasser*
    - **Beskrivelse:** *Kassestørrelser*

1. Kontroller, at følgende linjer findes, i oversigtspanelet **Detaljer** for containergruppen *Kasser*. Hvis ikke, skal du vælge **Ny** for at tilføje dem.

    - Linje 1:

        - **Løbenummer:** *1*
        - **Containertype:** *Kasse-Stor*
        - **Containerudnyttelse i procent:** *100*

    - Linje 2:

        - **Løbenummer:** *2*
        - **Containertype:** *Kasse-Mellem*
        - **Containerudnyttelse i procent:** *100*

    - Linje 3:

        - **Løbenummer:** *3*
        - **Containertype:** *Kasse-Lille*
        - **Containerudnyttelse i procent:** *100*

### <a name="create-a-new-container-build-template"></a>Oprette en ny containerbuildskabelon

Følg disse trin for at oprette en ny containerbuildskabelon:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Skabelon til container-build**.
1. Vælg **Ny** for at oprette en skabelon til containerbuild, der har følgende indstillinger:

    - **Løbenummer:** *1*
    - **Containerskabelon-id:** *Kasse*
    - **Containergruppe-id:** *Kasser*
    - **Grundlæggende forespørgselstyper:** *Salgsfordelingslinje*
    - **Kode for bølgetrin:** *234*
    - **Tillad opdeling af plukninger:** *Ja*
    - **Pakningsstrategi for containere:** *Pak kun i aktuel container*
    - **Pakning efter vejledningsenhed:** *Nej*

1. Mens rækken for den nye skabelon stadig er markeret, skal du vælge **Rediger forespørgsel** i handlingsruden.
1. Der vises en standarddialogboks med forespørgselseditoren. Vælg **Tilføj** under fanen **Sortering** for at tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Midlertidige arbejdstransaktioner*
    - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
    - **Felt:** *Ordrenummer*
    - **Søgeretning:** *Stigende*

    > [!IMPORTANT]
    > For at undgå at skulle tjekke alle de andre åbne containere og for at gøre processen hurtigere ved at kontrollere én container ad gangen, skal du bruge strategien *Pak kun i aktuel container* ud over sortering efter ordrenummer. Denne kombination vil fungere som en arbejdspause i en arbejdsskabelon.

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. Mens rækken for den nye skabelon stadig er markeret, skal du vælge **Begrænsninger i containerblanding** i handlingsruden.

    Du vil nu tilføje en begrænsning, der anbringer varer fra en enkelt ordre i en enkelt container. Varer fra en anden ordre anbringes i en separat container.

1. Vælg **Ny** for at oprette en blandingsbegrænsning, der har følgende indstillinger:

    - **Tabel:** *Salgsordrer*
    - **Vælg felt:** *SalesId* (Feltet vises som *Salgsordre* i gitteret).

1. Vælg **OK** for at tilføje begrænsningen.
1. Luk siden.

### <a name="set-up-a-wave-template-for-containerization"></a>Konfigurere en bølgeskabelon til containerisering

Følg disse trin for at konfigurere en bølgeskabelon.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. I listeruden skal du angive feltet **Bølgeskabelontype** til *Forsendelse*.
1. Vælg skabelonen **63 Containerisering** på listen.
1. Vælg **Rediger** i handlingsruden.
1. Find følgende linje i kolonnen **Valgte metoder** i oversigtspanelet **Metoder**:

    - **Metodenavn:** *containerisering*
    - **Navn:** *Containerisering*

1. Indstil feltet **Kode for bølgetrin** for linjen til *234*.

### <a name="set-up-a-work-template"></a>Opsætning af en arbejdsskabelon

Følg disse trin for at konfigurere en arbejdsskabelon.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Angiv feltet **Arbejdsordretype** til *Salgsordrer*.
1. Find og vælg den arbejdsskabelon, der skal bruges til pakning af enkelte ordrer pr. container, i gitteret **Oversigt**. I dette scenario skal du vælge skabelonen **63 Pluk til container**.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. Der vises en standarddialogboks med forespørgselseditoren. Tilføj følgende linjer under fanen **Sortering**:

    - Linje 1:

        - **Tabel:** *Midlertidige arbejdstransaktioner*
        - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
        - **Felt:** *Forsendelses-id*
        - **Søgeretning:** *Stigende*

    - Linje 2:

        - **Tabel:** *Midlertidige arbejdstransaktioner*
        - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
        - **Felt:** *Ordrenummer*
        - **Søgeretning:** *Stigende*

    - Linje 3:

        - **Tabel:** *Midlertidige arbejdstransaktioner*
        - **Afledt tabel:** *Midlertidige arbejdstransaktioner*
        - **Felt:** *Container-id*
        - **Søgeretning:** *Stigende*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. Du får vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?" Vælg **Ja** for at fortsætte.
1. Mens skabelonen **63 Pluk til container** stadig er valgt, skal du vælge **Opgaveoverskriften skifter** i handlingsruden.

    Du kan nu anvende indstillinger for at afbryde arbejdet, så hver container i ordren knyttes til én arbejdsordre.

1. Markér afkrydsningsfeltet **Gruppe efter dette felt** for hver række på siden **Opgaveoverskriften skifter** (**Forsendelses-id**, **Ordrenummer** og **Container-id**).
1. Luk siden.

### <a name="set-up-shipment-consolidation-policies"></a>Konfigurere politikker for forsendelseskonsolidering

Følg disse trin for at konfigurere en politik for forsendelseskonsolidering:

1. Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.
1. Indstil feltet **Politiktype** i listeruden til *Salgsordrer*.
1. Vælg politikken **Standard** på listen.
1. Vælg **Rediger** i handlingsruden.
1. Gå til oversigtspanelet **Konsolideringsfelter** på listen **Valgte felter**, vælg den række, hvor feltet **Feltnavn** er indstillet til *Ordrenummer*.
1. Vælg knappen **Fjern** ![venstre pil.](media/backward-button.png) For at flytte feltet til listen over **Resterende felter**.
1. Vælg **Gem** i handlingsruden.

### <a name="set-up-physical-dimensions-for-the-product"></a>Konfigurere fysiske dimensioner for produktet

Hvis du vil konfigurere fysiske dimensioner for de produkter, der skal bruges i dette scenario, skal du følge disse trin.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg det produkt, hvor feltet **Varenummer** er angivet til *A0001*.
1. I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.
1. På siden **Fysiske dimensioner** kan du se følgende linje i gitteret:

    - **Enhed:** *stk.*
    - **Bruttovægt:** *3,00*
    - **Bredde:** *2,00*
    - **Dybde:** *2,00*
    - **Højde:** *4,00*
    - **Mængde:** *16,00*

1. Luk siden.
1. Vælg det produkt, hvor feltet **Varenummer** er angivet til *A0002*.
1. I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.
1. På siden **Fysiske dimensioner** kan du se følgende linje i gitteret:

    - **Enhed:** *stk.*
    - **Bruttovægt:** *4,00*
    - **Bredde:** *3,00*
    - **Dybde:** *1,00*
    - **Højde:** *3,00*
    - **Mængde:** *9,00*

### <a name="create-sales-order-1"></a>Opret salgsordre 1

Følg disse trin for at oprette en salgsordre.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Der vises en dialogboks til oprettelse af en ny salgsordre. Angiv følgende værdier:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *63*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Tilføj følgende salgslinjer i oversigtspanelet **Salgsordrelinjer**:

    - Linje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *2*

    - Linje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *2*

1. Vælg den første linje, og vælg derefter **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reservér parti**. Luk derefter siden.
1. Gentag de to foregående trin for den anden linje.
1. Luk siden.

### <a name="create-sales-order-2"></a>Opret salgsordre 2

Følg disse trin for at oprette endnu en salgsordre.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Der vises en dialogboks til oprettelse af en ny salgsordre. Angiv følgende værdier:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *63*

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Tilføj følgende salgslinjer i oversigtspanelet **Salgsordrelinjer**:

    - Linje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *4*

    - Linje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *4*

1. Vælg den første linje, og vælg derefter **Lager \> Reservation**.
1. På siden **Reservation** skal du vælge **Reservér parti**. Luk derefter siden.
1. Gentag de to foregående trin for den anden linje.
1. Luk siden.

### <a name="create-the-load"></a>Oprette lasten

Udfør følgende trin for at oprette en last for hvert ordre, du har oprettet i dette scenarie, og frigiv den derefter til lagerstedet.

1. Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.
1. Under fanen **Salgslinjer** kan du finde og vælge alle salgsordrelinjer fra de salgsordrer, du har oprettet for dette scenario.
1. I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**. De valgte ordrelinjer føjes til en ny last.
1. I dialogboksen **Tildeling af lastskabelon** skal du gå til feltet **Lastskabelon-id** og vælge en lastskabelon, f.eks. *40' Container*.
1. Vælg **OK** for at lukke dialogboksen.
1. I sektionen **Laster** skal du vælge og finde den last, du lige har oprettet.
1. Vælg **Frigiv \> Frigiv til lagersted**.
1. I dialogboksen **Frigiv til lagersted** skal du vælge **OK** for at frigive den valgte last til lagerstedet.

### <a name="verify-the-shipments-and-containers"></a>Kontrollere forsendelser og containere

I følgende procedure kan du kontrollere de forsendelser, der er oprettet. Du kan bruge den til at gennemse den ordre, du har oprettet til dette scenario, for at sikre dig, at du har opnået de forventede resultater.

1. Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.
1. Find og vælg den forsendelse, der er oprettet for den last, du netop har frigivet.
1. Åbn fanen **Transport** i handlingsruden, og vælg **Vis containere**.
1. Bekræft, at varerne fra salgsordrerne er pakket i to forskellige containere.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Containerisering](wave-containerization.md)
