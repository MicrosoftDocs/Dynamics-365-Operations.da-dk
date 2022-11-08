---
title: Ofte stillede spørgsmål om overførsel af Human Resources-kunde
description: Denne artikel besvarer ofte stillede spørgsmål om overførsel af Microsoft Dynamics 365 Human Resources til finans og drift-flettet infrastruktur.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734352"
---
# <a name="human-resources-customer-migration"></a>Overførsel af Human Resources-kunde

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Hvordan skal Dynamics 365 Human Resources-kunder planlægge at flytte til finans og drift-infrastrukturen?

To kategorier af Microsoft Dynamics 365 Human Resources-kunder påvirkes og vil være nødt til at foretage ændringer for at sikre, at de findes i den seneste finans og drift-infrastruktur:

- Kunder, der bruger Dynamics 365 Human Resources og ikke har andre driftsapps fra Dynamics 365
- Kunder, der bruger både Dynamics 365 Human Resources og Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce eller Dynamics 365 Project Operations

Uanset, hvilken kategori de tilhører, skal kunderne flytte data til et nyligt oprettet miljø i finans og drift-infrastrukturen og kontrollere, at fletningen er fuldført korrekt.

Fremover har appen Dynamics 365 Human Resources sit eget finans og drift-miljø, der er adskilt fra andre driftsapps. På denne måde kan kunderne få fordel af indstillingerne for extensibility uden at skulle flette de aktuelle data. Microsoft leverer værktøj og et sandkassemiljø, som kunder kan bruge til at teste og validere overflytning af data, før de flytter til et produktionsmiljø. Værktøjet aktiverer en næsten automatisk proces og er tilgængelig fra august til november 2022.

Kunder, der bruger andre apps i finans og drift-infrastrukturen, får mulighed for at flette deres human resources-data sammen med et eksisterende miljø. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Hvornår flyttes kunder til finans og drift-infrastrukturen?

Overflytningen for hver organisation afhænger af den aktuelle konfiguration og parathed med hensyn til overflytning til finans og drift-infrastrukturen. Det anbefales, at kunder arbejder sammen med deres Microsoft-partner for at finde den bedste sti fremad.

- Organisationer, der bruger **Human Resources**-modulet i Dynamics 365 Finance, vil kunne aktivere nye egenskaber fra Dynamics 365 Human Resources som en del af den almindelige proces til opdatering af Én version. Der planlægges nye funktioner til at blive generelt tilgængelige fra januar 2022.
- Organisationer, der bruger Dynamics 365 Human Resources, har adgang til værktøjer, som de kan bruge til at fuldføre fletningen af infrastrukturen. Microsoft vil arbejde sammen med kunderne om overførsel for at hjælpe med at forhindre, at der opstår problemer med servicen. Kunderne har 12 måneder til at foretage overførslen med start fra det tidspunkt, hvor overflytningsværktøjet bliver tilgængeligt.
- Organisationer, som både Dynamics 365 Human Resources og **Human Resources** bruger modulet kan flytte deres enkeltstående Human Resources-infrastruktur til finans og drift-infrastrukturen. En anden mulighed er at bruge fletteværktøjet til at få miljøet i ét enkelt miljø. Der er ingen krav eller tidsramme for fletning af de to miljøer.

