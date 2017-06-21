---
title: Oprette et budget ud fra posteringskonti og totalkonti
description: "Denne artikel indeholder en oversigt over processen til at oprette budgetter baseret på totalkonti. Der beskrives også, hvordan du aktiverer budgetstyring for totalkonti, hvis budgetstyring er påkrævet."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 89ddb0f246eb1d874ff0f2b5305f30355905c45e
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Oprette et budget ud fra posteringskonti og totalkonti

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over processen til at oprette budgetter baseret på totalkonti. Der beskrives også, hvordan du aktiverer budgetstyring for totalkonti, hvis budgetstyring er påkrævet.

Både budgetplanen og dokumenter med budgetregisterposter giver mulighed for budgettering på hovedkonti, som har hovedkontotypen **Total**. Faktiske kan kun bogføres til hovedkonti med transaktioner. 

For den periodiske proces **Generér budgetplan fra finanskonto** under fanen **Kilde** kan du angive hovedkontotypen **Total** som et kriterium. I så fald medtages hver totalhovedkonto i målbudgetplanen, og beløbet vil være lig med det samlede beløb for intervallet af de markerede hovedkonti. 

Du kan aktivere budgetstyring for hovedkonti af typen **Total**. Denne funktionalitet understøttes ved hjælp af budgetgrupper. For hver totalhovedkonto skal det budget, der skal kontrolleres for en budgetgruppe, være oprettet på siden **Konfiguration af budgetstyring**. De kriterier, du angiver, skal omfatte totalhovedkontoen og intervallet af konti. For at fremskynde oprettelsen af budgetgrupper kan du udnytte fordelen ved budgetkontrolgruppernes dataenhed. 

Når et budget bruges til rapportering, f.eks. i et regnskab, består budgetsummen for totalkontoen af følgende beløb:

-   De budgetter, der er oprettet ud fra de enkelte posteringsfinanskonti i totalkontoens interval.
-   Det budgetbeløb, der direkte er angivet på totalkontoen.

Derfor kan du oprette separate budgetter for de væsentligste posteringskonti i totalkontoens interval og derefter føje det tilgængelige budgetbeløb til totalkontoen.




