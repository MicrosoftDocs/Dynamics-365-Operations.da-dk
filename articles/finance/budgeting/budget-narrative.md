---
title: Fortælling om budgetplan
description: Dette emne forklarer, hvordan en beskrivelse og en omsætningsoversigt medtages i en budgetplan.
author: v-kiarnd
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 85fde8289fc22ededa429b1a93117074d66955c2e8767990930bcc4efffd98ee
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772865"
---
# <a name="budget-plan-narrative"></a>Fortælling om budgetplan

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Når du planlægger at publicere budgetbøger eller -dokumenter, kan det nogle gange være nødvendigt at medtage en beskrivelse og/eller en omsætningsoversigt i en budgetplan. Disse oplysninger kan omfatte en beskrivelse af budgetplanen eller en liste over forudsætninger, performance-målinger, omsætningsoplysninger eller foreslåede ændringer af ydelser, der har resulteret i beløbene på bestemte budgetlinjer. Denne funktion giver dig mulighed for at bruge en HTML-editor til at styre budgetplanlægninger for at dokumentere de overvejelser, der har været under oprettelsen af planen.

Du kan bruge kontrolelementet til at skrive nyt indhold, eller du kan indsætte indhold, der er skrevet og formateret i en anden teksteditor, f.eks. Microsoft Word. I dokumentationsområdet kan du også ændre skrifttyper og tekstformatering. Yderligere funktioner, herunder stavekontrol, kan aktiveres.
 
Det indhold, der føjes til disse to sektioner, kan udskrives separat i en dokumentationsrapport for budgetplanen.
 
## <a name="setting-up-the-budget-plan-narrative"></a>Konfigurere dokumentationen for budgetplanen

Gennemfør følgende trin for at aktivere dokumentationsområdet for budgetplanen, og brug den nyeste HTML-editor, der er tilgængelig i produktet.
1.  Aktivér **Dokumentation for budgetplan** under funktionsstyring. Du kan også aktivere det **Nye HTML-editorkontrolelement** i arbejdsområdet til **funktionsstyring**, så der bruges en mere aktuel editor.
2.  Vælg en budgetplan i **modulet Budgetplanlægning**. 
3.  Vælg **Overskrift** for at åbne visningen **Overskrift** og aktivere adgang til sektionen **Fortælling om budgetplan**. Felterne i dette afsnit er normalt ikke synlige i **Linje**-visningen.
4.  Udvid sektionen **Dokumentation for budgetplan**, og tilføj beskrivelser eller omsætningsoplysninger, der skal medtages i budgetplanen.

Der kræves ingen ekstra tilladelser for at ændre fortællingen for budgetplanen.

## <a name="include-budget-plan-narrative-fields-when-you-copy-budget-plans"></a>Medtage fortællingsfelter i budgetplan, når du kopierer budgetplaner

Følg disse trin for at aktivere budgetplanens fortællingsbeskrivelse og indtægtsoversigten, der skal kopieres til nye budgetplaner.

1. Sørg for, at handlingen **Fortælling om budgetplan** er aktiveret i funktionsstyring som beskrevet i forrige afsnit.
2. I funktionsstyring skal du aktivere funktionen **Medtag budgetplansfortælling, når du kopierer budgetplaner**. Denne funktion tilføjer en **Fortælling om budgetplan**-sektion og to flag, der bruges til kopiering af budgetplan: **Medtag budgetbeskrivelse** og **Medtag omsætningsoversigt**.
3. Du kan angive nye flag fra følgende sider:

    - **Budgetplaner:**

        1. Gå til **Budgettering \> Budgetplaner**.
        2. Vælg den budgetplan, der skal kopieres.
        3. Vælg **Kopi af** i gruppen **Ny** under fanen **Budgetplan** i handlingsruden.

        Dialogboksen **Kopiér en budgetplan**, der vises, indeholder de nye flag.

    - **Opret budgetplan fra en budgetplan:**

        - Gå til **Budgettering \> Periodisk \> Opret budgetplan fra en budgetplan**.

        Siden indeholder de nye flag. Flagene er dog kun tilgængelige, når **Handling**-feltet er angivet til **Opret en ny budgetplan**.

4. Vælg de fortællingsfelter, der skal kopieres til den nye plan. Du kan udføre dette trin enten fra siden **Budgetplaner** eller fra siden **Opret budgetplan fra en budgetplan**.

Når budgetplanen er blevet kopieret, kopieres de valgte fortællingsfelter for budgetplaner til den nye plan.
