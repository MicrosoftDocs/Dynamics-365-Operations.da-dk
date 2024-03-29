---
title: Oversigt over oprettelse af arbejdsgange
description: Denne artikel beskriver, hvordan du opretter en arbejdsgang.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "195583"
- intro-internal
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 1343061ba06d13e68a98b05c013867af0a4d07a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864480"
---
# <a name="create-workflows-overview"></a>Oversigt over oprettelse af arbejdsgange

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikel beskriver, hvordan du opretter en arbejdsgang.

## <a name="open-the-workflow-editor"></a>Åbne arbejdsgangseditoren

De typer arbejdsgange, du kan oprette, afhænger af hvilket modul, du arbejder i. Udfør følgende trin for at vælge den type arbejdsgang, der skal oprettes, og for at åbne arbejdsgangseditoren.

1. Åbn det modul, som du vil oprette en ny arbejdsgang for. For eksempel hvis du vil oprette en arbejdsgang for indkøbsrekvisitioner, skal du klikke på **Indkøb og forsyning**.
2. Klik på **Konfigurer** &gt; **\[Arbejdsgange\] for modulnavn**.
3. Klik på **Ny** i handlingsruden på listesiden.
4. På siden **Opret arbejdsgang** skal du vælge typen af arbejdsgang, du vil oprette, og derefter klikke på **Opret arbejdsgang**. Arbejdsgangseditoren vises. Brug nu følgende procedurer til at designe arbejdsgangen.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Trække arbejdsgangselementer over på lærredet

Området **Arbejdsgangselementer** i arbejdsgangseditoren indeholder de elementer, du kan føje til arbejdsgangen. Du kan tilføje elementer i arbejdsgangen ved at trække dem til lærredet.

## <a name="connect-the-elements"></a>Forbinde elementerne

Du kan forbinde et arbejdsgangselement med et andet ved at holde markøren over elementet, indtil der vises forbindelsespunkter. Klik på et forbindelsespunkt, og træk det til et andet element. Kontrollér, at alle elementerne forbindes.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurere arbejdsgangens egenskaber

Følg nedenstående trin for at konfigurere egenskaberne for arbejdsgangen.

1. Klik på lærredet for at sikre, at der ikke er markeret noget arbejdsgangselement.
2. Klik på **Egenskaber** for at åbne siden **Egenskaber** for arbejdsgangen.
3. Følg procedurerne i artiklen [Konfigurer egenskaberne for arbejdsgange](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurere arbejdsgangselementer

Konfigurer hvert af de elementer, du har trukket over på lærredet. Du kan finde flere oplysninger om konfiguration af hvert enkelt arbejdsgangselement i følgende emner.

- [Konfigurere manuelle opgave i en arbejdsgang](configure-manual-task-workflow.md)
- [Konfigurere automatiserede opgaver i en arbejdsgang](configure-automated-task-workflow.md)
- [Konfigurere godkendelsesprocesser i en arbejdsgang](configure-approval-process-workflow.md)
- [Konfigurere godkendelsestrin i en arbejdsgang](configure-approval-step-workflow.md)
- [Konfigurere manuelle beslutninger i en arbejdsgang](configure-manual-decision-workflow.md)
- [Konfigurere betingede beslutninger i en arbejdsgang](configure-conditional-decision-workflow.md)
- [Konfigurere parallelle grene i en arbejdsgang](configure-parallel-activity-workflow.md)
- [Konfigurere en parallel gren](configure-parallel-branch-workflow.md)
- [Konfigurere arbejdsgange for linjeelementer](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Rette fejl eller afhjælpe advarsler

I ruden **Fejl og advarsler** nederst i arbejdsgangseditoren vises meddelelser, der er genereret i forbindelse med arbejdsgangen. Du kan finde det element, hvor der er opstået en fejl eller advarsel, ved at dobbeltklikke på fejl- eller advarselsmeddelelsen. Alle fejl skal rettes og advarsler afhjælpes, før du kan aktivere arbejdsgangen.

## <a name="save-and-activate-the-workflow"></a>Gemme og aktivere arbejdsgangen

Udfør følgende trin, når du er klar til at gemme og aktivere arbejdsgangen.

1. Klik på **Gem og luk** for at lukke arbejdsgangseditoren og for at åbne siden **Gem arbejdsgang**.
2. Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen, og klik derefter på **OK**.
3. Hvis alle fejl og advarsler er løst, vises siden **Aktivér arbejdsgang**. Vælg en af følgende indstillinger:

    - Hvis du vil aktivere denne version af arbejdsgangen, skal du klikke på **Aktivér den nye version**. Når en arbejdsgang er aktiv, kan brugerne sende dokumenter til behandling og godkendelse i arbejdsgangen.
    - Hvis du ikke vil aktivere denne version, skal du klikke på **Aktivér ikke den nye version**. Du kan aktivere arbejdsgangen senere.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]