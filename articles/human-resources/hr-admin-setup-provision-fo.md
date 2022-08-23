---
title: Klargøre Human Resources i infrastruktur til finans og drift
description: Denne artikel forklarer processen med klargøring af et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources i infrastrukturen i finans og drift.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221586"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Klargøre Human Resources i infrastruktur til finans og drift

_**Anvendes på:** Human Resources i program til finans og drift-infrastruktur_ 

> [!NOTE]
> Fra og med juli 2022 kan der ikke klargøres nye personalemiljøer på den enkeltstående infrastruktur for Personale, og der kan ikke oprettes nye Microsoft Dynamics Lifecycle Services-projekter (LCS) på den. Kunder kan udrulle Personale-miljøer på infrastrukturen i program til finans og drift.

Denne artikel forklarer processen med klargøring af et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources i infrastrukturen i finans og drift.

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være på plads, før du kan klargøre dit nye miljø:

- Du har købt Human Resources via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Dynamics 365-licens, der allerede indeholder Human Resources-serviceplanen, og du ikke kan udføre trinnene i denne artikel, kan du kontakte Support.
- Den globale administrator er logget på [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) og har oprettet et nyt Human Resources-projekt.

## <a name="provision-a-human-resources-trial-environment"></a>Klargøre et Human Resources-testmiljø

