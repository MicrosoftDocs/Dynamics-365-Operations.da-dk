---
title: Konfigurere projektressourcer
description: Dette emne giver oplysninger om opsætning eller anmodning om projektressourcer.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760508"
---
# <a name="set-up-project-resources"></a>Konfigurere projektressourcer

[!include [banner](../includes/banner.md)]

Du skal oprette en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet. Projektledere kan udføre ressourceudjævning som en del af ressourceoptimering, når de konfigurerer kalenderen. Baseret på kalendertidsplanen kan der sættes begrænsninger på ressourcer. Du kan oprette en kalender på siden **Kalendere**.

Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i det firma, du konfigurerer ressourcer til. Du kan også vælge arbejdere fra andre firmaer i organisationen. Disse arbejdere kaldes interne ressourcer.

Nedenstående fremgangsmåder forklarer, hvordan du konfigurerer en arbejder som en projektressource i virksomheden, og hvordan du opretter en intern projektressource.

## <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1. På siden **Arbejdere** på listen **Arbejdere** skal du vælge den arbejder, som du vil tilføje som en projektressource, og åbne arbejderposten.
2. I handlingsruden skal du vælge **Projekt** &gt; **Konfiguration** &gt; **Opsætning af projekt**.
3. Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags foreløbig tildeling. Foreløbige tildelinger kan bruges, når ressourcestyringen eller projektlederen i forvejen ved, hvilke projekter ressourcen skal arbejde på. Foreløbige tildelinger kan også være baseret på anmodning fra en projektsponsor eller kunde. Når du vil tildele et projekt foreløbigt, skal du vælge det relevante projekt på siden **Tildel projekter** under fanen **Projekter** på listen **Resterende projekter**.

## <a name="set-up-an-intercompany-resource"></a>Opret en intern ressource

Når du opretter en arbejder som en intern ressource, skal du fuldføre opsætningen både i firmaet, der udlåner, og i firmaet, der låner.

### <a name="in-the-lending-company"></a>I firmaet, der udlåner

1. I Finance skal du kontrollere, at firmaet, der låner, er markeret, og derefter skal du fuldføre proceduren i det forrige afsnit, "Konfigurere en arbejder som en projektressource".
2. På siden **Mellemregning** skal du vælge **Ny**.
3. I feltet **Id for juridisk enhed** skal du vælge firmaet, der udlåner. Udfyld de resterende felter efter behov, og vælg derefter **Gem**.
4. På siden **Intern afregningspris** skal du vælge **Ny**.
5. I feltet **Udlånt til (juridisk enhed)** skal du vælge det relevante firma.
6. Hvis du kun vil låne firmaet, der låner, den ressource, du oprettede i starten af dette afsnit i feltet **Ressource** skal du vælge navnet på den ressource, du har oprettet. Hvis du vil gøre alle ressourcer i firmaet tilgængelige for firmaet, der låner, skal du lade feltet **Ressource** stå tomt.
7. På siden **Parametre for projektstyring og regnskab** under fanen **Intern** skal du angive indstillingen **Aktivér intern ressourceplanlægning og timesedler** til **Ja**.

### <a name="in-the-borrowing-company"></a>I firmaet, der låner

- På siden **Liste over ressourcer** skal du i søgefiltret angive navnet på den ressource, du oprettede for firmaet, der udlåner, for at kontrollere, at navnet er inkluderet på ressourcelisten for firmaet, der låner.

## <a name="request-project-resources"></a>Anmode om projektressourcer
Planlægningsfunktionen projektressource giver kun ressourcechefer mulighed for at distribuere bemandingsressourcer på opgaver eller projekter. Udfør følgende opgaver for at aktivere denne funktion, eller kontrollér, at de er blevet fuldført:

- Konfigurer nummerserier.
- Konfigurer arbejdsgange i Projektstyring og regnskab.
- Aktivér arbejdsgange for ressourceanmodning

Når de foregående opgaver er fuldført, kan du udføre følgende opgaver efter behov:

- Opret en ressourceanmodning fra en midlertidigt reserveret bemandingsressource.
- Overvåg ressourceanmodninger.
- Opfyld ressourceanmodninger.
- Anmod om en bemandingsressource fra et WBS.
- Reservér ressourcer til et projekt uden at have en anmodning om en bemandingsressource.
