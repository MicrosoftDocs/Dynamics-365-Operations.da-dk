---
title: Vælg en teknologi til dataintegration
description: Denne artikel indeholder retningslinjer for forskellige muligheder for integration med data administreret af Personale, som beskriver egenskaberne for de forskellige integrationsteknologier, så integratorerne kan træffe rigtige beslutninger om, hvilke teknologier der bedst opfylder deres behov.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029882"
---
# <a name="choose-a-data-integration-technology"></a>Vælg en teknologi til dataintegration

Dynamics 365 Human Resources administrerer forretningsdata, der er nyttige i en lang række forretningsprocesser. Denne artikel indeholder retningslinjer for forskellige muligheder for integration med data administreret af Personale, som beskriver egenskaberne for de forskellige integrationsteknologier, så integratorerne kan træffe rigtige beslutninger om, hvilke teknologier der bedst opfylder deres behov.

## <a name="data-integration-vision"></a>Dataintegrationsvision

Microsoft ser forretningsdata som et vigtigt aktiv, der gør dit firma unikt. Din virksomhedens data er yderst værdifulde. Data, der indsamles og vedligeholdes af en del af virksomheden, vedrører data, der er indsamlet af en anden del af virksomheden, og disse relationer kan bruges til at forbedre forretningsprocesser og business intelligence i hele organisationen. Nem, sikker og stabil adgang til dine forretningsdata, uanset hvilket system der "ejer" dataene er et centralt punkt i den vision, vi har for dataintegration med Personale.

