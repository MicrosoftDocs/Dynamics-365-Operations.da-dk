---
title: Behandle, gennemgå og bogføre rabatter
description: I dette emne beskrives, hvordan du behandler dine rabatstyringsaftaler, beregner deres rabatter, gennemgår de posteringer, der er oprettet, bogfører posteringer og gennemgår posteringerne.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: e255c60889fdb49dfd8a1fd01be839b6405b02c6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919863"
---
# <a name="process-review-and-post-rebates"></a>Behandle, gennemgå og bogføre rabatter

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du behandler dine rabatstyringsaftaler, beregner deres rabatter, gennemgår de posteringer, der er oprettet, bogfører posteringer og gennemgår posteringerne.

## <a name="change-the-status-of-a-deal"></a>Ændre status for en aftale

Du kan tildele en status til hver enkelt aftale, så den lettere kan spores. Denne status er kun til orientering.

1. Vælg en aftale (f.eks. på siden [**Alle rabatstyringsaftaler**](rebate-management-deals.md)).
1. Vælg **Skift status** i gruppen **Vedligehold** i handlingsruden under fanen **Rabatstyringsaftaler**.
1. I dialogboksen **Skift status** skal du angive feltet **Rabatstatus** til en ny status.
1. Vælg **OK**.

## <a name="calculate-fifo-purchase-prices"></a>Beregne FIFO-købspriser

Den periodiske opgave **Beregn FIFO-købspris** skal køres for at beregne rabatter for [aftaler](rebate-management-deals.md), hvor feltet **Prisgrundlag** er angivet til *FIFO*. Systemet bruger en FIFO-regel (First In, First Out) til at beregne værdien af den lagerbeholdning, der er solgt. Denne værdi bruges derefter til at beregne kreditorrabatter.

Gå til **Rabatstyring \> Periodiske opgaver \> Beregn FIFO-købspris**. Vælg **OK** for at køre beregningen i den dialogboks, der vises.

## <a name="process-rebate-management-deals"></a>Behandle rabatstyringsaftaler

Når du behandler en aftale, beregner systemet alle relevante rabatter og royalties, der er konfigureret. Kun valgte aftaler, der har beregningsperioder, som er klar til at blive beregnet, og som har statussen *Aktiv*, behandles. Når behandlingen er fuldført, genererer systemet et sæt transaktioner, du kan gennemgå og derefter bogføre.

> [!NOTE]
> I alle tilfælde behandles rabatterne på det niveau, der er angivet af de enkelte aftalers **Afstem efter**-indstilling (*Aftale* eller *Linje*). Du kan kun foretage beregninger for enkeltlinjer i aftaler, hvor feltet **Afstem efter** er angivet til *Linje*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Behandle alle linjer for en eller flere aftaler

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg rækken for hver aftale, du vil behandle (eller åbn den aftale, du vil behandle).
1. Vælg en af følgende kommandoer i gruppen **Generer** under fanen **Rabatstyringsaftaler** i handlingsruden:

    - **Proces \> Hensættelse** – Hensættelse af et sæt periodiseringer for hver relevant rabataftale, men bogfør ikke.
    - **Proces \> Rabatstyring** – Behandle en række posteringer, der angiver værdien af rabatten for hver enkelt aftale.
    - **Proces \> Afskrivning** – Tilbagefør tidligere bogførte posteringer for at afskrive dem, så nye rabataftaletransaktioner kan beregnes.

1. Angiv felterne **Fra dato** og **Til dato** i den dialogboks, der vises, for at definere datointervallet for beregningen.
1. Vælg **OK** for at køre beregningen.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Behandle en eller flere specifikke aftalelinjer for en valgt aftale

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Åbn den aftale, du vil behandle en linje fra.
1. Vælg fanen **Linjer** øverst til højre.
1. Vælg rækken for hver aftalelinje, du vil behandle, i oversigtspanelet **Rabatstyring**.
1. Vælg en af følgende kommandoer på værktøjslinjen i oversigtspanelet **Rabatstyring**. (Disse kommandoer er kun tilgængelige for aftaler, hvor **Afstem efter**-feltet er angivet til *Linje*).

    - **Proces \> Hensættelse** – Hensættelse af et sæt periodiseringer for hver relevant aftalelinje, men bogfør ikke.
    - **Proces \> Rabatstyring** – Behandle en række posteringer, der angiver værdien af rabatten for hver enkelt aftalelinje.
    - **Proces \> Afskrivning** – Tilbagefør tidligere bogførte posteringer for at afskrive dem, så nye rabataftaletransaktioner kan beregnes.

