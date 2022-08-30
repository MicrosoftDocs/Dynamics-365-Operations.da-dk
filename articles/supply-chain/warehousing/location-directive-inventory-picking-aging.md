---
title: Lokalitetsvejledning til aldersfordelt lagerpluk
description: Denne artikel forklarer, hvordan du kan bruge lokalitetsvejledningsstrategierne FIFO (first in, First Out) og LIFO (last in, first out) under plukning.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4ed1308ea36b731b156b518182846b60a59528d5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335609"
---
# <a name="location-directive-inventory-picking-aging"></a>Lokalitetsvejledning til aldersfordelt lagerpluk

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan bruge lokalitetsvejledningsstrategierne FIFO (first in, First Out) og LIFO (last in, first out) under plukning. Disse strategier fungerer sammen med de aldersfordelingsdatoer, der registreres på lokationer, så lagervarer kan spores, når de først er kommet ind på lagerstedet. Funktionen *Aldersfordeling i lokalitetsvejledning til lagerpluk* bruger datoen på lokationen til at bestemme aldersfordeling. Funktionen *Lokationsstatus for lagersted* opdaterer datoen på lokationen ud fra datoen på nummerpladen.

Du kan bruge strategierne FIFO og LIFO til at sende både batchsporede varer og varer, der ikke er batchsporede, baseret på den dato, hvor lagerbeholdningen blev angivet. Denne facilitet kan især være nyttig for ikke-batchsporet lager, hvor en udløbsdato ikke er tilgængelig til brug ved sortering.

Når lageret først modtages eller oprettes på lagerstedet, opdaterer systemet den relevante nummerplade, så den aktuelle dato vises som aldersfordelingsdato. Denne dato bruges derefter af lokalitetsvejledningsstrategier til at identificere den ældste eller nyeste lagerbeholdning på lagerstedet. Hvis lageret flyttes til en lokation, der ikke spores på basis af en nummerplade, opdateres selve lokationen med aldersfordelingsoplysninger, og disse oplysninger bruges derefter af strategierne.

## <a name="turn-on-the-feature"></a>Slå funktionen til

Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) i denne rækkefølge:

1. *Placeringsstatus for lagersted* (fra og med version 10.0.29 er denne funktion obligatorisk og kan ikke deaktiveres. Du kan finde flere oplysninger under [Placeringsstatus for lagersted](warehouse-location-status.md).)
1. *Aldersfordeling i lokalitetsvejledning til lagerpluk*

## <a name="feature-requirements"></a>Funktionskrav

Hvis du vil bruge denne funktion, skal du angive indstillingen **Aktiver lokationsstatus** til *Ja* for alle de [lokationsprofiler ](tasks/create-location-profile.md), der bruges til at gemme lagerbeholdningen. Hvis du vil angive denne indstilling for en lokationsprofil, skal du gå til **Lokationsstyring \> Opsætning \> Lagersted \> Lokationsprofiler** og vælge lokationsprofilen. Du kan finde indstillingen i oversigtspanelet **Generelt**.

## <a name="feature-scenarios"></a>Funktionsscenarier

Dette afsnit indeholder eksempler, der viser, hvordan du kan konfigurere og bruge FIFO- og LIFO-strategier.

> [!TIP]
> Dette afsnit har to scenarier, én til FIFO og én til LIFO. De fremgangsmåder, der gives, forudsætter, at du udfører begge scenarier i rækkefølge. Det anbefales, at du udfører begge scenarier, så du kan opleve forskellene mellem de to strategier.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem disse scenarier ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge disse scenarier som vejledning i at bruge funktionen i et produktionssystem. I dette tilfælde skal du dog erstatte dine egne værdier for hver af de indstillinger, der beskrives her.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Konfigurere scenarierne

Demodataene kræver opsætning og lagerreguleringer for at understøtte scenarierne. Udfør følgende trin for at oprette de lagerdata, der kræves for at arbejde dig gennem FIFO-og LIFO-scenarierne.

1. Log på et system, hvor demodata er installeret, og vælg den juridiske enhed **USMF**.
1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **Rediger** i handlingsruden.
1. Vælg **PRODUKTION-05** på listen over lokationsprofiler.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Aktiver lokationsstatus** til *Ja*.
1. Vælg **Gem**.
1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. På listen over lokationsvejledninger skal du vælge **63 Pluk containerisering**.
1. Vælg **Rediger** for at sætte siden i redigeringstilstand.
1. Gå til oversigtspanelet **Handlinger i lokationsvejledning**, find den linje, hvor feltet **Løbenummer** er indstillet til *1*, og følg et af disse trin:

    - Hvis du konfigurerer et FIFO-scenarie, skal du ændre værdien i feltet **Strategi** til *Lokation med aldersfordelt FIFO*.
    - Hvis du konfigurerer et LIFO-scenarie, skal du ændre værdien i feltet **Strategi** til *Lokation med aldersfordelt LIFO*.

1. Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Vælg forespørgselsdialogboksen skal du under fanen **Interval** vælge **Tilføj** for at føje en linje og derefter indstille følgende værdier:

    - **Tabel:** *Lokationer*
    - **Afledt tabel:** *Lokationer*
    - **Felt:** *Zone-id*
    - **Kriterier:** *Produktion*

