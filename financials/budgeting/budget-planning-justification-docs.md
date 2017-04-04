---
title: "Budget planlægning berettigelsesdokumenter"
description: "Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget til at forklare, hvorfor det er nødvendigt med et specifikt budget."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budget planlægning berettigelsesdokumenter

Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget til at forklare, hvorfor det er nødvendigt med et specifikt budget. 

En budgetplansskabelon er oprettet af budgetadministrator i Microsoft Word og knyttet til den aktuelle proces i budgetplanlægningen. Ejere af budgettet kan derefter åbne skabelonen og har data, der udfyldes automatisk i Word, der er baseret på deres budgetanmodning. De kan derefter tilføje yderligere tekst eller data, før lagring og tilknytning af deres personlige berettigelsesdokumentet til deres budgetplan.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Konfigurere Microsoft Dynamics Office-tilføjelsesprogrammet til Microsoft Word

1.  Åbn et nyt dokument i Microsoft Word.
2.  Klik på **Indsæt** på båndet, og klik **Store**.
3.  Søg efter Microsoft Dynamics Office-tilføjelsesprogrammet og klik på **Tilføj**.
4.  I Word, i højre rude, klik på **Tilføj oplysninger om**.
5.  Skriv eller Indsæt Webadressen til-serveren, og klik på **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definer den begrundelse skabelon i Microsoft Word

1.  Klik på **Design** i Microsoft Dynamics-kontor i når du har logget.
2.  Headeroplysninger, bruge den **Tilføj felter** knap.
3.  Vælg datakilden enhed til BudgetPlanJustification, og klik på **næste**. **Bemærk:** dette objekt er påkrævet for alle berettigelsesdokumentet. Andre enheder kan bruges, men overførslen tilbage til Microsoft Dynamics 365 for handlinger mislykkes, hvis dette objekt medtages ikke.
4.  Tilføje BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber-etiketter og værdier i Word-dokumentet. **Bemærk:** du kan bruge dine egne etiketter, i stedet for de standardetiketter, hvis det er nødvendigt.
5.  Klik på **gjort** til at fuldføre hovedsektionen.
6.  Linje niveau detaljer for budgetbeløb plan, ved at klikke på **Tilføj tabel**.
7.  Igen, Vælg datakilden enhed til BudgetPlanJustification, og klik på **næste**.
8.  Tilføje felter til EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount. **Bemærk:** hvis kommentarer kan tilføjes i individuelle budgetplanlinjer, der kan føjes til tabellen her.
9.  Tilføj eventuelle yderligere anvisninger til at levere til slutbrugeren, og udføre nødvendige formatering eller typografier i dokumentet.
10. Gemme dokumentet på din lokale computer og lukke filen, før du fortsætter.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Konfigurere budgetplanlægningsprocessen til at bruge skabelonen begrundelse

1.  Gå til Microsoft Dynamics 365 for operationer, **budgettering**&gt;**Setup**&gt;**budgetplanlægning**&gt;**begrundelse dokumentskabeloner**.
2.  Klik på **ny**, og gå til det nyoprettede Microsoft Word-dokument.
3.  Angiv en skabelonnavn og beskrivelse. Click **OK**.
4.  Gå til **budgettering**&gt;**Setup**&gt;**Budget****planlægning**&gt;**Budget planlægningen af**.
5.  Vælg den proces, hvor skabelonen begrundelse skal bruges, og klik på **Rediger**.
6.  I den **begrundelse dokumentskabelon**, Marker den relevante skabelon, og Gem.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redigere og gemme personlige berettigelsesdokumenter

1.  Oprette en ny budgetplan i Dynamics 365 for operationer, eller Åbn en eksisterende budgetplan.
2.  I den **begrundelse** i rullemenuen, Vælg **Opret ny begrundelse**.
3.  Efter at have udfyldt i detaljer, vælge for at overføre den personlige dokument fra den **begrundelse** i rullemenuen.