1. Angiv felterne **Fra dato** og **Til dato** i den dialogboks, der vises, for at definere datointervallet for beregningen.
1. Vælg **OK** for at køre beregningen.

### <a name="process-deals-using-a-batch-job"></a>Behandle aftaler ved hjælp af et batchjob

I stedet for at behandle bestemte aftaler eller aftalelinjer kan du køre et batchjob for at behandle flere aftaler på én gang. Du kan vælge at anvende postfiltre og/eller konfigurere en gentagelsesplan. Hvis du vil behandle aftaler ved hjælp af et batchjob, skal du benytte følgende fremgangsmåde.

1. Udfør ét af følgende trin:

    - Gå til **Rabatstyring \> Periodiske opgaver \> Proces \> Hensættelse** for at hensætte et sæt periodiseringer for hver relevante aftale, men uden at bogføre dem.
    - Gå til **Rabatstyring \> Periodiske opgaver \> Proces \> Rabatstyring** for at behandle en række posteringer, der angiver værdien af rabatten for hver aftale.
    - Go to **Rabatstyring \> Periodiske opgaver \> Proces \> Afskrivning** for at tilbageføre tidligere bogførte posteringer for at afskrive dem, så nye rabataftaletransaktioner kan beregnes.

1. I den dialogboks, der vises i oversigtspanelet **Parametre** skal du i sektionen **Periode** indstille felterne **Fra dato** og **Til dato** for at definere datointervallet for posteringerne til beregningen.
1. Angiv felterne **Fra dato** og **Til dato** i sektionen **Garantiperiode** for at definere datointervallet garantier i beregningen.
1. I oversigtspanelet **Poster, der skal medtages**, kan du konfigurere filtre for at begrænse det sæt aftaler, som batchjobbet skal behandle. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. I oversigtspanelet **Kør i baggrunden** kan du konfigurere batchbehandling og planlægningsindstillinger efter behov. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. Vælg **OK** for at køre og/eller planlægge beregningen.

## <a name="view-and-edit-rebate-management-transactions"></a>Se og redigere posteringer for rabatstyring

Når du behandler en eller flere aftaler, opretter systemet posteringer, som du kan se og måske redigere, inden du bogfører dem.

1. Udfør ét af følgende trin:

    - Vælg den aftale, du vil have vist posteringer for (f.eks. på siden [**Alle rabatstyringsaftaler**](rebate-management-deals.md)). I handlingsruden under fanen **Rabatstyringsaftaler** skal du i gruppen **Transaktioner** vælge **Transaktioner** eller **Garantitransaktioner**, afhængigt af den type postering du vil have vist.
    - Åbn en aftale (f.eks. på siden [**Alle rabatstyringsaftaler**](rebate-management-deals.md)) for at se dens detaljer. Vælg den aftalelinje, du vil have vist posteringer for, i oversigtspanelet **Rabatstyring**. Derefter skal du vælge **Transaktioner** eller **Garantitransaktioner** på værktøjslinjen afhængigt af, hvilken type postering du vil have vist. (Disse knapper er kun tilgængelige for aftaler, hvor **Afstem efter**-feltet er angivet til *Linje*).

