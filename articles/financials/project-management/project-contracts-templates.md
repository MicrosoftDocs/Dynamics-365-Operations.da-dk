---
title: Synkronisere projektkontrakter og projekter direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561456"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere projektkontrakter og projekter direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, skal du installere KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflow for Project Service Automation til Finance and Operations

> [!NOTE]
> Før du kan bruge løsningen til integration af Project Service Automation med Finance and Operations, skal du være fortrolig med Microsoft Dynamics 365-dataintegrationsfunktionen.

Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonen, der er tilgængelig med dataintegrationsfunktionen, muliggør strømmen af data om projektkontrakter, projekter, projektkontraktlinjer og milepæle i projektkontraktlinje fra Project Service Automation til Finance and Operations.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere projektkontrakter og projekter fra Project Service Automation med Finance and Operations:

- **Navn på skabelonen i dataintegration:** Projekter og kontrakter (PSA til Fin and Ops)
- **Navnet på opgaverne i projektet:**

    - Projektkontrakter PSA til Fin and Ops
    - Projekter PSA til Fin and Ops
    - Projektkontraktlinjer PSA til Fin and Ops
    - Milepæle i projektkontraktlinjer PSA til Fin and Ops

Før der kan foretages synkronisering af projektkontrakter og projekter, skal du synkronisere konti.

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Bestillinger                           | Integrationsenhed for projektkontrakt                |
| Projekter                         | Integrationsenhed for projekt                         |
| Ordrelinjer                      | Integrationsenhed for projektkontraktlinje           |
| Milepæle i projektkontraktlinje | Integrationsenhed for milepæl i projektkontraktlinje |

## <a name="entity-flow"></a>Enhedsflow

Projektkontrakter administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektkontrakter. Som en del af integrationsskabelonen, kan du indstille integrationskilden i Finance and Operations for projektkontrakten.

Tid og materiale-projekter og faste prisprojekter administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projekter. Som en del af skabelonintegrationen, kan du indstille integrationskilden i Finance and Operations for projektet.

Projektkontraktlinjer administreres i Project Service Automation, og de synkroniseres med Finance and Operations som faktureringsregler for projektkontrakter. Hvis faktureringsmetoden er forskellig fra standardtypen for projektet, opdaterer synkroniseringen projekttypen for kontraktlinjeprojektet og projektgruppen,.

Milepæle i projektkontraktlinjer administreres i Project Service Automation, og de synkroniseres med Finance and Operations som milepæle i faktureringsregler for projektkontrakter.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Løsning til integration af Project Service Automation med Finance and Operations

Feltet **Projektkontrakt-ID** er tilgængeligt på siden **Projektkontrakter**. Feltet er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.

Når en ny projektkontrakt oprettes, og der ikke allerede findes en værdi for **Projektkontrakt-id**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **ORD** efterfulgt af en trinvist stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ORD-01022-Z4M9Q0**.

Feltet **Projektnummer** er tilgængeligt på siden **Projekter**. Feltet er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.

Når et nyt projekt oprettes, og der ikke allerede findes en værdi for et **Projektnummer**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **PRJ** efterfulgt af en trinvist stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **PRJ-01049-CCNID0**.

Når Project Service Automation til Finance and Operations-integrationsløsning anvendes<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, indstiller et opgraderingsscript feltet **Projektkontrakt-ID** for eksisterende projektkontrakter og feltet **Projektnummer** for eksisterende projekter i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

- Før der kan foretages synkronisering af projektkontrakter og projekter, skal du synkronisere konti.
- I dit forbindelsessæt skal du tilføje en felttilknytning for integrationsnøglen for **msdyn\_organizationalunits** til **msdyn\_name \[Navn\]**. Du skal evt. først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- I dit forbindelsessæt skal du tilføje en felttilknytning for integrationsnøglen for **msdyn\_projects** til **msdynce\_projectnumber \[Projektnummer\]**. Du skal evt. først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- **SourceDataID** for projektkontrakter og projekter kan opdateres til en anden værdi eller fjernes fra tilknytningen. Skabelonens standardværdi er **Project Service Automation**.
- **PaymentTerms**-tilknytningen skal opdateres, så den afspejler gyldige betalingsbetingelserne i Finance and Operations. Du kan også fjerne tilknytningen fra projektopgaven. Standardværdikortet har standardværdier for demodata. Følgende tabel viser værdierne i Project Service Automation.

    | Værdi | Betegnelse   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | 2% 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis følgende betingelser er opfyldt:

- Du har salgsordrer i Microsoft Dynamics 365 for Sales.
- Du har flere organisationsenheder i Project Service Automation, og disse organisationsenheder knyttes til flere juridiske enheder i Finance and Operations.

Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:

- Skabelonen Projekter og kontrakter (PSA til Fin and Ops) har et standardfilter, der kun indeholder salgsordrer af typen **Workflowopgave (msdyn\_ordertype = 192350001)**. Dette filter hjælper med til at sikre, at der ikke oprettes projektkontrakter for salgsordrer i Finance and Operations. Hvis du opretter din egen skabelon, skal du tilføje dette filter.
- Du skal oprette et Power-forespørgselsfiltret, der kun indeholder de kontraktorganisationer, der skal synkroniseres til den juridiske enhed for integrationsforbindelsessættet. For eksempel skal projektkontrakter, du har med kontraktorganisationsenheden i Contoso USA, synkroniseres med den juridiske enhed for USSI, mens projektkontrakter, du har med kontraktorganisationsenheden i Contoso Global, synkroniseres med den juridiske enhed for USMF. Hvis du ikke føjer dette filter til din opgavetilknytning, synkroniseres alle projektkontrakter med den juridiske enhed, der er defineret for forbindelsessættet, uanset kontraktorganisationsenheden.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE] 
> Felterne **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** og **AddressZipCode** medtages ikke i standardtilknytningen for projektkontrakter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres for projektkontrakter.
>
> Felterne **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** og **ProjectType** medtages ikke i standardtilknytningen for projekter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres for projekter.

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
