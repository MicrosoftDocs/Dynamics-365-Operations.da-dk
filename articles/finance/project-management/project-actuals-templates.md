---
title: Synkronisere faktiske projektoplysninger direkte fra Project Service Automation med projektintegrationskladden til bogføring i Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Microsoft Dynamics 365 Project Service Automation til Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770329"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronisere faktiske projektoplysninger direkte fra Project Service Automation med projektintegrationskladden til bogføring i Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

Skabelonen synkroniserer transaktioner fra Project Service Automation med en midlertidig tabel i Finance. Når synkroniseringen er fuldført, **skal** du importere dataene fra den midlertidige tabel til integrationskladden.

> [!NOTE]
> - Integration af faktiske projektoplysninger er tilgængelige fra og med version 8.0.1.
> - Hvis du bruger Enterprise edition 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.
> - Hvis du bruger version 7.3.0, og du bringer gebyrtransaktioner fra Project Service Automation, skal du installere KB 4345320 for at medtage disse gebyrer i projektfakturaen.
> - Hvis du indtaster momsbeløb på tids- eller udgiftsposteringer i Project Service Automation, skal du installere Project Service Automation opdatering 7. Ellers bliver de faktiske momsoplysninger ikke knyttet til de faktiske tids- eller udgiftsoplysninger, der er tilknyttet, og de bliver ikke synkroniseret med Finance. Kontakt Support for at få flere oplysninger.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektoplysninger fra Project Service Automation til Finance.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Faktiske projektoplysninger fra Project Service Automation

### <a name="template-and-tasks"></a>Skabelon og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft Power Apps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere faktiske projektoplysninger fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Faktiske projektoplysninger (PSA til Fin and Ops)
- **Navnet på opgaverne i projektet:**

    - Faktiske oplysninger
    - TransactionConnections

### <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finans                                   |
|----------------------------|----------------------------------------------------------|
| Faktiske oplysninger                    | Integrationsenhed for projektets faktiske tal                   |
| Transaktionsforbindelser    | Integrationsenhed for relationer for projekttransaktion |

### <a name="entity-flow"></a>Enhedsflow

Faktiske projektoplysninger administreres i Project Service Automation, og de synkroniseres med projektintegrationskladden i Finance. Regnskaber anvendes baseret på økonomiske standarddimensioner og konteringsopsætningen.

### <a name="prerequisites"></a>Forudsætninger

Før synkroniseringen af faktiske oplysninger kan udføres, skal du konfigurere integrationsparametrene i Project Service Automation og synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.

### <a name="power-query"></a>Power-forespørgsel

I skabelonen til faktiske projektoplysninger skal du bruge Microsoft Power-forespørgsel til Excel til at udføre disse opgaver:

- Omdanne transaktionstypen i Project Service Automation til den korrekte transaktionstype i Finance. Denne transformation er allerede defineret i skabelonen Faktiske projektoplysninger (PSA til Fin and Ops).
- Omdanne faktureringstypen i Project Service Automation til den korrekte faktureringstype i Finance. Denne transformation er allerede defineret i skabelonen Faktiske projektoplysninger (PSA til Fin and Ops). Faktureringstypen knyttes derefter til linjeegenskaben baseret på konfigurationen på siden **Project Service Automation-integrationsparametre**.
- Filtrere til specifikke ressourceorganisationsenheder, der skal synkroniseres med denne skabelon.
- Hvis faktiske oplysninger om intern tid eller interne udgifter skal synkroniseres med Finance, skal du konvertere kontraktorganisationsenheden til den korrekte juridiske enhed i Finance. I skabelonen Faktiske projektoplysninger (PSA til Fin and Ops) er der defineret en betinget kolonne baseret på demodata. Du skal opdatere den sidste indsatte betingelseskolonne til de korrekte juridiske enheder. Ellers kan det medføre enten en integrationsfejl, eller at forkerte faktiske transaktioner importeres til Finance.
- Hvis faktiske oplysninger om intern tid eller interne udgifter ikke synkroniseres med Finance, skal du slette den sidste indsatte betingelseskolonne fra skabelonen. Ellers kan det medføre enten en integrationsfejl, eller at forkerte faktiske transaktioner importeres til Finance.

