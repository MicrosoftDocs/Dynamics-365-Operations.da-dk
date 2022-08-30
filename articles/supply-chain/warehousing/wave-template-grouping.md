---
title: Bølgeskabelongruppering
description: Gruppering af bølgeskabeloner gør, at systemet kan bruge opsætninger af bøgeskabeloner til at bestemme, baseret på kriterier, du definerer, hvordan den skal opdele frigivne linjer og tildele dem til nye eller eksisterende bølger. Denne funktion kan være nyttig i lagre, hvor bølger oprettes på basis af bestemte kriterier, men hvor lederne foretrækker at oprette bølger automatisk i stedet for manuelt.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a48e6a81299badf4b811e1cf905beb06099e5a24
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335969"
---
# <a name="wave-template-grouping"></a>Bølgeskabelongruppering

[!include [banner](../includes/banner.md)]

Gruppering af bølgeskabeloner gør, at systemet kan bruge opsætninger af [bøgeskabeloner](tasks/configure-wave-processing.md) til at bestemme, baseret på kriterier, du definerer, hvordan den skal opdele frigivne linjer og tildele dem til nye eller eksisterende bølger. Denne funktion kan være nyttig i lagre, hvor bølger oprettes på basis af bestemte kriterier, men hvor lederne foretrækker at oprette bølger automatisk i stedet for manuelt. Det gør det muligt for systemet at føje hver nyligt frigivet forsendelse til den første bølge, der findes, og som har tilsvarende værdier i grupperingsfeltet. Hvis der ikke findes et match, opretter systemet en ny bølge til den nye forsendelse.

> [!IMPORTANT]
> Gruppering af bølgeskabeloner understøttes ikke for arbejdstyperne *valg af råmateriale til produktion* eller *kanban-plukning*. Det skyldes, at bølgegruppering er baseret på forsendelser, og at disse arbejdstyper ikke bruger forsendelser.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Slå funktionen til gruppering af bølgeskabeloner til

Før du kan bruge funktionen *Gruppering af bølgeskabeloner*, skal den være aktiveret for dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Gruppering af bølgeskabeloner*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Angiv en bølgeskabelon til at bruge gruppering af bølgeskabeloner

Hvis du vil gøre gruppering af bølgeskabeloner tilgængelig, skal du følge disse trin til at konfigurere din [bølgeskabelon](tasks/configure-wave-processing.md).

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Vælg den bølgeskabelon, der skal konfigureres, i ruden til venstre. Hvis du forbedrer at arbejde via scenariet senere i denne artikel ved hjælp af demodata, skal du vælge **62 Standard for forsendelse**.
1. Vælg **Rediger** for at sætte siden i redigeringstilstand.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Automatiser vølgeoprettelse:** *Ja*
    - **Tildel til åbne bølger:** *Ja*
    - **Udfør behandling af bølgen ved frigivelse til lagerstedet:** *Nej*

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgslen.
1. Gennemgå sorteringskriterierne under fanen sortering i dialogboksen **Forespørgsel**, og sørg for, at der findes en regel, der omfatter det felt, du vil bruge til at gruppere dine bølger.

    Hvis du forbereder at arbejde gennem scenariet med demonstrationsdata, skal du tilføje en række, der har følgende værdier:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Fragttjeneste*

        > [!NOTE]
        > Når du har valgt denne værdi, får du muligvis vist følgende meddelelse: "Feltet Fragttjeneste er ikke et indeksfelt. Vil du tilføje sortering på dette?" Vælg **Ja** for at tilføje sortering.

    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at gemme dine ændringer og lukke forespørgselsdialogboksen.
1. Gå til handlingsruden, og vælg **Gruppering af bølgeskabeloner**.
1. På siden **Gruppering af bølgeskabeloner** skal du markere afkrydsningsfeltet **Gruppér efter** efter for hver række, du vil bruge til at gruppere ordrelinjerne i bølger efter behov. Hvis du forbereder at arbejde dig gennem scenariet med demonstrationsdata, skal du markere afkrydsningsfeltet **Gruppér efter** for rækken *Fragttjeneste*.
1. Vælg **Gem**.
1. Luk siden **Gruppering af bølgeskabeloner**.
1. Vælg **Gem** for at gemme skabelonen.

