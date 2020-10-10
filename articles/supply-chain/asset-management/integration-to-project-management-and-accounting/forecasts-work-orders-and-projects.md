---
title: Budgetter, arbejdsordrer og projekter
description: Dette emne forklarer integrering af budgetter og arbejdsordrer i modulet Projektstyring og regnskab i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888805"
---
# <a name="forecasts-work-orders-and-projects"></a>Budgetter, arbejdsordrer og projekter

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver udføres integrationen med modulet **Projektstyring og regnskab** for at hjælpe med at optimere omkostningsstyringen, så brugerne kan spore omkostninger i budgetter for vedligeholdelsesjobtyper og arbejdsordrejob.

Sporing af prognoser for vedligeholdelsesjobtyper kræver to indstillinger:

1. Vælg et projekt i **Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring**, og klik derefter på fanen **Aktiver** på oversigtspanelet **Projekt** i feltet **Vedligeholdelsesprognoseprojekt**, og vælg et projekt.

2. Når du opretter en standardlinje for en vedligeholdelsesjobtype, oprettes der automatisk et aktivitetsnummer for linjen på siden **Standarder for vedligeholdelsesjobtype** (**Styring af aktiver** > **Opsætning** > **Job** > **Standarder for vedligeholdelsesjobtype**).

Budgetterede job af typen vedligeholdelse tjener to formål: 

- Du kan spore omkostninger i budgetter for vedligeholdelsesjobtyper i modulet **Projektstyring og regnskab**. 
- Budgetter overføres automatisk til et jobprojekt for en arbejdsordre, når du vælger en vedligeholdelsesjobtype i et arbejdsordrejob.

Hvis du vil spore omkostninger for job i arbejdsordrer, skal du først konfigurere arbejdsordreprojekter. Du kan finde flere oplysninger i [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Projekter for arbejdsordrejob

Når du opretter et arbejdsordrejob på en arbejdsordre, bestemmes arbejdsordreprojektet af opsætningen af det overordnede projekt for arbejdsordrer på siden **Opsætning af arbejdsordreprojekt** (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**).

Projekter for arbejdsordrejob oprettes ved hjælp af en kombination af følgende oplysninger om arbejdsordrer:

- Den arbejdsordretype, der er valgt på arbejdsordren 
- Det arbejdssted, der er relateret til aktivet på arbejdsordrejobbet
- Den aktivtype, der er relateret til aktivet på arbejdsordrejobbet  
- Det forventede start- og sluttidspunkt, der er angivet på arbejdsordren  

Nogle af disse oplysninger findes muligvis ikke på en arbejdsordre. Derfor sker søgningen efter et overordnet projekt til en arbejdsordre ved hjælp af den tilgængelige kombination af data og valg af det projekt-id, der svarer til arbejdsordredata.

Se f.eks. følgende illustration: På grund af den måde, hvorpå **lastbilsmotorens** aktivtype er konfigureret, vil alle de arbejdsordrer, der oprettes med **lastbilmotorens** aktivtype, være et underprojekt med projekt-id 000186.

![Figur 1](media/01-integration-to-pma.png)

Formålet med projekt-id'et på arbejdsordrejobbet og det relaterede aktivitetsnummer er at spore omkostninger, der er relateret til arbejdsordrejobbet, og det aktiv, der er valgt på det, i modulet **Projektstyring og regnskab**. (Hvis du vil have vist projekt-id og aktivitetsnummer, skal du vælge **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** og derefter vælge arbejdsordren. I oversigtspanelet **Linjedetaljer** viser feltet **Projekt-id** projekt-id'et, og feltet **Aktivitetsnummer** viser aktivitetsnummeret). Du kan finde flere oplysninger om omkostningsstyring i Styring af aktiver ved at se [Omkostnings- og datokontrol](../controlling-and-reporting/cost-and-date-control.md).

Følgende illustration viser en grafisk oversigt over projekter for arbejdsordrer og relaterede projektaktiviteter.

![Figur 2](media/02-integration-to-pma.png)