#### <a name="contract-organizational-unit"></a>Kontraktorganisationsenhed
Du kan opdatere den indsatte betingelseskolonne i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen. Vælg linket **Avanceret forespørgsel og filtrering** for at åbne Power-forespørgslen.

- Hvis du bruger standardskabelonen Faktiske projektoplysninger (PSA til Fin and Ops) i Power-forespørgslen, skal du vælge den sidste **indsatte betingelse** i sektionen **Anvendte trin**. I posten **Funktion** skal du erstatte **USSI** med navnet på den juridiske enhed, der skal bruges sammen med integrationen. Tilføj yderligere betingelser efter behov til posten **Funktion**, og opdater **else**-betingelsen fra **USMF** til den korrekte juridiske enhed.
- Hvis du opretter en ny skabelon, skal du tilføje kolonnen for at understøtte intern tid og interne udgifter. Vælg **Tilføj betinget kolonne**, og giv kolonnen et navn, f.eks. **LegalEntity**. Angiv en betingelse for kolonnen, hvor, hvis **msdyn\_contractorganizationalunitid.msdyn\_name** er \<organizational unit\>, så \<enter the legal entity\>; ellers null.

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustrationer viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af skabelon](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Tilknytning af skabelon](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importere fra den midlertidige tabel efter integration af Project Service Automation

Importen fra den midlertidige tabels periodiske proces skal køres efter synkroniseringen af faktiske oplysninger fra Project Service Automation til Finance. Denne proces importerer projektposteringerne fra den midlertidige tabel til Project Service Automation-integrationskladden, hvor regnskaberne anvendes, og de importerede transaktioner kan bogføres. Vi anbefaler, at du kører denne proces i batchtilstand og eventuelt konfigurerer den til at køre som en tilbagevendende batch.

## <a name="update-actuals-from-finance"></a>Opdatere faktiske oplysninger fra Finance

### <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere bilagsnummer og moms for bogførte projekttransaktioner fra Finance til Project Service Automation:

- **Navnet på skabelonen i dataintegration:** Opdatering af faktiske projektoplysninger (Fin and Ops til PSA)
- **Navnet på opgaverne i projektet:**

    - Faktiske oplysninger 
    - TransactionConnections

### <a name="entity-set"></a>Enhedssæt

| Finans                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrationsenhed for projektets faktiske tal                   | Faktiske oplysninger                    |
| Integrationsenhed for relationer for projekttransaktion | Transaktionsforbindelser    |

### <a name="entity-flow"></a>Enhedsflow

Faktiske projektoplysninger administreres i Project Service Automation, og de synkroniseres med projektintegrationskladden i Finance. Når de faktiske oplysninger er bogført i Finance, opdateres de i Project Service Automation med bilagsnummeret fra Finance. Hvis moms blev tilføjet i Finance, oprettes nye faktiske momsoplysninger i Project Service Automation.

### <a name="power-query"></a>Power-forespørgsel

I skabelonen Opdatering af faktiske projektoplysninger skal du bruge Power-forespørgsel til at udføre disse opgaver:

- Omdanne transaktionstypen i Finance til den korrekte transaktionstype i Project Service Automation. Denne transformation er allerede defineret i skabelonen Opdatering af faktiske projektoplysninger (Fin and Ops til PSA).
- Omdanne faktureringstypen i Finance til den korrekte faktureringstype i Project Service Automation. Denne transformation er allerede defineret i skabelonen Opdatering af faktiske projektoplysninger (Fin and Ops til PSA).

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser de feltoplysninger, der synkroniseres fra Finance til Project Service Automation.

[![Tilknytning af skabelon](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Tilknytning af skabelon](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
