---
title: Ofte stillede spørgsmål om fletning af Dynamics 365 Human Resources-infrastruktur
description: Denne artikel besvarer ofte stillede spørgsmål om fletningen af infrastruktur for Microsoft Dynamics 365 Human Resources og programmer til finans og drift.
author: twheeloc
ms.date: 08/13/2021
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
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203193"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Ofte stillede spørgsmål om fletning af Dynamics 365 Human Resources-infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Hvad er Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources leverer værktøjer, der kan hjælpe personaleteam med at øge organisationens fleksibilitet, transformere medarbejdernes erfaring og optimere personaleprogrammer for at oprette en arbejdsplads, hvor medarbejdere og virksomheden kan blive ansat. Du kan finde flere oplysninger om Dynamics 365 Human Resources i [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Transformere medarbejdererfaringer.** Fastholdelse af de bedste medarbejdere ved at styrker ledere og medarbejdere via connectede selvbetjeningserfaringer, der er med til at skabe ansættelse og vækst.
- **Optimer HR-programmer.** Reducer driftsomkostningerne, og opret medarbejderfokuseret orlov og fravær, tid, gode og kompensationsstyringsprogrammer.
- **Øg organisationsuligheden.** Gør HR i stand til at arbejde med den færdighed, som virksomheden har brug for, ved at bruge Dataverse og Microsoft Power Platform til at centralisere persondata, så de nemt kan udvide Dynamics 365 Human Resources.
- **Få indsigt i arbejdsstyrken.** Foretag databaserede beslutninger ved hjælp af muligheden for at analysere og visualisere persondata på detaljerede dashboards, der er tilgængelige på alle enheder.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Værdi og fordele ved infrastrukturens fletning

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hvad er fletning af Dynamics 365 Human Resources-infrastruktur?

Der er i øjeblikket to separate grupper af personalefunktioner i to forskellige infrastrukturen i Dynamics 365:

- **Dynamics 365 Human Resources** – En uafhængig app, der kører på en uafhængig infrastruktur. Da denne app blev sendt, blev infrastrukturen adskilt fra andre apps til Dynamics 365-handlinger. Vores kunder bruger denne app til at øge forståelsen af organisationen, optimere HR-programmer, transformere medarbejdererfaringer og få indsigt i arbejdsstyrken.
- **HR-modul** – Et ældre sæt egenskaber, der tidligere var en del af SKU (Unified Operations licensing stock keeping unit). HR-modulet kører på den finans og drift-infrastruktur, hvilket er det samme på tværs af alle operationsapps. Disse apps inkluderer Dynamics 365 Finance, Dynamics 365 Project Operations og Dynamics 365 Supply Chain Management. Kunder fik HR-funktionerne som en del af Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

I løbet af de seneste tre år har Microsoft ikke føjet nye egenskaber eller forbedringer til personalemodulet. I stedet har vores investeringsaktiver fokuseret på Dynamics 365 Human Resources-appen.

Hvis disse to egenskaber bliver sporet på samme infrastruktur, kan vi hjælpe kunder med at få følgende fordele:

- Forbedringer, der er blevet føjet til Dynamics 365 Human Resources de seneste tre år, herunder forbedret orlovs- og fraværsstyring og -rapportering.
- Forbedret udvidelse via Microsoft Power Platform og muligheden for at udvide forretningslogik til at personalisere sider.
- Forbedret udrulning, forbedrede opdateringer og vedligeholdelse, der er vedvarende i form af Application Lifecycle Management (ALM), Lifecycle Services, geografisk tilgængelighed og meget mere.
- Mere effektiv, efterhånden som vores teknikerteam bruger delte tjenester, værktøj og reducerede platformomkostninger.

Denne overførsel påvirker kunder, som aktuelt bruger enten Dynamics 365 Human Resources eller det ældre HR-modul.

## <a name="glossary-of-terms-used-in-this-faq"></a>Ordliste til begreber, der bruges i denne Ofte stillede spørgsmål

- **Dynamics 365 Human Resources** – Vores aktuelle og fremtidige produkt, der tilbyder HR-egenskaber på markedet.
- **HR-modul** – Et ældre sæt egenskaber, der tidligere var licenseret med Unified Operations-tilbud. Egenskaberne aktiveres, når en kunde ejer Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.
- **Finans og drift-infrastruktur** – Den udviklingsarkitektur, der bruges af operationerne, herunder Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. Denne infrastruktur er den, der vil blive brugt fremadrettet. I denne Ofte stillede spørgsmål henviser termen *flettet infrastruktur* til finans og drift-miljøet.
- **Human resources-infrastruktur –** Den udviklingsarkitektur, der tidligere er brugt til Dynamics 365 Human Resources-appen. Fletningen af infrastrukturen placerer Dynamics 365 Human Resources i samme infrastruktur som finans og drifts. Den selvstændig infrastruktur afbrydes ikke.

## <a name="general-questions-about-the-infrastructure-merge"></a>Generelle spørgsmål om fletningen af infrastrukturen

### <a name="will-customers-lose-any-features-or-capabilities"></a>Mister kunder nogen funktioner eller egenskaber?

Vores målsætning er at minimere den effekt, denne overførsel har på kunder. Vi fjerner ikke nogen funktioner eller egenskaber. Der vil være funktionel paritet mellem Dynamics 365 Human Resources og HR-modulet. Hvis der findes en funktion i begge infrastrukturen, anvendes Dynamics 365 Human Resources-erfaringen.

