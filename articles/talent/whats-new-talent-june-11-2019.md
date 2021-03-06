---
title: Nyheder eller ændringer i Dynamics 365 Talent (11. juni 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20dc0768463d9a5d6762cb062deb0bdbe4d53fe3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528663"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (11. juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="search-engine-optimization-for-job-posts"></a>Optimering af søgemaskine for jobopslag

Når du har aktiveret **Optimering af søgemaskine** i Dynamics 365 Talent: Attract Administration, informerer Attract Google indekserings-API'et for at gennemsøge websiden, når du aktiverer og slår et nyt job op eller opdaterer et eksisterende job. På denne måde vil jobbet blive vist i søgeresultaterne på Google og andre søgemaskiner.

Når du ikke fjerner et jobopslag, imformerer Attract på samme måde indekserings-API'et, så jobbet, hvis opslag er blevet fjernet, ikke vises i søgeresultaterne.

> [!NOTE]
> Webcrawlers har ikke en defineret tidsramme til gennemsøgning af websider eller opdatering af søgeresultater.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Jobgodkendelser vises på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id'et, jobtitlen, andre godkendere og datoen, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig skal godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

De ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2337.

### <a name="platform-update-27-for-finance-and-operations"></a>Platform update 27 til Finance and Operations

Du kan finde yderligere oplysninger om Platform update 27 til Finance and Operations under [Funktioner i prøveversionen af Dynamics 365 Finance and Operations (juni 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Funktionsstyringsarbejdsområde i Talent

Arbejdsområdet **Administration af funktioner** i **Systemadministration** giver dig mulighed for at få vist, aktivere, deaktivere og planlægge funktioner, der er blevet leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet **Administration af funktioner** til at aktivere dem og få vist dokumentationen til dem.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

Det udstedende enhed understøtter nu brugerdefinerede felter.

### <a name="new-common-data-service-entities"></a>Nye Common Data Service-enheder

Enheden Opgavegruppe er blevet tilføjet.

## <a name="in-preview"></a>Som eksempel

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Visningsfunktioner vil kun blive aktiveret i sandkassemiljøer

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er Produktion eller Sandkasse. Sandkasse-forekomsttypen giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Få vist udvidede oplysninger om rapportperformance i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye fornyede gennemgange. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede.

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Medarbejdere, ledere og personaleafdelingen kan udskrive en medarbejders performancegennemgang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]