> [!NOTE]
> Fra og med april 2022 vil testmiljøerne i Human Resources ikke være tilgængelige i det enkeltstående program. Potentielle kunder, der er interesseret i at evaluere Human Resources-funktionerne i programmer til finans og drift, kan gøre dette ved hjælp af den gratis 30-dages prøve sammen med demodataene. Dynamics 365 Finance inkluderer de Human Resources-funktioner, der er hentet til finansinfrastrukturen via fletning af det enkeltstående program. Du kan finde flere oplysninger i [fletning af hr-tilbud, der giver kunder egenskaber](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Du kan finde flere oplysninger om Dynamics 365 Finance i den [trinvise vejledning](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Planlægge miljøer i Human Resources

Før du opretter dit første miljø med Human Resources, skal du planlægge miljøets behov nøje for dit projekt. Et basisabonnement på Human Resources omfatter to miljøer: et produktionsmiljø og standardgodkendelsestestet (sandkasse) miljø. Afhængigt af, hvor kompleks projektet er, kan det være nødvendigt at købe flere sandkassemiljøer for at understøtte projektaktiviteter.

Overvejelser i forbindelse med yderligere valgfri miljøer:

- **Overflytning af data** Dataoverførselsaktiviteter, så dit sandkassemiljø kan bruges til testformål i hele projektet. Et ekstra miljø gør det muligt at fortsætte dataoverflytningsaktiviteter, mens test- og konfigurationsaktiviteter finder sted samtidigt i et andet miljø.
- **Integration** – Konfigurer og test integrationer, der kan omfatte oprindelige integrationer eller brugerdefinerede integrationer, som f.eks. integration med løn, sporingssystemer for ansøgere eller benefit-systemer og -leverandører.
- **Kursus** - Du har muligvis brug for et separat miljø, der er konfigureret med et sæt kursusdata, for at medarbejderne kan bruge det nye system. 
- **Projekt i flere faser** - Du kan have brug for et yderligere miljø for at understøtte konfiguration, overflytning af data, test eller andre aktiviteter i en projektfase, der er planlagt efter projektets første start.
- **Udvikling** – I finans og drift-infrastruktur kan du nu udvide løsningen og udvikle dine egne tilpasninger. Hver udvikler skal bruge deres eget udviklingsmiljø. Du kan finde oplysninger i [Implementere og få adgang til udviklingsmiljøer](../fin-ops-core/dev-itpro/dev-tools/access-instances.md).
- **GULD** – Til nye installationer er det en almindelig praksis at bruge et separat GOLD-miljø, der holdes uafhængigt af konfiguration og overflytning af data. Dette miljø kan bruges i hele implementeringen til at opdatere andre miljøer. Den bruges til at oprette et nyt produktionsmiljø med grundlæggende konfiguration og overflytning af data. Du kan ikke implementere et produktionsmiljø på finans og drift-infrastrukturen, før du har fuldført go-live-parathedsprocessen. Du kan finde flere oplysninger i [Klargøring til go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Når du overvejer dit miljø, anbefales følgende:
>
> - Brug dit standardmiljø til accepttest (tidligere Sandbox) eller et andet miljø til at udføre en genvej, før du går i gang.
> - Opbevar en detaljeret tjekliste for overgangen, som omfatter de enkelte datapakker, der skal bruges til at overflytte de endelige data til produktionsmiljøet i løbet af overgangen til udgivelsen. Denne anbefaling er især vigtig, hvis du ikke har et separat GOLD-miljø, hvor du kan lagre dine konfigurationer.
> - Brug dit standardmiljø til accept (tidligere Sandbox) eller et andet niveau 2-miljø eller et højere miljø som TEST-miljøet i hele projektet. Hvis du har brug for flere miljøer, kan organisationen købe dem for yderligere omkostninger.

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt

Når du vil bruge LCS til at administrere dine Human Resources-miljøer, skal du først oprette et LCS-projekt. Hvis du vil overføre personalemiljøet til finans og drift-infrastruktur, skal du oprette et nyt LCS-projekt til finansierings- og operationsapps. Hvis du allerede har et LCS-projekt til andre apps til finans og handlinger, kan du aktivere personalefunktionerne i arbejdsområdet til **funktionsstyring**. Få flere oplysninger i [Oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Når en ny kunde logger på Personale, omfatter abonnementet et arbejdsområde til implementeringsprojekt. Når kunden har aktiveret servicen, skal lejeradministratoren logge på <https://lcs.dynamics.com> ved hjælp af lejerkontoen. Projektarbejdsområdet oprettes automatisk for organisationen. Du kan finde flere oplysninger i [Lifecycle Services (LCS) til programmer til finans og drift](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md).

> [!NOTE]
> For at sikre en vellykket klargøring skal den konto, du bruger til klargøring af Human Resources-miljøet, enten tildeles rollen **Systemadministrator** eller **Systemtilpasser** i det Power Apps-miljø, der er tilknyttet Human Resources-miljøet. Se [Konfigurere brugersikkerhed for ressourcer](/power-platform/admin/database-security) for at få flere oplysninger om tildeling af sikkerhedsroller til brugere i Microsoft Power Platform.

Du skal fuldføre processen til start af LCS-projektet, før du kan begynde at implementere miljøer. Du kan finde flere oplysninger under [Projekt-onboarding](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md). Du kan finde flere oplysninger om, hvordan du bruger LCS, i [brugervejledningen til Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md).

## <a name="deploy-human-resources-environments"></a>Planlægge miljøer i Human Resources

Implementering af økonomi- og operationsapps, herunder Personale, i skyen, kræver, at du forstår miljøet og det abonnement, du implementerer på, hvem der kan udføre hvilke opgaver og hvilke data og tilpasninger, du skal administrere. Det anbefales, at du bruger en tjenestekonto i stedet for en navngivet bruger, når du implementerer nye miljøer. Du kan finde flere oplysninger om, hvordan du implementerer miljøer i infrastrukturen i finans og drift, i [Oversigt over implementering i skyen](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Du kan implementere et produktionsmiljø til Human Resources på finans og drift-infrastruktur, når du har fuldført go-live-parathedsprocessen. Du kan finde flere oplysninger i [Klargøring til go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md). Denne proces omfatter estimator for abonnement i LCS. Du kan finde flere oplysninger i [Abonnementsvurdering](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integrere Microsoft Power Platform med Human Resources

Microsoft Power Platform indeholder en række egenskaber til Dynamics 365-programmer via Power Platform Administration. Du kan integrere og udvide brugen af Human Resources-data ved hjælp af Microsoft Power Platform. Oplysninger om, hvordan du integrerer Personale med Microsoft Power Platform, finder du i [Microsoft Power Platform-integration med programmer til finans og drift](../fin-ops-core/dev-itpro/power-platform/overview.md).

## <a name="supported-geographies"></a>Understøttede geografier

Du kan finde oplysninger om de sprog og geografisk oplysninger, der understøttes i Human Resources, i [Global by design: Få mere at vide om lande og sprog, der understøttes](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet

Som standard har den globale administrator, der oprettede miljøet, adgang til det. Du skal eksplicit tildele andre programbrugere adgang. Du skal tilføje brugere og tildele dem de relevante roller i Human Resources-miljøet. Du kan finde flere oplysninger under [Opret nye brugere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Yderligere ressourcer
Du kan få mere at vide om, hvordan du bruger og administrerer projekter i LCS i programmet til finans og drift-infrastruktur ved hjælp af følgende ressourcer:

- [Ressourcer til Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Brugervejledning til Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Oversigt over selvbetjeningsinstallation](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Startside til handlinger til databaseflytning](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