Historisk set har integration af data mellem flere systemer altid været vanskelig.
Microsoft er i færd med at gøre dataintegration nemmere og et stort skridt i forhold til dette mål realiseres via [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Fremadrettet skal Personale gøre Common Data Service til den foretrukne offentlige brugergrænseflade for Personale-data. Med tiden forventer vi, at alle de vigtigste data, der administreres af Personale, vil blive vist i Common Data Service. Vi anbefaler at vælge Common Data Service som teknologi til de fleste former for integrering af programmer. Da vi er klar over, at det ikke er alle data, som dit program kræver, der aktuelt findes i Common Data Service, og at dine projekttidslinjer muligvis kræver en anden teknologi, vil vi gerne informeres, når Common Data Service ikke opfylder dine krav til integration.

## <a name="integration-technologies"></a>Integrationsteknologier

I følgende afsnit beskrives de forskellige teknologier til dataintegration, der kan bruges sammen med Personale.

### <a name="common-data-service-entities"></a>Common Data Service-enheder

Common Data Service er den foretrukne offentlige datagrænseflade til Personale. Common Data Service er baseret på en velafprøvet platform, som kan føres tilbage til Dynamics 365 "XRM"-platformen, som [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-løsningerne er baseret på.

Common Data Service stiller en platform til rådighed for dataenheder og et API til at få adgang til disse enheder. Når Personale implementeres i din organisation, er Personale tilknyttet en Common Data Service-forekomst, og de enheder, der vedligeholder Personale-data, installeres i denne Common Data Service-forekomst, hvilket gør objekterne og deres data tilgængelige for alle programmer, der kan oprette forbindelse til Common Data Service-forekomsten. Afhængigt af hvilke Personale-apps du bruger, udfører Personale enten datahandlinger direkte i forhold til Common Data Service-enhederne (dette er tilfældet for Attract og Onboard) eller synkroniserer data til/fra Common Data Service-enhederne.

Når dataenhederne, der viser de data, som programmerne til integration skal bruge, findes i Common Data Service, kan du få fuldt udbytte af [Common Data Service og de API'er, det understøtter](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Blandt de understøttede API'er er [Dynamics 365 Web-API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), som leverer en OData-implementering til adgang til Common Data Service-data.

Common Data Service-enhederne og de tilknyttede API'er er den bedste mulighed for at få adgang til Personale-data fra webprogrammer, webtjenester/API'er og fra alle andre programmer, der har forbindelse til OData-feeds.

> [!NOTE]
> Beslutningen om at gøre Common Data Service til den foretrukne datagrænseflade for Personale er truffet for nylig, og det kan derfor være, at de Personale-dataenheder, du skal bruge til din integration, endnu ikke er tilgængelige i Common Data Service<sup>1</sup>. Hvis de Personale-enheder, der kræves til din integration, endnu ikke er tilgængelige, kan du vente på, at dataenhederne bliver tilgængelige, eller du kan bruge en af de andre integrationsteknologier, der er beskrevet nedenfor.
> 
> Som standard er Common Data Service-integration slået fra i nye miljøer, der ikke indeholder de leverede demonstrationsdata. Den er aktiveret i nye miljøer, der indeholder demodata, og datasynkroniseringen i miljøerne starter, når den er klargjort. Når miljøet er klar til at synkronisere data, kan du aktivere integration.

<sup>1</sup>Du kan finde en liste over Personale-enheder i Common Data Service i [Personale og Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). For Attract og Onboard er alle enheder tilgængelige i Common Data Service.

### <a name="dmfdixf-entities"></a>DMF/DIXF-enheder

Personale, der primært er bygget på samme platform som Finance and Operations-programmer, tilbyder [Data Management Framework (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), også kaldet Struktur for dataimport og -eksport eller DIXF, og et sæt dataenheder, der kan bruges til import/eksport af data til/fra Personale. Selvom Common Data Service-enheder er den foretrukne grænseflade til dataintegration for Personale, vil DMF-enhederne stadig være nyttige i nogle situationer, f.eks. når:

- Common Data Service-enheder endnu ikke er tilgængelige.

- Integrationen kræver, at der er mulighed for højtydende import/eksport af massedata.

DMF-enheder giver i øjeblikket den mest fuldstændige datadækning for Personale-data.

DMF er ikke egnet til integration i realtid (f.eks. når der kræves omgående brugerfeedback i en brugergrænseflade), da pakkehandlinger er planlagte batchjob, og der ofte vil være en ventetid på 1-2 minutter, før batchtjenesten henter jobbet til afvikling, samt den tid der skal bruges til at fuldføre import-/eksporthandlingen.

DMF kan være den bedste mulighed, når der kræves højt gennemløb (f.eks. import/eksport af mange tusinde poster, der er planlagt til at køre om natten).

> [!NOTE]
> DMF er ikke tilgængelig for Attract og Onboard.

### <a name="dmf-package-rest-api"></a>REST API for DMF-pakke

DMF har en [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) til manipulering af datapakker. Denne API kan bruges til programmeringsmæssigt at interagere med DMF, hvilket gør det muligt at udføre handlinger som:

- Importere en datapakke.

- Eksportere en datapakke.

- Kontrollere status for en import-/eksporthandling.

REST API for DMF-pakke er fuldt understøttet i Personale: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF indeholder desuden en effektiv funktion (kendt som [Brug din egen database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) eller BYOD (Bring Your Own Database)), der tillader Personale at eksportere data til din egen Microsoft Azure SQL-database. Dette giver stor fleksibilitet, for når dataene findes i din egen SQL-database, kan du gøre brug af alle programmer eller middleware, der kan oprette forbindelse til en SQL DataStore.

BYOD skal generelt betragtes som en skrivebeskyttet løsning. Mens du kan manipulere og gemme de data, du ønsker, i Azure SQL-databasen (som f.eks. til datamiks), synkroniseres de data, der er gemt i Azure SQL-databasen, ikke tilbage til Personale.

BYOD er velegnet til rapporteringsløsninger, dataintegrationer, datamiks, som en datakilde til en [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/)-pipeline.

> [!NOTE]
> BYOD er ikke tilgængelig for Attract og Onboard.

### <a name="odata-enabled-entities"></a>OData-aktiverede enheder

De fleste DMF-enheder er også aktiveret til at få adgang via datatjenesten Personale (OData). Den dokumentation, der leveres til [Finance and Operations OData-tjenestes](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) gælder generelt også for Personale, selvom dokumentation om oprettelse af dine egne OData-viste enheder ikke gælder.

Selvom Common Data Service og OData-implementeringen leveret af Common Data Service (via [Dynamics 365 Web-API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) foretrækkes i forhold til Personale-datatjenesten, har Personale-datatjenesten p.t. en mere komplet enhedsdækning for Personale-data.

### <a name="excel-add-in"></a>Excel-tilføjelsesprogram

[Excel-tilføjelsesprogrammet](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) gør brug af OData-aktiverede enheder under overfladen. Det er en praktisk måde at få en slutbruger til at hente og redigere Personale-data ved hjælp af den velkendte Excel-brugergrænseflade.

Excel-Tilføjelsesprogrammet er velegnet til ad hoc dataimport/-eksport udført af virksomhedsdomæneeksperter. En anden integrationsteknologi vil være mere passende til tilbagevendende dataintegration, der kræver programmeret automatisering.

### <a name="data-integrator"></a>Dataintegrator

Common Data Service-administratorens oplevelse leverer en [Dataintegrator-tjeneste](https://docs.microsoft.com/powerapps/administrator/data-integrator), der kan bruges til dataintegrationer til/fra Common Data Service. Dataintegrator kan bruges til at definere integrationsprojekter (ofte baseret på foruddefinerede skabeloner, som programudviklere har skræddersyet til bestemte integrationer). Integrationsprojekter kan planlægges til at køre automatisk i en tilbagevendende tidsplan eller køres manuelt.

Dataintegrator-projekter er egnede til Common Data Service-batchintegration og er et godt valg til integration mellem programmerne i Dynamics 365-familien. Som eksempel herpå har Microsoft en Dataintegrator-skabelon, der er klar til brug, og som kan bruges til integration af data fra Personale til Dynamics 365 Finance. Du kan finde flere oplysninger i [Integration fra Dynamics 365 Human Resources to Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power-forespørgsel

Dataintegrator understøtter også [Power-forespørgsel](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (via dens [Avanceret forespørgsel-funktion](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Power-forespørgsel har effektiv, fleksibel datafiltrering og transformering, herunder det omfattende M-formelsprog, og vil sandsynligvis være kendt af dem, som har erfaring med at udvikle Power BI-rapporter.

## <a name="deciding-on-an-integration-technology"></a>Beslutning om en integrationsteknologi

Med så mange forskellige integrationsteknologier, der er til rådighed, kan beslutningen om, hvilken integrations metode der skal bruges, nogle gange være overvældende. Hen over tid, og specielt i takt med at datadækningen i Common Data Service udvikles, bliver beslutningen nemmere, hvor Common Data Service i de fleste tilfælde vil være den foretrukne datagrænseflade. Men indtil da kan det være, at Common Data Service endnu ikke opfylder dine behov. I nedenstående tabel kan du opsummere nogle af de vigtigste karakteristika ved de forskellige muligheder for integrationsteknologi.

| Technology/Tool/API    | Tilbagevendende integrationer                   | Synkron/asynkron                    | Programadgang via en API        | Relevante datadiskenheder                                   | Datadækning                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-enheder           | Ja, med brug af Dataintegrator eller middleware | Synkroniser asynkron, batch (via Dataintegrator) | Ja, via Dynamics 365 Web-API (OData) | Varierer efter brug (understøtter sideinddeling til interaktiv brug) | Forbedring<sup>2</sup>                       |
| DMF-entiteter           | Ja, planlagt via middleware        | Asynkon, batch                                | Ja, via REST API for DMF-pakke         | Høj (hundredtusindvis af poster)                    | Høj                                |
| REST API for DMF-pakke   | Ja, planlagt via middleware        | Asynkon, batch                                | Ja                                       | Høj (hundredtusindvis af poster)                    | API understøtter alle DMF-enheder       |
| BYOD                   | Ja, planlagt af administrator i Personale        | Asynkon, batch                                | Nej<sup>3</sup>                                    | Høj (hundredtusindvis af poster)                    | Understøtter alle DMF-enheder           |
| OData-aktiverede enheder | Ja, ved hjælp af middleware                    | Synkroniser                                        | Ja, via Personale-datatjenesten (OData)  | Varierer efter brug (understøtter sideinddeling til interaktiv brug) | Høj                                |
| Excel-tilføjelsesprogram           | Nr.                                       | Synkroniser                                        | Nr.                                        | Mellem (titusindvis af poster)                      | Understøtter alle OData-aktiverede enheder |
| Dataintegrator        | Ja, planlagt i Dataintegrator        | Asynkon, batch                                | Nr.                                        | Varierer efter brug                                       | Understøtter alle Common Data Service-enheder           |

<sup>2</sup>Microsoft investerer i stor stil i øget datadækning for Common Data Service-enheder og anbefaler Common Data Service som den foretrukne datagrænseflade, når dækning er tilgængelig. I øjeblikket Common Data Service er datadækningen lav i forhold til DMF og OData-aktiverede enheder.

<sup>3</sup>SQL-database har programmeringsmæssig adgang.

## <a name="summary"></a>Resume

Dine forretningsdata er et værdifuldt aktiv, men værdien kan formindskes meget, hvis det er svært at bruge dataene til bestemte formål (f.eks. rapportering, datamiks eller brugerdefinerede programmer). Dynamics 365 Human Resources indeholder flere teknologier til arbejde med dine data uden for Personale-programmets brugergrænseflade, hvilket giver mulighed for at integrere programadgang til dataene. Dette emne indeholder en beskrivelse af de tilgængelige integrationsteknologier og nogle af deres vigtigste egenskaber. Disse oplysninger bør hjælpe dig med at træffe bedre beslutninger om, hvilke metoder der skal bruges til integrationsprojekter.

