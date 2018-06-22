---
title: Synkronisere projektestimater fra Project Service Automation direkte til projektbudgetter i Finance and Operations
description: I dette emne beskrives skabelonerne og de underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Synkronisere projektestimater fra Project Service Automation direkte til projektbudgetter i Finance and Operations

I dette emne beskrives skabelonerne og de underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflow for Project Service Automation til Finance and Operations

Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om projekttimeestimater og projektudgiftsestimater fra Project Service Automation til Finance and Operations.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere projekttimeestimater fra Project Service Automation med Finance and Operations:

-  **Navn på skabelonen i dataintegration:** Projekttimeestimater (PSA til Fin and Ops)

-  **Navnet på opgaverne i projektet:** 
    - Transaktionsrelationer 
    - Udgiftsestimater

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projektopgaver                   | Integrationsenhed for projekttimeestimater   |

## <a name="entity-flow"></a>Enhedsflow

Projekttimeestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projekttimebudgetter.

## <a name="preconditions"></a>Betingelser

Før der kan foretages synkronisering af projekttimeestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel i skabelonen til projekttimeestimater til at:
- Angiv det **Budgetmodel-id**, der skal bruges, når integrationen opretter nye timebudgetter.
- Frafiltrere eventuelle ressourcespecifikke poster i opgaven, som vil få integrationen med timebudgetter til at mislykkes
- Frafiltrere tomme posteringskategorirækker. Hvis dette ikke gøres, kan det resultere i forkerte timebudgetter.

### <a name="forecast-model-id"></a>Budgetmodel-id
Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen. Vælg for at åbne avanceret forespørgsel og filtrering.
- Hvis du bruger standardskabelonen for Microsoft Project-timebudgetter (PSA til Fin and Ops), skal du vælge **Indsat betingelse** i sektionen **Anvendte trin**. I **Funktion**-posten skal du erstatte **O_forecast** med navnet på det **Budgetmodel-id**, der skal bruges sammen med integrationen. Standardskabelonen har et budgetmodel-id fra demodataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. Vælg **Tilføj betinget kolonne**, og giv kolonnen et navn, f.eks. ModelID. Angiv betingelsen for kolonnen, hvor hvis Projektopgave ikke er null, så<enter the forecast model ID>; else null.

### <a name="filter-out-resource-specific-records"></a>Frafiltrere ressourcespecifikke poster
Skabelonen til projekttimeestimater (PSA til Fin and Ops) indeholder et standardfilter, der fjerner eventuelle ressourcespecifikke poster. Hvis du opretter din egen skabelon, skal du tilføje dette filter. I formularen Avanceret forespørgsel og filtrering skal du vælge at filtrere på kolonnen **msdyn_islinetask** for kun at medtage **falske** poster.

### <a name="filter-out-empty-transaction-category-rows"></a>Frafiltrere tomme posteringskategorirækker
Du skal tilføje et filter for at fjerne rækker med tomme posteringskategorier. Det er nødvendigt, uanset om du bruger standardskabelonen eller opretter din egen skabelon. Dette filter fjerner eventuelle oversigtsrækker, der kommer fra Project Service Automation, der kan forårsage, at timebudgetterne i Finance and Operations bliver forkerte. Vælg i formularen Avanceret forespørgsel og filtrering for at frafiltrere de null-poster i kolonnen **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftsestimater fra Project Service Automation med Finance and Operations:

-  **Navn på skabelonen i dataintegration:** Projektudgiftsestimater (PSA til Fin and Ops)
-  **Navnet på opgaverne i projektet:** 
     - Transaktionsrelationer 
     - Udgiftsestimater

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Transaktionsforbindelser         | Integrationsenhed for relationer for projekttransaktion.   |
| Estimatlinjer                  | Integrationsenhed for projektudgiftsestimater.           |

## <a name="entity-flow"></a>Enhedsflow

Projektudgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektudgiftsbudgetter.

## <a name="prerequisites"></a>Forudsætninger

Før der kan foretages synkronisering af projektudgiftsestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel i skabelonen til projektudgiftsestimater til at:
- Filtrere for kun at medtage linjeposter med udgiftsestimater
- Angiv det **Budgetmodel-id**, der skal bruges, når integrationen opretter nye timebudgetter.
- Transformere faktureringstyperne.
- Transformere transaktionstyperne.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrere for kun at medtage udgiftsestimatlinjer
Skabelonen til projektudgiftsestimater (PSA til Fin and Ops) har et standardfilter, der kun medtager udgiftslinjer i integrationen. Hvis du opretter din egen skabelon, skal du tilføje dette filter. Vælg transaktionsrelationsopgaven, og klik på **Tilknyt**-pilen. Vælg **Avanceret forespørgsel og filtrering**. Filtrer på kolonnen **msdyn_transactiontype1** for kun at medtage **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Budgetmodel-id
Du kan opdatere standardbudgetmodel-id'et i skabelonen for opgaven Udgiftsestimater ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen. Vælg for at åbne avanceret forespørgsel og filtrering.
- Hvis du bruger standardskabelonen for Microsoft Project-udgiftsestimater (PSA til Fin and Ops), skal du først vælge **Indsat betingelse** i sektionen **Anvendte trin**. I **Funktion**-posten skal du erstatte **O_forecast** med navnet på det **Budgetmodel-id**, der skal bruges sammen med integrationen. Standardskabelonen har et budgetmodel-id fra demodataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. Vælg **Tilføj betinget kolonne**, og giv kolonnen et navn, f.eks. ModelID. Angiv betingelsen for den kolonne, hvor hvis Estimatlinje-id ikke er null, så < enter the forecast model ID >; else null.

### <a name="transform-the-billing-types"></a>Transformere faktureringstyperne
Skabelonen til projektudgiftsestimater (PSA til Fin and Ops) har en betinget kolonne, der er til føjet for at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen.
- Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg **Tilføj betinget kolonne** i formularen Avanceret forespørgsel og filtrering. Giv kolonnen et navn, f.eks. "BillingType". Angiv betingelsen på følgende måde:

    If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**

### <a name="transform-the-transaction-types"></a>Transformere transaktionstyperne
Skabelonen til projektudgiftsestimater (PSA til Fin and Ops) har en betinget kolonne, der er til føjet for at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen.
- Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg **Tilføj betinget kolonne** i formularen Avanceret forespørgsel og filtrering. Giv kolonnen et navn, f.eks. "TransactionType". Betingelsen angives som følger: If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Tilknytning af skabelon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