### <a name="will-the-user-experience-change"></a>Vil min brugeroplevelse ændre sig?

Brugeroplevelsen vil være konsistent med standardoplevelsen i Dynamics 365-platformen. Selvom den generelle erfaring for dashboardet og menuerne stadig er den samme, vil den blive tilpasset den almindelige oplevelse i Dynamics 365 Finance-app. Navigation inkluderer både moduler og arbejdsområder, giver mulighed for foretrukne med mere. Arbejdsområderne Dynamics 365 Human Resources, f.eks. **Personalestyring** og **Personer**, flettes sammen med den økonomiske og driftsmæssige infrastruktur. I fremtiden vil nye egenskaber blive leveret via Funktionsstyring, som giver kunderne mulighed for at se nye funktioner og bestemme, hvilke funktioner de vil bruge. Yderligere oplysninger finder du i [oversigt over funktionsstyring](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og [dokumentation til brugergrænsefladen](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Hvornår skal Dynamics 365 Human Resources-infrastrukturfletning være fuldført?

Infrastrukturen vil blive rullet ud i faser, så kunderne får tid til at planlægge og udføre de nødvendige trin. Vi begyndte at få udrullet egenskaber i Dynamics 2021-udgivelsesbølge 2. Vi planlægger at fuldføre alle produktudviklingsindsatser for dette projekt ved udgangen af 2022 udgivelsesbølge 2. Bemærk, at tidslinjer kan ændres. De fleste opdaterede oplysninger findes i [udgivelsesplanerne](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Hvilken uddannelse og hvilke ressourcer er tilgængelige som hjælp i infrastrukturfletning?

Der leveres dokumentation, som beskriver hvert enkelt trin i infrastrukturfletteprocessen i detaljer. Vi vil levere yderligere uddannelsesressourcer, som f.eks. kursusressourcer, alt efter hvad der er nødvendigt for at hjælpe kunder og partnere med en problemfri overførsel.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Vil der ske ændringer i udviklingsfunktionerne, når infrastrukturfletningen er fuldført?

Du kan få mere at vide om udviklingsegenskaber i [Startside for udvikling og tilpasning](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Spørgsmål om tilgængelighed af funktioner

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Vil integrationen af LinkedIn Talent Hub fungerer i finans og drift-infrastruktur?

Nej, LinkedIn Talent Hub-integrationen bliver ikke en del af den sammenflettede infrastruktur. Public Application Programming Interface (API'er) er tilgængelige til integration med sporingsløsninger til rekruttering og ansøgere. Kunder, der planlægger at bruge LinkedIn Talent Hub, skal samarbejde med deres Microsoft-partner for at blive integreret ved hjælp af de leverede API'er. Yderligere oplysninger om ATS-integrations-API'er [(Applicant Tracking System) finder du i introduktionen til API-systemet for ansøgere](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Vil de egenskaber, der aktuelt kun er tilgængelige i Dynamics 365 Human Resources (f.eks. orlovsstyring og styring af goder) være tilgængelige, når fletningen er fuldført?

Ja. Alle Dynamics 365 Human Resources-programegenskaber kommer til finans- og operationsinfrastrukturen. Funktionerne gøres tilgængelige i en trinvis tilgang. Hvis du vil have opdaterede oplysninger om den flettede infrastrukturs tilgængelighed med funktioner, kan du jævnligt gennemse [frigivelsesplanerne](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Vil Ceridian-integration med Dynamics 365 Human Resources være tilgængelig, når infrastrukturfletningen er fuldført?

Ceridian er ved at oprette en V2-integration med Dynamics 365 Human Resources, der benytter løn-API'erne. Den filbaserede integration, der aktuelt findes i Dynamics 365 Human Resources, overføres ikke til finans og drift-infrastrukturen. Du kan finde flere oplysninger i [Introduktion til Løn-API](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Medtages ansøgersporing eller -onboarding/offboarding af medarbejderens funktioner?

I tidligere versioner har vi oprettet ATS Integration API for at sætte partnere og kunder i stand til at oprette ATS-integration med Personale. Yderligere ATS-relaterede funktioner blev tilgængelige i 2022 meter 1. Vi vil fortsætte med at forbedre disse API'er i fremtidige versioner.

Den personalefunktionalitet, der aktuelt findes i infrastrukturen i finans og drift, omfatter nogle rekrutteringsstyringsfunktionaliteter, der ikke findes i Dynamics 365 Human Resources. Når infrastrukturfletningen er fuldført, er denne funktionalitet tilgængelige for alle Human Resources-kunder. Denne funktionalitet giver lightweight ATS-funktionalitet. Vi planlægger dog ikke at udvide denne funktionalitet i fremtiden. Kunder, der har brug for mere avancerede funktioner, kan få fordel af integration med ATS. Yderligere oplysninger om ATS-integration af API'er findes i [Applicant Tracking System-integration til API-introduktion](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Vil de Dynamics AX 2012-opgraderingsværktøjer, der i øjeblikket er tilgængelige, blive brugt til opgradering af HR-modulet i AX 2012 til Dynamics 365 Human Resources-app?

Ja. Opgrader fra Dynamics AX 2012 til Dynamics 365 Human Resources vil bruge samme opgraderingssti og -værktøj, som bruges til at opgradere til den seneste version af andre Dynamics 365 rift-apps, f.eks. Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.

Du kan finde flere oplysninger om overflytningen til finans og drift-infrastrukturen i [Human Resource-kundemigration, ofte stillede spørgsmål](./customer-migration.md).
