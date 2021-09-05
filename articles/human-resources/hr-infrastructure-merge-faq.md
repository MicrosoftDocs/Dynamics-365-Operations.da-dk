---
title: Ofte stillede spørgsmål om fletning af Dynamics 365 Human Resources-infrastruktur
description: I dette emne besvares ofte stillede spørgsmål om fletningen af infrastruktur for Microsoft Dynamics 365 Human Resources- og Finance and Operations-apps.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ae2896eda98a8f9545d465e941d5b50065ae94b
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386533"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Ofte stillede spørgsmål om fletning af Dynamics 365 Human Resources-infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne besvares ofte stillede spørgsmål om fletningen af infrastruktur for Microsoft Dynamics 365 Human Resources- og Finance and Operations-apps.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hvad er fletning af Dynamics 365 Human Resources-infrastruktur?

Dynamics 365 Human Resources er et selvstændigt program, der bruger en anden infrastruktur end andre Finance and Operations-apps, f.eks. Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Project Operations. Fletningen af infrastrukturen placerer Dynamics 365 Human Resources i samme infrastruktur som andre Finance and Operations-apps.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Værdi og fordele ved infrastrukturens fletning

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Min organisation bruger Dynamics 365 Human Resources til at administrere HR-handlinger. Hvilke fordele kan vi se i disse ændringer?

- Disse ændringer fjerner den forvirring som skyldes flere sæt personalefunktioner (HR) i Dynamics 365.
- De muliggør både udvidelse af Microsoft Power Platform og en metode til at udvide forretningslogik og funktionsmuligheder.
- De giver ensartethed mellem Dynamics 365 Human Resources og andre Finance and Operations-apps i form af Application Lifecycle Management (ALM), Microsoft Dynamics Lifecycle Services (LCS), geografisk tilgængelighed, udvidelsesmuligheder og meget mere.
- De giver dig mulighed for at benytte delte tjenester og værktøjer og reducere omkostningerne.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Min organisation bruger Human Resources-modulet i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Hvilke fordele kan vi se i disse ændringer?

De funktioner og investeringer, der er tilføjet i Dynamics 365 Human Resources, vil nu være tilgængelige for kunder, der bruger HR-modulet i Dynamics 365 Finance. Nogle af disse funktioner omfatter styring af orlov og fravær, styring af goder og opgavestyring.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Mister jeg funktioner eller muligheder, som jeg har i øjeblikket?

