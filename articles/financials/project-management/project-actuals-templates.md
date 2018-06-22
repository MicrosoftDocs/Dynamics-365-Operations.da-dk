---
title: "Synkronisere faktiske projektoplysninger fra Project Service Automation direkte med projektintegrationskladden til bogføring i Finance and Operations"
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronisere faktiske projektoplysninger fra Project Service Automation direkte med projektintegrationskladden til bogføring i Finance and Operations

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere faktiske projektoplysninger direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.

Skabelonen synkroniserer transaktioner fra Project Service Automation med en midlertidig tabel i Finance and Operations. Når synkroniseringen er fuldført, skal du importere fra den midlertidige tabel til integrationskladden.

> [!NOTE]
> Integration af faktiske projektoplysninger er tilgængelig i Dynamics 365 for Finance and Operations version 8.01.

> [!NOTE]
> Hvis du indtaster momsbeløb på tids- eller udgiftsposteringer i Project Service Automation, skal du installere Project Service Automation opdatering 7. Hvis opdateringen ikke er installeret, bliver de faktiske momsoplysninger ikke knyttet til de faktiske tids- eller udgiftsoplysninger, der er tilknyttet, og synkroniseres ikke med Finance and Operations. Kontakt Support for at få flere oplysninger.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflow for Project Service Automation til Finance and Operations

Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektoplysninger fra Project Service Automation til Finance and Operations.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere faktiske projektoplysninger fra Project Service Automation til Finance and Operations:

-  **Navnet på skabelonen i dataintegration:** Faktiske projektoplysninger (PSA til Fin and Ops)

-  **Navnet på opgaverne i projektet:** 
    - Faktiske oplysninger 
    - TransactionConnections

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Faktiske oplysninger                         | Integrationsenhed for projektets faktiske tal                      |
| Transaktionsforbindelser         | Integrationsenhed for relationer for projekttransaktion    |

## <a name="entity-flow"></a>Enhedsflow

Faktiske projektoplysninger administreres i Project Service Automation, og de synkroniseres med projektintegrationskladden i Finance and Operations. Regnskaber anvendes baseret på økonomiske standarddimensioner og konteringsopsætningen.

## <a name="preconditions"></a>Betingelser

Før synkroniseringen af faktiske oplysninger kan udføres, skal du konfigurere integrationsparametrene i Project Service Automation og synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel i skabelonen til faktiske projektoplysninger til at:
- Omdanne **posteringstypen** i Project Service Automation til den korrekte **posteringstype** i Finance and Operations. Denne transformation er allerede defineret i skabelon til faktiske oplysninger (PSA til Fin and Ops).
- Omdanne **faktureringstypen** i Project Service Automation til den korrekte **faktureringstype** i Finance and Operations. Denne transformation er allerede defineret i skabelon til faktiske oplysninger (PSA til Fin and Ops). Faktureringstypen knyttes derefter til **linjeegenskaben** baseret på konfigurationen i formularen med integrationsparametre til Dynamics 365 for Project Service Automation.
- Filtrere til specifikke **Ressourceorganisationsenheder**, der skal synkroniseres med denne skabelon.
- Hvis **faktiske oplysninger om intern tid eller interne udgifter** skal synkroniseres med Finance and Operations, skal du konvertere **kontraktorganisationsenheden** til den korrekte **juridiske enhed** i Finance and Operations. Skabelonen til projektets faktiske oplysninger (PSA til Fin and Ops) har en betinget kolonne, der er defineret ud fra demodata. Du skal opdatere den sidste indsatte betingelseskolonne til de korrekte juridiske enheder. Hvis du ikke gør det, kan det medføre enten en integrationsfejl, eller at forkerte faktiske posteringer importeres til Finance and Operations.
- Hvis **faktiske oplysninger om intern tid eller interne udgifter** ikke synkroniseres med Finance and Operations, skal du slette den sidste indsatte betingelseskolonne fra skabelonen. Hvis du ikke gør det, kan det medføre enten en integrationsfejl, eller at forkerte faktiske posteringer importeres til Finance and Operations.

### <a name="contract-organizational-unit"></a>Kontaktorganisationsenhed
Du kan opdatere den indsatte betingelseskolonne i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen. Vælg for at åbne avanceret forespørgsel og filtrering.
- Hvis du bruger standardskabelonen for faktiske Microsoft Project-værdier (PSA til Fin and Ops), skal du vælge den sidste **indsatte betingelse** i sektionen **Anvendte trin**. I **Funktion**-posten skal du erstatte **USSI** med navnet på den **juridiske enhed**, der skal bruges sammen med integrationen. Tilføj yderligere betingelser efter behov for **Funktion**-posten, og opdater **else**-betingelsen fra **USMF** til den korrekte **juridiske enhed**.
- Hvis du opretter en ny skabelon, skal du tilføje denne kolonne for at understøtte intern tid og interne udgifter. Vælg **Tilføj betinget kolonne**, og giv kolonnen et navn, f.eks. LegalEntity. Angiv betingelsen for kolonnen, hvor hvis msdyn_contractorganizationalunitid.msdyn_name er <organizational unit>, så er <enter the Legal entity>; else null.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Tilknytning af skabelon](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Importér fra midlertidig tabel

Importen fra den midlertidige tabels periodiske proces skal køres efter synkroniseringen af faktiske oplysninger fra Project Service Automation til Finance and Operations. Denne proces importerer projektposteringerne fra den midlertidige tabel til Project Service Automation-integrationskladden, hvor regnskaberne anvendes, og de importerede transaktioner kan bogføres. Det anbefales, at du kører denne proces i batchtilstand og eventuelt konfigurerer den til at køre som en tilbagevendende batch.

## <a name="update-actuals"></a>Opdatere faktiske oplysninger

Følgende skabeloner og underliggende opgaver bruges til at synkronisere bilagsnummer og moms for bogførte projekttransaktioner fra Finance and Operations til Project Service Automation:

-  **Navnet på skabelonen i dataintegration:** Opdatering af faktiske projektoplysninger (Fin and Ops til PSA)
-  **Navnet på opgaverne i projektet:** 
     - Faktiske oplysninger 
     - TransactionConnections

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Integrationsenhed for projektets faktiske tal                         | Faktiske oplysninger                           |
| Integrationsenhed for relationer for projekttransaktion       | Transaktionsforbindelser           |

## <a name="entity-flow"></a>Enhedsflow

Faktiske projektoplysninger administreres i Project Service Automation, og de synkroniseres med projektintegrationskladden i Finance and Operations. Når de faktiske oplysninger er bogført i Finance and Operations, opdateres de i Project Service Automation med bilagsnummeret fra Finance and Operations. Hvis moms blev tilføjet i Finance and Operations, oprettes nye faktiske momsoplysninger i Project Service Automation.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel i opdateringsskabelonen med faktiske projektoplysninger til at:
- Omdanne **posteringstypen** i Finance and Operations til den korrekte **posteringstype** i Project Service Automation. Denne transformation er allerede defineret i opdateringsskabelonen med faktiske oplysninger (Fin and Ops til PSA).
- Omdanne **faktureringstypen** i Finance and Operations til den korrekte **faktureringstype** i Project Service Automation. Denne transformation er allerede defineret i opdateringsskabelonen med faktiske oplysninger (Fin and Ops til PSA).

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Finance and Operations til Project Service Automation.

[![Tilknytning af skabelon](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Tilknytning af skabelon](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




