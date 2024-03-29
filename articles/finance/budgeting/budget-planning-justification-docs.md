---
title: Berettigelsesdokumenter til budgetplanlægning
description: Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget, som kan forklare, hvorfor det er nødvendigt med et specifikt budget.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711765"
---
# <a name="budget-planning-justification-documents"></a>Berettigelsesdokumenter til budgetplanlægning

[!include [banner](../includes/banner.md)]

Berettigelsesdokumenter giver en fortælling for dem, der anmoder om et budget, som kan forklare, hvorfor det er nødvendigt med et specifikt budget. 

En budgetplansskabelon oprettes af budgetadministratoren i Microsoft Word og knyttes til den aktuelle proces i budgetplanlægningen. Ejere af budgettet kan derefter åbne skabelonen og automatisk få udfyldt felter i Word med data baseret på deres budgetanmodning. De kan derefter tilføje yderligere tekst eller data, før deres personlige berettigelsesdokument gemmes og knyttes til deres budgetplan.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Opsætning af Microsoft Dynamics-tilføjelsesprogram til Microsoft Word

1.  Åbn et nyt Microsoft Word-dokument.
2.  Klik på **Indsæt** på båndet, og klik på **Gem**.
3.  Søg efter Microsoft Dynamics Office-tilføjelsesprogrammet, og klik på **Tilføj**.
4.  I Word, i højre rude, skal du klikke på **Tilføj serveroplysninger**.
5.  Skriv eller indsæt webadressen til serveren, og klik på **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definere berettigelsesskabelonen i Microsoft Word

1.  Klik på **Design** i Microsoft Dynamics Office-tilføjelsesprogrammet, når du har logget.
2.  Til headeroplysninger skal du bruge knappen **Tilføj felter**.
3.  Vælg BudgetPlanJustification for enhedsdatakilden, og klik på **Næste**. **Bemærk:** Denne enhed er påkrævet for alle berettigelsesdokumenter. Andre enheder kan bruges, men uploaden tilbage til Microsoft Dynamics 365 Finance mislykkes, hvis denne enhed ikke medtages.
4.  Tilføj BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber-etiketter og værdier i Word-dokumentet. **Bemærk:** Du kan bruge dine egne etiketter i stedet for standardetiketterne, hvis det er nødvendigt.
5.  Klik på **Udført** for at fuldføre headersektionen.
6.  Du kan angive detaljer for budgetplanbeløb på linjeniveau ved at klikke på **Tilføj tabel**.
7.  Vælg igen BudgetPlanJustification som datakilde for enheden, og klik på **Næste**.
8.  Tilføj felter for EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount. **Bemærk:** Hvis der kan tilføjes kommentarer i individuelle budgetplanlinjer, kan de føjes til tabellen her.
9.  Tilføj eventuelle yderligere anvisninger til slutbrugeren, og udfør evt. formatering eller lignende ændringer i dokumentet.
10. Gem dokumentet på din lokale computer, og luk filen, før du fortsætter.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Konfigurere budgetplanlægningsprocessen til at bruge berettigelsesskabelonen

1.  Gå til **Budgettering** &gt; **Opsætning** &gt; **Budgetplanlægning** &gt; **Skabeloner for berettigelsesdokumenter**.
2.  Klik på **Ny**, og gå til det nyoprettede Microsoft Word-dokument.
3.  Angiv et visningsnavn og en beskrivelse til skabelonen. Klik på **OK**.
4.  Gå til **Budgettering** &gt; **Opsætning** &gt; **Budget** **planlægning** &gt; **Budgetplanlægningsproces**.
5.  Vælg den proces, hvor berettigelsesskabelonen skal bruges, og klik på **Rediger**.
6.  Vælg den relevante skabelon i feltet **Skabelon for berettigelsesdokument**, og Gem.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redigere og gemme personligt tilpassede berettigelsesdokumenter

1.  Opret en ny budgetplan, eller åbn en eksisterende budgetplan.
2.  Vælg **Opret ny berettigelse** i rullemenuen **Berettigelse**.
3.  Når du har angivet detaljerne, skal du vælge at overføre det personligt tilpassede dokument fra **Berettigelse**-rullemenuen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
