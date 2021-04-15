---
title: Bølgeoprettelse og -behandling
description: Dette emne beskriver, hvordan du opretter, behandler og frigiver en bølge for at oprette plukkearbejde for en last, forsendelse, produktionsordre eller kanban-ordre.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 36e1bd7f88a27b2da0672bf9d9ecb1e217fc44d3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813645"
---
# <a name="wave-creation-and-processing"></a>Bølgeoprettelse og -behandling

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter, behandler og frigiver en bølge for at oprette plukkearbejde for en last, forsendelse, produktionsordre eller kanban-ordre. Du kan oprette bølger til følgende typer ordrer:

- **Salgsordrer** – Brug forsendelsesbølger for at medtage linjer fra salgsordrer. Når en salgsordre er frigivet til lagerstedet, kan salgsordrelinjerne medtages i bølgen.
- **Produktionsordrer** – Brug produktionsbølger for at medtage linjer fra produktets stykliste.
- **Kanban-ordrer** – Kanban-bølger omfatter pluklistelinjer fra kanban-ordrer.

Når det gælder salgsordrer og kanban-ordrer, skal der reserveres lager, før ordren frigives til lagerstedet. Ellers kan varerne eller fordelingslinjerne ikke behandles i en bølge. Produktionsordrer er dog lidt mere fleksible. For produktionsordrer kan du vælge en af følgende indstillinger:

- Kræver, at alle materialer reserveres, før det er muligt at frigive en ordre til lagerstedet.
- Giv mulighed for, at produktionsordrer kan frigives til lagerstedet, selvom ikke alle materialerne kan reserveres. Hvis du vælger denne indstilling, skal du gentage frigivelsen til lagerprocessen manuelt, når de ekstra materialer bliver tilgængelige. Dette er f.eks. nyttigt, hvis du har de materialer, du skal bruge til at starte en produktion og kan vente, indtil de ekstra materialer bliver tilgængelige.