Når et nyt arbejdsordrejob oprettes på en arbejdsordre, oprettes der automatisk et arbejdsordreprojekt for jobbet. De økonomiske dimensioner for aktivet, der er tilknyttet arbejdsordrejobbet, overføres automatisk til arbejdsordreprojektet.

Den projektaktivitet, der er oprettet for et arbejdsordrejob, har relaterede oplysninger tilknyttet. Disse oplysninger handler om vedligeholdelsesjobtype, vedligeholdelsesjobtypevariant og handel. Dette er nyttigt, hvis du f.eks. opretter en indkøbsordre ud fra en arbejdsordre (se [Indkøb](../work-orders/procurement.md)), eller hvis du bruger modulet **Projektstyring og regnskab** til tidsregistrering.

Hvis aktivet er installeret på et arbejdssted, og dette aktiv senere installeres på et andet arbejdssted, opdateres de økonomiske dimensioner, der er relateret til det nye arbejdssted, automatisk på aktivet. Når du derefter opretter et arbejdsordrejob for aktivet, henter arbejdsordreprojektet for arbejdsordrejobbet automatisk de økonomiske dimensioner, der nu er relateret til aktivet. Når du derfor bruger arbejdssteder, kan omkostningerne altid spores på de arbejdssteder, hvor et aktiv var installeret på et givet tidspunkt. Den automatiske opdatering af økonomiske dimensioner hjælper med at garantere en fuldstændig sporbarhed af omkostninger til projektstyring og rapportering.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Arbejdsordreprojekter, livscyklustilstande for arbejdsordrer, projektstadier og projekttyper

For at hjælpe med at garantere at livscyklusser for arbejdsordrer og relaterede projektstadier i arbejdsordrer bruges korrekt, skal du overveje afhængighederne i forhold til modulet **Projektstyring og regnskab**:

- I modulet **Projektstyring og regnskab** opsættes projektstadier for projekttyper på siden **Parametre for projektstyring og regnskab**.  
- På siden **Parametre for projektstyring og regnskab** skal du bruge afkrydsningsfelterne til at vælge relevante projektstadier for alle de projekttyper, du skal bruge. I de følgende illustrationer er der valgt fem stadier (**Oprettet**, **Forkalkuleret**, **Planlagt**, **Under behandling** og **Afsluttet**) for projekttyperne **Tid og materiale** og **Intern**. Disse fem stadier er relevante for både interne vedligeholdelsesjob og servicevedligeholdelsesjob.
- I modulet **Styring af aktiver** defineres projekttyper af de projektgrupper, du opretter på siden **Opsætning af arbejdsordreprojekt** > fanen **Projektgruppe** (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**).  
- De projektgrupper, der er opsat på siden **Opsætning af arbejdsordreprojekt**, bruges, når du opretter arbejdsordrer. Når en arbejdsordre er oprettet, oprettes der automatisk et arbejdsordreprojekt for arbejdsordren.  
- Hver livscyklustilstand for arbejdsordre skal have et relateret projektstadie.  
- Projektstadiet, der er relateret til en livscyklustilstand for en arbejdsordre, skal defineres som et aktivt stadie for den projektgruppe, der er defineret i arbejdsordreprojektet. Arbejdsordreprojektet oprettes automatisk på en arbejdsordre.
- Når du opretter en ny arbejdsordre, er den automatiske tildeling af et arbejdsordreprojekt baseret på opsætningen på siden **Opsætning af arbejdsordreprojekt**.  

Følgende illustrationer viser tilknytningerne mellem projektgrupper for arbejdsordrer, relaterede projekttyper, projektstadier og livscyklustilstande for arbejdsordrer.

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

Du kan finde flere oplysninger om, hvordan du konfigurerer arbejdsordreprojekter ved at se [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md). Du kan finde flere oplysninger om, hvordan du opretter livscyklustilstande for arbejdsordrer i [Livscyklustilstande for arbejdsordre](../setup-for-work-orders/work-order-lifecycle-states.md).

I følgende illustration vises en grafisk oversigt over de forskellige projekter, der oprettes i modulet **Styring af aktiver**, for at aktivere integration med modulet **Projektstyring og regnskab**. Den viser også de arbejdsprocesser, som projekterne er relateret til.

![Figur 6](media/06-integration-to-pma.png)

