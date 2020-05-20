---
title: Oprette budgetmodeller for projektbudgetter
description: I dette emne beskrives, hvordan du opretter en budgetmodel for resterende budgetter.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321773"
---
# <a name="create-forecast-models-for-project-budgets"></a>Oprette budgetmodeller for projektbudgetter 

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du opretter en budgetmodel for resterende budgetter. I et projekt, der er underlagt budgetstyring, bruges to typer af budgetter: oprindeligt og resterende. Når du opretter et projektbudget, skal du angive de budgetmodeller for det oprindelige og det resterende budget, der er oprettet på siden **Budgetmodeller**. Der oprettes projektbudgetter på basis af de angivne modeller, når du gør projektbudgettet bindende.

> [!NOTE]
> En budgetmodel, der bruges til budgetstyring, kan ikke have en undermodel eller bruges som undermodel.

1. Vælg **Projektstyring og regnskab** > **Konfiguration** > **Budgetter**  > **Budgetmodeller**.
2. Vælg **Ny** for at oprette en ny budgetmodel, og angiv derefter et id-nummer på den nye model og et navn til den. 
3. Angiv indstillingen **Stoppet** til **Ja** for at forhindre ændringer af budgetlinjer i budgetmodellen. 
4. Hvis du vil generere likviditetsbudgetter i finans med de budgetlinjer, som er tilknyttet modellen, skal du angive **Medtage budgetter i likviditetsbudgetter** til **Ja**. 
5. Hvis du vil bruge projektdatoen som fakturadatoen, skal du angive **Budgetfakturadato** til **Ja**. 
6. Vælg en af følgende modeltyper i feltet **Budgettype**:

   - **Oprindeligt budget**: Brug denne modeltype til de oprindelige budgetbeløb, der bliver bindende, når det indledende budget er oprettet og godkendt.
   - **Resterende budget**: Brug denne modeltype til de resterende budgetbeløb, så længe projektet løber. Saldiene i denne budgetmodel reduceres med faktiske posteringer og forøges eller formindskes med budgetrevisioner.
   - **Overførsel**: Brug det overførte budgetbeløb for projektet. Overførsel er en valgfri proces, der kan bruges til at overføre ikke-anvendte budgetbeløb fra ét regnskabsår til et andet.

7. Angiv følgende indstillinger efter behov:

   - Aktivér **Budgetfakturadato** for at bruge projektdatoen som fakturadatoen.
   - Aktivér **Budget med IGVA** for at foretage budgettering baseret på igangværende forarbejdning (IGVF), og vælg derefter IGVA-typen. 
   - Du kan beholde den standardbaserede **Budgettype** som **Ingen** eller angive en ny type. Budgettypen kan ikke ændres, når du har ændret en post.     
    > [!NOTE]
    > Hvis du ændrer standardbudgettypen, er alle andre indstillinger ikke tilgængelige for opdateringer, og du kan ikke genbruge denne budgetmodel. 
   


 