Der vil være funktionel paritet mellem Dynamics 365 Human Resources og HR-modulet i Finance and Operations-apps. Dynamics 365 Human Resources vil have forrang for lignende funktioner. Få flere oplysninger i [Oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Vil mine brugere få en anden oplevelse?

De nye HR-funktioner administreres via Funktionsstyring. Debitorerne skal beslutte, om de vil konfigurere dem. I nogle tilfælde kan funktioner være blevet ændret. I disse tilfælde vil der blive leveret dokumentation.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Hvordan påvirker denne ændring mig, hvis jeg er en eksisterende kunde, og jeg bruger både HR-modulet i Finance and Operations-infrastrukturen og Dynamics 365 Human Resources gennem brugerdefinerede integrationer?

Der kræves ikke længere brugerdefinerede integrationer mellem Dynamics 365 Human Resources og HR-modulet i Dynamics 365 Finance. Alle HR-data findes i samme database som andre Finance and Operations-apps.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Overflytning fra Dynamics 365 Human Resources til Finance and Operations-apps

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Min organisation bruger Dynamics 365 Human Resources til at administrere HR-handlinger. Hvad skal vi planlægge for at overflytte til den nye oplevelse?

Hvis din organisation bruger Dynamics 365 Human Resources, men ikke bruger andre Finance and Operations-apps, overflyttes Human Resources-miljøet til den nye infrastruktur. En stor del af denne overflytningsproces vil være automatiseret. Der vil være processer for overflytning af databasen og synkronisering af den med den nye infrastruktur.

Desuden findes der værktøjer, så du kan teste overflytningsprocessen og validere dataene og oplevelsen, før du overflytter produktionsmiljøet.

Hvis organisationen bruger både Dynamics 365 Human Resources og og andre Finance and Operations-apps, skal du planlægge mere tid til validering for at sikre, at dataene overflyttes korrekt til det nye miljø. Overflytningen til den nye infrastruktur fletter dataene fra Human Resources-miljøet med Finance and Operations-miljøet. Datakonflikter kræver brugerinput for at afgøre, hvordan konflikten skal løses. Brugere og administratorer skal administrere de datatilknytninger, hvor der er konflikter, og teste overflytningen til sandkassemiljøer inden overflytningen af produktionsmiljøer.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Min organisation bruger Human Resources-modulet i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Hvad skal vi planlægge for at overflytte til den nye oplevelse?

For organisationer, der bruger HR-modulet i Finance and Operations-apps, anvendes den nye funktion fra Dynamics 365 Human Resources til dit miljø via standardprocessen for opdatering af Én version. Du kan forvente at få vist de nye funktioner i dit miljø, efterhånden som de bliver tilgængelige med de enkelte opdateringer. Du kan bruge Funktionsstyring til at aktivere nye funktioner, men du skal planlægge at validere disse funktioner. Følg de processer, du har etableret for validering af andre opdateringer af miljøet. Du kan finde flere oplysninger om, hvordan opdateringer anvendes i Finance and Operations-apps, i [Oversigt over Én version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Hvornår bliver organisationen overflyttet?

Overflytningen for hver organisation afhænger af den aktuelle konfiguration og parathed med hensyn til overflytning til den nye infrastruktur. Disse datoer kan blive ændret.

- Organisationer, der bruger HR-modulet i Finance and Operations-apps, modtager HR-funktionen til Dynamics 365 Human Resources som del af den almindelige opdateringsproces for Én version. Der planlægges nye funktioner til at blive generelt tilgængelige fra januar 2022.
- Organisationer, der kun bruger Dynamics 365 Human Resources, vil have adgang til overflytningsværktøjet, så de kan påbegynde test og starte overflytningen fra midt i 2022. Den dato, hvor overflytningen til den nye infrastruktur skal være fuldført, inden den ikke er fastlagt endnu. Det vil dog være mindst ét år efter den dato, hvor overflytningsværktøjet bliver tilgængeligt.
- Organisationer, der bruger både Dynamics 365 Human Resources og andre Finance and Operations-apps, vil have adgang til overflytningsværktøjet, så de kan påbegynde test og starte overflytningen sidst i 2022. Den dato, hvor overflytningen til den nye infrastruktur skal være fuldført, inden den ikke er fastlagt endnu. Det vil dog være mindst ét år efter den dato, hvor overflytningsværktøjet bliver tilgængeligt.

Du kan finde flere oplysninger om de nye funktioner til Dynamics 365 Human Resources i [Nyheder eller ændringer i Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Min organisation kører ikke Dynamics 365 Human Resources endnu. Skal vi arbejde med modulet Human Resources i Finance and Operations-apps eller med Dynamics 365 Human Resources-appen i den ældre infrastruktur?

Det er vigtigt at overveje, hvilke HR-funktioner der er behov for, og hvornår funktionen bliver tilgængelig i den nye infrastruktur. Hvis organisationen skal bruge kernefunktionaliteten til personalestyring, er den i øjeblikket tilgængelig i HR-modulet i Finance and Operations-apps i den nye infrastruktur. Funktionsparitet mellem HR-modulet i Finance and Operations-apps og Dynamics 365 Human Resources-appen forventes i versionen 10.0.25, som er planlagt til at blive generelt tilgængelig i marts 2022. Integrationsfunktioner som Teams-appen og Dataverse-enhedsintegrationer vil være tilgængelige i senere versioner.

Hvis organisationens behov for HR-funktionaliteten vil være tilgængelige i den nye infrastruktur inden for den tidsramme, hvor organisationen vil køre den, kan det være nemmere at køre HR-modulet i Finance and Operations-apps. Det vil resultere i en nemmere overflytning, da det vil være en standardprogramopgradering til Dynamics 365 Human Resources-applikationen, og kunden vil allerede benytte den nye infrastruktur. Hvis organisationen beslutter at køre Dynamics 365 Human Resources-applikationen i den ældre infrastruktur, skal en overflytning af miljøet flyttes til den nye infrastruktur. Det kan undgås ved at køre i den nye infrastruktur.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Jeg bruger nye funktioner, der kun er tilgængelige i Dynamics 365 Human Resources (f.eks. **Orlov og fravær** og **Frynsegodeadministration**). Vil disse funktioner nu også være tilgængelige i Human Resources-modulet i Finance and Operations-infrastrukturen?

Ja, alle moduler fra Dynamics 365 Human Resources vil fungere som i Finance and Operations-apps, og der vil være en funktionsparitet på 100 procent. Som en del af den overordnede overflytningsstrategi for kunder, der i øjeblikket bruger disse funktioner i HR, vil kundedata blive overflyttet, så de fortsat fungerer i Finance and Operations-infrastrukturen.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Jeg bruger de nye funktioner til administration af frynsegoder i Dynamics 365 Human Resources. Jeg har opbygget brugerdefinerede integrationer med HR-modulet i Finance and Operations-infrastrukturen, så jeg kan udnytte lønfunktionerne ved at bruge frynsegodedata. Vil disse brugerdefinerede integrationer være påkrævet fremover?

Som en del af fletningen af infrastrukturen oprettes HR-data i samme database som andre Finance and Operations-apps. Det er ikke længere være nødvendigt at integrere modulerne i Finance and Operations-apps.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Min organisation bruger en eller flere ISV-løsninger sammen med Dynamics 365 Human Resources. Vil vores ISV-løsninger blive overflyttet automatisk?

Overflytningsoplevelsen for den enkelte uafhængige softwareleverandør (ISV) vil variere, afhængigt af løsningens integrationsmetode. Microsoft vil fungere tæt sammen med ISV'er for at sikre en problemfri overgang til den nye infrastruktur.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Min organisation bruger LinkedIn Talent Hub-integration sammen med Dynamics 365 Human Resources. Vil denne integration fortsat fungere, når ændringen af infrastrukturen er fuldført?

Nej, integrationen af LinkedIn Talent Hub fungerer fortsat ikke efter overflytningen til den nye infrastruktur. Tjenesten til integration af LinkedIn Talent Hub udgår med den ældre Dynamics 365 Human Resources-infrastruktur.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Min organisation bruger Human Resources-appen til Teams. Vil appen fortsat fungere, når ændringen af infrastrukturen er fuldført?

Ja, Human Resources-appen til Teams vil fortsat fungere efter overflytningen til den nye infrastruktur.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Min organisation har konfigureret brugerdefineret sikkerhed i Dynamics 365 Human Resources. Vil vores brugerdefinerede sikkerhed stadig blive anvendt, når ændringen af infrastrukturen er fuldført?

Ja, brugerdefinerede sikkerhedskonfigurationer bliver inkluderet i overflytningen af data til den nye infrastruktur.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Vi bruger dataintegrator til at flytte data mellem Dynamics 365 Human Resources og Finance and Operations-apps. Hvordan påvirkes de data, der er ved at blive integreret?

HR-data, der findes i øjeblikket i Dynamics 365 Human Resources, synkroniseres med Dataverse. Dataintegrator kan derefter bruges til envejssynkronisering med Finance and Operations-apps. Efter overflytningen til den nye infrastruktur vil HR-data være indbyggede i Finance and Operations-appsene. Dataintegrator vil ikke længere være nødvendig for at synkronisere dataene mellem Finance and Operations-apps og Human Resources.

De aktuelle indbyggede Dataverse-datatabeller til Human Resources vil fortsat synkronisere dataene fra miljøet med den nye infrastruktur. Enhederne konverteres til at understøtte dobbeltskrivning. Alle andre dataintegrationer, der er konfigureret via Dataintegrator i forhold til disse tabeller for andre Dynamics 365-apps, vil fortsat fungere, som de er konfigureret i øjeblikket.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Vi bruger dobbeltskrivning til at flytte HR-data mellem Dataverse og andre Finance and Operations-apps. Hvordan påvirkes de data, der i øjeblikket bliver integreret, af overflytningen til den nye infrastruktur?

HR-data vil være indbyggede i Finance and Operations-apps i den nye infrastrukturs miljø. Dobbeltskrivning bruges til at flytte HR-data mellem det nye miljø og Dataverse-miljøet.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Vi har opbygget brugerdefinerede integrationer fra Dynamics 365 Human Resources til et eller flere eksterne systemer. Vil vi skulle udvikle nye integrationer, når ændringen af infrastrukturen er fuldført?

Det afhænger af integrationens slutpunkt. Du kan finde flere oplysninger om de integrationsteknologier, der findes i Finance and Operations-apps, og hvordan du vælger den bedste integrationsteknologi, i [Oversigt over integration](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Vi har udvidet Dataverse til Dynamics 365 Human Resources. Vil disse udvidelser blive overflyttet automatisk?

Hvis Dynamics 365 Human Resources- og Finance and Operations-miljøerne, der vil blive samlet i miljøet i den nye infrastruktur, er forbundet med samme Dataverse-miljø, vil de to apps fortsat være forbundet med samme Dataverse-miljø efter overflytningen. Der kræves ingen overflytning for Dataverse-udvidelser.

Hvis Dynamics 365 Human Resources- og Finance and Operations-miljøerne i øjeblikket er forbundet med separate Dataverse-miljøer, vil de to Dataverse-miljøer imidlertid skulle kombineres, så de er forbundet med ét enkelt miljø i den nye infrastruktur. For denne Dataverse-overflytning kan de Dataverse-tabeller, der er standard for Human Resources-løsningerne, oprette forbindelse til og gensynkroniseres med det nye Dataverse-miljø. Eventuelle udvidelser til Dataverse-miljøet overflyttes ikke automatisk, men skal geninstalleres i det nye miljø. Det anbefales at bruge administrerede løsninger til at administrere dine Dataverse-udvidelser. Du kan finde flere oplysninger i [Introduktion til løsninger](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Vi har konfigureret Microsoft Power Automate-flow og/eller Microsoft Power Apps til at fungere sammen med Dynamics 365 Human Resources. Vil disse Microsoft Power Platform-komponenter blive overflyttet og fungere automatisk, når ændringen af infrastrukturen er fuldført?

Power Apps, Power Automate-flow og andre Microsoft Power Platform-tilpasninger ligner Dataverse-udvidelser. Om de fungerer automatisk efter overflytningen til den nye infrastruktur, afhænger af, om Human Resources-appen og Finance and Operations-appsene er forbundet med samme Power Apps-miljø før overflytningen.

Hvis appsene har forbindelse til det samme Power Apps-miljø, fortsætter de med at være tilsluttet det pågældende Power Apps-miljø efter overflytningen til den nye infrastruktur. I dette tilfælde vil Power Apps, Power Automate-flow og andre Microsoft Power Platform-tilpasninger fortsat fungere uden yderligere konfiguration. Det anbefales at bruge administrerede løsninger til at administrere dine applikationsudvidelser i Dataverse. Du kan finde flere oplysninger i [Introduktion til løsninger](/powerapps/developer/data-platform/introduction-solutions).

Men hvis Human Resources-appen og Finance and Operations-appsene er forbundet med separate Power Apps-miljøer, skal de kombineres som en del af overflytningen. Denne opgave kræver, at Power Apps og andre tilpasninger geninstalleres i det nye miljø.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Vi har aktiveret virtuelle Dataverse-tabeller for Dynamics 365 Human Resources. Hvad sker der med disse tabeller under overflytningen?

Hvis miljøet i den nye infrastruktur forbliver forbundet med det Dataverse-miljø, der aktuelt er forbundet med Dynamics 365 Human Resources, vil de virtuelle Dataverse-tabeller, der er genereret i det pågældende miljø, fungere efter overflytningen uden yderligere konfiguration.

Men hvis miljøet i den nye infrastruktur er forbundet med et andet Dataverse-miljø efter overflytningen, skal de virtuelle tabeller genereres igen i det nye Dataverse-miljø.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Vi har udviklet en integration ved hjælp af ATS-API (Applicant Tracking System), Løn-API, virtuelle Dataverse-tabeller for Dynamics 365 Human Resources eller andre enheder i Web-API'en for Dataverse. Vil disse integrationer fortsat fungere, når ændringen af infrastrukturen er fuldført?

Hvis miljøet i den nye infrastruktur forbliver forbundet med det -miljø, der aktuelt er forbundet med Dynamics 365 Human Resources, vil de virtuelle Dataverse-tabeller, vil alle integrationer, der er udviklet i forhold til Web-API'en for Dataverse fortsat fungere efter overflytningen er fuldført.

Hvis miljøet i den nye infrastruktur er forbundet med et andet Dataverse-miljø efter overflytningen, vil alle integrationer, der er udviklet i forhold til Web-API'en for Dataverse imidlertid skulle omkonfigureres, for at de kan oprette forbindelse til det nye Dataverse-miljø.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Påvirkes Azure-området, når mit miljø overflyttes?

Det forventes, at Human Resources-miljøet typisk vil forblive i samme Azure-område under overflytningen. Den eneste undtagelse er, hvis Human Resources-miljøet flettes sammen med et Finance and Operations-miljø, der er i et andet område. I dette tilfælde overflyttes Human Resources-miljøet til Azure-området i Finance and Operations-miljøet.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Min organisation er afhængig af arbejdsgange i Dynamics 365 Human Resources for en eller flere forretningsprocesser. Vil arbejdsgange automatisk blive overflyttet?

Ja, konfigurationer, historik og igangværende arbejdsgange vil blive overflyttet.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Hvilken uddannelse og hvilke ressourcer er tilgængelige som hjælp i overflytningsprocessen?

Der leveres komplet dokumentation, som beskriver hvert enkelt trin i overflytningsprocessen i detaljer. Der kan også være yderligere uddannelsesressourcer som f.eks. videoer og workshops tilgængelige afhængigt af behovet.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Min organisation har oprettet gemte visninger i Dynamics 365 Human Resources for at forbedre anvendeligheden af brugergrænsefladen. Vil de gemte visninger blive overflyttet automatisk?

Ja, gemte visninger vil blive overflyttet til den nye infrastruktur.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Vi bruger Ceridian sammen med Dynamics 365 Human Resources. Vil Ceridian-integration være tilgængelig, når ændringen af infrastrukturen er fuldført? 

Integrationen med Ceridian vil blive overflyttet til Løn-API-baseret integration. Den filbaserede integration, der aktuelt findes i Dynamics 365 Human Resources, overføres ikke til Finance and Operations-infrastrukturen. Du kan finde flere oplysninger i [Introduktion til Løn-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Hvordan påvirker overflytningen tjenesteopdateringsprocessen?

Efter overflytningen vil kunderne have meget større fleksibilitet i forhold til ALM- og tjenesteopdateringer. Der vil ikke længere blive anvendt tjenesteopdateringer til Human Resources-miljøer. Tjenesten vil i stedet følge processer og funktioner for opdatering af Èn version-tjenesten. Derfor vil konfigurationsindstillinger for opdateringer være tilgængelige via LCS. Du kan finde flere oplysninger i [Oversigt over En version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Hvordan vil overflytningen påvirke mit LCS-projekt for Dynamics 365 Human Resources?

Overflytningen til den nye infrastruktur vil flytte administrationen af dine Dynamics 365 Human Resources-miljøer til et Finance and Operations-implementeringsprojekt. Hvis overflytningen fletter Dynamics 365 Human Resources med et eksisterende Finance and Operations-miljø, flettes dit LCS-projekt for Human Resources i LCS-implementeringsprojektet for Finance and Operations-appen. Hvis du i øjeblikket kun bruger Dynamics 365 Human Resources, oprettes der et nyt LCS-implementeringsprojekt, og det eksisterende LCS-projekt for Human Resources overflyttes til det nye projekt.

Det nye projekt vil være af samme projekttype, som Finance and Operations-apps bruger. Det vil have de samme funktioner og muligheder for miljøstyring. Du kan finde flere oplysninger i [Ressourcer til Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Vi har knyttet vores opgaveregistreringer til Forretningsmodeldesigner i Human Resources. Hvordan overflyttes og flettes Forretningsmodeldesigner i LCS?

Forretningsprocesbiblioteker til LCS-projektet overflyttes til det nye LCS-projekt for Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Min organisation bruger i øjeblikket kun Dynamics 365 Human Resources. Hvilke ressourcer er tilgængelige, så vi kan få mere at vide om udviklingsfunktionerne, når ændringen i infrastrukturen er fuldført?

Der vil være udvidelsesmuligheder både til Microsoft Power Platform og Finance and Operations, som kan bruges til udvikling. Du kan finde flere oplysninger under [Udvikle og tilpasse startside](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Vi har aktiverede funktioner i Dynamics 365 Human Resources. Vil disse funktioner automatisk blive aktiveret under overflytningen?

Om en funktion aktiveres automatisk i den nye infrastruktur, bestemmes for hver enkelt funktion. Disse oplysninger vil blive medtaget i funktionsdokumentationen.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Hvad sker der med min BYOD-database under overflytningen?

Import- og eksportkonfigurationer for din egen database (BYOD) vil blive overflyttet til den nye infrastruktur.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Hvad sker der med min Azure Data Lake under overflytningen?

Enhver eksport, der aktuelt er konfigureret til Azure Data Lake Storage i Finance and Operations-apps, vedligeholder den samme konfiguration efter overflytningen.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Vi bruger i øjeblikket Dynamics AX 2012. Vil de opgraderingsværktøjer, der i øjeblikket er tilgængelige, blive brugt til opgradering af HR-modulet i AX 2012 til Dynamics 365 Human Resources?

Ja. Dynamics 365 Human Resources vil blive inkluderet i den flettede kodebase og infrastruktur for Finance and Operations-apps. En opgradering fra Dynamics AX 2012 til Dynamics 365 Human Resources vil bruge samme opgraderingssti og -værktøj, som bruges til at opgradere til den seneste version af Finance and Operations-apps.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Vi bruger Dokumenthåndtering sammen med Dynamics 365 Human Resources. Hvad sker der med dokumenterne under overflytningen?

Dokumenterne forbliver i det eksisterende dokumentlager. De skal tilknyttes på ny til miljøet i den nye infrastruktur.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Hvad sker der med de batchjob, som vi har konfigureret i Dynamics 365 Human Resources efter overflytningen?

Relevante batchjob migreres automatisk til den nye infrastruktur.

## <a name="licensing-impact"></a>Påvirkning af licenser

Denne dokumentation tilsidesætter eller erstatter ingen juridisk dokumentation, som omhandler brugsrettighederne.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Min organisation bruger Dynamics 365 Human Resources til at administrere HR-handlinger. Bliver vores licenser eller omkostninger ændret?

Kunder, der har købt Dynamics 365 Human Resources-licenser, bliver ikke påvirket. Der sker ingen licensoverflytning for disse kunder. Den supplerende SKU-enhed (Stock Keeping Unit) for sandkassen, som var specifik for Human Resources, kan ikke længere bruges. Kunderne kan i stedet vælge at købe en sankasse for Finance and Operations-apps Niveau 2 til en lidt lavere pris. Eksisterende kunder, som har købt en Human Resources-sandkasse, overflyttes til en sandkasse for Finance and Operations-apps Niveau 2 uden yderligere omkostninger.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Min organisation bruger Human Resources-modulet i Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Bliver mine licenser eller omkostninger ændret?

Eksisterende brugere af Dynamics 365-apps og brugere af selvstændige Dynamics 365 Finance, Supply Chain Management, Commerce og Project Operations kan få adgang til Human Resources som en del af disse licenser indtil februar 2025, eller indtil den aktuelle licensaftale udløber, hvad der end optræder først. Du kan vælge at flytte til Human Resources-licenser tidligere, hvis det hjælper dig med at opnå større besparelser. Fra og med februar 2025 skal alle eksisterende CSP- og EA-kunder rulle HR-modulet af og købe Human Resources-licenser for at udnytte de nye funktioner, der bliver tilføjet i Finance and Operations-appsene.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Min organisation er i gang med Dynamics 365 Finance, Supply Chain Management, Commerce eller Project Operations. Vil vi skulle købe et supplerende miljø for at understøtte fletningen af infrastrukturen?

Der kræves ingen ekstra miljøer for at understøtte ændringen af infrastrukturen.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Hvem kan jeg henvende mig til, hvis jeg har flere spørgsmål om produktlicenser?

Hvis du har spørgsmål om licenser, kan du finde flere oplysninger i [Biz Apps Hub – Priser og licenser for D365](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Hvis disse oplysninger ikke hjælper dig med dit problem, kan du åbne en anmodning med LicenseQ.