Du kan finde opdaterede oplysninger ved jævnligt at kontrollere [frigivelsesplanerne](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Vil kunder stadig have brug for brugerdefineret integration mellem Dynamics 365 Human Resources og Human Resources-modulet?

- Kunder, som både har Dynamics 365 Human Resources og finans og drift-infrastrukturelle miljøer, der er integreret i øjeblikket, skal fortsætte med at integrere de to miljøer efter sammenlægningen.
- Kunder, der vælger at holde deres Dynamics 365 Human Resources-miljø adskilt fra det eksisterende økonomi- og driftsappmiljø, skal fortsætte med at integrere miljøet for at gøre dataene tilgængelige i begge miljøer.
- Kunder kan fortsætte med at bruge DataIntegrator til at kopiere data mellem de to miljøer. Kunder, der fletter data i et enkelt miljø efter overflytningen, behøver ikke længere at integrere dataene, da alle data vil være i en enkelt database.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Vil kunde-ISV-løsninger blive overflyttet automatisk?

Overflytningsoplevelsen for den enkelte uafhængige softwareleverandør (ISV) vil variere, afhængigt af løsningens integrationsmetode. Microsoft vil fungere tæt sammen med ISV'er for at sikre en problemfri overgang til den nye finans og drift-infrastruktur. Mange ISV-løsninger er baseret på Dataverse ved hjælp af funktionerne i Microsoft Power Platform. Disse løsninger afhænger af Dataverse-integrationen mellem Dynamics 365 Human Resources-miljøet og Dataverse-miljøet. Integrationen i Dataverse udfases som del af den infrastrukturelle fletning. I infrastrukturen i finans og drift planlægges nye rutekort, der skal erstatte funktionerne i Dataverse-integration.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Hvordan påvirkes den dataintegrator, der flytter data mellem Dynamics 365 Human Resources og andre Dynamics 365-apps?

Når kunder flytter til finans og drift-infrastruktur, skal de fortsætte med at integrere data mellem de to miljøer. Kunder kan fortsætte med at bruge dataintegratoren til at udføre disse dataoverflytningsopgaver. Kunder, der vælger at planlægge deres Dynamics 365 Human Resources-miljø adskilt fra det eksisterende programmer til finans og drift, skal fortsætte med at integrere data mellem de to miljøer. For kunder, der fletter de to miljøer til et enkelt miljø, er det ikke længere nødvendigt at integrere de to miljøer.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Hvordan flyttes data mellem Dynamics 365 Human Resources i finans og drift-infrastrukturen og Dataverse efter migrationen?

Den aktuelle Dataverse-integration mellem Dynamics 365 Human Resources og Dataverse udfases som en del af finans og drift-infrastruktur. Der er planer om at introducere disse for at knytte finans og driftsenhederne til Dataverse-tabellerne. Kunderne skal beslutte, hvilke kort der skal bruges til implementeringen. Det anbefales, at du bruger virtuelle tabeller til integration og isv-løsninger, medmindre der er et bestemt forretningsområde, hvor der er brug for at duplikere dataene i Dataverse for at køre forretningslogik.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Hvordan påvirker overflytningen Dataverse-udvidelser til Dynamics 365 Human Resources?

Kunder skal overflyttes til et sandboksmiljø, før de overfører produktionsmiljøet. Når kunder overfører deres sandboksmiljø, skal de oprette en kopi af deres Dataverse-miljø for at kunne oprette forbindelse til det nye finans og drift-overflyttede miljø. Vi anbefaler, at en kunde både kopierer dataene og løsningerne for miljøet, så de svarer til kundens aktuelle produktionsmiljø.

Når kunder er klar til at overflytte produktionsmiljøet Dynamics 365 Human Resources, overfører Microsoft automatisk databasen og Azure Blob-lagring. Den overflyttede database og lager peger mod et nyt miljø i finans og drift-infrastrukturen til samme Dataverse-produktionsmiljø. Før dataene kan fortsætte med at blive kopiere til Dataverse, skal kunderne aktivere alle de adressekort, der kræves til integration, udvidelser og ISV-løsninger, der er indbygget i Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Vil Microsoft Power Platform-komponenter der blev bygget til Dynamics 365 Human Resources automatisk fungere, når ændringen af infrastrukturen er fuldført?

Apps, der oprettes i Power Apps, flow, der oprettes i Power Automate og andre Microsoft Power Platform-tilpasninger er som Dataverse-udvidelser. Under overflytningen af produktionsmiljøer for kunder, har det ingen indflydelse på Dataverse-miljøer, heller ingen udvidelser. Tilpasninger af apps, flow og andre Power Microsoft Platform-tilpasninger skal fortsætte med at fungere, uden at det kræver yderligere konfiguration.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Hvad sker der med disse virtuelle Dataverse-tabeller til Dynamics 365 Human Resources under overflytningen?

Når kunder overfører deres Dynamics 365 Human Resources-miljø til finans og drift-infrastrukturen, vil miljøet fortsat være tilsluttet det Dataverse-miljø, der aktuelt er tilsluttet Dynamics 365 Human Resources. De virtuelle Dataverse-tabeller, der er genereret i miljøet, fortsætter med at fungere, uden at der kræves yderligere konfiguration. De virtuelle tabeller skal muligvis genereres igen i det Dataverse-miljø, hvor der er oprettet forbindelse til en kundes eksisterende finans og drift-miljø.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Hvordan skal en integration, der bruger API (Applicant Tracking System), Løn API, virtuelle Dataverse-tabeller til Dynamics 365 Human Resources eller andre enheder i Dataverse web-API'en fungere, når infrastrukturfletningen er fuldført?

Når kunder overfører deres Dynamics 365 Human Resources-miljø til finans og drift-infrastrukturen, vil miljøet fortsat være tilsluttet det Dataverse-miljø, der aktuelt er tilsluttet Dynamics 365 Human Resources. Alle integrationer, der er udviklet mod Dataverse web-API'en, fortsætter med at arbejde, efter at overflytningen er fuldført.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Vores organisation har konfigureret brugerdefineret sikkerhed i Dynamics 365 Human Resources. Vil vores brugerdefinerede sikkerhed stadig blive anvendt, når ændringen af infrastrukturen er fuldført?

Ja, brugerdefinerede sikkerhedskonfigurationer bliver inkluderet i overflytningen af data.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vil arbejdsgange i Dynamics 365 Human Resources automatisk blive overflyttet?

Ja, konfigurationer, historik og igangværende arbejdsgange vil blive overflyttet til flettet infrastruktur.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vil de gemte visninger i Dynamics 365 Human Resources blive overflyttet automatisk?

Ja, gemte visninger vil blive overflyttet til den nye infrastruktur.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Vil funktioner, der aktiveres i Dynamics 365 Human Resources, automatisk være tilgængelige efter fletningen af infrastrukturen?

- Funktioner, der kun er tilgængelige for Dynamics 365 Human Resources administreres via Funktionsstyring for kunder, der bruger modulet **Human Resources**. Normalt er disse funktioner ikke som standard aktiverede. Alle funktioner, der skal aktiveres som standard, vil blive dokumenteret.
- Funktioner i infrastrukturen, der bruger Dynamics 365 Human Resources, vil være tilgængelige for kunder. Alle funktioner, der ikke er tilgængelige, bliver dokumenteret. Alle de funktioner, der er aktiveret i det aktuelle Dynamics 365 Human Resources-miljø, aktiveres i den flettede infrastruktur. Få flere oplysninger i [Oversigt over funktionsstyring](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Hvad sker der med BYOD-databaser under overflytningen?

Import- og eksportkonfigurationer for din egen database (BYOD) vil blive overflyttet til finans og drift-infrastrukturen.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Påvirkes Azure-området, når mit kundemiljø overflyttes?

Miljøet Dynamics 365 Human Resources forbliver i samme Azure-område ved overflytningen. Hvis der er et krav om at flytte et miljø til et andet Azure-område, skal kunderne følge standardtrinnene til overflytning til en ny region, når overflytningen er gennemført.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Hvad sker der med min Azure Data Lake under overflytningen?

Enhver eksport, der aktuelt er konfigureret til Azure Data Lake i programmer til finans og drift, vedligeholder den samme konfiguration efter overflytningen.

> [!NOTE]
> Tilknytninger, der skrives på, skal aktiveres, før der kan fortsættes med at skrive data fra Human Resource-miljøet til Dataverse.

Kunder, der vil eksportere Personale-data til dataregistret, kan aktivere denne funktion, når overflytningen til finans og drift-infrastrukturen er gennemført. Du kan finde flere oplysninger i [Data Lake – Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Kunder kan knytte flere finans og drift-miljøer til samme datasø. De enkelte miljøer peger dog på en anden mappe og container. Kunder, der planlægger at flette miljøer senere, skal planlægge deres tilgang nøje.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Hvilken overflytning er påkrævet, hvis en kunde i øjeblikket bruger modulet Human Resources?

Kunder, der bruger **Human Resources**-modulet får denne nye funktionalitet fra i Dynamics 365 Human Resources, der anvendes i deres miljø via standardprocessen for opdatering af One Version. Kunder kan forvente at få vist de nye funktioner i deres miljø, efterhånden som de bliver tilgængelige med de enkelte opdateringer. Kunder kan bruge Administration af funktioner til at aktivere funktioner. Kunder skal planlægge at validere disse nye funktioner ved at bruge de processer, de allerede har på plads, og bruge til at validere andre opdateringer i deres miljø.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Hvad sker der med tilpassede integrationer med eksterne systemer?

Kunder skal overflytte integration med finans og drift-miljøet. Da slutpunktet for dette miljø er forskelligt, skal kunderne muligvis opdatere eller ændre integrationerne, så de peger på det nye miljø. Denne opgave er primært en manuel proces, og de ændringer, der kræves, afhænger af arkitekturen i integrationen. Kunder skal samarbejde med deres Microsoft-partner for at finde den bedste metode til flytning af integration.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Hvad sker der med Microsoft Power Platform (Dataverse) udvidelser, hvis kunder fletter et Dynamics 365 Human Resources-miljø med et eksisterende økonomi- og operationsmiljø?

Hvis kunder beslutter at flette et Dynamics 365 Human Resources-miljø og et eksisterende finans og drift-miljø til en enkelt Dataverse-forekomst efter overflytningen, skal deres Dataverse-miljøer samles som en del af fletteprocessen. Denne opgave kræver, at alle programmer, der oprettes ved hjælp af Power Apps og andre tilpasninger geninstalleres i det nye miljø.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Hvad sker der med dokumenterne under overflytningen?

Når kunder overfører deres Dynamics 365 Human Resources-miljø til finans og drift-infrastrukturen, vil dokumenterne forblive i det eksisterende dokumentlager og vil automatisk blive knyttet til det nye miljø i finans og drift-infrastrukturen.

I en fremtidig version vil der blive leveret nye dataenheder. Når ændringen er foretaget, kan kunder, der vælger at flette deres Dynamics 365 Human Resources-miljø med et eksisterende økonomi- og operationsmiljø, eksportere dokumenter og flytte dem til det eksisterende miljø.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Efter overflytningen, hvad sker der med de batchjob, som vi har konfigureret i Dynamics 365 Human Resources?

Batchjobs skal konfigureres igen i finans og drift-miljøet. Kunder skal evaluere hvert batchjob og sammenligne det med den aktuelle liste over batchjob i finans og drift-miljøet. Kunder bør også analysere den overordnede batchplan, når de fletter de to sæt batchjob for at finde ud af, om der skal foretages ændringer i batchplanen, prioriteter eller batchgrupper.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Hvordan vil overflytningen påvirke LCS-projektet for Dynamics 365 Human Resources?

Kunder skal oprette et nyt Microsoft Dynamics Lifecycle Service-projekt (LCS), og de skal vælge finans- og operationsapps som produkt og **implementering** som projekttype. Et nyt felt af underprojekttypen er også tilgængeligt, når der oprettes et LCS-projekt. Kunder skal vælge indstillingen til Dynamics 365 Human Resources-overflytning for at overflytte et eksisterende LCS-projekt i Personale til finans og drift-infrastrukturen.

Funktionerne i LCS-projekter vedrørende finans og drift er forskellige fra funktionerne i LCS-projekter under Personale.

Hvis nye kunder skal kunne gå i gang, skal de udføre følgende opgaver:

- Fuldføre projektonboarding.
- Fuldføre metoden.
- Udfylde abonnementsestimator.
- Fuldføre go-live-parathedsprocessen.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Hvordan overflyttes Forretningsprocesmodeller?

Kunder skal eksportere biblioteket til forretningsprocesmodeller fra Personale LCS-projektet og importere det til finans og drift LCS-projektet. Desuden skal kunder opdatere Indstillingerne for Hjælp i programmet, så de peger på det nye LCS-projekt.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Hvordan påvirker overflytningen tjenesteopdateringsprocessen?

Efter overflytningen vil kunderne have meget større fleksibilitet til administration af programlevetiden (ALM) og tjenesteopdateringer. Der vil ikke længere blive automatisk anvendt tjenesteopdateringer til Human Resources-miljøer. Tjenesten vil i stedet følge processerne og funktionerne til opdatering af én version for tjenesten, og konfigurationsindstillinger for opdateringer via LCS vil være aktiveret.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Er kunder berettiget til FastTrack-hjælp til fletningen af infrastrukturen?

Microsoft definerer stadig, hvilke værktøjer og ressourcer der skal være tilgængelige fra FastTrack som hjælp til fletningen.

## <a name="licensing-impact"></a>Påvirkning af licenser

Yderligere oplysninger om, hvordan licenserne påvirkes, finder du i [Dynamics 365 Human Resources-infrastrukturfletning](hr-infrastructure-merge.md#licensing).
