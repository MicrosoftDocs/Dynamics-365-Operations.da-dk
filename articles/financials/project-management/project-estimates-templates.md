---
title: Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556546"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere.
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflow for Project Service Automation til Finance and Operations

Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om projekttimeestimater og projektudgiftsestimater fra Project Service Automation til Finance and Operations.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekttimeestimater

### <a name="template-and-tasks"></a>Skabelon og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere projekttimeestimater fra Project Service Automation med Finance and Operations:

- **Navn på skabelonen i dataintegration:** Projekttimeestimater (PSA til Fin and Ops)
- **Navnet på opgaverne i projektet:**

    - Transaktionsrelationer
    - Udgiftsestimater

### <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Projektopgaver              | Integrationsenhed for projekttimeestimater |

### <a name="entity-flow"></a>Enhedsflow

Projekttimeestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projekttimebudgetter.

### <a name="prerequisites"></a>Forudsætninger

Før der kan foretages synkronisering af projekttimeestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.

### <a name="power-query"></a>Power-forespørgsel

I skabelonen til projekttimeestimater skal du bruge Microsoft Power-forespørgsel til Excel til at udføre disse opgaver:

- Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.
- Frafiltrer eventuelle ressourcespecifikke poster i opgaven, som vil få integrationen med timebudgetter til at mislykkes.
- Frafiltrere tomme posteringskategorirækker. Hvis denne opgave ikke kan fuldføres, kan det resultere i forkerte timebudgetter.

#### <a name="set-the-default-forecast-model-id"></a>Angiv standardbudgetmodel-id'et.

Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen. Vælg derefter linket **Avanceret forespørgsel og filtrering**.

- Hvis du bruger standardskabelonen Projekttimeestimater (PSA til Fin and Ops), skal du vælge **Indsat betingelse** på listen over **Anvendte trin**. I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen. Standardskabelonen har et budgetmodel-id fra demodataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**. Angiv betingelsen for kolonne, hvor hvis Projektopgave ikke er null, så \<enter the forecast model ID\>; else null.

#### <a name="filter-out-resource-specific-records"></a>Frafiltrere ressourcespecifikke poster

Skabelonen Projekttimeestimater (PSA til Fin and Ops) indeholder et standardfilter, der fjerner eventuelle ressourcespecifikke poster. Hvis du opretter din egen skabelon, skal du tilføje dette filter. Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere på kolonnen **msdyn\_islinetask**, så kun **falske** poster medtages.

#### <a name="filter-out-empty-transaction-category-rows"></a>Frafiltrere tomme posteringskategorirækker

Du skal tilføje et filter for at fjerne rækker, der har tomme posteringskategorier. Denne opgave er påkrævet, uanset om du bruger standardskabelonen eller opretter din egen skabelon. Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, der kan forårsage, at timebudgetterne i Finance and Operations bliver forkerte. Vælg linket **Avanceret forespørgsel og filtrering** for at frafiltrere null-poster i kolonnen **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektudgiftsestimater

### <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgaver bruges til at synkronisere projektudgiftsestimater fra Project Service Automation med Finance and Operations:

- **Navn på skabelonen i dataintegration:** Projektudgiftsestimater (PSA til Fin and Ops)
- **Navnet på opgaverne i projektet:**

    - Transaktionsrelationer 
    - Udgiftsestimater

### <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Transaktionsforbindelser    | Integrationsenhed for relationer for projekttransaktion |
| Estimatlinjer             | Integrationsenhed for projektudgiftsestimater         |

### <a name="entity-flow"></a>Enhedsflow

Projektudgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektudgiftsbudgetter.

### <a name="prerequisites"></a>Forudsætninger

Før der kan foretages synkronisering af projektudgiftsestimater, skal du synkronisere projekter, projektopgaver og transaktionskategorier for projektudgifter.

### <a name="power-query"></a>Power-forespørgsel

I skabelonen til projektudgiftsestimater skal du skal bruge Power-forespørgsel til at udføre følgende opgaver:

- Filtrere for kun at medtage linjeposter med udgiftsestimater.
- Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.
- Transformere faktureringstyperne.
- Transformere transaktionstyperne.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrere for kun at medtage udgiftsestimatlinjer

Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) har et standardfilter, der kun medtager udgiftslinjer i integrationen. Hvis du opretter din egen skabelon, skal du tilføje dette filter. Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering**. Filtrer på kolonnen **msdyn\_transactiontype1** for kun at medtage **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Angiv standardbudgetmodel-id'et.

Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering**.

- Hvis du bruger standardskabelonen Projektudgiftsestimater (PSA til Fin and Ops), skal du i Power-forespørgsel først vælge **Indsat betingelse** i sektionen **Anvendte trin**. I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen. Standardskabelonen har et budgetmodel-id fra demodataene.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne. I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**. Angiv betingelsen for den kolonne, hvor hvis Estimatlinje-id ikke er null, så \<enter the forecast model ID\>; else null.

#### <a name="transform-the-billing-types"></a>Transformere faktureringstyperne

Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen. Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**. Angiv et navn til den nye kolonne, f.eks. **BillingType**. Angiv derefter følgende betingelse:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformere transaktionstyperne

Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen. Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne. Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**. Angiv et navn til den nye kolonne, f.eks. **TransactionType**. Angiv derefter følgende betingelse:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Tilknytning af skabelon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
