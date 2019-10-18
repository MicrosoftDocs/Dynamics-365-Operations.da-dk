---
title: Synkronisere projektkontrakter og projekter direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250455"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere projektkontrakter og projekter direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE] 
> Hvis du bruger Enterprise Edition 7.3.0, skal du installere KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

> [!NOTE]
> Før du kan bruge løsningen til integration af Project Service Automation med Finance, skal du være fortrolig med Dynamics 365-dataintegrationsfunktionen.

Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance. Integrationsskabelonen, der er tilgængelig med dataintegrationsfunktionen, muliggør strømmen af data om projektkontrakter, projekter, projektkontraktlinjer og milepæle i projektkontraktlinje fra Project Service Automation til Finance.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.

[![Dataflow for Project Service Automation-integration med Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere projektkontrakter og projekter fra Project Service Automation til Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integration med Dynamics 365 Project Service Automation v2.x
- **Navn på skabelonen i dataintegration:** Projekter og kontrakter (PSA til Fin and Ops)
- **Navnet på opgaverne i projektet:**

    - Projektkontrakter PSA til Fin and Ops
    - Projekter PSA til Fin and Ops
    - Projektkontraktlinjer PSA til Fin and Ops
    - Milepæle i projektkontraktlinjer PSA til Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integration med Dynamics 365 Project Service Automation v3.x
Der er en skemaændring i Project Service Automation, der påvirker skabelonen til milepæl med projektkontraktlinjer, og brug af skabelonens v2-version skal bruges til at integrere Project service Automation v3.x med Dynamics 365.

- **Navn på skabelonen i dataintegration:** Projekter og kontrakter (PSA 3.x til Fin and Ops) - v2
- **Navnet på opgaverne i projektet:**

    - Projektkontrakter PSA til Fin and Ops
    - Projekter PSA til Fin and Ops
    - Projektkontraktlinjer PSA til Fin and Ops
    - Milepæle i projektkontraktlinjer PSA til Fin and Ops

Før der kan foretages synkronisering af projektkontrakter og projekter, skal du synkronisere konti.

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation       | Finans                                                |
|----------------------------------|--------------------------------------------------------|
| Bestillinger                           | Integrationsenhed for projektkontrakt                |
| Projekter                         | Integrationsenhed for projekt                         |
| Ordrelinjer                      | Integrationsenhed for projektkontraktlinje           |
| Milepæle i projektkontraktlinje | Integrationsenhed for milepæl i projektkontraktlinje |

## <a name="entity-flow"></a>Enhedsflow

Projektkontrakter administreres i Project Service Automation, og de synkroniseres med Finance som projektkontrakter. Som en del af integrationsskabelonen, kan du indstille integrationskilden i Finance for projektkontrakten.

Tid og materiale-projekter og faste prisprojekter administreres i Project Service Automation, og de synkroniseres med Finance som projekter. Som en del af skabelonintegrationen kan du indstille integrationskilden i Finance for projektet.

Projektkontraktlinjer administreres i Project Service Automation, og de synkroniseres med Finance som faktureringsregler for projektkontrakter. Hvis faktureringsmetoden er forskellig fra standardtypen for projektet, opdaterer synkroniseringen projekttypen for kontraktlinjeprojektet og projektgruppen,.

Milepæle i projektkontraktlinjer administreres i Project Service Automation, og de synkroniseres med Finance som milepæle i faktureringsregler for projektkontrakter.

## <a name="project-service-automation-to-finance-integration-solution"></a>Løsning til integration af Project Service Automation med Finance

Feltet **Projektkontrakt-ID** er tilgængeligt på siden **Projektkontrakter**. Feltet er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.

Når en ny projektkontrakt oprettes, og der ikke allerede findes en værdi for **Projektkontrakt-id**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **ORD** efterfulgt af en trinvist stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ORD-01022-Z4M9Q0**.

Feltet **Projektnummer** er tilgængeligt på siden **Projekter**. Feltet er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.

Når et nyt projekt oprettes, og der ikke allerede findes en værdi for et **Projektnummer**, oprettes den automatisk ved hjælp af en nummerserie. Værdien består af **PRJ** efterfulgt af en trinvist stigende nummerserie og et suffiks på seks tegn. Her er et eksempel: **PRJ-01049-CCNID0**.

Når Project Service Automation til Finance-integrationsløsning anvendes, indstiller et opgraderingsscript feltet **Projektkontrakt-id** for eksisterende projektkontrakter og feltet **Projektnummer** for eksisterende projekter i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

- Før der kan foretages synkronisering af projektkontrakter og projekter, skal du synkronisere konti.
- I dit forbindelsessæt skal du tilføje en felttilknytning for integrationsnøglen for **msdyn\_organizationalunits** til **msdyn\_name \[Navn\]**. Du skal evt. først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- I dit forbindelsessæt skal du tilføje en felttilknytning for integrationsnøglen for **msdyn\_projects** til **msdynce\_projectnumber \[Projektnummer\]**. Du skal evt. først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** for projektkontrakter og projekter kan opdateres til en anden værdi eller fjernes fra tilknytningen. Skabelonens standardværdi er **Project Service Automation**.
- **PaymentTerms**-tilknytningen skal opdateres, så den afspejler gyldige betalingsbetingelser i Finance. Du kan også fjerne tilknytningen fra projektopgaven. Standardværdikortet har standardværdier for demodata. Følgende tabel viser værdierne i Project Service Automation.

    | Værdi | Betegnelse   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | 2% 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis følgende betingelser er opfyldt:

- Du har salgsordrer i Dynamics 365 Sales.
- Du har flere organisationsenheder i Project Service Automation, og disse organisationsenheder knyttes til flere juridiske enheder i Finance.

Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:

- Skabelonen Projekter og kontrakter (PSA til Fin and Ops) har et standardfilter, der kun indeholder salgsordrer af typen **Workflowopgave (msdyn\_ordertype = 192350001)**. Dette filter hjælper med til at sikre, at der ikke oprettes projektkontrakter for salgsordrer i Finance. Hvis du opretter din egen skabelon, skal du tilføje dette filter.
- Du skal oprette et Power-forespørgselsfiltret, der kun indeholder de kontraktorganisationer, der skal synkroniseres til den juridiske enhed for integrationsforbindelsessættet. For eksempel skal projektkontrakter, du har med kontraktorganisationsenheden i Contoso USA, synkroniseres med den juridiske enhed for USSI, mens projektkontrakter, du har med kontraktorganisationsenheden i Contoso Global, synkroniseres med den juridiske enhed for USMF. Hvis du ikke føjer dette filter til din opgavetilknytning, synkroniseres alle projektkontrakter med den juridiske enhed, der er defineret for forbindelsessættet, uanset kontraktorganisationsenheden.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE] 
> Felterne **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** og **AddressZipCode** medtages ikke i standardtilknytningen for projektkontrakter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres for projektkontrakter.
>
> Felterne **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** og **ProjectType** medtages ikke i standardtilknytningen for projekter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres for projekter.

Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af skabelon](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Tilknytning af skabelon](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Tilknytning af milepæl for projektkontraktlinjer i skabelonen Projekter og kontrakter (PSA 3.x til Dynamics) - v2:

[![Tilknytning af skabelon](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
