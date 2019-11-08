---
title: Integration med Microsoft Project-klienten
description: Planlægning og vedligeholdelse af en projektplan kan være kompleks, så projektledere skal bruge værktøjer, som kan hjælper dem med at administrere denne opgave. Integration med Microsoft Project-klienten giver understøttelse til at åbne og styre et arbejdsopgavehierarki for projektet.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174792"
---
# <a name="microsoft-project-client-integration"></a>Integration med Microsoft Project-klienten

[!include [banner](../includes/banner.md)]

Planlægning og vedligeholdelse af en projektplan kan være kompleks, så projektledere skal bruge værktøjer, som kan hjælper dem med at administrere denne opgave. Integration med Microsoft Project-klienten giver understøttelse til at åbne og styre et arbejdsopgavehierarki for projektet. Projektlederen kan publicere eventuelle ændringer tilbage til arbejdsopgavehierarkiet i Dynamics 365 Finance-projektet.

> [!NOTE]
> Hvis du bruger opdateringen fra juli (version 10.0.4), skal du installere KB 4054797 og KB 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurere tilføjelsesprogrammet til Microsoft Project-klient
Hvis du vil aktivere integrationen med Microsoft Project-klienten, skal et tilføjelsesprogram til Microsoft Dynamics 365 skal installeres i brugerens klientprogram Microsoft Project. Dette gøres ved at åbne **Arbejdsområdet til projektstyring**.

• Klik på **Konfigurer tilføjelsesprogram til Project-klient** fra sektionen **Links** > **Konfiguration** af arbejdsområdet.

• Klik på **Åbn**, og klik derefter på **Kør**, når du bliver bedt om det.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Åbne og redigere en eksisterende kladde til arbejdsopgavehierarki i Microsoft Project-klienten
Hvis et projekt i Dynamics 365 Finance allerede har et arbejdsopgavehierarki, der er oprettet, kan arbejdsopgavehierarkiet åbnes i programmet Microsoft Project Client, hvis arbejdsopgavehierarkiet er i kladdestatus. Du åbner fra siden **Project** ved at klikke på linket **Åbne i Microsoft Project** under fanen **Plan**. Denne side kan også åbnes fra Microsoft Project-klientprogrammet ved at klikke på **Åbn** under fanen **Microsoft Dynamics 365**. Vælg **Juridisk enhed** og **Projekt** på listen.

> [!NOTE]
> Hvis du bruger Internet Explorer som browser, skal du klikke på **Gem** for manuelt at åbne fra den placering, filen er overført til. Eller klik på **Gem og åbn** for at åbne filen i Microsoft Project-klienten. Omdøb ikke filnavnet, når du gemmer.

Før du redigerer filen med Microsoft Project Client, skal du tjekke den ud. Klik på **Check ud** under fanen **Microsoft Dynamics 365**. Dette forhindrer andre brugere i samtidig at redigere arbejdsopgavehierarkiet inde fra Finance. For at udgive arbejdsopgavehierarkiet, når du har fuldført alle redigeringer, skal du klikke på **Check ind** under fanen **Microsoft Dynamics 365**.

Hvis et projektteam allerede er føjet til projektet i Finance, udfyldes ressourcelisten med teammedlemmerne. Hvis et projektteam endnu ikke er føjet til projektet, kan du vælge ressourcer og opbygge teamet i Microsoft Project-klienten ved at klikke på knappen **Ressourcer** under fanen **Microsoft Dynamics 365**. 

Følgende data synkroniseres tilbage til Finance som en del af check-in-processen:

•   Arbejdsrutinenavn

•   Startdato

•   Slutdato

•   Forgængere

•   Ressourcenavne

•   Kategori

•   Ressourcekategori

•   Arbejdstimer

•   Notater

•   Prioritet

> [!NOTE]
> Hvis du føjer andre kolonner til din Microsoft Project-klientfil, bliver de ikke gemt i filen og vises ikke, når filen åbnes igen.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Oprette arbejdsopgavehierarki til et eksisterende projekt ved hjælp af Microsoft Project-klient
Du opretter et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project-klient ved at følge disse trin:


1.  Åbn Microsoft Project-klient.

2.  Under fanen **Microsoft Dynamics 365** skal du klikke på **Åbn**.

3.  Vælg **Juridisk enhed** for projektet.

4.  Vælg **Projekt**.

5.  Klik på **Check ud** under fanen **Microsoft Dynamics 365**.

6.  Når du er klar til at udgive til Finance, skal du klikke på **Check ind** under fanen **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstat det eksisterende arbejdsopgavehierarki for et eksisterende projekt ved hjælp af Microsoft Project-klient
Hvis du vil oprette en ny arbejdsopgavehierarki ved hjælp af Microsoft Project-klienten og erstatte en eksisterende arbejdsopgavehierarki for et eksisterende projekt, skal du følge disse trin:

1.  Åbn Microsoft Project-klienten.

2.  Opret tidsplanen i Microsoft Project-klienten.

3.  Under fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Erstat eksisterende projekt**.

4.  Vælg **Juridisk enhed** for projektet.

5.  Vælg **Projekt**.

6.  Klik på **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Opret et nyt projekt fra Microsoft Project-klienten


1.  Åbn Microsoft Project-klienten.

2.  Opret tidsplanen i Microsoft Project-klienten.

3.  Under fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Gem i nyt projekt**.

4.  Vælg **Juridisk enhed** for projektet.

5.  Angiv **Projekt-id'et** om nødvendigt.

6.  Angiv **Projektnavn**.

7.  Vælg **Projekttype**, **Projektgruppe** og **Projektkontrakt-id**. Du kan også oprette en ny projektkontrakt ved at klikke på **Ny**.

8.  Vælg den **kalender** der skal bruges til fremskaffelse af ressourcer.

11. Klik på **OK**.