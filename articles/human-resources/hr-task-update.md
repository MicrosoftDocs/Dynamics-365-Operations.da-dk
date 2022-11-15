---
title: Konfigurere opgaver i Opgavestyring
description: I denne artikel beskrives det, hvordan du opretter opgaver i Opgavestyring i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745383"
---
# <a name="set-up-tasks-in-task-management"></a>Konfigurere opgaver i Opgavestyring

[!INCLUDE [PEAP](../includes/peap-1.md)]

I versioner af Microsoft Dynamics 365 Human Resources før version 10.0.30 skulle brugere, der ønskede at redigere en opgave, redigere opgaven enkeltvis på de enkelte tjeklister, der indeholdt den. Men fra og med Human Resources version 10.0.30 kan brugerne vælge, hvordan redigerede opgaver håndteres. Hvis en opgave, der redigeres, findes på en tjekliste, skal indstillingen **Aktivér opgradering af opgavestyring** være valgt under fanen **Opgavestyring** på siden **Delte parametre for personale** for at aktivere tjeklisten til brug af den redigerede opgave.

[![Indstillingen Aktivér opgradering af opgavestyring på siden Delte parametre for personale.](./media/task-update.png)](./media/task-update.png)

Hvis du redigerer opgaver, der skal anvendes til alle tilknyttede tjeklisteopgaver, skal der allerede findes en relation mellem opgaven i opgavebiblioteket og opgaven på tjeklisten. Der er tilføjet en indstilling for at oprette relationen mellem biblioteksopgaven og tjeklisteopgaven.

Du kan oprette opgaver enkeltvist og derefter genbruge dem på flere tjeklister. Hvis du vil oprette en opgave, skal du vælge **Ny** under fanen **Opgaver** på siden **Opsætning af onboarding**.

## <a name="set-up-tasks"></a>Konfigurere opgaver

Du kan tildele en oprettet opgave til flere tjeklister ved at vælge opgaven og derefter vælge **Anvend på kontrollister** i menuen.

Du kan også føje opgaver direkte til tjeklisten. Hvis du vil føje en opgave til en tjekliste, skal du enten oprette en ny tjekliste, som opgaven skal føjes til, på siden **Opsætning af onboarding** under fanen **Tjekliste** eller føje opgaven til en eksisterende tjekliste.

Hvis du vil redigere en opgave i biblioteket, skal du vælge **Rediger** i menuen Opgavebibliotek. Hvis opgaven er knyttet til nogen tjeklister, vises disse tjeklister på siden **Rediger opgave**. Hvis opgaverne i nogen af tjeklisterne skal opdateres med redigeringerne, skal du markere disse tjeklister i afsnittet **Anvend på kontrollister**.

Hvis du vil slette opgaver fra opgavebiblioteket, skal du vælge **Slet**. Hvis en opgave er tilknyttet en tjekliste, slettes opgaven ikke fra tjeklisten. Der kræves en separat handling for at fjerne en opgave fra en tjekliste.

### <a name="set-up-checklists"></a>Konfigurere tjeklister

En tjekliste er en gruppe opgaver. Du kan oprette lige så mange tjeklister, du har brug for, og du kan tildele de samme opgaver til flere tjeklister. Når du opretter en tjekliste, skal du angive en ejer og en kalender.

Hvis du vil oprette en ny opgave på en tjekliste, skal du vælge **Ny** på menulinjen Opgave. Når du opretter en ny opgave, kan du vælge at føje opgaven til opgavebiblioteket, så den kan deles på tværs af flere tjeklister. Du kan kun føje opgaven til opgavebiblioteket, hvis indstillingen **Anvend opgave på biblioteket** er angivet til **Ja**. Hvis du føjer opgaven til opgavebiblioteket, kan du også føje opgaven til andre tjeklister samtidig ved at vælge disse tjeklister i afsnittet **Anvend på kontrollister**. Hvis du vælger ikke at føje opgaven til opgavebiblioteket, findes den kun på den tjekliste, hvor du opretter den.

Hvis du vil redigere en opgave på en tjekliste, skal du vælge **Rediger** i menuen Opgave. Hvis opgaven er knyttet til nogen tjeklister, vises disse tjeklister på siden **Rediger opgave**. Hvis opgaverne i nogen af de andre tjeklister skal opdateres med redigeringerne, skal du markere disse tjeklister i afsnittet **Anvend på kontrollister**.

Hvis du vil fjerne opgaver fra tjeklisten, skal du vælge **Fjern**. Denne handling fjerner opgaverne fra tjeklisten. De slettes ikke fra opgavebiblioteket. Hvis du vil slette opgaver fra biblioteket, skal du åbne **Opgavebibliotek** og vælge **Slet**.
