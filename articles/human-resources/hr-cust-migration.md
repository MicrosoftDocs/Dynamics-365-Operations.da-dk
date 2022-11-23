---
title: Dynamics 365 Human Resources-kundeoverførsel til finans og drift-infrastrukturen
description: Denne artikel beskriver kundeoverførsel af Microsoft Dynamics 365 Human Resources til finans og drift-infrastrukturen.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760356"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources-kundeoverførsel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Overførsel af kunder er en "flytning" (bevægelse) af en kundedatabase til finans- og driftsinfrastrukturen. Værktøjet til automatisk overførsel bruges til formålet. Resultatet er et nyt finans- og driftsmiljø, hvor kundens Human Resources-database bruges.

## <a name="prerequisites"></a>Forudsætninger

### <a name="user-access-and-permissions"></a>Brugeradgang og -tilladelser

- Microsoft Dynamics Lifecycle Services-brugeren skal have rollen **Organisationsadministrator**.
- Brugeren skal kunne [oprette Azure DevOps-projekter](/azure/devops/organizations/projects/create-project) eller bruge et eksisterende Azure DevOps-projekt.
- Brugeren skal have adgang til at [oprette et Azure DevOps-sikkerhedstoken til personlig adgang](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) eller have et token, der er tilgængeligt til brug.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse-miljøbackup (sandkasse)

 - Valgfrit, men anbefales: Opdater det eksisterende Human Resources-sandkassemiljø ved hjælp af en kopi af Human Resources-produktionsmiljøet.
 - Opret et nyt Dataverse-miljø ved hjælp af Power Platform Administration.
 - Kopiér det eksisterende Dataverse-miljø, som er sammenkædet med den enkeltstående Human Resources-app, til det miljø, du oprettede i forrige trin.

