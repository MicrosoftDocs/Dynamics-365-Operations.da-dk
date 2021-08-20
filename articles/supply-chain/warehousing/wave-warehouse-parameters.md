---
title: Lagerstedsparametre til bølgebehandling
description: Dette emne beskriver, hvordan du konfigurerer lagerstedsparametre til bølgebehandling. Du kan bruge bølgebehandling til at gruppere plukkearbejde for flere arbejdsordrer i en enkelt bølge.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: e26c1b308242176e916d9e930f7eded5df49de6683af03dbdab42358c724831a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766529"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Lagerstedsparametre til bølgebehandling

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer lagerstedsparametre til bølgebehandling. Du kan bruge bølgebehandling til at gruppere plukkearbejde for flere arbejdsordrer i en enkelt bølge.

Hvis du vil bruge bølgebehandling, skal du angive følgende på siden **Parametre for lokationsstyring**:

- Hvis du kan behandle bølger ved hjælp af et batchjob.
- Hvis du indsamler oplysninger i en logfil, når bølger behandles.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Konfigurere lokationsstyringsparametre for bølgebehandling

Følg disse trin for at konfigurere lagerstedsparametre for bølgebehandling:

1. Gå til **Lokationsstyring** \> **Konfiguration** \> **Parametre til lokationsstyring**.

1. Foretag følgende indstillinger i oversigtspanelet **Bølgebehandling**:

    - **Batchgruppe til behandling af bølge** - Vælg den batchgruppe, der skal bruges, når du behandler bølger ved hjælp af batchjob. Batchgruppen angiver den server, hvor batchjobbene køres på.
    - **Udfør behandling af bølger i batch** – Vælg, om du vil aktivere, at bølger behandles automatisk af et batchjob. Du skal angive dette til *Ja*, hvis du vil bruge parallel behandling. Du kan konfigurere batchjobbet på siden **Udfør behandling af bølger**. (Se også noten i slutningen af denne liste).
    - **Opret log over bølgestatus** – Vælg, om systemet skal generere en logpost, hver gang der fordeling af en vare og dens dimensioner starter og slutter. Du skal kun aktivere denne log, når du har brug for den, f.eks. under den indledende test eller ved fejlfinding. Du finder flere oplysninger under [Bølgefordeling](wave-allocation-method.md).
    - **Opret log med historik for behandling af bølger** – Vælg, om du automatisk vil gemme oplysninger om en bølge i en logfil, efter at bølgen er behandlet, herunder den parallelle behandling af ventende fordelinger. Du skal normalt kun aktivere dette under fejlfinding, da det tilføjer ekstra indirekte omkostninger. Du kan få vist loggen ved at gå **Lokationsstyring \> Udgående bølger \> Log for bølgebehandlingshistorik**. Du kan finde flere oplysninger under [Bølgeoprettelse og -behandling](wave-processing.md).
    - **Opret log med containeriseringshistorik** – Vælg, om du automatisk vil gemme oplysninger om containerisering for en bølge i en logfil, efter at bølgen er behandlet. Du kan få vist loggen ved at gå **Lokationsstyring \> Pakning og containerisering \> Containeriseringshistorik**.
    - **Vent på lås (ms)** – Angiv tid i millisekunder, som et fordelingstrin venter på en systemressource, der er låst af et andet fordelingstrin. Når denne tid overskrides, behandles bølgen ikke, og der vises en fejlmeddelelse.

1. Foretag følgende indstilling i oversigtspanelet **Frigiv til lagersted**:

    - **Fejl ved batchfejl** – Vælg, om der skal genereres en fejl, når en frigivelse til lagerstedsbatchjobbet mislykkes. Hvis denne indstilling er aktiveret, afsluttes mislykkede job med statussen *Fejl*. Hvis den er deaktiveret, afsluttes mislykkede job med statussen *Afsluttet*.

> [!NOTE]
> I den bølgeskabelon, der bruges til at behandle bølgen, kan du angive de indstillinger, der automatiserer bølgebehandlingen. Hvis du angiver en tidsplan for batchjobbet, skal du koordinere timingen med indstillingerne for automatisering i bølgeskabelonen. Du kan finde flere oplysninger i [Oprette en bølgeskabelon](wave-templates.md).
>
> Hvis du bruger *Transportstyring* og *Avanceret lokationsstyring*, kan du angive, om du vil konsolidere laster, når du behandler en bølge. For eksempel er dette nyttigt, når flere små laster kan leveres på samme tid. Hvis du vil konsolidere laster, når du behandler en bølge, skal du markere afkrydsningsfeltet **Konsolider laster under bølgebehandling** under fanen **Laster**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Konfigurere en hel eller delvis reservation for produktionsbølger

Når det gælder salgsordrer og kanban-ordrer, skal der reserveres lager, før ordren frigives til lagerstedet. Ellers kan varerne eller fordelingslinjerne ikke behandles i en bølge. Produktionsordrer er dog lidt mere fleksible. Når det gælder produktionsordrer, kan du angive følgende:

- Giv mulighed for, at produktionsordrer kan frigives til lagerstedet, selvom alle materialerne ikke kan reserveres. Hvis du vælger denne indstilling, skal du gentage frigivelsen til lagerprocessen manuelt, når de ekstra materialer bliver tilgængelige. Dette er f.eks. nyttigt, hvis du har de materialer, du skal bruge til at starte en produktion og kan vente, indtil de ekstra materialer bliver tilgængelige.
- Kræver, at alle materialer reserveres, før det er muligt at frigive en ordre til lagerstedet.

Følg disse trin for at kræve fuld reservation eller tillade delvis reservation:

1. Gå til **Produktionsstyring** \> **Konfiguration** \> **Produktionsstyringsparametre**.
1. Vælg standardindstillingen i feltet **Frigiv til lagersted** under fanen **Generelt**.
