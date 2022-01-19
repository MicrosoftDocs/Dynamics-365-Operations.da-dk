---
title: Servicebeskrivelse af Finance and Operations-apps
description: Dette emne indeholder servicebeskrivelsen til Finance and Operations-apps.
author: tomhig
ms.date: 01/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 85f82a863f0bde4c0414760fa2477651242538f2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952360"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Servicebeskrivelse af Finance and Operations-apps

[!include[banner](../includes/banner.md)]

Finance and Operations-apps er ERP-software (Enterprise Resource Planning)-software som en tjeneste (SaaS)-tilbud, der er baseret på og til [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Tjenesten Finance and Operations giver organisationer adgang til ERP-funktioner, der understøtter deres entydige behov, og som hjælper dem med at tilpasse sig ændringer i virksomhedsmiljøer, uden at de kræver, at de administrerer infrastrukturen. Finance and Operations-apps kan omfatte et eller flere af følgende løsningsområder:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Sammen med [business intelligence](/power-bi/fundamentals/power-bi-service-overview), [infrastruktur](https://azure.microsoft.com/global-infrastructure/), [beregn](/azure/service-fabric/service-fabric-overview) og [databasetjenester](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) giver disse apps organisationer mulighed for at køre branchespecifikke og driftsmæssige forretningsprocesser. Kunder, der understøttes af deres implementeringspartner, bestemmer konfigurationen af den forretningsprogramlogik, der passer bedst sammen med deres entydige forretningsprocesser. Funktionalitet og forretningsprocesser kan udvides eller udvides via en eller en kombination af følgende løsninger:

- Indbygget [tilpasningserfaring](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)-værktøjer
- [Visual Studio](https://visualstudio.microsoft.com)–baseret [Finance and Operations softwareudviklingssæt (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) og [Azure DevOps build automation](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Uafhængige softwareleverandørløsninger fra [AppSource](https://appsource.microsoft.com/partners)

Baseret på behov vælger kunderne deres løsningsmetode. De arbejder sammen med deres implementeringspartner for at definere, udvikle og teste deres løsning ved hjælp af de værktøjer og bedste fremgangsmåder, der findes i [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Der findes fire almindelige scenarier:

- Konfiguration Finance and Operations af standardapps "out of the box" (ingen udvidelser)
- Finance and Operations-konfiguration af apps, der omfatter en eller flere isv-løsninger
- Finance and Operations-konfiguration af apps, der omfatter en eller flere kundespecifikke udvidelser
- Finance and Operations-konfiguration af apps, herunder en kombination af kundespecifikke udvidelser og en eller flere løsninger fra isv

Organisationer kan matche deres firmavækst ved nemt at tilføje brugere og forretningsprocesser via en simpel, transparent abonnementsmodel. Du kan finde flere oplysninger i [licensvejledningen til Dynamics 365](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Driftsmodel

Driftsmodellen for Finance and Operations-apps definerer specifikke roller og ansvarsområder for kunden, implementeringspartneren og Microsoft i hele tjenestens livscyklus. Yderligere oplysninger finder du i [Operationer i skyen og servicering](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Brugerdefinerede aktiviteter

Kunder arbejder sammen med deres partner og [Microsoft FastTrack](/dynamics365/fasttrack/) efter [Dynamics 365-implementeringsvejledningen](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), [Success by Design](/dynamics365/fasttrack/success-by-design-overview)-skabeloner og de værktøjer og best practice-skabeloner, der findes i [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) til implementering af deres løsning. Af almindelige aktiviteter kan nævnes:

- Brugeridentitet og sikkerhedsstyring
- Definere, udvikle og betjene forretningsprocesser
- Definere, udvikle, teste og operere udvidelser
- Overvåge og administrere installationer uden for produktion
- Administrere programopdateringer og validere udvidelser
- Administrere ISV-løsninger og integration af 3 fejlparter

### <a name="microsoft-responsibilities"></a>Microsoft-ansvarsområder

Microsoft administrerer Finance and Operations-tjenesten ved at implementere, overvåge og servicere kundesandkasse og produktionsmiljøer i abonnementet Microsoft. Denne administration omfatter tildeling af den nødvendige systeminfrastruktur til kørsel af tjenesten og proaktiv kommunikation med kunderne om tjenestens tilstand. Ansvarsområder omfatter:

**Infrastrukturstyring**
- Sikkerhed og isolation
- Operativsystemer og virtualisering
- Servere, lagre og netværke
- Datacenterkraft, netværk, afkøling

**Styring af applikationsplatform**
- Overvågning og notifikation af 24/7-program
- Diagnosticering, platformopdateringer, rettelser, serviceopdateringer
- Programrute, belastningsjustering, lokationsreplikering
- Klargøring og styring af miljø
- Databasestyring, høj tilgængelighed (HA)/it-katastrofeberedskab (DR), skala, handlinger
- Beregn implementering, skaler op og ned

## <a name="system-configuration"></a>Systemkonfiguration

Finance and Operations-apps skaleres i henhold til transaktionens volumen og brugerbelastningen. Hver enkelt implementering af kunder resulterer i en entydig løsning, der består af følgende elementer:

- **Datasammensætning** – Et entydigt sæt parametre, der styrer funktionaliteten, organisationens layout, masterdatastrukturen (f.eks. økonomiske dimensioner og lagerdimensioner) og granulariteten af sporing af posteringer.
- **Udvidelse og konfiguration** – Udvidelsesmekanismer, der bruger kodeudvidelser, ISV-løsninger og entydige konfigurationer, der omfatter arbejdsgange, integrationer og rapportkonfigurationer.
- **Brugsmønstre** – En entydig kombination af onlinebrug og batchbrug sammen med muligheden for at integrere med upstream- og downstream-systemer for samlet dataflow og muligheden for at skelne mellem forskellige oplysninger baseret på de oplysninger, kunderne bruger i deres forretningsprocesser.

Microsoft konfigurerer produktionsmiljøer, der er dimensioneret til håndtering af transaktionsmængder og bruger samtidighed. Microsoft er ansvarlig for følgende opgaver:

- Korrekt fordeling af ressourcerne i produktionsmiljøer på baggrund af kundens profiloplysninger i [vurderingen til LCS-abonnementet](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Løbende overvågning og forbedring af servicetilgængelighed for produktionsmiljøer
- Analysere og fejlfinde problemer med systemets ydeevne med Finance and Operations-apps

For at sikre, at en implementering er konfigureret til høj performance, skal kunder udføre disse opgaver:

- Giver nøjagtige brugsoplysninger om Finance and Operations-implementeringen i [LCS-abonnementsvurderingen](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Opbyg og test udvidelser til performance og skala.
- Test datakonfigurationerne korrekt for performance.
- Sikre skalerbarhed ved at udføre [performancetest](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018), før de går i gang.

## <a name="onboarding-and-implementation"></a>Onboarde og implementere

I følgende tabel vises typiske start- og implementeringshændelser.

| Anmodning | Forventet Microsoft-handling | Forventet handling for en kunde/implementeringspartner |
|---|---|---|
| Første tilbudskøb | Der oprettes et LCS-projekt efter købet af tilbuddet baseret på en hændelse, der udløses af kunden. | Gå gennem Enterprise Agreement (EA ) eller Cloud Solution Provider (CSP) [forretningsprocessen](before-you-buy.md). Partneren opretter en lejer for kunden, hvis det er relevant. |
| Tilføjelseskøb | Giv kunden adgang til det tilføjelsesprogrammet, der er valgt under implementeringen. | Ikke anvendelig |
| Planlægning og analyse af implementering | Indeholder relevante værktøjer i LCS, f.eks. [Forretningsprocesmodel (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) og [samkørsel med Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Skal du planlægge projekter, konfigurere Azure DevOps, fuldføre systemadministratorer og konfigurere admin-konti. |

Yderligere oplysninger finder du i [Onboarding et implementeringsprojekt](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalisering

Finance and Operations-apps vises fra flere Azure-områder over hele verden. Finance and Operations-apps indeholder funktioner, der understøtter forskellige lande/områder og modersmål. Du kan finde flere oplysninger i [Funktioner for localization og regulatory features](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Lande-/områdespecifikke overvejelser

- Kunder i regulerede industri- eller erhvervsorganisationer, der gør forretning med enheder i Frankrig, der kræver lokal databopæl, skal gennemgå [Finance and Operations i Frankrig](../../dev-itpro/deployment/france-local-deployment.md).
- Kunder, der har operationer i Kina, bør gennemgå [Azures Kina-strategiplan](/azure/china/) og [Finance and Operations, der drives af 21Vianet i Kina](../../dev-itpro/deployment/china-local-deployment.md).
- Kunder, der har operationer i Rusland, bør gennemse [russisk lov om tilpasning af personlige data](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Generel forordning om databeskyttelse (GDPR)

I forbindelse med Finance and Operations-apps fungerer Microsoft som en processor. Som dataprocessor indeholder Finance and Operations processer og funktioner, der kan hjælpe kunderne med at overholde GDPR-forpligtelser som datacontrollere. Du kan få flere oplysninger under [GDPR – oversigt](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Miljø og datastyring

Dette afsnit indeholder en beskrivelse af nogle af de typiske hændelser i miljøet og datastyringen, der forekommer i tjenesten.

### <a name="environment-and-data-management-events-for-production-instances"></a>Hændelser i miljø- og datastyring for produktionsforekomster

LCS indeholder [værktøjer til selvbetjening](../../dev-itpro/deployment/infrastructure-stack.md) og [databasebevægelser](../../dev-itpro/database/dbmovement-operations.md), der bruges til at udføre miljø- og datastyringsopgaver. Her er nogle eksempler:

**Hændelse:** [Anmode om en produktionsforekomst](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Fuldfør [Go-Live-checklisten](../imp-lifecycle/prepare-go-live.md), og send den til Microsoft [FastTrack-teamet](/dynamics365/fasttrack/).
- Udfyld [vurderingen for LCS-abonnementet](../../dev-itpro/lifecycle-services/subscription-estimator.md), før du anmoder om en produktionsforekomst.
- Fuldfør alle de implementeringsopgaver, der er angivet i [LCS-metoden](../../dev-itpro/lifecycle-services/create-methodology.md).

**Hændelse:** [Kopiere en sandkassedatabase til en produktionsforekomst](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Udføres for en go-live eller en faktisk go-live-overskæring.

**Hændelse:** [Vedligeholdelsestilstand](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Aktiver vedligeholdelsestilstand i LCS.
2. Fuldfør den nødvendige vedligeholdelse.
3. Deaktiver vedligeholdelsestilstand i LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Hændelser i miljø- og datastyring for ikke-produktionsforekomster

LCS indeholder [værktøjer til selvbetjening](../../dev-itpro/deployment/infrastructure-stack.md) og [databasebevægelser](../../dev-itpro/database/dbmovement-operations.md), der bruges til at udføre miljø- og datastyringsopgaver. Her er nogle eksempler:

**Hændelse:** [Implementere en ny sandkasseforekomst](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Kontroller, at alle påkrævede forekomster er [planlagt](../imp-lifecycle/environment-planning.md), og at de relevante tillægstilbud er købt.
- Kør installationsprocessen i LCS.
- Fuldfør alle de implementeringsopgaver, der er angivet i LCS-kontrollisten.
    
>[!NOTE]
>Et udviklingsmiljø for sandkasser er en virtuel maskine (VM), der [implementeres på kundens Azure-abonnement](../../dev-itpro/dev-tools/access-instances.md) og administreres af kunden.

**Hændelse:** [Kopiere en gylden konfigurationsdatabase fra sandkasse til produktion](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Udføres for en go-live eller en faktisk go-live-overskæring.

**Hændelse:** [Gendanne en tidsbaseret sikkerhedskopi af en produktion til en forekomst, der ikke er en produktionsforekomst](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Kør indstillingen [Opdater database](../../dev-itpro/database/database-refresh.md) i LCS.
- Efterkopier: Slet eller sløre følsomme data via scripts, juster miljøspecifikke programkonfigurationer (f.eks. integrationsslutpunkter) og aktiver eller tilføj brugere. Bemærk, at disse ændringer foretages ved at anvende en [datapakke](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Hændelse:** [Tidsbaseret databasegendannelse for ikke-produktionsforekomster](../../dev-itpro/database/database-point-in-time-restore.md)

- Accepter, at processen ikke kan fortrydes.
- Kør tidsgendannelseshandlingen i LCS.

**Hændelse:** Kopiere en lag 2-sandkassedatabase til en udviklingssandkasse til fejlfinding og [fejlfinding](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Kør databaseeksporthandlingen i LCS i trin 2-sandkassemiljøet.
- Importer og opdater databasen i udviklingsmiljøet.

## <a name="data-backup-and-retention"></a>Sikkerhedskopiering og lagring af data

Databaser til Finance and Operations-miljøer i SaaS-abonnementet er beskyttede af automatiske sikkerhedskopier. I forbindelse med produktionsmiljøer tilbageholdes automatiske sikkerhedskopier i 28 dage, medmindre Microsoft tilbageføres. I forbindelse med sandbox-miljøer (Tier 2+)-miljøer gemmes de i syv dage. En tilbageførsel af produktionsmiljøet kan ske, hvis der opstår fejl under en planlagt vedligeholdelsesopdatering.

Yderligere oplysninger om automatiske sikkerhedskopier finder du i [Automated backups - Azure SQL Database &SQL Managed Instance](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Serviceaktivitetsansvar

I følgende tabel beskrives nogle af de typiske scenarier og aktiviteter for tjenesten. Den angiver også, om Microsoft, kunden eller både Microsoft og kunden er efter behov for aktiviteterne.

| Aktivitet | Microsofts ansvar | Kundens ansvar |
|---|---|---|
| **Klargør oprindelige lejere** | | |
| Tilpas størrelsen på den forventede belastning i LCS ved hjælp af værktøjet Abonnementsestimering, og anmode om, at der klargøres bestemte miljøer. | | X |
| Klargøre alle produktionsforekomster og ikke-produktionsforekomster. | X | |
| Validere installerede produktionsforekomster og ikke-produktionsforekomster. | | X |
| **Tjenesteopdateringer** | |
| Anvend serviceopdateringer til angivne forekomster uden for produktion og produktion. | X | |
| Anvend manuelle serviceopdateringer fra LCS på sandboksforekomster. Definer, udvikle, teste opdateringen og levere kodeopdateringspakken tilbage til LCS. | | X |
| Anmod om, og planlæg, at der skal anvendes forlængelsesopdateringer på produktionsforekomsten. | | X |
| Opret en kode og sikkerhedskopiering af data til produktionsforekomsten, før der anvendes opdateringer. | X | |
| Hvis der opstår fejl, skal du tilbagerulle produktionsforekomsten til koden og datasikkerhedskopien. | X | |
| **Datastyring (sikkerhedskopier, gendan og opdater)** | | |
| Sikkerhedskopier databasen. | X | |
| Fastlæg, at der er høj tilgængelighed og en plan for genoprettelse efter planen for udlæg. | X | |
| Overvåge ydeevnen for databasen med produktionsforekomster. | X | |
| Indstil ydeevnen for databasen med produktionsforekomster. | X | |
| Udfør tidsopdatering af en database med produktionsforekomster til en forekomst, som ikke er en produktionsforekomst. | | X |
| **Opdatere infrastrukturen** | | |
| Planlæg regelmæssige opdateringer af infrastrukturen. | X | |
| **Op- og nedskalering (brugere, lagring og forekomster)** | | |
| Køb yderligere brugere og tilføjelser, der ikke er produktionsomkostninger på. | | X |
| Opdater brugsændringerne i værktøjet til estimator for LCS-abonnement. | | X |
| Rapportér eventuelle væsentlige problemer med ydeevnen, der påvirker brugen af tjenesten. | | X |
| Administrer proaktivt de ressourcer, der kræves til den relevante service. | X | |
| Undersøg og fejlfinde hændelser. | X | |
| **Sikkerhed (brugeradgang)** | | |
| Giv brugeren adgang til tjenesten. | | X |
| Giver LCS-projektadgang til administration og operation af forekomster, der blev implementeret via LCS. | | X |
| **Overvåge produktionsforekomster** | | |
| Overvåge produktionsforekomster døgnet rundt. | X | |
| Giv kunden besked proaktivt om hændelser, der involverer produktionsforekomsten. | X | |
| **Administrere og overvåge forekomster, der ikke er produktionsforekomster** | | |
| Administrer forekomster, der ikke er produktionsforekomster, ved hjælp af LCS. | | X |
| Overvåge ikke-produktionsforekomster. | | X |

## <a name="service-update-strategy"></a>Strategi for tjenesteopdatering

I overensstemmelse med [politikken for softwarelivscyklus](../../dev-itpro/migration-upgrade/versions-update-policy.md), Finance and Operations-apps følger Microsofts [politik for levetidscyklus](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), som dækker produkter, der løbende serviceret og understøttes. 

Microsoft udgiver otte tjenesteopdateringer til Finance and Operations-apps hvert år i de følgende måneder:

- Januar
- Februar
- April
- Maj
- Juli
- August
- Oktober
- November

>[!NOTE]
>April og oktober er større udgivelsesbølger. Kunder kan midlertidigt afbryde en enkelt serviceopdatering i op til tre fortløbende opdateringscyklusser.

Du kan gennemse flere oplysninger under følgende emner:

- [Oversigt over One Version-tjenesteopdateringer](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Konfigurere serviceopdateringer i LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Afbryde serviceopdateringer midlertidigt i LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Få besked om serviceopdateringer i LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regression af testværktøjer til validering af serviceopdateringer](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 udløsning og udgivelsesbølger](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Sikkerhed og administrativ adgang

Administrativ adgang til et Finance and Operations-produktionsmiljø kontrolleres og registreres nøje. Kundedata håndteres i overensstemmelse med vilkårene [for Microsoft Online Services](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Administratoradgang for kunder

Kundens administrator har adgang til produktionsforekomster eller forekomster, der ikke er produktionsforekomster, som beskrevet i følgende tabel:

| Miljøtype | Formål | Niveau for kundeadgang |
|---|---|---|
| **Ikke-produktion**<br>Trin 1-sandkasse | Et ikke-produktionsmiljø, som kunder installerer til udviklings-, demonstrations- eller kursusformål. | En Tier 1-sandkasse (kaldes også et miljø med skyen) er et kundestyret VM, der implementeres på kundens Azure-abonnement fra LCS. Da kundens Azure-abonnement er en VM-del, har kunden fuld administrativ adgang til miljøet via Fjernskrivebord. |
| **Ikke-produktion**<br>Trin 2 (eller højere) sandkasse | Et ikke-produktionsmiljø, som kunderne implementerer til test af brugeraccept, integrationstest, uddannelse, stadieindsættelse eller andre scenarier før produktion. | Trin 2 og højere sandkasser implementeres i Finance and Operations-abonnementet SaaS. Der gives adgang til Azure SQL-databaser, der er tilknyttet ikke-produktionsmiljøet, via [just-in-time-adgang](../../dev-itpro/database/database-just-in-time-jit-access.md). Adgangen til fjernskrivebord er ikke tilgængelig. |
| **Produktion** | Et produktionsmiljø implementeres, når projektet [er klar til første live](/imp-lifecycle/environment-planning.md#production-system-readiness). | Produktionsmiljøer implementeres på SaaS-abonnementet. Al adgang er via browser, tjenesteslutpunkter eller LCS. |

### <a name="microsoft-administrative-access"></a>Administratoradgang til Microsoft

Følgende tabel viser de forskellige adgangsniveauer for forskellige Microsoft-administratorer:

| Administrator | Debitordato |
|---|---|
| Team med operationssvar<br>(Begrænset til kun nøglemedarbejdere) | Der gives adgang via en supportbillet. Adgangen overvåges og begrænses til varigheden af supportaktiviteten. |
| Microsoft Customer Support Services (CSS) | Ingen direkte adgang. Kunden kan bruge skærmdeling til at arbejde med supportmedarbejdere for at fejlfinde problemer. |
| Teknisk | Ingen direkte adgang. Teamet med operationssvar kan bruge skærmdeling til at arbejde med teknikere til fejlfinding af problemer. |
| Andre i Microsoft | Ingen adgang. |

## <a name="monitoring"></a>Overvågning

Microsoft har fået hjælp i et omfattende værktøjssæt til at overvåge og diagnosticere kunders produktionsforekomster. Microsoft overvåger kundernes produktionsmiljøer 24 timer om dagen 7 dage om ugen. Yderligere oplysninger finder du i [Understøttelse og overvågning af produktion](../imp-lifecycle/production-support-monitoring.md).

| Microsoft-ansvarsområder | Kundeansvarsområder |
|---|---|
| <ul><li>Overvåge tilgængeligheden af tjenesten.</li><li>Overvåge og modtage påmindelser løbende via metriske sundhedsværdier og computerskærme for kritiske komponenter som F.eks. Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce og Management Reporter.</li><li>Overvåge ydeevnen, som forårsages af infrastrukturelle tjenester (f.eks. Azure Active Directory \[Azure AD\] og Azure SQL).</li><li>Hvis Microsoft beslutter, at en enkelt proces eller et enkelt batchjob forårsager aberrationer, afsluttes den pågældende proces eller det pågældende job, når du har kommunikeret med kunden.</li></ul> | <ul><li>Overvåge ændringer af programkonfigurationer og udvidelser, der kan forårsage funktions- og ydeevneproblemer.</li><li>Programfejl skal være nyttige ved brug af overvågningsværktøjerne. Brug disse værktøjer til at diagnose af brugerrapporterede performance-afvigelser.</li><li>Informer Microsoft om, at der forventes belastning af systemet efter forventet spidsbelastning.</li><li>Hvis den gældende tjeneste ikke er tilgængelig i produktionsforekomsten, kan kunden bruge LCS til at rapportere [et produktionssvigt](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Når supportanmodninger sendes online via LCS, giver kunder Microsoft mulighed for at levere hurtig og dyb teknisk ekspertise på den mest effektive måde. Selvom der findes en telefonindstilling, bør den kun bruges, hvis onlineindstillingen ikke er tilgængelig. Du kan finde flere oplysninger under [Indstillinger for telefontjeneste](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Hændelsesstyring

Microsoft reagerer på og løser hændelser baseret på alvorsgrader. Microsofts alvorsgrader kan ændres under den første vurdering af hændelsen, og efterhånden som flere oplysninger om virkningen og området bliver tilgængelige. Hvis hændelsen reduceres, forbliver alvorligheden af hændelsen uændret.

Du kan finde flere oplysninger om alvorsgrader i denne [alvorsgradstabel](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Forretningskontinuitet i forbindelse med høj tilgængelighed og genoprettelse efter naturkatastrofer 

Microsoft giver forretningskontinuitet og genoprettelse efter fejl til produktionsforekomster af Finance and Operations-apps i tilfælde af, at Azure-området dækker hele området. Yderligere oplysninger finder du i [Forretningskontinuitet og it-katastrofeberedskab](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Højt tilgængelighed** – Høj tilgængelighed-funktioner giver mulighed for at forhindre nedetid som følge af fejl i en enkelt node i et Azure-datacenter. I arkitekturen i hver tjenestes sky bruges Azure-tilgængelighedssæt til beregningslag for at forhindre enkeltpunkt-of-fejl-hændelser. Høj tilgængelighed til databaser angives via [Azure SQL HA-funktionerne](/azure/azure-sql/database/high-availability-sla).
- **it-katastrofeberedskab** – [Azure-funktioner til opkrævning af fejl](/azure/best-practices-availability-paired-regions) beskyttes hver enkelt tjeneste mod udfald, der overordnet påvirker et helt Azure-datacenter. Her er nogle af disse årsager:

    - Azure SQL Active-Replication til den primære database (business database).
    - Kopier af Azure Blob-lagring (som indeholder vedhæftede dokumenter) i andre Azure-områder.
    - Sekundær region til Azure SQL- og Azure Blob-lagrings replikeringerne.

De primære databutikker understøttes til replikering. Komponenterne til hver enkelt tjeneste, f.eks. Management Reporter og butik med enheder, bruger derfor konverterede data fra den primære database. Disse data skal genereres, når genoprettelseswebstedet er konfigureret, og tjenesten er startet. Genstande i kundekoden og lagrede data, der blev gendannet, bruges til at geninstallationen af webstedet. Ved geninstallationen kan der bruges tilstands replikering af beregningsnoderne sammen med lokaliteten andre komponenter, så de gendannede databutikker kan konfigurere det sekundære sted. Hvis ved hjælp af fejlinddrivelse bruges til at inddrive kundens produktionsforekomst, opfylder Microsoft og kunden deres ansvarsområder inden for [hændelsesstyringen](service-description.md#incident-management).

Microsofts planer og procedurer for naturkatastrofer undersøges jævnligt via SOC-revisioner (System and Organization Controls). Disse overholdelsesrevisioner er en bekræftelse af den tekniske proces og den trinvise proces i Microsofts DR, herunder Dynamics 365 Finance and Operations-apps. [Overvågningsrapporter om overholdelse af SOC](/compliance/regulatory/offering-soc-2) og alle andre overholdelsesrapporter er tilgængelige på [Microsoft Trust Center Compliance Offerings](/compliance/regulatory/offering-home).

| Microsoft-ansvarsområder | Kundeansvarsområder |
|---|---|
| Microsoft hensættelser et sekundært miljø i det azure-parrede datacenter, når den primære produktionsforekomst implementeres. Yderligere oplysninger finder du i [Forretningskontinuitet og it-katastrofeberedskab (BCDR): Azure-parrede områder](/azure/best-practices-availability-paired-regions). | None |
| Microsoft aktiverer de oplysninger om Azure SQL og Azure Blob Storage, når den primære produktionsforekomst implementeres. | None |
| Microsoft aktiverer automatisk sikkerhedskopiering af Azure SQL-databaserne. | None |
| <p>Når der opstår svigt, bestemmer Microsoft, om der skal udføres en failover for kunden, og om der vil være tab af data. Kunder kan opleve at miste data i op til 15 minutter, afhængigt af arten af og tidspunktet for afbrydelsen. | I tilfælde af tab af data kan kunden være nødt til at angive skriftlig afhændelse, for at det kan udløse en failover. |
| Når der opstår en fejl, fungerer den gældende tjeneste i begrænset tilstand. Opdateringsvedligeholdelse kan ikke udløses i failover-tilstand. | Kunden kan ikke anmode om pakkeinstallationer eller andre almindelige anmodninger om vedligeholdelse i failover-tilstand. |
| Når datacenter bliver driftsklart, vender Microsoft tilbage til produktionsforekomsten i det primære Azure-område. Normal genoptag operationer. | Kunden skal muligvis ikke logge af produktionsforekomsten i det primære Azure-område. |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operations-supporttilbud

Teknisk support er tilgængelig på markeder, hvor Finance and Operations- tjenester tilbydes. [Supporterfaringer](../../dev-itpro/lifecycle-services/lcs-support.md) findes i LCS eller Finance and Operations-apps. Her er nogle eksempler:

- [Problemsøgning](../../dev-itpro/lifecycle-services/issue-search-lcs.md) i LCS
- [Integreret teknisk support](../../dev-itpro/lifecycle-services/support-experience.md) i Finance and Operations-apps
- [Skybaseret support](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) i LCS

Microsoft tilbyder Finance and Operations-kunder tre supportplaner: Premier, Professional Direct og den support, der er inkluderet i abonnementet. Supportniveauet er forskelligt for de forskellige planer. I følgende tabel vises en sammenligning af de tre planer.

| Supportfunktion | Premier | Professional Direct | Abonnement |
|---|---|---|---|
| Ubegrænset afsendelse af pause/ret hændelse | Ja | Ja | Ja |
| 24/7 adgang via LCS | Ja | Ja | Ja |
| Svartid for hændelse | Mindre end en time | Mindre end en time | Næste arbejdsdag |
| Rådgivningstimer | Puljer anskaffes pr. aftale. | Nej | Nej |
| Dedikeret supportkontoadministrator | Ja | Nej | Nej |
| Dedikeret supporttekniker | Involveret i henhold til en separat aftale | Nej | Nej |

Du kan finde flere oplysninger under [Support-oversigt](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Proces til involvering af support

I tilfælde af hændelser, der involverer Finance and Operations-apps, sender kunder supportbilletter til Microsoft via LCS. CSS håndterer hændelserne baseret på kundens supportplan og alvorligheden af hændelsen, som angivet af CSS.

### <a name="service-level-agreement"></a>Serviceniveauaftale

Microsoft har en tilgængelighedssats på 99,9 % pr. måned for tjenesten. Hvis Microsoft ikke opnår og vedligeholder serviceniveauet for den pågældende tjeneste som beskrevet i serviceniveauaftalen, kan kunden blive berettiget til en kreditering af en del af det månedlige servicegebyrer for denne tjeneste. Yderligere oplysninger om, hvordan du starter en servicekreditering, finder du i afsnittet "Krav" i serviceniveauaftalen [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Vigtige ressourcer

- **[Center for tillid](https://www.microsoft.com/trust-center)** – Få oplysninger om, hvor dine Finance and Operations-data gemmes, samt yderligere oplysninger om procedurer for beskyttelse af personlige oplysninger, overholdelse og sikkerhedsprocedurer.
- **[Vilkår og dokumentation til licenser](https://www.microsoftvolumelicensing.com/)** – Du får hurtig adgang til vilkår, betingelser og supplerende oplysninger, der er relevante for brugen af produkter og tjenester, der er licens til via Microsofts programmer til volumenlicens.
- **[Licensbetingelser](https://www.microsoft.com/licensing/product-licensing/)** – Ressourcerne på denne side definerer vilkår og betingelser for de programmer og onlinetjenester, du køber via Microsoft erhvervslicensprogrammer.
- **[Microsoft Lifecycle Policy](/lifecycle/)** – Denne side giver konsistente og forudsigelige retningslinjer for tilgængeligheden af support i hele et produkts levetid.
- **[Licensvejledning](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Du kan bruge denne vejledning til at få mere at vide om, hvordan du licenserer Dynamics 365.
- **[Kundesupport](https://dynamics.microsoft.com/support/)** – Få brancheførende support til dine Dynamics 365-apps.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – Administrer programlivscyklussen, og gå i retning af forudsigelige, gentagelige implementeringer af høj kvalitet.
- **[Implementeringsvejledning til Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** – Implementeringsvejledning til Dynamics 365 dokumenterer timetestede Success by Design-principper og indeholder en vejledning til arkitekter, build, test og udrulning af Dynamics 365-løsninger.

## <a name="definitions"></a>Definitioner

### <a name="azure-region"></a>[Azure-region](/azure/availability-zones/az-overview#regions)

Et geografisk område, hvor der findes et eller flere Azure-datacenter. Som eksempler kan nævnes USA og Europa.

### <a name="business-process-modeler-bpm"></a>[Forretningsmodeldesigner (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Et værktøj i LCS, der hjælper med at udføre en analyse af fit-gap til en given implementering ved hjælp af forretningsprocesdefinitioner fra American Productivity & Quality Center (APQC), der understøttes i Finance and Operations-apps.

### <a name="cloud-solution-provider"></a>Udbyder af skyløsning

En partner, der er en del af Microsoft Cloud Solution Provider-programmet (CSP), og som giver kunder værditilvækst i skytjenester, support, én faktura og kundestyring i større skala.

### <a name="customer"></a>Kunde

En forretningsenhed, der forbruger Finance and Operations-apps og er repræsenteret af en lejer i Office 365.

### <a name="development-environment"></a>Udviklingsmiljø

Et ikke-produktionssandkassemiljø, der bruges til at udvikle udvidelser. Kunder implementerer dette miljø på deres eget Azure-abonnement fra LCS. Dette miljø kan også bruges til demonstrations-, kursus- eller andre testopgaver. Det kaldes også et [Trin 1 sandkasse](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Nedetid

En periode, hvor brugere ikke kan logge på eller få adgang til deres aktive lejer på grund af en fejl i den ikke-udløbne platform eller tjenesteinfrastrukturen, som Microsoft beslutter af automatiseret sundhedsovervågning og systemlogfiler. Nedetid inkluderer ikke planlagt nedetid, funktionaliteten ved tilføjelsesprogrammet Service, manglende adgang til tjenesten på grund af dine ændringer af tjenesten eller perioder, hvor skalaenhedskapaciteten overskrides.

### <a name="implementation-partner"></a>Implementeringspartner

Den partner, som kunden vælger at tilpasse, konfigurere, implementere og administrere Finance and Operations-løsningerne.

### <a name="incident"></a>Hændelse

Et problem, som kunderne oplever, når de bruger Finance and Operations-tjenesten, og som de sender en flybillet til via LCS.

### <a name="microsoft-customer-support-services-css"></a>Microsoft Customer Support Services (CSS)

Det globale Microsoft-supportteam, der er dedikeret til at levere kvalitetsservice til Finance and Operations-apps.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Den administrative portal til livscyklusstyring af Finance and Operations-apps fra prøve til implementering, til administration af efterproduktion og support. Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Ikke-produktionsforekomst

En af følgende forekomster af en tjeneste, som kunden bruger til at validere udvidelser og udføre andre udviklingsopgaver:

- **Sandkasse Trin 1** – Udviklerforekomst (kunde-tilknyttet)
- **Sandkasse Trin 2** – Standardaccept af testforekomst
- **Sandkasse Trin 3-5** – Tilføjelsessandkasser

Du kan finde flere oplysninger om Trin 2 til og med 5 i [Vælge det korrekte Trin 2-miljø eller et højere miljø](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Produktionsforekomst

Et Finance and Operations-miljø, som kunden bruger til at administrere de "live" daglige transaktioner og forretningsprocesser.

### <a name="sandbox-environment"></a>Sandkassemiljø

Et ikke-produktionsmiljø, som kunden bruger til demonstration, uddannelse, test af brugergodkendelse, validering af udvidelser og andre testopgaver.

### <a name="service"></a>Ydelse

En af de kernetjenester, der er inkluderet i Finance and Operations-apps.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Serviceniveauaftale (SLA) til Microsoft-onlinetjenester

Serviceniveauaftalen (SLA) gælder for Microsofts onlinetjenester. Du kan finde flere oplysninger under [Serviceniveauaftaler](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Tjenesteopdatering

Microsoft Finance and Operations-tjenestemiljøer på ensartet basis via serviceopdateringer. Kunder opretter deres egen serviceopdateringskalender ud fra deres forretningsbehov. Du kan finde flere oplysninger under [One Version-tjenesteopdateringer](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Den struktur, der systematisk leder en implementering gennem en række vurderinger på kritiske stadier for at sikre optimal arkitektur, sikkerhed, ydeevne og brugeroplevelse for en Dynamics 365-løsning.

### <a name="user"></a>Bruger

En enkelt person, der anvender Finance and Operations-miljøer, og som er tilknyttet en kundes lejer.
