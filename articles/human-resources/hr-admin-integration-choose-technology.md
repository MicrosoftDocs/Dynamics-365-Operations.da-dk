---
title: Vælg en dataintegrationsteknologi
description: Denne artikel indeholder oplysninger om integration med data, der administreres Human Resources. Den beskriver forskellige integrationsteknologier, der kan hjælpe dig med at afgøre, hvilke teknologier der bedst opfylder dine behov.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
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
ms.openlocfilehash: 9e6eeac66cff24d193e30aa942039707fc0aed52
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528335"
---
# <a name="choose-a-data-integration-technology"></a>Vælg en dataintegrationsteknologi

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikel indeholder oplysninger om integration med data, der administreres af Dynamics 365 Human Resources. Den beskriver forskellige integrationsteknologier, der kan hjælpe dig med at afgøre, hvilke teknologier der bedst opfylder dine behov.

## <a name="data-integration-background"></a>Baggrund for dataintegration

Forretningsdata er et vigtigt aktiv, der gør dit firma unikt. Din virksomhedens data er yderst værdifulde. Du kan bruge relationerne mellem data, der indsamles i hele virksomheden, for at forbedre forretningsprocesser og Business Intelligence i hele organisationen. Vi bestræber os på at give dig nem, sikker og stabil adgang til dine forretningsdata, uanset hvilket system de kommer fra.