Du kan angive, hvilke af disse produktionsordreindstillinger der som standard skal bruges, ved hjælp af feltet **Krav til materialereservation** på siden **Produktionsstyringsparametre**. Du kan dog når som helst ændre indstillingen for hver produktionsordre. Yderligere oplysninger finder du i [Lagerstedsparametre til behandling af bølger](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Oprette og behandle en bølge

Følgende diagram viser flowet for, hvordan forsendelsesbølger oprettes, behandles og frigives. Tallene svarer til oplysningerne senere i denne sektion.

![Proces for oprettelse af en bølge](media/wave-processing-diagram.png "Proces for oprettelse af en bølge")

### <a name="prerequisites"></a>Forudsætninger

Før du starter, skal der være en bølgeskabelon tilgængelig til den type bølge, du vil oprette (forsendelse, produktion eller kanban). Bølgeskabelonen opretter mange indstillinger for, hvordan bølgen skal genereres og behandles, herunder hvilke trin der skal udføres manuelt, og hvilke der udføres automatisk. Du finder flere oplysninger under [Bølgeskabeloner](wave-templates.md).

### <a name="create-a-wave"></a>Opret en bølge

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Oprette bølger automatisk baseret på lagersted og ordretype

Hvis du vil oprette bølger automatisk, skal du konfigurere [Bølgeskabeloner](wave-templates.md), som gælder for hver relevant ordretype og lagersted. Sørg for, at skabelonen har indstillingen **Automatisk oprettelse af bølge** angivet til *Ja*.

#### <a name="manually-create-waves"></a>Oprette bølger manuelt

Følg disse trin for at oprette en bølge manuelt:

1. Sørg for, at de relevante [Bølgeskabeloner](wave-templates.md) ikke er angivet til automatisk at oprette en bølge til lagerstedet og ordretyperne, hvor du vil gøre det manuelt.
1. Afhængigt af den type bølge du vil oprette, skal du gøre ét af følgende:

    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Vælg **Bølge** i handlingsruden.
    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Produktionsbølger** \> **Alle produktionsbølger**. Vælg **Produktionsbølge** i handlingsruden.
    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Kanban-bølger** \> **Alle kanban-bølger**. Vælg **Opret bølge** i handlingsruden.

1. Angiv en kort beskrivelse af bølgen i feltet **Beskrivelse**. Denne bør angive, hvad du behandler i bølgen.

1. Vælg bølgeskabelon for den type bølge, du vil oprette, i feltet **Navn på bølgeskabelon**. Bølgeskabelon indeholder bølgemetoder, der udfører handlinger som f.eks. oprettelse af arbejde for bølgen. Bølgeskabelonen til forsendelsesbølger kan eksempelvis indeholde metoder til oprettelse af belastninger, tildeling af linjer til bølger, genopfyldning og oprettelse af plukkearbejde for bølgen.

1. Hvis du vil bruge bølgeattributterne som ekstra forespørgselskriterier for bølgen, skal du vælge attributterne i **Bølgeattributter**-felterne.

### <a name="specify-what-to-include-in-a-wave"></a>Angive, hvad der skal medtages i en bølge

Når der er oprettet en bølge, er du klar til at begynde at føje indhold til den.

> [!NOTE]
> Hvis det er nødvendigt, kan du føje linjer til en bølge, også efter at den er behandlet, så længe den ikke er frigivet.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Angive automatisk, hvad der skal medtages i en bølge

Hvis du vil oprette bølger automatisk, skal du konfigurere [Bølgeskabeloner](wave-templates.md), som gælder for hver relevant ordretype og lagersted. Sørg for, at skabelonen har indstillingen **Automatisk oprettelse af bølge** angivet til *Ja*. Alternativt kan skabelonen automatisk tildele linjer til enhver kvalificerende åben bølge, hvis indstillingen **Tildel til åbne bølger** er angivet til *Ja*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Angive manuelt, hvad der skal medtages i en bølge

Når der er oprettet en bølge, men endnu ikke frigivet, kan du manuelt angive, hvad den skal indeholde. Sådan tilføjer du linjer i en bølge manuelt:

1. Afhængigt af den type bølge du vil føje linjer til, skal du gøre ét af følgende:

    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Vælg **Bølge** i handlingsruden.
    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Produktionsbølger** \> **Alle produktionsbølger**. Vælg **Produktionsbølge** i handlingsruden.
    - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Kanban-bølger** \> **Alle kanban-bølger**. Vælg **Opret bølge** i handlingsruden.

1. Vælg bølgen. Vælg en af følgende i handlingsruden:

      - **Vedligehold forsendelser**
      - **Vedligehold produktioner**
      - **Vedligehold pluklister til kanban-job**

1. Vælg den linje, der skal føjes til bølgen, i den øverste del af vinduet, og vælg derefter **Føj til bølge**. Linjen flyttes til oversigtspanelet **Bølgelinjer**.

    Gentag dette trin for hver linje, der skal tilføjes. Hvis du vil tilføje alle linjer, skal du vælge **Tilføj alle**.

    > [!TIP]
    > Til forsendelsesbølger kan du hurtigt finde en bestemt ordre ved at vælge et brugerdefineret filter i feltet **Bølgefilterkode**. Bølgefilterkoder indeholder forespørgselskriterier for forsendelser, som er oprettet i formularen **Bølgefiltre**. Dette felt er ikke tilgængeligt for produktionsbølger eller kanban-bølger.
    > En grøn markering i kolonnen **På bølge** angiver, at forsendelsen er blevet føjet til bølgen.

### <a name="process-the-wave-to-create-the-picking-work"></a>Behandle bølgen for at oprette plukkearbejdet

Når en bølge er blevet oprettet og indeholder alle de nødvendige linjer, er du klar til at behandle den for at oprette det tilsvarende plukarbejde.

#### <a name="automatically-process-a-wave"></a>Behandle en bølge automatisk

Hvis du automatisk vil behandle en bølge, skal du konfigurere de relevante [bølgeskabeloner](wave-templates.md) med de nødvendige automatiske behandlingsindstillinger.

#### <a name="manually-process-a-wave"></a>Behandle en bølge manuelt

Du kan kun behandle en bølge, når **Bølgestatus** er *Oprettet*. Når du har behandlet en bølge, ændres **Bølgestatus** til *Afholdes*.

Hvis du vil behandle en bølge manuelt, der har alt det påkrævede indhold, skal du følge disse trin:

1. Afhængigt af den type bølge du vil behandle, skal du gøre ét af følgende:

    - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Vælg **Bølge** i handlingsruden.
    - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Produktionsbølger** \> **Alle produktionsbølger**. Vælg **Produktionsbølge** i handlingsruden.
    - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Kanban-bølger** \> **Alle kanban-bølger**. Vælg **Opret bølge** i handlingsruden.

1. Vælg den bølge, der skal behandles. Vælg **Behandl** i handlingsruden.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Frigiv bølgen til lagerstedet for at starte plukning og pakning

Du skal behandle en bølge, før du kan frigive den. Når du frigiver bølgen, er plukkearbejdet tilgængeligt på lagerstedet. Du kan annullere en bølge, efter den er udgivet, og tilføje flere linjer, men du kan ikke ændre linjerne.

#### <a name="automatically-release-a-wave"></a>Frigive en bølge automatisk

Hvis du automatisk vil behandle en bølge, skal du konfigurere de relevante [bølgeskabeloner](wave-templates.md) med de nødvendige automatiske behandlingsindstillinger.

#### <a name="manually-release-a-wave"></a>Frigive en bølge manuelt

Følg disse trin for at frigive en bølge manuelt:

1. Afhængigt af den type bølge du vil frigive, skal du gøre ét af følgende:

      - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Vælg **Bølge** i handlingsruden.
      - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Produktionsbølger** \> **Alle produktionsbølger**. Vælg **Produktionsbølge** i handlingsruden.
      - Vælg **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Kanban-bølger** \> **Alle kanban-bølger**. Vælg **Opret bølge** i handlingsruden.

1. Vælg den bølge, der skal frigives. Vælg **Frigiv bølge** i handlingsruden.

## <a name="containerize-a-wave"></a>Containerisere en bølge

Automatiseret containerisering opretter containere og plukkearbejde til forsendelser, når en bølge behandles. Yderligere oplysninger om, hvordan det konfigureres, finder du i [Containerisering](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Arbejde med den planlagte oprettelse af arbejde

Når funktionen *Planlæg oprettelse af arbejde* er aktiveret, opretter bølgebehandling det planlagte arbejde, som senere vil blive brugt af den nye arbejdsoprettelsesproces. Under oprettelse af arbejde blokeres arbejdet ved hjælp af funktionen *Blokering af arbejde i hele organisationen*. Du kan finde flere oplysninger i [Planlægge oprettelse af arbejde under bølge](configure-wave-schedule-work-creation.md).

Følgende rutediagram viser, hvordan planlagt arbejde oprettes under bølgebehandling.

![Planlæg arbejdsoprettelse](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlagt arbejde

På siden **Detaljer om planlagt arbejde** (**Lokationsstyring \> Arbejde \> Detaljer om planlagt arbejde**) vises oplysninger om det planlagte arbejde, der oprindeligt blev oprettet under behandling af bølger. Følgende værdier af **Processtatus** er tilgængelige:

- **Sat i kø** – Det planlagte arbejde venter på at blive brugt til at oprette arbejde.
- **Fuldført** – Det planlagte arbejde er brugt til at oprette arbejde.
- **Mislykkedes** – Bølgebehandlingen er mislykket. Bemærk, at det planlagte arbejde kan være i tilstanden **Mislykkedes** med eller uden relateret faktisk arbejde. Når den faktiske arbejdsoprettelsesproces mislykkes, forbliver det faktiske arbejde med status *Annulleret*.

### <a name="batch-job-for-the-work-creation-process"></a>Batchjob for processen til oprettelse af arbejde

Hvis du vil have vist batchjobbene til behandling af bølger, skal du vælge **Batchjob** i handlingsruden på siden **Alle bølger**.

Herfra kan du få vist alle oplysninger om batchopgaven for hvert enkelt batchjob-id.

## <a name="cancel-a-wave"></a>Annullere en bølge

Hvis det er nødvendigt, kan du annullere en bølge, der er blevet behandlet. Hvis du vil annullere en bølge og det plukkearbejde, der blev oprettet, skal du følge disse trin:

1. Afhængigt af den type bølge du vil annullere, skal du gøre ét af følgende:

      - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**.
      - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Produktionsbølger** \> **Alle produktionsbølger**.
      - Gå til **Lokationsstyring** \> **Fælles** \> **Bølger** \> **Kanban-bølger** \> **Alle kanban-bølger**.

1. Vælg den bølge, du vil annullere. I handlingsruden skal du under fanen **Arbejde** vælge **Annuller**.

## <a name="review-wave-batch-job-details"></a>Gennemgå oplysninger om batchjob for bølge

Brug siden **Detaljer om bølgebatchjob** til at undersøge batchjob og relaterede opgaver, der er tilknyttet en hvilken som helst bølge. Dette er især nyttigt ved fejlfinding af en bølge, der er mislykket. Uden denne funktion er det kun administratorer, der typisk har adgang til batchjoboplysninger. Siden **Detaljer om bølgebatchjob** kan gøres tilgængelige for brugere, der ikke er administratorer, og giver en skrivebeskyttet visning af batchjob og relaterede opgaver.

### <a name="enable-the-wave-batch-job-details-page"></a>Aktivere siden Detaljer om bølgebatchjob

Hvis systemet ikke allerede indeholder siden **Detaljer om bølgebatchjob**, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere *Detaljer om bølgebatchjob*.

### <a name="use-the-wave-batch-job-details-page"></a>Bruge siden Detaljer om bølgebatchjob

Siden **Detaljer om bølgebatchjob** kombinerer batchjob og batchjobopgaver, som giver dig mulighed for at undersøge alle trin i bølgen, uden at du behøver at navigere frem og tilbage mellem et enkelt batchjob og batchopgavelisten. Siden giver også adgang til batchloggen, og hvis du har de nødvendige tilladelser, findes der et link til siden **Batchjob**.

Hvis du vil åbne denne side, skal du vælge en af flere forskellige bølgesider og derefter vælge **Detaljer om bølgebatchjob** i handlingsruden.

## <a name="review-load-validation-and-error-messages"></a>Gennemgå lastvalidering og fejlmeddelelser

Under behandling af bølger validerer systemet og viser status for hver lastlinje i bølgen. Hvis der ikke forekommer advarsler, fortsætter den til næste bølgetrin. Hvis der forekommer advarsler, vises følgende fejl i stedet, efter at hele bølgen er valideret:

> Der blev fundet ugyldige lastlinjer i bølge. Fjern de ugyldige lastlinjer.

Derefter kan du gennemgå den endelige status for hver lastlinje i bølgen og rette alle advarsler, inden du forsøger igen. På den måde kan du se alle advarslerne på én gang, inden du genbehandler bølgen. (I tidligere versioner standsede systemet behandlingen af bølgen efter den første advarsel, så du kunne kun rette advarsler én ad gangen).

Den måde, som systemet viser statusmeddelelserne på, afhænger af, hvordan du har angivet indstillingen **Opret log med historik for behandling af bølger** på siden **Lokationsstyringsparametre**.

- Når **Opret log med historik for behandling af bølger** angives til *Nej*, vises statusmeddelelserne for lastlinjen i **infologgen**.
- Når **Opret log med historik for behandling af bølger** angives til *Ja*, vises statusmeddelelserne for lastlinjen på siden **Log for bølgebehandlingshistorik**. Du kan få vist loggen ved at gå **Lokationsstyring \> Udgående bølger \> Log for bølgebehandlingshistorik**.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurere eksempel på behandling af bølge](tasks/configure-wave-processing.md)
- [Bølgeskabeloner](wave-templates.md)
- [Containerisering](wave-containerization.md)