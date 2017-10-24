---
title: Oprette en arbejdsgang
description: Dette emner beskriver, hvordan du opretter en arbejdsgang.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4d57e47fe7f38a43ecfdfbdd701d7e6a7d7800d6
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-workflow"></a>Oprette en arbejdsgang

[!include[banner](../includes/banner.md)]


Dette emner beskriver, hvordan du opretter en arbejdsgang.

<a name="open-the-workflow-editor"></a>Åbne arbejdsgangseditoren
------------------------

Det Microsoft Dynamics 365 for Finance and Operations-modul, du arbejder i, bestemmer typerne af arbejdsgange, du kan oprette. Udfør følgende trin for at vælge den type arbejdsgang, der skal oprettes, og for at åbne arbejdsgangseditoren.

1.  Åbn det modul, som du vil oprette en ny arbejdsgang for. For eksempel hvis du vil oprette en arbejdsgang for indkøbsrekvisitioner, skal du klikke på **Indkøb og forsyning**.
2.  Klik på **Konfigurer** &gt; **\[Arbejdsgange\] for modulnavn**.
3.  Klik på **Ny** i handlingsruden på listesiden.
4.  På siden **Opret arbejdsgang** skal du vælge typen af arbejdsgang, du vil oprette, og derefter klikke på **Opret arbejdsgang**. Arbejdsgangseditoren vises. Brug nu følgende procedurer til at designe arbejdsgangen.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Trække arbejdsgangselementer over på lærredet
Området **Arbejdsgangselementer** i arbejdsgangseditoren indeholder de elementer, du kan føje til arbejdsgangen. Du kan tilføje elementer i arbejdsgangen ved at trække dem til lærredet.

## <a name="connect-the-elements"></a>Forbinde elementerne
Du kan forbinde et arbejdsgangselement med et andet ved at holde markøren over elementet, indtil der vises forbindelsespunkter. Klik på et forbindelsespunkt, og træk det til et andet element. Kontrollér, at alle elementerne forbindes.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurere arbejdsgangens egenskaber
Følg nedenstående trin for at konfigurere egenskaberne for arbejdsgangen.

1.  Klik på lærredet for at sikre, at der ikke er markeret noget arbejdsgangselement.
2.  Klik på **Egenskaber** for at åbne siden **Egenskaber** for arbejdsgangen.
3.  Følg procedurerne i emnet [Konfigurere egenskaberne for en arbejdsgang](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurere arbejdsgangselementer
Konfigurer hvert af de elementer, du har trukket over på lærredet. Du kan finde flere oplysninger om konfiguration af hvert enkelt arbejdsgangselement i følgende emner.

-   [Konfigurere en manuel opgave](configure-manual-task-workflow.md)
-   [Konfigurere en automatiseret opgave](configure-automated-task-workflow.md)
-   [Konfigurere en godkendelsesproces](configure-approval-process-workflow.md)
-   [Konfigurere et godkendelsestrin](configure-approval-step-workflow.md)
-   [Konfigurere en manuel beslutning](configure-manual-decision-workflow.md)
-   [Konfigurere en betinget beslutning](configure-conditional-decision-workflow.md)
-   [Konfigurere en parallel aktivitet](configure-parallel-activity-workflow.md)
-   [Konfigurere en parallel gren](configure-parallel-branch-workflow.md)
-   [Konfigurere en arbejdsgang for linjeelement](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Rette fejl eller afhjælpe advarsler
I ruden **Fejl og advarsler** nederst i arbejdsgangseditoren vises meddelelser, der er genereret i forbindelse med arbejdsgangen. Du kan finde det element, hvor der er opstået en fejl eller advarsel, ved at dobbeltklikke på fejl- eller advarselsmeddelelsen. Alle fejl skal rettes og advarsler afhjælpes, før du kan aktivere arbejdsgangen.

## <a name="save-and-activate-the-workflow"></a>Gemme og aktivere arbejdsgangen
Udfør følgende trin, når du er klar til at gemme og aktivere arbejdsgangen.

1.  Klik på **Gem og luk** for at lukke arbejdsgangseditoren og for at åbne siden **Gem arbejdsgang**.
2.  Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen, og klik derefter på **OK**.
3.  Hvis alle fejl og advarsler er løst, vises siden **Aktivér arbejdsgang**. Vælg en af følgende indstillinger:
    -   Hvis du vil aktivere denne version af arbejdsgangen, skal du klikke på **Aktivér den nye version**. Når en arbejdsgang er aktiv, kan brugerne sende dokumenter til behandling og godkendelse i arbejdsgangen.
    -   Hvis du ikke vil aktivere denne version, skal du klikke på **Aktivér ikke den nye version**. Du kan aktivere arbejdsgangen senere.






