---
title: Opret et nyt projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter et nyt projekt.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760503"
---
# <a name="create-a-new-project"></a>Opret et nyt projekt

[!include [banner](../includes/banner.md)]

Udfør følgende trin for at oprette et nyt projekt.

1. På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:

    - **Projekttype:** Tid og materialer
    - **Projektnavn:** XYZ-opgradering fase 2
    - **Projektgruppe:** TM\_WIP
    - **Projektkontrakt-id:** 00000002

2. Vælg **Opret projekt**.

## <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1. På siden **Arbejdere** på listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere har konfigureret kompetencer for, og åbne arbejderposten.
2. Vælg **Tildel projekter** i gruppen **Konfiguration** under fanen **Projekt** i handlingsruden.
3. På siden **Ressourcevalidering af projekttildelinger** under fanen **Projekter** skal du i feltet **Føj projektet til udvalgte projekter** filtrere på projektet **XYZ-opgradering fase 2**.
4. I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at føje det til ruden **Valgte projekter**.

Du kan også tildele kategorier til en ressource, hvis det er nødvendigt. Kategoritypen er enten **Omkostning** eller **Indtægter**. Kategoritypen bestemmes af din organisation. Hvis en ressource ikke er tildelt nogen kategorier, leder Finance efter standardkategorien på timepriser for omkostninger og indtægter.

## <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere projektressource- og rollekarakteristika

En projektleder kan bruge projektressourcefunktionaliteten til at oprette de roller, der er nødvendige for projektet. Roller kan bruges, hvis bekræftede ressourcer stadig er ukendte, når ressourcer reserveres. Roller kan midlertidigt reserveres som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev ansat til at udføre et tids- og materialeprojekt, der har et godkendt projektcharter. Juniorprojektlederen er stadig ved at færdiggøre omfanget af projektet. Ressourcestyringen identificerer i øjeblikket bestemte ressourcer, der skal reserveres til arbejde på det nye projekt. På grund af projektets kritiske natur har projektsponsoren anmodet om, at en af rollerne er seniorprojektleder. Ressourcechefen skal anskaffe den nye ressource og definere rollen i systemet i tilfælde af, at juniorprojektlederen kræver ressourceoplysninger under projektplanlægningen.

Følgende fremgangsmåde viser, hvordan ressourcechefen kan konfigurere seniorprojektlederrollen og knytte ressourceegenskaber til den. Rollen kan senere bruges til at søge efter tilgængelige ressourcer, der svarer til de krævede ressourcekompetencer.

1. På siden **Konfigurer roller** skal du vælge **Ny** og angive følgende værdier:

    - **Rolle-id:** Seniorprojektleder
    - **Beskrivelse:** Seniorprojektleder

2. Vælg **Opret**.
3. Vælg rollen **Seniorprojektleder**, og vælg derefter **Konfigurer egenskaber**.
4. Vælg **Færdighed** i feltet **Karakteristikatype**.
5. I feltet **Tilgængelige karakteristika** skal du angive den færdighed, du søger efter.
6. I **Karakteristikatype** feltet skal du vælge **Certifikat**.
7. I feltet **Tilgængelige karakteristika** skal du angive den certifikattype, du søger efter.

## <a name="assign-a-project-resource-to-a-project"></a>Tildele en projektressource til et projekt

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.
2. Under fanen **Projektteam og planlægning** skal vælge **Tilføj**.
3. I feltet **Rolle** skal du vælge **Teammedlem**.
4. Vælg **Reservér fra kalender**.
5. På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.
6. På siden **Juster visningsindstillinger** skal du angive følgende værdier:

    - **Viser format for datoområde:** Dag
    - **Vis beskrivelser af tilgængelighed:** Ja
    - **Vis resterende kapacitet:** Ja

7. Vælg en ressource på listen over ressourcer.
8. Vælg **Definitiv reservation** og **Fuld kapacitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Tildele en ressource til en standardrolle

Som en hjælp kan projektledere eller ressourcechefer rulle længere ned i de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyligt erhvervet ressource. Da Daniel f.eks. blev ansat, havde han erfaring og kompetence til at udfylde rollen Forretningsanalytiker. Ressourcechefen tildelte denne rolle som Daniels standardrolle. Derfor tilføjede ressourcechefen Daniel til en pulje af forretningsanalytikere, der er tilgængelige til at arbejde på projekter.

Under ressourcereservationen kan projektledere filtrere de ressourceroller, der er tilgængelige for arbejde på projekter. De kan bruge disse oplysninger som et kriterium, når de foretager beslutningsanalyse med flere kriterier under ressourceopfyldelsen. De kan også føje andre ressourcekarakteristika til filteret for at søge efter ressourcer, som har særlige kvalifikationer, uddannelse og erfaringer med et givent projekt.

**Scenarie:** Et godkendt projekt er startet, og rollen som seniorprojektleder blev reserveret som en planlagt ressource i løbet af projektets planlægningsstadie. Ressourcestyringen har nu fået en ressource, der skal opfylde rollen som seniorprojektleder.

1. Vælg **Daniel Goldschmidt** på siden **Liste over ressourcer**.
2. På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:

    - **Gyldig fra:** Angiv den aktuelle dato.
    - **Udløb:** Angiv **Aldrig**.
    - **Rolle:** Angiv **Seniorprojektleder**.

3. Vælg **Gem**, og luk derefter siden.
4. Under fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og **PMP**-certifikatet.