1. Siden **Datoposteringer for rabatstyring** eller **Garantiposter for rabatstyring** vises. Den indeholder et gitter, hvor hver linje repræsenterer en samling posteringer fra en enkelt rabat eller garantiperiode. Vælg en række i gitteret, og vælg derefter **Kildeposteringer** i handlingsruden for at få vist de posteringer, der tilhører den pågældende række.
1. Den side, der vises, indeholder en liste over de posteringer af den valgte type, der tilhører den valgte række. Hver enkelt postering indeholder relevante oplysninger afhængigt af posteringstypen. I forbindelse med garantitransaktioner kan du kun få vist listen. I forbindelse med andre posteringstyper kan du udføre følgende handlinger på denne side:

    - Hvis du vil kontrollere den samlede værdi af alle indkasserede transaktioner, kan du se feltet **Indkasseret beløb**.
    - Hvis du vil have vist flere oplysninger om en postering, skal du markere den og derefter vælge fanen **Generelt**, **Økonomisk dimension** eller **Dimension**.
    - Hvis du vil have vist fradrag, der gælder, skal du vælge **Fradragstransaktioner** i handlingsruden. Du kan finde flere oplysninger i [Fradragsprincipper for rabat](rebate-reduction-principle.md).
    - Hvis du vil markere transaktioner som enten indkasserede eller ikke indkasserede, hvis du bruger en kravproces, skal du vælge de relevante rækker og derefter vælge en af følgende kommandoer i handlingsruden. (Du aktiverer kravprocesser på siden [**Parametre til rabatstyring**](rebate-management-parameters.md)).

        - **Angiv indkasserede \> Alle** – Markér alle transaktioner som indkasserede.
        - **Angiv indkasserede \> Udvalgte** – Markér de valgte transaktioner som indkasserede.
        - **Angiv ikke indkasserede \> Alle** – Markér alle transaktioner som ikke indkasserede.
        - **Angiv ikke indkasserede \> Udvalgte** – Markér de valgte transaktioner som ikke indkasserede.

    - Hvis du vil bogføre kravet på en eller flere linjer, skal du vælge de relevante linjer og derefter vælge **Bogfør** i handlingsruden. (Knappen **Bogfør** er kun tilgængelig for rabatposteringer. Den er ikke tilgængelig for hensættelses- og afskrivningsposteringer). I dialogboksen **Bogfør** angives felterne **Fra dato** og **Til dato** automatisk. Angiv feltet **Bogføringsdato**, og vælg derefter **OK**.
    - Hvis du vil regulere det beløb, der vises for en hvilken som helst åben eller ikke-bogført transaktion, skal du vælge transaktionen og derefter benytte følgende fremgangsmåde:

        - Rediger værdien i feltet **Rettet beløb**.
        - I handlingsruden skal du vælge **Angiv rettelse**. Angiv derefter en værdi i feltet **Rettet beløb** på rullelisten i dialogboksen, der vises.

> [!NOTE]
> Når du behandler den næste periode, indeholder posteringslisten eventuelle ikke indkasserede posteringer fra den forrige bogføring samt eventuelle nye posteringer for den valgte periode.

## <a name="post-rebates-transactions"></a>Bogføre rabattransaktioner

Hvis du vil bogføre værdien af rabatter og fradrag, skal du køre bogføringsprocessen, medmindre du har konfigureret systemet til at bogføre dem automatisk.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Konfigurere systemet til at bogføre alle transaktioner automatisk