## <a name="scenario"></a>Scenario

Dette afsnit indeholder et script, som du kan arbejde med for at finde ud af, hvad funktionen gør, og hvordan du arbejder med den.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge dette scenarie som vejledning til brug af funktionen, når du arbejder i et produktionssystem. Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.

### <a name="scenario-wave-template-grouping"></a>Scenarie: gruppering af bølgeskabeloner

I dette scenarie vises, hvordan du kan bruge gruppering af bølgeskabeloner til automatisk at oprette flere bølger baseret på grupperingskriterier, der er defineret i en bølgeskabelon. I dette scenarie er bølgeskabelonen konfigureret i systemet, så der oprettes en bølge pr. fragttjeneste.

Før du går i gang, skal du forberede din bølgeskabelon som beskrevet i afsnittet [Angiv en bølgeskabelon til at bruge gruppering af bølgeskabeloner](#set-up-template) tidligere i denne artikel. Hvis du vil arbejde med demonstrationsdata i dette scenarie, skal du sørge for at bruge de demonstrationsdatasværdier, der er foreslået i den pågældende procedure. Denne indstilling vil gruppere dine bølger efter den fragtmand, der er angivet for hver salgsordre.

#### <a name="create-sales-order-1"></a>Opret salgsordre 1

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-004*.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.

1. Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.
1. Den nye salgsordre åbnes i visningen **Linjer**. Notér dig salgsordrenummeret.
1. Skift til **overskriftsvisningen**.
1. Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:

    - **Fragtmand:** *Air Cargo*
    - **Fragttjeneste:** *Air*

1. Skift tilbage til visningen **Linjer**.
1. Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Varenummer:** *A0002*
    - **Antal:** *2*

1. Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre. Noter dig bølge-id-nummeret og forsendelses-id-numrene.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Få vist den bølge, der er oprettet fra salgsordre 1

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg det bølge-id, der blev oprettet fra salgsordren.
1. Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.
1. Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer**.

#### <a name="create-sales-order-2"></a>Opret salgsordre 2

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-005*.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.

1. Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.
1. Den nye salgsordre åbnes i visningen **Linjer**. Notér dig salgsordrenummeret.
1. Skift til **overskriftsvisningen**.
1. Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:

    - **Fragtmand:** *Flower moving*
    - **Fragttjeneste:** *Std*

1. Skift tilbage til visningen **Linjer**.
1. Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Varenummer:** *A0001*
    - **Antal:** *1*

1. Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre. Noter dig bølge-id-nummeret og forsendelses-id-numrene. Bemærk, at bølge-id'et ikke er det samme som bølge-id'et for den første salgsordre.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Få vist den bølge, der er oprettet fra salgsordre 2

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg det bølge-id, der blev oprettet fra den anden salgsordre.
1. Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.
1. Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer**.

Der blev oprettet en ny bølge til denne forsendelse, fordi den bruger en anden fragttjeneste end den første salgsordre.

#### <a name="create-sales-order-3"></a>Opret salgsordre 3

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-006*.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.

1. Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.
1. Den nye salgsordre åbnes i visningen **Linjer**. Notér dig salgsordrenummeret.
1. Skift til **overskriftsvisningen**.
1. Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:

    - **Fragtmand:** *Air Cargo*
    - **Fragttjeneste:** *Air*

1. Skift tilbage til visningen **Linjer**.
1. Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.
1. Angiv følgende værdier på den nye linje:

    - **Varenummer:** *A0001*
    - **Antal:** *1*

1. Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre. Noter dig bølge-id-nummeret og forsendelses-id-numrene. Forsendelsen er tildelt den eksisterende bølge fra den første salgsordre.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Få vist bølgen for salgsordre 1 og 3

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg det bølge-id, der blev oprettet fra den tredje salgsordre.
1. Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.
1. Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer** sammen med forsendelsen for den første salgsordre.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]