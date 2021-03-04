---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070211"
---
# <a name="financial-reporting-faq"></a>Ofte stillede spørgsmål vedrørende Økonomirapportering 

Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?

Scenario: USMF-demofirmaet har en finansbalancerapport, som ikke ønsker, at alle brugere af økonomirapportering skal kunne se i D365. Løsning: Du kan bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun bestemte brugere kan få adgang til rapporten. 

1.  Log på Rapportdesigner til økonomirapporter

2.  Opret en ny trædiagramdefinition (Fil | Ny | Trædiagramdefinition) a.    Dobbeltklik på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.
  i.    Klik på Brugere og Grupper.  
          1. Vælg de brugere eller grupper, som skal have adgang til denne rapport. 
          
[![brugerskærm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![sikkerhedsskærm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klik på **Gem**.
  
[![knappen Gem](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Tilføj den nye trædiagramdefinition i rapportdefinitionen

[![trædiagramdefinition, formular](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  I trædiagramdefinitionen skal du klikke på Indstilling og under "Valg af rapporteringsenhed" og "Medtag alle enheder"

[![formular til valg af rapporteringsenhed](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Før:** [![før skærmbillede](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Efter:** [![efter skærmbillede](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Bemærk: Årsagen til ovenstående meddelelse er, at min bruger ikke har adgang til rapporten, efter at der har anvendt enhedssikkerhed



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Hvordan kan jeg bestemme, hvilke konti der ikke svarer til mine saldi i D365?

Når du har en rapport, der ikke svarer til det, du ville forvente i D365, kan du gøre følgende for at identificere disse konti og afvigelserne. 

### <a name="in-financial-reporter-report-designer"></a>I Rapportdesigner til økonomirapporter

1.  Opret en ny rækkedefinition a.    Klik på Rediger | Indsæt rækker fra dimensioner i.  Vælg MainAccount [![Vælg hovedkontoskærm](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Klik på Ok b.    Gem rækkedefinitionen

2.  Opret en ny kolonnedefinition     [![Opret en ny kolonnedefinition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Opret en ny rapportdefinition a.    Klik på Indstillinger, og fjern markeringen [![Indstillinger-formular](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Opret rapporten. 

5.  Eksporter rapporten til Excel.

### <a name="in-d365"></a>I D365: 
1.  Klik på Finans | Forespørgsler og rapporter | Råbalance a.    Parametre i.  Fra dato: Startdato for regnskabsåret ii. Til dato: Den dato, hvor du genererede rapporten til iii.    Økonomiske dimensionsopsætninger "Hovedkontoopsætninger" [![Hovedkontoformular](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Klik på Beregn

2.  Eksporter rapporten til Excel

Du skal nu kunne kopiere data fra FR Excel-rapporten til rapporten D365 Råbalance og sammenligne kolonnerne med "Ultimosaldo".
