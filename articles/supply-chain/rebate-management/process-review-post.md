---
title: Behandle, gennemgå og bogføre rabatter
description: I dette emne beskrives, hvordan du behandler dine rabatstyringsaftaler, beregner deres rabatter, gennemgår de posteringer, der er oprettet, bogfører posteringer og gennemgår posteringerne.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: db3c7561a7249930def2e519f3b6718c429fa3ba
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500469"
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

## <a name="create-source-transactions"></a>Oprette kildetransaktioner

Du kan oprette de salgsordrer eller indkøbsordrer, der har kildetransaktioner, enten før eller efter du har oprettet en relevant rabatstyringsaftale.

Du kan konfigurere de enkelte aftalelinjer, så der automatisk oprettes en rabathensættelse ved at bogføre leveringen eller fakturaen for en salgsordre eller indkøbsordre. Angiv feltet **Transaktionstype** for aftalelinjen til *Levering* eller *Faktura*, og angiv indstillingen **Behandling ved bogføring** til *Ja*. Hvis feltet **Transaktionstype** er angivet til *Ordre*, deaktiveres behandling ved bogføring. I forbindelse med kildeposteringer, der er oprettet, efter at en aftale er blevet aktiveret, kan du stadig behandle hensættelsen som beskrevet i afsnittet [Behandle rabatstyringsaftaler](#process-deals) senere i dette emne.

### <a name="enable-price-details"></a>Aktivér prisdetaljer

Før du kan oprette kildeposteringer, skal du aktivere indstillingen **Aktivér prisdetaljer** for debitorer.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Under fanen **Priser** i oversigtspanelet **Prisdetaljer** skal du vælge *Ja* i indstillingen **Aktivér prisdetaljer**.

### <a name="create-a-source-transaction"></a>Oprette en kildetransaktion

Du kan oprette en kildetransaktion på følgende måde.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny**.

    For at efterligne den måde, som rabatkrav vil blive genereret på, skal du nu oprette en salgsordre, hvor produktet og antallet kvalificerer pågældende kunde til en rabat.

1. Angiv eller vælg en kunde, der skal kvalificeres til en rabataftale, i feltet **Debitorkonto**.
1. Vælg **OK** for at oprette salgsordren.
1. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje og angive følgende indstillinger for den:

    - **Varenummer** – Angiv en vare, der er kvalificeret til en rabat.
    - **Antal** – Angiv et antal, der er kvalificeret til en rabataftale, der omfatter en linje, hvor feltet **Basis** er angivet til *Antal*.
    - **Enhedspris** – Angiv en pris, der er kvalificeret til en rabataftale, der omfatter en linje, hvor feltet **Basis** er angivet til *Værdi*.
    - **Lokation** – Vælg en lokation, hvor produktet er tilgængeligt, og som er kvalificeret til en rabathandel.
    - **Lagersted** – Vælg et lagersted, hvor produktet er tilgængeligt, og som er kvalificeret til en rabathandel.

1. I oversigtspanelet **Salgsordrelinjer** skal du på værktøjslinjen vælge **Salgsordrelinjer \> Prisdetaljer**. Denne kommando er kun tilgængelig, hvis du har aktiveret prisdetaljer som beskrevet i forrige afsnit.
1. På siden **Prisdetaljer** skal du vælge oversigtspanelet **Rabatstyring**. Dette overgigtspanel viser alle rabatstyringsaftaler, der gælder for den aktuelle ordrelinje, og viser det anslåede rabatbeløb i ordrens valuta. Bemærk, at beløbene kun er estimater af de fremtidige rabatkrav. De faktiske rabatbeløb kan være anderledes. Her er nogle af de faktorer, der kan påvirke de faktiske beløb:

    - Det samlede salgsvolumen, som kunden opnåede i henhold til en periodisk rabataftale.
    - Om kunden har returneret alle antal eller delmængder.
    - Om den relevante salgsordre har opnået den transaktionstype (*Ordre, Levering* eller *Faktura*), der er defineret for rabatstyringsaftalen.
    - Aftalens **Output**-værdi. Der vises et tomt rabatbeløb for aftaler, hvor feltet **Output** er angivet til *Vare*.

1. Bemærk, at sektionen **Forkalkulering af avance** indeholder følgende felter i oversigtspanelet **Detaljer**. Disse felter tilføjes af Rabatstyring. Alle disse viser værdier pr. enhed (mens felterne i oversigtspanelet **Rabatstyring** viser de samlede værdier for linjen).

    - **Rabatbeløb for rabatstyring** (kun salgsordrer)
    - **Royaltybeløb for rabatstyring** (kun salgsordrer)
    - **Kreditorrabatbeløb for rabatstyring** (salgsordrer og indkøbsordrer)

1. Luk siden **Prisdetaljer**.
1. Hvis salgsordren ikke er kvalificeret til de rabatter, du lige har set, skal du følge disse trin for at udelukke rabatter. (Du udelukker dog normalt ikke rabatter).

    1. I oversigtspanelet **Salgsordrelinjer** skal du vælge den ønskede linje.
    1. Angiv indstillingen **Udeluk fra rabatstyring** til **Ja** under fanen **Pris og rabat** i oversigtspanelet *Linjedetaljer*. Denne indstilling gælder ikke for indkøbsordrer. Desuden er det kun debitorrabatter, der udelukkes, når denne indstilling er angivet til *Ja*. Kunderoyaltyrabatter og leverandørrabatter gælder stadig.

1. Vælg **Bogfør følgeseddel** i gruppen **Opret** under fanen **Pluk og pak** i handlingsruden.
1. Vælg **Alle** i feltet **Antal** i oversigtspanelet *Parametre*.
1. Vælg **OK**.
1. Vælg **OK**, hvis du bliver bedt om at bekræfte handlingen.
1. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
1. Vælg **Alle** eller **Følgeseddel** i feltet *Antal* i oversigtspanelet *Parametre*.
1. Vælg **OK**.
1. Vælg **OK**, hvis du bliver bedt om at bekræfte handlingen.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Behandle rabatstyringsaftaler

Når du behandler en aftale, beregner systemet alle relevante rabatter og royalties, der er konfigureret. Kun valgte aftaler, der har beregningsperioder, som er klar til at blive beregnet, og som har statussen *Aktiv*, behandles. Når behandlingen er fuldført, genererer systemet et sæt transaktioner, du kan gennemgå og derefter bogføre.

> [!NOTE]
> I alle tilfælde behandles rabatterne på det niveau, der er angivet af de enkelte aftalers **Afstem efter**-indstilling (*Aftale* eller *Linje*). Du kan kun foretage beregninger for enkeltlinjer i aftaler, hvor feltet **Afstem efter** er angivet til *Linje*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Behandle alle linjer for en eller flere aftaler

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg rækken for hver aftale, du vil behandle (eller åbn den aftale, du vil behandle).
1. Vælg en af følgende kommandoer i gruppen **Generer** under fanen **Rabatstyringsaftaler** i handlingsruden:

    - **Proces \> Hensættelse** – Hensættelse af et sæt periodiseringer for hver relevant rabataftale, men bogfør ikke. Dette menupunkt er ikke tilgængeligt for aftaler, hvor feltet **Rabatoutput** er angivet til *Vare*.
    - **Proces \> Rabatstyring** – Behandle en række posteringer, der angiver værdien af rabatten for hver enkelt aftale.
    - **Proces \> Afskrivning** – For hver kildepostering for rabataftalen og den angivne periode skal du behandle afvigelsen mellem de beløb, der blev bogført for en hensættelse og for rabatstyring. Dette menupunkt er ikke tilgængeligt for aftaler, hvor feltet **Rabatoutput** er angivet til *Vare*.

1. Angiv felterne **Fra dato** og **Til dato** i den dialogboks, der vises, for at definere datointervallet for beregningen.
1. Vælg **OK** for at køre beregningen.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Behandle en eller flere specifikke aftalelinjer for en valgt aftale

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Åbn den aftale, du vil behandle en linje fra.
1. Vælg fanen **Linjer** øverst til højre.
1. Vælg rækken for hver aftalelinje, du vil behandle, i oversigtspanelet **Rabatstyring**.
1. Vælg en af følgende kommandoer på værktøjslinjen i oversigtspanelet **Rabatstyring**. (Disse kommandoer er kun tilgængelige for aftaler, hvor **Afstem efter**-feltet er angivet til *Linje*).

    - **Proces \> Hensættelse** – Hensættelse af et sæt periodiseringer for hver relevant aftalelinje, men bogfør ikke. Dette menupunkt er ikke tilgængeligt for aftaler, hvor feltet **Rabatoutput** er angivet til *Vare*.
    - **Proces \> Rabatstyring** – Behandle en række posteringer, der angiver værdien af rabatten for hver enkelt aftalelinje.
    - **Proces \> Afskrivning** – For hver kildepostering for rabataftalen og den angivne periode skal du behandle afvigelsen mellem de beløb, der blev bogført for en hensættelse og for rabatstyring. Dette menupunkt er ikke tilgængeligt for aftaler, hvor feltet **Rabatoutput** er angivet til *Vare*. 

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

### <a name="process-deals-by-using-the-rebate-workbench"></a>Behandle aftaler ved at bruge rabatpanelet

I stedet for at behandle bestemte aftaler eller aftalelinjer kan du bruge *rabatpanelet* til at behandle flere aftaler på én gang. Du kan vælge at anvende postfiltre og/eller konfigurere en gentagelsesplan. Du behøver ikke markere rækker. Systemet behandler alle linjer, der opfylder de dato- og filterkrav, du konfigurerer.

Hvis du vil behandle aftaler ved hjælp af rabatpanelet, skal du benytte følgende fremgangsmåde.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
1. Vælg en af følgende kommandoer i gruppen **Behandling** under fanen **Rabatpanel** i handlingsruden:

    - **Proces \> Hensæt** – Hensæt et sæt periodiseringer for hver relevant aftalelinje, men bogfør ikke periodiseringer.
    - **Proces \> Rabatstyring** – Behandle en række posteringer, der angiver værdien af rabatten for hver enkelt aftalelinje.
    - **Proces \> Afskrivning** – Foretag behandling af afvigelsen mellem hensættelse og rabatstyring, der blev bogført for hver kildetransaktion pr. rabataftale og angivne periode.

1. I dialogboksen **Rabatstyring** skal du i sektionen **Periode** indstille felterne **Fra dato** og **Til dato** for at definere datointervallet for beregningen.
1. Angiv felterne **Fra dato** og **Til dato** i sektionen **Garantiperiode** for at definere datointervallet for garantier i beregningen.
1. I oversigtspanelet **Poster, der skal medtages**, kan du konfigurere filtre for at begrænse det sæt aftaler, som batchjobbet skal behandle. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. I oversigtspanelet **Kør i baggrunden** kan du konfigurere batchbehandling og planlægningsindstillinger efter behov. Disse indstillinger fungerer på samme måde, som de fungerer for andre typer batchjob.
1. Vælg **OK** for at køre og/eller planlægge beregningen.

## <a name="view-and-edit-rebate-management-transactions"></a>Se og redigere posteringer for rabatstyring

Når du behandler en eller flere aftaler, opretter systemet posteringer, som du kan se og måske redigere, inden du bogfører dem.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Se og redigere transaktioner for rabatstyring ved hjælp af listesiden Rabataftaler

Følg disse trin for at se og redigere transaktioner for rabatstyring ved hjælp af listesiden Rabataftaler.

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

    - Vælg **Bogfør** i handlingsruden for at bogføre kravet for alle relevante linjer. Hvis du bruger en kravproces (når indstillingen **Brug kravproces** er aktiveret på siden **Parametre for rabatstyring**), er det kun de linjer, der er markeret som **Indkasseret**, som bogføres. Ellers bogføres alle kildeposteringer for den valgte rabatpostering. Knappen **Bogfør** er kun tilgængelig for rabatposteringer. Den er ikke tilgængelig for hensættelses- og afskrivningsposteringer. I dialogboksen **Bogfør** angives felterne **Fra dato** og **Til dato** automatisk. Angiv feltet **Bogføringsdato**, og vælg derefter **OK**.
    - Hvis du vil regulere det beløb, der vises for en hvilken som helst åben eller ikke-bogført transaktion, skal du vælge transaktionen og derefter benytte følgende fremgangsmåde:

        - Rediger værdien i feltet **Rettet beløb**.
        - I handlingsruden skal du vælge **Angiv rettelse**. Angiv derefter en værdi i feltet **Rettet beløb** på rullelisten i dialogboksen, der vises.

> [!NOTE]
> Hvis du bruger en kravproses, når du behandler den næste periode, indeholder posteringslisten eventuelle ikke-indkasserede posteringer fra den forrige bogføring samt eventuelle nye posteringer for den valgte periode.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Se og redigere transaktioner for rabatstyring ved hjælp af rabatpanelet

Følg disse trin for at se og redigere transaktioner for rabatstyring ved hjælp af rabatpanelet.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
1. Angiv feltet **Vis** til *Ikke bogført*.
1. På siden **Rabatpanel** vises en liste over transaktionerne. Hver transaktion indeholder relevante detaljer. Disse oplysninger varierer, afhængigt af transaktionstypen. Du kan udføre følgende opgaver på denne side:

    - Hvis du vil have vist flere oplysninger om en postering, skal du markere den og derefter vælge fanen **Generelt**, **Økonomisk dimension** eller **Dimension**.
    - Hvis du bruger en kravproces, kan du markere transaktioner som enten indkasserede eller ikke indkasserede. Vælg de relevante rækker, og vælg derefter en af følgende kommandoer under fanen **Rabatpanel** i handlingsruden. (Du aktiverer kravprocesser på siden [**Parametre til rabatstyring**](rebate-management-parameters.md)).

        - **Angiv indkasserede** – Markér de valgte transaktioner som indkasserede.
        - **Angiv ikke indkasserede** – Markér de valgte transaktioner som ikke indkasserede.

    - Hvis du vil bogføre kravet for en eller flere linjer, skal du vælge de relevante linjer. I handlingsruden skal du under fanen **Rabatpanel** vælge **Bogfør**. Knappen **Bogfør** er tilgængelig for hensættelses-, rabat- og afskrivningsposteringer. I dialogboksen **Bogfør** angives felterne **Fra dato** og **Til dato** automatisk. Angiv feltet **Bogføringsdato**, og vælg derefter **OK**.
    - Hvis du vil regulere det beløb, der vises for en hvilken som helst åben eller ikke-bogført transaktion, skal du vælge transaktionen og derefter benytte følgende fremgangsmåde:

        - Rediger værdien i feltet **Rettet beløb**.
        - I handlingsruden skal du under fanen **Rabatpanel** vælge **Angiv rettelse**. Angiv derefter en værdi i feltet **Rettet beløb** på rullelisten i dialogboksen, der vises.

> [!NOTE]
> Hvis du bruger en kravproses, når du behandler den næste periode, indeholder posteringslisten eventuelle ikke-indkasserede posteringer fra den forrige bogføring samt eventuelle nye posteringer for den valgte periode.

## <a name="post-rebates-transactions"></a>Bogføre rabattransaktioner

Hvis du vil bogføre værdien af en behandlet hensættelse, et rabatstyringsbeløb og en afskrivning, skal du køre bogføringsprocessen. Bogføringsprocessen markerer hensættelses-, rabatstyrings- eller afskrivningsposteringer som bogført og opretter målposteringen. Hvis du ikke behøver at gennemse målposteringen, kan disse posteringer konfigureres, så de bogføres automatisk.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Konfigurere systemet til at bogføre alle måltransaktioner automatisk

Du kan konfigurere systemet til at bogføre alle målposteringer, så snart de er genereret af en hensættelse, et rabatstyringsbeløb og en afskrivning, ved at aktivere indstillingen **Bogfør automatisk kladder** og/eller **Bogfør automatisk fritekstfakturaer** på siden **Parametre for rabatstyring**. Yderligere oplysninger finder du i [Parametre til rabatstyring](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Bogføre transaktioner for alle linjer til en eller flere aftaler

Når du har behandlet de relevante aftaler, skal du følge disse trin for at gennemse og bogføre de genererede posteringer for alle linjer for en eller flere aftaler.

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg rækken for hver aftale, du vil bogføre (eller åbn den aftale, du vil bogføre).
1. Vælg en af følgende kommandoer i gruppen **Generer** under fanen **Rabatstyringsaftaler** i handlingsruden:

    - **Bogfør \> Hensættelse** – Bogfør tilgængelige periodiseringsposteringer, du har oprettet.
    - **Bogfør \> Rabatstyring** – Bogfør tilgængelige rabatposteringer, du har oprettet.
    - **Bogfør \> Afskrivning** – Bogfør tilgængelige afskrivningsposteringer, du har oprettet.

1. Angiv feltet **Bogføringsdato** i den viste dialogboks. Angiv derefter felterne **Fra dato** og **Til dato** for at definere datointervallet for transaktioner, der skal bogføres.
1. Vælg **OK** for at bogføre transaktionerne.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Bogføre transaktioner for en eller flere specifikke aftalelinjer i en valgt aftale

Når du har behandlet de relevante aftaler, skal du følge disse trin for at gennemse og bogføre de genererede posteringer for en eller flere specifikke aftalelinjer for en valgt aftale. Denne procedure gælder kun for aftaler, hvor feltet **Afstem efter** er angivet til *Linje*.

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

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Bogføre transaktioner ved at bruge rabatpanelet

Når du har behandlet hensættelses-, rabat- eller afskrivningsposteringer, skal du følge disse trin for at bruge rabatpanelet til at gennemse og bogføre de genererede posteringer for en eller flere specifikke posteringslinjer for alle aftaler.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
1. Vælg rækken for hver transaktionslinje, der skal bogføres, i gitteret. Du kan vælge ikke-bogførte hensættelses-, rabat- og/eller afskrivningsposteringer. Der gælder følgende regler:

    - Systemet bogfører også alle linjer, der har samme værdi for **Rabattransaktionsnummer** som de linjer, du vælger.
    - Systemet bogfører ikke linjer af transaktionstypen *Rabat*, der ikke er markeret som indkasseret.
    - Hvis du vælger linjer, der allerede er bogført, springes de bogførte linjer over.
    - Knappen **Bogfør** er kun tilgængelig, hvis du vælger mindst én ikke-bogført linje.

1. I handlingsruden skal du vælge **Bogfør** i gruppen **Behandling** under fanen **Rabatpanel**.
1. Angiv feltet **Bogføringsdato** i dialogboksen **Bogfør**. Felterne **Fra dato** og **Til dato** angives automatisk på basis af den tidligste værdi for **Fra dato** og den seneste **Til dato** for de markerede rækker.
1. Vælg **OK** for at bogføre transaktionerne.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Gennemse rabatstyringskladder

Når posteringerne er bogført, kan du gennemse de kladder, dokumenter eller elementer, der er resultatet. Målposterne for rabatter og royalties er baseret på den betalingstype, der er angivet i posteringsprofilen og rabattens outputtype. Hvis rabatoutputtet f.eks. er angivet til *Vare*, oprettes der en salgsordre for en debitorrabat, og der oprettes en indkøbsordre for en kreditorrabat. Disse ordrer kan ses via målposteringerne. Hvis betalingen er konfigureret til at bruge Kreditor, oprettes der også en kreditorfaktura for den kreditor, der er konfigureret for debitoren, for debitorrabatter.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Gennemse kladder ved hjælp af listesiden Rabataftaler

Hvis du vil gennemse de kladdeposteringer, der er knyttet til en rabatstyringsaftale, skal du følge disse trin.

1. Åbn [listesiden med relevante rabataftaler](rebate-management-deals.md) for den type rabat, du vil arbejde med.
1. Vælg den aftale, der skal kontrolleres kladdeposteringer for.
1. I handlingsruden under fanen **Rabatstyringsaftaler** skal du i gruppen **Transaktioner** vælge enten **Transaktioner** eller **Garantitransaktioner**, afhængigt af den type transaktioner du vil se.
1. Angiv feltet **Vis** til *Alle* eller *Bogført*.
1. Find og vælg den posteringssamling, du vil kontrollere, og vælg derefter en af følgende knapper i handlingsruden. (Disse knapper er kun tilgængelige, når der findes relevante posteringer for den valgte posteringssamling).

    - **Målposteringer** – Gennemse relevante kladder og andre typer dokumenter, der er genereret af den valgte aftale.
    - **Varer** – Gennemse de relevante salgsordrer eller indkøbsordrer, der er genereret af den valgte aftale.

1. Der vises en liste over relevante kladder, dokumenter eller varer. Hvis du vil have vist flere oplysninger om en kladde, et dokument eller en vare, skal du vælge rækken og derefter vælge **Vis detaljer** i handlingsruden.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Gennemgå kladder ved at bruge rabatpanelet

Hvis du vil gennemgå kladder ved hjælp af rabatpanelet, skal du benytte følgende fremgangsmåde.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
1. Angiv feltet **Vis** til _Alle_ eller _Bogført_.
1. Find og vælg den linje, du vil inspicere. Vælg derefter **Målposteringer** i gruppen **Vis** under fanen **Rabatpanel** i handlingsruden. Denne knap er kun tilgængelig, hvis der findes relevante posteringer for den valgte linje.
1. Der vises en liste over relevante kladder, dokumenter eller varer. Hvis du vil have vist flere oplysninger om en kladde, et dokument eller en vare, skal du vælge rækken og derefter vælge **Vis detaljer** i handlingsruden.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Posteringer for rabatstyring i fradragspanelet

Når du bogfører en postering i Rabatstyring, der har en af følgende værdier af **Betalingstype**, opretter systemet en debitorfradragskladde eller en fritekstfaktura for den relevante debitorkonto:

- Debitorfradrag
- Debitorfradrag på momsfaktura
- Samhandelsforbrug
- Rapportering

Når en målpostering er oprettet og bogført, er den tilgængelig som en åben postering på siden **Fradragspanel** (**Salg og marketing \> Handelsrabatter \> Fradrag \> Fradragspanel**). Åbne posteringer har værdien **Kravtype** for *Rabatstyring*, og der er en værdi for **Rabattransaktionsnummer** tilgængelig, så du kan spore det. Datoen angives til bogføringsdatoen for målposteringen i Rabatstyring. Hvis du vil bruge fradragspanelet til at udligne åbne posteringer med eksisterende fradrag for samme debitorkonto, skal du vælge **Vedligehold \> Afstem** i handlingsruden.

Du kan finde flere oplysninger under [Administrere fradrag ved hjælp af fradragspanelet](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Fjerne ikke-bogførte transaktioner

Når du har behandlet hensættelses-, rabat- eller afskrivningsposteringer, skal du benytte følgende fremgangsmåde for at fjerne valgte ikke-bogførte posteringer.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
2. Angiv feltet **Vis** til *Ikke bogført*.
3. Find og vælg de transaktioner, der skal slettes. I handlingsruden skal du vælge **Fjern** i gruppen **Behandling** under fanen **Rabatpanel**.
4. Vælg **OK** for at slette de ikke-bogførte transaktioner.

## <a name="cancel-a-posted-provision"></a>Annullere en bogført hensættelse

Når du har behandlet og bogført en hensættelse, skal du følge disse trin for at annullere de bogførte hensættelsestransaktioner.

1. Gå til **Rabatstyring \> Rabatstyringsaftaler \> Rabatpanel**.
2. Angiv feltet **Vis** til *Bogført*.
3. Find og vælg de hensættelsestransaktioner, der skal annulleres. I handlingsruden skal du vælge **Annuller hensættelse** i gruppen **Behandling** under fanen **Rabatpanel**.
4. Vælg **OK** for at tilbageføre transaktionerne.

Disse tilbageførsler af hensættelser vil også være synlige i de relevante [Rabatstyringskladder](#review-journals).
