---
title: Oprette vedligeholdelsesbudgetter
description: Denne artikel forklarer, hvordan du opretter et vedligeholdelsesbudget i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858034"
---
# <a name="create-maintenance-budgets"></a>Oprette vedligeholdelsesbudgetter

[!include [banner](../../includes/banner.md)]

 



Vedligeholdelsesbudgetter bruges til at give en oversigt over forventede omkostninger ved forebyggende vedligeholdelse. Budgetlinjer beregnes på basis af linjer i vedligeholdelsestidsplanen, der har en forventet startdato i budgetperioden.

Vedligeholdelsesbudgetter er baseret på de omkostningstyper, der bruges i aktivstyring: **Præventiv**, **Korrigerende** og **Investering**. Budgetomkostninger for investeringsvedligeholdelse medtages for aktive aktiver, der har en erstatningsdato i løbet af budgetperioden og en relateret erstatningsværdi. Budgetomkostninger for korrigerende vedligeholdelse medtages, hvis en tidligere korrektionsdato er inkluderet i budgetberegningen. I dette tilfælde beregnes korrigerende omkostninger fra en tidligere periode for den samme fremtidige periode, som du beregner vedligeholdelsesbudgettet for.

## <a name="create-a-maintenance-budget"></a>Oprette et vedligeholdelsesbudget

1. Vælg **Styring af aktiver** \> **Forespørgsler** \> **Vedligeholdelsesbudget** \> **Budget**.
2. Vælg **Opret budget**.
3. I feltet **Vedligeholdelsesbudget** skal du indtaste et budget-id.
4. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Angiv start- og slutdatoerne for budgetperioden i felterne **Fra-dato** og **Til-dato** i oversigtspanelet **Periode**.
5. Hvis du vil medtage korrigerende budgetomkostninger, der beregnes på grundlag af faktiske omkostninger fra en tidligere periode, skal du angive startdatoen for den periode, som disse omkostninger skal medtages fra, i feltet **Korrigerende fra-dato**.
6. Afhængigt af det detaljeringsniveau, der kræves i budgettet, skal du angive de relevante indstillinger i de fem oversigtspaneler **Gruppér efter**.
7. Vælg **OK**.
8. Vælg **Budgetlinjer** for at åbne siden **Vedligeholdelsesbudgetlinjer**, hvor du kan få vist alle de budgetlinjer, der er oprettet for perioden.
9. Hvis du vil godkende budgettet, skal du vælge det på siden **Vedligeholdelsesbudgetter** og derefter vælge **Godkend**. Vælg derefter **OK** i dialogboksen **Godkend budget**. Dit navn angives i feltet **Godkendt af** på siden **Vedligeholdelse budgetter**.

    > [!NOTE]
    > Når du har godkendt et vedligeholdelsesbudget, kan du ikke genberegne eller regulere de relaterede linjer på siden **Vedligeholdelsesbudgetlinjer**, medmindre du først har fjernet godkendelsen. Hvis du vil fjerne godkendelsen af et vedligeholdelsesbudget, skal du vælge det på siden **Vedligeholdelsesbudgetter** og derefter vælge **Godkend**. Vælg derefter **OK** i dialogboksen **Godkend budget**.

![Vedligeholdelsesbudgetter.](media/01-maintenance-budgets.png)

Du kan også oprette et nyt vedligeholdelsesbudget ved at kopiere et eksisterende budget. Vælg det budget, du vil kopiere, på siden **Vedligeholdelsesbudgetter**, og vælg derefter **Kopiér**. Denne fremgangsmåde er nyttig, hvis du f.eks. har oprettet et budget for én måned og vil kopiere det til andre måneder.

> [!NOTE]
> Vedligeholdelsesbudgettet beregner kun budgetomkostninger baseret på vedligeholdelsestidsplanslinjer. Hvis du vil beregne faktiske omkostninger for den samme periode, kan du udføre denne beregning på siden **Omkostningsstyring for aktiv**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]