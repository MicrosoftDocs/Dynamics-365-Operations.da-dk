---
title: Oprette et projektteam
description: Dette emne indeholder oplysninger om, hvordan du opretter og styrer projektteams.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760504"
---
# <a name="create-a-project-team"></a>Oprette et projektteam

[!include [banner](../includes/banner.md)]

Hvis en projektleder vil bruge de roller, der er tidligere angivet i et projekt, skal han eller hun knytte rollerne til projektet. Der kan tildeles flere roller til et projekt. For at undgå forvirring mærkes disse roller automatisk under reservation. Hvis projektlederen f.eks. kræver tre softwareteknikere, oprettes der automatisk tre softwareteknikerroller, der navngives **softwaretekniker 1**, **softwaretekniker 2** og **softwaretekniker 3**. Hvis rollekarakteristika tidligere var defineret for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere karakteristika efter behov for at indsnævre søgningen yderligere.

Visningsindstillinger kan også tilpasses for at give et bedre overblik over ressourcetilgængelighed. Er der indstillinger, som kan vise tilgængelighed pr. time, dag, uge, måned, kvartal og år. Der er også en indstilling, som kan vise tilgængelig og resterende kapacitet for ressourcer. Denne indstilling er nyttig til tidsstyring, når du skal vurdere ledig tid til aktiviteter eller ressourcetilgængelighed.

Projektlederen kan vælge en rolle på siden, og hvis der er en tilgængelig ressource, der passer til behovet, kan han eller hun vælge at reservere en ressource, der kan udfylde rollen. Bemærk, at ressourcerne ikke behøver at være reserveret på dette tidspunkt i planlægningen. Når du opretter et arbejdsopgavehierarki, kan du erstatte roller med bemandingsressourcer til projektet. Hvis roller erstattes med bemandingsressourcer i arbejdsopgavehierarkiet, opdaterer ressourcekonfigurationen automatisk projektteamlisten og -planlægningen.

[![Projektteamliste, der omfatter både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for reservation af en ressource til et projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse reservationsindstillinger kan annulleres når som helst, hvis ressourcetildelinger ændres. Der findes to typer reservationer:

- **Definitiv reservation** – Ressourcereservationen blev godkendt og bekræftet for arbejde på opgaven for den angivne varighed.
- **Foreløbig reservation** – Ressourcereservationerne er foreløbig angivet til at arbejde på opgaven for den angivne varighed.

I følgende fremgangsmåde beskrives, hvordan et projektteam oprettes.

## <a name="create-a-project-team"></a>Oprette et projektteam

1. Vælg et projekt på listesiden **Alle projekter**, og vælg derefter **Rediger**.
2. Under fanen **Projektteam og planlægning** i feltet **Planlæg slutdato** skal du angive startdato for tidsplanen plus en måned. For eksempel hvis tidsplanens startdato er 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.
3. Vælg **Tilføj**.
4. I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Seniorprojektleder**.
5. Vælg **Påkrævede kompetencer**.
6. På siden **Vælg egenskaber** er de karakteristika, som du tidligere har angivet for seniorprojektlederrollen markeret som standard. Vælg **OK**.
7. På siden **Føj roller til projekt** i feltet **Antal ressourcer** skal du angive **1**.
8. I feltet **Ressource** viser opslaget alle ressourcer, der har de nødvendige kompetencer. Vælg **Daniel Goldschmidt**, og vælg derefter **Opret**.
9. Vælg **Tilføj** på siden **Projekt**.
10. I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Teammedlem**. Angiv **5** i feltet **Antal ressourcer**.
11. Vælg **Opret**.
12. På siden **Projekter** skal du vælge **Opfyld ressource**.

## <a name="monitor-project-teams"></a>Overvåg projektteam
1. På siden **Alle projekter** skal du vælge linket **Projekt-id** for projektet **XYZ-opgradering fase 2**.
2. På oversigtspanelet **Projektteam og planlægning** skal kontrollere, at projektets ressourcer er angivet korrekt.
