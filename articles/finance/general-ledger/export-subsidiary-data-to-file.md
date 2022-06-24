---
title: Eksporter datterselskabsdata til filer
description: Denne artikel forklarer, hvordan du forbereder eksport af data fra Microsoft Dynamics 365 Finance og derefter importerer dem til en konsolideret juridisk enhed.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7c5334e206d28a5ae1c8097db5356cd1057b7180
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876147"
---
# <a name="export-subsidiary-data-to-files"></a>Eksporter datterselskabsdata til filer

[!include [banner](../includes/banner.md)]

Brug siden **Eksport** (**Systemadministration \> Arbejdsområder \> Import/eksport**) til at forberede eksport af datterselskabsdata til filer, der derefter kan importeres til en konsolideret juridisk enhed. Yderligere oplysninger om import- og eksportprocesser i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Opret en juridisk enhed til brug i konsolideringsprocessen. Du kan finde flere oplysninger om at oprette juridiske enheder i [Oprette juridisk enhed](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Du kan finde flere oplysninger i [Forberede en juridisk enhed til brug i konsolideringsprocessen](prepare-company-for-consolidation.md) og [Konfigurere en juridisk enhed til konsolidering](set-up-subsidiary-company-for-consolidation.md). 

2. Gå til **Konsolideringer \> Eksporter firmasaldi**. På siden **Eksporter firmasaldi** skal du angive detaljerne om konsolideringen under fanen **Kriterium** ved at angive følgende felter.

    | Felt                             | Betegnelse |
    |-----------------------------------|-------|
    | Hovedkonto                      | Angiv de konti, der skal konsolideres. Hvis du vil medtage alle konti, skal du lade dette felt være tomt. |
    | Brug koncernkonto         | Hvis du har angivet koncernkonti, skal du angive denne indstilling til **Ja**. |
    | Vælg koncernkonto fra | Vælg enten **Hovedkonto** eller **Konsolideringskontogruppe**. |
    | Koncernkontogruppe       | Vælg en koncernkontogruppe, du vil klassificere koncernkontoen efter. |
    | Konsolideringsperiode              | Angiv "fra" og "til" datointerval til konsolideringen. |
    | Medtag faktiske beløb            | Angiv denne indstilling til **Ja**, hvis du vil medtage faktiske beløb. |
    | Medtag budgetbeløb            | Angiv denne indstilling til **Ja**, hvis du vil medtage budgetbeløb i konsolideringer. |
    | Budgetmodeller                     | Angiv den budgetmodel, der skal medtages. |

3. Angiv på fanen **Økonomiske dimensioner** detaljerne i konsolideringen.

    - Angiv de økonomiske dimension, der skal overføres fra transaktionerne i datterselskabskontiene til transaktionerne i den konsoliderede juridiske enhed.
    - Vælg de økonomiske dimensioner i oversigten .
    - Identificer den korrekte specifikation for hver økonomisk dimension, der konsolideres. De tilgængelige indstillinger omfatter **Dimension**, **Gruppedimension**, **Regnskab** og **Konto**.

        > [!NOTE]
        > Med indstillingen **Gruppedimension** kan du definere den dimensionsværdi, der bruges af den gruppe af firmaer, der konsolideres.

    - Angiv den segmentrækkefølge, der skal konsolideres i.

4. På fanen **Juridiske enheder** skal du følge disse trin for at angive den juridiske enhed, der skal eksporteres:

    1. Vælg **Ny**.
    2. Angiv den juridiske enhed i feltet **Juridisk kildeenhed**.

        Hvis samme kriterier gælder for flere datterselskaber, der er i samme database, kan du overføre data fra disse datterselskaber til separate eksportfiler i en enkelt handling:

        1. Opret en linje for hver juridisk datterselskabsenhed, hvis konti skal eksporteres til filer. Disse filer importeres senere til den konsoliderede juridiske enhed.
        2. For hvert datterselskab skal du angive navnet på datterselskabet og navnet på den eksportfil, der oprettes under eksportjobbet.

    3. I feltet **Kontotype til omregningsdifferencer** skal du vælge **Drift og tab** eller **Balance**.
    4. Angiv et filnavn til den eksportfil, der oprettes.

5. Vælg **OK** for at køre eksporten.

Når eksporten er fuldført, modtager du en meddelelse, der viser antallet af poster, der er gemt i hver fil. Derefter kan du importere filerne til den konsoliderede juridiske enhed.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