1. Vælg **OK** for at anvende dine indstillinger og lukke forespørgselsdialogboksen.
1. Vælg **Gem** for at gemme ændringer til lokationsvejledningen.
1. Udfør følgende trin på en mobilenhed eller i *Dynamics 365 Supply Chain Management-lagerstedsappen* på din pc for at fjerne eksisterende lagerbeholdning fra lagerstedet for at understøtte scenarierne:

    1. Log på lagersted *63* ved at bruge det relevante bruger-id og den relevante adgangskode.
    1. Vælg **Kvalitet** i hovedmenuen.
    1. Vælg **Kasseres** i menuen **Kvalitetsstyring**.
    1. Gå til siden **Kasseres**, vælg feltet **LOK/NP**, og angiv derefter *63\_1*.
    1. Vælg **Angiv** eller **OK**.
    1. Bekræft oplysningerne for **Kasseres** for **Regulering ud** ved at vælge **Angiv** eller **OK**.

    Når nummerpladelageret er reguleret, får du vist meddelelsen om at "arbejde er fuldført".

    Disse trin afslutter lageret på to lokationer i demodataene. Hver lokation har en forskellig aldersfordelt dato. Lokation *PR-001* har en aldersfordelt dato den 15. april 2017, og lokation *PR-002* har en aldersfordelt dato den 29. januar 2017. Begge lokationer indeholder varen *A0001*.

    Hvis du vil have vist disse oplysninger, skal du gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste** og derefter filtrere efter lagersted *63* og vare *A0001*. I de rækker, hvor feltet **Lokation** er angivet til *PR-001* eller *PR-002*, skal du vælge en linje med en positiv værdi for **Fysisk lager** og derefter vælge **Transaktioner** i handlingsruden. Feltet **Fysisk dato** viser en dato, der svarer til en af de tidligere nævnte aldersfordelte datoer.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Scenario 1: Konfigurere og bruge aldersfordelt FIFO-lokation

FIFO-strategien finder den lokation, der indeholder den ældste aldersfordelte dato, og fordeler plukningen baseret på den pågældende aldersfordelte dato.

1. Hvis du ikke allerede har gjort det, skal du [forberede de eksempeldata](#demo-set-up), der kræves til dette scenarie.
1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-001*.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *63*.

1. Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Det omfatter at medtage en ny tom række i gitteret i oversigtspanelet **Salgsordrelinjer**. På den nye linje skal du angive feltet **Varenummer** til *A0001* og feltet **Antal** til *1*.
1. Vælg **reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du i vælge **Reserver parti** for at reservere det bestilte antal fra lager på det valgte lagersted.
1. Luk siden **Reservation**.
1. Gå til siden **Salgsordre**, og vælg **Frigiv til lager** i gruppen **Handlinger** på fanen **Lager** i handlingsruden. Du får orienterende meddelelser. Systemet opretter en forsendelse, føjer den til en ny last og opretter det nødvendige arbejde.
1. I oversigtspanelet **Salgsordrelinjer** i menuen **Lager** skal du vælge **Arbejdsdetaljer** for at åbne det arbejde, der er oprettet for denne salgsordre. Bemærk, at den linje, hvor værdien for **Arbejdstype** er *Pluk*, viser en værdi for **Lokation** *PR-002*. Denne lokation indeholder den nummerplade, der har den ældste aldersfordelte dato (FIFO).
1. Vælg **Lagersted \> Forsendelsesoplysninger**.
1. I oversigtspanelet **Generelt** skal du notere dig bølge-id'et, så du kan bruge det i scenarie 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Scenarie 2: Konfigurere og bruge aldersfordelt LIFO-lokation

LIFO-strategien finder den lokation, der indeholder den nyeste aldersfordelte dato, og fordeler plukningen baseret på den pågældende aldersfordelte dato. I scenarie 2 skal du redigere opsætningen af scenari1 1 (FIFO) og genbruge den salgsordre og bølge, der blev oprettet i løbet af dette scenarie.

1. Før du starter dette scenario, skal du konfigurere og fuldføre hele FIFO-scenariet som beskrevet i det [forrige afsnit](#fifo-demo). I dette scenarie kan du genbruge bølgen og det meste af den opsætning, der blev oprettet i det pågældende scenarie.
1. Rediger lokalitetsvejledningen **63 Pluk containerisering**, så den bruger den strategi for *Aldersfordelt LIFO på lokation*, der er beskrevet i den første del af [proceduren for konfiguration af scenarier](#demo-set-up).

    Derefter skal du ændre den bølge, der er oprettet for salgsordren, i scenarie 1, så den bruger strategien *Aldersfordelt LIFO for lokation*.

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg og åbn den bølge, der indeholder den ordre, som du oprettede for FIFO-scenariet.
1. Gå til handlingsruden og vælg **Annuller** på fanen **Arbejde** for at annullere det arbejde, du har oprettet for FIFO-scenariet.
1. I handlingsruden under fanen **Bølge** i gruppen **Bølge** skal du vælge **Udfør behandling**.
1. Når behandlingen er fuldført, skal du i handlingsruden under **Bølge** i gruppen **Relaterede oplysninger** vælge **Arbejde** for at åbne det arbejde, der er oprettet for denne bølge.
1. På fanen **Oversigt** på siden **Arbejde** skal der være to linjer. Vælg den linje, hvor feltet **Arbejdsstatus** er angivet til *Åben*.
1. Bemærk, at den linje, hvor værdien for **Arbejdstype** er *Pluk*, viser en værdi for **Lokation** *PR-001*. Denne lokation indeholder den nummerplade, der har den nyeste aldersfordelte dato (LIFO).

I disse scenarier har du set, hvordan aldersfordelt strategi dirigerer arbejdet til det lagersted, der enten har det ældste lager eller det nyeste lager, afhængigt af den valgte strategi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
