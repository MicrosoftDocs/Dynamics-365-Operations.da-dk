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
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e3c86bd32a05a392fcb82a86f2c461cc3abfb03
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

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




