---
title: Nyheder eller ændringer i Dynamics 365 for Talent (25. juni 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e32768c898e2934b95eb8ab7b212337aff0c1556
ms.sourcegitcommit: fbe6d35ed35aa01f438990e2880c3a3cf223ea8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/27/2019
ms.locfileid: "1704463"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-25-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (25. juni 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Kommer snart i Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Jobgodkendelser vises på startsiden

Godkendelser vises i området **Godkendelser** på dashboardet. Godkendere kan gennemse deres godkendelser under **Tildelt til dig**, som viser job-id'et, jobtitlen, andre godkendere og datoen, hvor jobbet blev tildelt. Brugere, der sender et job til godkendelse, kan gennemse deres job under **Anmodet af dig**, som viser de godkendere, der stadig skal godkende det sendte job.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Der vises en forkert værdi for den primære stilling (314266)

Disse ændringer vil konsekvent vise indstillingen **Primær stilling** på alle sider.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Kan ikke redigere efter tilbagekald af arbejdsgangen i gennemsyn (318180)

Gennemgang, der er tilbagekaldt via arbejdsgangen, kan nu redigeres.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Feltet for endelige kommentarer under gennemgange oversættes ikke (325921)

Etiketten **Endelige kommenaterer** oversættes i Talent.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Visningsfunktioner vil kun blive aktiveret i sandkassemiljøer

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er **Produktion** eller **Sandkasse**. **Sandkasse**-forekomsttypen giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til **Produktion**-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til **Sandkasse**-forekomsttypen, skal du kontakte [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Som eksempel

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begræns orlovstyper i anmodninger om fridage

Organisationer kan tilbyde mange typer orlov til medarbejdere. Det kan dog være hensigtsmæssigt, at medarbejderne ikke sender anmodninger om fritid for nogle orlovstyper. Disse orlovstyper administreres muligvis af personaleafdelingen. I denne version kan du konfigurere, hvilke orlovstyper medarbejdere kan sende anmodninger om fritid for. 

## <a name="coming-soon-in-core-hr"></a>Kommer snart i Core HR

### <a name="feature-management-area-in-talent"></a>Funktionsstyringsområde i Talent

**Funktionsstyring** vil blive fjernet fra **Systemadministration**  på grund af problemer med funktionen. Vi introducerer **Administration af funktioner** igen i en fremtidig version. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Understøttelse i Common Data Service-enheden af brugerdefinerede felter

Følgende enheder understøtter brugerdefinerede felter: **Lønkoder**, **Fastløn-hændelse** **Kompensationsgitter**, **Lønperiode** og **Kompensationsreferencepunkt**. 

### <a name="new-common-data-service-entities"></a>Nye Common Data Service-enheder

Enheden **Årsagskoder** føjes til Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Få vist performanceoplysninger for direkte og udvidede underordnede i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye fornyede gennemgange. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede.

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Medarbejdere, ledere og personaleafdelingen kan udskrive en medarbejders performancegennemgang.