Historisk set har integration af data mellem flere systemer altid været vanskelig.
Microsoft er i færd med at gøre dataintegration nemmere og et stort skridt i forhold til dette mål realiseres via [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Human Resources gør Common Data Service til den foretrukne offentlige brugergrænseflade for Human Resources-data. Med tiden forventer vi, at alle de vigtigste data, der administreres af Personale, vil blive vist i Common Data Service. Vi anbefaler at vælge Common Data Service som teknologi til de fleste former for integrering af programmer.

Vi er klar over, at Common Data Service muligvis ikke endnu indeholder de data, som dit program kræver. Vi er også klar over, at din tidslinje for projektet måske kræver en alternativ teknologi. Husk at give os besked, når Common Data Service ikke opfylder dine integrationsbehov.

## <a name="integration-technologies"></a>Integrationsteknologier

I følgende afsnit beskrives de forskellige teknologier til dataintegration, der kan bruges sammen med Personale.

### <a name="common-data-service-entities"></a>Common Data Service-enheder

Common Data Service er den foretrukne offentlige datagrænseflade til Personale. Det skyldes Dynamics 365 XRM-platformen, som bruges af [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement)-løsninger.

Common Data Service leverer en platform og en API til dataenheder. Når du implementerer Human Resources, opretter programmet forbindelse til en Common Data Service-forekomst. Enhederne for Human Resources-data implementeres i den pågældende Common Data Service-forekomst. Enhederne og deres data er tilgængelige for alle programmer, der kan oprette forbindelse til Common Data Service-forekomsten. Human Resources synkroniserer data til og fra Common Data Service-enhederne.

Når de dataenheder, der kræves af dine integrerede apps, er i Common Data Service, kan du fuldt ud bruge [Common Data Service og de API'er, det understøtter](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Blandt de understøttede API'er er [Dynamics 365 Web-API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), som leverer en OData-implementering til adgang til Common Data Service-data.

Common Data Service-enhederne og deres tilknyttede API'er er den bedste mulighed for at få adgang til Human Resources-data fra webprogrammer, webtjenester/API'er og fra alle andre programmer, der har forbindelse til OData-feeds.

> [!NOTE]
> Da beslutningen om at gøre Common Data Service til den foretrukne datagrænseflade for Human Resources blev truffet for nylig, er de Human Resources-dataenheder, du skal bruge til din integration, muligvis endnu ikke tilgængelige i Common Data Service.
</br>
> Du kan finde en liste over de Human Resources-enheder, som er tilgængelige, i Common Data Service, i [Human Resources og Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Hvis de Human Resources-enheder, der kræves til din integration, endnu ikke er tilgængelige, skal du vente på, at dataenhederne bliver tilgængelige, eller du kan bruge en af de andre integrationsteknologier, der er beskrevet nedenfor.
> </br>
> Som standard er Common Data Service-integration slået fra i nye miljøer, der ikke indeholder de leverede demonstrationsdata. Den er aktiveret i nye miljøer, der indeholder demodata, og datasynkroniseringen i miljøerne starter, når den er klargjort. Når miljøet er klar til at synkronisere data, kan du aktivere integration.

### <a name="dmfdixf-entities"></a>DMF/DIXF-enheder

Human Resources, der primært bygger på samme platform som Finance and Operations-programmer, tilbyder en [DMF (Data Management Framework)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). DMF er også kendt som DIXF (Data Import Export Framework). Human Resources omfatter et sæt dataenheder, du kan bruge til at importere og eksportere Human Resources-data. Selvom Common Data Service-enheder er den foretrukne grænseflade til dataintegration for Human Resources, vil DMF-enhederne stadig være nyttige i nogle situationer, f.eks. når:

- Common Data Service-enheder endnu ikke er tilgængelige.

- Integrationen kræver funktioner til højtydende import/eksport af massedata.

DMF-enheder giver i øjeblikket den mest fuldstændige datadækning for Personale-data.

DMF er ikke egnet til realtidsintegrationer, f.eks. når du har brug for øjeblikkelig brugerfeedback i en brugergrænseflade. Pakkeoperationer er planlagte batchjob og har ofte en ventetid på 1-2 minutter, før batchtjenesten plukker jobbet til afvikling, plus den tid, der eventuelt kræves til at fuldføre import- eller eksportoperationen.

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

DMF indeholder desuden en effektiv funktion (kendt som [Brug din egen database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) eller BYOD (Bring Your Own Database)), der tillader Human Resources at eksportere data til din egen Microsoft Azure SQL-database. Denne funktion giver en enorm fleksibilitet. Når dataene findes i din egen SQL-database, kan du bruge alle programmer eller middleware, der kan oprette forbindelse til en SQL DataStore.

BYOD er hovedsageligt en skrivebeskyttet løsning. Mens du kan manipulere og gemme de data, du ønsker, i Azure SQL-databasen (som f.eks. til datamiks), synkroniseres de data, der er gemt i Azure SQL-databasen, ikke tilbage til Human Resources.

BYOD er velegnet til rapporteringsløsninger, dataintegrationer, datamiks, som en datakilde til en [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/)-pipeline.

> [!NOTE]
> BYOD er ikke tilgængelig for Attract og Onboard.

### <a name="odata-enabled-entities"></a>OData-aktiverede enheder

De fleste DMF-enheder er også aktiveret til at få adgang via datatjenesten Personale (OData). Dokumentationen til [Finance and Operations OData-tjenesten](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) gælder for Human Resources, bortset fra når du opretter dine egne enheder, der vises i OData.

Selvom Common Data Service og OData-implementeringen leveret af Common Data Service (via [Dynamics 365 Web-API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) foretrækkes i forhold til Personale-datatjenesten, har Personale-datatjenesten p.t. en mere komplet enhedsdækning for Personale-data.

### <a name="excel-add-in"></a>Excel-tilføjelsesprogram

[Excel-tilføjelsesprogrammet](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) gør brug af OData-aktiverede enheder under overfladen. Det er en praktisk måde at få en slutbruger til at hente og redigere Personale-data ved hjælp af den velkendte Excel-brugergrænseflade.

Excel-Tilføjelsesprogrammet er velegnet til ad hoc dataimport/-eksport udført af virksomhedsdomæneeksperter. En anden integrationsteknologi vil være mere passende til tilbagevendende dataintegration, der kræver programmeret automatisering.

### <a name="data-integrator"></a>Dataintegrator

Du kan bruge [Dataintegrator-tjenesten](https://docs.microsoft.com/powerapps/administrator/data-integrator) til at integrere data til og fra Common Data Service. Du kan bruge Data Integrator til at definere integrationsprojekter, der ofte er baseret på foruddefinerede skabeloner, som programudviklere har skræddersyet til bestemte integrationer. Du kan planlægge integrationsprojekter til at køre automatisk i en tilbagevendende tidsplan eller køre dem manuelt.

Data Integrator-projekter er egnede til Common Data Service-batch-integrationer. De er et godt valg til integration mellem Dynamics 365-programmerne. Microsoft leverer f.eks. en Data Integrator-skabelon til integration af data fra Human Resources til Dynamics 365 Finance. Du kan få mere at vide om skabelonen i [Integration fra Dynamics 365 Human Resources til Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power-forespørgsel

Data Integrator understøtter [Power-forespørgsel](https://docs.microsoft.com/power-query/power-query-what-is-power-query) via dens [Avanceret forespørgsel-funktion](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query indeholder en effektiv, fleksibel datafiltrering og -transformering, herunder det avancerede M-formelsprog. Du kender sikkert Power Query, hvis du har udviklet Power BI-rapporter.

## <a name="deciding-on-an-integration-technology"></a>Beslutning om en integrationsteknologi

Med så mange forskellige integrationsteknologier, der er til rådighed, kan beslutningen om, hvilken integrations metode der skal bruges, nogle gange være overvældende. I takt med at datadækningen i Common Data Service udvikles, bliver beslutningen nemmere, da Common Data Service i de fleste tilfælde vil være den foretrukne datagrænseflade. Indtil da kan det være, at Common Data Service endnu ikke opfylder dine behov. I nedenstående tabel opsummeres nogle af de vigtigste karakteristika ved mulighederne for integrationsteknologi.

| Technology/Tool/API    | Tilbagevendende integrationer                   | Synkron/asynkron                    | Programadgang via en API        | Relevante datadiskenheder                                   | Datadækning                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service-enheder           | Ja, med brug af Dataintegrator eller middleware | Synkroniser asynkron, batch (via Dataintegrator) | Ja, via Dynamics 365 Web-API (OData) | Varierer efter brug (understøtter sideinddeling til interaktiv brug) | Forbedring<sup>2</sup>                       |
| DMF-entiteter           | Ja, planlagt via middleware        | Asynkon, batch                                | Ja, via REST API for DMF-pakke         | Høj (hundredtusindvis af poster)                    | Høj                                |
| REST API for DMF-pakke   | Ja, planlagt via middleware        | Asynkon, batch                                | Ja                                       | Høj (hundredtusindvis af poster)                    | API understøtter alle DMF-enheder       |
| BYOD                   | Ja, planlagt af administrator i Personale        | Asynkon, batch                                | Nej<sup>3</sup>                                    | Høj (hundredtusindvis af poster)                    | Understøtter alle DMF-enheder           |
| OData-aktiverede enheder | Ja, ved hjælp af middleware                    | Synkroniser                                        | Ja, via Personale-datatjenesten (OData)  | Varierer efter brug (understøtter sideinddeling til interaktiv brug) | Høj                                |
| Excel-tilføjelsesprogram           | Nr.                                       | Synkroniser                                        | Nr.                                        | Mellem (titusindvis af poster)                      | Understøtter alle OData-aktiverede enheder |
| Dataintegrator        | Ja, planlagt i Dataintegrator        | Asynkon, batch                                | Nr.                                        | Varierer efter brug                                       | Understøtter alle Common Data Service-enheder           |

<sup>2</sup>Microsoft investerer meget for at øge datadækningen af Common Data Service-enheder. Vi anbefaler, at du bruger Common Data Service, når dækningen er tilgængelig. I øjeblikket er Common Data Service-datadækningen lav sammenlignet med DMF- og OData-aktiverede enheder.

<sup>3</sup>SQL-database har programmeringsmæssig adgang.
