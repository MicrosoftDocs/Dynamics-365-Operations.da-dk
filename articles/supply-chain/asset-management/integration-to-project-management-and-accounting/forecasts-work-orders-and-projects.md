---
title: Budgetter, arbejdsordrer og projekter
description: Dette emne forklarer integrering af budgetter og arbejdsordrer i modulet Projektstyring og regnskab i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886810"
---
# <a name="forecasts-work-orders-and-projects"></a>Budgetter, arbejdsordrer og projekter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Styring af aktiver udføres integrationen med modulet **Projektstyring og regnskab** for at optimere omkostningsstyringen, hvilket giver brugerne mulighed for at spore omkostninger i budgetter for vedligeholdelsesjobtyper og arbejdsordrejob.

Der skal foretages to indstillinger, før der kan spores budgetter for vedligeholdelsesjobtyper:

1. Vælg et projekt i **Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring** > **Aktiver**-link > oversigtspanelet **Projekt** > feltet **Vedligeholdelsesprognoseprojekt**.

2. Når du opretter en standardlinje for en vedligeholdelsesjobtype i **Standarder for vedligeholdelsesjobtype**, oprettes der automatisk et aktivitetsnummer for linjen (**Styring af aktiver** > **Opsætning** > **Job** > **Standarder for vedligeholdelsesjobtype**).

Budgetter for vedligeholdelsesjobtyper tjener to formål: Du kan spore omkostninger til budgetter for vedligeholdelsesjobtyper i modulet **Projektstyring og regnskab**. Desuden overføres budgetter automatisk til et jobprojekt for en arbejdsordre, når du vælger en vedligeholdelsesjobtype i et arbejdsordrejob.

Hvis du vil spore omkostninger for job i arbejdsordrer, skal du først konfigurere arbejdsordreprojekter. Se afsnittet [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md) for at få en beskrivelse af proceduren.

## <a name="work-order-job-projects"></a>Projekter for arbejdsordrejob

Når du opretter et arbejdsordrejob på en arbejdsordre, bestemmes arbejdsordreprojektet af opsætningen af det overordnede projekt for arbejdsordrer i **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**.

Projekter for arbejdsordrejob oprettes ved hjælp af en kombination af følgende oplysninger om arbejdsordrer:

- Den arbejdsordretype, der er valgt på arbejdsordren 
- Det arbejdssted, der er relateret til aktivet på arbejdsordrejobbet
- Den aktivtype, der er relateret til aktivet på arbejdsordrejobbet  
- Det forventede start- og sluttidspunkt, der er angivet på arbejdsordren  

Det er muligt, at ikke alle ovennævnte oplysninger findes på en arbejdsordre. Derfor sker søgningen efter et overordnet projekt til en arbejdsordre ved hjælp af den tilgængelige kombination af data og valg af det projekt-id, der svarer til arbejdsordredata.

Eksempel: Opsætningen af aktivtypen "Truck Engine" i figuren nedenfor betyder, at alle de arbejdsordrejob, der oprettes med den pågældende aktivtype, vil være et underprojekt af projekt-id'et "000186".

![Figur 1](media/01-integration-to-pma.png)

Formålet med projekt-id'et på arbejdsordrejobbet og det relaterede aktivitetsnummer (**Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** > vælg arbejdsordre på liste > oversigtspanelet **Linjedetaljer** > feltet **Projekt-id** og feltet **Aktivitetsnummer**) er at spore omkostninger, der vedrører arbejdsordrejobbet, og det aktiv, der er valgt på arbejdsordrejobbet, i modulet **Projektstyring og regnskab**. 

I figuren nedenfor ser du en grafisk oversigt over projekter for arbejdsordrer og relaterede projektaktiviteter.

![Figur 2](media/02-integration-to-pma.png)