> [!NOTE]
> Når du tilføjer en database, skal du sikre dig, at indstillingen **Aktivér Dynamics 365-apps** er angivet til **Ja**. Du kan finde detaljerede oplysninger i [Forberede et Power Platform-miljø](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse-kapacitet

1. Brug siden **Oversigt** i Power Platform Administration til at kontrollere, at [Dataverse-lageret](/power-platform/admin/finance-operations-storage-capacity) har tilstrækkelig ledig kapacitet til miljøkopien.
2. Hvis der ikke er tilstrækkelig ledig kapacitet, kan du bruge [vejledningen til at frigøre lagerplads](/power-platform/admin/free-storage-space) til at reducere det samlede forbrug. Kunder kan også [tilføje yderligere lagerkapacitet](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Kundeoverførselsproces

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Oprette et Lifecycle Services-projekt til Human Resources-overførsel

Det første trin er at oprette et nyt projekt til implementering af finans og drift i Lifecycle Services. Kunden får et eksisterende Lifecycle Services-projekt i Human Resources. De eksisterende Human Resources-miljøer overføres til det nye implementeringsprojekt for finans og drift.

Hvis du vil oprette et nyt projekt, skal du følge disse trin.

1. Log på Lifecycle Services som den globale administrator eller den udpegede servicekontobruger.
2. Vælg **Opret/nyt (+)** på Lifecycle Services-startsiden.
3. Vælg programmer til finans og drift som produkt.
4. Vælg **Implementering** i feltet **Projektformål**.
5. Angiv et projektnavn og en beskrivelse.
6. I feltet **Brugerdefineret projekttype** skal du vælge **Microsoft Dynamics 365 Human Resources-overførsel**.
7. Markér afkrydsningsfeltet for at acceptere vilkår og betingelser.
8. Vælg **Opret**.

Når du har oprettet et nyt Lifecycle Services-projekt, skal du følge disse trin for at konfigurere det.

1. Vælg **Projektonboarding** for at fuldføre projektonboarding. Du kan finde flere oplysninger under [Projekt-onboarding](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Vælg det samme område som dine aktuelle miljøer. Dette valg påvirker ikke overførslen.
    - For ældre systemer skal du vælge **Andet**.

2. Fuldfør projektindstillingerne. Som en del af dette trin skal du konfigurere SharePoint-onlinebiblioteket, Azure DevOps og Azure-forbindelser, hvis det er nødvendigt. Yderligere oplysninger finder du i [Brugervejledning til Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Kunder kan bruge et eksisterende Azure DevOps-projekt og det tilknyttede sikkerhedstoken til personlig adgang. Hvis der bruges et eksisterende projekt, er de konfigurationer, der er knyttet til projektet, automatisk tilgængelige og kan gennemses for nøjagtighed.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Overføre et Human Resources-sandkassemiljø

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Forberede overførsel til sandkassemiljøet

Når der er oprettet et nyt Lifecycle Services-projekt, og processen til onboarding af projektet er fuldført, er du klar til at overføre det første miljø. Før du starter denne proces, anbefales det, at du opdaterer det sandboksmiljø, du vil overføre fra produktionsmiljøet, i den enkeltstående infrastruktur.

#### <a name="prepare-a-power-platform-environment"></a>Klargøre et Power Platform-miljø

> [!NOTE]
> Dette trin gælder kun for overførsel af sandkassemiljøet. Når du overfører produktionsmiljøet, overføres det eksisterende Power Platform-administrationsmiljø, der er tilknyttet produktionsmiljøet. Når du tilføjer en database, skal du sikre dig, at knappen **Aktivér Dynamics 365-apps** er angivet til **Ja**. 

- I Power Platform Administration skal du [oprette et miljø med en database](/power-platform/admin/create-environment#create-an-environment-with-a-database), der skal bruges til sandkasseoverførsel, eller vælge et eksisterende miljø.
- [Kopiér et miljø](/power-platform/admin/copy-environment) for at opdatere det Power Platform-miljø, der bruges til tilknytning.

#### <a name="migrate-the-sandbox-environment"></a>Overføre sandkassemiljøet

1. Log på Lifecycle Services som den globale administrator eller den udpegede servicekontobruger.

    > [!NOTE]
    > Vi anbefaler, at du bruger en navngivet brugerkonto. Den bruger, som er logget på, skal have sikkerhedsrollen **Miljøadministrator** eller **Projektejer** i det enkeltstående Human Resources Lifecycle Services-projekt.

2. Åbn det nyoprettede Human Resources-overførselsprojekt.
3. Gennemgå og fuldfør de relevante faser i overførselsmetoden og projektonboarding.
4. I ruden **Standard: Standardgodkendelsestest** på projektdashboardet skal du vælge **Overfør HR**.
5. I ruden **Vælg miljø til overførsel** skal du vælge det relevante Lifecycle Services-projekt og det oprindelige Human Resources-miljø (fra dit enkeltstående Human Resources-kildeprogram).
6. Aktivér **Knyt til nyt Power Platform-miljø**, og vælg det relevante Power Platform-miljø. Vælg derefter **Næste**.
7. Udfyld guiden **Installationsindstillinger (finans og drift – sandkasse)** for at bekræfte detaljer og kundetilslutning, og vælg derefter **Installer**.

I miljøtilstanden vises status. Staten ændres fra **Indlæser** til **Installerer** til **Installeret**.

> [!NOTE]
> Produktionsruden er først tilgængelig, når checklisten til go-live-projektparathed er fuldført. Du kan finde flere oplysninger i [Klargøring til go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Overvejelser og antagelser

Der findes et Human Resources-sandkassemiljø i et Lifecycle Services-projekt på den lejer, der har følgende karakteristika:

- Human Resources-sandkassemiljøet er ikke kædet sammen med et eksisterende flettet miljø. Der kan kun ske én overførsel ad gangen for et givet Human Resources-miljø.
- Antallet af sandkassemiljøer, der er tilladt ad gangen, er baseret på Human Resources-licens. Hvis der er købt tilstrækkelig licens til lejeren, vises der flere sandkassemiljøer i ruden **Miljøer** til projektet.
- Overførsler skal ske til miljøer af samme type. Det vil sige, at der kun kan foretages overførsel fra sandkasse til sandkasse eller produktion til produktion.

    > [!NOTE]
    > Det er kun Human Resources-miljøtyper, der tages i betragtning, når produktionens eller sandkassens status bestemmes. Hvis miljøet er kategoriseret forkert (dvs. et produktionsmiljø er markeret som et sandkassemiljø, eller et sandkassemiljø er markeret som et produktionsmiljø), skal du kontakte Support.

- Hvis overførslen ikke lykkes, vises en fejlfejlmeddelelse, og knappen **Slet** bliver tilgængelig. Brug denne knap til at slette den mislykkede overførsel. Du kan derefter overføre miljøet igen.

#### <a name="validate-the-sandbox-migration"></a>Validere sandkasseoverførslen

Når overførselsprocessen for sandkassen er fuldført, skal du oprette en detaljeret testplan, der skal kontrollere og godkende alle forretningsprocesser.

Før du begynder at teste, skal du validere følgende oplysninger:

- Bekræft, at det overførte miljø er tilgængeligt på den URL-adresse, der er genereret.
- Bekræft, at brugere har adgang til den overførte sandkasse.
- Bekræft, at Dataverse-miljøet, der er knyttet til det overførte sandboksmiljø, er tilgængeligt.
- Kontrollér forskellige data for at bekræfte, at de nyeste data er tilgængelige.
- Fuldfør de kritiske forretningsprocesser til validering.
- Bekræft, at dine sikkerhedspolitikker er gældende.
- Bekræft, at batchjob udløses som forventet.

Du har ikke adgang fra fjernskrivebord til den overførte sandkasse. Du kan bruge funktioner og værktøjer til selvbetjening til at udføre følgende handlinger for dine sandkassemiljøer på Niveau 2+:

- Få adgang til [Azure SQL-databasen](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Få adgang til [logfiler](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Brug [perfmon-værktøjer](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Slå [Vedligeholdelsestilstand til/fra](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Genstart [tjenester](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Konfigurer [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Du kan finde flere oplysninger under [Ofte stillede spørgsmål om selvbetjeningsinstallation](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Overføre et Human Resources-produktionsmiljø

Når du er færdig med at overføre og validere et sandboksmiljø, skal du følge disse trin for at overføre produktionsmiljøet.

#### <a name="prerequisites"></a>Forudsætninger

- Abonnementsestimator skal være fuldført.
- [Parathedsvurderingen](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) for udgivelse skal være fuldført.

#### <a name="migrate-the-production-environment"></a>Overføre produktionsmiljøet

1. Log på Lifecycle Services som den globale administrator eller den udpegede servicekontobruger.

    > [!NOTE]
    > Vi anbefaler, at du bruger en navngivet brugerkonto. Den bruger, som er logget på, skal have sikkerhedsrollen **Miljøadministrator** eller **Projektejer** i Lifecycle Services-projektet.

2. Åbn det nye Human Resources-overførselsprojekt.
3. Gennemgå og fuldfør de relevante faser i overførselsmetoden og projektonboarding.
4. I ruden **Produktion** på projektdashboardet skal du vælge **Overfør HR**.
5. I ruden **Vælg miljø til overførsel** skal du vælge det relevante Lifecycle Services-projekt og det oprindelige Human Resources-miljø (fra dit enkeltstående Human Resources-kildeprogram). Vælg derefter **Næste**.
6. Udfyld guiden **Installationsindstillinger (finans og drift – sandkasse)** for at bekræfte detaljer og kundetilslutning, og vælg derefter **Installer**.

I miljøtilstanden vises installationsstatus. Staten ændres fra **Indlæser** til **Installerer** til **Installeret**.

#### <a name="post-migration-considerations"></a>Overvejelser efter overførsel

- Anvend de seneste [kvalitetsopdateringer](/fin-ops-core/fin-ops/get-started/quality-updates) på dine miljøer.
- Hvis du bruger [virtuelle tabeller](hr-admin-integration-common-data-service-virtual-entities.md), skal du konfigurere slutpunkterne igen.
- Konfigurer integration med dobbeltskrivning igen. Evaluer, hvilke enheder der skal aktiveres.
- Overvej at bruge virtuelle tabeller som erstatning for integration af dobbeltskrivning.

#### <a name="dual-write-integration"></a>Integration med dobbeltskrivning

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Konfigurere Microsoft Power Platform-integration med dobbeltskrivning

1. Gå til Power Platform Administration, og vælg **Miljøer** i venstre navigation.
2. Vælg det tidligere kopierede/opdaterede miljø, og bekræft, at status er **Klar**.
3. Gå til Lifecycle Services, og bekræft, at status for overførselsprojektet er **Installeret**.
4. I det overførte miljø skal du vælge **Alle detaljer** for at gennemse flere detaljer og [konfigurere et dobbeltskrivningsprogram](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. I ruden **Konfiguration af program til dobbeltskrivning** skal du markere afkrydsningsfeltet for at acceptere at tilknytte og synkronisere data mellem databaser og derefter vælge **Konfigurer**.
6. Når du får vist en meddelelsesboks for en vellykket konfiguration af dobbeltskrivning, skal du vælge **OK**.
7. Du kan overvåge statussen for konfigurationen i detaljerne.
8. Når konfigurationen er fuldført, skal du vælge **Link til Power Platform-miljø** for at synkronisere de tilgængelige dataenheder.
9. Når statussen angiver, at der er tilknyttet miljøer, skal du gå til Power Platform Administration for at gennemse og vælge de relevante dataenheder.
10. Vælg **Dynamics 365-apps \> Ressourcer** i ruden til venstre.
11. Bekræft, at statussen for Human Resources-appen til dobbeltskrivning er **Aktiveret**.
12. Vælg Human Resources-appen til dobbeltskrivning, og vælg derefter **Installer**.
13. Vælg det relevante miljø, som pakken skal installeres i, i ruden **Installer Dynamics 365 Human Resources-app til dobbeltskrivning**.
14. Markér afkrydsningsfeltet for at acceptere servicebetingelserne, og vælg derefter **Installer**.
15. I Dynamics 365-appmiljøet er statussen **Installerer**, mens installationen er i gang. Den opdateres til **Installeret**, når installationen er fuldført.

##### <a name="review-and-apply-a-dual-write-solution"></a>Gennemse og anvende en løsning til dobbeltskrivning

1. Gå i det nye finans- og driftsmiljø til **Datastyring \> Dobbeltskrivning**.
2. Vælg **Anvend løsning**.
3. I ruden skal du vælge **Installerede Dynamics-løsninger**, **Enhedstilknytninger for programkerne til dobbeltskrivning** og **Dynamics 365 Human Resources-tilknytninger**. Vælg derefter **Anvend**. Der vises en meddelelse om, at løsningen er anvendt. Når løsningen er anvendt korrekt, vises alle de tilgængelige tabeltilknytninger.
4. Gennemse de tilgængelige tabeltilknytninger for at vælge og køre integrationen ved hjælp af dobbeltskrivning.
5. Når du kører dobbeltskrivningsintegration for første gang for tabeltilknytninger, skal du markere afkrydsningsfeltet **Første synkronisering**. Hvis der findes en eksisterende integration fra Human Resources-kildemiljøet, behøver du ikke at markere afkrydsningsfeltet **Første synkronisering**, når du kører integrationen for tabeltilknytninger.

#### <a name="recommended-practices"></a>Anbefalede fremgangsmåder

I dette afsnit skitseres anbefalingerne for overførsel fra den enkeltstående infrastruktur til den økonomiske og driftsmæssige infrastruktur.

- Det anbefales, at du arbejder sammen med din Microsoft Dynamics-partner for at få hjælp til overførsel af Human Resources-miljøet.
- Planlæg det relevante tidspunkt for test af fuld brugeraccept (UAT) i det overførte sandkassemiljø.
- Planlæg og dokumentér de detaljerede trin til overførsel af integration til det overførte miljø.
- Opret en detaljeret checkliste for at skitsere overgangsprocessen for overførslen.
- Planlæg en passende mængde nedetid for virksomheden, mens du foretager overførslen.
- Det anbefales stærkt, at FastTrack-kvalificerede kunder samarbejder med deres arkitekt til FastTrack-løsningen, så de kan få hjælp til overførselsprocessen.
- Det anbefales, at du opdaterer dit sandkassemiljø i den enkeltstående infrastruktur, før du laver den første overførsel. Denne opdatering skal omfatte det Dataverse-miljø, der er forbundet med det sandkassemiljø, du planlægger at overføre til.
- Det anbefales, at du bruger en servicekonto, når du installerer, overfører og opretter dit Lifecycle Services-projekt.
- Planlæg at opgradere sandkassemiljøet til UAT-validering på den seneste generelt tilgængelige version. Du kan finde flere oplysninger under [overvejelser](hr-infrastructure-merge.md#considerations).