Du kan konfigurere systemet til at bogføre alle posteringer, så snart de er genereret, ved at aktivere indstillingen **Bogfør automatisk kladder** og/eller **Bogfør automatisk fritekstfakturaer** på siden **Parametre for rabatstyring**. Yderligere oplysninger finder du i [Parametre til rabatstyring](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Bogføre transaktioner for alle linjer til en eller flere aftaler

Hvis du ikke bruger automatisk bogføring, når du har behandlet de relevante aftaler, skal du følge disse trin for at gennemse og bogføre de genererede posteringer for alle linjer for en eller flere aftaler.

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg rækken for hver aftale, du vil bogføre (eller åbn den aftale, du vil bogføre).
1. Vælg en af følgende kommandoer i gruppen **Generer** under fanen **Rabatstyringsaftaler** i handlingsruden:

    - **Bogfør \> Hensættelse** – Bogfør tilgængelige periodiseringsposteringer, du har oprettet.
    - **Bogfør \> Rabatstyring** – Bogfør tilgængelige rabatposteringer, du har oprettet.
    - **Bogfør \> Afskrivning** – Bogfør tilgængelige afskrivningsposteringer, du har oprettet.

1. Angiv feltet **Bogføringsdato** i den viste dialogboks. Angiv derefter felterne **Fra dato** og **Til dato** for at definere datointervallet for transaktioner, der skal bogføres.
1. Vælg **OK** for at bogføre transaktionerne.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Bogføre transaktioner for en eller flere specifikke aftalelinjer i en valgt aftale

Hvis du ikke bruger automatisk bogføring, når du har behandlet de relevante aftaler, skal du følge disse trin for at gennemse og bogføre de genererede posteringer for en eller flere specifikke aftalelinjer for en valgt aftale.

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Åbn den aftale, der indeholder en linje, du vil bogføre transaktioner for.
1. Vælg fanen **Linjer** øverst til højre.
1. Vælg rækken for hver aftalelinje, du vil bogføre, i oversigtspanelet **Rabatstyring**.
1. Vælg en af følgende kommandoer på værktøjslinjen i oversigtspanelet **Rabatstyring**. (Disse kommandoer er kun tilgængelige for aftaler, hvor **Afstem efter** er angivet til *Linje*).

    - **Bogfør \> Hensættelse** – Bogfør tilgængelige periodiseringsposteringer, du har oprettet.
    - **Bogfør \> Rabatstyring** – Bogfør tilgængelige rabatposteringer, du har oprettet.
    - **Bogfør \> Afskrivning** – Bogfør tilgængelige afskrivningsposteringer, du har oprettet.

1. Angiv feltet **Bogføringsdato** i den viste dialogboks. Angiv derefter felterne **Fra dato** og **Til dato** for at definere datointervallet for transaktioner, der skal bogføres.
1. Vælg **OK** for at bogføre transaktionerne.

### <a name="post-transactions-using-a-batch-job"></a>Bogføre posteringer ved hjælp af et batchjob

I stedet for at bogføre posteringer for bestemte aftaler eller aftalelinjer kan du køre et batchjob for at bogføre posteringer for flere aftaler på én gang. Du kan vælge at anvende postfiltre og/eller konfigurere en gentagelsesplan. Hvis du vil bogføre posteringer ved hjælp af et batchjob, skal du benytte følgende fremgangsmåde.

1. Udfør ét af følgende trin:

    - Gå til **Rabatstyring \> Periodiske opgaver \> Bogfør \> Hensættelse** for at bogføre de tilgængelige periodiseringsposteringer, du har oprettet.
    - Gå til **Rabatstyring \> Periodiske opgaver \> Bogfør \> Rabatstyring** for at bogføre de tilgængelige rabatposteringer, du har oprettet.
    - Gå til **Rabatstyring \> Periodiske opgaver \> Bogfør \> Afskrivning** for at bogføre de tilgængelige afskrivningsposteringer, du har oprettet.

1. Angiv **Bogføringsdato**-feltet i sektionen **Periode** i oversigtspanelet **Parametre** i den dialogboks, der vises. Angiv derefter felterne **Fra dato** og **Til dato** for at definere datointervallet for transaktioner, der skal bogføres. 
1. Angiv felterne **Fra dato** og **Til dato** i sektionen **Garantiperiode** for at definere datointervallet for de garantier, der skal bogføres.
1. I oversigtspanelet **Poster, der skal medtages**, kan du konfigurere filtre for at begrænse det sæt aftaler, som batchjobbet skal behandle. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. I oversigtspanelet **Kør i baggrunden** kan du konfigurere batchbehandling og planlægningsindstillinger efter behov. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. Vælg **OK** for at køre og/eller planlægge beregningen.

## <a name="review-rebate-management-journals"></a>Gennemse rabatstyringskladder

Når posteringerne er bogført, kan du gennemse de kladder, dokumenter eller elementer, der er resultatet. Målposterne for rabatter og royalties er baseret på den betalingstype, der er angivet i posteringsprofilen og rabattens outputtype. Hvis rabatoutputtet f.eks. er angivet til *Vare*, oprettes der en salgsordre, som kan ses via målposteringerne. Hvis betalingen er konfigureret til at bruge Kreditor, oprettes der også en kreditorfaktura for den kreditor, der er konfigureret for debitoren, for debitorrabatter.

Hvis du vil gennemse de kladdeposteringer, der er knyttet til en rabatstyringsaftale, skal du følge disse trin.

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg den aftale, der skal kontrolleres kladdeposteringer for.
1. I handlingsruden under fanen **Rabatstyringsaftaler** skal du i gruppen **Transaktioner** vælge enten **Transaktioner** eller **Rabattransaktioner**, afhængigt af den type transaktioner du vil se.
1. Kontrollér, at feltet **Vis** er angivet til *Alle* eller *Bogført*.
1. Find og vælg den posteringssamling, du vil kontrollere, og vælg derefter en af følgende knapper i handlingsruden. (Disse knapper er kun tilgængelige, når der findes relevante posteringer for den valgte posteringssamling).

    - **Målposteringer** – Gennemse relevante kladder og andre typer dokumenter, der er genereret af den valgte aftale.
    - **Varer** – Gennemse relevante varer, der er genereret af den valgte aftale.

1. Der vises en liste over relevante kladder, dokumenter eller varer. Hvis du vil have vist flere oplysninger om en kladde, et dokument eller en vare, skal du vælge rækken og derefter vælge **Vis detaljer** i handlingsruden.