Når et nyt arbejdsordrejob oprettes på en arbejdsordre, oprettes der automatisk et arbejdsordreprojekt for jobbet. De økonomiske dimensioner for aktivet, der er tilknyttet arbejdsordrejobbet, overføres automatisk til arbejdsordreprojektet. Den projektaktivitet, der er oprettet for et arbejdsordrejob, har relaterede oplysninger tilknyttet vedrørende vedligeholdelsesjobtype, variant af vedligeholdelsesjobtype og fag. Disse data er nyttige, hvis du f.eks. opretter en indkøbsordre ud fra en arbejdsordre se( [Indkøb](../work-orders/procurement.md)), eller hvis du bruger modulet **Projektstyring og regnskab** til tidsregistrering.  

Hvis aktivet er installeret på et arbejdssted, og dette aktiv senere installeres på et andet arbejdssted, opdateres de økonomiske dimensioner, der er relateret til det nye arbejdssted, automatisk på aktivet. Når du efterfølgende opretter et arbejdsordrejob for aktivet, henter arbejdsordreprojektet for arbejdsordrejobbet automatisk de økonomiske dimensioner, der nu er relateret til aktivet. Det betyder, at omkostninger altid kan spores på de arbejdssteder, hvor et aktiv var installeret på et givet tidspunkt, når du bruger arbejdssteder. Den automatiske opdatering af økonomiske dimensioner sikrer en fuldstændig sporbarhed af omkostninger til projektstyring og rapportering.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Arbejdsordreprojekter, livscyklustilstande for arbejdsordrer, projektstadier og projekttyper

For at sikre korrekt brug af livscyklusser for arbejdsordrer og relaterede projektstadier i arbejdsordrer skal du overveje afhængighederne i forhold til modulet **Projektstyring og regnskab**:

- I modulet **Projektstyring og regnskab** defineres projektstadier for projekttyper i **Parametre for projektstyring og regnskab**.  
- I **Parametre for projektstyring og regnskab** skal du huske at markere de relevante afkrydsningsfelter for projektstadier for alle de projekttyper, du skal bruge. I figuren herunder er de fem stadier **Oprettet** - **Forkalkuleret** - **Planlagt** - **Under behandling** - **Afsluttet** blevet valgt for projekttyperne "Tid og materiale" og "Intern". Disse fem stadier er relevante for både interne vedligeholdelses- og servicevedligeholdelsesjob.  
- I **Styring af aktiver** defineres projekttyper af de projektgrupper, du opretter i formen **Opsætning af arbejdsordreprojekt** > link til **Projektgruppe**.  
- Opsætningen af projektgrupper i **Opsætning af arbejdsordreprojekt** bruges, når du opretter arbejdsordrer. Når en arbejdsordre er oprettet, oprettes der automatisk et arbejdsordreprojekt for arbejdsordren.  
- Livscyklustilstande for arbejdsordrer skal hver have et relateret projektstadie.  
- Projektstadiet, der er knyttet til en livscyklustilstand for en arbejdsordre, skal defineres som et aktivt stadie for den projektgruppe, der er defineret i arbejdsordreprojektet. Arbejdsordreprojektet oprettes automatisk på en arbejdsordre.  
- Når du opretter en ny arbejdsordre, er den automatiske tildeling af et arbejdsordreprojekt baseret på opsætningen i **Opsætning af arbejdsordreprojekt** (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**).  

Tilknytninger mellem projektgrupper for arbejdsordrer, relaterede projekttyper, projektstadier og livscyklustilstande for arbejdsordrer vises i nedenstående figurer.  

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

Se [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md) for at få oplysninger om, hvordan du kan konfigurere arbejdsordreprojekter, og [Livscyklustilstande for arbejdsordre](../setup-for-work-orders/work-order-lifecycle-states.md) vedrørende, hvordan du kan oprette livscyklustilstande for arbejdsordrer.

I figuren herunder vises en grafisk oversigt over de forskellige projekter, der oprettes i modulet **Styring af aktiver** for at tillade integration med modulet **Projektstyring og regnskab** samt de arbejdsprocesser, som projekterne er relateret til.

![Figur 6](media/06-integration-to-pma.png)

