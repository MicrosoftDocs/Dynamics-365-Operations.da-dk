---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923019"
---
# <a name="financial-reporting-faq"></a>Ofte stillede spørgsmål vedrørende Økonomirapportering 

Dette emne indeholder svar på ofte stillede spørgsmål om økonomirapportering. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?

I følgende eksempel vises, hvordan du kan begrænse adgangen til en rapport ved hjælp af sikkerhedstræet.

USMF-demofirmaet har en finansbalancerapport, som ikke alle brugere af økonomirapportering bør have adgang til. Til at begrænse adgangen kan du bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun bestemte brugere kan få adgang til rapporten. Benyt følgende fremgangsmåde for at begrænse adgangen: 

1. Log på Financial Reporter Report Designer.
2. Opret en ny trædefinition. Gå til **Fil > Ny > Trædefinition**.
3. Dobbeltklik på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.
4. Vælg **Brugere og Grupper**.  
5. Vælg de brugere eller grupper, som har behov for at have adgang til denne rapport. 
6. Vælg **Gem**.
7. Tilføj den nye trædefinition i rapportdefinitionen.
8. Vælg **Indstilling** i trædefinitionen. Vælg **Medtag alle enheder** under **Valg af rapporteringsenhed**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Hvordan identificerer jeg, hvilke konti der ikke svarer til mine saldi?

Når du har en rapport, der ikke har tilsvarende saldi, kan du gøre følgende for at identificere hver af kontiene og afvigelserne. 

**Financial Reporter Report Designer**
1. I Financial Reporter Report Designer skal du oprette en ny rækkedefinition. 
2. Vælg **Rediger > Indsæt rækker fra dimensioner**.
3. Vælg **MainAccount**.  
4. Vælg **OK**.
5. Gem rækkedefinitionen.
6. Opret en ny kolonnedefinition
7. Opret en ny rapportdefinition.
8. Vælg **Indstillinger**, og fjern markering af denne indstilling.  
9. Opret rapporten. 
10. Eksporter rapporten til Microsoft Excel.

**Dynamics 365 Finance** 
1. I Dynamics 365 Finance skal du gå til **Finans > Forespørgsler og rapporter > Råbalance**.
2. Angiv følgende parametre:
   - **Fra dato** – Angiv starten af regnskabsåret.
   - **Til dato** – Angiv den dato, rapporten skal genereres for.
   - **Økonomisk dimension** – Angiv dette felt til **Hovedkontosæt**.
 3. Vælg **Beregn**.
 4. Eksporter rapporten til Microsoft Excel.

Du skal nu kunne kopiere data fra Excel-rapporten i økonomirapport til rapporten Råbalance, så du kan sammenligne kolonnerne med **Ultimosaldo**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]