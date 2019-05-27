---
title: Styre lagerarbejdere
description: I denne artikel beskrives, hvordan du kan bruge Dynamics 365 for Finance and Operations til at styre og overvåge det arbejde, der udføres af medarbejderne på dine lagersteder.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5a35d0a52d6f5bf995ce54f10eab92147b0e76a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572552"
---
# <a name="manage-warehouse-workers"></a>Styre lagerarbejdere

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan du kan bruge Microsoft Dynamics 365 for Finance and Operations til at styre og overvåge det arbejde, der udføres af medarbejderne på dine lagersteder.

Hvis du bruger funktionerne i Lagerstedsstyring, henvises alle arbejderhandlinger på lagersted som *arbejde*. Arbejde som f.eks. plukning, flytning og optælling af den disponible lagerbeholdning registreres ved hjælp af mobilenheder. Før en lagermedarbejder kan udføre arbejdet, skal han eller hun skal være tilknyttet en arbejder i Personale. Hver **Arbejder**-konto kan have flere lagerstedsarbejdsbrugere, der er knyttet til den. Disse arbejdsbrugere kan arbejde på forskellige lagersteder og kan have forskellige adgangsniveauer til forskellige mobilenhedsmenuer. Du kan tænke på lagerstedsarbejdsbrugerne som flere logons for den valgte arbejder. De enkelte arbejdsbrugere har et standardlagersted, og bestemte arbejdsgange vises i de menupunkter, der er tilgængelige for den arbejdsbruger. 

Hvis du vil oprette en ny arbejdsbruger skal du på siden **Arbejdere** under fanen **Generelt** klikke på **Arbejder** i sektionen **Lagersteder**. Du skal angive et bruger-id, et brugernavn, et standardlagersted og et menunavn. Denne menu er indlæst, når brugeren logger på Warehouse Mobile Device Portal, og gør det muligt at definere, hvilke menupunkter brugeren har adgang til. 

Som en del af opsætningen for hver arbejdsbruger kan du også definere bestemte arbejdsgange. Du kan for eksempel bruge feltet **Er en cyklusoptællingssupervisor** til at angive, om brugeren kan behandle justeringer for at afvikle optællingsuoverensstemmelser under en optællingshandling, eller om disse justeringer først skal revideres af en anden person.

## <a name="defining-labor-standards"></a>Definere arbejdsstandarder
Siden **Arbejdsstandarder** gør det muligt at definere beregningsmetoder, som systemet bruger til at beregne den anslåede tid, som bestemt type arbejde kræver. Denne definition kan indstilles på et generisk niveau eller på et bestemt niveau. Du kan for eksempel definere den tid, der er nødvendig for at behandle salgsordre med pluk pr. vægt for en bestemt enhedsdefinition, når en bestemt plukproces anvendes. På samme tid kan du registrere den tid, der er baseret på en anden beregningsmetode, for put-handlingen for den disponible lagerbeholdning, der er plukket. 

Hvis du vil aktivere de arbejdsstandarder, du har defineret, skal du vælge indstillingen **Tillad arbejdskraft standarder** for hvert lagersted, hvor arbejdsstandarder skal bruges.

## <a name="monitoring-and-controlling-warehouse-work"></a>Overvåge og styre lagerstedsarbejde
Siden **Alt arbejde** gør det muligt at overvåge og vedligeholde alt arbejde, der er planlagt, igangsat og afsluttet. På denne side kan du opdatere forskellige processer som f.eks. lagerstedsarbejde, brugertildelinger og arbejdsprioritet. Du kan også gå længere ned i de oplysninger, der er relateret til arbejdshovedet og arbejdslinjerne, for at få en forståelse af de forventede eller fuldførte arbejdsprocesser. 

Hvis du aktiverer indstillingen **Arbejdsstandarder**, kan du se den beregnede estimerede tid for arbejdet. Når arbejdet derefter er behandlet, vises den faktiske tid også for hver arbejdshandling. På denne måde kan du sammenligne estimerede tidsberegninger med den faktiske tid. 

Desuden kan du bruge den anslåede tid i reglerne til automatisk at opdele arbejde under arbejdsoprettelsen. På denne måde kan du afbalancere arbejdet ud fra tid, det forventes at fuldføre opgaverne. 

Analyse af den tid, der bruges til at behandle arbejdselementer, kan forbedre lagermedarbejderes effektivitet. Følgende rapporter er tilgængelige til at hjælpe med denne analyse:

-   **Arbejde efter bruger** – denne rapport viser arbejdernes produktivitet baseret på de faktiske tider mod forventede tider.
-   **Arbejde efter arbejdstransaktionstype** – du kan bruge denne rapport til at undersøge ineffektivitet i specifikke lagerstedsprocesser. Du bemærker eksempelvis, at pluk til flytteordrer tager længere tid i denne uge end i tidligere uger. Du kan derefter bruge disse oplysninger til yderligere undersøgelse.




